---
title: Privater Sensor Pool
description: Eine Sammlung biometrischer Einheiten, die für die ausschließliche Verwendung durch eine Client Anwendung reserviert sind. Private Pools unterstützen proprietäre Authentifizierungsmethoden und ermöglichen es einer Client Anwendung, mithilfe von vom Hersteller angegebenen Steuerungs Befehlen auf eine biometrische Einheit zuzugreifen.
ms.assetid: f0ccbafd-e7a8-4389-bd05-0b062dfc4dc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf829290b0e412247b5e629a46e8c0efdafb4880
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207311"
---
# <a name="private-sensor-pool"></a>Privater Sensor Pool

Ein privater Sensor Pool ist eine Sammlung von biometrischen Einheiten, die für die ausschließliche Verwendung durch eine Client Anwendung reserviert sind. Private Pools unterstützen proprietäre Authentifizierungsmethoden und ermöglichen es einer Client Anwendung, mithilfe von vom Hersteller angegebenen Steuerungs Befehlen auf eine biometrische Einheit zuzugreifen. Biometrische Einheiten in einem privaten Sensor Pool:

-   Sind nur für die Client Anwendung verfügbar, die den Pool erstellt hat.
-   Sendet Ereignis Hinweise, die durch den Abschluss von biometrischen Vorgängen generiert wurden, ohne Berücksichtigung des aktuellen Fenster Fokus direkt an die Anwendung.
-   Verwenden Sie GUIDs, um biometrische Vorlagen zu identifizieren.
-   Geben Sie eine einzelne, von der Anwendung ausgewählte Vorlagen Datenbank frei.

Private Sensor Pools müssen verwendet werden, wenn die Client Anwendung Folgendes:

-   Verwaltet eine Auflistung dedizierter biometrischer Einheiten, die eine anwendungsspezifische Vorlagen Datenbank verwenden. Betrachten Sie beispielsweise eine Mitarbeiter Anwesenheits Anwendung, bei der Mitarbeiter ihre Ankunft bei der Arbeit signalisieren, indem Sie Ihren Finger auf einen Fingerabdruckleser wischen. Die Mitarbeiter haben keine Windows-Konten auf dem Computer, auf dem die Anwendung ausgeführt wird. Stattdessen werden ihre Fingerabdrücke von GUIDs identifiziert, die von der Anwesenheits Anwendung verwaltet werden.
-   Sammelt biometrische Beispiele anstelle der Zuordnung von Beispielen zu SIDs.
-   Versetzt die Hardware der biometrischen Einheit in den Wartungsmodus, um die Firmware zu aktualisieren.
-   Sendet Hersteller definierte Steuerungsbefehle an die Hardware oder Software für biometrische Geräte.
-   Versucht, eine biometrische Einheit mit dem integrierten Speicher zu konfigurieren, damit Sie im erweiterten Modus ausgeführt werden kann, die Einheit aber die erforderlichen Hash Vorgänge nicht ausführen kann.
-   Wird von einer Remotedesktop Client Sitzung ausgeführt.

> [!Note]  
> Anwendungen können private Sensor Pools nur für Fingerabdruck-Biometrie erstellen. Wenn eine Anwendung versucht, eine für etwas anderes zu erstellen (z. b. Gesicht), schlägt die Anforderung fehl.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines privaten Sensor Pools](creating-a-private-sensor-pool.md)
</dt> <dt>

[Sensor Pools](sensor-pools.md)
</dt> <dt>

[System Sensor Pool](system-sensor-pool.md)
</dt> </dl>

 

 




