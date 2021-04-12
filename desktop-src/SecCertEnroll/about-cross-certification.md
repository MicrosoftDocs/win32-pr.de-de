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
# <a name="cross-certification"></a><span data-ttu-id="3b725-103">Kreuz Zertifizierung</span><span class="sxs-lookup"><span data-stu-id="3b725-103">Cross Certification</span></span>

<span data-ttu-id="3b725-104">Die Kreuz Zertifizierung ermöglicht Entitäten in einer Public Key-Infrastruktur (PKI), Entitäten in einer anderen PKI zu vertrauen.</span><span class="sxs-lookup"><span data-stu-id="3b725-104">Cross certification enables entities in one public key infrastructure (PKI) to trust entities in another PKI.</span></span> <span data-ttu-id="3b725-105">Diese Beziehung zwischen der gegenseitigen Vertrauensstellung wird in der Regel von einem übergreifenden Zertifizierungs Vertrag zwischen den Zertifizierungsstellen (CAS) in jeder PKI unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3b725-105">This mutual trust relationship is typically supported by a cross-certification agreement between the certification authorities (CAs) in each PKI.</span></span> <span data-ttu-id="3b725-106">Mit der Vereinbarung werden die Zuständigkeiten und die Haftung der einzelnen Parteien festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3b725-106">The agreement establishes the responsibilities and liability of each party.</span></span>

<span data-ttu-id="3b725-107">Eine gegenseitige Vertrauensstellung zwischen zwei ZS erfordert, dass jede Zertifizierungsstelle ein Zertifikat für das andere ausgibt, um die Beziehung in beide Richtungen herzustellen.</span><span class="sxs-lookup"><span data-stu-id="3b725-107">A mutual trust relationship between two CAs requires that each CA issue a certificate to the other to establish the relationship in both directions.</span></span> <span data-ttu-id="3b725-108">Der Pfad der Vertrauensstellung ist nicht hierarchische (keine der leitenden Zertifizierungsstellen ist der anderen Zertifizierungsstelle untergeordnet), obwohl es sich bei den separaten PKIs um Zertifikat Hierarchien handeln kann.</span><span class="sxs-lookup"><span data-stu-id="3b725-108">The path of trust is not hierarchal (neither of the governing CAs is subordinate to the other) although the separate PKIs may be certificate hierarchies.</span></span> <span data-ttu-id="3b725-109">Nachdem zwei Zertifizierungsstellen die Vertrauens Bedingungen und die ausgestellten Zertifikate festgelegt haben, können die Entitäten innerhalb der separaten PKIs mit den in den Zertifikaten angegebenen Richtlinien interagieren.</span><span class="sxs-lookup"><span data-stu-id="3b725-109">After two CAs have established and specified the terms of trust and issued certificates to each other, entities within the separate PKIs can interact subject to the policies specified in the certificates.</span></span>

![Kreuz Zertifizierungs Diagramm](images/cross-certification.png)

## <a name="related-topics"></a><span data-ttu-id="3b725-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3b725-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b725-112">Trust-Modelle</span><span class="sxs-lookup"><span data-stu-id="3b725-112">Trust Models</span></span>](about-trust-models.md)
</dt> </dl>

 

 



