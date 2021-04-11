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
# <a name="time-based-notifications"></a>Time-Based Benachrichtigungen

Sie können das Betriebssystem Benachrichtigen, um in regelmäßigen Abständen Joystick-Nachrichten an eine Anwendung zu senden, indem Sie den *fchanged* -Parameter von [**joysetcapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) auf **false** festlegen und die Intervalllänge zwischen aufeinander folgenden Nachrichten angeben. Weisen Sie zu diesem Zweck dem *uperiod* -Parameter einen Wert zwischen den minimalen und maximalen Abruf Frequenzen für den Joystick zu. Sie können diesen Bereich mithilfe der [**joygetdevcaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) -Funktion ermitteln, die die **Member wperiodmin** und **wperiodmax** in der [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) -Struktur füllt. Wenn der *uperiod* -Wert außerhalb des gültigen Abruf Häufigkeits Bereichs für den Joystick liegt, verwendet der Joystick Treiber die minimale oder maximale Abruf Häufigkeit, je nachdem, welcher Wert dem *uperiod* -Wert näher liegt.

> [!Note]  
> Windows richtet ein Timer-Ereignis mit jedem aufzurufenden Befehl von **joysetcapture** ein.

 

 

 