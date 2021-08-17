---
description: Die in der C-Laufzeit enthaltenen Zeitfunktionen verwenden den Zeittyp t, um die Anzahl der Sekunden seit \_ Mitternacht, dem 1. Januar 1970, zu repräsentieren. Im folgenden Beispiel wird ein Time \_ t-Wert mithilfe der Int32x32To64-Funktion in eine Dateizeit konvertiert.
ms.assetid: f626c0b2-a5a1-475d-9a24-64e7b0407278
title: Konvertieren eines time_t werts in eine Dateizeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30fc7161e55bb235690f5c7d5fe0f4cd575bd7c902d5357606290def0509f6b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764511"
---
# <a name="converting-a-time_t-value-to-a-file-time"></a>Konvertieren eines \_ Zeitwerts in eine Dateizeit

Die in der C-Laufzeit enthaltenen Zeitfunktionen verwenden den Zeittyp t, um die Anzahl der Sekunden seit \_ Mitternacht, dem 1. Januar 1970, zu repräsentieren. Im folgenden Beispiel wird ein Time \_ t-Wert mithilfe der [**Int32x32To64-Funktion in**](/windows/desktop/api/winnt/nf-winnt-int32x32to64) eine Dateizeit konvertiert.


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



Nachdem Sie eine Dateizeit erhalten haben, können Sie diesen Wert mithilfe der [**FileTimeToSystemTime-Funktion in die Systemzeit**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime) konvertieren.

 

 
