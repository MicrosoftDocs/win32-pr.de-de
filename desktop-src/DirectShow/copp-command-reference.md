---
description: COPP-Befehlsreferenz
ms.assetid: b21db1cf-cac3-41d6-8189-6e01c8f91a7d
title: COPP-Befehlsreferenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50dfeebe42b877604ab880ef1855035242d6eca8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343952"
---
# <a name="copp-command-reference"></a>COPP-Befehlsreferenz

In diesem Abschnitt werden die Befehle des Certified Output Protection Protocol (COPP) beschrieben. Die folgenden Befehle sind definiert.



| Get-Help              | GUID                             |
|----------------------|----------------------------------|
| Schutz Ebene festlegen | **DXVA- \_ coppsetschutzlevel** |
| Signalisierung festlegen        | **DXVA- \_ coppsetsignalisierung**       |



 

Befehl zum Festlegen der Schutz Ebene

Legt die Schutz Ebene für einen angegebenen Ausgabe Schutzmechanismus fest. Abhängig vom Connector ist es möglicherweise möglich, mehr als einen Schutzmechanismus auf demselben Connector mit unterschiedlichen Einstellungen für jeden Mechanismus anzuwenden.

**GUID**: DXVA- \_ coppsetschutzlevel

**Eingabedaten**: eine [**DXVA-Struktur " \_ coppsetschutzlevelcmddata**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetprotectionlevelcmddata) ".

Signalisierungs Befehl festlegen

Gibt Informationen zum anderen Videosignal als der Schutz Ebene an.

Für CGMS-A erfordern bestimmte Schutzstandards, dass das Televsion-Signalinformationen über das Seitenverhältnis und andere Informationen in denselben VBI-Wellenform-Paketen wie die CGMS-a-Bits enthält. Fernsehgeräte können schlecht angezeigt werden, wenn die Seitenverhältnis Informationen nicht mit dem Videostream konsistent sind. Die Anwendung kann diesen Befehl verwenden, um das Seitenverhältnis anzugeben, damit der Grafiktreiber die richtigen VBI-Pakete generieren kann.

Dieser Befehl ist auch erweiterbar, wenn in zukünftigen Standards zusätzliche Signalinformationen erforderlich sind.

**GUID**: DXVA- \_ coppsetsignalisierung

**Eingabedaten**: eine [**DXVA-Struktur " \_ coppsetsignalingcmddata**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetsignalingcmddata) ".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Certified Output Protection-Protokolls (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



