---
title: Aktivieren von STRICT
description: Wenn Sie das STRICT-Symbol definieren, aktivieren Sie Features, die beim Deklarieren und Verwenden von Typen mehr Sorgfalt erfordern.
ms.assetid: 4029c7a7-108a-40cb-8600-eb23968e9d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca6ca814d69910620b89095cc18be3b37601329dc053937d5772243097537c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561794"
---
# <a name="enabling-strict"></a>Aktivieren von STRICT

Wenn Sie das **STRICT-Symbol** definieren, aktivieren Sie Features, die beim Deklarieren und Verwenden von Typen mehr Sorgfalt erfordern. Dies hilft Ihnen, portableren Code zu schreiben. Diese zusätzliche Sorgfalt reduziert auch die Debugzeit. Durch aktivieren von **STRICT** werden bestimmte Datentypen neu definiert, sodass der Compiler die Zuweisung von einem Typ zu einem anderen ohne explizite Umwandlung nicht zulässt. Dies ist besonders hilfreich bei Windows Code. Fehler bei der Übergabe von Datentypen werden zur Kompilierzeit gemeldet, anstatt schwerwiegende Fehler zur Laufzeit zu verursachen.

Bei Visual C++ ist  die STRICT-Typüberprüfung standardmäßig definiert.

Um **STRICT** dateiweise zu definieren, fügen Sie eine **\# define-Anweisung** ein, bevor Sie Windows.h einschließen:


```C++
#define STRICT
#include <windows.h>
```



Wenn **STRICT** definiert ist, ändern sich [Datentypdefinitionen](windows-data-types.md) wie folgt:

-   Bestimmte Handletypen sind so definiert, dass sie sich gegenseitig ausschließen. Beispielsweise können Sie kein **HWND** übergeben, wenn ein **HDC-Typargument** erforderlich ist. Ohne **STRICT** werden alle Handles als **HANDLE** definiert, sodass der Compiler sie nicht daran hindert, einen Handletyp zu verwenden, bei dem ein anderer Typ erwartet wird.
-   Alle Rückruffunktionstypen (z. B. Dialogprozessen, Fensterprozessen und Hookprozessen) werden mit vollständigen Prototypen definiert. Dadurch wird verhindert, dass Rückruffunktionen mit falschen Parameterlisten deklariert werden.
-   Parameter- und Rückgabewerttypen, die einen generischen Zeiger verwenden sollten, werden ordnungsgemäß als **LPVOID** und nicht als **LPSTR** oder ein anderer Zeigertyp deklariert.
-   Die [**COMSTAT-Struktur**](/windows/desktop/api/winbase/ns-winbase-comstat) wird gemäß dem ANSI-Standard deklariert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Deaktivieren von STRICT](disabling-strict.md)
</dt> <dt>

[STRICT Compliance](strict-compliance.md)
</dt> </dl>

 

 
