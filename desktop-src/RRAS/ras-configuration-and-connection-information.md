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
# <a name="ras-configuration-and-connection-information"></a>RAS-Konfiguration und Verbindungsinformationen

Anwendungen, die unter Windows NT 4,0 und höheren Versionen und Windows 95 ausgeführt werden, können die Funktion " [**rasenumschlag**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) " verwenden, um Informationen über die vorhandenen Verbindungen auf dem lokalen Computer zu erhalten. Die Informationen für jede Verbindung enthalten ein Verbindungs Handle und den Namen des Telefonbucheintrags, der zum Herstellen der Verbindung verwendet wird. Sie können das Verbindungs Handle in einem Aufrufen der Funktion " [**rasgetconnectstatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) " verwenden, um den aktuellen Status der Verbindung abzurufen.

Windows NT Server 4,0 und höhere Versionen bieten zwei neue Funktionen zum Abrufen von RAS-Informationen. Diese Funktionen werden von Windows 95 nicht unterstützt.

Die Funktion " [**rasenredevices**](/windows/desktop/api/Ras/nf-ras-rasenumdevicesa) " gibt den Namen und den Typ der RAS-fähigen Geräte zurück, die auf dem lokalen Computer konfiguriert sind.

Die Funktion " [**rasconnectionnotification**](/windows/desktop/api/Ras/nf-ras-rasconnectionnotificationa) " gibt ein Ereignis Objekt an, das vom System signalisiert wird, wenn eine RAS-Verbindung erstellt oder beendet wird.

 

 




