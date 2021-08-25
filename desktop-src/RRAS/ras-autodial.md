---
title: RAS AutoDial
description: Ein Feature namens \0034;Standardverbindung \ 0034; wurde dem System in Windows XP hinzugefügt.
ms.assetid: 8ef832ed-97e4-4941-adb2-b35ce3a75fd1
keywords:
- AutoDial, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7956148919505eb16d1fb2fe9bc045fa7ecbaa7e2959c430e15f8013ef372ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909870"
---
# <a name="ras-autodial"></a>RAS AutoDial

Eine Funktion namens "Standardverbindung" wurde dem System in Windows XP hinzugefügt. Bei einem fehlgeschlagenen Verbindungsversuch sucht das System nach einer expliziten Übereinstimmung (für Winsock-Name oder Freigabename) in der Datenbank, falls dies nicht der Fehler ist, wählt es die Standardverbindung aus, sofern vorhanden.

**Windows 2000:** Wenn beim Versuch, eine Verbindung mit einer Netzwerkadresse herzustellen, ein Fehler auftritt, weil der Host nicht erreicht werden kann, kann das Feature AutoDial automatisch einen DFÜ-Verbindungsvorgang starten. Hierzu durchsucht AutoDial seine Datenbank mit Netzwerkadressen, um einen Telefonbucheintrag zu finden, mit dem die Verbindung hergestellt werden kann.

**Windows NT 4.0: ** RAS behält eine Datenbank mit den Winsock-Namen und/oder Freigabenamen bei, die Sie erfolgreich erreicht haben, während eine RAS/VPN-Verbindung aktiv war. Wenn später ein Winsock- oder Freigabeverbindungsversuch fehlschlägt, überprüft das System diese Datenbank und bietet an, die gespeicherte Verbindung für Sie zu wählen.

 

 




