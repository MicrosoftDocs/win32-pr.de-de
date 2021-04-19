---
description: Hardware Anbieter Objekte
ms.assetid: d1724219-1487-485b-9c52-5003069fe9e2
title: Hardware Anbieter Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1aaebf61e97487b48a6b8bf0dbd91cc6aa3e0bd
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "106353239"
---
# <a name="hardware-provider-objects"></a>Hardware Anbieter Objekte

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Das VDS-Objektmodell enthält eine Reihe von Objekten, mit denen Hardware Anbieter Entitäten abgefragt und konfiguriert werden können. (Beachten Sie, dass VDS zwar einen Softwareanbieter enthält, aber einen Hardware Anbieter und die zugeordnete Hardware separat kaufen müssen, um die Hardware Anbieter Objekte nutzen zu können.) Diese Hardware Anbieter Objekte stellen physische Geräte (z. b. Subsysteme, Laufwerke und Controller) und virtuelle Geräte (z. b. LUNs und LUN-plexes) dar.

Ein Hardware Anbieter sollte ein COM-Objekt für jedes physische oder virtuelle Gerät erstellen.

Die folgende Abbildung zeigt die Beziehung zwischen dem Anbieter Objekt und dem Satz von Hardware Anbieter Objekten sowie die Beziehung zwischen den verschiedenen Hardware Anbieter Objekten selbst.

![Diagramm, das die Beziehung zwischen "Provider" und "Subsystem", "controller", "LUN", "LUN Plex", "Drive" und "Spindel" anzeigt. ](images/vdshwobjects.png)

Ein Anbieter Objekt kann eine beliebige Anzahl von Subsystemen enthalten. Alle Hardware Anbieter können mehrere Instanzen desselben subsystemmodells verwalten. Viele Hardware Anbieter können auch mehrere Instanzen von unterschiedlichen subsystemmodellen verwalten. Ein einzelner Computer kann eine beliebige Anzahl von Hardwareanbietern hosten.

Ein Subsystem-Objekt kann eine beliebige Anzahl von Controllern und Laufwerken enthalten und kann beliebig viele LUNs enthalten. Ein LUN-Objekt besteht aus mindestens einem LUN-Plex, und jeder LUN-Plex ist abhängig vom Plex-Typ einem oder mehreren Laufwerken zugeordnet. Controller Objekte können Dateneingaben/-Ausgaben für eine beliebige Anzahl von LUN-Objekten verwalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[VDS-Objektmodell](vds-object-model.md)
</dt> </dl>

 

 
