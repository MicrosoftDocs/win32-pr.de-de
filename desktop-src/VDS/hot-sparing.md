---
description: Hot Sparing
ms.assetid: 2faf2f3f-f459-4e41-9c8e-042c7b72281b
title: Hot Sparing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61b8df9bc27e303277c869901872a9b879cb2d7df32764589501b9d33a51c3fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125950"
---
# <a name="hot-sparing"></a>Hot Sparing

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die [Windows Storage Verwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Hot Sparing ist die Ersetzung eines Datenträgers oder Laufwerks durch einen fehlerhaften oder fehlerhaften Datenträger oder ein fehlerhaftes Laufwerk. (Hardwareanbieter agieren auf Laufwerken, Softwareanbieter agieren auf Datenträgern.) Sie können ein Hotsparlaufwerk für alle LUNs im Subsystem freigeben oder es einer bestimmten LUN zuordnen. Ebenso können Sie einen Hotspardatenträger einem einzelnen Volume, einem Paket und einem Softwareanbieter zuordnen oder ihn für alle Hosts in einem SAN freigeben.

Wenn das zugeordnete Volume oder die zugehörige LUN fehlertolerant ist, können Sie ein Hotspare für einen ausgefallenen Datenträger oder ein Laufwerk ersetzen und alle betroffenen Paritäts-RAID- oder Spiegelungen neu erstellen. Sie können einen fehlerhaften Datenträger auch dann durch einen Hotspare ersetzen, wenn das zugeordnete Volume oder die zugehörige LUN nicht fehlertolerant ist. Unter der Annahme, dass Sie den bevorstehenden Fehler vor einem schwerwiegenden Datenverlust ermitteln können, können Sie das Hotspare vorübergehend auf den fehlerhaften Datenträger oder das fehlerhafte Laufwerk spiegeln und dann den fehlerhaften Datenträger oder das fehlerhafte Laufwerk entfernen.

Hot Sparing kann automatisch oder manuell erfolgen. Wenn ein Anbieter automatisches Hot Sparing implementiert, führt er die Ersetzung dynamisch aus. Manuelles HotSparen erfordert Operator- oder Anwendungseingriff. Ein Hotspare kann Teildaten oder Formatierungen aus einer vorherigen Verwendung enthalten. VDS überschreibt den Hotspare, wenn die Ersetzung erfolgt.

Sie können kein Hotspare für gewöhnliche Bindungsvorgänge verwenden. Wenn der Hotspare größer als der ausgefallene Datenträger oder das ausgefallene Laufwerk ist, bleibt jeglicher zusätzlicher Speicherplatz ungenutzt, bis er explizit für die Bindung verfügbar deklariert wird. Sobald der Hotspare für die Wiederherstellung verwendet wurde, ist der Datenträger oder das Laufwerk kein Hotspare mehr. Anders ausgedrückt: Eine 16-Gigabyte-Spindel kann nicht als zwei 8-Gigabyte-Hotspares fungieren.

 

 
