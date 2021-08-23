---
description: Um Zeit und Arbeitsspeicher bei der Arbeit mit vielen Symboldateien zu sparen, verwenden Sie die Funktion SymSetOptions, um die Option verzögertes Laden von Symbolen (SYMOPT \_ DEFERRED \_ LOADS) festzulegen.
ms.assetid: 40c9384f-00ed-40cd-9687-b76b69e74f87
title: Verzögertes Laden von Symbolen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8682de9ac8eaea78e037bf85ea8a17cd88e63bb56468ab39df3d1887fcc66801
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957149"
---
# <a name="deferred-symbol-loading"></a>Verzögertes Laden von Symbolen

Um Zeit und Arbeitsspeicher bei der Arbeit mit vielen Symboldateien zu sparen, verwenden Sie die [**Funktion SymSetOptions,**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) um die Option verzögertes Laden von Symbolen (SYMOPT \_ DEFERRED \_ LOADS) festzulegen, und verwenden Sie dann die [**Funktion SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) oder [**SymInitialize,**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) um Symbole zu laden, die für alle Module zurückgestellt sind. Der Symbolhandler listet Symbole auf, die für die Module verfügbar sind, aber die Debuginformationen werden erst im Arbeitsspeicher zugeordnet, wenn sie angefordert werden. Dies ist die bevorzugte Methode zur effizienten Verwendung von Debugsymbolen. Alle Funktionen, die Symbole verwenden, sind vom verzögerten Laden von Symbolen betroffen.

 

 



