---
description: Konfigurations Stapel
ms.assetid: 1f0f75d6-3553-4ee1-8ee6-bd617da4a109
title: Konfigurations Stapel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b50b90629556b5ed00db712b49fe8fa4e48ea8cc
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104554710"
---
# <a name="configuration-stacking"></a>Konfigurations Stapel

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Das Stapeln umfasst die Verkettung eines Satzes logischer Block Zuordnungen. Sie können mehrere LUNs aus demselben Subsystem in einer LUN stapeln. Sie können eine LUN mit Volumes aus demselben Paket unter einem Volume stapeln. Außerdem können Sie mehrere LUNs Stapeln, die von heterogenen Subsystemen unter einem Volume angezeigt werden.

Wie in der folgenden Abbildung gezeigt, wird durch das Erstellen eines Volumes die vorhandene Bindung einer Beitragenden LUN nicht geändert. Ebenso wird durch die Bindung eines Volumes nicht die Bindung einer Beitragenden LUN aufgehoben. Die Abbildung zeigt die RAID 0 1 (0 + 1)-Konfiguration. Diese bekannte Konfiguration kombiniert Striping (RAID 0) und Spiegelung (RAID 1), die den schnellen Datenzugriff von RAID 0 mit der Zuverlässigkeit von RAID 1 verbindet.

![Diagramm, das eine RAID 0 1 (0 + 1)-Konfiguration anzeigt.](images/vdsstacklunvolzeroplusone.png)

Beitragende LUNs können unterschiedliche Bindungs Typen aufweisen. Viele Konfigurationen sind mit VDS möglich, sind aber sehr unwahrscheinlich, wie z. b. in der nächsten Abbildung. In diesem Beispiel ist ein Volume Plex eine stripesetlun und die andere eine drei-Wege-gespiegelte LUN.

![Diagramm, das eine VDS-Konfiguration anzeigt, bei der ein Volume Plex eine stripesetlun und die andere eine 3-Wege-gespiegelte LUN ist.](images/vdsstacklunvol.png)

Obwohl dieses Beispiel nicht praktikabel ist, wird ein wichtiger Aspekt beim Stapeln veranschaulicht. Da das Stapeln verkettet, fügt VDS die drei LUN-plexes den beiden volumeplexen für insgesamt fünf plexes hinzu.

 

 
