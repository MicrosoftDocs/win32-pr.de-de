---
title: Informationen zu TBS
description: Ein Systemdienst, der die transparente Freigabe der Trusted Platform Module (TPM) ermöglicht.
ms.assetid: 5ab3f514-dea9-48f7-97d9-abc774e2a273
keywords:
- TPM Base Services TBS , Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4997bf6181a1da7aabaf811d0f1d0cf3e3ca813bb11a8f2d73b3b286e4e5ebde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117954452"
---
# <a name="about-tbs"></a>Informationen zu TBS

Das FEATURE TPM-Basisdienste (TPM Base Services, TBS) ist ein Systemdienst, der die transparente Freigabe der Trusted Platform Module (TPM) ermöglicht. Sie teilt gleichzeitig die TPM-Ressourcen für mehrere Anwendungen auf demselben physischen Computer, auch wenn diese Anwendungen auf verschiedenen virtuellen Computern ausgeführt werden. Ab Windows 8 und Windows Server 2012 ist TBS auf allen Systemen mit einem TPM vorinstalliert.

Die Trusted Computing Group (TCG) definiert eine Trusted Platform Module, die kryptografische Funktionen zur Bereitstellung von Vertrauen in die Plattform bietet. Da das TPM in Hardware implementiert ist, verfügt es über endliche Ressourcen. Das TCG definiert auch einen Softwarestapel, der diese Ressourcen verwendet, um vertrauenswürdige Vorgänge für Anwendungssoftware zu ermöglichen. Es wird jedoch keine bereitstellungsbasierte Ausführung einer TSS-Implementierung zusammen mit Betriebssystemsoftware bereitgestellt, die möglicherweise auch TPM-Ressourcen verwendet. Das TBS-Feature löst dieses Problem, indem es jedem Softwarestapel, der mit TBS kommuniziert, die Verwendung von TPM-Ressourcen ermöglicht, um nach anderen Softwarestapeln zu prüfen, die möglicherweise auf dem Computer ausgeführt werden.

Die TPM-Spezifikation und die TCG-Softwarestapelspezifikation (TSS) sind unter [https://www.trustedcomputinggroup.org](https://www.trustedcomputinggroup.org/) verfügbar.

TBS wird als Out-of-Process-Dienst implementiert, der Befehle akzeptiert, die einen RPC-Dienst verwenden. Eine dynamisch verknüpfte Bibliothek stellt die C-Sprachschnittstelle bereit und kommuniziert mit dem TBS-Dienst.

> [!Note]  
> Der TBS-Dienst akzeptiert nur RPC-Anforderungen vom lokalen Computer.

 

Die Hauptziele der TBS sind:

-   Stellen Sie eine effiziente Freigabe eingeschränkter TPM-Ressourcen wie Schlüsselslots, Autorisierungssitzungsslots und Transportslots zur Verfügung.
-   Stellen Sie priorisierten und synchronisierten Zugriff auf TPM-Ressourcen zwischen mehreren Instanzen von TPM-Softwarestapeln zur Verfügung.
-   Stellen Sie eine geeignete Verwaltung von TPM-Ressourcen über Energiezustände hinweg zur Verfügung.
-   Verhindern Sie, dass TPM-Softwarestapel auf TPM-Befehle zugreifen, die entweder aufgrund von Plattformeinschränkungen oder administrativen Anforderungen eingeschränkt werden sollten.

Die folgende Abbildung zeigt die Beziehung zwischen TBS und TPM.

![Beziehung der TBs im Benutzermodus zum TPM im Kernelmodus](images/tbs-block-diagram-as11601.png)

 

 




