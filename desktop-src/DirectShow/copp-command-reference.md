---
description: COPP-Befehlsreferenz
ms.assetid: b21db1cf-cac3-41d6-8189-6e01c8f91a7d
title: COPP-Befehlsreferenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1a706863464b6f303e05cb88e28a075dffbfba7b6bf54f8289a2699e66a76f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565970"
---
# <a name="copp-command-reference"></a>COPP-Befehlsreferenz

In diesem Abschnitt werden die COPP-Befehle (Certified Output Protection Protocol) beschrieben. Die folgenden Befehle sind definiert.



| Befehl              | GUID                             |
|----------------------|----------------------------------|
| Festlegen der Schutzebene | **DXVA \_ COPPSetProtectionLevel** |
| Festlegen der Signalisierung        | **DXVA \_ COPPSetSignaling**       |



 

Befehl "Schutzebene festlegen"

Legt die Schutzebene für einen angegebenen Ausgabeschutzmechanismus fest. Je nach Connector kann es möglich sein, mehrere Schutzmechanismen für denselben Connector mit unterschiedlichen Einstellungen für jeden Mechanismus anzuwenden.

**GUID:** DXVA \_ COPPSetProtectionLevel

**Eingabedaten:** Eine [**\_ DXVA-COPPSetProtectionLevelCmdData-Struktur.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetprotectionlevelcmddata)

Befehl "Signalisierung festlegen"

Gibt Informationen über das Videosignal an, das nicht die Schutzebene ist.

Für CGMS-A erfordern bestimmte Schutzstandards, dass das Televsionssignal Informationen über das Seitenverhältnis und andere Informationen innerhalb der gleichen VBI-Wellenformpakete wie die CGMS-A-Bits enthält. Fernsehgeräte werden möglicherweise schlecht angezeigt, wenn die Informationen zum Seitenverhältnis nicht mit dem Videostream konsistent sind. Die Anwendung kann diesen Befehl verwenden, um das Seitenverhältnis anzugeben, damit der Grafiktreiber die richtigen VBI-Pakete generieren kann.

Dieser Befehl ist auch erweiterbar, wenn in zukünftigen Standards zusätzliche Signalinformationen erforderlich sind.

**GUID:** DXVA \_ COPPSetSignaling

**Eingabedaten:** Eine [**\_ DXVA-COPPSetSignalingCmdData-Struktur.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetsignalingcmddata)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Certified Output Protection Protocol (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



