---
title: Benachrichtigungsmeldungen
description: Benachrichtigungsmeldungen
ms.assetid: 9e8ccc1b-85a9-44bf-b561-6ad4c10cddd1
keywords:
- -Benachrichtigungen
- -Nachrichten
- -, Position
- -Schaltflächen
- MM_JOY1 Nachrichten
- MM_JOY2 Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27113adeb6f9fd4444f8fc30431df0eab686db667fa2674e81d7f5d4e568be64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140340"
---
# <a name="joystick-notification-messages"></a>Benachrichtigungsmeldungen

Mit Benachrichtigungen wird Ihre Anwendung darüber informiert, dass sich die Position eines Bzw. einer seiner Schaltflächen geändert hat. Nachrichten, die mit MM MM MM1 beginnen, werden an die Funktion gesendet, wenn Ihre Anwendung Eingaben vom Zierer unter Verwendung des BezeichnersIDENTID1 anfing, und MM-NACHRICHTEN VOM2-Nachrichten werden gesendet, wenn Ihre Anwendung eingaben von der -Kennung mithilfe des \_ Bezeichners \_ 2 anfing.

Die Meldungen in der folgenden Tabelle geben den Status der Schaltflächen an:



| `Message`                                         | BESCHREIBUNG                                                     |
|-------------------------------------------------|-----------------------------------------------------------------|
| [**MM \_ MM MM1BUTTONDOWN**](mm-joy1buttondown.md) | Es wurde eine Schaltfläche auf dem Computer MITID1 gedrückt.              |
| [**MM \_ MM MM1BUTTONUP**](mm-joy1buttonup.md)     | Eine Schaltfläche auf dem Computer "besendid1" wurde veröffentlicht.             |
| [**MM \_ MM MM1MOVE**](mm-joy1move.md)             | Die Position von "Positionsänderung" in x- oder y-Richtung wurde geändert. |
| [**MM \_ MM MM1ZMOVE**](mm-joy1zmove.md)           | Die Position von "Positionsänderung" in der Z-Richtung wurde geändert.       |
| [**MM \_ MM MM2BUTTONDOWN**](mm-joy2buttondown.md) | Es wurde eine Schaltfläche auf dem Computer MITID2 gedrückt.              |
| [**MM \_ MM MM2BUTTONUP**](mm-joy2buttonup.md)     | Es wurde eine Schaltfläche auf der NSDID2 veröffentlicht.             |
| [**MM \_ MM MM2MOVE**](mm-joy2move.md)             | Die Position von " x" oder "y" wurde geändert.  |
| [**MM \_ MM MM2ZMOVE**](mm-joy2zmove.md)           | Die Position von Positionswechseln in Z-Richtung wurde durch Denkrichtung des 50-0-00-00-16-00       |



 

Alle Meldungen melden nicht vorhandene Schaltflächen als freigegeben.

 

 




