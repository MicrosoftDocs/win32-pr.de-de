---
description: Softwareanbieterobjekte
ms.assetid: 0d415238-7558-4d90-a122-e65ae7760344
title: Softwareanbieterobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 507abb00b67b51ad68eb0592ff4fa7b5201cff5be0587b7170662556238feb50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137157"
---
# <a name="software-provider-objects"></a>Softwareanbieterobjekte

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die Windows Storage Verwaltungs-API. [](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Softwareanbieterobjekte modellieren physische Geräte wie IDE-Datenträger und CD-ROMs sowie virtuelle Elemente wie Pakete, Volumes und Volumeplexes. Die folgende Abbildung zeigt die Beziehung zwischen dem Anbieterobjekt und dem Satz von Softwareanbieterobjekten sowie die Beziehung zwischen den verschiedenen Softwareanbieterobjekten selbst.

![Diagramm, das die Beziehung zwischen einem Anbieter und Softwareanbieterobjekten wie "Pack" und "Volume" zeigt.](images/vdsswobjects.png)

Ein Anbieterobjekt kann null oder mehr Pakete enthalten. Ein Paketobjekt kann null oder mehr Datenträger und Volumes enthalten. Ein Volume besteht aus mindestens einem Volumeplex, und jeder Volumeplex kann je nach Plextyp einem oder mehrere Datenträgern zuordnen. VDS verwaltet nicht zugewiesene Datenträger direkt ohne Paketcontainer. In den verbleibenden Themen dieses Abschnitts werden die Objekte pack, disk, volume und volume plex beschrieben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[VDS-Objektmodell](vds-object-model.md)
</dt> </dl>

 

 
