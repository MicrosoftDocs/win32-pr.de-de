---
description: Im folgenden Beispiel wird die Arbeitsstation mithilfe der LockWorkStation-Funktion gesperrt. Das System zeigt das Dialogfeld Arbeitsstation sperren an. Der Text des Dialogfelds besagt, dass die Arbeitsstation verwendet wird und vom Benutzer gesperrt wurde.
ms.assetid: 7cbf9a0a-dfab-42e6-9a71-bb240121f59f
title: Sperren der Arbeitsstation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b349a3e41cf7a8059cb24fc0c3ade66d179777e70fbd84bd21cac3d46502f1cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117963807"
---
# <a name="how-to-lock-the-workstation"></a>Sperren der Arbeitsstation

Im folgenden Beispiel wird die Arbeitsstation mithilfe der [**LockWorkStation-Funktion**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation) gesperrt. Das System zeigt das Dialogfeld **Arbeitsstation sperren** an. Der Text des Dialogfelds besagt, dass die Arbeitsstation verwendet wird und vom Benutzer gesperrt wurde.


```C++
#include <windows.h>
#include <stdio.h>

#pragma comment( lib, "user32.lib" )

void main()
{
    // Lock the workstation.

    if( !LockWorkStation() )
        printf ("LockWorkStation failed with %d\n", GetLastError());
}
```



Um zu bestimmen, ob die Arbeitsstation gesperrt ist, testen Sie, ob das Fenster sichtbar ist.

Die Arbeitsstation kann vom Benutzer oder einem Administrator entsperrt werden. Drücken Sie STRG+ALT+ENTF, und melden Sie sich an, um das System zu entsperren. Um Benachrichtigungen zu erhalten, wenn sich der Benutzer anmeldet, verwenden Sie die [**WTSRegisterSessionNotification-Funktion,**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) um sich für den Empfang von [**WM \_ WTSSESSION \_ CHANGE-Meldungen**](../termserv/wm-wtssession-change.md) zu registrieren. Wenn diese Meldung empfangen wird, überprüfen Sie, ob der *wParam-Parameter* gleich WTS \_ SESSION LOCK \_ ist.

 

 
