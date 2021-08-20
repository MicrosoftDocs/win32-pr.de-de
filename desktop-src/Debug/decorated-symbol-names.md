---
description: Ein verzierter Symbolname enthält Zeichen, die unterscheiden, wie ein öffentliches Symbol deklariert wurde.
ms.assetid: f02fa21d-3fe9-4838-a938-3136c34bc0e8
title: Verzierte Symbolnamen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60432788b69f0c8779030f32a190ccfb55859434f714a13f769b328ee246a309
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076414"
---
# <a name="decorated-symbol-names"></a>Verzierte Symbolnamen

Ein verzierter Symbolname enthält Zeichen, die unterscheiden, wie ein öffentliches Symbol deklariert wurde. Bei stdcall-Funktionen enthalten Namen das @-Zeichen und eine Dezimalzahl, die die Anzahl von Bytes \_ \_ in den Funktionsparametern angibt. Der verzierte Name der [**LoadLibrary-Funktion ist**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) beispielsweise LoadLibrary@4 . Bei C++-Funktionen ist die Namensdekoration komplexer und variiert von Compiler zu Compiler.

Verwenden Sie zum Abrufen des nicht gekennzeichneten Symbolnamens die [**UnDecorateSymbolName-Funktion.**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) Alternativ können Sie die [**SymSetOptions-Funktion**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) aufrufen, um an fordern, dass der Symbolhandler immer Symbole mit nicht korkorrekturierten Namen präsentiert. Sie müssen diese Option festlegen, bevor Sie die Symbole laden, da der Symbolhandler die Symbolnamentabellen zur Ladezeit erstellt.

 

 
