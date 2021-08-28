---
description: Verwenden von SymSrv
ms.assetid: d400f222-c50c-4c7b-8f8a-0c3ed3bba3b9
title: Verwenden von SymSrv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1f0abcbd76b710e6a9429baa1ceff6d3a53a0df
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886501"
---
# <a name="using-symsrv"></a>Verwenden von SymSrv

SymSrv liefert Symboldateien aus zentralisierten Symbolspeichern. Diese Speicher können eine beliebige Anzahl von Symboldateien enthalten, die einer beliebigen Anzahl von Programmen oder Betriebssystemen entspricht. Die Speicher können auch Binärdateien enthalten, die besonders beim Debuggen von Minidumpdateien nützlich sind.

Die Speicher können die tatsächlichen Symbol- und Binärdateien oder einfach Zeiger auf Symboldateien enthalten. Wenn der Speicher Zeiger enthält, ruft SymSrv die eigentlichen Dateien direkt aus ihren Quellen ab.

SymSrv kann auch einen großen Symbolspeicher in eine kleinere Teilmenge aufteilen, die für eine spezielle Debugaufgabe geeignet ist.

Schließlich kann SymSrv Symboldateien aus einer HTTP- oder HTTPS-Quelle abrufen, indem die vom Betriebssystem bereitgestellten Anmeldeinformationen verwendet werden. SymSrv unterstützt HTTPS-Websites, die durch Smartcards, Zertifikate und reguläre Anmeldungen und Kennwörter geschützt sind.

## <a name="setting-the-symbol-path"></a>Festlegen des Symbolpfads

Wie unter [Symbolpfade](symbol-paths.md)beschrieben, kann der Symbolpfad ( NT SYMBOL PATH-Umgebungsvariable) aus mehreren Pfadelementen durch \_ \_ \_ Semikolons getrennt werden. Wenn eines oder mehrere dieser Pfadelemente mit dem Text "srv" beginnen, ist das Element ein Symbolserver und verwendet \* SymSrv, um Symboldateien zu suchen.

> [!Note]  
> Wenn der Text "srv" nicht angegeben ist, das tatsächliche Pfadelement jedoch ein Symbolserverspeicher ist, dann wird der Symbolhandler so agieren, als wäre \* "srv" \* angegeben. Der Symbolhandler bestimmt dies, indem er im Stammverzeichnis des angegebenen Pfads nach einer Datei namens "pingme.txt" sucht.

 

Ebenso wie Symbolpfade aus Symbolpfadelementen, die durch Semikolons getrennt sind, besteht der Symbolserver aus Symbolspeicherelementen, die durch Sternchen getrennt sind. Nach dem Präfix "srv" können bis zu 10 \* Symbolspeicher angezeigt werden. Auf der linken Seite der Liste aufgeführte Speicher werden als *Downstreamspeicher* und Speicher auf der rechten Seite als *Upstreamspeicher* bezeichnet.

<dl> srv \* *SymbolStore*  
srv \* *SymbolStore1* \* *SymbolStoreN*  
</dl>

Wenn nur ein Symbolspeicherelement im Pfad enthalten ist, versucht SymSrv, die angeforderte Datei direkt aus diesem Speicher zu verwenden.

Wenn der Pfad zwei Symbolspeicher enthält, sucht SymSrv im Symbolspeicher ganz links nach der Symboldatei. Wenn die Datei dort ist, wird sie verwendet. Wenn dies nicht der Fehler ist, sucht SymSrv sofort nach rechts im Symbolspeicher. Wenn die Datei dort ist, wird sie in den linken Speicher kopiert und von dort aus geöffnet.

Wenn mehr als zwei Speicher verfügbar sind, bleibt dieses Verhalten so lange auf der rechten Seite, bis die Datei gefunden wird oder keine Speicher mehr in der Liste enthalten sind.

Die Datei wird nie aus einem Speicher geöffnet, sondern aus dem äußersten linken Speicher. Wenn die Datei an einer anderen Stelle in der Kette gefunden wird, wird sie in jeden Speicher links davon kopiert. Dieser Kopiervorgang wird als "kaskadierend" bezeichnet und bietet bestimmte Vorteile, die später in diesem Dokument erläutert werden.

## <a name="types-of-symbol-stores"></a>Typen von Symbolspeichern

Die folgende Tabelle enthält Beispiele für die unterstützten Symbolspeichertypen.

|  Symbolspeichertyp       |  Beschreibung |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \\\\\\Serverfreigabe          | Ein vollqualifizierter UNC-Pfad zu einer Freigabe auf einem Remoteserver.                                                                                                                                                                                                                                                                                                 |
| c: \\ LocalCache             | Ein Pfad zu einem Verzeichnis auf dem Clientcomputer.                                                                                                                                                                                                                                                                                                             |
| https://InternetSite        | Die URL zu einer Website, die die Symbole hosten. Muss der äußerste rechte Speicher in der Liste sein und darf nicht der einzige Speicher in der Liste sein.                                                                                                                                                                                                                          |
| https://SecureInternetSite | Die URL zu einer sicheren Website, die die Symbole hosten. Dies kann Kennwörter, Windows Anmeldeinformationen, Zertifikate und Smartcards unterstützen. Muss der äußerste rechte Speicher in der Liste sein und darf nicht der einzige Speicher in der Liste sein.                                                                                                                              |
| &lt;blank&gt;              | Wenn kein Text zwischen zwei Sternchen angezeigt wird, gibt dies den *standardmäßigen Downstreamspeicher an.* Der Speicherort wird durch Aufrufen von [**SymSetHomeDirectory festgelegt.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory) Der Standardwert ist ein Verzeichnis namens "sym" direkt unterhalb des Programmverzeichnisses der aufrufenden Anwendung. Dies wird manchmal als der lokale *Standardcache bezeichnet.* |



 

Da ein HTTP-basierter Symbolspeicher nicht in geschrieben werden kann, muss er der äußerste rechte Speicher in der Liste sein. Wenn sich ein HTTP-basierter Symbolspeicher in der Mitte oder links in der Speicherliste befindet, wäre es nicht möglich, gefundene Dateien in ihn zu kopieren, und die Kette würde unterbrochen. Da der Symbolhandler keine Datei von einer Website öffnen kann, sollte ein HTTP-basierter Speicher nicht der äußerste linke Speicher oder nur der Speicher in der Liste sein. Wenn SymSrv jemals mit diesem Symbolpfad angezeigt wird, wird versucht, die Wiederherstellung zu versuchen, indem die Datei in den standardmäßigen Downstreamspeicher kopiert und von dort aus geöffnet wird, unabhängig davon, ob der Standardmäßige Downstreamspeicher im Symbolpfad angegeben ist oder nicht.

## <a name="examples"></a>Beispiele

Um SymSrv mit einem Symbolspeicher in \\ \\ \\ mybuilds mysymbols zu verwenden, legen Sie den folgenden Symbolpfad fest:

**set \_ NT \_ SYMBOL \_ PATH= srv \* \\ \\ mybuilds \\ mysymbols**

So legen Sie den Symbolpfad so fest, dass der Debugger Symboldateien aus einem Symbolspeicher in mybuilds mysymbols in Ihr lokales Verzeichnis \\ \\ kopiert \\ c: \\ localsymbols, verwenden Sie:

**set \_ NT \_ SYMBOL \_ PATH=srv \* c: \\ localsymbols \* \\ \\ mybuilds \\ mysymbols**

Verwenden Sie Zum Festlegen des Symbolpfads, damit der Debugger Symboldateien aus einem Symbolspeicher in mybuilds mysymbols in den Standardmäßigen Downstreamspeicher kopiert (in der Regel \\ \\ \\ c: \\ debuggers \\ sym), verwenden Sie:

**set \_ NT \_ SYMBOL \_ PATH=srv \* \* \\ \\ mybuilds \\ mysymbols**

Um einen kaskadierenden Speicher zu verwenden, legen Sie den folgenden Symbolpfad fest:

**set \_ NT SYMBOL PATH = \_ \_ srv \* c: \\ localsymbols \* \\ \\ NearbyServer \\ store\*https://DistantServer**

In diesem Beispiel sucht SymSrv zuerst in c: \\ localsymbols nach der Datei. Wenn sie dort gefunden wird, wird ein Pfad zur Datei zurückgeben. Andernfalls sucht SymSrv im \\ \\ NearbyServer-Speicher nach \\ der Datei. Wenn sie dort gefunden wird, kopiert SymSrv die Datei in c: localsymbols und gibt einen Pfad zur Datei zurück. Wenn sie nicht gefunden wird, sucht SymSrv in nach der Datei, und wenn sie dort gefunden wird, kopiert SymSrv die Datei in den NearbyServer-Speicher und dann nach \\ https://DistantServer \\ \\ \\ c: \\ localsymbols.

Dieses letzte Beispiel zeigt, wie das umsichtige Design eines Symbolpfads verwendet werden kann, um das Herunterladen von Symbolen zu optimieren. Wenn Sie über eine Arbeitswebsite mit einer Gruppe von Debuggern verfügen und alle Symbole von einem entfernten Ort erhalten müssen, können Sie einen gemeinsamen Server mit einem Symbolspeicher in der Nähe aller Debugger einrichten. Richten Sie dann jeden Debugger mit dem oben angegebenen Symbolpfad ein. Der erste Debugger, der eine bestimmte Version von foo.pdb erfordert, wird ihn aus dem NearbyServer-Speicher und dann auf seinen eigenen Computer https://DistantServer \\ \\ \\ in c: \\ localsymbols herunterladen. Der nächste Debugger, der dieselbe Datei erfordert, kann sie aus dem NearbyServer Store herunterladen, da sie bereits vom vorherigen Debugger an diesen \\ \\ Speicherort heruntergeladen \\ wurde. Dieses Zwischenspeichern auf mehreren Ebene spart viel Zeit und Netzwerkbandbreite.

## <a name="microsoft-symbol-store"></a>Microsoft Symbol Store

Microsoft bietet Zugriff auf einen Internetsymbolserver, der Symboldateien für die vielen Versionen des Windows enthält. Es ist nicht garantiert, dass dieser Katalog von Symbolen vollständig ist, aber er ist umfangreich. Andere Microsoft-Produkte werden ebenfalls dargestellt.

Der Internetsymbolserver wird mit einer Vielzahl von Windows-Symbolen für Microsoft Windows-Betriebssysteme aufgefüllt, einschließlich Hotfixes, Service Packs, Sicherheitsrolluppaketen und Verkaufsversionen. Symbole sind auch auf dem Server für aktuelle Betaversionen und Release Candidates für Windows-Produkte sowie eine Vielzahl anderer Microsoft-Produkte wie Microsoft Internet Explorer.

Wenn Sie während des Debuggens Zugriff auf das Internet haben, können Sie den Debugger so konfigurieren, dass symbole bei Bedarf während einer Debugsitzung heruntergeladen werden, anstatt Symboldateien separat vor einer Debugsitzung herunterzuladen. Die Symbole werden an einen von Ihnen angegebenen Verzeichnisspeicherort heruntergeladen, und der Debugger lädt sie dann von dort aus.

Die URL für den Microsoft-Symbolspeicher ist https://msdl.microsoft.com/download/symbols . Das folgende Beispiel zeigt, wie Sie den Debuggersymbolpfad festlegen (ersetzen Sie den Downstreamspeicherpfad *durch c: \\ DownstreamStore*):

``` syntax
srv*c:\DownstreamStore*https://msdl.microsoft.com/download/symbols
```

## <a name="compressed-files"></a>Komprimierte Dateien

SymSrv ist mit Symbolspeichern kompatibel, die komprimierte Dateien enthalten, solange diese Komprimierung mit dem compress.exe-Tool vorgefertigt wurde, das mit dem Windows Server 2003 Resource Kit verteilt wurde. Komprimierte Dateien sollten einen Unterstrich als letztes Zeichen in ihren Dateierweiterungen enthalten (z. B. module1.pd \_ oder module2.db \_ ). Weitere Informationen finden Sie unter [Verwenden von SymStore.](using-symstore.md)

Beim Kaskadieren werden Dateien nicht dekomprimiert, es sei denn, der Zielspeicher ist der äußerste linke Speicher im Pfad. Wenn nur ein Speicher im Pfad enthalten ist und er eine komprimierte Datei enthält, kopiert SymSrv die Datei in den Standard-Downstreamspeicher und öffnet sie von dort aus, auch wenn der Standardmäßige Downstreamspeicher im Symbolpfad nicht angegeben ist.

**DbgHelp 6.1 und früher:** Wenn die Dateien im Masterspeicher komprimiert sind, müssen Sie einen Downstreamspeicher verwenden. SymSrv dekomprimiert alle Dateien, bevor sie in den Downstreamspeicher kopiert werden.

## <a name="deleting-the-cache"></a>Löschen des Caches

Wenn Sie einen Downstreamspeicher als Cache verwenden, können Sie dieses Verzeichnis jederzeit löschen, um Speicherplatz zu sparen.

Es ist möglich, über einen umfangreichen Symbolspeicher zu verfügen, der Symboldateien für viele verschiedene Programme oder Windows enthält. Wenn Sie die version of Windows auf dem Zielcomputer aktualisieren, werden alle zwischengespeicherten Symboldateien mit der früheren Version übereinstimmen. Diese zwischengespeicherten Dateien werden nicht weiter verwendet, daher ist dies möglicherweise ein guter Zeitpunkt, um den Cache zu löschen.

Debugtools für Windows verfügt über ein Hilfsprogramm namens agestore.exe, das Dateien selektiv aus einer Verzeichnisstruktur entfernt und die zuletzt verwendeten Dateien beibelässt. Dieses Tool ist für das Löschen nicht verwendeter Dateien aus Symbolserverspeichern konzipiert. Sie können viele Optionen steuern, z. B. Abschneidedatums- und Verzeichnisgrößenalgorithmen.

## <a name="flat-cache-directory"></a>Flatcacheverzeichnis

Es ist möglich, den standardmäßigen Downstreamspeicher als flaches Verzeichnis und nicht als Standardsymbolstruktur zu deklarieren. Rufen Sie hierzu die [**SymSetOptions-Funktion**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) mit **SYMOPT \_ FLAT \_ DIRECTORY** auf (dadurch wird auch die **Option SSRVOPT \_ FLAT DEFAULT \_ \_ STORE** in SymSrv festgelegt). Rufen Sie [**symSetHomeDirectory**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory) auf, bevor Sie dies tun. Andernfalls können die Symboldateien in das Programmverzeichnis geschrieben werden.

## <a name="pointer-files"></a>Zeigerdateien

SymStore kann Dateien erstellen und verwenden, die auf eine Zieldatei anstatt auf die Zieldatei selbst verweisen. Wenn ein Symbolspeicher eine solche Zeigerdatei enthält, besteht die Standardeinstellung darin, die Datei aus dem in der Zeigerdatei angegebenen Speicherort in den Speicher zu kopieren. Um einen Speicher so zu konfigurieren, dass die Zeigerdatei anstelle der Datei kopiert wird, auf die sie verweist, erstellen Sie eine Datei namens wantsptr.txt im Stammverzeichnis des Zielspeichers. Der Inhalt wantsptr.txt ist nicht wichtig, sondern nur das Vorhandensein der Datei.

## <a name="excluding-files-from-symbols-list"></a>Ausschließen von Dateien aus der Symbolliste

Um Dateien von einer Symbolsuche auszuschließen, können Sie deren Namen in symsrv.ini oder in der Registrierung angeben. Um die Dateien in symsrv.ini anzugeben, erstellen Sie einen Abschnitt mit dem Namen Ausschlüsse, und listen Sie die Dateien auf. Die Dateinamen können Platzhalter enthalten, wie im folgenden Beispiel gezeigt:

``` syntax
[Exclusions]
dbghelp.pdb
symsrv.*
mso*
```

Symsrv.ini sollten sich im gleichen Verzeichnis befinden, in dem sich symsrv.dll befindet. In den meisten Installationen ist die Datei nicht vorhanden, und Sie müssen eine neue erstellen.

Alternativ können Sie die auszuschließenden Dateien in der Registrierung speichern. Erstellen Sie den folgenden Registrierungsschlüssel: **HKEY \_ LOCAL MACHINE Software Microsoft Symbol Server \_ \\ \\ \\ \\ Exclusions**. Store jeden Dateinamen als Zeichenfolgenwert (REG \_ SZ) innerhalb dieses Schlüssels. Der Name des Zeichenfolgenwerts gibt den Namen der auszuschließenden Datei an. Sie können den Inhalt des Zeichenfolgenwerts verwenden, um einen Kommentar zu speichern, der beschreibt, warum die Datei ausgeschlossen wird.

## <a name="installation"></a>Installation

Der Symbolserver SymSrv (symsrv.dll) ist im Paket Debugtools für Windows enthalten. Sie muss im gleichen Verzeichnis wie die Kopie der dbghelp.dll installiert werden, die Sie laden. Weitere Informationen finden Sie unter [Aufrufen der DbgHelp-Bibliothek.](calling-the-dbghelp-library.md)

 

 



