---
description: Die DbgHelp-Bibliothek verwendet den Symbolsuchpfad, um Debugsymbole (PDB- und DBG-Dateien) zu suchen. Der Suchpfad kann aus einem oder mehr Pfadelementen durch Semikolons getrennt sein.
ms.assetid: 3527f589-285b-4cdf-b024-17920971a904
title: Symbolpfade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fddf01dfbb5aedfcdd2d96cdfd5d4fdd10e6d3f71b5c69024917ddac534d3824
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405900"
---
# <a name="symbol-paths"></a>Symbolpfade

Die DbgHelp-Bibliothek verwendet den Symbolsuchpfad, um Debugsymbole (PDB- und DBG-Dateien) zu suchen. Der Suchpfad kann aus einem oder mehr Pfadelementen durch Semikolons getrennt sein.

## <a name="specifying-search-paths"></a>Angeben von Suchpfaden

Um anzugeben, wo der Symbolhandler Datenträgerverzeichnisse nach Symboldateien durchsucht, rufen Sie die [**SymSetSearchPath-Funktion**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) auf. Alternativ können Sie einen Symbolsuchpfad im *UserSearchPath-Parameter* der [**SymInitialize-Funktion**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) angeben.

Der *UserSearchPath-Parameter* in [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) und der *SearchPath-Parameter* in [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) verwenden einen Zeiger auf eine auf NULL terminierte Zeichenfolge, die einen Pfad oder eine Reihe von Pfaden angibt, die durch ein Semikolon getrennt sind. Der Symbolhandler verwendet diese Pfade, um nach Symboldateien zu suchen. Wenn dieser Parameter **NULL ist,** durchsucht der Symbolhandler das Verzeichnis, das das Modul enthält, nach dem Symbole durchsucht werden. Andernfalls durchsucht der Symbolhandler zunächst die von der Anwendung festgelegten Pfade, bevor er das Modulverzeichnis durchsucht, wenn dieser Parameter als **Nicht-NULL-Wert** angegeben wird. Wenn Sie die Umgebungsvariable NT SYMBOL PATH oder NT ALT SYMBOL PATH festlegen, sucht der Symbolhandler in der folgenden \_ \_ Reihenfolge nach \_ \_ \_ \_ \_ Symboldateien:

1. Die \_ NT \_ SYMBOL \_ PATH-Umgebungsvariable.
2. Die \_ NT ALT SYMBOL \_ \_ \_ PATH-Umgebungsvariable.
3. Das Verzeichnis, das das entsprechende Modul enthält.

Rufen Sie zum Abrufen der Suchpfade die [**SymGetSearchPath-Funktion**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath) auf.

Der Suchpfad für Programmdatenbankdateien (PDB) ist anders als der Pfad für Debugdateien (DBG). Der Algorithmus wird durch die Funktionalität der Symbolbibliothek bestimmt. Standardmäßig erstellt Microsoft Visual C/C++ Microsoft-Formatsymbole, entfernt sie aus dem Bild und platziert sie in einer separaten PDB-Datei. In der Regel befindet sich die PDB-Datei in dem Verzeichnis, das das ausführbare Image enthält. Visual C/C++ bettet den absoluten Pfad zur PDB-Datei in das ausführbare Image ein. Wenn der Symbolhandler die PDB-Datei an diesem Speicherort nicht finden kann oder die PDB-Datei in ein anderes Verzeichnis verschoben wurde, sucht der Symbolhandler die PDB-Datei unter Verwendung des für DBG-Dateien beschriebenen Suchpfads.

## <a name="path-element-types"></a>Path-Elementtypen

Es gibt drei Arten von Pfadelementen.

### <a name="standard-path-element"></a>Standard Path-Element

Ein Standardpfadelement wird durch Suchen im Stammverzeichnis des Verzeichnisses durchsucht, das durch das path-Element angegeben wird. Der Symbolhandler sucht auch in einem Unterverzeichnis von "Symbolen", das der Dateierweiterung des Moduls entspricht, nach dem Symbole suchen. Dies ist in der Regel "dll", "exe" oder "sys". Schließlich sucht er in einem Unterverzeichnis namens "symbols" mit einem Verzeichnis mit dem gleichen Namen wie die Erweiterung. Wenn das Symbolpfadelement beispielsweise "c: mySymbols" und die Datei, nach der Symbole gesucht werden, "boo.dll" ist, werden die folgenden Verzeichnisse \\ durchsucht.

- c: \\ mySymbols  
- c: \\ mySymbols \\ dll  
- c: \\ mySymbols \\ symbols \\ dll  

Der Symbolhandler verwendet diese Logik, um alle Pfadelemente zu  durchsuchen, die die Kriterien nicht erfüllen, um ein Symbolserver oder Cache *zu* sein (siehe unten).

### <a name="symbol-server-path-element"></a>SymbolServer Path-Element

Ein *Symbolserver-Pfadelement* verwendet eine spezielle Technologie, mit der ein Symbol gefunden werden kann, das genau mit dem in Frage gestellten Modul übereinstimmen kann. Weitere Informationen finden Sie unter Verwenden von [SymSrv.](using-symsrv.md)

Der Symbolhandler behandelt ein Path-Element als Symbolserver, wenn es mit dem Text "srv" \* beginnt.

> [!Note]  
> Wenn der Text "srv" nicht angegeben ist, das tatsächliche Pfadelement jedoch ein Symbolserverspeicher ist, dann wird der Symbolhandler so agieren, als wäre \* "srv" \* angegeben. Der Symbolhandler bestimmt dies, indem er im Stammverzeichnis des angegebenen Pfads nach einer Datei namens "pingme.txt" sucht.

 

### <a name="cache-path-element"></a>Cache Path-Element

Ein *Cachepfadelement* ist eine Variation eines Symbolserverpfadelements.

Dieses Verzeichnis wird wie jeder andere Symbolserver durchsucht. Wenn das Symbol hier jedoch nicht gefunden wird und es sich in einem Pfadelement weiter unten in der Kette des Symbolpfads befindet, wird das Symbol kopiert und auf dem in diesem Element angegebenen Symbolserver gespeichert.

Der Symbolhandler behandelt ein Path-Element als Cacheelement, wenn es mit dem Text "cache" \* beginnt. Um einen Cache in "c: myCache" anzugeben, verwenden Sie ein Symbolpfadelement \\ von "cache \* c: \\ myCache".

## <a name="example-search-path"></a>Beispiel für einen Suchpfad

Um zu sehen, wie dies funktioniert, legen Sie diesen Suchpfad fest.

`cache*c:\myCache;srv*\\symbols\symbols`

<!-- 
See example from https://docs.microsoft.com/windows-hardware/drivers/debugger/symbol-path
cache*c:\MySymbols;srv*https://msdl.microsoft.com/download/symbols
-->

Im Folgenden finden Sie eine Auflistung der ausführlichen Ausgabe des Symbolhandlers bei der Suche nach "ntdll.pdb" unter Verwendung des oben aufgeführten Suchpfads.

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

Die ersten drei Zeilen der Ausgabe zeigen den Symbolhandler, der das erste Pfadelement von `.` verarbeitet. Dies ist ein Standardpfadelement.

Die vierte Zeile zeigt den Symbolhandler, der den Symbolserver verwendet, um nach der Datei im zweiten Pfadelement von zu suchen, bei dem es sich `cache*c:\myCache` um ein Cachepfadelement handelt.

Die fünfte Zeile zeigt, dass die Datei im dritten Pfadelement von gefunden wird, bei dem `srv*\\symbols\symbols` es sich um ein Symbolserver-Pfadelement handelt.

Die sechste Zeile zeigt, dass die Datei in den Cache kopiert wird.

Die letzten beiden Zeilen, in denen die Datei aus dem Cache geöffnet wird.
