---
description: Das Anbieter Objekt modelliert das Programm, das für die Speicherverwaltung zuständig ist.
ms.assetid: 131e927d-d32a-44f6-8aae-28839cfa9e7d
title: Anbieter Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb36517f0091776b9429911212610134f31077a2
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104553091"
---
# <a name="provider-object"></a>Anbieter Objekt

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Das Anbieter Objekt modelliert das Programm, das für die Speicherverwaltung zuständig ist. Dieses Objekt ermöglicht den Zugriff auf die Funktionalität des Softwareanbieters und des Hardware Anbieters. Anbieter Programme führen Vorgänge für Software Geräte (Volumes und Datenträger) und Hardware Geräte (Speicher Subsysteme und Arrays von Laufwerken hinter RAID-Controllern) aus.

VDS registriert ein Anbieter Objekt als COM-Objekt in der Windows-Registrierung und verwendet enthaltene Schnittstellen (keine Aggregation), um die restlichen Objekte zu implementieren, wobei alle Schnittstellen und Methoden umwickelt und Funktionen bedingt hinzugefügt werden. Die Objekte und Schnittstellen, die vom Anbieter Objekt umschließt werden, unterscheiden sich je nach Anbietertyp.

Es ist nicht möglich, ein Anbieter Objekt direkt aus der Anwendung zu instanziieren. Stattdessen müssen Sie VDS starten, einen Zeiger auf ein Dienst Objekt abrufen und das Dienst Objekt verwenden, um die dem Host bekannten Anbieter abzufragen. Anweisungen zum Laden von VDS finden Sie unter [Start-und Dienst Objekte](startup-and-service-objects.md).

Verwenden Sie die [**ivdsservice:: queryproviders**](/windows/desktop/api/Vds/nf-vds-ivdsservice-queryproviders) -Methode, um die registrierten Anbieter Programme auf einem Host aufzuzählen. Mit dem ersten Parameter der-Methode können Sie nur Softwareanbieter, nur Hardware Anbieter oder beides angeben. Mit einem Provider-Objekt können Sie Vorgänge für die Objekte ausführen, die von diesem Anbieter verwaltet werden. Wie die folgende Abbildung zeigt, können Sie die Methoden verwenden, die von der [**ivdsswprovider**](/windows/desktop/api/Vds/nn-vds-ivdsswprovider) -Schnittstelle verfügbar gemacht werden, um Paket Objekte zu erstellen und abzufragen, die mit Softwareanbietern verknüpft sind. Ebenso können Sie die Methoden der [**ivdshwprovider**](/windows/desktop/api/Vds/nn-vds-ivdshwprovider) -Schnittstelle verwenden, um mit den Subsystem-Objekten zu interagieren, die Hardwareanbietern zugeordnet sind.

![Diagramm, das eine "Anwendung" in "Providers", dann "Pack", "Subsystem" und dann "Spindles" anzeigt.](images/vdsproviderobject.png)

Objekteigenschaften enthalten einen beständigen GUID-Objekt Bezeichner, der einen bestimmten Anbieter darstellt, und eine zweite GUID, die die Anbieter Version darstellt. Beachten Sie, dass andere Objekt Bezeichner im VDS-Objektmodell nicht permanent sind. Die restlichen Eigenschaften für dieses Objekt umfassen einen Anbieter Namen, zusätzliche Versionsinformationen, den Anbietertyp Software oder die Hardware), verschiedene Flags und eine Einstellung für die Neuerstellungs Priorität, die nur für Softwareanbieter gilt.

In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet. 

| type                                                                                         | Element                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden                                            | [**Ivdsprovider**](/windows/desktop/api/Vds/nn-vds-ivdsprovider)                                                                                                                                                                                                                                                           |
| Schnittstellen, die immer nur von Softwareanbietern verfügbar gemacht werden                                | [**Ivdsswprovider**](/windows/desktop/api/Vds/nn-vds-ivdsswprovider)                                                                                                                                                                                                                                                       |
| Schnittstellen, die immer nur von Hardwareanbietern verfügbar gemacht werden                                | [**Ivdshwprovider**](/windows/desktop/api/Vds/nn-vds-ivdshwprovider)                                                                                                                                                                                                                                                       |
| Schnittstellen, die von diesem Objekt verfügbar gemacht werden können                                                | [**Ivdsprovidersupport**](/windows/desktop/api/Vds/nn-vds-ivdsprovidersupport)                                                                                                                                                                                                                                             |
| Schnittstellen, die möglicherweise nur von Hardwareanbietern verfügbar gemacht werden                                    | [**Ivdshwprovidertype**](/windows/desktop/api/Vds/nn-vds-ivdshwprovidertype), [**ivdshwproviderstoragepools**](/windows/desktop/api/Vds/nn-vds-ivdshwproviderstoragepools)**Windows Server 2008, Windows Vista und Windows Server 2003:** die [**ivdshwproviderstoragepools**](/windows/desktop/api/Vds/nn-vds-ivdshwproviderstoragepools) -Schnittstelle wird nicht unterstützt.<br/> |
| Schnittstellen, die immer implementiert, aber nicht für Anwendungen verfügbar gemacht werden                       | [**Ivdsproviderprivate**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdsproviderprivate)                                                                                                                                                                                                                                             |
| Schnittstellen, die immer von Hardwareanbietern implementiert werden, aber nicht für Anwendungen verfügbar gemacht werden | [**Ivdshwproviderprivate**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdshwproviderprivate)                                                                                                                                                                                                                                         |
| Schnittstellen, die möglicherweise von Hardwareanbietern implementiert, aber nicht für Anwendungen verfügbar gemacht werden     | [**Ivdshwproviderprivatempio**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdshwproviderprivatempio)                                                                                                                                                                                                                                 |
| Zugehörige Enumerationen                                                                      | [**VDS \_ \_Anbieterflag**](/windows/desktop/api/Vds/ne-vds-vds_provider_flag), [**VDS- \_ Abfrage \_ \_ anbieterflag**](/windows/desktop/api/Vds/ne-vds-vds_query_provider_flag)und [**VDS- \_ \_ Anbietertyp**](/windows/desktop/api/Vds/ne-vds-vds_provider_type).                                                                                                                         |
| Zugeordnete Strukturen                                                                        | Keine.                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[VDS-Objektmodell](vds-object-model.md)
</dt> <dt>

[Start-und Dienst Objekte](startup-and-service-objects.md)
</dt> <dt>

[**Ivdsservice:: queryproviders**](/windows/desktop/api/Vds/nf-vds-ivdsservice-queryproviders)
</dt> <dt>

[**Ivdsswprovider**](/windows/desktop/api/Vds/nn-vds-ivdsswprovider)
</dt> <dt>

[**Ivdshwprovider**](/windows/desktop/api/Vds/nn-vds-ivdshwprovider)
</dt> </dl>

 

