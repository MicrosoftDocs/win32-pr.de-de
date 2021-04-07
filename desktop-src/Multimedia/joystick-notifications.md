---
title: Joystick Benachrichtigungen
description: Joystick Benachrichtigungen
ms.assetid: 523dfae3-bbd5-4955-96f3-1710e29d003f
keywords:
- Joysticks, Benachrichtigungen
- Joysticks, Meldungen
- erfasste Joystick
- entkoppelt-Joystick
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2791f8da14107d50afe90d8efbdbfe79acba3093
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038950"
---
# <a name="joystick-notifications"></a>Joystick Benachrichtigungen

Mithilfe der [**joysetcapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) -Funktion können Sie direkte Joystick Nachrichten erfassen, die an eine Funktion gesendet werden sollen. Nur eine Anwendung kann Nachrichten von einem Joystick erfassen, aber Sie können den Joystick mithilfe der [**joygetpos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) -Funktion oder der [**joygetposex**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) -Funktion von einer anderen Anwendung Abfragen.

> [!Note]  
> Eine Joystick Nachricht kann die Anwendung, die den Joystick aufgezeichnet hat, nicht erreichen, wenn eine zweite Anwendung **joygetpos** oder **joygetposex** verwendet, um den Joystick ungefähr zur gleichen Zeit abzufragen, in der die Nachricht gesendet wird. In diesem Fall könnte die zweite Anwendung die Nachricht abfangen.

 

Wenn Sie Nachrichten von zwei an das System angefügten Joystick erfassen möchten, verwenden Sie für jeden Joystick zweimal [**joysetcapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) . Ihr Fenster empfängt separate und unterschiedliche Meldungen für jedes Gerät.

Sie können einen aufgezeichneten Joystick mithilfe der [**joyreleasecapture**](/windows/win32/api/joystickapi/nf-joystickapi-joyreleasecapture) -Funktion freigeben. Wenn eine Anwendung den Joystick vor dem Beenden nicht freigibt, wird der Joystick automatisch kurz nach dem Zerstören des Erfassungs Fensters freigegeben.

Ein nicht ausgezeichteter Joystick kann nicht erfasst werden. Die Funktion " **joysetcapture** " gibt "joyerr" zurück, \_ Wenn das angegebene Gerät nicht getrennt ist.

 

 