---
description: Konfigurations Übersicht
ms.assetid: 5cdc21a1-ff55-4c36-8106-b045256778ce
title: Konfigurations Übersicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4db13827bf08ee65ed8015f0c19ba2980a9a71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958860"
---
# <a name="configuration-overview"></a>Konfigurations Übersicht

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Wenn Sie mit den von VDS definierten Objekten nicht vertraut sind, lesen Sie das [VDS-Objektmodell](vds-object-model.md).

Die Konfigurations Komplexität eines virtuellen Datenträgers kann von sehr einfach bis fein optimiert reichen. Die virtuellen Datenträger "keine Sorgfalt", "kostenlos" und "Enterprise" definieren drei typische Konfigurations Perspektiven. Jede Perspektive weist etwas andere Anforderungen auf:

-   Virtuelle Datenträger ohne Sorgfalt sind leicht zu konfigurieren, vielleicht nur zur Automatisierung der Partitionierung und Formatierung neuer Datenträger oder zum vorübergehenden Erstellen eines gespiegelten Volumes für die Migration von Daten von einem Datenträger zu einem anderen ohne Ausfallzeiten. Solche Datenträger eignen sich für Notebook-Computer und andere Systeme mit einem oder wenigen Datenträgern.
-   Virtuelle Datenträger mit freiem Speicherplatz bieten Speicher, der selbst konfigurierend, Selbstreparatur und verfügbar erscheint. verwendet Stripesetvolumes und LUNs, um eine bessere Leistung zu erzielen. verwendet gespiegelte Volumes und LUNs, um eine bessere Verfügbarkeit zu erzielen. und verwendet Pakete, um die Fehlermodi zu bereinigen und zu enthalten. Diese Konfigurations Ebene ist ideal, wenn Sie alte, kleine, langsame System Datenträger durch neue, große, schnelle Datenträger ersetzen. Sie eignet sich außerdem ideal für die Spiegelung von Daten mit automatischem hotsparsam – mit einer einzelnen Ersatz Spindel können viele Spindeln geschützt werden. Weitere Informationen finden Sie unter [Hot sparsam](hot-sparing.md).

    Kleine Sans sind abhängig von der Flexibilität und Automatisierung, die von dieser Konfigurations Ebene angeboten wird, wie NAS-Geräte (Network Attached Storage). Virtuelle Datenträger ohne Datenträger vereinfachen die Konsolidierung des Anwendungs Speichers – z. b. den Speicher für SQL und Exchange – ohne die Server zu konsolidieren.

-   Virtuelle Enterprise-Datenträger enthalten sehr große oder komplexe Unternehmens Konfigurationen mit zusätzlichen standortspezifischen oder anwendungsspezifischen Anforderungen. Administratoren optimieren das Speichersubsystem für eine einzelne Anwendung, die nur selten ausgeführt werden kann, z. b. ein monatlicher Batch Berichterstattungs Auftrag in einem Transaktionssystem, der die Bestellung übernimmt. Virtuelle Enterprise-Datenträger müssen skaliert werden, die Echt Zeit Aktivität des Speicher Subsystems anzeigen und die Anforderungen von praktischen Administratoren erfüllen.

Weitere Informationen zu spiegeln, Streifen und anderen Konfigurationsoptionen in VDS finden Sie unter [Volume-und LUN-Bindung](volume-and-lun-binding.md). Mit einer erweiterten Konfigurations Methode, die als Stapeln bezeichnet wird, können Sie die Konfigurationen kombinieren, die vorhandenen Volumes und LUNs zugeordnet sind. Weitere Informationen finden Sie unter [Konfigurations Stapel](configuration-stacking.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dienst für virtuelle Datenträger](virtual-disk-service-portal.md)
</dt> <dt>

[VDS-Objektmodell](vds-object-model.md)
</dt> <dt>

[Heiß sparsam](hot-sparing.md)
</dt> <dt>

[Volume- und LUN-Bindung](volume-and-lun-binding.md)
</dt> <dt>

[Konfigurations Stapel](configuration-stacking.md)
</dt> </dl>

 

 
