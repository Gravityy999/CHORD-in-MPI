Prima functie pe care am implementat-o este build_finger_table(), unde doar am folosit
formulele din PDF pentru a calcula start si node. Urmatoarea functie este
closest_preceding_finger unde am parcurs in sens invers vectorul fingers[] si am returnat
prima valoare care se afla in intervaul definit de cheie si self.id. Daca nu gasesc o valoare
compatibila, returnez succesorul lui self. A treia functie este handle_lookup_request unde
verific pe care dintre cele trei cazuri ma aflu si fac send cu tag-ul necesar. In main, initiez
lookup-urile initiale si trimit mesajul catre propriul rank mpi. In while(1) care se opreste doar
cand conditiile dintr-un if sunt indeplinite(numarul de done-uri primite sa fie egal cu numarul
de rank-uri -1 iar rank-ul curent sa trimita la randul sau done). Astept un mesaj mpi iar in
functie de tag intru pe unul dintre cele trei cazuri.
