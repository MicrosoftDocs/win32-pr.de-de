---
description: Nachdem eine Symboldatei in den Symbolhandler geladen wurde, kann eine Anwendung mithilfe der Symbollocatorfunktionen Symbolinformationen für eine angegebene Adresse zurückgeben.
ms.assetid: bfc068e1-eced-4ab2-80a3-acc2ed07c841
title: Suchen von Symbolen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a90aae9d2894ca8abc7470b2068b508655a50bcb76e1a122f2307f81273abec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912699"
---
# <a name="finding-symbols"></a>Suchen von Symbolen

Nachdem eine Symboldatei in den Symbolhandler geladen wurde, kann eine Anwendung mithilfe der Symbollocatorfunktionen Symbolinformationen für eine angegebene Adresse zurückgeben. Diese Funktionen können auch einen Quellcodedateinamen und einen Zeilennummerspeicherort für eine Adresse finden.

## <a name="enumerating-symbol-files"></a>Aufzählen von Symboldateien

Rufen Sie die [**SymEnumerateModules64-Funktion**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules) auf, um eine Liste aller Symboldateien abzurufen, die durch den Modulnamen geladen wurden. Ein Beispiel finden Sie unter [Aufzählen von Symbolmodulen.](enumerating-symbol-modules.md) Um eine Liste von Symbolen für ein bestimmtes Modul abzurufen, rufen Sie die [**SymEnumSymbols-Funktion**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) auf. Ein Beispiel finden Sie unter [Aufzählen von Symbolen.](enumerating-symbols.md)

## <a name="retrieving-symbols-by-address"></a>Abrufen von Symbolen nach Adresse

Verwenden Sie die [**SymFromAddr-Funktion,**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) um symbolische Informationen für eine bestimmte Adresse abzurufen. Diese Funktion ruft Informationen ab und speichert sie in einer [**SYMBOL \_ INFO-Struktur.**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) Da Symbolnamen eine variable Länge haben, müssen Sie zusätzlichen Pufferspeicher nach der **SYMBOL \_ INFO-Strukturdeklaration** bereitstellen. Ein Beispiel finden Sie unter [Abrufen von Symbolinformationen nach Adresse.](retrieving-symbol-information-by-address.md)

Beachten Sie, dass sich die Adresse nicht an einer Symbolgrenze befinden muss. Wenn die Adresse nach dem Anfang eines Symbols, aber vor dem Ende des Symbols (dem Anfang des Symbols plus der Symbolgröße) liegt, sucht die Funktion nach dem Symbol.

## <a name="retrieving-symbols-by-symbol-name"></a>Abrufen von Symbolen nach Symbolname

Verwenden Sie die [**SymFromName-Funktion,**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) um symbolische Informationen in einer [**SYMBOL \_ INFO-Struktur**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) für ein bestimmtes Modul und einen Symbolnamen abzurufen. Wenn verzögertes Laden von Symbolen festgelegt ist, versucht **SymFromName,** die Symboldatei für ein Modul zu laden, wenn es noch nicht geladen wurde. Um einen Modulnamen zusammen mit einem Symbolnamen anzugeben, verwenden Sie die Syntax *Module*! *SymName*. Das Zeichen "!" begrenzt den Modulnamen vom Symbolnamen. Ein Beispiel finden Sie unter [Abrufen von Symbolinformationen nach Name](retrieving-symbol-information-by-name.md).

## <a name="retrieving-line-numbers-by-address"></a>Abrufen von Zeilennummern nach Adresse

Verwenden Sie die [**SymGetLineFromAddr64-Funktion,**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) um den Quellcodespeicherort für eine bestimmte Adresse abzurufen. Diese Funktion füllt eine [**IMAGEHLP \_ LINE64-Struktur**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) aus, die den Quelldateinamen und den Speicherort der Zeilennummer enthält, auf die von der angegebenen Adresse verwiesen wird. Ein Beispiel finden Sie unter [Abrufen von Symbolinformationen nach Adresse.](retrieving-symbol-information-by-address.md)

## <a name="retrieving-line-numbers-by-symbol-name"></a>Abrufen von Zeilennummern nach Symbolname

Verwenden Sie die [**SymGetLineFromName64-Funktion,**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) um den Quellcodespeicherort für einen bestimmten Symbolnamen abzurufen. Diese Funktion ähnelt [**SymGetSymFromName64,**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)ruft jedoch eine [**IMAGEHLP \_ LINE64-Struktur**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) ab. Um [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) oder **SymGetLineFromName64** zu verwenden, müssen Sie die Load Lines-Option (SYMOPT LOAD LINES) mithilfe der \_ \_ [**SymSetOptions-Funktion**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) festlegen. Ein Beispiel finden Sie unter [Abrufen von Symbolinformationen nach Name](retrieving-symbol-information-by-name.md).

 

 



