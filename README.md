Pokemon
=======
Целта на нашата семинарска работа е да направиме апликација која ќе имплементира една од најпознатите три за Nintendo 3DS, а тоа е играта Pokemon. Нашата идеа е да претставиме дел од можностите или функционалностите во играта Pokemon, односно ќе бидат имплементирани можноста за креирање на сопствен аватар, избирање на сопствен почетен Pokemon, едноставна навигација низ мапата при што е овозможена битка помеѓу Pokemoni од различни области, купување на нови Pokemoni кои ќе ти бидат од корист за победување на Pokemoni-те од наредните стази кои се се потешки се победување. Дополнително ќе имаме и мала игра наменета за собирање на поени, односно пари, се со цел да се олесни купувањето на појаки Pokemoni.
Идеата за играта ја измисливме сами, направивме целосна замисла за изгледот на апликацијата.

<img src="https://fbcdn-sphotos-b-a.akamaihd.net/hphotos-ak-frc3/t1.0-9/q71/s720x720/10171007_863618393665260_9047700993413522808_n.jpg" alt="HowToPlay Screen"/> </li>
Во кодот има имплементации на класи за Pokemon, Avatar(Trainer), Animations, Attack..(na Marijana)
Класата Animations е основната класа која ја користиме за доловување на анимацијата за движењата на Pokemoni-те, како и нивните меѓусебни напаѓања. Таа се состои од поле од Bitmaps и нивни редни броеви. За имплементација на овие движења го користиме методот GiveNextImage() со кој редоследно се исцртуваат сликите.
Следната класа, класата Attack, е задолжена за реализација на нападите на Pokemoni-те. Таа се состои од име на нападот, како и вкупно 18 типови на напади: Normal, Big, Dark, Dragon, Electric, Fairy, Figurry, Fire, Flyry, Ghost, Gross, Ground, Ice, Poison, Psychic, Rock, Steel и Water така што при битката помеѓу два Pokemoni од различен тип ќе играат огромна улога заради предностите и слабостите на Pokemoni-те. Следен параметар во класата Attack е Damage или сила на нападот, Effect – опис на нападот, Opponent кој кажува дали нападот се извршува врз противникот, и последниот параметар од оваа класа е Animacija кој го користиме за визуелно претставување на нападот врз противникот.
Следната класа е Pokemon. Доста важна класа затоа што во неа се претставуваат главните херои во играта. За секој Pokemon се дефинирани следните параметри: име на Pokemon-от, тип, следи параметарот кој ги опишува предностите на дадениот Pokemon параметарот StrongAdjust, односно ги опишуваме предностите на еден Pokemon врз друг. Спротивно на овој е параметарот Weakness. Следи параметарот LifePoints, овие поени се всушност јачината на Pokemon-от, пославите Pokemoni имаат помалку LifePoints па затоа се полесни за победување. Тука чуваме и листа од класата Attack, односно секој Pokemon има по 4 напади предефинирани за него кои најчесто се од ист тп како и Pokemon-от. Параметарот AnimacijaPokemon е всушност објект од Animations и го корстиме за изгледот и движењето на Pokemon-от. Последен е параметарот CenaPokemonкој како што кажува името е цената на Pokemon-от кој ќе биде достапен во Pokemon Shop – продавницата за Pokemon.
Следната класа Trainer претставува класа за Аватарот. Нејзини параметри се :  име(Name) на аватарот, Gender – машки или женски, кој се избира на почетокот на играта, Money – парите со кои располагаме во моментот. Потоа, оваа класа има четири параметри од типот Image. Аватарот има листа од класата Pokemon, така што секој trainer може да има колку што сака Pokemoni и какви што сака. И последниот параметар е листа од тип bool – Leveli кој ни покажува кои стази ти има отворено карактерот, односно на кои места го има победено противникот
