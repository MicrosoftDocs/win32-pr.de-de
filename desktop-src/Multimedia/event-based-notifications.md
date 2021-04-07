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
# <a name="event-based-notifications"></a>Event-Based Benachrichtigungen

Sie können das System auffordern, Joystick Meldungen an eine Anwendung zu senden, wenn sich die Position einer Joystick Achse um einen Wert ändert, der größer ist als der *Bewegungs Schwellen* Wert des Geräts. Der Verschiebungs Schwellenwert ist die Entfernung, auf die der Joystick verschoben werden muss, bevor eine Änderungs Meldung zum Ändern der Position an ein Fenster gesendet wird, das das Gerät erfasst hat. Weitere Informationen finden Sie unter [**mm \_ JOY1MOVE**](mm-joy1move.md), [**mm \_ JOY1ZMOVE**](mm-joy1zmove.md), [**mm \_ JOY2MOVE**](mm-joy2move.md)oder [**mm \_ JOY2ZMOVE**](mm-joy2zmove.md).

Der Schwellenwert ist anfänglich NULL. Sie können den Bewegungs Schwellenwert mithilfe der Funktion " [**joysetthreshold**](/windows/win32/api/joystickapi/nf-joystickapi-joysetthreshold) " festlegen. Sie können die minimale Abruf Häufigkeit des Joysticks mithilfe der [**joygetdevcaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) -Funktion abrufen.

 

 