---
title: Ändern von Benachrichtigungsflags
description: Ändern von Benachrichtigungsflags
ms.assetid: 1f1aef71-a2b7-49ad-a0bc-f61f10b701c9
keywords:
- Change
- Ändern von Benachrichtigungsflags
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f5311e3313bf23c92972395143d288483181e7a69212115082a2f150d7d1bb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791834"
---
# <a name="change-notification-flags"></a>Ändern von Benachrichtigungsflags



| Konstante                         | Wert      | Beschreibung                                                                                                                                                           |
|----------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ RTM-NUM-ÄNDERUNGSTYPEN \_          | 3          | Gibt die Anzahl der Änderungstypen an, die derzeit vom Routingtabellen-Manager verwendet werden.                                                                            |
| RTM \_ CHANGE \_ TYPE \_ ALL           | 0x0001     | Benachrichtigt den Client über jede Änderung an einem Ziel.                                                                                                                   |
| \_RTM-ÄNDERUNGSTYP \_ \_ AM BESTEN          | 0x0002     | Benachrichtigt den Client über Änderungen an der besten Route oder über Änderungen an der besten Route.                                                                                     |
| \_ \_ RTM-ÄNDERUNGSTYPWEITERLEITUNG \_    | 0x0004     | Benachrichtigt den Client über alle am besten geeigneten Routenänderungen, die sich auf die Weiterleitung auswirken (z. B. Änderungen am nächsten Hop).                                                                      |
| RTM \_ NOTIFY \_ ONLY \_ MARKED \_ DESTS | 0x00010000 | Benachrichtigt den Client über Änderungen an Zielen, die der Client markiert hat. Wenn dieses Flag nicht angegeben ist, werden Änderungsbenachrichtigungsmeldungen für alle Ziele gesendet. |



 

 

 




