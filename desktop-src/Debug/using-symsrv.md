---
description: Verwenden von SymSrv
ms.assetid: d400f222-c50c-4c7b-8f8a-0c3ed3bba3b9
title: Verwenden von SymSrv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae79d9fd045ab3ce946c14468e56419d3074858c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214156"
---
# <a name="using-symsrv"></a>Verwenden von SymSrv

SymSrv liefert Symbol Dateien aus zentralisierten Symbol speichern. Diese Speicher können beliebig viele Symbol Dateien enthalten, die einer beliebigen Anzahl von Programmen oder Betriebssystemen entsprechen. Die Speicher können auch Binärdateien enthalten, die besonders nützlich sind, wenn minidumpdateien debuggt werden.

Die Speicher können die eigentlichen Symbol-und Binärdateien oder einfach Zeiger auf Symbol Dateien enthalten. Wenn der Speicher Zeiger enthält, ruft SymSrv die eigentlichen Dateien direkt aus den Quellen ab.

SymSrv kann auch einen großen Symbol Speicher in eine kleinere Teilmenge aufteilen, die für eine spezialisierte debugaufgabe geeignet ist.

Schließlich kann SymSrv Symbol Dateien aus einer HTTP-oder HTTPS-Quelle abrufen, indem die vom Betriebssystem bereitgestellten Anmelde Informationen verwendet werden. SymSrv unterstützt HTTPS-Websites, die durch Smartcards, Zertifikate und reguläre Anmeldungen und Kenn Wörter geschützt sind.

## <a name="setting-the-symbol-path"></a>Festlegen des Symbol Pfads

Wie in [Symbol Pfaden](symbol-paths.md)beschrieben, kann der Symbol Pfad (die \_ \_ \_ Umgebungsvariable des NT-Symbol Pfads) aus mehreren Pfad Elementen bestehen, die durch Semikolons getrennt sind. Wenn eines oder mehrere dieser Pfad Elemente mit dem Text "SRV \* " beginnen, ist das Element ein Symbol Server und verwendet SymSrv, um Symbol Dateien zu suchen.

> [!Note]  
> Wenn der "SRV \* "-Text nicht angegeben ist, aber das eigentliche Path-Element ein Symbol Server Speicher ist, verhält sich der Symbol Handler so, als ob "SRV \* " angegeben wurde. Der Symbol Handler trifft diese Bestimmung durchsuchen nach dem vorhanden sein einer Datei namens "pingme.txt" im Stammverzeichnis des angegebenen Pfads.

 

Ebenso wie Symbol Pfade aus Symbol Pfad Elementen bestehen, die durch Semikolons getrennt sind, bestehen Symbol Server aus Symbol Speicherelementen, die durch Sternchen voneinander getrennt sind. Nach dem Präfix "SRV" können bis zu 10 Symbol Speicher vorhanden sein \* . Filialen, die auf der linken Seite der Liste aufgelistet werden, *werden als* downstreamspeicher bezeichnet und werden auf der rechten Seite als upstreamspeicher *bezeichnet* .

<dl> SRV- \* *Symbolspeicher*  
SRV \* *SymbolStore1* \* *symbolstoren*  
</dl>

Wenn nur ein Symbol Speicher Element im Pfad enthalten ist, versucht SymSrv, die angeforderte Datei direkt aus diesem Speicher zu verwenden.

Wenn der Pfad zwei Symbol Speicher enthält, sucht SymSrv nach der Symbol Datei im Symbol Speicher ganz links. Wenn die Datei vorhanden ist, wird Sie verwendet. Wenn dies nicht der Fall ist, sucht SymSrv sofort nach rechts im Symbol Speicher. Wenn die Datei vorhanden ist, wird Sie in den linken Speicher kopiert und von dort aus geöffnet.

Wenn mehr als zwei Speicher vorhanden sind, wird dieses Verhalten nach rechts fortgesetzt, bis die Datei gefunden wird oder keine weiteren Speicher in der Liste vorhanden sind.

Die Datei wird nie aus einem Speicher, sondern dem am weitesten links stehenden Speicher geöffnet. Wenn die Datei an einer anderen Stelle in der Kette gefunden wird, wird Sie in alle Filialen auf der linken Seite kopiert. Dieser Kopiervorgang wird als "Cascading" bezeichnet und bietet bestimmte Vorteile, die später in diesem Dokument vereinfacht werden.

## <a name="types-of-symbol-stores"></a>Typen von Symbol Speichern

In der folgenden Tabelle werden Beispiele für die unterstützten Symbol Speichertypen angezeigt.

|                            |                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \\\\Server \\ Freigabe          | Ein voll qualifizierter UNC-Pfad zu einer Freigabe auf einem Remote Server.                                                                                                                                                                                                                                                                                                 |
| c: \\ localcache             | Ein Pfad zu einem Verzeichnis auf dem Client Computer.                                                                                                                                                                                                                                                                                                             |
| https://InternetSite        | Die URL zu einer Website, auf der die Symbole gehostet werden. Muss der äußteste Speicher in der Liste sein und sollte nicht der einzige Speicher in der Liste sein.                                                                                                                                                                                                                          |
| https://SecureInternetSite | Die URL zu einer sicheren Website, auf der die Symbole gehostet werden. Hiermit können Kenn Wörter, Windows-Anmelde Informationen, Zertifikate und Smartcards unterstützt werden. Muss der äußteste Speicher in der Liste sein und sollte nicht der einzige Speicher in der Liste sein.                                                                                                                              |
| <blank>              | Wenn kein Text zwischen zwei Sternchen vorhanden ist, gibt dies den standardmäßigen *downstreamspeicher* an. Der Speicherort wird durch Aufrufen von [**symsethomedirectory**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory)festgelegt. Der Standardwert ist ein Verzeichnis namens "Sym" direkt unterhalb des Programmverzeichnisses der aufrufenden Anwendung. Dies wird manchmal als *Lokaler Standard Cache* bezeichnet. |



 

Da auf einen HTTP-basierten Symbol Speicher nicht geschrieben werden kann, muss es sich um den am weitesten rechts stehenden Speicher in der Liste handeln. Wenn sich ein HTTP-basierter Symbol Speicher in der Mitte oder auf der linken Seite der Speicher Liste befand, wäre es nicht möglich, gefundene Dateien darauf zu kopieren, und die Kette wäre beschädigt. Da der Symbol Handler eine Datei nicht von einer Website öffnen kann, sollte ein HTTP-basierter Speicher nicht der äußteste oder einzige Speicher in der Liste sein. Wenn SymSrv jemals mit diesem Symbol Pfad dargestellt wird, wird versucht, die Datei wiederherzustellen, indem die Datei in den standardmäßigen downstreamspeicher kopiert und von dort aus geöffnet wird, unabhängig davon, ob der standardmäßige downstreamspeicher im Symbol Pfad angegeben ist.

## <a name="examples"></a>Beispiele

\\ \\ \\ Legen Sie den folgenden Symbol Pfad fest, um SymSrv mit einem Symbol Speicher auf mybuilds mysymbols zu verwenden:

**Festlegen des \_ NT- \_ Symbol \_ Pfads = SRV \* \\ \\ mybuilds \\ mysymbols**

Verwenden Sie Folgendes, um den Symbol Pfad so festzulegen, dass der Debugger Symbol Dateien aus einem Symbol Speicher auf \\ \\ mybuilds \\ mysymbols in das lokale Verzeichnis c: \\ localsymbols kopiert:

**Legen Sie \_ NT- \_ Symbol \_ Pfad = SRV \* c: \\ localsymbols \* \\ \\ mybuilds \\ mysymbols fest.**

Zum Festlegen des Symbol Pfads, sodass der Debugger Symbol Dateien aus einem Symbol Speicher auf \\ \\ mybuilds \\ in den standardmäßigen downstreamspeicher kopiert (in der Regel c: Debugger \\ \\ SYM), verwenden Sie Folgendes:

**Festlegen des \_ NT- \_ Symbol \_ Pfads = SRV \* \* \\ \\ mybuilds \\ mysymbols**

Legen Sie den folgenden Symbol Pfad fest, um einen kaskadierenden Speicher zu verwenden:

**Legen Sie \_ NT- \_ Symbol \_ Pfad = SRV \* c: \\ localsymbols \* \\ \\ nearbyserver- \\ Speicher fest.\*https://DistantServer**

In diesem Beispiel sucht SymSrv zuerst in c: localsymbols nach der Datei \\ . Wenn Sie dort gefunden wird, wird ein Pfad zur Datei zurückgegeben. Andernfalls sucht SymSrv im \\ \\ nearbyserver-Speicher nach der Datei \\ . Wenn Sie dort gefunden wird, wird die Datei von SymSrv in c: \\ localsymbols kopiert und ein Pfad zur Datei zurückgegeben. Wenn Sie nicht gefunden wird, sucht SymSrv die Datei in https://DistantServer , und wenn Sie dort gefunden wird, kopiert SymSrv die Datei in den \\ \\ nearbyserver- \\ Speicher und anschließend in c: \\ localsymbols.

In diesem letzten Beispiel wird gezeigt, wie das Herunterladen von Symbolen mithilfe des durchsichtigen Entwurfs eines Symbol Pfads optimiert werden kann. Wenn Sie über eine Arbeits Website mit einer Gruppe von Debuggern verfügen und alle Symbole von einem entfernten Speicherort erhalten müssen, können Sie einen gemeinsamen Server mit einem Symbol Speicher in der Nähe aller debuggger einrichten. Richten Sie dann jeden Debugger mit dem oben aufgeführten Symbol Pfad ein. Der erste Debugger, der eine bestimmte Version von foo. pdb erfordert, lädt ihn aus in den https://DistantServer \\ \\ nearbyserver \\ -Speicher und dann auf seinen eigenen Computer in c: \\ localsymbols herunter. Der nächste Debugger, der die gleiche Datei erfordert, kann ihn aus \\ \\ dem nearbyserver-Speicher herunterladen, \\ da er bereits vom vorherigen Debugger an diesen Speicherort heruntergeladen wurde. Diese mehrstufige Zwischenspeicherung spart eine beträchtliche Zeit und Netzwerkbandbreite.

## <a name="microsoft-symbol-store"></a>Microsoft-Symbol Speicher

Microsoft bietet Zugriff auf einen Internet Symbol Server, der Symbol Dateien für die vielen Versionen des Windows-Betriebssystems enthält. Es ist nicht garantiert, dass dieser Katalog von Symbolen fertig ist, aber er ist umfangreich. Andere Microsoft-Produkte werden ebenfalls dargestellt.

Der Internet Symbol Server wird mit einer Vielzahl von Windows-Symbolen für Microsoft Windows-Betriebssysteme aufgefüllt, einschließlich Hotfixes, Service Packs, Sicherheitsrollup-Pakete und Einzelhandels Releases. Symbole sind auch auf dem Server für aktuelle Betas und Releasekandidaten für Windows-Produkte sowie eine Vielzahl anderer Microsoft-Produkte, wie z. b. Microsoft Internet Explorer, verfügbar.

Wenn Sie während des Debuggens auf das Internet zugreifen können, können Sie den Debugger so konfigurieren, dass während einer Debugsitzung erforderliche Symbole heruntergeladen werden, anstatt Symbol Dateien vor einer Debugsitzung separat herunterzuladen. Die Symbole werden an einen Verzeichnis Speicherort heruntergeladen, den Sie angeben, und dann lädt der Debugger Sie von dort.

Die URL für den Microsoft-Symbol Speicher lautet https://msdl.microsoft.com/download/symbols . Im folgenden Beispiel wird gezeigt, wie der debuggersymbolpfad festgelegt wird (durch ihren Downstream-Speicherpfad für *c: \\ downstreamstore* ersetzt):

``` syntax
srv*c:\DownstreamStore*https://msdl.microsoft.com/download/symbols
```

## <a name="compressed-files"></a>Komprimierte Dateien

SymSrv ist mit Symbol Speichern kompatibel, die komprimierte Dateien enthalten, sofern diese Komprimierung mit dem compress.exe Tool, das mit dem Resource Kit von Windows Server 2003 verteilt wurde, vorgeformt wurde. Komprimierte Dateien sollten einen Unterstrich als letztes Zeichen in ihren Dateierweiterungen aufweisen (z. b. Module1. PD \_ oder Module2. DB \_ ). Weitere Informationen finden [Sie unter Verwenden von SymStore](using-symstore.md).

Beim Kaskadieren werden Dateien nicht dekomprimiert, es sei denn, der Zielspeicher ist der am weitesten links stehende Speicher im Pfad. Wenn sich nur ein Speicher im Pfad befindet und eine komprimierte Datei enthält, kopiert SymSrv die Datei in den standardmäßigen downstreamspeicher und öffnet sie von dort aus, auch wenn der standardmäßige downstreamspeicher nicht im Symbol Pfad angegeben wird.

**Dbghelp 6,1 und früher.:** Wenn die Dateien im Master Speicher komprimiert sind, müssen Sie einen downstreamspeicher verwenden. SymSrv dekomprimiert alle Dateien, bevor Sie in den downstreamspeicher kopiert werden.

## <a name="deleting-the-cache"></a>Löschen des Caches

Wenn Sie einen downstreamspeicher als Cache verwenden, können Sie dieses Verzeichnis jederzeit löschen, um Speicherplatz zu sparen.

Es ist möglich, einen umfangreichen Symbol Speicher zu haben, der Symbol Dateien für viele verschiedene Programme oder Windows-Versionen enthält. Wenn Sie die auf dem Zielcomputer verwendete Windows-Version aktualisieren, entsprechen alle zwischengespeicherten Symbol Dateien der früheren Version. Diese zwischengespeicherten Dateien werden nicht weiter verwendet, und daher kann es sinnvoll sein, den Cache zu löschen.

Debuggingtools für Windows verfügen über ein Hilfsprogramm mit dem Namen agestore.exe, das Dateien selektiv aus einer Verzeichnisstruktur entfernt und die zuletzt verwendeten Dateien verlässt. Dieses Tool dient zum Bereinigen nicht verwendeter Dateien aus Symbol Server speichern. Sie ermöglicht es Ihnen, viele Optionen zu steuern, einschließlich der Algorithmen zum Ausschneiden von Datums-und Verzeichnis Größen.

## <a name="flat-cache-directory"></a>Flatcache-Verzeichnis

Es ist möglich, den standardmäßigen downstreamspeicher als ein flatdirectory anstelle einer standardmäßigen Symbol Struktur zu deklarieren. Um dies zu tun, wenden Sie die [**symsetoptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) -Funktion mit dem **symopt- \_ \_ flatdirectory** an (Dadurch wird auch die Option " **ssrvopt \_ Flat \_ Default \_ Store** " in SymSrv festgelegt). Achten Sie darauf, dass Sie zunächst " [**SYM-thomedirectory**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory) " anrufen. Andernfalls können die Symbol Dateien in das Programmverzeichnis geschrieben werden.

## <a name="pointer-files"></a>Zeiger Dateien

SymStore kann Dateien erstellen und verwenden, die auf eine Zieldatei und nicht auf die Zieldatei selbst verweisen. Wenn ein Symbol Speicher eine solche Zeiger Datei enthält, wird standardmäßig die Datei aus dem Speicherort kopiert, der in der Zeiger Datei in den Speicher angegeben ist. Um einen Speicher so zu konfigurieren, dass die Zeiger Datei anstelle der Datei, auf die Sie verweist, kopiert wird, erstellen Sie eine Datei mit dem Namen wantsptr.txt im Stammverzeichnis des Zielspeicher. Der Inhalt wantsptr.txt ist nicht wichtig, sondern nur das vorhanden sein der Datei.

## <a name="excluding-files-from-symbols-list"></a>Ausschließen von Dateien aus der Symbolliste

Um Dateien aus einer Symbol Suche auszuschließen, können Sie Ihre Namen in symsrv.ini oder in der Registrierung angeben. Um die Dateien in symsrv.ini anzugeben, erstellen Sie einen Abschnitt mit dem Namen Ausschlüsse, und Listen Sie die Dateien auf. Die Dateinamen können Platzhalter enthalten, wie im folgenden Beispiel gezeigt:

``` syntax
[Exclusions]
dbghelp.pdb
symsrv.*
mso*
```

Symsrv.ini sollte sich in demselben Verzeichnis befinden, in dem sich symsrv.dll befindet. In den meisten Installationen ist die Datei nicht vorhanden, und Sie müssen eine neue Datei erstellen.

Alternativ können Sie die Dateien speichern, die in der Registrierung ausgeschlossen werden sollen. Erstellen Sie den folgenden Registrierungsschlüssel: **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Symbol Server \\ Ausschlüsse**. Speichern Sie jeden Dateinamen als Zeichen folgen Wert (reg \_ SZ) in diesem Schlüssel. Der Name des Zeichen folgen Werts gibt den Namen der Datei an, die ausgeschlossen werden soll. Sie können den Inhalt des Zeichen folgen Werts zum Speichern eines Kommentars verwenden, der beschreibt, warum die Datei ausgeschlossen wird.

## <a name="installation"></a>Installation

Der Symbol Server SymSrv (symsrv.dll) ist im Paket Debugtools für Windows enthalten. Sie muss im gleichen Verzeichnis installiert werden wie die Kopie der dbghelp.dll, die Sie laden. Weitere Informationen finden Sie unter [Aufrufen der DbgHelp-Bibliothek](calling-the-dbghelp-library.md).

 

 



