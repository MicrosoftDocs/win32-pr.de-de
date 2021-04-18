---
title: RAS-AutoDial
description: Eine Funktion mit dem Namen \ 0034; Standardverbindung \ 0034; wurde dem System in Windows XP hinzugefügt.
ms.assetid: 8ef832ed-97e4-4941-adb2-b35ce3a75fd1
keywords:
- AutoDial, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc2da449b91dd34165038b8d9f07b73926a943a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340859"
---
# <a name="ras-autodial"></a>RAS-AutoDial

Dem System in Windows XP wurde eine Funktion mit dem Namen "Standardverbindung" hinzugefügt. Wenn ein Verbindungsversuch fehlschlägt, prüft das System, ob eine explizite Entsprechung vorliegt (für den Winsock-Namen oder Freigabe Namen), wenn dies nicht der Fall ist, die Standardverbindung, sofern vorhanden.

**Windows 2000:** Wenn der Versuch, eine Verbindung mit einer Netzwerkadresse herzustellen, fehlschlägt, weil der Host nicht erreicht werden kann, kann das AutoDial-Feature automatisch einen DFÜ-Verbindungsvorgang starten. Zu diesem Zweck durchsucht AutoDial seine Datenbank von Netzwerkadressen, um einen Telefonbucheintrag zu finden, der zum Herstellen der Verbindung verwendet werden kann.

**Windows NT 4,0:  ** RAS speichert eine Datenbank mit den Winsock-Namen und/oder Freigabe Namen, die Sie erfolgreich erreicht haben, während eine RAS/VPN-Verbindung aktiv war. Wenn bei einem Winsock-oder Freigabe Verbindungsversuch zu einem späteren Zeitpunkt ein Fehler auftritt, prüft das System diese Datenbank und bietet die Möglichkeit, die gespeicherte Verbindung für Sie zu wählen.

 

 




