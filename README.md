Збир игри
============
<img src="http://i.imgur.com/BWdVBEm.png?1" alt="pocetna" align="left" ></img>
Она што ние го направивме е апликација која во себе содржи четири игри. Тоа се игрите : </br>
<ul>
<li>Повторување;</li>
<li>Змија;</li>
<li>Милионер;</li>
<li>Камен ,лист, ножици</li>
</ul>


<p align="justify">Повторување е симулација на играта позната како Simon (www.freesimon.org) .  Змија е симулација на играта Snake (http://playsnake.org/).  Милионер е симулација на квизот „Кој сака да биде Милионер“. Камен, лист, ножици е симулација на истоимената детска игра.</p>
  </br></br>
<h3>Змија</h3>
<hr>

<p align="justify">
<img src="http://i.imgur.com/lJ0hbmN.png?1" alt="snake" align="right" ></img>
Змија е симулација на познатата игра Snake. Со стрелките на тастатурата одредуваме во кој правец да се движи змијата (горе,
доле, лево или десно) и не смее да удри во ѕидот. На површината има една крофна и змијата треба да ја изеде. Кога ќе ја изеде на друго место се појавува друга крофна, а должината на змијата се зголемува. Имаме имплементирано 4 класи. Krofna класата содржи
координати на крофната и слика. Во конструкторот се иницијализира положбата на крофната, а во методот Draw се исцртува крофната.
Класата Krug има само конструктор кој ги иницијализира координатите на кругот. Класата Zmija содржи листа од кругови
(List<Krug>). Има еден void метод addCircle() кој додава нов круг на листата од кругови. Во SnakeGame класата чуваме информации
за насоката на змијата, инстанци од класите Zmija иKrofna, брзина и поени. Во конструкторот додаваме на змијата три кругови и
крофната ја иницијализираме на рандом позиција. Во методот NovaKrofna се создава нова крофна со рандом позиција, а во методот
setDir ја одредуваме насоката според притиснатите копчиња од тастатура. Во главната форма имаме метод pictureBox1_Paint којшто
ја исцртува змијата на секој интервал од тајмерот, а во методот timer_tick се повикува претходниот метод и проверува дали
играчпт удрил во ѕид или ја изедил опашката, или победил.</p>
</br></br></br>
<h3>Повторување</h3>
<hr>

<p align="justify">Повторување е едноставна игра на меморија. <img src="http://i.imgur.com/NtCXhPa.png?2" alt="simon" align="left" margin="5px"></img>Имаме дадена низа од четири бои кои играчот треба да ги погоди и при секоја итерација низата се зголемува за една боја. Идејата ја добивме од интернет, додека целиот код е напишан од нас. Имаме една класа SimonGame во која што имаме низа од стрингови (боите) и моментален индекс (до каде точно има додавано бои во низата). Во конструкторот се создава нова низа. Имаме еден метод addNiza којшто додава рандом боја во низата. Во главната форма имаме четири копчиња, секое со соодветна боја. Имаме методи за клик на секое од копчињата, кој проверува дали сме ја погодиле бојата од низата. При секоја итерација на тајмерот соодветно се прикажува следната боја од низата на секое од копчињата. Играта е победена доколку играчот погоди 20 бои по ред.
</p>
</br></br></br></br></br></br></br>
<h3>Камен, лист, ножици</h3>
<hr>

<p align="justify"><img src="http://i.imgur.com/7uGWjzT.png?1" alt="rock" align="right"></img>
Камен, лист, ножици е симулација на една едноставна игра која сите сме ја играле кога сме биле мали. Оваа игра се игра меѓу корисникот и компјутерот. Одбирате помеѓу камен, лист и ножици, а  истовремено и компјутерот одбира едно. Сега, победникот се бира според следните правила: Каменот ги крши ножиците. Ножиците го сечат листот. Листот го прикрива каменот.
Оваа игра е имплементирана во самата форма. Содржи листа(List<String>) во која се чуваат резултатите од играњето, Boolean променлива преку која проверуваме кој е на ред да избере . Корисникот избира едно од трите понудени – камен, лист или ножици на тој начин што клика на една од сликите прикажани. Тие слики всушност се копчиња и кога ќе кликне корисникот на било кое од нив, се обработува настанот Click. Во Click настанот на секое од трите копчиња е направено да се прикаже сликата која ја избрал корисникот, да се повика методот за избор на компјутерот, изборот на компјутерот се прикажува во соодветната лабела, во лабелата за резултат се прикажува тековниот резултат и во листата со резултати се додава и прикажува тековниот резултат. Методот за избор на компјутерот ја избира сликата на компјутерот така што со помош на Random  се избира еден број од 0,3 и според него се се добива избраната слика. На копчето Ресетирај, се бришат сите  досегашни резултати. На копчето Затвори прозорец , се враќаме на првичната форма.
</p>
</br></br></br>
<h3>Милионер</h3>
<hr>
<p align="justify"> <img src="http://i.imgur.com/f4XkWwy.png?2" alt="milioner" align="left"></img> 
Оваа игра има класа Prasanje која ги содржи податоците за текстот на прашањето(string), точниот одговор(string), категорија на прашањето(string – бидејќи има три сигурни суми, потребно ни е да имаме прашања од три категории : лесни, средни и тешки) , листа од понудени одговори(List<String>). Исто така, имаме  и класа MilionerGame која содржи листа од прашања (List<Prasanja>), и три листи од броеви на лесни, средни, тешки прашања.  Во оваа класа има метод izgenerirajPrasanja(), кој во секоја од листите генерира по пет прашања во зависност од категоријата, тоа го прави со помош на Random. Прашањата ги вади од листата со прашања и ги групира според категоријата. Исто така, оваа класа има и метод addQuestion(), кој додава прашање во листата со прашања. Имаме и класа dodadiBazaPrasanja() во која се додаваат сите прашања како објекти од класата Prasanje vo класата MilionerGame. 
Овде, освен главната форма имаме и помошна форма која се отвара кога корисникот ќе кликне на Повикај пријател. 
Играта е симулирана на тој начин што откако ќе се започне играта со клик на копчето Нова Игра, се генерираат 15 прашања за корисникот . Доколку корисникот одговори точно на прашањето, се брише првиот елемент од листата на соодветната категорија и со клик на следно прашање се прикажува следнито прашање. При секое одговорено прашање се поместува индексот на листата со суми за еден.  Доколку одговорите грешно, играта завршува.
</p> 
</br></br></br>
<h3>Опис на метод</h3>
<hr>
</br></br>
<p align="justify"> Овој метод се наоѓа во ZmijaForm и со него се исцртува движењето на змијата. Најпрво се исцртува храната (крофната). Потоа се проверува дали координатите на крофната се поклопуваат со координатите на главата на змијата. Ако се поклопуваат тоа значи дека змијата ја изедила крофната и се генерира нова крофна на рандом позиција, се зглемува должината на змијата и се зголемуваат поените на играчот. Следно ја проверуваме насоката на движење на змијата. Ако се движи на десно ја исцртуваме главата со црна боја со зголемена X координата, ја зачувуваме претходната состојба и соодветно ја зголемуваме координатата. Истото се прави и за другите насоки. Потоа со еден for циклус се исцртува остатокот од змијата со црвена боја со што вториот круг од змијата се исцртува на претходната позиција каде што била главата, третата на втората итн. При секоја итерација се чува состојбата на претходниот круг од змијата.</p>
<p>
<pre>
private void pictureBox1_Paint(object sender, PaintEventArgs e)
        {
            Graphics g = e.Graphics;
            game.food.Draw(g);

            if ((game.snake.snake[0].X == game.food.X && game.snake.snake[0].Y == game.food.Y))
            {
                game.snake.addCircle();
                game.NovaKrofna(g);
                game.Poeni++;
                flag = true;
            }
            Brush b;
            if (game.dir == SnakeGame.Direction.Right)
            {
                g.FillEllipse(Brushes.Black, game.snake.snake[0].X + 20, game.snake.snake[0].Y, 20, 20);
                prevX = game.snake.snake[0].X;
                prevY = game.snake.snake[0].Y;
                game.snake.snake[0].X += 20;
            }
            else if (game.dir == SnakeGame.Direction.Down)
            {
                g.FillEllipse(Brushes.Black, game.snake.snake[0].X, game.snake.snake[0].Y + 20, 20, 20);
                prevY = game.snake.snake[0].Y;
                prevX = game.snake.snake[0].X;
                game.snake.snake[0].Y += 20;
            }
            else if (game.dir == SnakeGame.Direction.Left)
            {
                g.FillEllipse(Brushes.Black, game.snake.snake[0].X - 20, game.snake.snake[0].Y, 20, 20);
                prevY = game.snake.snake[0].Y;
                prevX = game.snake.snake[0].X;
                game.snake.snake[0].X -= 20;
            }
            else if (game.dir == SnakeGame.Direction.Up)
            {
                g.FillEllipse(Brushes.Black, game.snake.snake[0].X, game.snake.snake[0].Y - 20, 20, 20);
                prevY = game.snake.snake[0].Y;
                prevX = game.snake.snake[0].X;
                game.snake.snake[0].Y -= 20;
            }
            for (int i = 1; i &lt; game.snake.snake.Count; i++)
            {

                b = Brushes.Red;
                g.FillEllipse(b, prevX, prevY, 20, 20);
                float tempx = prevX, tempy = prevY;
                prevX = game.snake.snake[i].X;
                prevY = game.snake.snake[i].Y;
                game.snake.snake[i].X = tempx;
                game.snake.snake[i].Y = tempy;

            }
}}

</pre></p>

