---
title: Privater Sensorpool
description: Eine Sammlung biometrischer Einheiten, die für die exklusive Verwendung durch eine Clientanwendung reserviert sind. Private Pools unterstützen proprietäre Authentifizierungsmethoden und ermöglichen einer Clientanwendung den Zugriff auf eine biometrische Einheit mithilfe von vom Anbieter angegebenen Steuerungsbefehlen.
ms.assetid: f0ccbafd-e7a8-4389-bd05-0b062dfc4dc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 306f4e0d4e28cfb29dda694e835348721113a5c23ec51054169537282ae2c365
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119480440"
---
# <a name="private-sensor-pool"></a>Privater Sensorpool

Ein privater Sensorpool ist eine Sammlung biometrischer Einheiten, die für die exklusive Verwendung durch eine Clientanwendung reserviert sind. Private Pools unterstützen proprietäre Authentifizierungsmethoden und ermöglichen einer Clientanwendung den Zugriff auf eine biometrische Einheit mithilfe von vom Anbieter angegebenen Steuerungsbefehlen. Biometrische Einheiten in einem privaten Sensorpool:

-   Sind nur für die Clientanwendung verfügbar, die den Pool erstellt hat.
-   Senden Sie Ereignisbenachrichtigungen, die durch den Abschluss biometrischer Vorgänge generiert wurden, direkt an die Anwendung, ohne den aktuellen Fensterfokus zu beachten.
-   Verwenden Sie GUIDs, um biometrische Vorlagen zu identifizieren.
-   Freigeben einer einzelnen, von der Anwendung ausgewählten Vorlagendatenbank.

Private Sensorpools müssen verwendet werden, wenn die Clientanwendung:

-   Verwaltet eine Sammlung dedizierter biometrischer Einheiten, die eine anwendungsspezifische Vorlagendatenbank verwenden. Ein Beispiel hierfür ist eine Anwendung zur Teilnahme von Mitarbeitern, bei der Mitarbeiter ihre Ankunft bei der Arbeit signalisieren, indem sie mit dem Finger auf einen Fingerabdruckleser wischen. Die Mitarbeiter verfügen nicht über Windows auf dem Computer, auf dem die Anwendung ausgeführt wird. Stattdessen werden ihre Fingerabdrücke durch GUIDs identifiziert, die von der Attendance-Anwendung verwaltet werden.
-   Sammelt biometrische Stichproben, anstatt einfach Stichproben SIDs zu karten.
-   Stellt die Hardware für biometrische Einheiten in den Wartungsmodus ein, um die Firmware zu aktualisieren.
-   Sendet vom Anbieter definierte Steuerungsbefehle an die Hardware oder Software der biometrischen Einheit.
-   Versucht, eine biometrische Einheit mit integriertem Speicher für den Betrieb im erweiterten Modus zu konfigurieren, aber die Einheit kann die erforderlichen Hashvorgänge nicht ausführen.
-   Wird über eine Remotedesktop Clientsitzung ausgeführt.

> [!Note]  
> Anwendungen können private Sensorpools nur für biometrische Fingerabdrücke erstellen. Wenn eine Anwendung versucht, eine für etwas anderes (z. B. Gesichtserkennung) zu erstellen, wird die Anforderung fehlschlagen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines privaten Sensorpools](creating-a-private-sensor-pool.md)
</dt> <dt>

[Sensorpools](sensor-pools.md)
</dt> <dt>

[Systemsensorpool](system-sensor-pool.md)
</dt> </dl>

 

 




