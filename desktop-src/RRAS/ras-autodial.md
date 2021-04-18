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
# <a name="ras-autodial"></a><span data-ttu-id="2d988-104">RAS-AutoDial</span><span class="sxs-lookup"><span data-stu-id="2d988-104">RAS AutoDial</span></span>

<span data-ttu-id="2d988-105">Dem System in Windows XP wurde eine Funktion mit dem Namen "Standardverbindung" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2d988-105">A feature called "default connection" was added to the system in Windows XP.</span></span> <span data-ttu-id="2d988-106">Wenn ein Verbindungsversuch fehlschlägt, prüft das System, ob eine explizite Entsprechung vorliegt (für den Winsock-Namen oder Freigabe Namen), wenn dies nicht der Fall ist, die Standardverbindung, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2d988-106">If there is a failed connection attempt, the system checks for an explicit match (for Winsock name or share name) in the database if not, it dials the default connection if there is one.</span></span>

<span data-ttu-id="2d988-107">**Windows 2000:** Wenn der Versuch, eine Verbindung mit einer Netzwerkadresse herzustellen, fehlschlägt, weil der Host nicht erreicht werden kann, kann das AutoDial-Feature automatisch einen DFÜ-Verbindungsvorgang starten.</span><span class="sxs-lookup"><span data-stu-id="2d988-107">**Windows 2000:** When an attempt to connect to a network address fails because the host cannot be reached, the AutoDial feature can automatically start a dial-up connection operation.</span></span> <span data-ttu-id="2d988-108">Zu diesem Zweck durchsucht AutoDial seine Datenbank von Netzwerkadressen, um einen Telefonbucheintrag zu finden, der zum Herstellen der Verbindung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2d988-108">To do this, AutoDial searches its database of network addresses to find a phone-book entry that it can use to establish the connection.</span></span>

<span data-ttu-id="2d988-109">**Windows NT 4,0:  ** RAS speichert eine Datenbank mit den Winsock-Namen und/oder Freigabe Namen, die Sie erfolgreich erreicht haben, während eine RAS/VPN-Verbindung aktiv war.</span><span class="sxs-lookup"><span data-stu-id="2d988-109">**Windows NT 4.0:  ** RAS keeps a database of the Winsock names and/or share names that you have successfully reached while a RAS/VPN connection was active.</span></span> <span data-ttu-id="2d988-110">Wenn bei einem Winsock-oder Freigabe Verbindungsversuch zu einem späteren Zeitpunkt ein Fehler auftritt, prüft das System diese Datenbank und bietet die Möglichkeit, die gespeicherte Verbindung für Sie zu wählen.</span><span class="sxs-lookup"><span data-stu-id="2d988-110">Later, when a winsock or share connection attempt fails, the system checks this database and offers to dial the stored connection for you.</span></span>

 

 




