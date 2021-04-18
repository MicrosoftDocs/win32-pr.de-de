---
title: Benachrichtigungshub ändern
description: Benachrichtigungshub ändern
ms.assetid: 1f1aef71-a2b7-49ad-a0bc-f61f10b701c9
keywords:
- Änderung
- Benachrichtigungshub ändern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e6d3015be29c84b6b93b47b373d05f96f4388b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310187"
---
# <a name="change-notification-flags"></a>Benachrichtigungshub ändern



| Konstante                         | Wert      | BESCHREIBUNG                                                                                                                                                           |
|----------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RTM \_ NUM- \_ Änderungs \_ Typen          | 3          | Gibt die Anzahl der Änderungs Typen an, die zurzeit vom Routing Tabellen-Manager verwendet werden.                                                                            |
| RTM \_ - \_ Änderungstyp \_ alle           | 0x0001     | Benachrichtigt den Client über alle Änderungen an einem Ziel.                                                                                                                   |
| RTM \_ - \_ Änderungstyp \_ am besten          | 0x0002     | Benachrichtigt den Client über Änderungen an der besten Route oder wenn die beste Route geändert wird.                                                                                     |
| RTM \_ - \_ Änderungstyp \_ Weiterleitung    | 0x0004     | Benachrichtigt den Client über alle optimalen Weiterleitungs Änderungen, die sich auf die Weiterleitung auswirken (z. b. Änderungen am nächsten Hop).                                                                      |
| RTM \_ benachrichtigt \_ nur \_ markierte \_ Geräte-Geräte | 0x00010000 | Benachrichtigt den Client über Änderungen an Zielen, die der Client markiert hat. Wenn dieses Flag nicht angegeben wird, werden Änderungs Benachrichtigungs Meldungen für alle Ziele gesendet. |



 

 

 




