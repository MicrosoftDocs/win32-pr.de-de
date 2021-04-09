---
description: Software Anbieter Objekte
ms.assetid: 0d415238-7558-4d90-a122-e65ae7760344
title: Software Anbieter Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c16f81cd975c892760d1851720e65584453e7745
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "103869335"
---
# <a name="software-provider-objects"></a>Software Anbieter Objekte

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Software Anbieter Objekte modellieren physische Geräte, z. b. IDE-Datenträger und CD-ROMs, sowie virtuelle Elemente wie Pakete, Volumes und Volumeplexes. Die folgende Abbildung zeigt die Beziehung zwischen dem Anbieter Objekt und dem Satz von Softwareanbieter Objekten sowie die Beziehung zwischen den verschiedenen Softwareanbieter Objekten selbst.

![Diagramm, das die Beziehung zwischen einem Anbieter-und Softwareanbieter Objekt, wie z. b. "Pack" und "Volume", anzeigt.](images/vdsswobjects.png)

Ein Anbieter Objekt kann NULL oder mehr Pakete enthalten. Ein Pack-Objekt kann NULL oder mehr Datenträger und Volumes enthalten. Ein Volume besteht aus mindestens einem Volume Plex, und jeder volumeplex kann je nach Plex-Typ einem oder mehreren Datenträgern zugeordnet werden. VDS verwaltet nicht zugewiesene Datenträger direkt ohne Paket Container. In den restlichen Themen dieses Abschnitts werden die Plex-Objekte Pack, Disk, Volume und Volume beschrieben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[VDS-Objektmodell](vds-object-model.md)
</dt> </dl>

 

 
