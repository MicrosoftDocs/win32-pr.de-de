---
description: Die in der C-Laufzeit enthaltenen Zeitfunktionen verwenden den Time \_ t-Typ zur Darstellung der Anzahl von Sekunden, die seit Mitternacht des 1. Januar 1970 verstrichen sind. Im folgenden Beispiel wird ein Time \_ t-Wert mithilfe der Int32x32To64-Funktion in eine Datei Zeit konvertiert.
ms.assetid: f626c0b2-a5a1-475d-9a24-64e7b0407278
title: Wandeln eines time_t Werts in eine Datei Zeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee866efaed716fb12d2501337236afdb7cf641b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366269"
---
# <a name="converting-a-time_t-value-to-a-file-time"></a>Umrechnen eines time \_ t-Werts in eine Datei Zeit

Die in der C-Laufzeit enthaltenen Zeitfunktionen verwenden den Time \_ t-Typ zur Darstellung der Anzahl von Sekunden, die seit Mitternacht des 1. Januar 1970 verstrichen sind. Im folgenden Beispiel wird ein Time \_ t-Wert mithilfe der [**Int32x32To64**](/windows/desktop/api/winnt/nf-winnt-int32x32to64) -Funktion in eine Datei Zeit konvertiert.


```C++
#include <windows.h>
#include <time.h>

void TimetToFileTime( time_t t, LPFILETIME pft )
{
    LONGLONG ll = Int32x32To64(t, 10000000) + 116444736000000000;
    pft->dwLowDateTime = (DWORD) ll;
    pft->dwHighDateTime = ll >>32;
}
```



Nachdem Sie einen dateizeitpunkt erhalten haben, können Sie diesen Wert mithilfe der [**filetimedesystemtime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime) -Funktion in Systemzeit konvertieren.

 

 
