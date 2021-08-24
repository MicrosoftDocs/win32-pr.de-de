---
description: Verwenden von SymSrv
ms.assetid: d400f222-c50c-4c7b-8f8a-0c3ed3bba3b9
title: Verwenden von SymSrv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 197a627e50c6be3a3e8636378890025a6dde091948954e2709935c7dc84fa30c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655030"
---
# <a name="using-symsrv"></a>Verwenden von SymSrv

SymSrv stellt Symboldateien aus zentralisierten Symbolspeichern bereit. Diese Speicher können eine beliebige Anzahl von Symboldateien enthalten, die einer beliebigen Anzahl von Programmen oder Betriebssystemen entsprechen. Die Speicher können auch Binärdateien enthalten, die besonders beim Debuggen von Minidumpdateien nützlich sind.

Die Speicher können die tatsächlichen Symbol- und Binärdateien oder einfach Zeiger auf Symboldateien enthalten. Wenn der Speicher Zeiger enthält, ruft SymSrv die eigentlichen Dateien direkt aus ihren Quellen ab.

SymSrv kann auch einen großen Symbolspeicher in eine kleinere Teilmenge untergliedern, die für einen speziellen Debugtask geeignet ist.

Schließlich kann SymSrv Symboldateien aus einer HTTP- oder HTTPS-Quelle abrufen, indem die vom Betriebssystem bereitgestellten Anmeldeinformationen verwendet werden. SymSrv unterstützt HTTPS-Websites, die durch Smartcards, Zertifikate und reguläre Anmeldungen und Kennwörter geschützt sind.

## <a name="setting-the-symbol-path"></a>Festlegen des Symbolpfads

Wie unter [Symbolpfade](symbol-paths.md)beschrieben, kann der Symbolpfad \_ (NT \_ SYMBOL \_ PATH-Umgebungsvariable) aus mehreren Pfadelementen bestehen, die durch Semikolons getrennt sind. Wenn eines oder mehrere dieser Pfadelemente mit dem Text "srv" \* beginnen, ist das Element ein Symbolserver und verwendet SymSrv, um Symboldateien zu suchen.

> [!Note]  
> Wenn der Text "srv" \* nicht angegeben ist, aber das tatsächliche Pfadelement ein Symbolserverspeicher ist, fungiert der Symbolhandler so, als ob "srv" \* angegeben wäre. Der Symbolhandler ermittelt diese Bestimmung, indem er im Stammverzeichnis des angegebenen Pfads nach einer Datei namens "pingme.txt" sucht.

 

Ebenso wie Symbolpfade aus Symbolpfadelementen bestehen, die durch Semikolons getrennt sind, bestehen Symbolserver aus Symbolspeicherelementen, die durch Sternchen getrennt sind. Nach dem Präfix "srv" können bis zu 10 Symbolspeicher vorhanden \* sein. Auf der linken Seite der Liste aufgeführte Speicher werden *als Downstreamspeicher* bezeichnet, und Speicher auf der rechten Seite werden *als Upstreamspeicher* bezeichnet.

<dl> srv \* *SymbolStore*  
srv \* *SymbolStore1* \* *SymbolStoreN*  
</dl>

Wenn nur ein Symbolspeicherelement im Pfad enthalten ist, versucht SymSrv, die angeforderte Datei direkt aus diesem Speicher zu verwenden.

Wenn sich im Pfad zwei Symbolspeicher befinden, sucht SymSrv im Symbolspeicher ganz links nach der Symboldatei. Wenn die Datei vorhanden ist, wird sie verwendet. Wenn er nicht vorhanden ist, sucht SymSrv sofort rechts im Symbolspeicher. Wenn die Datei vorhanden ist, wird sie in den linken Speicher kopiert und von dort aus geöffnet.

Wenn mehr als zwei Speicher vorhanden sind, wird dieses Verhalten nach rechts fortgesetzt, bis die Datei gefunden wird oder keine weiteren Speicher in der Liste vorhanden sind.

Die Datei wird nie in einem Speicher geöffnet, sondern im äußersten linken Speicher. Wenn die Datei an einer anderen Stelle in der Kette gefunden wird, wird sie in jeden Speicher auf der linken Seite kopiert. Dieser Kopiervorgang wird als "kaskadierend" bezeichnet und bietet bestimmte Vorteile, die später in diesem Dokument beschrieben werden.

## <a name="types-of-symbol-stores"></a>Typen von Symbolspeichern

In der folgenden Tabelle werden Beispiele für die unterstützten Symbolspeichertypen angezeigt.

|  Symbolspeichertyp       |  Beschreibung |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \\\\\\Serverfreigabe          | Ein vollqualifizierter UNC-Pfad zu einer Freigabe auf einem Remoteserver.                                                                                                                                                                                                                                                                                                 |
| c: \\ LocalCache             | Ein Pfad zu einem Verzeichnis auf dem Clientcomputer.                                                                                                                                                                                                                                                                                                             |
| https://InternetSite        | Die URL zu einer Website, die die Symbole hostet. Muss der am weitesten rechts in der Liste enthaltene Speicher sein und darf nicht der einzige Speicher in der Liste sein.                                                                                                                                                                                                                          |
| https://SecureInternetSite | Die URL zu einer sicheren Website, auf der die Symbole gehostet werden. Dies kann Kennwörter, Windows Anmeldeinformationen, Zertifikate und Smartcards unterstützen. Muss der am weitesten rechts in der Liste enthaltene Speicher sein und darf nicht der einzige Speicher in der Liste sein.                                                                                                                              |
| <blank>              | Wenn kein Text zwischen zwei Sternchen vorhanden ist, gibt dies den *standardmäßigen Downstreamspeicher* an. Der Speicherort wird durch Aufrufen von [**SymSetHomeDirectory**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory)festgelegt. Der Standardwert ist ein Verzeichnis namens "sym" direkt unterhalb des Programmverzeichnisses der aufrufenden Anwendung. Dies wird manchmal als *lokaler Standardcache* bezeichnet. |



 

Da ein HTTP-basierter Symbolspeicher nicht in geschrieben werden kann, muss er der äußerste rechte Speicher in der Liste sein. Wenn sich ein HTTP-basierter Symbolspeicher in der Mitte oder auf der linken Seite der Speicherliste befindet, wäre es nicht möglich, gefundene Dateien in ihn zu kopieren, und die Kette würde unterbrochen. Da der Symbolhandler eine Datei von einer Website aus nicht öffnen kann, sollte ein HTTP-basierter Speicher nicht ganz links oder nur in der Liste gespeichert werden. Wenn SymSrv jemals mit diesem Symbolpfad angezeigt wird, wird versucht, die Wiederherstellung zu versuchen, indem die Datei in den standardmäßigen Downstreamspeicher kopiert und von dort aus geöffnet wird, unabhängig davon, ob der standardmäßige Downstreamspeicher im Symbolpfad angegeben ist oder nicht.

## <a name="examples"></a>Beispiele

Um SymSrv mit einem Symbolspeicher auf \\ \\ mybuilds \\ mysymbols zu verwenden, legen Sie den folgenden Symbolpfad fest:

**set \_ NT \_ SYMBOL \_ PATH= srv \* \\ \\ mybuilds \\ mysymbols**

Um den Symbolpfad so festzulegen, dass der Debugger Symboldateien aus einem Symbolspeicher auf \\ \\ mybuilds \\ mysymbols in Ihr lokales Verzeichnis kopiert, verwenden Sie c: \\ localsymbols:

**set \_ NT \_ SYMBOL \_ PATH=srv \* c: \\ localsymbols \* \\ \\ mybuilds \\ mysymbols**

Verwenden Sie Folgendes, um den Symbolpfad so festzulegen, dass der Debugger Symboldateien aus einem Symbolspeicher in \\ \\ mybuilds \\ mysymbols in den standardmäßigen Downstreamspeicher kopiert (in der Regel c: \\ debugger \\ sym):

**set \_ NT \_ SYMBOL \_ PATH=srv \* \* \\ \\ mybuilds \\ mysymbols**

Um einen kaskadierenden Speicher zu verwenden, legen Sie den folgenden Symbolpfad fest:

**set \_ NT SYMBOL PATH = \_ \_ srv \* c: \\ localsymbols \* \\ \\ NearbyServer \\ store\*https://DistantServer**

In diesem Beispiel sucht SymSrv zuerst nach der Datei in c: \\ localsymbols. Wenn sie dort gefunden wird, wird ein Pfad zur Datei zurückgegeben. Andernfalls sucht SymSrv im \\ \\ NearbyServer-Speicher nach der \\ Datei. Wenn sie dort gefunden wird, kopiert SymSrv die Datei in c: \\ localsymbols und gibt einen Pfad zur Datei zurück. Wenn sie nicht gefunden wird, sucht SymSrv nach der Datei in https://DistantServer , und wenn sie dort gefunden wird, kopiert SymSrv die Datei in den \\ \\ \\ NearbyServer-Speicher und dann in c: \\ localsymbols.

In diesem letzten Beispiel wird gezeigt, wie ein mit Vorsicht gestalteter Symbolpfad verwendet werden kann, um das Herunterladen von Symbolen zu optimieren. Wenn Sie über eine Arbeitswebsite mit einer Gruppe von Debuggern verfügen und alle Symbole von einem entfernten Ort abrufen müssen, können Sie einen gemeinsamen Server mit einem Symbolspeicher in der Nähe aller Debugger einrichten. Richten Sie dann jeden Debugger mit dem obigen Symbolpfad ein. Der erste Debugger, der eine bestimmte Version von foo.pdb erfordert, lädt ihn aus https://DistantServer dem \\ \\ \\ NearbyServer-Speicher und dann auf seinen eigenen Computer in c: \\ localsymbols herunter. Der nächste Debugger, der dieselbe Datei erfordert, kann sie aus dem \\ \\ NearbyServer-Speicher \\ herunterladen, da er bereits vom vorherigen Debugger an diesen Speicherort heruntergeladen wurde. Diese Zwischenspeicherung auf mehreren Ebenen spart viel Zeit und Netzwerkbandbreite.

## <a name="microsoft-symbol-store"></a>Microsoft Symbol Store

Microsoft bietet Zugriff auf einen Internetsymbolserver, der Symboldateien für die vielen Versionen des Windows Betriebssystems enthält. Dieser Katalog von Symbolen ist nicht garantiert vollständig, aber er ist umfangreich. Andere Microsoft-Produkte werden ebenfalls dargestellt.

Der Internetsymbolserver wird mit einer Vielzahl von Windows Symbolen für Microsoft Windows-Betriebssysteme aufgefüllt, einschließlich Hotfixes, Service Packs, Sicherheitsrolluppaketen und Verkaufsversionen. Symbole sind auch auf dem Server für aktuelle Betaversionen und Releasekandidaten für Windows Produkte sowie eine Vielzahl anderer Microsoft-Produkte verfügbar, z. B. Microsoft Internet Explorer.

Wenn Sie während des Debuggens Zugriff auf das Internet haben, können Sie den Debugger so konfigurieren, dass Symbole bei Bedarf während einer Debugsitzung heruntergeladen werden, anstatt Symboldateien vor einer Debugsitzung separat herunterzuladen. Die Symbole werden an einen verzeichnisspeicherort heruntergeladen, den Sie angeben, und dann lädt der Debugger sie von dort.

Die URL für den Microsoft-Symbolspeicher lautet https://msdl.microsoft.com/download/symbols . Das folgende Beispiel zeigt, wie Sie den Debuggersymbolpfad festlegen (ersetzen Sie den Downstreamspeicherpfad durch *c: \\ DownstreamStore):*

``` syntax
srv*c:\DownstreamStore*https://msdl.microsoft.com/download/symbols
```

## <a name="compressed-files"></a>Komprimierte Dateien

SymSrv ist mit Symbolspeichern kompatibel, die komprimierte Dateien enthalten, solange diese Komprimierung mit dem compress.exe Tool vorab formatiert wurde, das mit dem Windows Server 2003 Resource Kit verteilt wurde. Komprimierte Dateien sollten einen Unterstrich als letztes Zeichen in ihren Dateierweiterungen aufweisen (z.B. module1.pd \_ oder module2.db). \_ Weitere Informationen finden Sie unter [Verwenden von SymStore.](using-symstore.md)

Beim Kaskadieren werden Dateien nicht dekomprimiert, es sei denn, der Zielspeicher ist der äußerste linke Speicher im Pfad. Wenn sich nur ein Speicher im Pfad befindet und er eine komprimierte Datei enthält, kopiert SymSrv die Datei in den standardmäßigen Downstreamspeicher und öffnet sie von dort aus, obwohl der standardmäßige Downstreamspeicher nicht im Symbolpfad angegeben ist.

**DbgHelp 6.1 und früher:** Wenn die Dateien im Masterspeicher komprimiert sind, müssen Sie einen Downstreamspeicher verwenden. SymSrv entkomprimiert alle Dateien, bevor sie in den Downstreamspeicher kopiert werden.

## <a name="deleting-the-cache"></a>Löschen des Caches

Wenn Sie einen Downstreamspeicher als Cache verwenden, können Sie dieses Verzeichnis jederzeit löschen, um Speicherplatz zu sparen.

Es ist möglich, einen großen Symbolspeicher zu haben, der Symboldateien für viele verschiedene Programme oder Windows Versionen enthält. Wenn Sie die Version von Windows aktualisieren, die auf dem Zielcomputer verwendet wird, stimmen alle zwischengespeicherten Symboldateien mit der früheren Version überein. Diese zwischengespeicherten Dateien werden nicht weiter verwendet, und daher ist es möglicherweise ein guter Zeitpunkt, den Cache zu löschen.

Debugtools für Windows verfügt über ein Hilfsprogramm namens agestore.exe, das selektiv Dateien aus einer Verzeichnisstruktur entfernt und die zuletzt verwendeten Dateien beilässt. Dieses Tool ist für das Löschen nicht verwendeter Dateien aus Symbolserverspeichern konzipiert. Sie können viele Optionen steuern, einschließlich Stichtag- und Verzeichnisgrößenalgorithmen.

## <a name="flat-cache-directory"></a>Flatcacheverzeichnis

Es ist möglich, den standardmäßigen Downstreamspeicher als flaches Verzeichnis und nicht als Standardsymbolstruktur zu deklarieren. Rufen Sie hierzu die [**Funktion SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) mit **SYMOPT \_ FLAT \_ DIRECTORY** auf (dadurch wird auch die Option **SSRVOPT \_ FLAT DEFAULT \_ \_ STORE** in SymSrv festgelegt). Rufen Sie [**symSetHomeDirectory**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory) auf, bevor Sie dies tun. Andernfalls können die Symboldateien in das Programmverzeichnis geschrieben werden.

## <a name="pointer-files"></a>Zeigerdateien

SymStore kann Dateien erstellen und verwenden, die auf eine Zieldatei anstatt auf die Zieldatei selbst zeigen. Wenn ein Symbolspeicher eine solche Zeigerdatei enthält, wird die Datei standardmäßig von dem in der Zeigerdatei angegebenen Speicherort in den Speicher kopiert. Um einen Speicher so zu konfigurieren, dass die Zeigerdatei anstelle der Datei kopiert wird, auf die sie verweist, erstellen Sie eine Datei namens wantsptr.txt im Stammverzeichnis des Zielspeichers. Der Inhalt der wantsptr.txt ist nicht wichtig, sondern nur das Vorhandensein der Datei.

## <a name="excluding-files-from-symbols-list"></a>Ausschließen von Dateien aus der Symbolliste

Um Dateien von einer Symbolsuche auszuschließen, können Sie deren Namen in der symsrv.ini oder in der Registrierung angeben. Um die Dateien in der symsrv.ini, erstellen Sie einen Abschnitt namens Ausschlüsse, und listen Sie die Dateien auf. Die Dateinamen können Platzhalter enthalten, wie im folgenden Beispiel gezeigt:

``` syntax
[Exclusions]
dbghelp.pdb
symsrv.*
mso*
```

Symsrv.ini sollte sich in demselben Verzeichnis befinden, in dem sich symsrv.dll befindet. In den meisten Installationen ist die Datei nicht vorhanden, und Sie müssen eine neue erstellen.

Alternativ können Sie die Dateien speichern, die in der Registrierung ausgeschlossen werden sollen. Erstellen Sie den folgenden Registrierungsschlüssel: **HKEY \_ LOCAL MACHINE Software Microsoft Symbol Server \_ \\ \\ \\ \\ Exclusions**. Store jeden Dateinamen als Zeichenfolgenwert (REG \_ SZ) in diesem Schlüssel. Der Name des Zeichenfolgenwerts gibt den Namen der auszuschließenden Datei an. Sie können den Inhalt des Zeichenfolgenwerts verwenden, um einen Kommentar zu speichern, der beschreibt, warum die Datei ausgeschlossen wird.

## <a name="installation"></a>Installation

Der Symbolserver SymSrv (symsrv.dll) ist im Debugtools für Windows enthalten. Sie muss im gleichen Verzeichnis installiert sein wie die Kopie der dbghelp.dll, die Sie laden. Weitere Informationen finden Sie unter [Aufrufen der DbgHelp-Bibliothek.](calling-the-dbghelp-library.md)

 

 



