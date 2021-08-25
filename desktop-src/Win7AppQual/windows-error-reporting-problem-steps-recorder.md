---
description: Windows-Fehlerberichterstattung Problemaufzeichnung
ms.assetid: ce5db84a-53b6-4a7f-bee4-d198d8a6781e
title: Windows-Fehlerberichterstattung Problemaufzeichnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba90b76b3d486dc0708e0803609539fda6d6141d0a6f3ab100ba0ce198846fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118328082"
---
# <a name="windows-error-reporting-problem-steps-recorder"></a>Windows-Fehlerberichterstattung Problemaufzeichnung

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** – Windows 7  
**Server** – Windows Server 2008 R2  


## <a name="description"></a>Beschreibung

Vor Windows 7 sammelte Windows-Fehlerberichterstattung (WER) Fehlerberichte, die auf Probleme hindeuteten, die repariert werden mussten. Diese Fehlerberichte enthalten hilfreiche Informationen, die die allgemeine Natur eines Problems beschreiben, aber nicht genügend Informationen, um die Grundursache zu ermitteln. Dazu benötigen Entwickler ein Tool, um das Absturz-/Hängen-Szenario für das Debuggen zu reproduzieren.

Eine neue Anwendung, Problemaufzeichnung (PSR.exe), wird in allen Builds von Windows 7 ausgeliefert. Dieses Feature ermöglicht die Sammlung der Aktionen, die von einem Benutzer ausgeführt werden, während ein Absturz auftritt, sodass Tester und Entwickler die Situation für Analyse und Debuggen reproduzieren können.

## <a name="usage"></a>Verbrauch

Derzeit muss ein Windows-Fehlerberichterstattung-Dienstentwickler die PSR-Aktivierung für eine Anwendung anfordern. Microsoft-Supportorganisationen verwenden dieses Tool auch bei der Problembehandlung bei Endbenutzern. Es gibt Pläne, PSR nach der Veröffentlichung von Windows 7 unter Windows Quality Online Services (Winqual) verfügbar zu machen.

**Hinweis:** Wenn PSR für eine Anwendung aktiviert ist, kann die Leistung der Anwendung beeinträchtigt werden.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Windows-Fehlerberichterstattung Blogeintrag](/archive/blogs/wer/)
-   [Windows Quality Online Services (Winqual)](https://winqual.microsoft.com)

 

 
