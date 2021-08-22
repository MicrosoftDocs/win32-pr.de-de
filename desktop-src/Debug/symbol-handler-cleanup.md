---
description: Verwenden Sie die SymCleanup-Funktion, um den gesamten vom Symbolhandler für einen Prozess verwendeten Arbeitsspeicher freizugeben.
ms.assetid: d442b2f2-9225-43fd-bd25-274322857834
title: Symbolhandlerbereinigung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6db42f1fedfe68af4ab6eab885aefff0e8eb56e4ac9262f79adef8733f7ee7d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956959"
---
# <a name="symbol-handler-cleanup"></a>Symbolhandlerbereinigung

Verwenden Sie die [**SymCleanup-Funktion,**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) um den gesamten vom Symbolhandler für einen Prozess verwendeten Arbeitsspeicher freizugeben. Diese Funktion listet alle geladenen Module auf, gibt jedes Modul frei und gibt den für die Liste der Module belegten Arbeitsspeicher frei. Nachdem Sie **SymCleanup** aufgerufen haben, können Sie das Prozesshandle erst dann in den Symbolbehandlungsfunktionen verwenden, wenn Sie die [**SymInitialize-Funktion**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) aufrufen.

 

 



