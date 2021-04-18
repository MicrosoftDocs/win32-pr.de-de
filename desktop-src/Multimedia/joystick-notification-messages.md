---
title: Joystick Benachrichtigungs Meldungen
description: Joystick Benachrichtigungs Meldungen
ms.assetid: 9e8ccc1b-85a9-44bf-b561-6ad4c10cddd1
keywords:
- Joysticks, Benachrichtigungen
- Joysticks, Meldungen
- Joysticks, Position
- Joysticks, Schaltflächen
- MM_JOY1 Meldungen
- MM_JOY2 Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 698f999dab49ea6684e9184f6ed5c46286518b97
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338173"
---
# <a name="joystick-notification-messages"></a>Joystick Benachrichtigungs Meldungen

Joystick Nachrichten benachrichtigen Ihre Anwendung, dass sich die Position eines Joysticks geändert hat oder eine der Schaltflächen den Status geändert hat. Nachrichten, die mit mm \_ JOY1 beginnen, werden an die Funktion gesendet, wenn Ihre Anwendung mithilfe des Bezeichners JOYSTICKID1 Eingaben aus dem Joystick anfordert, und mm \_ JOY2-Nachrichten werden gesendet, wenn Ihre Anwendung Eingaben vom Joystick mithilfe des Bezeichners JOYSTICKID2 anfordert.

In den Nachrichten in der folgenden Tabelle wird der Status der Joystick Schaltflächen identifiziert:



| `Message`                                         | BESCHREIBUNG                                                     |
|-------------------------------------------------|-----------------------------------------------------------------|
| [**MM \_ JOY1BUTTONDOWN**](mm-joy1buttondown.md) | Eine Schaltfläche auf dem Joystick JOYSTICKID1 wurde gedrückt.              |
| [**MM \_ JOY1BUTTONUP**](mm-joy1buttonup.md)     | Eine Schaltfläche auf dem Joystick JOYSTICKID1 wurde freigegeben.             |
| [**MM \_ JOY1MOVE**](mm-joy1move.md)             | Joystick JOYSTICKID1 geänderte Position in der x-oder y-Richtung. |
| [**MM \_ JOY1ZMOVE**](mm-joy1zmove.md)           | Joystick JOYSTICKID1 geänderte Position in z-Richtung.       |
| [**MM \_ JOY2BUTTONDOWN**](mm-joy2buttondown.md) | Eine Schaltfläche auf dem Joystick JOYSTICKID2 wurde gedrückt.              |
| [**MM \_ JOY2BUTTONUP**](mm-joy2buttonup.md)     | Eine Schaltfläche auf dem Joystick JOYSTICKID2 wurde freigegeben.             |
| [**MM \_ JOY2MOVE**](mm-joy2move.md)             | Joystick JOYSTICKID2 geänderte Position in der x-oder y-Richtung  |
| [**MM \_ JOY2ZMOVE**](mm-joy2zmove.md)           | Joystick JOYSTICKID2 geänderte Position in z-Richtung.       |



 

Alle Nachrichten melden nicht vorhandene Schaltflächen als freigegeben.

 

 




