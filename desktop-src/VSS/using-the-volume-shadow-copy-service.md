---
description: Bei VSS-Sicherungs-und-Wiederherstellungs Vorgängen wird jeweils ein Protokoll für die Interaktion der Systeme verwendet, die Massenspeicher (Writer) verwenden, und diejenigen, die Sie sichern (Requester).
ms.assetid: c4dae5ce-0dfa-46ec-909f-8ae79d50a9cb
title: Verwenden des Volumeschattenkopie-Dienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06a1c81d79de30085f783feb02b7a7d47d5dc765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526303"
---
# <a name="using-the-volume-shadow-copy-service"></a>Verwenden des Volumeschattenkopie-Dienst

Bei VSS-Sicherungs-und-Wiederherstellungs Vorgängen wird jeweils ein Protokoll für die Interaktion der Systeme verwendet, die Massenspeicher (Writer) verwenden, und diejenigen, die Sie sichern (Requester).

Sowohl Sicherungs-als auch Wiederherstellungs Vorgänge werden hauptsächlich von der anfordernden Person gesteuert, die das Verhalten von Writer und Anbietern steuert, indem systemweite com-Ereignisse für den Writer erzeugt werden. Da Ereignis generierende Methoden asynchron sind, haben Writer eine eingeschränkte Kontrolle über den Zustand des Anforderers über die für VSS verfügbaren asynchronen Handler (siehe [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)).

Diese Interaktion erfordert grundlegende Datenstrukturen, die Dateien und Gruppen von Dateien ([*Komponenten*](vssgloss-c.md)) beschreiben, sowie ein Metadatenmodell, um die Speicherung von Sicherungs Informationen und die Kommunikation zwischen Writer und Anforderer zuzulassen.

-   [VSS-Anwendungskompatibilität](usage-conventions.md)
-   [Konfigurieren von VSS](configuring-vss.md)
-   [VSS-Metadaten](vss-metadata.md)
-   [Arbeiten mit selekabilität und logischen Pfaden](working-with-selectability-and-logical-paths.md)
-   [Übersicht über die Verarbeitung einer Sicherung unter VSS](overview-of-processing-a-backup-under-vss.md)
-   [Übersicht über die Verarbeitung einer Wiederherstellung unter VSS](overview-of-processing-a-restore-under-vss.md)

 

 



