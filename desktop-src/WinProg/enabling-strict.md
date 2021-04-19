---
title: Aktivieren von Strict
description: Wenn Sie das Strict-Symbol definieren, aktivieren Sie Features, die beim Deklarieren und Verwenden von Typen mehr Sorgfalt erfordern.
ms.assetid: 4029c7a7-108a-40cb-8600-eb23968e9d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0400b67025f11dc9c58553f6835b2a8e2b36b4c
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "106351186"
---
# <a name="enabling-strict"></a>Aktivieren von Strict

Wenn Sie das **Strict** -Symbol definieren, aktivieren Sie Features, die beim Deklarieren und Verwenden von Typen mehr Sorgfalt erfordern. Dies hilft Ihnen beim Schreiben von portablen Code. Dadurch wird auch die Debugzeit reduziert. Durch das Aktivieren von **Strict** werden bestimmte Datentypen definiert, sodass der Compiler keine Zuweisung von einem Typ zu einem anderen ohne explizite Umwandlung zulässt. Dies ist insbesondere bei Windows-Code hilfreich. Fehler beim Übergeben von Datentypen werden zur Kompilierzeit gemeldet, anstatt schwerwiegende Fehler zur Laufzeit zu verursachen.

Bei Visual C++ ist die **strikte** Typüberprüfung standardmäßig definiert.

Um **Strict** für eine Datei zu definieren, fügen Sie eine **\# define** -Anweisung ein, bevor Sie Windows. h einschließen:


```C++
#define STRICT
#include <windows.h>
```



Wenn **Strict** definiert ist, ändern sich die [Datentyp](windows-data-types.md) Definitionen wie folgt:

-   Bestimmte handle-Typen werden so definiert, dass Sie sich gegenseitig ausschließen. Beispielsweise können Sie kein **HWND** übergeben, in dem ein **hdc** -Typargument erforderlich ist. Ohne **strikte** werden alle Handles als **handle** definiert, sodass der Compiler nicht verhindert, dass Sie einen Typ von Handle verwenden, wenn ein anderer Typ erwartet wird.
-   Alle Rückruf Funktionstypen (z. b. Dialog Prozeduren, Fenster Prozeduren und Hook-Prozeduren) werden mit vollständigen Prototypen definiert. Dadurch wird verhindert, dass Rückruf Funktionen mit falschen Parameterlisten deklariert werden.
-   Parameter-und Rückgabe Werttypen, die einen generischen Zeiger verwenden sollten, werden als **LPVOID** anstelle von **LPSTR** oder einem anderen Zeigertyp deklariert.
-   Die [**comstat**](/windows/desktop/api/winbase/ns-winbase-comstat) -Struktur wird gemäß dem ANSI-Standard deklariert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Deaktivieren von Strict](disabling-strict.md)
</dt> <dt>

[Strikte Konformität](strict-compliance.md)
</dt> </dl>

 

 
