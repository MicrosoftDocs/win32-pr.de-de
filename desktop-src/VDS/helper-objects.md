---
description: 'VDS bietet zwei Hilfsobjekte: das-Enumerationsobjekt und das Async-Objekt. In diesem Thema werden die einzelnen Objekte beschrieben und Links zu Beispielen für die Funktionsweise von Aufrufern von Aufrufern bereitstellt.'
ms.assetid: 0f809c71-a3bd-4c62-8086-9651ea1a3400
title: Hilfsobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac5193003abd10d9fa2c311b250272d9ad5847a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218501"
---
# <a name="helper-objects"></a>Hilfsobjekte

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

VDS bietet zwei Hilfsobjekte: das-Enumerationsobjekt und das Async-Objekt. In diesem Thema werden die einzelnen Objekte beschrieben und Links zu Beispielen für die Funktionsweise von Aufrufern von Aufrufern bereitstellt.

## <a name="enumeration-object"></a>Enumerationsobjekt

Ein Enumerationsobjekt listet einen Satz von VDS-Objekten eines bestimmten Typs auf. Bei Objekten kann es sich um Anbieter, Subsysteme, Controller, LUNs, LUN-plexes, Laufwerke, Festplatten Pakete, Datenträger, Volumes oder Volumeplexes handeln. Aufrufer können einen Zeiger auf ein bestimmtes Objekt erhalten, indem Sie das gewünschte Objekt aus der-Enumeration auswählen, das von der entsprechenden-Methode zurückgegeben wird. Ein Codebeispiel finden Sie unter [Arbeiten mit enumerationsobjekten](working-with-enumeration-objects.md).

In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet. 

| type                                              | Element                                  |
|---------------------------------------------------|------------------------------------------|
| Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden | [**Ienumvdsobject**](/windows/desktop/api/Vds/nn-vds-ienumvdsobject) |
| Zugehörige Enumerationen                           | Keine.                                    |
| Zugeordnete Strukturen                             | Keine.                                    |



 

## <a name="async-object"></a>Async-Objekt

Asynchrone Vorgänge werden von einem Async-Objekt verwaltet. Methoden, die asynchrone Vorgänge initiieren, geben einen Zeiger auf eine [**ivdsasync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) -Schnittstelle zurück, die es dem Aufrufer ermöglicht, den Status des asynchronen Vorgangs abzubrechen, zu warten und abzufragen.

VDS-Vorgänge mit langer Ausführungszeit werden in der Regel asynchron implementiert. Die Softwareanbieter Programme Basic und Dynamic implementieren asynchrone Methoden konsistent für Volume-, Partitions-und Datenträger Vorgänge. Hardware Anbieter implementieren optional asynchrone Methoden, die asynchron in Beziehung stehen. Unabhängig davon, wie der Anbieter die-Methode implementiert, muss der Vorgang einen Zeiger auf eine [**ivdsasync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) -Schnittstelle an den Aufrufer zurückgeben. Ein Codebeispiel finden Sie unter [Verwalten von asynchronen Vorgängen](managing-asynchronous-operations.md).

Zu den asynchronen Vorgängen gehören:

-   Erstellen einer LUN, eines Volumes oder einer Partition.
-   Formatieren eines Volumes oder einer Partition.
-   Hinzufügen oder Entfernen einer LUN oder eines volumeplex.
-   Aufteilen eines volumeplex.
-   Erweitern oder Verkleinern einer LUN oder eines Volumes.
-   Wiederherstellen einer LUN oder eines Volumes.
-   Bereinigen eines Datenträgers.
-   Ersetzen eines Datenträgers.

In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet. 

| type                                              | Element                        |
|---------------------------------------------------|--------------------------------|
| Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden | [**Ivdsasync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) |
| Zugehörige Enumerationen                           | Keine.                          |
| Zugeordnete Strukturen                             | Keine.                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[VDS-Objektmodell](vds-object-model.md)
</dt> <dt>

[**Ivdsasync**](/windows/desktop/api/Vds/nn-vds-ivdsasync)
</dt> <dt>

[Arbeiten mit enumerationsobjekten](working-with-enumeration-objects.md)
</dt> <dt>

[Verwalten von asynchronen Vorgängen](managing-asynchronous-operations.md)
</dt> </dl>

 

 
