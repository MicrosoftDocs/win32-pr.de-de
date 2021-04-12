---
description: Die Kreuz Zertifizierung ermöglicht Entitäten in einer Public Key-Infrastruktur (PKI), Entitäten in einer anderen PKI zu vertrauen.
ms.assetid: 93cdb10d-4b77-4511-8c5b-c27b290f9154
title: Kreuz Zertifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b18fcb8317145b7239464893391c5d2231ab1cb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217160"
---
# <a name="cross-certification"></a>Kreuz Zertifizierung

Die Kreuz Zertifizierung ermöglicht Entitäten in einer Public Key-Infrastruktur (PKI), Entitäten in einer anderen PKI zu vertrauen. Diese Beziehung zwischen der gegenseitigen Vertrauensstellung wird in der Regel von einem übergreifenden Zertifizierungs Vertrag zwischen den Zertifizierungsstellen (CAS) in jeder PKI unterstützt. Mit der Vereinbarung werden die Zuständigkeiten und die Haftung der einzelnen Parteien festgelegt.

Eine gegenseitige Vertrauensstellung zwischen zwei ZS erfordert, dass jede Zertifizierungsstelle ein Zertifikat für das andere ausgibt, um die Beziehung in beide Richtungen herzustellen. Der Pfad der Vertrauensstellung ist nicht hierarchische (keine der leitenden Zertifizierungsstellen ist der anderen Zertifizierungsstelle untergeordnet), obwohl es sich bei den separaten PKIs um Zertifikat Hierarchien handeln kann. Nachdem zwei Zertifizierungsstellen die Vertrauens Bedingungen und die ausgestellten Zertifikate festgelegt haben, können die Entitäten innerhalb der separaten PKIs mit den in den Zertifikaten angegebenen Richtlinien interagieren.

![Kreuz Zertifizierungs Diagramm](images/cross-certification.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Trust-Modelle](about-trust-models.md)
</dt> </dl>

 

 



