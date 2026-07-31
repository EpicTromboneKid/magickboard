# magickboard
Chessboard that can move its own pieces!
It relies on a corexy gantry under the hood and an EPM (electropermanent) magnet to hold state without power, while looking like a normal chessboard with a 40mm height.

i was looking at the feasibility of a 5 bar linkage for this, but unfortunately, while the 5 bar is faster, it requires a much larger margin on all sides, so i'll stick with corexy
- however, i don't want to service it that often, so i'll have to look at steel-reinforced belts or something similar
- it'll use an epm for basically no power draw while idle (alnico can be flipped with a current spike, permanent nd magnet)
- rfid tags embedded in each square? we'll see if the magnet interferes in the first prototype
- can communicate with the lichess API (since unfortunately, chess.com does not seem to have a public-facing eboard API)
- looks like a normal wood board when not in use (i.e. all display elements are UNDER wood and not using a normal oled screen)
- supports chess960 and other variants that can be played OTB
- also voice controls
physical dimensions
- i want it to be as close to a tournament set as possible, including the pieces and board
- this means a 50x50cm board area with 5x5cm squares and a 9.5 cm king.
- while the playable area is 50x50, i'd probably like a margin of ~7cm on all sides, and one side with the controls and game timer (automatic)
- preferably also <2in thickness
challenges:
- i need to see if the rfids are embeddable in the squares themselves, and i'll probably use fiberglass to back the bottom so it's rigid even if someone ragequits
- does an epm even work here?? will it be able to handle everything
- also how loud will this be?
- i need to make a 4x4 prototype for this with off-the-shelf parts (most likely just cheap 3d printer things)
- for the prototype, i'll just use cardboard or someting similar where i can slip the rfid tags into the center without much effort and then use a good wood like maple or cherry for the actual board
- brains will probably be nrf52840 (since it has bt support), and i haven't decided if i want the ai running fully locally on the chessboard (which means it would need a pretty beefy processor+ram) or if i want to have it run over bt connected to my phone
