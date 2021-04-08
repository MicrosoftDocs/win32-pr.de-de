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
# <a name="monthdaystate"></a><span data-ttu-id="c1ac0-103">MONTHDAYSTATE</span><span class="sxs-lookup"><span data-stu-id="c1ac0-103">MONTHDAYSTATE</span></span>

<span data-ttu-id="c1ac0-104">Der MONTHDAYSTATE-Datentyp ist ein Bitfeld, das den Status der einzelnen Tage eines Monats enthält.</span><span class="sxs-lookup"><span data-stu-id="c1ac0-104">The MONTHDAYSTATE data type is a bitfield that holds the state of each day in a month.</span></span> <span data-ttu-id="c1ac0-105">Der-Datentyp wird in "kommctrl. h" wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="c1ac0-105">The data type is defined in Commctrl.h as follows:</span></span>


```
typedef DWORD MONTHDAYSTATE, *LPMONTHDAYSTATE;
```



<span data-ttu-id="c1ac0-106">Jedes Bit (0 bis 30) stellt den Status eines Tags in einem Monat dar.</span><span class="sxs-lookup"><span data-stu-id="c1ac0-106">Each bit (0 through 30) represents the state of a day in a month.</span></span> <span data-ttu-id="c1ac0-107">Wenn ein Bit ist, wird der entsprechende Tag fett angezeigt. Andernfalls wird Sie ohne Betonung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c1ac0-107">If a bit is on, the corresponding day will be displayed in bold; otherwise it will be displayed with no emphasis.</span></span>

<span data-ttu-id="c1ac0-108">Dieser Datentyp wird mit der [**MCM \_ SetDayState**](mcm-setdaystate.md) -Nachricht und dem entsprechenden Makro, [**monthcal \_ SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate), verwendet.</span><span class="sxs-lookup"><span data-stu-id="c1ac0-108">This data type is used with the [**MCM\_SETDAYSTATE**](mcm-setdaystate.md) message and the corresponding macro, [**MonthCal\_SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate).</span></span> <span data-ttu-id="c1ac0-109">Wenn die Werte von "MONTHDAYSTATE" in Bezug auf Monate verwendet werden, die kürzer als 31 Tage sind, wird nur auf die benötigten Bits zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="c1ac0-109">When MONTHDAYSTATE values are used in reference to months shorter than 31 days, only the needed bits will be accessed.</span></span>

<span data-ttu-id="c1ac0-110">Dieser Datentyp wurde zuerst in [Version 4,70](common-control-versions.md) von Comctl32.dll definiert.</span><span class="sxs-lookup"><span data-stu-id="c1ac0-110">This data type was first defined in [Version 4.70](common-control-versions.md) of Comctl32.dll.</span></span>

 

 




