---
title: Time-Based Benachrichtigungen
description: Time-Based Benachrichtigungen
ms.assetid: cf7bc0d4-f3bd-4416-b85f-0ff51a0efbbc
keywords:
- Joysticks, Benachrichtigungen
- Joysticks, Meldungen
- Joysticks, zeitbasierte Benachrichtigungen
- zeitbasierte Joystick Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15dff2a6140bd993157f20e92488afce1b646e20
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948598"
---
# <a name="time-based-notifications"></a><span data-ttu-id="a86a9-107">Time-Based Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="a86a9-107">Time-Based Notifications</span></span>

<span data-ttu-id="a86a9-108">Sie können das Betriebssystem Benachrichtigen, um in regelmäßigen Abständen Joystick-Nachrichten an eine Anwendung zu senden, indem Sie den *fchanged* -Parameter von [**joysetcapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) auf **false** festlegen und die Intervalllänge zwischen aufeinander folgenden Nachrichten angeben.</span><span class="sxs-lookup"><span data-stu-id="a86a9-108">You can notify the operating system to send joystick messages to an application at regular time intervals by setting the *fChanged* parameter of [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) to **FALSE** and by specifying the interval length between successive messages.</span></span> <span data-ttu-id="a86a9-109">Weisen Sie zu diesem Zweck dem *uperiod* -Parameter einen Wert zwischen den minimalen und maximalen Abruf Frequenzen für den Joystick zu.</span><span class="sxs-lookup"><span data-stu-id="a86a9-109">To do this, assign the *uPeriod* parameter a value between the minimum and maximum polling frequencies for the joystick.</span></span> <span data-ttu-id="a86a9-110">Sie können diesen Bereich mithilfe der [**joygetdevcaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) -Funktion ermitteln, die die **Member wperiodmin** und **wperiodmax** in der [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) -Struktur füllt.</span><span class="sxs-lookup"><span data-stu-id="a86a9-110">You can determine this range by using the [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) function, which fills the **wPeriodMin** and **wPeriodMax** members in the [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) structure.</span></span> <span data-ttu-id="a86a9-111">Wenn der *uperiod* -Wert außerhalb des gültigen Abruf Häufigkeits Bereichs für den Joystick liegt, verwendet der Joystick Treiber die minimale oder maximale Abruf Häufigkeit, je nachdem, welcher Wert dem *uperiod* -Wert näher liegt.</span><span class="sxs-lookup"><span data-stu-id="a86a9-111">If the *uPeriod* value is outside the range of valid polling frequencies for the joystick, the joystick driver uses the minimum or maximum polling frequency, whichever is closer to the *uPeriod* value.</span></span>

> [!Note]  
> <span data-ttu-id="a86a9-112">Windows richtet ein Timer-Ereignis mit jedem aufzurufenden Befehl von **joysetcapture** ein.</span><span class="sxs-lookup"><span data-stu-id="a86a9-112">Windows sets up a timer event with each call to **joySetCapture**.</span></span>

 

 

 