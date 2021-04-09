---
description: Im folgenden Beispiel wird die Arbeitsstation mithilfe der Lock Workstation-Funktion gesperrt. Das System zeigt das Dialogfeld Arbeitsstation sperren an. Der Dialogfeld Text besagt, dass die Arbeitsstation verwendet wird und vom Benutzer gesperrt wurde.
ms.assetid: 7cbf9a0a-dfab-42e6-9a71-bb240121f59f
title: Vorgehensweise beim Sperren der Arbeitsstation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa6c198816613a13914c44a5a51f5317e2019f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865712"
---
# <a name="how-to-lock-the-workstation"></a>Vorgehensweise beim Sperren der Arbeitsstation

Im folgenden Beispiel wird die Arbeitsstation mithilfe der [**Lock Workstation**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation) -Funktion gesperrt. Das System zeigt das Dialogfeld **Arbeitsstation sperren** an. Der Dialogfeld Text besagt, dass die Arbeitsstation verwendet wird und vom Benutzer gesperrt wurde.


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



Überprüfen Sie, ob das Fenster sichtbar ist, um zu bestimmen, ob die Arbeitsstation gesperrt ist.

Die Arbeitsstation kann vom Benutzer oder einem Administrator entsperrt werden. Drücken Sie zum Entsperren des Systems STRG + ALT + ENTF, und melden Sie sich an. Um bei der Anmeldung des Benutzers eine Benachrichtigung zu erhalten, verwenden Sie die [**wzregistersessionnotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) -Funktion, um sich für den Empfang von [**WM- \_ \_ Änderungs**](../termserv/wm-wtssession-change.md) Nachrichten zu registrieren. Wenn diese Meldung empfangen wird, überprüfen Sie, ob der *wParam* -Parameter gleich der WTS- \_ Sitzungs \_ Sperre ist.

 

 
