---
description: Der Symbolhandler dient zum Nachverfolgen verschiedener Sätze von Symboldateien.
ms.assetid: 1bd7ac25-e46d-442b-b365-52edcd8bf922
title: Initialisierung des Symbolhandlers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9d3664a564b0198d97549f2815abebf0e5e6058beb197ed33ca191a64407f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406080"
---
# <a name="symbol-handler-initialization"></a>Initialisierung des Symbolhandlers

Der Symbolhandler dient zum Nachverfolgen verschiedener Sätze von Symboldateien.

Um den Symbolhandler zu initialisieren, rufen Sie die [**SymInitialize-Funktion**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) auf. Der *hProcess-Parameter* kann eine eindeutige beliebige Zahl, ein von der [**GetCurrentProcess-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) zurückgegebener Wert oder der Bezeichner eines ausgeführten Prozesses sein. Der *fInvadeProcess-Parameter* gibt an, ob der Symbolhandler die vom Prozess geladenen Module aufzählen und Symbole für jedes seiner Module laden soll. Wenn *fInvadeProcess* **true ist,** muss der *hProcess-Parameter* der von **GetCurrentProcess** zurückgegebene Wert oder der Bezeichner eines vorhandenen Prozesses sein. Um diese Liste zu aktualisieren, verwenden Sie die [**SymRefreshModuleList-Funktion.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist)

Die *Verwendung von fInvadeProcess* ist eine einfache Möglichkeit, alle Symboldateien für einen Prozess zu laden. Der Symbolhandler versucht jedoch nicht, Symbole für Module zu laden, die anschließend von der [**LoadLibrary-Funktion geladen**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) werden. In diesem Fall müssen [**Sie die SymLoadModuleEx-Funktion**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) verwenden.

 

 
