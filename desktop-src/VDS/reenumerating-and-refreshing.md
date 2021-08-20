---
description: Aufzählen und Aktualisieren
ms.assetid: 67d34946-47df-43e2-8ca7-628d0671b869
title: Aufzählen und Aktualisieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42f19d28d44234b773988f3038666212caf447fb45dee39435b0d99169f92212
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125920"
---
# <a name="reenumerating-and-refreshing"></a>Aufzählen und Aktualisieren

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die Windows Storage Verwaltungs-API. [](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Beim Reenumerationsvorgang werden neu verbundene und neu getrennte Geräte gefunden. Der Aktualisierungsvorgang aktualisiert die Konfigurationsinformationen vorhandener Geräte.

**So aufzählen Sie Softwareanbieterobjekte erneut**

-   Rufen Sie [**die IVdsService::Reenumerate-Methode**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) auf. Diese Methode entdeckt alle neu verbundenen und getrennten Datenträger und CD-ROM-Laufwerke und stellt sicher, dass alle Datenträger über den richtigen Besitzer verfügen. VDS besitzt Unformatiert-Datenträger oder Datenträger mit Fehlern. Der Basic-Anbieter besitzt Basisdatenträger. und der dynamische Anbieter besitzt dynamische Datenträger. Dieser Vorgang kann das Scannen interner Subsystem-Buslinien und das Warten auf Time outs umfassen.

**So aufzählen und aktualisieren Sie Softwareanbieterobjekte**

-   Rufen Sie [**die IVdsService::Reenumerate-Methode**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) auf, und rufen Sie dann die [**IVdsService::Refresh-Methode**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) auf. Zusätzlich zur Suche nach neu verbundenen und getrennten Datenträgern und CD-ROM-Laufwerken aktualisiert diese Kombination von Methoden alle Datenträger-, Volume- und Plexinformationen im VDS-Cache für Datenträger, die nicht kürzlich verbunden oder getrennt wurden. Rufen **Sie Refresh** allein auf, um die Eigenschafteninformationen vorhandener Objekte im Cache zu aktualisieren. Dieser Vorgang kann das Scannen interner Subsystem-Buslinien und das Warten auf Time outs umfassen. Beachten Sie, dass VDS den Cache automatisch aktualisiert, wenn eine Änderung auftritt, die eine Benachrichtigung auslöst. Außerdem kann das Aufrufen **von Refresh** als Reaktion auf eine VDS-Benachrichtigung dazu führen, dass eine Endlosschleife von Benachrichtigungen gesendet wird. Aus diesen Gründen **sollte Die Aktualisierung** nur aufgerufen werden, wenn der Cache anscheinend nicht ordnungsgemäß aktualisiert wird.

**So aufzählen Sie Hardwaresubsysteme erneut**

-   Rufen Sie [**die IVdsHwProvider::Reenumerate-Methode**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate) auf. Je nach Anbieter kann dieser Vorgang das Senden von Netzwerkpaketen und das Warten auf Time outs, das erneute Einscannen von SCSI-Bus und das Warten auf Time outs und so weiter umfassen.

**So aufzählen Sie Hardwaresubsystemobjekte erneut**

-   Rufen Sie [**die IVdsSubSystem::Reenumerate-Methode**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate) auf, um die Objekte (in der Regel Laufwerke) im Subsystem zu inventarieren. Je nach Subsystem kann dieser Vorgang das Scannen interner Subsystem-Buslinien und das Warten auf Time outs umfassen.

**So aktualisieren Sie Hardwaresubsysteme und Subsystemobjekte**

-   Rufen Sie [**die IVdsHwProvider::Refresh-Methode**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh) auf, um den VDS-Cache mit Informationen zu vorhandenen Subsystemen zu aktualisieren, die von VDS-Hardwareanbietern verwaltet werden. Beachten Sie, dass VDS den Cache automatisch aktualisiert, wenn eine Änderung auftritt, die eine Benachrichtigung auslöst. Außerdem kann das Aufrufen [**von Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) als Reaktion auf eine VDS-Benachrichtigung dazu führen, dass eine Endlosschleife von Benachrichtigungen gesendet wird. Aus diesen Gründen **sollte Die Aktualisierung** nur aufgerufen werden, wenn der Cache anscheinend nicht ordnungsgemäß aktualisiert wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von VDS](using-vds.md)
</dt> <dt>

[**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[**IVdsService::Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh)
</dt> <dt>

[**IVdsHwProvider::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate)
</dt> <dt>

[**IVdsSubSystem::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate)
</dt> <dt>

[**IVdsHwProvider::Refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh)
</dt> </dl>

 

 
