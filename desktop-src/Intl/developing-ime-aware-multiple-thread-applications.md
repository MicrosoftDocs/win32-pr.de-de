---
description: Der IMM enthält eine Threadidentifikationsüberprüfung, die bestimmt, ob ein aufrufende Thread der Ersteller eines angegebenen Eingabemethode-Kontexthandks (HIMC-Typ) oder Fensterhand handle (HWND-Typ) ist.
ms.assetid: da55d6fe-a620-4ea7-9055-91bcd3233267
title: Entwickeln IME-Aware Anwendungen mit mehreren Threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf495922d347119db3b8b517af13c850f2f19dfc558609f93f24953f0a3386a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949595"
---
# <a name="developing-ime-aware-multiple-thread-applications"></a>Entwickeln IME-Aware Anwendungen mit mehreren Threads

Der IMM enthält eine Threadidentifikationsüberprüfung, die bestimmt, ob ein aufrufende Thread der Ersteller eines angegebenen Eingabemethode-Kontexthandks (HIMC-Typ) oder Fensterhand handle (HWND-Typ) ist. Wenn der Thread nicht der Ersteller des Handles ist, schlägt die aufgerufene IMM-Funktion fehl, und ein nachfolgender Aufruf von [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt ERROR \_ INVALID ACCESS \_ zurück.

> [!Note]  
> Die aktuelle IMM-Architektur bietet keine Synchronisierungsmöglichkeit für den Zugriff auf IMM-Handles.

 

Um die Threadidentifikationsüberprüfung zu verwenden, müssen Ihre Anwendungen die folgenden Richtlinien einhalten:

-   Ein Thread sollte nicht auf den Eingabekontext zugreifen, der von einem anderen Thread erstellt wurde.
-   Ein Thread sollte einem fenster, das von einem anderen Thread erstellt wurde, keinen Eingabekontext zuordnen und umgekehrt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Eingabemethode-Managers](using-input-method-manager.md)
</dt> </dl>

 

 
