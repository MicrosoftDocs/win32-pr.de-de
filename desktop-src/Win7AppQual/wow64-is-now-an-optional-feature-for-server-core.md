---
description: WoW64 ist jetzt ein optionales Feature für Server Core
ms.assetid: 9a918cd3-60a0-4231-975a-bee12de5c812
title: WoW64-Status in Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fad947dac85707d3c9c89a2cffea38c4a4850a6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084048"
---
# <a name="wow64-is-now-an-optional-feature-for-server-core"></a>WoW64 ist jetzt ein optionales Feature für Server Core

## <a name="affected-platforms"></a>Betroffene Plattformen

**Server** – Windows Server 2008 R2  



## <a name="feature-impact"></a>Auswirkung von Features

 **Schweregrad:** Niedrig  
**Häufigkeit** – Niedrig  





## <a name="description"></a>BESCHREIBUNG

Mit der Server Core-Installationsoption für Windows Server 2008 R2 können Sie WoW64 deinstallieren. WoW64 ist jetzt ein optionales Feature, das Sie deinstallieren können, wenn 32-Bit-Code nicht ausgeführt werden muss.

Darüber hinaus erfordern die Rollen Active Directory und Active Directory Lightweight Directory Services WoW64, um in Windows Server 2008 R2 ausgeführt zu werden.

## <a name="manifestation-of-impact"></a>Auswirkungen

Wenn Sie WoW64 deinstallieren, erhalten Administratoren, die 32-Bit-Code auf Server Core ausführen, eine Fehlermeldung, dass die Anwendung nicht ausgeführt werden kann. Wenn Administratoren versuchen, Active Directory und Active Directory Lightweight Directory Services ausführen, erhalten sie eine Fehlermeldung.

## <a name="mitigation"></a>Minderung

Installieren Sie WoW64.

## <a name="solution"></a>Lösung

Die bevorzugte Lösung besteht in der Bereitstellung einer 64-Bit-Version des Codes, um die Ausführung auf Server Core ohne WoW64 zu ermöglichen.

Stellen Sie zumindest eine Benutzerdokumentation zur Verfügung, in der Sie darauf hindechen, dass Zum Ausführen von 32-Bit-Code WoW64 installiert werden muss.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Kompatibilitäts-, Leistungs-, Zuverlässigkeits- und Nutzbarkeitstests

Stellen Sie sicher, dass der verwendete Code 64-Bit ist.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [WOW64-Implementierungsdetails](../winprog64/wow64-implementation-details.md)
-   [Debuggen von WOW64](../winprog64/debugging-wow64.md)
-   [Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))

 

 
