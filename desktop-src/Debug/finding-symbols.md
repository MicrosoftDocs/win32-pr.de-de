---
description: Nachdem eine Symbol Datei in den Symbol Handler geladen wurde, kann eine Anwendung mit den symbollocatorfunktionen Symbol Informationen für eine angegebene Adresse zurückgeben.
ms.assetid: bfc068e1-eced-4ab2-80a3-acc2ed07c841
title: Suchen von Symbolen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f65830032cf363771b14f779726c59d976e8d30
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125701"
---
# <a name="finding-symbols"></a>Suchen von Symbolen

Nachdem eine Symbol Datei in den Symbol Handler geladen wurde, kann eine Anwendung mit den symbollocatorfunktionen Symbol Informationen für eine angegebene Adresse zurückgeben. Diese Funktionen können auch den Quell Code Dateinamen und den Speicherort der Zeilennummer für eine Adresse finden.

## <a name="enumerating-symbol-files"></a>Auflisten von Symbol Dateien

Rufen Sie die [**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules) -Funktion auf, um eine Liste aller durch den Modulnamen geladenen Symbol Dateien abzurufen. Ein Beispiel finden Sie unter Auflisten von [Symbol Modulen](enumerating-symbol-modules.md). Rufen Sie zum Abrufen einer Liste von Symbolen für ein bestimmtes Modul die [**symenumschlag Symbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) -Funktion auf. Ein Beispiel finden Sie unter Auflisten von [Symbolen](enumerating-symbols.md).

## <a name="retrieving-symbols-by-address"></a>Abrufen von Symbolen nach Adresse

Verwenden Sie die [**symfromaddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) -Funktion, um symbolische Informationen für eine bestimmte Adresse abzurufen. Diese Funktion Ruft Informationen ab und speichert Sie in einer [**Symbol \_ Informations**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) Struktur. Da Symbolnamen eine Variable Länge haben, müssen Sie nach der Deklaration der **Symbol \_ Info** Struktur zusätzlichen Pufferbereich bereitstellen. Ein Beispiel finden Sie unter [Abrufen von Symbol Informationen nach Adresse](retrieving-symbol-information-by-address.md).

Beachten Sie, dass sich die Adresse nicht an einer Symbol Grenze befinden muss. Wenn die Adresse nach dem Anfang eines Symbols, aber vor dem Ende des Symbols (dem Anfang des Symbols plus der Symbolgröße) liegt, wird das Symbol von der Funktion gefunden.

## <a name="retrieving-symbols-by-symbol-name"></a>Abrufen von Symbolen nach Symbol Name

Um symbolische Informationen in einer [**Symbol Informations \_**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) Struktur für ein bestimmtes Modul und einen Symbolnamen abzurufen, verwenden Sie die [**symfromname**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) -Funktion. Wenn verzögertes Laden von Symbolen festgelegt ist, versucht **symfromname** , die Symbol Datei für ein Modul zu laden, wenn es nicht bereits geladen wurde. Um einen Modulnamen zusammen mit einem Symbolnamen anzugeben, verwenden Sie das Syntax *Modul*! *Symname*. Das Zeichen "!" begrenzt den Modulnamen vom Symbolnamen. Ein Beispiel finden Sie unter [Abrufen von Symbol Informationen nach Name](retrieving-symbol-information-by-name.md).

## <a name="retrieving-line-numbers-by-address"></a>Abrufen von Zeilennummern nach Adresse

Verwenden Sie die [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) -Funktion, um den Quell Code Speicherort für eine bestimmte Adresse abzurufen. Diese Funktion füllt eine [**imagehlp \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) -Struktur, die den Quell Dateinamen und den Speicherort der Zeilennummer enthält, auf die von der angegebenen Adresse verwiesen wird. Ein Beispiel finden Sie unter [Abrufen von Symbol Informationen nach Adresse](retrieving-symbol-information-by-address.md).

## <a name="retrieving-line-numbers-by-symbol-name"></a>Abrufen von Zeilennummern nach Symbol Name

Verwenden Sie die [**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) -Funktion, um den Quell Code Speicherort für einen bestimmten Symbolnamen abzurufen. Diese Funktion ähnelt [**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname), aber Ruft eine [**imagehlp \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) -Struktur ab. Wenn Sie [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) oder **SymGetLineFromName64** verwenden möchten, müssen Sie die Option zum Laden von Zeilen (symopt- \_ Auslastungs \_ Linien) mithilfe der [**symsetoptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) -Funktion festlegen. Ein Beispiel finden Sie unter [Abrufen von Symbol Informationen nach Name](retrieving-symbol-information-by-name.md).

 

 



