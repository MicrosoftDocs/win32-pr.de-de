---
description: Die DbgHelp-Bibliothek verwendet den Symbol Suchpfad, um Debugsymbole (PDB-und dbg-Dateien) zu suchen. Der Suchpfad kann aus einem oder mehreren Pfad Elementen bestehen, die durch Semikolons getrennt sind.
ms.assetid: 3527f589-285b-4cdf-b024-17920971a904
title: Symbolpfade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 977772e45c345e1e990dc038fccd852d17d279dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958294"
---
# <a name="symbol-paths"></a>Symbolpfade

Die DbgHelp-Bibliothek verwendet den Symbol Suchpfad, um Debugsymbole (PDB-und dbg-Dateien) zu suchen. Der Suchpfad kann aus einem oder mehreren Pfad Elementen bestehen, die durch Semikolons getrennt sind.

## <a name="specifying-search-paths"></a>Angeben von Suchpfaden

Um anzugeben, wo der Symbol Handler Datenträger Verzeichnisse nach Symbol Dateien durchsucht, müssen Sie die [**symsetsearchpath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) -Funktion aufrufen. Alternativ können Sie einen Symbol Suchpfad im *usersearchpath* -Parameter der [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) -Funktion angeben.

Der *usersearchpath* -Parameter in " [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) " und der " *SearchPath* "-Parameter in " [**symsetsearchpath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) " verwenden einen Zeiger auf eine auf NULL endenden Zeichenfolge, die einen Pfad oder eine Reihe von Pfaden durch ein Semikolon getrennt angibt. Der Symbol Handler verwendet diese Pfade, um nach Symbol Dateien zu suchen. Wenn dieser Parameter **null** ist, durchsucht der Symbol Handler das Verzeichnis, das das Modul enthält, für das Symbole durchsucht werden. Andernfalls, wenn dieser Parameter als nicht-**null** -Wert angegeben wird, durchsucht der Symbol Handler zuerst die Pfade, die von der Anwendung festgelegt wurden, bevor das Modul Verzeichnis durchsucht wird. Wenn Sie die \_ \_ Umgebungsvariable NT-Symbol \_ Pfad oder \_ NT-alt- \_ \_ Symbol Pfad festlegen \_ , sucht der Symbol Handler in der folgenden Reihenfolge nach Symbol Dateien:

1. Die \_ Umgebungsvariable für den NT- \_ Symbol \_ Pfad.
2. Die \_ NT- \_ alt- \_ Symbol Pfad- \_ Umgebungsvariable.
3. Das Verzeichnis, das das entsprechende Modul enthält.

Rufen Sie zum Abrufen der Suchpfade die [**symgetsearchpath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath) -Funktion auf.

Der Suchpfad für Programm Datenbankdateien (. pdb) unterscheidet sich von dem Pfad für Debugdateien (. dbg). Der Algorithmus wird durch die Funktionalität der Symbol Bibliothek bestimmt. Standardmäßig erstellt Microsoft Visual C/C++ Microsoft-Format Symbole, entfernt Sie aus dem Image und platziert Sie in einer separaten PDB-Datei. In der Regel befindet sich die PDB-Datei in dem Verzeichnis, das das ausführbare Image enthält. Visual C/C++ bettet den absoluten Pfad zur PDB-Datei im ausführbaren Image ein. Wenn der Symbol Handler die PDB-Datei an diesem Speicherort nicht finden kann oder wenn die PDB-Datei in ein anderes Verzeichnis verschoben wurde, sucht der Symbol Handler die PDB-Datei mithilfe des Suchpfads, der für dbg-Dateien beschrieben wird.

## <a name="path-element-types"></a>Pfad Element Typen

Es gibt drei Typen von Pfad Elementen.

### <a name="standard-path-element"></a>Standard Pfad Element

Ein Standardpfad Element wird durchsucht, indem im Stammverzeichnis des Verzeichnisses gesucht wird, das vom Path-Element angegeben wird. Der Symbol Handler sucht auch in einem Unterverzeichnis von "Symbols", das mit der Dateierweiterung des Moduls übereinstimmt, nach dem die Symbole gesucht werden. Dabei handelt es sich in der Regel um "dll", "exe" oder "sys". Schließlich wird in einem Unterverzeichnis mit dem Namen "Symbols" ein Verzeichnis mit dem gleichen Namen wie die Erweiterung angezeigt. Wenn das Symbol Pfad Element z. b. "c: \\ mysymbols" lautet und die Datei, nach der Symbole gesucht werden, "boo.dll" ist, werden die folgenden Verzeichnisse durchsucht.

- c: \\ mysymbols  
- c: \\ mysymbols- \\ dll  
- c: \\ mysymbols- \\ Symbol- \\ dll  

Der Symbol Handler verwendet diese Logik, um alle Path-Elemente zu durchsuchen, die die Kriterien nicht als *Symbol Server* oder *Cache* (unten beschrieben) erfüllen.

### <a name="symbol-server-path-element"></a>Symbol Server Pfad-Element

Ein *Symbol Server* -Pfad Element verwendet spezielle Technologie, die ein Symbol finden kann, das eine exakte Entsprechung für das betreffende Modul ist. Weitere Informationen finden [Sie unter Verwenden von SymSrv](using-symsrv.md) .

Der Symbol Handler behandelt ein Path-Element als Symbol Server, wenn er mit dem Text "SRV \* " beginnt.

> [!Note]  
> Wenn der "SRV \* "-Text nicht angegeben ist, aber das eigentliche Path-Element ein Symbol Server Speicher ist, verhält sich der Symbol Handler so, als ob "SRV \* " angegeben wurde. Der Symbol Handler trifft diese Bestimmung durchsuchen nach dem vorhanden sein einer Datei namens "pingme.txt" im Stammverzeichnis des angegebenen Pfads.

 

### <a name="cache-path-element"></a>Cache Pfad Element

Ein *Cache* Pfad Element ist eine Variation eines Symbol Server-Pfad Elements.

Dieses Verzeichnis wird wie ein beliebiger anderer Symbol Server durchsucht. Wenn das Symbol hier jedoch nicht gefunden wird und es in einem Path-Element weiter unten in der Kette des Symbol Pfads gefunden wird, wird das Symbol kopiert und auf dem Symbol Server gespeichert, der in diesem Element angegeben ist.

Der Symbol Handler behandelt ein Path-Element als Cache Element, wenn es mit dem Text "Cache \* " beginnt. Um einen Cache in "c: \\ myCache" anzugeben, verwenden Sie ein Symbol Pfad Element von "Cache \* c: \\ myCache".

## <a name="example-search-path"></a>Beispiel Suchpfad

Um zu sehen, wie dies funktioniert, legen Sie diesen Suchpfad fest.

`cache*c:\myCache;srv*\\symbols\symbols`

<!-- 
See example from https://docs.microsoft.com/windows-hardware/drivers/debugger/symbol-path
cache*c:\MySymbols;srv*https://msdl.microsoft.com/download/symbols
-->

Im folgenden finden Sie eine Auflistung der ausführlichen Ausgabe des Symbol Handlers bei der Suche nach "Ntdll. pdb" mit dem oben aufgeführten Suchpfad.

```
DBGHELP: .\ntdll.pdb - file not found
DBGHELP: .\dll\ntdll.pdb - file not found
DBGHELP: .\symbols\dll\ntdll.pdb - file not found
SYMSRV: c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb not found
SYMSRV: ntdll.pdb from \\symbols\symbols: 10497024 bytes - copied
DBGHELP: c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb already cached
DBGHELP: ntdll - private symbols & lines
c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb
```

Die ersten drei Zeilen der Ausgabe zeigen den Symbol Handler, der das erste Pfad Element von verarbeitet `.` . Dies ist ein Standardpfad Element.

Die vierte Zeile zeigt den Symbol Handler, der den Symbol Server verwendet, um nach der Datei im zweiten Path-Element zu suchen, bei `cache*c:\myCache` dem es sich um ein Cache Pfad Element handelt.

Die fünfte Zeile zeigt, dass sich die Datei im dritten Path-Element von befindet `srv*\\symbols\symbols` , bei dem es sich um ein Symbol Server-Pfad Element handelt.

Die sechste Zeile zeigt, dass die Datei in den Cache kopiert wird.

Die letzten zwei Zeilen, in denen die Datei aus dem Cache geöffnet wird.
