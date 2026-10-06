# OS egzamino pasiruošimas / OS exam prep (Ubuntu)

Kiekviename skyriuje (`NN_Tema/Potemė/uzduotis_atsakymai.txt`) – užduoties
punktai iš .docx failų, prie kiekvieno: komanda(-os), paaiškinimas lietuviškai
(LT) ir angliškai (EN).

Each topic folder (`NN_Topic/Subtopic/uzduotis_atsakymai.txt`) holds the
assignment tasks from the .docx files, each with the command(s) and an
explanation in Lithuanian (LT) and English (EN).

| Skyrius | Turinys |
|---|---|
| `00_KOMANDU_SANTRAUKA.txt` | visų komandų santrauka / full cheat sheet |
| `01_Ivadas/Teorija` | OS įvado santrauka (OS-intro.pdf) |
| `02_Failai_ir_katalogai/` | Failai ir katalogai, Atsiskaitymas1 |
| `03_Vartotojai_grupes_teises/` | Vartotojai, Vartotojai_teisės, Failų prieigos teisės |
| `04_Procesai_ir_tarnybos/` | OS procesai, systemd tarnybos |
| `04b_Kartojimas_Teksto_redaktoriai/` | nano / vim |
| `05_Archyvatoriai_paketai/` | tar/zip/gzip, apt/dpkg/snap/PPA/source |
| `06_Shell_scenarijai/` | bash scenarijai |
| `07_Nuotolinis_pasiekiamumas/` | IP, SSH, scp |
| `08_Git_GitHub_VSCode/` | git santrauka |
| `09_Apache_Nginx/` | Apache2, Nginx, domenas |
| `09b_Kartojimas_Aplinkos_kintamieji/` | aplinkos kintamieji |
| `10_Docker/` | Docker, Dockerfile, compose |
| `11_Debesijos_kompiuterija/` | debesijos teorija |
| `12_Pasiruosimas_atsiskaitymui/` | pasiruošimas kontroliniui (abu darbai, uzd_1–7) ir OS kontrolinis (18 punktų) |

## Terminų žodynas / LT → EN glossary

Course terms that don't map obviously to the English you know.

| LT (as used in the course) | EN | Watch out |
|---|---|---|
| tarnyba | service / daemon (systemd unit) | not "job" or "task" |
| tarnybinė stotis | server | literally "service station" |
| apvalkalas / interpretatorius | shell | literally "shell/casing" |
| scenarijus | script | literally "scenario" |
| katalogas | directory / folder | not "catalog" |
| teisės / prieigos teisės | permissions | literally "rights" |
| šeimininkas / savininkas | owner (of a file) | "šeimininkas" = literally "master/host" |
| nuoroda / simbolinė nuoroda | link / symlink | "kieta nuoroda" = hard link |
| glaudinti / suspausti | compress | "suarchyvuoti" = archive (tar), "išarchyvuoti" = extract |
| paketas | package | "paketų valdymas" = package management |
| saugykla | repository (apt) or storage | context decides |
| atvaizdas | image (Docker / ISO) | literally "reflection"; "paveikslėlis" = picture |
| konteineris | container | same word |
| branduolys | kernel | literally "core/nucleus" |
| įkrova / įkrovimas | boot | "perkrauti" = reboot, or restart a service |
| prievadas | port (network) | not "harbour" (uostas) |
| ugniasienė | firewall | ufw tasks |
| grįžtamojo ryšio adresas | loopback address | 127.0.0.1 |
| viešasis / privatus IP | public / private IP | |
| tinklalapis / svetainė | web page / website | "talpinti" = host (a site) |
| virtualus hostas | virtual host (Apache) | |
| nutolęs / nuotolinis | remote | "nuotolinis pasiekiamumas" = remote access |
| vartotojas / naudotojas | user | both used interchangeably |
| šakninis vartotojas | root user | literally "root-ish" |
| administratoriaus teisės | admin rights = sudo group | |
| pagrindinė / pirminė grupė | primary group (`-g`) | "papildomos grupės" = supplementary (`-G`) |
| namų katalogas | home directory | |
| paslėptas failas | hidden (dot) file | |
| plėtinys | file extension | |
| koduotas slaptažodis | hashed password (/etc/shadow) | "coded" really means hashed |
| zombiniai procesai | zombie processes | |
| išeities kodas | source code | literally "exit code"! Exit status is "grįžimo kodas" |
| vykdomasis / paleidžiamasis failas | executable | "paleisti" = run/launch, "vykdyti" = execute |
| išvesti į ekraną | print to screen / output | "išvestis" = output, "įvestis" = input |
| nukreipti | redirect (`>` `>>`) | |
| kintamasis | variable | "aplinkos kintamieji" = environment variables |
| atnaujinti sistemą | update + upgrade | always two commands: `apt update`, `apt upgrade` |
| įdiegti / įsirašyti / instaliuoti | install | all three used |
| pašalinti / ištrinti | remove / delete | |
| perkelti / nukopijuoti / pervadinti | move / copy / rename | |
| surūšiuoti | sort | "pasikartojimai" = duplicates |
| išlygiuoti | justify (nano Ctrl+J) | |
| sunumeruoti | number the lines (`nl`, `cat -n`) | |
| ekrano nuotrauka / atvaizdas | screenshot | |
| debesija / debesų kompiuterija | cloud computing | |
| virtuali mašina | virtual machine | "Host sistema" kept in English |
| distribucija | distro | |
| atvirasis kodas | open source | |
| laisva programinė įranga | free (libre) software | "nemokama" = free of charge |
| tvarkyklė | driver | |
| žurnalas / log'ai | log | journalctl = "sistemos žurnalas" |
| būsena | status / state | `systemctl status` |
| automatinis paleidimas | autostart (enable / disable) | |
| atsiskaitymas / kontrolinis | assessment / test | "užduotis" = task, "punktas" = item/step |

### Grammar traps when reading tasks

- Case endings change the surrounding words, not the name: "katalogo Bandymas turinį" = "the contents of directory Bandymas".
- "kataloge X sukurkite" = create **inside** X. "katalogą X sukurkite" = create X **itself**.
- į = into/to, iš = from, prie = (attach) to, su = with. "Pridėkite vartotoją prie grupės" = add the user to the group.
- `*` before a task number = optional / harder task.
- tšk. = taškai = points.

### Abbreviations and borrowed words

- OS = operacinė sistema, PĮ = programinė įranga (software), VM = virtuali mašina.
- English words often keep Lithuanian endings: log'sus, hostas, shell'as, deb paketas, PPA, snap, PuTTY.
