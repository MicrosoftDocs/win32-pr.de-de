---
title: Event-Based Benachrichtigungen
description: Event-Based Benachrichtigungen
ms.assetid: bd483865-f983-416a-9b72-475fe9679cd1
keywords:
- Joysticks, Benachrichtigungen
- Joysticks, Meldungen
- Joysticks, ereignisbasierte Benachrichtigungen
- Joysticks, Bewegungs Schwellenwert
- ereignisbasierte Joystick Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1aa36809942593cdbe21b61af0d4f07f02b186a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725129"
---
# <a name="event-based-notifications"></a><span data-ttu-id="ce475-108">Event-Based Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="ce475-108">Event-Based Notifications</span></span>

<span data-ttu-id="ce475-109">Sie können das System auffordern, Joystick Meldungen an eine Anwendung zu senden, wenn sich die Position einer Joystick Achse um einen Wert ändert, der größer ist als der *Bewegungs Schwellen* Wert des Geräts.</span><span class="sxs-lookup"><span data-stu-id="ce475-109">You can ask the system to send joystick messages to an application whenever the position of a joystick axis changes by a value greater than the *movement threshold* of the device.</span></span> <span data-ttu-id="ce475-110">Der Verschiebungs Schwellenwert ist die Entfernung, auf die der Joystick verschoben werden muss, bevor eine Änderungs Meldung zum Ändern der Position an ein Fenster gesendet wird, das das Gerät erfasst hat.</span><span class="sxs-lookup"><span data-stu-id="ce475-110">The movement threshold is the distance the joystick must be moved before a joystick position change message is sent to a window that has captured the device.</span></span> <span data-ttu-id="ce475-111">Weitere Informationen finden Sie unter [**mm \_ JOY1MOVE**](mm-joy1move.md), [**mm \_ JOY1ZMOVE**](mm-joy1zmove.md), [**mm \_ JOY2MOVE**](mm-joy2move.md)oder [**mm \_ JOY2ZMOVE**](mm-joy2zmove.md).</span><span class="sxs-lookup"><span data-stu-id="ce475-111">For more information, see [**MM\_JOY1MOVE**](mm-joy1move.md), [**MM\_JOY1ZMOVE**](mm-joy1zmove.md), [**MM\_JOY2MOVE**](mm-joy2move.md), or [**MM\_JOY2ZMOVE**](mm-joy2zmove.md).</span></span>

<span data-ttu-id="ce475-112">Der Schwellenwert ist anfänglich NULL.</span><span class="sxs-lookup"><span data-stu-id="ce475-112">The threshold is initially zero.</span></span> <span data-ttu-id="ce475-113">Sie können den Bewegungs Schwellenwert mithilfe der Funktion " [**joysetthreshold**](/windows/win32/api/joystickapi/nf-joystickapi-joysetthreshold) " festlegen.</span><span class="sxs-lookup"><span data-stu-id="ce475-113">You can set the movement threshold by using the [**joySetThreshold**](/windows/win32/api/joystickapi/nf-joystickapi-joysetthreshold) function.</span></span> <span data-ttu-id="ce475-114">Sie können die minimale Abruf Häufigkeit des Joysticks mithilfe der [**joygetdevcaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) -Funktion abrufen.</span><span class="sxs-lookup"><span data-stu-id="ce475-114">You can retrieve the minimum polling frequency of the joystick by using the [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) function.</span></span>

 

 