---
title: RAS-Konfiguration und Verbindungsinformationen
description: Anwendungen, die unter Windows NT 4.0 und höher und Windows 95 ausgeführt werden, können die RasEnumConnections-Funktion verwenden, um Informationen zu den vorhandenen Verbindungen auf dem lokalen Computer zu erhalten.
ms.assetid: b738ed87-1ff5-4366-9e83-08ac08ec261c
keywords:
- Konfiguration und Verbindung, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af528af93318247b7f88a50dc1db240670d17bcc48e11a7d683bfccd9054d671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673430"
---
# <a name="ras-configuration-and-connection-information"></a>RAS-Konfiguration und Verbindungsinformationen

Anwendungen, die unter Windows NT 4.0 und höher und Windows 95 ausgeführt werden, können die [**RasEnumConnections-Funktion**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) verwenden, um Informationen zu den vorhandenen Verbindungen auf dem lokalen Computer zu erhalten. Die Informationen für jede Verbindung enthalten ein Verbindungshand handle und den Namen des Telefonbucheintrags, der zum Herstellen der Verbindung verwendet wird. Sie können das Verbindungshandl in einem Aufruf der [**RasGetConnectStatus-Funktion**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) verwenden, um den aktuellen Status der Verbindung zu erhalten.

Windows NT Server 4.0 und höher stellen zwei neue Funktionen zum Abrufen von RAS-Informationen zur Verfügung. Windows 95does unterstützen diese Funktionen nicht.

Die [**RasEnumDevices-Funktion**](/windows/desktop/api/Ras/nf-ras-rasenumdevicesa) gibt den Namen und Typ der RAS-fähigen Geräte zurück, die auf dem lokalen Computer konfiguriert sind.

Die [**RasConnectionNotification-Funktion**](/windows/desktop/api/Ras/nf-ras-rasconnectionnotificationa) gibt ein Ereignisobjekt an, das vom System signalisiert wird, wenn eine RAS-Verbindung erstellt oder beendet wird.

 

 




