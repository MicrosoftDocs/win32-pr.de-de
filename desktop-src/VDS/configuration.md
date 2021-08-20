---
description: Übersicht über die Konfiguration
ms.assetid: 5cdc21a1-ff55-4c36-8106-b045256778ce
title: Übersicht über die Konfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b742cb5ca2f287cd8b50b9f248d0ebec1174bfd71b59f0630bd9fb98864309c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007950"
---
# <a name="configuration-overview"></a>Übersicht über die Konfiguration

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die [Windows Storage Verwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Wenn Sie mit den von VDS definierten Objekten nicht vertraut sind, finden Sie weitere Informationen unter [VDS-Objektmodell.](vds-object-model.md)

Die Konfigurationskomplexität eines virtuellen Datenträgers kann von sehr einfach bis fein abgestimmt reichen. Virtuelle Datenträger vom Typ "No Care", "Free-from-Care" und "Enterprise" definieren drei typische Konfigurationsperspektiven. Jede Perspektive stellt etwas andere Anforderungen dar:

-   Virtuelle Datenträger ohne Sorgfalt sind leicht konfiguriert, möglicherweise nur, um die Partitionierung und Formatierung neuer Datenträger zu automatisieren oder vorübergehend ein gespiegeltes Volume für die Migration von Daten von einem Datenträger zu einem anderen ohne Ausfallzeiten zu erstellen. Solche Datenträger eignen sich gut für Notebookcomputer und andere Systeme mit einem oder einigen wenigen Datenträgern.
-   Virtuelle Datenträger mit kostenloser Behandlung stellen Speicher bereit, der selbstkonfiguriert, selbstreparierend und verfügbar erscheint. verwendet Stripesetvolumes und LUNs, um eine bessere Leistung zu erzielen. verwendet gespiegelte Volumes und LUNs, um eine bessere Verfügbarkeit zu erzielen. und verwendet Pakete, um die Fehlermodi zu bereinigen und einzudämmen. Diese Konfigurationsebene ist ideal, wenn alte, kleine, langsame Systemdatenträger durch neue, große, schnelle Datenträger ersetzt werden. Sie eignet sich auch ideal für die Spiegelung von Daten mit automatisiertem Hot Sparing– eine einzelne Ersatzspindel kann viele Spindeln schützen. Weitere Informationen finden Sie unter [Hot Sparing](hot-sparing.md).

    Kleine SANs hängen von der Flexibilität und Automatisierung ab, die von dieser Konfigurationsebene geboten wird, ebenso wie NAS-Appliances (Network Attached Storage). Virtuelle Datenträger mit kostenloser Verwaltung vereinfachen die Konsolidierung des Anwendungsspeichers , z. B. des Speichers für SQL und Exchange, ohne die Server zu konsolidieren.

-   Enterprise virtuellen Datenträger enthalten sehr große oder komplexe Unternehmenskonfigurationen mit zusätzlichen standort- oder anwendungsspezifischen Anforderungen. Administratoren optimieren das Speichersubsystem für eine einzelne Anwendung, die möglicherweise nur selten ausgeführt wird, z. B. für einen monatlichen Batchberichtsauftrag in einem Bestelltransaktionssystem. Enterprise virtuelle Datenträger müssen skaliert werden, die Echtzeitaktivität des Speichersubsystems anzeigen und die Anforderungen der praktischen Administratoren erfüllen.

Weitere Informationen zu Spiegelungen, Stripes und den anderen Konfigurationsoptionen in VDS finden Sie unter [Volume- und LUN-Bindung.](volume-and-lun-binding.md) Ein erweitertes Konfigurationsverfahren, das als Stapeling bezeichnet wird, ermöglicht es Ihnen, die Konfigurationen zu kombinieren, die vorhandenen Volumes und LUNs zugeordnet sind. Weitere Informationen finden Sie unter [Konfigurationsstapel.](configuration-stacking.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dienst für virtuelle Datenträger](virtual-disk-service-portal.md)
</dt> <dt>

[VDS-Objektmodell](vds-object-model.md)
</dt> <dt>

[Hot Sparing](hot-sparing.md)
</dt> <dt>

[Volume- und LUN-Bindung](volume-and-lun-binding.md)
</dt> <dt>

[Konfigurationsstapel](configuration-stacking.md)
</dt> </dl>

 

 
