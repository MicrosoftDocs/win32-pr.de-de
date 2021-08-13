---
title: Registrieren einer Hookfunktion
description: Clientanwendungen empfangen WinEvents in einer WinEventProc-Rückruffunktion. Die von der Rückruffunktion ausgeführten Aktionen werden von der Anwendung definiert, die Syntax muss jedoch wie im Prototyp angegeben sein.
ms.assetid: 7e999335-6a41-4d22-82ef-1a8dd6cb656e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c444d2ee291cb07386e775a649ba0c3d42486c45b70e4d3f4629b9b67274f89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118564650"
---
# <a name="registering-a-hook-function"></a>Registrieren einer Hookfunktion

Clientanwendungen empfangen WinEvents in einer [*WinEventProc-Rückruffunktion.*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) Die von der Rückruffunktion ausgeführten Aktionen werden von der Anwendung definiert, die Syntax muss jedoch wie im Prototyp angegeben sein.

Bevor ereignisse empfangen werden können, muss die Funktion durch Aufrufen von [**SetWinEventHook registriert werden.**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) Der Client kann **SetWinEventHook** mehr als einmal aufrufen, um verschiedene Hookfunktionen zu registrieren oder zusätzliche Ereignisse für eine zuvor registrierte Hookfunktion zu festlegen.

Beim Aufrufen [**von SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) gibt der Client an, welche Ereignisse empfangen und wie sie empfangen werden sollen. Der Client hat die folgenden Auswahl:

-   Empfangen aller Ereignisse oder einer bestimmten Gruppe von Ereignissen.
-   Empfangen von Ereignissen von allen Threads oder von einem bestimmten Thread.
-   Empfangen von Ereignissen von allen Prozessen oder von einem bestimmten Prozess.
-   Behandeln von Ereignissen im Prozess oder out of process.

Wenn ein Ereignis generiert wird, das den angegebenen Kriterien entspricht, ruft das System die [*WinEventProc-Rückruffunktion*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) (oder "Hookprozedur") des Clients auf. Die Parameter, die die Hookfunktion empfängt, informieren den Client über das Fenster, das Objekt und das mögliche untergeordnete Element, das das Ereignis generiert hat. Ein Client verwendet diese Parameter in einem Objektabrufaufruf, z. B. [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).

 

 




