### React Tic Tac Toe Game

#### 🎈Calculate Winner Logic :
```js
 const winner = calculateWinner(counters);
  let status = "";
  if (winner) {
    status = "Winner : " + winner;
  } else {
    status = "Player : " + (xIsNext ? "X" : "O");
  }

  return (
    <>
      <div className="title">
        <Header />
        <div className="board">
          <div className="status">{status}</div>
          <Square value={counters[0]} onCounterClick={() => handleClick(0)} />
          <Square value={counters[1]} onCounterClick={() => handleClick(1)} />
          <Square value={counters[2]} onCounterClick={() => handleClick(2)} />
          <Square value={counters[3]} onCounterClick={() => handleClick(3)} />
          <Square value={counters[4]} onCounterClick={() => handleClick(4)} />
          <Square value={counters[5]} onCounterClick={() => handleClick(5)} />
          <Square value={counters[6]} onCounterClick={() => handleClick(6)} />
          <Square value={counters[7]} onCounterClick={() => handleClick(7)} />
          <Square value={counters[8]} onCounterClick={() => handleClick(8)} />
          <a href="https://zumpy.rozistudio.com/game/"><button className="restart">Restart</button></a>
        </div>
      </div>
    </>
  );
};

export default Board;

const calculateWinner = (counters) => {
  const lines = [
    [0, 1, 2],
    [3, 4, 5],
    [6, 7, 8],
    [0, 3, 6],
    [1, 4, 7],
    [2, 5, 8],
    [0, 4, 8],
    [2, 4, 6],
  ];

  for (let i = 0; i < lines.length; i++) {
    const [a, b, c] = lines[i];
    if (counters[a] && counters[a] === counters[b] && counters[c]) {
      return counters[a];
    }
  }
  return false;
};

```

### Thank You 🎇
