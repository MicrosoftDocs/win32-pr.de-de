---
description: WoW64 ist jetzt ein optionales Feature für Server Core
ms.assetid: 9a918cd3-60a0-4231-975a-bee12de5c812
title: WoW64-Status in Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f836d361e172527bf23c7e51ea0071790d3857d6611d8a12ff62185226d3f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994470"
---
# <a name="wow64-is-now-an-optional-feature-for-server-core"></a>WoW64 ist jetzt ein optionales Feature für Server Core

## <a name="affected-platforms"></a>Betroffene Plattformen

**Server** – Windows Server 2008 R2  



## <a name="feature-impact"></a>Auswirkungen auf Features

 **Schweregrad –** Niedrig  
**Häufigkeit** : Niedrig  





## <a name="description"></a>Beschreibung

Mit der Server Core-Installationsoption für Windows Server 2008 R2 können Sie WoW64 deinstallieren. WoW64 ist jetzt ein optionales Feature, das Sie deinstallieren können, wenn es nicht erforderlich ist, 32-Bit-Code auszuführen.

Darüber hinaus benötigen die Active Directory- und Active Directory Lightweight Directory Services-Rollen WoW64, um in Windows Server 2008 R2 ausgeführt zu werden.

## <a name="manifestation-of-impact"></a>Auswirkungen

Wenn Sie WoW64 deinstallieren, erhalten Administratoren, die 32-Bit-Code auf Server Core ausführen, eine Fehlermeldung, dass die Anwendung nicht ausgeführt werden kann. Wenn Administratoren versuchen, Active Directory auszuführen und Active Directory Lightweight Directory Services, erhalten sie eine Fehlermeldung.

## <a name="mitigation"></a>Minderung

Installieren Sie WoW64.

## <a name="solution"></a>Lösung

Die bevorzugte Lösung besteht darin, eine 64-Bit-Version des Codes bereitzustellen, damit er auf Server Core ohne WoW64 ausgeführt werden kann.

Stellen Sie mindestens eine Benutzerdokumentation bereit, und beachten Sie, dass zum Ausführen von 32-Bit-Code WoW64 installiert werden muss.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Kompatibilitäts-, Leistungs-, Zuverlässigkeits- und Benutzerfreundlichkeitstests

Vergewissern Sie sich, dass der gesamte verwendete Code 64-Bit ist.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [WOW64-Implementierungsdetails](../winprog64/wow64-implementation-details.md)
-   [Debuggen von WOW64](../winprog64/debugging-wow64.md)
-   [Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))

 

 
