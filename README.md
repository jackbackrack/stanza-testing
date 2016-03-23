# stanza-testing
stanza testing inspired by junit

# examples

    deftest char-test :
      var char = 'a'
      val char-prop = CharProp({ char }, { char = _ }, 1, 'a', 'c')
      assert-equal(pull(char-prop), 'a', "C0")
      assert-equal(push(char-prop, 'b'), 'b', "C1")
      assert-equal(incr(char-prop), 'c', "C2")
      assert-equal(decr(char-prop), 'b', "C3")

    defn main () :
      run-all-tests()

    main()
