---
description: .
ms.assetid: 9a918cd3-60a0-4231-975a-bee12de5c812
title: WOW64-Status in Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a121c6bb9c4fb2cd052825bb4c2d5e3dbd0183c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366282"
---
# <a name="wow64-is-now-an-optional-feature-for-server-core"></a>WOW64 ist jetzt ein optionales Feature für Server Core.

## <a name="affected-platforms"></a>Betroffene Plattformen

**Server** -Windows Server 2008 R2  



## <a name="feature-impact"></a>Auswirkungen von Features

 **Schweregrad** -niedrig  
**Häufigkeit** -niedrig  





## <a name="description"></a>BESCHREIBUNG

Mit der Server Core-Installationsoption für Windows Server 2008 R2 können Sie WOW64 deinstallieren. WOW64 ist jetzt ein optionales Feature, das Sie deinstallieren können, wenn es nicht erforderlich ist, 32-Bit-Code auszuführen.

Außerdem ist für die Active Directory-und Active Directory Lightweight Directory Services Rollen WOW64 erforderlich, um unter Windows Server 2008 R2 ausgeführt werden zu können.

## <a name="manifestation-of-impact"></a>Erscheinung der Auswirkung

Wenn Sie WOW64 deinstallieren, erhalten Administratoren, die 32-Bit-Code auf Server Core ausführen, eine Fehlermeldung, dass die Anwendung nicht ausgeführt werden kann. Wenn Administratoren versuchen, Active Directory und Active Directory Lightweight Directory Services auszuführen, erhalten Sie eine Fehlermeldung.

## <a name="mitigation"></a>Minderung

Installieren Sie WOW64.

## <a name="solution"></a>Lösung

Die bevorzugte Lösung besteht darin, eine 64-Bit-Version des Codes bereitzustellen, damit Sie auf Server Core ausgeführt werden kann, ohne dass WOW64 erforderlich ist.

Geben Sie mindestens eine Benutzerdokumentation an, die darauf hinweist, dass zum Ausführen von 32-Bit-Code WOW64 installiert werden muss.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Tests der Kompatibilität, Leistung, Zuverlässigkeit und Benutzerfreundlichkeit

Vergewissern Sie sich, dass der gesamte verwendete Code 64-Bit ist.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [WOW64-Implementierungs Details](../winprog64/wow64-implementation-details.md)
-   [Debuggen WOW64](../winprog64/debugging-wow64.md)
-   [Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))

 

 
