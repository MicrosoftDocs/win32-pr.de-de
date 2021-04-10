---
description: Das ordnungsgemäße Einrichten von Symbolen für das Debuggen kann eine schwierige Aufgabe sein, insbesondere für das Kernel Debugging.
ms.assetid: 96b2c9db-58fb-4c28-b17c-3b1cc06ed96b
title: "  Symbolserver und Symbolspeicher"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 644410fcb929308a259c5fc752f55742bfb23bae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214103"
---
# <a name="symbol-server-and-symbol-stores"></a>  Symbolserver und Symbolspeicher

Das ordnungsgemäße Einrichten von Symbolen für das Debuggen kann eine schwierige Aufgabe sein, insbesondere für das Kernel Debugging. Häufig ist es erforderlich, dass Sie die Namen und Releases aller Produkte auf Ihrem Computer kennen. Der Debugger muss in der Lage sein, die Symbol Dateien zu finden, die den einzelnen Produkt Releases und Service Pack entsprechen. Dies kann zu einem extrem langen Symbol Pfad führen, der aus einer langen Liste von Verzeichnissen besteht.

Verwenden Sie den *Symbol Server*, um diese Schwierigkeiten beim koordinieren von Symbol Dateien zu vereinfachen. Der Symbol Server ermöglicht den Debuggern das automatische Abrufen der richtigen Symbol Dateien ohne Produktnamen, Releases oder Buildnummern. Debugtools für Windows enthalten den SymSrv-Symbol Server.

Der Symbol Server wird aktiviert, indem eine bestimmte Text Zeichenfolge in den Symbol Pfad eingeschlossen wird. Jedes Mal, wenn der Debugger Symbole für ein neu geladenes Modul laden muss, ruft er den Symbol Server auf, um die entsprechenden Symbol Dateien zu suchen. Der Symbol Server verwendet die Dateien in einem *Symbol Speicher*. Dies ist eine Sammlung von Symbol Dateien, einem Index und einem Tool, das von einem Administrator zum Hinzufügen und Löschen von Dateien verwendet werden kann. Die Dateien werden nach eindeutigen Parametern, wie z. b. Zeitstempel und Bildgröße, indiziert. Debugtools für Windows enthalten ein Symbol Speicher Tool namens SymStore.

Weitere Informationen finden Sie unter

-   [Verwenden von SymSrv](using-symsrv.md)
-   [Verwenden von SymStore](using-symstore.md)
-   [Verwenden anderer Symbol Speicher](using-other-symbol-stores.md)
-   [Optionen für SymStore-Command-Line](symstore-command-line-options.md)
-   [Symbol Server und Internet Firewalls](symbol-servers-and-internet-firewalls.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Symbol Dateien](symbol-files.md)
</dt> </dl>

 

 



