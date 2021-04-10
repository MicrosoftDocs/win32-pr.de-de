---
description: Der Symbol Handler dient zum Nachverfolgen verschiedener Sätze von Symbol Dateien.
ms.assetid: 1bd7ac25-e46d-442b-b365-52edcd8bf922
title: Initialisierung von Symbol Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 146af0e1118e85a3478ca45be7a86c4b1d8dfe83
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126050"
---
# <a name="symbol-handler-initialization"></a>Initialisierung von Symbol Handlern

Der Symbol Handler dient zum Nachverfolgen verschiedener Sätze von Symbol Dateien.

Zum Initialisieren des Symbol Handlers wird die [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) -Funktion aufgerufen. Der *hProcess* -Parameter kann eine eindeutige beliebige Zahl, ein Wert, der von der [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) -Funktion zurückgegeben wird, oder der Bezeichner eines beliebigen laufenden Prozesses sein. Der *finvadeprocess* -Parameter gibt an, ob der Symbol Handler die vom Prozess geladenen Module aufzählen und Symbole für die einzelnen Module laden soll. Wenn *finvadeprocess* auf **true** festgelegt ist, muss der *hProcess* -Parameter der von **GetCurrentProcess** zurückgegebene Wert oder der Bezeichner eines vorhandenen Prozesses sein. Um diese Liste zu aktualisieren, verwenden Sie die [**symrefresh modulelist**](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist) -Funktion.

Die Verwendung von *finvadeprocess* ist eine einfache Möglichkeit, alle Symbol Dateien für einen Prozess zu laden. Der Symbol Handler versucht jedoch nicht, Symbole für Module zu laden, die anschließend von der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion geladen werden. In diesem Fall müssen Sie die [**symloadmoduleex**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) -Funktion verwenden.

 

 
