---
description: Die Funktionen für die Symbolverarbeitung der DbgHelp-API haben sich im Laufe der Jahre weiterentwickelt.
ms.assetid: 6dc41682-6104-418b-b045-7afe8c2b11e9
title: Öffentliche, globale und lokale Symbole
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ecaa40549b091af204f2e318aefef8a256408e5f81b461e63a54c333719dd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406100"
---
# <a name="public-global-and-local-symbols"></a>Öffentliche, globale und lokale Symbole

Die Funktionen für die Symbolverarbeitung der DbgHelp-API haben sich im Laufe der Jahre weiterentwickelt. Um sicherzustellen, dass Ihr Code in einer Vielzahl von Szenarien funktioniert und vollständige Details zu den Symbolen bereitstellt, verwenden Sie nach Möglichkeit die neuesten Funktionen. [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) ersetzt beispielsweise [**SymEnumerateSymbols64,**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols) [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) ersetzt [**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)und [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) ersetzt [**SymGetSymFromAddr64.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr)

## <a name="public-symbols"></a>Öffentliche Symbole

Anfängliche Versionen von DbgHelp.dll die ausschließliche Untersuchung öffentlicher Symbole unterstützt. Diese Symbole werden für jedes Element im Code generiert, das zwischen verschiedenen Quelldateien verfügbar gemacht werden muss. Sie enthalten auch alle Elemente, die aus dem Modul exportiert werden.

Die Symbole werden entweder in das Bild eingebettet oder separat in einer DBG- oder PDB-Datei gespeichert. Die einzigen gespeicherten Informationen sind der Symbolname und die Adresse. Die Namen sind als ergänzte Namen verfügbar. Um nicht korrigierte Namen anzuzeigen, rufen Sie die [**SymSetOptions-Funktion**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) mit SYMOPT \_ UNDNAME auf, oder verwenden Sie die [**UnDecorateSymbolName-Funktion.**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname)

Beachten Sie, dass die DbgHelp-API anfänglich nicht für die Unterstützung mehrerer Instanzen desselben Symbols innerhalb eines Moduls konzipiert wurde. Dies liegt daran, dass öffentliche Symbole auf eindeutige Namen innerhalb eines Moduls beschränkt sind. Daher gibt [**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname) nur das erste übereinstimmende Symbol zurück. Um alle übereinstimmenden Symbole abzurufen, rufen Sie [**SymEnumSymbols auf.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols)

## <a name="global-and-local-symbols"></a>Globale und lokale Symbole

Neuere Versionen von DbgHelp.dll unterstützen globale und lokale Symbole, wenn PDB-Dateien verwendet werden. Diese neuen Versionen umfassen statische Funktionen, Funktionen, die in einer Quelldatei enthalten sind, Funktionsparameter und lokale Variablen. Wenn DbgHelp nach einem Symbol sucht, überprüft es die globalen und lokalen Symboltabellen, bevor die öffentliche Symboltabelle überprüft wird. Dies liegt daran, dass für diese Symboltypen mehr Informationen als für öffentliche Symbole verfügbar sind.

Globale und lokale Symbole werden mit nicht korrigierten Namen gespeichert. Daher hat das SYMOPT \_ UNDNAME-Flag keine Auswirkungen. Um ergänzte Symbolnamen zu erhalten, müssen Sie das FLAG SYMOPT \_ PUBLICS \_ ONLY verwenden. Dadurch sucht DbgHelp nur nach den öffentlichen Symbolen.

Um lokale Symbole oder Funktionsparameter anzuzeigen, rufen Sie die [**SymSetContext-Funktion**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetcontext) auf, wobei der **InstructionOffset-Member** der [**IMAGEHLP \_ STACK \_ FRAME-Struktur**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_stack_frame) auf die Adresse eines beliebigen Funktionssymbols festgelegt ist. Nachfolgende Aufrufe von [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) und [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) können im Kontext dieser Adresse ausgeführt werden. Legen Sie hierzu den *BaseOfDll-Parameter* auf **NULL** fest, und lassen Sie den Modulspezifizierer aus dem *Parameter Name* oder *Mask* aus. Dies zwingt DbgHelp, innerhalb des durch **SymSetContext** angegebenen Bereichs nach übereinstimmenden Symbolen zu suchen.

Um zu bestimmen, ob ein Symbol ein Parameter ist, überprüfen Sie den **Flags-Member** der [**SYMBOL \_ INFO-Struktur.**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) Wenn das Symbol ein Parameter ist, enthält der Member SYMFLAG \_ PARAMETER. Wenn es sich um ein lokales Symbol handelt, enthält das Element SYMFLAG \_ LOCAL.

 

 



