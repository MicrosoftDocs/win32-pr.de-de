---
title: RAS-Konfiguration und Verbindungsinformationen
description: Anwendungen, die unter Windows NT 4,0 und höheren Versionen und Windows 95 ausgeführt werden, können die Funktion "rasenumschlag" verwenden, um Informationen über die vorhandenen Verbindungen auf dem lokalen Computer zu erhalten.
ms.assetid: b738ed87-1ff5-4366-9e83-08ac08ec261c
keywords:
- Konfiguration und Verbindung, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44c4e768f4686a24857a75212e40f2e64bc91109
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337984"
---
# <a name="ras-configuration-and-connection-information"></a><span data-ttu-id="7b6b2-104">RAS-Konfiguration und Verbindungsinformationen</span><span class="sxs-lookup"><span data-stu-id="7b6b2-104">RAS Configuration and Connection Information</span></span>

<span data-ttu-id="7b6b2-105">Anwendungen, die unter Windows NT 4,0 und höheren Versionen und Windows 95 ausgeführt werden, können die Funktion " [**rasenumschlag**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) " verwenden, um Informationen über die vorhandenen Verbindungen auf dem lokalen Computer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-105">Applications running on Windows NT 4.0 and later versions, and Windows 95, can use the [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) function to get information about the existing connections on the local computer.</span></span> <span data-ttu-id="7b6b2-106">Die Informationen für jede Verbindung enthalten ein Verbindungs Handle und den Namen des Telefonbucheintrags, der zum Herstellen der Verbindung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-106">The information for each connection includes a connection handle and the name of the phone-book entry used to establish the connection.</span></span> <span data-ttu-id="7b6b2-107">Sie können das Verbindungs Handle in einem Aufrufen der Funktion " [**rasgetconnectstatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) " verwenden, um den aktuellen Status der Verbindung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-107">You can use the connection handle in a call to the [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) function get the current status of the connection.</span></span>

<span data-ttu-id="7b6b2-108">Windows NT Server 4,0 und höhere Versionen bieten zwei neue Funktionen zum Abrufen von RAS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-108">Windows NT Server 4.0 and later versions provide two new functions for retrieving RAS information.</span></span> <span data-ttu-id="7b6b2-109">Diese Funktionen werden von Windows 95 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-109">Windows 95does not support these functions.</span></span>

<span data-ttu-id="7b6b2-110">Die Funktion " [**rasenredevices**](/windows/desktop/api/Ras/nf-ras-rasenumdevicesa) " gibt den Namen und den Typ der RAS-fähigen Geräte zurück, die auf dem lokalen Computer konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-110">The [**RasEnumDevices**](/windows/desktop/api/Ras/nf-ras-rasenumdevicesa) function returns the name and type of the RAS-capable devices that are configured on the local computer.</span></span>

<span data-ttu-id="7b6b2-111">Die Funktion " [**rasconnectionnotification**](/windows/desktop/api/Ras/nf-ras-rasconnectionnotificationa) " gibt ein Ereignis Objekt an, das vom System signalisiert wird, wenn eine RAS-Verbindung erstellt oder beendet wird.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-111">The [**RasConnectionNotification**](/windows/desktop/api/Ras/nf-ras-rasconnectionnotificationa) function specifies an event object that the system signals when a RAS connection is created or terminated.</span></span>

 

 




