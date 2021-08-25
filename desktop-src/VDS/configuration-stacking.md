---
description: Konfigurationsstapeling
ms.assetid: 1f0f75d6-3553-4ee1-8ee6-bd617da4a109
title: Konfigurationsstapeling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9018a2484ce4e5b9121d08abffee54911531b7f421cfef75643594e827fe350e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905560"
---
# <a name="configuration-stacking"></a>Konfigurationsstapeling

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die Windows Storage Verwaltungs-API. [](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Beim Stapeln wird ein Satz logischer Blockzuordnungen verkettet. Sie können mehrere LUNs aus dem gleichen Subsystem unter einer LUN stapeln. Sie können eine LUN zusammen mit Volumes aus demselben Paket unter einem Volume stapeln. Darüber hinaus können Sie mehrere LUNs stapeln, die von heterogenen Subsystemen unter einem Volume zur Oberfläche kommen.

Wie die folgende Abbildung zeigt, ändert das Erstellen eines Volumes nicht die vorhandene Bindung einer beitragenden LUN. Ebenso wird durch das Entbinden eines Volumes die Bindung einer beitragenden LUN nicht entbinden. Die Abbildung zeigt die RAID 0 1(0+1)-Konfiguration. Diese bekannte Konfiguration kombiniert Striping (RAID 0) und Spiegelung (RAID 1), die den schnellen Datenzugriff von RAID 0 mit der Zuverlässigkeit von RAID 1 kombinieren.

![Diagramm, das eine RAID 0 1(0+1)-Konfiguration zeigt.](images/vdsstacklunvolzeroplusone.png)

Beitragende LUNs können unterschiedliche Bindungstypen haben. Viele Konfigurationen sind mit VDS möglich, aber sehr unwahrscheinlich, z. B. die nächste Abbildung. In diesem Beispiel ist ein Volumeplex eine Striping-LUN, die andere eine dreigespiegelte LUN.

![Diagramm, das eine VDS-Konfiguration zeigt, bei der ein Volumeplex eine Striping-LUN und die andere eine gespiegelte 3-Wege-LUN ist.](images/vdsstacklunvol.png)

Obwohl dies nicht praktikabel ist, veranschaulicht dieses Beispiel einen wichtigen Aspekt des Stapelns. Da das Stapeln Plexe verkettet, fügt VDS die drei LUN-Plexes den beiden Volumeplexes für insgesamt fünf Plexe hinzu.

 

 
