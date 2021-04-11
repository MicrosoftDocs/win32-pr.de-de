---
title: Informationen zu TSB
description: Ein-Systemdienst, der die transparente Freigabe der Trusted Platform Module (TPM)-Ressourcen ermöglicht.
ms.assetid: 5ab3f514-dea9-48f7-97d9-abc774e2a273
keywords:
- TPM-Basisdienste-TSB, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a5d40b1fca688676978f274cb976afedb6e6a56
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104208729"
---
# <a name="about-tbs"></a>Informationen zu TSB

Das TPM-Basis Dienst Feature (TSB) ist ein Systemdienst, der die transparente Freigabe der Trusted Platform Module (TPM)-Ressourcen ermöglicht. Die TPM-Ressourcen werden gleichzeitig auf mehrere Anwendungen auf demselben physischen Computer verteilt, auch wenn diese Anwendungen auf unterschiedlichen virtuellen Computern ausgeführt werden. Ab Windows 8 und Windows Server 2012 ist TSB auf allen Systemen mit einem TPM vorinstalliert.

Der Trusted Computing Group (TCG) definiert eine Trusted Platform Module, die Kryptografiefunktionen bereitstellt, die für die Bereitstellung von Vertrauen in der Plattform konzipiert sind Da das TPM in der Hardware implementiert ist, verfügt es über begrenzte Ressourcen. Das TCG definiert auch einen Software Stapel, der diese Ressourcen verwendet, um vertrauenswürdige Vorgänge für Anwendungssoftware bereitzustellen. Es wird jedoch keine Bereitstellung für die parallele Ausführung einer TSS-Implementierung mit Betriebssystem Software vorgenommen, die möglicherweise auch TPM-Ressourcen verwendet. Das TSB-Feature löst dieses Problem, indem jeder Software Stapel, der mit TSB kommuniziert, die Überprüfung von TPM-Ressourcen für andere Software Stapel verwendet, die möglicherweise auf dem Computer ausgeführt werden.

Die TPM-Spezifikation und die TSS-Spezifikation (TCG Software Stack) finden Sie unter [https://www.trustedcomputinggroup.org](https://www.trustedcomputinggroup.org/) .

TSB wird als Prozess interner Dienst implementiert, der Befehle annimmt, die einen RPC-Dienst verwenden. Eine dynamisch verknüpfte Bibliothek stellt die Programmiersprache C dar und kommuniziert mit dem TSB-Dienst.

> [!Note]  
> Der TSB-Dienst akzeptiert nur RPC-Anforderungen vom lokalen Computer.

 

Die wichtigsten Ziele der TSB lauten:

-   Bieten Sie eine effiziente Freigabe von eingeschränkten TPM-Ressourcen, z. b. Schlüssel Slots, Slots von Autorisierungs Sitzungen und Transport Slots.
-   Stellen Sie einen priorisierten und synchronisierten Zugriff auf TPM-Ressourcen zwischen mehreren Instanzen von TPM-Software Stapeln bereit.
-   Sorgen Sie für eine angemessene Verwaltung von TPM-Ressourcen in den Energiezuständen.
-   Verhindern Sie, dass TPM-Software Stapel auf TPM-Befehle zugreifen, die aufgrund von Platt Form Einschränkungen oder administrativen Anforderungen eingeschränkt werden sollten.

Die folgende Abbildung zeigt die Beziehung zwischen den TSB und dem TPM.

![Beziehung der TSB im Benutzermodus mit dem TPM im Kernel Modus](images/tbs-block-diagram-as11601.png)

 

 




