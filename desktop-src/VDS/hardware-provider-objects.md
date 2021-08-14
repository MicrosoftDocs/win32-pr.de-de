---
description: Hardwareanbieterobjekte
ms.assetid: d1724219-1487-485b-9c52-5003069fe9e2
title: Hardwareanbieterobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c0050b6a9754b25b6a5027d9470cb2fc46911bf4ab3ef852454d1f0698a1d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125964"
---
# <a name="hardware-provider-objects"></a>Hardwareanbieterobjekte

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die [Windows Storage Verwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Das VDS-Objektmodell enthält eine Reihe von Objekten zum Abfragen und Konfigurieren von Hardwareanbieterentitäten. (Beachten Sie, dass VDS zwar einen Softwareanbieter enthält, sie aber separat einen Hardwareanbieter und die zugehörige Hardware erwerben müssen, um die Hardwareanbieterobjekte nutzen zu können.) Diese Hardwareanbieterobjekte stellen physische Geräte (z. B. Subsysteme, Laufwerke und Controller) und virtuelle Geräte (z. B. LUNs und LUN-Plexes) dar.

Ein Hardwareanbieter sollte ein COM-Objekt für jedes physische oder virtuelle Gerät erstellen.

Die folgende Abbildung zeigt die Beziehung zwischen dem Anbieterobjekt und dem Satz von Hardwareanbieterobjekten sowie die Beziehung zwischen den verschiedenen Hardwareanbieterobjekten selbst.

![Diagramm, das die Beziehung zwischen "Provider" und "Subsystem", "Controller", "LUN", "LUN plex", "Drive" und "Spindel" zeigt. ](images/vdshwobjects.png)

Ein Anbieterobjekt kann eine beliebige Anzahl von Subsystemen enthalten. Alle Hardwareanbieter können mehrere Instanzen desselben Subsystemmodells verwalten. Viele Hardwareanbieter können auch mehrere Instanzen verschiedener Subsystemmodelle verwalten. Ein einzelner Computer kann eine beliebige Anzahl von Hardwareanbietern hosten.

Ein Subsystemobjekt kann eine beliebige Anzahl von Controllern und Laufwerken enthalten und eine beliebige Anzahl von LUNs aufweisen. Ein LUN-Objekt besteht aus mindestens einem LUN-Plex, und jedes LUN-Plex wird je nach Plextyp einem oder mehreren Laufwerken zugeordnet. Controllerobjekte können die Dateneingabe/-ausgabe für eine beliebige Anzahl von LUN-Objekten verwalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[VDS-Objektmodell](vds-object-model.md)
</dt> </dl>

 

 
