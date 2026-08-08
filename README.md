# 313TGVS

# Argumentum

Argumentum este un proiect experimental pentru organizarea și analizarea ideilor sub forma unui grafic interactiv de argumente.

În loc să prezinte o discuție ca pe o listă obișnuită de texte, proiectul o transformă într-o structură vizuală în care fiecare idee poate deschide noi ramuri: argumente, contraargumente, răspunsuri, obiecții, concluzii și idei secundare.

Cum funcționează

La început este afișat un singur nod principal. Acesta reprezintă premisa sau întrebarea de la care pornește analiza.

Prin apăsarea unui nod, se deschide următorul nivel al graficului. Fiecare nod poate avea la rândul său alte noduri, astfel încât structura poate continua pe cât de multe niveluri este nevoie.

Fiecare tip de idee are propria culoare:

- 🔵 Argument
- 🟥 Contraargument
- 🟢 Răspuns
- 🟡 Idee / Context
- 🟣 Idee nouă
- ⚪ Premisă
- 🔴 Obiecție

Nodurile sunt conectate vizual, iar utilizatorul poate deplasa întregul grafic și poate face zoom pentru a urmări ramurile mai mari.

Structura datelor

În momentul de față, conținutul este păstrat într-un singur obiect JavaScript. Fiecare nod poate conține:

{
    text: "Ideea",

    type: "Argument",

    color: "blue",

    children: [
        {
            text: "Contraargument",
            type: "Contraargument",
            color: "burgundy",
            children: []
        }
    ]
}

Important este sistemul "children". Un nod poate avea copii, iar acei copii pot avea la rândul lor alți copii. În felul acesta, graficul nu are o limită practică de adâncime.

Direcția proiectului

Argumentum este încă în dezvoltare. Ideea este ca proiectul să evolueze dintr-un simplu grafic într-un spațiu în care o dezbatere întreagă poate fi construită și explorată vizual.

Printre direcțiile pe care le văd pentru proiect:

- categorii și subiecte separate;
- salvarea graficelor;
- posibilitatea de a adăuga noduri direct din interfață;
- editarea și ștergerea argumentelor;
- căutare în interiorul unui grafic;
- mai multe tipuri de relații între idei;
- surse și referințe atașate argumentelor;
- posibilitatea de a deschide și partaja un anumit grafic;
- export și import de structuri;
- colaborare între mai mulți utilizatori;
- istoricul modificărilor;
- o interfață mai apropiată de o tablă vizuală, unde ideile pot fi mutate și reorganizate liber.

Pentru moment, proiectul rămâne într-un singur fișier HTML, tocmai pentru a fi ușor de modificat, testat și rulat direct în browser.

Argumentum nu încearcă să spună care argument este adevărat. Scopul este să facă structura unei argumentări mai ușor de văzut, urmărit și analizat.