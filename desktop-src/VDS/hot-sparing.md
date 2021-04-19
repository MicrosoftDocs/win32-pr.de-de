---
description: Heiß sparsam
ms.assetid: 2faf2f3f-f459-4e41-9c8e-042c7b72281b
title: Heiß sparsam
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a4d007e9219ea79ae3bda31be595c33b537661a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360873"
---
# <a name="hot-sparing"></a>Heiß sparsam

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Hot sparsam ist die Ersetzung eines Datenträgers oder Laufwerks für einen fehlerhaften oder fehlgeschlagenen Datenträger oder ein Laufwerk. (Hardware Anbieter agieren auf Laufwerken; Softwareanbieter agieren auf Datenträgern.) Sie können ein Hot-Spare-Laufwerk für alle LUNs im Subsystem freigeben oder einer bestimmten LUN zuordnen. Ebenso können Sie einen Hotspare-Datenträger einem einzelnen Volume, Paket und Softwareanbieter zuordnen oder für alle Hosts in einem San freigeben.

Wenn das zugeordnete Volume oder die LUN fehlertolerant ist, können Sie einen Hotspare durch einen fehlerhaften Datenträger oder ein fehlerhafter Laufwerk ersetzen und alle betroffenen Paritäts-RAID oder-Spiegel neu erstellen. Sie können einen Hotspare durch einen fehlerhaften Datenträger ersetzen, auch wenn das zugehörige Volume oder die LUN nicht fehlertolerant ist. Vorausgesetzt, Sie können den bevorstehenden Fehler vor einem schwerwiegenden Datenverlust ermitteln, können Sie den Hot Spare vorübergehend auf dem fehlerhaften Datenträger oder Laufwerk spiegeln und dann den fehlerhaften Datenträger oder das Laufwerk entfernen.

Hot sparsam kann automatisch oder manuell erfolgen. Wenn ein Anbieter automatische heiße sparsam implementiert, führt er die Ersetzung dynamisch aus. Manuelles Hot sparsam erfordert Operator-oder Anwendungs Eingriffe. Ein Hot Spare kann partielle Daten oder Formatierungen aus einer vorherigen Verwendung enthalten. VDS überschreibt den Hotspare, wenn die Ersetzung auftritt.

Es ist nicht möglich, einen Hotspare für normale Bindungs Vorgänge zu verwenden. Wenn der Hotspare größer ist als der fehlgeschlagene Datenträger oder das Laufwerk, bleibt der überschüssige Speicherplatz so lange ungenutzt, bis er explizit für die Bindung zur Verfügung steht. Sobald der Hotspare für die Wiederherstellung verwendet wurde, ist der Datenträger oder das Laufwerk kein Hot Spare mehr. Anders ausgedrückt: eine Spindel mit 1 16 Gigabyte kann nicht als "2 8-Gigabyte Hot Spares" fungieren.

 

 
