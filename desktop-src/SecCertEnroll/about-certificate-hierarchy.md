---
description: Wenn sich die Anzahl der ausgestellten Zertifikate in einer Public Key-Infrastruktur (PKI) erhöht, kann es für eine einzelne Zertifizierungsstelle (ca) schwierig werden, die ausgestellten Zertifikate effektiv nachzuverfolgen.
ms.assetid: f1642c1c-d2cd-4fa4-8a26-cebf3d6dcf23
title: Zertifikat Hierarchie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05c4ed9a69ff96ec0904e658444d6a32b65ed82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566635"
---
# <a name="certificate-hierarchy"></a>Zertifikat Hierarchie

Wenn sich die Anzahl der ausgestellten Zertifikate in einer Public Key-Infrastruktur (PKI) erhöht, kann es für eine einzelne Zertifizierungsstelle (ca) schwierig werden, die ausgestellten Zertifikate effektiv nachzuverfolgen. Eine Möglichkeit, dieses Problem zu beheben, besteht darin, eine Zertifikat Hierarchie zu erstellen, in der die Zertifizierungsstelle die Zertifizierungsstelle anweist, Zertifikate für untergeordnete Autoritäten auszustellen, die wiederum die Autorität an ihre untergeordneten Elemente delegieren können. Jede Zertifizierungsstelle delegiert die Zertifizierungsstelle, indem Sie ein Zertifizierungsstellen Zertifikat an einen untergeordneten- Die erste Zertifizierungsstelle in der Kette wird als Stamm bezeichnet, und es ist nicht erforderlich, dass eine Entität eine Vertrauensstellung mit einer Zertifizierungsstelle einrichtet, die sich in einer anderen [Zertifikat Kette](about-certificate-chain.md) befindet, in der sich die Entität befindet.

Die folgende Abbildung zeigt eine Zertifikat Hierarchie, die aus einer Stamm Zertifizierungsstelle besteht, zwei Zertifizierungsstellen, die der Stamm Zertifizierungsstelle untergeordnet sind (eine für die Marketingabteilung und eine für die Fertigungsabteilung), und Zertifizierungsstellen, die diesen untergeordnet sind.

![Zertifikat Hierarchie Diagramm](images/certificate-hierarchy.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Trust-Modelle](about-trust-models.md)
</dt> </dl>

 

 



