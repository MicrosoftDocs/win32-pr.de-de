---
description: Windows-Fehlerberichterstattung Problemaufzeichnung
ms.assetid: ce5db84a-53b6-4a7f-bee4-d198d8a6781e
title: Windows-Fehlerberichterstattung Problemaufzeichnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46abb8adf545152e34c2b2100022068291e3571f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084158"
---
# <a name="windows-error-reporting-problem-steps-recorder"></a>Windows-Fehlerberichterstattung Problemaufzeichnung

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** – Windows 7  
**Server** – Windows Server 2008 R2  


## <a name="description"></a>BESCHREIBUNG

Vor Windows 7 hat Windows-Fehlerberichterstattung (WER) Fehlerberichte gesammelt, die auf Reparaturprobleme hindeuteten. Diese Fehlerberichte enthalten hilfreiche Informationen, die die allgemeine Natur eines Problems beschreiben, aber nicht genügend Informationen, um die Grundursache zu bestimmen. Dafür benötigen Entwickler ein Tool, um das Absturz-/Hängen-Szenario für das Debuggen zu reproduzieren.

Eine neue Anwendung, Problemaufzeichnung (PSR.exe), wird für alle Builds von Windows 7 veröffentlicht. Dieses Feature ermöglicht das Sammeln der Aktionen, die von einem Benutzer bei einem Absturz ausgeführt werden, damit Tester und Entwickler die Situation für Analyse und Debuggen reproduzieren können.

## <a name="usage"></a>Verbrauch

Derzeit muss ein Windows-Fehlerberichterstattung-Dienstentwickler die PSR-Aktivierung für eine Anwendung anfordern. Microsoft-Supportorganisationen verwenden dieses Tool auch bei der Problembehandlung mit Endbenutzern. Es sind Pläne vorhanden, um PSR nach der Veröffentlichung von Windows 7 unter Windows Quality Online Services (Winqual) verfügbar zu machen.

**Hinweis:** Wenn PSR für eine Anwendung aktiviert ist, kann es für die Anwendung zu Leistungseinbußen führen.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Windows-Fehlerberichterstattung Blogeintrag](/archive/blogs/wer/)
-   [Windows Quality Online Services (Winqual)](https://winqual.microsoft.com)

 

 
