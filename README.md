
# Stockfish
cd src
make -j build ARCH=x86-64-modern

# Cute Chess
./bin/cutechess-cli -openings file=openings/modern-defense.pgn order=random -draw movenumber=40 movecount=4 score=8 -resign movecount=4 score=500 -concurrency 1 -engine cmd=Stockfish/src/stockfish -engine cmd=Stockfish/src/stockfish -each proto=uci trust option.Threads=14 option.SyzygyPath=share/tablebase-syzygy/ option.Hash=3584 depth=40 st=2 timemargin=100 -rounds 1 -pgnout test-1.pgn fi
