---
description: Um beim Arbeiten mit vielen Symbol Dateien Zeit und Arbeitsspeicher zu sparen, verwenden Sie die symsetoptions-Funktion, um das verzögerte Laden von Symbolen (symopt verzögert \_ \_ Loads) festzulegen.
ms.assetid: 40c9384f-00ed-40cd-9687-b76b69e74f87
title: Verzögerte Symbol Ladevorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d64d05a3ad7ad0fe4017f1ba6fa99625af33c2cc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958136"
---
# <a name="deferred-symbol-loading"></a>Verzögerte Symbol Ladevorgänge

Um beim Arbeiten mit vielen Symbol Dateien Zeit und Arbeitsspeicher zu sparen, verwenden Sie die [**symsetoptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) -Funktion, um das verzögerte Laden von Symbolen (symopt-verzögertes Laden) festzulegen \_ , und verwenden Sie \_ dann die [**symloadmoduleex**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) -oder [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) -Funktion zum Laden von Symbolen, die für alle Module Der Symbol Handler listet Symbole auf, die für die Module verfügbar sind. die Debuginformationen werden jedoch erst dann in den Arbeitsspeicher aufgenommen, wenn Sie angefordert werden. Dies ist die bevorzugte Methode zur effizienten Verwendung von Debugsymbolen. Alle Funktionen, die Symbole verwenden, sind von verzögertem Laden von Symbolen betroffen.

 

 



