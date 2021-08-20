---
description: 'VDS stellt zwei Hilfsobjekte bereit: das Enumerationsobjekt und das asynchrone Objekt. Dieses Thema beschreibt jedes dieser Objekte und enthält Links zu Beispielen für die Arbeit von Aufrufern mit den einzelnen Objekten.'
ms.assetid: 0f809c71-a3bd-4c62-8086-9651ea1a3400
title: Hilfsobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98464c31548309b50e21b2b8e3e20a867efe7ca647d7a9879efd0ef346e6a147
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999480"
---
# <a name="helper-objects"></a>Hilfsobjekte

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die [Windows Storage Verwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

VDS stellt zwei Hilfsobjekte bereit: das Enumerationsobjekt und das asynchrone Objekt. Dieses Thema beschreibt jedes dieser Objekte und enthält Links zu Beispielen für die Arbeit von Aufrufern mit den einzelnen Objekten.

## <a name="enumeration-object"></a>Enumerationsobjekt

Ein Enumerationsobjekt listet einen Satz von VDS-Objekten eines bestimmten Typs auf. Objekte können Anbieter, Subsysteme, Controller, LUNs, LUN-Plexes, Laufwerke, Datenträgerpakete, Datenträger, Volumes oder Volumeplexes sein. Aufrufer können einen Zeiger auf ein bestimmtes Objekt abrufen, indem sie das gewünschte Objekt aus der Enumeration auswählen, die von der entsprechenden Methode zurückgegeben wird. Ein Codebeispiel finden Sie unter [Arbeiten mit Enumerationsobjekten.](working-with-enumeration-objects.md)

In der folgenden Tabelle sind verwandte Schnittstellen, Enumerationen und Strukturen aufgeführt. 

| type                                              | Element                                  |
|---------------------------------------------------|------------------------------------------|
| Schnittstellen, die immer von diesem Objekt verfügbar gemacht werden | [**IEnumVdsObject**](/windows/desktop/api/Vds/nn-vds-ienumvdsobject) |
| Zugeordnete Enumerationen                           | Keine.                                    |
| Zugeordnete Strukturen                             | Keine.                                    |



 

## <a name="async-object"></a>Asynchrones Objekt

Ein asynchrones Objekt verwaltet asynchrone Vorgänge. Methoden, die asynchrone Vorgänge initiieren, geben einen Zeiger auf eine [**IVdsAsync-Schnittstelle**](/windows/desktop/api/Vds/nn-vds-ivdsasync) zurück, wodurch der Aufrufer den Status des asynchronen Vorgangs abbrechen, warten und abfragen kann.

VDS-Vorgänge mit langer Ausführungslaufzeit werden in der Regel asynchron implementiert. Die grundlegenden und dynamischen Softwareanbieterprogramme implementieren asynchrone Methoden konsistent für Volume-, Partitions- und Datenträgervorgänge. Hardwareanbieter implementieren optional asynchron bezogene Methoden asynchron. Unabhängig davon, wie der Anbieter die -Methode implementiert, muss der Vorgang einen Zeiger auf eine [**IVdsAsync-Schnittstelle**](/windows/desktop/api/Vds/nn-vds-ivdsasync) an den Aufrufer zurückgeben. Ein Codebeispiel finden Sie unter [Verwalten von asynchronen Vorgängen.](managing-asynchronous-operations.md)

Asynchrone Vorgänge umfassen Folgendes:

-   Erstellen einer LUN, eines Volumes oder einer Partition.
-   Formatieren eines Volumes oder einer Partition.
-   Hinzufügen oder Entfernen einer LUN oder volume plex.
-   Breaking a volume plex (Breaking a Volume Plex).
-   Erweitern oder Verkleinern einer LUN oder eines Volumes.
-   Wiederherstellen einer LUN oder eines Volumes.
-   Bereinigen eines Datenträgers.
-   Ersetzen eines Datenträgers.

In der folgenden Tabelle sind verwandte Schnittstellen, Enumerationen und Strukturen aufgeführt. 

| type                                              | Element                        |
|---------------------------------------------------|--------------------------------|
| Schnittstellen, die immer von diesem Objekt verfügbar gemacht werden | [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) |
| Zugeordnete Enumerationen                           | Keine.                          |
| Zugeordnete Strukturen                             | Keine.                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[VDS-Objektmodell](vds-object-model.md)
</dt> <dt>

[**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync)
</dt> <dt>

[Arbeiten mit Enumerationsobjekten](working-with-enumeration-objects.md)
</dt> <dt>

[Verwalten asynchroner Vorgänge](managing-asynchronous-operations.md)
</dt> </dl>

 

 
