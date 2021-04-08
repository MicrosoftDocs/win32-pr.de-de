---
title: Registrieren einer Hook-Funktion
description: Client Anwendungen empfangen WinEvents in einer wineventproc-Rückruffunktion. Die von der Rückruffunktion ausgeführten Aktionen werden von der Anwendung definiert, aber die Syntax muss wie im Prototyp angegeben angegeben werden.
ms.assetid: 7e999335-6a41-4d22-82ef-1a8dd6cb656e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b1f39a535b366af72b1034cc9344171d253ea0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855779"
---
# <a name="registering-a-hook-function"></a>Registrieren einer Hook-Funktion

Client Anwendungen empfangen WinEvents in einer [*wineventproc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) -Rückruffunktion. Die von der Rückruffunktion ausgeführten Aktionen werden von der Anwendung definiert, aber die Syntax muss wie im Prototyp angegeben angegeben werden.

Bevor Ereignisse empfangen werden können, muss die Funktion durch Aufrufen von [**setwineventhook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook)registriert werden. Der Client kann **setwineventhook** mehrmals aufrufen, um unterschiedliche Hook-Funktionen zu registrieren oder zusätzliche Ereignisse für eine zuvor registrierte Hook-Funktion festzulegen.

Beim Aufrufen von [**setwineventhook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) gibt der Client an, welche Ereignisse empfangen werden sollen und wie diese empfangen werden. Der Client kann Folgendes auswählen:

-   Empfangen Sie alle Ereignisse oder einen bestimmten Satz von Ereignissen.
-   Empfangen von Ereignissen von allen Threads oder von einem bestimmten Thread.
-   Empfangen von Ereignissen von allen Prozessen oder von einem bestimmten Prozess.
-   Behandeln von Ereignissen in Prozessen oder außerhalb des Prozesses.

Wenn ein Ereignis generiert wird, das den angegebenen Kriterien entspricht, ruft das System die [*wineventproc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) -Rückruffunktion (oder "Hook Procedure") des Clients auf. Die Parameter, die die Hook-Funktion empfängt, informieren den Client über das Fenster, das Objekt und das mögliche untergeordnete Element, das das Ereignis generiert hat. Ein Client verwendet diese Parameter in einem Objekt Abruf Aufrufs, z. [**b. accessibleobjectfromevent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).

 

 




