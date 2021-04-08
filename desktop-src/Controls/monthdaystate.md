---
title: MONTHDAYSTATE
description: Der MONTHDAYSTATE-Datentyp ist ein Bitfeld, das den Status der einzelnen Tage eines Monats enthält.
ms.assetid: eb3dd6cb-738e-424b-945b-1485798a444c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2286482460ec87982c46a564e8441edd9bf7bb43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855499"
---
# <a name="monthdaystate"></a>MONTHDAYSTATE

Der MONTHDAYSTATE-Datentyp ist ein Bitfeld, das den Status der einzelnen Tage eines Monats enthält. Der-Datentyp wird in "kommctrl. h" wie folgt definiert:


```
typedef DWORD MONTHDAYSTATE, *LPMONTHDAYSTATE;
```



Jedes Bit (0 bis 30) stellt den Status eines Tags in einem Monat dar. Wenn ein Bit ist, wird der entsprechende Tag fett angezeigt. Andernfalls wird Sie ohne Betonung angezeigt.

Dieser Datentyp wird mit der [**MCM \_ SetDayState**](mcm-setdaystate.md) -Nachricht und dem entsprechenden Makro, [**monthcal \_ SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate), verwendet. Wenn die Werte von "MONTHDAYSTATE" in Bezug auf Monate verwendet werden, die kürzer als 31 Tage sind, wird nur auf die benötigten Bits zugegriffen.

Dieser Datentyp wurde zuerst in [Version 4,70](common-control-versions.md) von Comctl32.dll definiert.

 

 




