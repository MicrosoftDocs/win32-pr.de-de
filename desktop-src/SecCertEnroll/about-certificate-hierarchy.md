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
# <a name="certificate-hierarchy"></a><span data-ttu-id="a305d-103">Zertifikat Hierarchie</span><span class="sxs-lookup"><span data-stu-id="a305d-103">Certificate Hierarchy</span></span>

<span data-ttu-id="a305d-104">Wenn sich die Anzahl der ausgestellten Zertifikate in einer Public Key-Infrastruktur (PKI) erhöht, kann es für eine einzelne Zertifizierungsstelle (ca) schwierig werden, die ausgestellten Zertifikate effektiv nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="a305d-104">As the number of issued certificates in a public key infrastructure (PKI) increases, it can become difficult for a single certification authority (CA) to effectively track the certificates it has issued.</span></span> <span data-ttu-id="a305d-105">Eine Möglichkeit, dieses Problem zu beheben, besteht darin, eine Zertifikat Hierarchie zu erstellen, in der die Zertifizierungsstelle die Zertifizierungsstelle anweist, Zertifikate für untergeordnete Autoritäten auszustellen, die wiederum die Autorität an ihre untergeordneten Elemente delegieren können.</span><span class="sxs-lookup"><span data-stu-id="a305d-105">One way to address this is to create a certificate hierarchy in which the CA delegates the authority to issue certificates to subordinate authorities which can, in turn, delegate authority to their subordinates.</span></span> <span data-ttu-id="a305d-106">Jede Zertifizierungsstelle delegiert die Zertifizierungsstelle, indem Sie ein Zertifizierungsstellen Zertifikat an einen untergeordneten-</span><span class="sxs-lookup"><span data-stu-id="a305d-106">Each CA delegates authority by issuing a CA certificate to a subordinate.</span></span> <span data-ttu-id="a305d-107">Die erste Zertifizierungsstelle in der Kette wird als Stamm bezeichnet, und es ist nicht erforderlich, dass eine Entität eine Vertrauensstellung mit einer Zertifizierungsstelle einrichtet, die sich in einer anderen [Zertifikat Kette](about-certificate-chain.md) befindet, in der sich die Entität befindet.</span><span class="sxs-lookup"><span data-stu-id="a305d-107">The initial CA in the chain is called the root, and it is not necessary for an entity to establish trust with any CA that resides on a different [Certificate Chain](about-certificate-chain.md) from that on which the entity resides.</span></span>

<span data-ttu-id="a305d-108">Die folgende Abbildung zeigt eine Zertifikat Hierarchie, die aus einer Stamm Zertifizierungsstelle besteht, zwei Zertifizierungsstellen, die der Stamm Zertifizierungsstelle untergeordnet sind (eine für die Marketingabteilung und eine für die Fertigungsabteilung), und Zertifizierungsstellen, die diesen untergeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a305d-108">The following illustration shows a certificate hierarchy made up of one root CA, two CAs subordinate to the root (one for the marketing department and one for the manufacturing department), and CAs that are subordinate to these.</span></span>

![Zertifikat Hierarchie Diagramm](images/certificate-hierarchy.png)

## <a name="related-topics"></a><span data-ttu-id="a305d-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a305d-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a305d-111">Trust-Modelle</span><span class="sxs-lookup"><span data-stu-id="a305d-111">Trust Models</span></span>](about-trust-models.md)
</dt> </dl>

 

 



