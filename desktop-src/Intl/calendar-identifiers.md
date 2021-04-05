---
description: In diesem Thema werden die Kalender Bezeichner (Datentyp-Calid) definiert, die zur Angabe unterschiedlicher Kalender verwendet werden.
ms.assetid: ba2e841e-e24e-476a-851e-a29b3af4f04d
title: Kalender Bezeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab9b931aea4a186af0849dfe8f6642c53744d364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751153"
---
# <a name="calendar-identifiers"></a>Kalender Bezeichner

In diesem Thema werden die Kalender Bezeichner (Datentyp-Calid) definiert, die zur Angabe unterschiedlicher Kalender verwendet werden. Ihre Anwendungen können diese Bezeichner verwenden, wenn Sie die folgenden nls-Funktionen und-Rückruf Funktionen verwenden, die über Parameter verfügen, die den Datentyp "Calid" akzeptieren:

-   [**Convertsystemtimeumcaldatetime**](convertsystemtimetocaldatetime.md)
-   [**Enumcalendarinfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa)
-   [**Enumcalendarinfoex**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa)
-   [**Enumcalendarinfoexex**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex)
-   [**Enumcalendarinfoprocex**](/previous-versions/windows/desktop/legacy/dd317807(v=vs.85))
-   [**Enumdateformatsprocex**](/previous-versions/windows/desktop/legacy/dd317814(v=vs.85))
-   [**Getcalendarinfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)
-   [**Getcalendarinfoex**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex)
-   [**Getcalendarsupporteddaterange**](getcalendarsupporteddaterange.md)
-   [**Iscalendarleapyear**](iscalendarleapyear.md)
-   [**Setcalendarinfo**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa)

Die folgenden Werte sind definiert. Alle anderen Werte sind reserviert. Diese Werte können nicht miteinander kombiniert werden.



Kalender-ID

Bedeutung

1

Cal \_ Gregorianisch

Gregorianisch (lokalisiert)

2

Cal- \_ Gregorianisch \_

Gregorianisch (englische Zeichen folgen immer)

3

Cal \_ Japan

Japanischer Kaiser ERA

4

Cal- \_ Taiwan

Taiwan-Kalender

5

Cal \_ Korea

Koreanischer Tangun-Zeitraum

6

Cal- \_ Hijri

Hijri (Arabisch, Mond)

7

Cal- \_ Thai

Thailändisch

8

Cal- \_ Hebräisch

Hebräisch (Mond)

9

Cal \_ Gregorianisch ( \_ \_ Französisch)

Gregorian Middle East French

10

Cal \_ Gregorianisch, \_ Arabisch

Gregorian Arabic

11

Cal \_ Gregorianisch (in \_ \_ englischer Sprache)

Gregorianisch, transliterierte Englisch

12

Cal \_ Gregorianischen \_ xlit \_ Französisch

Gregorianisches transliterierte Französisch

23

Cal-über- \_ Qura

**Windows Vista und höher:** Um Al Qura-Kalender (Arabisch Mond)



 

> [!Note]  
> Die Lücke bei der Nummerierung zwischen den Bezeichner Cal \_ Gregorianisch \_ xlit \_ Französisch und Cal-über- \_ Qura ist beabsichtigt. Der Kenn Zeichner für Cal--über- \_ Qura ist 23, nicht 13.

 

Außerdem erlauben [**enumcalendarinfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa) und [**enumcalendarinfoex**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) die Verwendung des Werts \_ \_ Enumeration all Kalenders, um eine Enumeration aller anwendbaren Kalender anzufordern.

Wert

Bedeutung

0xFFFFFFFF

\_alle Kalender aufzählen \_

Alle anwendbaren Kalender für das angegebene Gebiets Schema



 

 

 
