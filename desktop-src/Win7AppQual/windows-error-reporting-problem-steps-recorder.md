---
description: .
ms.assetid: ce5db84a-53b6-4a7f-bee4-d198d8a6781e
title: Windows-Fehlerberichterstattung Problem Aufzeichnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25fb70acef867b878063bd6011fde6867f7f0e75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759786"
---
# <a name="windows-error-reporting-problem-steps-recorder"></a>Windows-Fehlerberichterstattung Problem Aufzeichnung

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** – Windows 7  
**Server** – Windows Server 2008 R2  


## <a name="description"></a>BESCHREIBUNG

Vor Windows 7 wurden von Windows-Fehlerberichterstattung (wer) Fehlerberichte erfasst, die auf Probleme bei der Reparatur hinweisen. Diese Fehlerberichte enthalten hilfreiche Informationen, die die allgemeine Art eines Problems beschreiben, jedoch nicht genügend Informationen, um die Grundursache zu ermitteln. Dafür benötigen Entwickler ein Tool, um das Absturz-/stillstandzenario für das Debuggen zu reproduzieren.

Eine neue Anwendung, Problem Schritte Recorder (PSR.exe), wird auf allen Builds von Windows 7 ausgeliefert. Diese Funktion ermöglicht das Sammeln von Aktionen, die von einem Benutzer ausgeführt werden, während ein Absturz auftritt, sodass Tester und Entwickler die Situation für Analyse und Debuggen reproduzieren können.

## <a name="usage"></a>Verbrauch

Derzeit muss ein Windows-Fehlerberichterstattung Service-Entwickler PSR-Aktivierung für eine Anwendung anfordern. Microsoft-Support Organisationen verwenden dieses Tool auch bei der Problembehandlung mit Endbenutzern. Pläne sind vorhanden, um PSR nach der Veröffentlichung von Windows 7 unter Windows Quality Online Services (Winqual) verfügbar zu machen.

**Hinweis:** Wenn PSR für eine Anwendung aktiviert ist, kann es bei der Anwendung zu Leistungseinbußen kommen.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Blogeintrag Windows-Fehlerberichterstattung](/archive/blogs/wer/)
-   [Windows Quality Online Services (Winqual)](https://winqual.microsoft.com)

 

 
