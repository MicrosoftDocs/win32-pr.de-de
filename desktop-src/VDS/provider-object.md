---
description: Das Anbieterobjekt modelliert das Programm, das für die Speicherverwaltung verantwortlich ist.
ms.assetid: 131e927d-d32a-44f6-8aae-28839cfa9e7d
title: Anbieterobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bb64d879b8213970edd5887c2d7a217c434ec38a113d2c9f36cd9e1d73e564d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999465"
---
# <a name="provider-object"></a>Anbieterobjekt

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die Windows Storage Verwaltungs-API. [](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Das Anbieterobjekt modelliert das Programm, das für die Speicherverwaltung verantwortlich ist. Dieses Objekt ermöglicht den Zugriff sowohl auf die Funktionalität des Softwareanbieters als auch des Hardwareanbieters. Anbieterprogramme führen Vorgänge auf Softwaregeräten (Volumes und Datenträger) und Hardwaregeräten (Speichersubsysteme und Arrays von Laufwerken hinter RAID-Controllern) aus.

VDS registriert ein Anbieterobjekt als COM-Objekt in der Windows-Registrierung und verwendet enthaltene Schnittstellen (keine Aggregation), um die verbleibenden Objekte zu implementieren, um alle Schnittstellen und Methoden zu umschließen und bedingt Funktionen hinzufügen. Die Objekte und Schnittstellen, die vom Anbieterobjekt umschlossen werden, unterscheiden sich je nach Anbietertyp.

Sie können ein Anbieterobjekt nicht direkt aus Ihrer Anwendung instanziieren. Stattdessen müssen Sie VDS starten, einen Zeiger auf ein Dienstobjekt abrufen und das Dienstobjekt zum Abfragen der Anbieter verwenden, die dem Host bekannt sind. Anweisungen zum Laden von VDS finden Sie unter [Start- und Dienstobjekte.](startup-and-service-objects.md)

Verwenden Sie [**die IVdsService::QueryProviders-Methode,**](/windows/desktop/api/Vds/nf-vds-ivdsservice-queryproviders) um die registrierten Anbieterprogramme auf einem Host zu aufzählen. Mit dem ersten Parameter der -Methode können Sie nur Softwareanbieter, nur Hardwareanbieter oder beides angeben. Mit einem Anbieterobjekt können Sie Vorgänge für die objekte ausführen, die von diesem Anbieter verwaltet werden. Wie die folgende Abbildung zeigt, können Sie die Methoden verwenden, die von der [**IVdsSwProvider-Schnittstelle**](/windows/desktop/api/Vds/nn-vds-ivdsswprovider) verfügbar gemacht werden, um Paketobjekte zu erstellen und abfragen, die Softwareanbietern zugeordnet sind. Ebenso können Sie die Methoden auf der [**IVdsHwProvider-Schnittstelle**](/windows/desktop/api/Vds/nn-vds-ivdshwprovider) verwenden, um mit den Subsystemobjekten zu interagieren, die Hardwareanbietern zugeordnet sind.

![Diagramm, das eine "Anwendung" zeigt, die in "Anbieter", dann "Pack" oder "Subsystem" und dann in "Achsen" verzweigt ist.](images/vdsproviderobject.png)

Zu den Objekteigenschaften gehören ein persistenter GUID-Objektbezeichner, der einen bestimmten Anbieter darstellt, und eine zweite GUID, die die Anbieterversion darstellt. Beachten Sie, dass andere Objektbezeichner im VDS-Objektmodell nicht persistent sind. Die verbleibenden Eigenschaften für dieses Objekt umfassen einen Anbieternamen, zusätzliche Versionsinformationen, software- oder hardwarebasierten Anbietertyp, verschiedene Flags und eine Einstellung für die Neuerstellungspriorität, die nur für Softwareanbieter gilt.

In der folgenden Tabelle sind verwandte Schnittstellen, Enumerationen und Strukturen aufgeführt. 

| type                                                                                         | Element                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden                                            | [**IVdsProvider**](/windows/desktop/api/Vds/nn-vds-ivdsprovider)                                                                                                                                                                                                                                                           |
| Schnittstellen, die immer nur von Softwareanbietern verfügbar gemacht werden                                | [**IVdsSwProvider**](/windows/desktop/api/Vds/nn-vds-ivdsswprovider)                                                                                                                                                                                                                                                       |
| Schnittstellen, die immer nur von Hardwareanbietern verfügbar gemacht werden                                | [**IVdsHwProvider**](/windows/desktop/api/Vds/nn-vds-ivdshwprovider)                                                                                                                                                                                                                                                       |
| Schnittstellen, die von diesem Objekt verfügbar gemacht werden können                                                | [**IVdsProviderSupport**](/windows/desktop/api/Vds/nn-vds-ivdsprovidersupport)                                                                                                                                                                                                                                             |
| Schnittstellen, die möglicherweise nur von Hardwareanbietern verfügbar gemacht werden                                    | [**IVdsHwProviderType,**](/windows/desktop/api/Vds/nn-vds-ivdshwprovidertype) [**IVdsHwProviderStoragePools**](/windows/desktop/api/Vds/nn-vds-ivdshwproviderstoragepools)**Windows Server 2008, Windows Vista und Windows Server 2003:** Die [**IVdsHwProviderStoragePools-Schnittstelle**](/windows/desktop/api/Vds/nn-vds-ivdshwproviderstoragepools) wird nicht unterstützt.<br/> |
| Schnittstellen, die immer implementiert, aber nicht für Anwendungen verfügbar gemacht werden                       | [**IVdsProviderPrivate**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdsproviderprivate)                                                                                                                                                                                                                                             |
| Schnittstellen, die immer von Hardwareanbietern implementiert, aber nicht für Anwendungen verfügbar gemacht werden | [**IVdsHwProviderPrivate**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdshwproviderprivate)                                                                                                                                                                                                                                         |
| Schnittstellen, die von Hardwareanbietern implementiert, aber nicht für Anwendungen verfügbar gemacht werden können     | [**IVdsHwProviderPrivateMpio**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdshwproviderprivatempio)                                                                                                                                                                                                                                 |
| Zugeordnete Enumerationen                                                                      | [**VDS \_ \_ANBIETERFLAG,**](/windows/desktop/api/Vds/ne-vds-vds_provider_flag) [**\_ VDS-ABFRAGEANBIETERFLAG \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_query_provider_flag)UND [**\_ VDS-ANBIETERTYP \_**](/windows/desktop/api/Vds/ne-vds-vds_provider_type).                                                                                                                         |
| Zugeordnete Strukturen                                                                        | Keine.                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[VDS-Objektmodell](vds-object-model.md)
</dt> <dt>

[Start- und Dienstobjekte](startup-and-service-objects.md)
</dt> <dt>

[**IVdsService::QueryProviders**](/windows/desktop/api/Vds/nf-vds-ivdsservice-queryproviders)
</dt> <dt>

[**IVdsSwProvider**](/windows/desktop/api/Vds/nn-vds-ivdsswprovider)
</dt> <dt>

[**IVdsHwProvider**](/windows/desktop/api/Vds/nn-vds-ivdshwprovider)
</dt> </dl>

 

