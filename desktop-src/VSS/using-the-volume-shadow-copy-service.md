---
description: VsS-Sicherungs- und -Wiederherstellungsvorgänge verwenden jeweils ein Protokoll für die Interaktion der Systeme, die Massenspeicher (Writer) verwenden, und der Systeme, die sie sichern (Anforderer).
ms.assetid: c4dae5ce-0dfa-46ec-909f-8ae79d50a9cb
title: Verwenden der Volumeschattenkopie-Dienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ad0f07cc20da83f9401ff5194776300c5aad23a950b2fbc7f14f787fe22f01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866250"
---
# <a name="using-the-volume-shadow-copy-service"></a>Verwenden der Volumeschattenkopie-Dienst

VsS-Sicherungs- und -Wiederherstellungsvorgänge verwenden jeweils ein Protokoll für die Interaktion der Systeme, die Massenspeicher (Writer) verwenden, und der Systeme, die sie sichern (Anforderer).

Sicherungs- und Wiederherstellungsvorgänge werden in erster Linie vom Anforderer gesteuert, der das Writer- und Anbieterverhalten steuert, indem systemweite COM-Ereignisse generiert werden, die der Writer verarbeiten soll. Da ereignisgenerierende Methoden asynchron sind, verfügen Writer über eingeschränkte Kontrolle über den Zustand des Anfordernden über die für VSS verfügbaren asynchronen Handler (siehe [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)).

Diese Interaktion erfordert grundlegende Datenstrukturen, die Dateien und Gruppen von Dateien [*(Komponenten)*](vssgloss-c.md)beschreiben, sowie ein Metadatenmodell, um die Speicherung von Sicherungsinformationen zu ermöglichen und die Kommunikation zwischen Writer und Anforderer zu ermöglichen.

-   [VSS-Anwendungskompatibilität](usage-conventions.md)
-   [Konfigurieren von VSS](configuring-vss.md)
-   [VSS-Metadaten](vss-metadata.md)
-   [Arbeiten mit Selektivität und logischen Pfaden](working-with-selectability-and-logical-paths.md)
-   [Übersicht über die Verarbeitung einer Sicherung unter VSS](overview-of-processing-a-backup-under-vss.md)
-   [Übersicht über die Verarbeitung einer Wiederherstellung unter VSS](overview-of-processing-a-restore-under-vss.md)

 

 



