# Spec TicTacToe

  ## game.rb
    ### Game.tictactoe
      #### On s'attend que la méthode tictactoe fasse appel à Game.new
        ##### On s'attend que la méthode Game.new fasse appel à la méthode Board.new pour la création de @board
        ##### On s'attend que la méthode Game.new fasse appel à la méthode Player.new 2 fois 
        ##### On s'attend à ce que la méthode Game.new fasse appel à la méthode @board.show
      #### On s'attend à ce que la méthode game_on soit appelée
        - Tester que la partie respond_to à la méthode
    ### Game.game_on
      - Tests avec boucle pour vérifier l'incrémentation des turn
      #### On s'attend que la méthode game_on appelle Position.new
      #### On s'attend que la méthode game_on appelle ask(position, current_player)
        ##### On s'attend que la méthode ask appelle current_player(turn)
      #### On s'attend que la méthode game_on appelle play
        ##### On s'attend que la méthode play appelle current_player(turn)
      #### On s'attend que la méthode game_on appelle someone_winning?
        ##### On s'attend que la méthode someone_winning? appelle current_player(turn)
          - Si someone_winning? est true la boucle s'arrête et on teste le texte de victoire
      #### On s'attend que la méthode game_on appelle show_board
      #### On s'attend que la méthode game_on appelle print_endgame
    ### Game.current_player(turn)
      #### Alternance des players
        - Tester l'alternance
    ### Game.ask(position, player_name)
      #### Le tour du joueur
        ##### On s'attend que la méthode ask appelle Position.from_string
          - Tester que la méthode appelée le soit avec les bons attributs
        ##### On s'attend que la méthode ask appelle Board.valid?
          - Tester que lorsque board.valid? is true la boucle s'arrête
    ### Game.play(position, player_mark)
      #### On s'attend que la méthode play appelle @board.set
    ### Game.someone_winning?(board)
      - Tester chacune des conditions de victoire
    ### Game.show_board
      - Tester la présence de la phrase
      #### On s'attend que la méthode show_board appelle @board.show
    ### Game.print_engame
      - Tester la présence de la phrase
  ## board.rb
    ### Board.new
      - Tester le contenu de l'array
    ### Board.set(mark, position)
      - Raise error si la marque est autre chose que "0" ou "X"
      - Raise error si la position a déjà été jouée
      - Tester la position pour voir si la marque y a été mise
    ### Board.get(position)
      - position be_truthy
    ### Board.win?
    ### Board.valid?(position = Position.new)
      #### fait appel à la méthode get pour appeler la bonne valeur dans l'array du board
      - Tester la validité de plusieurs position
    ### Board.show
  ## player.rb
    ### Player.new
      - Tester l'erreur
      - Tester @@count après création de player
      - Tester les string
  ## position.rb
    ### Position.new
    ### Position.from_string(string)
      - Tester la condition unless
      - Tester les valeurs @row et @col
    ### Position.nil?
      - Tester le résultat avec différentes entrées
    ### Position.to_s