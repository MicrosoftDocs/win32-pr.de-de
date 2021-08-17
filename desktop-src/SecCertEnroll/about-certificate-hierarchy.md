---
description: Wenn die Anzahl ausgestellter Zertifikate in einer Public Key-Infrastruktur (PKI) zunimmt, kann es für eine einzelne Zertifizierungsstelle schwierig werden, die ausgestellten Zertifikate effektiv nachverfolgung zu können.
ms.assetid: f1642c1c-d2cd-4fa4-8a26-cebf3d6dcf23
title: Zertifikathierarchie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abc3420e3f0f09f88b4b9e7157ec8abacc9516520de4472a48189520e3e0e567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904975"
---
# <a name="certificate-hierarchy"></a>Zertifikathierarchie

Wenn die Anzahl ausgestellter Zertifikate in einer Public Key-Infrastruktur (PKI) zunimmt, kann es für eine einzelne Zertifizierungsstelle schwierig werden, die ausgestellten Zertifikate effektiv nachverfolgung zu können. Eine Möglichkeit, dies zu beheben, besteht in der Erstellung einer Zertifikathierarchie, in der die Zertifizierungsstelle die Autorität zum Ausstellen von Zertifikaten an untergeordnete Autoritäten delegiert, die wiederum die Autorität an ihre Untergeordneten delegieren können. Jede Zertifizierungsstelle delegiert die Autorität, indem sie ein Zertifizierungsstellenzertifikat an einen untergeordneten Mitarbeiter ausstellen. Die anfängliche Zertifizierungsstelle in der Kette wird als Stamm bezeichnet, und es ist nicht erforderlich, dass eine Entität eine Vertrauensstellung mit einer Zertifizierungsstelle aufbaut, die sich in einer anderen Zertifikatkette befindet als die, in der sich die Entität befindet. [](about-certificate-chain.md)

Die folgende Abbildung zeigt eine Zertifikathierarchie aus einer Stammzertifizierungsstelle, zwei Zertifizierungsstellen, die dem Stamm untergeordnet sind (eine für die Marketingabteilung und eine für die Fertigungsabteilung) und Zertifizierungsstellen, die diesen untergeordnet sind.

![Diagramm der Zertifikathierarchie](images/certificate-hierarchy.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertrauensmodelle](about-trust-models.md)
</dt> </dl>

 

 



