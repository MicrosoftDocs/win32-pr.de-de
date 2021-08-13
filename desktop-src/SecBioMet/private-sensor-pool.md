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
-   Senden Sie Ereignishinweise, die durch den Abschluss biometrischer Vorgänge generiert werden, direkt an die Anwendung, ohne den aktuellen Fensterfokus zu berücksichtigen.
-   Verwenden Sie GUIDs, um biometrische Vorlagen zu identifizieren.
-   Geben Sie eine einzelne, von der Anwendung ausgewählte Vorlagendatenbank frei.

Private Sensorpools müssen verwendet werden, wenn die Clientanwendung:

-   Verwaltet eine Sammlung dedizierter biometrischer Einheiten, die eine anwendungsspezifische Vorlagendatenbank verwenden. Stellen Sie sich beispielsweise eine Anwendung zur Mitarbeiterbetätigung vor, bei der Mitarbeiter ihre Ankunft bei der Arbeit signalisieren, indem sie mit dem Finger auf einen Fingerabdruckleser wischen. Die Mitarbeiter verfügen nicht über Windows Konten auf dem Computer, auf dem die Anwendung ausgeführt wird. Stattdessen werden ihre Fingerabdrücke durch GUIDs identifiziert, die von der Attendance-Anwendung verwaltet werden.
-   Erfasst biometrische Stichproben, anstatt einfach SiDs Stichproben zuzubilden.
-   Versetzt die Hardware biometrischer Einheiten in den Wartungsmodus, um die Firmware zu aktualisieren.
-   Sendet vom Hersteller definierte Steuerungsbefehle an die Hardware oder Software der biometrischen Einheit.
-   Versucht, eine biometrische Einheit mit Integriertem Speicher für den Betrieb im erweiterten Modus zu konfigurieren, aber die Einheit kann die erforderlichen Hashvorgänge nicht ausführen.
-   Wird über eine Remotedesktop Clientsitzung ausgeführt.

> [!Note]  
> Anwendungen können private Sensorpools nur für biometrische Fingerabdruckdaten erstellen. Wenn eine Anwendung versucht, eine Für andere Zwecke (z. B. Gesichtssuche) zu erstellen, schlägt die Anforderung fehl.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines privaten Sensorpools](creating-a-private-sensor-pool.md)
</dt> <dt>

[Sensorpools](sensor-pools.md)
</dt> <dt>

[Systemsensorpool](system-sensor-pool.md)
</dt> </dl>

 

 




