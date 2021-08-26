---
title: MONTHDAYSTATE
description: Der MONTHDAYSTATE-Datentyp ist ein Bitfeld, das den Zustand jedes Tages in einem Monat enthält.
ms.assetid: eb3dd6cb-738e-424b-945b-1485798a444c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4e21eed1293a53bce8f38f5bd4db09b8cbe3fbf649fb07348a5dca65e908727
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079860"
---
# <a name="monthdaystate"></a>MONTHDAYSTATE

Der MONTHDAYSTATE-Datentyp ist ein Bitfeld, das den Zustand jedes Tages in einem Monat enthält. Der Datentyp wird in Commctrl.h wie folgt definiert:


```
typedef DWORD MONTHDAYSTATE, *LPMONTHDAYSTATE;
```



Jedes Bit (0 bis 30) stellt den Zustand eines Tages in einem Monat dar. Wenn ein Bit ein on ist, wird der entsprechende Tag fett angezeigt. Andernfalls wird sie ohne Hervorhebung angezeigt.

Dieser Datentyp wird mit der [**MCM \_ SETDAYSTATE-Nachricht**](mcm-setdaystate.md) und dem entsprechenden Makro [**MonthCal \_ SetDayState verwendet.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate) Wenn MONTHDAYSTATE-Werte als Verweis auf Monate verwendet werden, die kürzer als 31 Tage sind, wird nur auf die erforderlichen Bits zugegriffen.

Dieser Datentyp wurde zuerst in [Version 4.70 des](common-control-versions.md) Comctl32.dll.

 

 




