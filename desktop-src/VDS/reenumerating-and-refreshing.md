---
description: Erneute Aufzählung und Aktualisierung
ms.assetid: 67d34946-47df-43e2-8ca7-628d0671b869
title: Erneute Aufzählung und Aktualisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a6302c817390ea2eb6bda3d5da0302c4bfefbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358955"
---
# <a name="reenumerating-and-refreshing"></a>Erneute Aufzählung und Aktualisierung

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Der Vorgang reenumeration ermittelt neu verbundene und neu getrennte Geräte. Der Aktualisierungs Vorgang aktualisiert die Konfigurationsinformationen vorhandener Geräte.

**So können Sie Softwareanbieter Objekte erneut aufzählen**

-   Aufrufen der [**ivdsservice:: REENUMERATE**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) -Methode. Diese Methode ermittelt alle neu verbundenen und nicht verbundenen Datenträger und CD-ROM-Laufwerke und stellt sicher, dass alle Datenträger über den richtigen Besitzer verfügen. VDS besitzt unformatierte Datenträger oder Datenträger mit Fehlern. der Basic-Anbieter besitzt Basis Datenträger. und der dynamische Anbieter besitzt dynamische Datenträger. Dieser Vorgang kann das Scannen interner subsystembusse und das warten auf Timeouts einschließen.

**So können Sie Softwareanbieter Objekte erneut auflisten und aktualisieren**

-   Aufrufen der [**ivdsservice:: REENUMERATE**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) -Methode und anschließendes Aufrufen der [**ivdsservice:: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) -Methode. Durch diese Kombination von Methoden werden nicht nur neu verbundene und nicht verbundene Datenträger und CD-ROM-Laufwerke ermittelt, sondern alle Datenträger-, Volume-und Plex-Informationen im VDS-Cache für Datenträger, die nicht vor kurzem verbunden oder getrennt wurden. Aufrufen von " **Aktualisieren** ", um die Eigenschafts Informationen vorhandener Objekte im Cache zu aktualisieren. Dieser Vorgang kann das Scannen interner subsystembusse und das warten auf Timeouts einschließen. Beachten Sie, dass VDS den Cache automatisch aktualisiert, sobald eine Änderung auftritt, die eine Benachrichtigung auslöst. Außerdem kann das Aufrufen einer **Aktualisierung** als Antwort auf eine VDS-Benachrichtigung dazu führen, dass eine Endlosschleife von Benachrichtigungen gesendet wird. Aus diesen Gründen sollte die **Aktualisierung** nur aufgerufen werden, wenn angezeigt wird, dass der Cache nicht ordnungsgemäß aktualisiert wird.

**So können Sie Hardware Subsysteme erneut aufzählen**

-   Aufrufen der [**ivdshwprovider:: REENUMERATE**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate) -Methode. Je nach Anbieter kann dieser Vorgang das Senden von Netzwerk Paketen und das warten auf Timeouts, das neudurch führen von SCSI-Bussen und das warten auf Timeouts usw. umfassen.

**So können Sie Hardware Subsystem-Objekte erneut aufzählen**

-   Nennen Sie die [**ivdssubsystem:: REENUMERATE**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate) -Methode, um die Objekte (in der Regel Laufwerke) im-Subsystem zu inventarisieren. Abhängig vom Subsystem kann dieser Vorgang das Scannen interner subsystembusse und das warten auf Timeouts einschließen.

**So aktualisieren Sie Hardware Subsysteme und Subsystem-Objekte**

-   Aufrufen der [**ivdshwprovider:: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh) -Methode, um den VDS-Cache mit Informationen zu vorhandenen Subsystemen zu aktualisieren, die von VDS-Hardwareanbietern verwaltet werden. Beachten Sie, dass VDS den Cache automatisch aktualisiert, sobald eine Änderung auftritt, die eine Benachrichtigung auslöst. Außerdem kann das Aufrufen einer [**Aktualisierung**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) als Antwort auf eine VDS-Benachrichtigung dazu führen, dass eine Endlosschleife von Benachrichtigungen gesendet wird. Aus diesen Gründen sollte die **Aktualisierung** nur aufgerufen werden, wenn angezeigt wird, dass der Cache nicht ordnungsgemäß aktualisiert wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von VDS](using-vds.md)
</dt> <dt>

[**Ivdsservice:: REENUMERATE**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[**Ivdsservice:: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh)
</dt> <dt>

[**Ivdshwprovider:: REENUMERATE**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate)
</dt> <dt>

[**Ivdssubsystem:: REENUMERATE**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate)
</dt> <dt>

[**Ivdshwprovider:: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh)
</dt> </dl>

 

 
