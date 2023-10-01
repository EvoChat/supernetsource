# supernetsource
sumber yang dipakai flooder untuk promosi yang belakangan sering muncul di berbagai IRC server
solusi mengatasi ini :
spamfilter
setting BPOM drone BL lebih ketat:
blacklist tordanme {
        dns {
                name tor.dan.me.uk;
                type record;
                reply { 100; };
        };
        action gline;
        ban-time 24h;
        reason "TOR detected";
};

blacklist spamrats {
        dns {
                name all.spamrats.com;
                type record;
                reply { 38; };
        };
        action gline;
        ban-time 24h;
        reason "host listed in the SpamRATS database. http://www.spamrats.com/lookup.php?ip=$i";
};
