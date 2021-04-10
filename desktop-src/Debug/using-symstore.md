---
description: SymStore (symstore.exe) ist ein Tool zum Erstellen von Symbol speichern. Sie ist im Paket Debugtools für Windows enthalten.
ms.assetid: fe8a96e9-e780-4e96-98ef-c5128515ee6c
title: Verwenden von SymStore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a87b5c527717d78adb9202fd1eddd54d1f44c02
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126812"
---
# <a name="using-symstore"></a>Verwenden von SymStore

SymStore (symstore.exe) ist ein Tool zum Erstellen von Symbol speichern. Sie ist im Paket [Debugtools für Windows](https://www.microsoft.com/?ref=go) enthalten.

SymStore speichert Symbole in einem Format, das es dem Debugger ermöglicht, die Symbole auf der Grundlage des Zeitstempels und der Größe des Bilds (für eine dbg-Datei oder ausführbare Datei) oder der Signatur und des Alters (für eine PDB-Datei) zu suchen. Der Vorteil des Symbol Speichers gegenüber dem herkömmlichen Symbol Speicherformat besteht darin, dass alle Symbole auf demselben Server gespeichert werden können und vom Debugger abgerufen und vom Debugger abgerufen werden können, ohne dass zuvor wissen, welches Produkt das entsprechende Symbol enthält.

Beachten Sie, dass mehrere Versionen von PDB-Symbol Dateien (z. b. öffentliche und private Versionen) nicht auf demselben Server gespeichert werden können, da Sie jeweils dieselbe Signatur und dasselbe Alter aufweisen.

## <a name="symstore-transactions"></a>SymStore-Transaktionen

Jeder Rückruf von SymStore wird als Transaktion aufgezeichnet. Es gibt zwei Arten von Transaktionen: Hinzufügen und löschen.

Wenn der Symbol Speicher erstellt wird, wird ein Verzeichnis mit dem Namen "000admin" unter dem Stammverzeichnis des Servers erstellt. Das Verzeichnis 000admin enthält eine Datei für jede Transaktion sowie die Protokolldateien Server.txt und History.txt. Die Server.txt Datei enthält eine Liste aller Transaktionen, die derzeit auf dem Server gespeichert sind. Die History.txt Datei enthält einen chronologischer Verlauf aller Transaktionen.

Jedes Mal, wenn SymStore Symbol Dateien speichert oder entfernt, wird eine neue Transaktionsnummer erstellt. Anschließend wird eine Datei, deren Name diese Transaktionsnummer ist, in 000admin erstellt. Diese Datei enthält eine Liste aller Dateien oder Zeiger, die während dieser Transaktion dem Symbol Speicher hinzugefügt wurden. Wenn eine Transaktion gelöscht wird, liest SymStore seine Transaktions Datei durch, um zu bestimmen, welche Dateien und Verweise gelöscht werden sollen.

Die Optionen " **Hinzufügen** " und " **del** " geben an, ob eine Transaktion zum Hinzufügen oder löschen ausgeführt werden soll Durch einschließen der **/p** -Option mit einem Add-Vorgang wird angegeben, dass ein Zeiger hinzugefügt werden soll. Wenn Sie die Option **/p** weglassen, wird angegeben, dass die tatsächliche Symbol Datei hinzugefügt werden soll.

Es ist auch möglich, den Symbol Speicher in zwei separaten Phasen zu erstellen. In der ersten Phase verwenden Sie SymStore mit der **/x** -Option, um eine Indexdatei zu erstellen. In der zweiten Phase verwenden Sie SymStore mit der **/y** -Option, um den eigentlichen Speicher von Dateien oder Zeigern aus den Informationen in der Indexdatei zu erstellen.

Dies kann aus verschiedenen Gründen eine sinnvolle Methode sein. So kann beispielsweise der Symbol Speicher problemlos neu erstellt werden, wenn der Speicher irgendwie verloren geht, solange die Indexdatei noch vorhanden ist. Möglicherweise hat der Computer, der die Symbol Dateien enthält, eine langsame Netzwerkverbindung mit dem Computer, auf dem der Symbol Speicher erstellt wird. In diesem Fall können Sie die Indexdatei auf demselben Computer wie die Symbol Dateien erstellen, die Indexdatei auf den zweiten Computer übertragen und dann den Speicher auf dem zweiten Computer erstellen.

Eine vollständige Liste aller Parameter für SymStore finden Sie unter [SymStore-Command-Line Optionen](symstore-command-line-options.md).

> [!Note]  
> SymStore unterstützt keine gleichzeitigen Transaktionen mehrerer Benutzer. Es wird empfohlen, dass ein Benutzer als "Administrator" für den Symbol Speicher festgelegt wird und für alle **Add** -und **del** -Transaktionen verantwortlich ist.

 

## <a name="transaction-examples"></a>Transaktions Beispiele

Im folgenden finden Sie zwei Beispiele für SymStore, in denen Symbol Zeiger für Build 3790 von Windows Server 2003 zu \\ \\ SampleDir \\ SymSrv hinzugefügt werden:

``` syntax
symstore add /r /p /f \\BuildServer\BuildShare\3790free\symbols\*.*
   /s \\sampledir\symsrv /t "Windows Server 2003" /v "Build 3790 x86 free"
   /c "Sample add"
symstore add /r /p /f \\BuildServer\BuildShare\3790Chk\symbols\*.* 
   /s \\sampledir\symsrv /t "Windows Server 2003" /v "Build 3790 x86 checked"
   /c "Sample add"
```

Im folgenden Beispiel fügt SymStore die eigentlichen Symbol Dateien für ein Anwendungsprojekt in \\ \\ largeapp- \\ appserver-Containern \\ zu \\ \\ TestDir \\ SymSrv hinzu:

``` syntax
symstore add /r /f \\largeapp\appserver\bins\*.* /s \\testdir\symsrv 
   /t "Large Application" /v "Build 432" /c "Sample add"
```

Im folgenden finden Sie ein Beispiel für die Verwendung einer Indexdatei. Zuerst erstellt SymStore eine Indexdatei auf der Grundlage der Auflistung von Symbol Dateien in \\ \\ largeapp- \\ appserver-Containern \\ \\ . In diesem Fall wird die Indexdatei auf einem dritten Computer, \\ \\ Hubserver \\ hubshare, platziert. Verwenden Sie die Option **/g** , um anzugeben, dass sich das Datei Präfix " \\ \\ largeapp \\ appserver" in Zukunft ändern kann:

``` syntax
symstore add /r /p /g \\largeapp\appserver /f 
   \\largeapp\appserver\bins\*.* 
   /x \\hubserver\hubshare\myindex.txt
```

Nehmen Sie nun an, dass Sie alle Symbol Dateien auf dem Computer \\ \\ largeapp \\ appserver verschieben und auf \\ \\ myarchive \\ appserver ablegen. Anschließend können Sie den Symbol Speicher selbst aus der Indexdatei \\ \\ Hubserver \\ hubshare \\myindex.txt wie folgt erstellen:

``` syntax
symstore add /y \\hubserver\hubshare\myindex.txt 
   /g \\myarchive\appserver /s \\sampledir\symsrv /p 
   /t "Large Application" /v "Build 432" /c "Sample Add from Index"
```

Im folgenden finden Sie ein Beispiel für ein SymStore, das eine von einer vorherigen Transaktion hinzugefügte Datei löscht. Im folgenden Abschnitt finden Sie eine Erläuterung zum Ermitteln der Transaktions-ID (in diesem Fall 0000000096).

``` syntax
symstore del /i 0000000096 /s \\sampledir\symsrv
```

## <a name="compressed-files"></a>Komprimierte Dateien

SymStore kann mit komprimierten Dateien auf zwei verschiedene Arten verwendet werden.

1.  Verwenden Sie SymStore mit der **/p** -Option, um Zeiger auf die Symbol Dateien zu speichern. Nachdem SymStore abgeschlossen ist, komprimieren Sie die Dateien, auf die die Zeiger verweisen.
2.  Verwenden Sie SymStore mit der **/x** -Option, um eine Indexdatei zu erstellen. Nachdem SymStore abgeschlossen ist, komprimieren Sie die in der Indexdatei aufgeführten Dateien. Verwenden Sie dann "SymStore" mit der Option **/y** (und, wenn gewünscht, die Option **/p** ), um die Dateien oder Zeiger auf die Dateien im Symbol Speicher zu speichern. (SymStore muss die Dateien nicht deinstalkomprimieren, um diesen Vorgang auszuführen.)

Der Symbol Server ist dafür verantwortlich, die Dateien zu dekomprimieren, wenn Sie benötigt werden.

Wenn Sie SymSrv als Symbol Server verwenden, sollte jede Komprimierung mithilfe des compress.exe Tools erfolgen, das mit dem Microsoft Windows Software Development Kit (SDK) verteilt wird. Komprimierte Dateien sollten einen Unterstrich als letztes Zeichen in ihren Dateierweiterungen aufweisen (z. b. Module1. PD \_ oder Module2. DB \_ ). Weitere Informationen finden [Sie unter Verwenden von SymSrv](using-symsrv.md).

## <a name="the-servertxt-and-historytxt-files"></a>Die server.txt-und history.txt Dateien

Beim Hinzufügen einer Transaktion werden server.txt und history.txt für die zukünftige Suchfunktion mehrere Informationselemente hinzugefügt. Im folgenden finden Sie ein Beispiel für eine Zeile in server.txt und history.txt für eine Transaktion zum Hinzufügen:

``` syntax
0000000096,add,ptr,10/09/99,00:08:32,Windows XP,x86 fre 1.156c-RTM-2,Added from \\mybuilds\symbols,
```

Dies ist eine durch Trennzeichen getrennte Zeile. Die Felder werden wie folgt definiert.



| Feld      | BESCHREIBUNG                                                                         |
|------------|-------------------------------------------------------------------------------------|
| 0000000096 | Transaktions-ID-Nummer, die von SymStore erstellt wurde.                                      |
| add        | Transaktionstyp. Dieses Feld kann entweder " **Add** " oder " **del**" lauten.                   |
| ptr        | Gibt an, ob Dateien oder Zeiger hinzugefügt wurden. Dieses Feld kann entweder " **File** " oder " **ptr**" lauten. |
| 10/09/99   | Datum, an dem die Transaktion aufgetreten ist                                                     |
| 00:08:32   | Zeitpunkt, zu dem die Transaktion gestartet wurde                                                      |
| Windows XP | Produkt                                                                            |
| x86-Fre    | Version (optional).                                                                 |
| Hinzugefügt von | Kommentar (optional)                                                                  |
| Nicht verwendet     | (Für die spätere Verwendung reserviert.)                                                           |



 

Im folgenden finden Sie einige Beispiel Zeilen aus der Transaktions Datei 0000000096. In jeder Zeile werden das Verzeichnis und der Speicherort der Datei oder des Zeigers aufgezeichnet, die dem Verzeichnis hinzugefügt wurde.

``` syntax
canon800.dbg\35d9fd51b000,\\mybuilds\symbols\sp4\dll\canon800.dbg
canonlbp.dbg\35d9fd521c000,\\mybuilds\symbols\sp4\dll\canonlbp.dbg
certadm.dbg\352bf2f48000,\\mybuilds\symbols\sp4\dll\certadm.dbg
certcli.dbg\352bf2f1b000,\\mybuilds\symbols\sp4\dll\certcli.dbg
certcrpt.dbg\352bf04911000,\\mybuilds\symbols\sp4\dll\certcrpt.dbg
certenc.dbg\352bf2f7f000,\\mybuilds\symbols\sp4\dll\certenc.dbg
```

Wenn Sie eine **del** -Transaktion verwenden, um die ursprünglichen **Add** -Transaktionen rückgängig zu machen, werden diese Zeilen aus server.txt entfernt, und history.txt wird die folgende Zeile hinzugefügt:

``` syntax
0000000105,del,0000000096
```

Die Felder für die Delete-Transaktion werden wie folgt definiert.



| Feld      | BESCHREIBUNG                                                       |
|------------|-------------------------------------------------------------------|
| 0000000105 | Transaktions-ID-Nummer, die von SymStore erstellt wurde.                    |
| del        | Transaktionstyp. Dieses Feld kann entweder " **Add** " oder " **del**" lauten. |
| 0000000096 | Die Transaktion, die gelöscht wurde.                                     |



 

## <a name="symbol-storage-format"></a>Symbol Speicher Format

SymStore verwendet das Dateisystem selbst als Datenbank. Es wird eine große Struktur von Verzeichnissen erstellt, wobei Verzeichnisnamen auf der Grundlage der Zeichenfolge für Zeitstempel, Signaturen, Alter und anderer Daten gespeichert werden.

Nachdem dem Server mehrere verschiedene ACPI. dbg-Dateien hinzugefügt wurden, können die Verzeichnisse beispielsweise wie folgt aussehen:

``` syntax
Directory of \\mybuilds\symsrv\acpi.dbg
10/06/1999  05:46p      <DIR>          .
10/06/1999  05:46p      <DIR>          ..
10/04/1999  01:54p      <DIR>          37cdb03962040
10/04/1999  01:49p      <DIR>          37cdb04027740
10/04/1999  12:56p      <DIR>          37e3eb1c62060
10/04/1999  12:51p      <DIR>          37e3ebcc27760
10/04/1999  12:45p      <DIR>          37ed151662060
10/04/1999  12:39p      <DIR>          37ed15dd27760
10/04/1999  11:33a      <DIR>          37f03ce962020
10/04/1999  11:21a      <DIR>          37f03cf7277c0
10/06/1999  05:38p      <DIR>          37fa7f00277e0
10/06/1999  05:46p      <DIR>          37fa7f01620a0
```

In diesem Beispiel könnte der Suchpfad für die ACPI. dbg-Symbol Datei etwa wie folgt aussehen: \\ \\ mybuilds \\ SymSrv \\ ACPI. dbg \\ 37cdb03962040.

Im Suchverzeichnis sind möglicherweise drei Dateien vorhanden:

1.  Wenn die Datei gespeichert wurde, ist ACPI. dbg dort vorhanden.
2.  Wenn ein Zeiger gespeichert wurde, ist eine Datei mit dem Namen file. PTR vorhanden, die den Pfad zur eigentlichen Symbol Datei enthält.
3.  Eine Datei mit dem Namen "refs. PTR", die eine Liste aller aktuellen Speicherorte für "ACPI. dbg" mit diesem Zeitstempel und der Abbild Größe enthält, die derzeit dem Symbol Speicher hinzugefügt werden.

In der Verzeichnis Auflistung von \\ \\ mybuilds \\ SymSrv \\ ACPI. dbg \\ 37cdb03962040 wird Folgendes angezeigt:

``` syntax
10/04/1999  01:54p                  52 file.ptr
10/04/1999  01:54p                  67 refs.ptr
```

Die Datei Datei ". PTR" enthält die Text Zeichenfolge " \\ \\ mybuilds \\ Symbols \\ x86 \\ 2128. chk \\ Symbols \\ sys \\ ACPI. dbg". Da in diesem Verzeichnis keine Datei mit dem Namen acpi. dbg vorhanden ist, versucht der Debugger, die Datei unter \\ \\ mybuilds \\ Symbols \\ x86 \\ 2128. chk \\ Symbols \\ sys \\ ACPI. dbg zu finden.

Der Inhalt von refs. PTR wird nur von SymStore verwendet, nicht vom Debugger. Diese Datei enthält einen Datensatz aller Transaktionen, die in diesem Verzeichnis durchgeführt wurden. Eine Beispiel Zeile von refs. PTR könnte wie folgt lauten:

``` syntax
0000000026,ptr,\\mybuilds\symbols\x86\2128.chk\symbols\sys\acpi.dbg
```

Dies zeigt, dass ein Zeiger auf \\ \\ mybuilds \\ Symbole \\ x86 \\ 2128. chk \\ Symbols \\ sys \\ ACPI. dbg mit der Transaktion "0000000026" hinzugefügt wurde.

Einige Symbol Dateien bleiben durch verschiedene Produkte oder Builds oder ein bestimmtes Produkt konstant. Ein Beispiel hierfür ist die Datei MSVCRT. pdb. Durch das Ausführen eines Verzeichnisses von \\ \\ mybuilds \\ SymSrv \\ msvcrt. pdb wird angezeigt, dass dem Symbol Server nur zwei Versionen von msvcrt. pdb hinzugefügt wurden:

``` syntax
Directory of \\mybuilds\symsrv\msvcrt.pdb
10/06/1999  05:37p      <DIR>          .
10/06/1999  05:37p      <DIR>          ..
10/04/1999  11:19a      <DIR>          37a8f40e2
10/06/1999  05:37p      <DIR>          37f2c2272
```

Durch das Erstellen eines Verzeichnisses von \\ \\ mybuilds \\ SymSrv \\ msvcrt. pdb \\ 37a8fi40e2 wird jedoch gezeigt, dass refs. PTR mehrere Zeiger enthält.

``` syntax
Directory of \\mybuilds\symsrv\msvcrt.pdb\37a8f40e2
10/05/1999  02:50p              54     file.ptr
10/05/1999  02:50p           2,039     refs.ptr
```

Der Inhalt von \\ \\ mybuilds \\ SymSrv \\ msvcrt. pdb \\ 37a8fi40e2 \\ refs. PTR lautet wie folgt:

``` syntax
0000000001,ptr,\\mybuilds\symbols\x86\2137\symbols\dll\msvcrt.pdb
0000000002,ptr,\\mybuilds\symbols\x86\2137.chk\symbols\dll\msvcrt.pdb
0000000003,ptr,\\mybuilds\symbols\x86\2138\symbols\dll\msvcrt.pdb
0000000004,ptr,\\mybuilds\symbols\x86\2138.chk\symbols\dll\msvcrt.pdb
0000000005,ptr,\\mybuilds\symbols\x86\2139\symbols\dll\msvcrt.pdb
0000000006,ptr,\\mybuilds\symbols\x86\2139.chk\symbols\dll\msvcrt.pdb
0000000007,ptr,\\mybuilds\symbols\x86\2140\symbols\dll\msvcrt.pdb
0000000008,ptr,\\mybuilds\symbols\x86\2140.chk\symbols\dll\msvcrt.pdb
0000000009,ptr,\\mybuilds\symbols\x86\2136\symbols\dll\msvcrt.pdb
0000000010,ptr,\\mybuilds\symbols\x86\2136.chk\symbols\dll\msvcrt.pdb
0000000011,ptr,\\mybuilds\symbols\x86\2135\symbols\dll\msvcrt.pdb
0000000012,ptr,\\mybuilds\symbols\x86\2135.chk\symbols\dll\msvcrt.pdb
0000000013,ptr,\\mybuilds\symbols\x86\2134\symbols\dll\msvcrt.pdb
0000000014,ptr,\\mybuilds\symbols\x86\2134.chk\symbols\dll\msvcrt.pdb
0000000015,ptr,\\mybuilds\symbols\x86\2133\symbols\dll\msvcrt.pdb
0000000016,ptr,\\mybuilds\symbols\x86\2133.chk\symbols\dll\msvcrt.pdb
0000000017,ptr,\\mybuilds\symbols\x86\2132\symbols\dll\msvcrt.pdb
0000000018,ptr,\\mybuilds\symbols\x86\2132.chk\symbols\dll\msvcrt.pdb
0000000019,ptr,\\mybuilds\symbols\x86\2131\symbols\dll\msvcrt.pdb
0000000020,ptr,\\mybuilds\symbols\x86\2131.chk\symbols\dll\msvcrt.pdb
0000000021,ptr,\\mybuilds\symbols\x86\2130\symbols\dll\msvcrt.pdb
0000000022,ptr,\\mybuilds\symbols\x86\2130.chk\symbols\dll\msvcrt.pdb
0000000023,ptr,\\mybuilds\symbols\x86\2129\symbols\dll\msvcrt.pdb
0000000024,ptr,\\mybuilds\symbols\x86\2129.chk\symbols\dll\msvcrt.pdb
0000000025,ptr,\\mybuilds\symbols\x86\2128\symbols\dll\msvcrt.pdb
0000000026,ptr,\\mybuilds\symbols\x86\2128.chk\symbols\dll\msvcrt.pdb
0000000027,ptr,\\mybuilds\symbols\x86\2141\symbols\dll\msvcrt.pdb
0000000028,ptr,\\mybuilds\symbols\x86\2141.chk\symbols\dll\msvcrt.pdb
0000000029,ptr,\\mybuilds\symbols\x86\2142\symbols\dll\msvcrt.pdb
0000000030,ptr,\\mybuilds\symbols\x86\2142.chk\symbols\dll\msvcrt.pdb
```

Dies zeigt, dass dieselbe msvcrt. PDB-Datei für mehrere Builds von Symbolen verwendet wurde, die auf \\ \\ mybuilds \\ SymSrv gespeichert wurden.

Im folgenden finden Sie ein Beispiel für ein Verzeichnis mit einer Mischung aus Datei-und Zeiger Ergänzungen:

``` syntax
Directory of E:\symsrv\dbghelp.dbg\38039ff439000
10/12/1999  01:54p         141,232     dbghelp.dbg
10/13/1999  04:57p              49     file.ptr
10/13/1999  04:57p             306     refs.ptr
```

In diesem Fall weist refs. PTR den folgenden Inhalt auf:

``` syntax
0000000043,file,e:\binaries\symbols\retail\dll\dbghelp.dbg
0000000044,file,f:\binaries\symbols\retail\dll\dbghelp.dbg
0000000045,file,g:\binaries\symbols\retail\dll\dbghelp.dbg
0000000046,ptr,\\sampledir\bin\symbols\retail\dll\dbghelp.dbg
0000000047,ptr,\\sampledir2\bin\symbols\retail\dll\dbghelp.dbg
```

Daher haben die Transaktionen 43, 44 und 45 dem Server dieselbe Datei hinzugefügt, und die Transaktionen 46 und 47 haben Zeiger hinzugefügt. Wenn die Transaktionen 43, 44 und 45 gelöscht werden, wird die Datei dbghelp. dbg aus dem Verzeichnis gelöscht. Das Verzeichnis erhält dann den folgenden Inhalt:

``` syntax
Directory of e:\symsrv\dbghelp.dbg\38039ff439000
10/13/1999  05:01p                   49 file.ptr
10/13/1999  05:01p                 130 refs.ptr
```

"File. PTR" enthält jetzt " \\ \\ sampledir2 \\ bin \\ Symbols \\ Retail \\ dll \\ dbghelp. dbg", und refs. PTR enthält

``` syntax
0000000046,ptr,\\sampledir\bin\symbols\retail\dll\dbghelp.dbg
0000000047,ptr,\\sampledir2\bin\symbols\retail\dll\dbghelp.dbg
```

Wenn der letzte Eintrag in refs. PTR ein Zeiger ist, ist die Datei Datei. PTR vorhanden und enthält den Pfad zu der zugeordneten Datei. Wenn der letzte Eintrag in refs. PTR eine Datei ist, ist in diesem Verzeichnis keine Datei. PTR vorhanden. Daher kann jeder Löschvorgang, durch den der endgültige Eintrag in refs. PTR entfernt wird, dazu führen, dass Datei. PTR erstellt, gelöscht oder geändert wird.

 

 



