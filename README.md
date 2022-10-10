<style>
    body {
        background-color: rgb(30, 30, 30);
        text-align: center;
        font-size: 16px;
        color: #fff;
    }
</style>

# Komendy Diskpart

## `Podstawy`

Program uruchamiamy wpisując w konsoli CMD polecenie diskpart

Pomoc dla całego narzędzia diskpart otrzymamy wpisując w konsoli polecenie **help diskpart** bądź **diskpart /?**

Musimy jednak pamiętać, że nie jest to cała dostępna pomoc a jedynie zbiór poleceń dostępny dla tego programu. Pomoc bardziej szczegółową otrzymamy wprowadzając polecenie help i dane polecenie np. **help list**

<div style="width: 100%; height: 5px; margin: 20px 0; background-color: #fff;">
</div>

**list disk** – dzięki niej uzyskamy informacje o numerze dysku.

**list partition** – dzięki niej wyświetlimy listę partycji na wybranym dysku.

**list volume** – dzięki niej wyświetlimy listę woluminów.

**list vdisk** – dzięki niej wyświetlimy listę dysków wirtualnych.

Jeżeli chcielibyśmy odczytać parametry dysku twardego, wystarczy w konsoli wpisać polecenie: **detail disk**

<div style="width: 100%; height: 5px; margin: 20px 0; background-color: #fff;">
</div>

## Polecenie **Shrink**

W celu sprawdzenia z jakimi parametrami możemy korzystać z polecenia **shrink**, wprowadźmy w konsoli: **help shrink**

Zastosowanie tego polecenia bez jakiegokolwiek parametru spowoduje zmniejszenie partycji o maksymalną wartość jaka jest dostępna. Jeżeli chcielibyśmy wiedzieć jaka będzie to przestrzeń przed zmniejszeniem, wpiszemy w konsoli polecenie: **shrink querymax**

Przy poleceniu **shrink** wielkość należy podawać w MB.  W konsoli wprowadzamy polecenie **shrink desired=1024**

## Tworzenie **Partycji**

Aby stworzyć partycje korzystamy z polecenia:
```
create partition primary size=1024
```

Słowa **create primary** oznaczają, że chcemy utworzyć **partycję podstawową**, słowo **size** mówi o pojemności nowej partycji.

## Formatowanie Partycji

Polecenie na szybkie formatowanie wygląda następująco:
```
format fs=ntfs quick
```

### **Przypisywanie litery**

Po sformatowaniu partycji, należy pamiętać o przypisaniu nowej litery dysku. W tym celu skorzystamy z polecenia:
```
assign letter k
```
gdzie **k** możemy zastąpić dowolną literą, oczywiście która nie była jeszcze wykorzystana.

<br>

Opuszczamy linię poleceń wpisując polecenie: exit
