---
description: Eine Zertifikat Kette ist eine hierarchische Sammlung von Zertifikaten, die vom Endbenutzer oder Computer zurück zu einer Vertrauensstellung führt, in der Regel die Stamm Zertifizierungsstelle (Certification Authority, ca) einer Organisation.
ms.assetid: 53701ede-269c-4949-b839-3f2b64cb5510
title: Zertifikatkette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e7509adb164c98cf07912af00af0d91c27ab8df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363001"
---
# <a name="certificate-chain"></a><span data-ttu-id="082f2-103">Zertifikatkette</span><span class="sxs-lookup"><span data-stu-id="082f2-103">Certificate Chain</span></span>

<span data-ttu-id="082f2-104">Eine Zertifikat Kette ist eine hierarchische Sammlung von Zertifikaten, die vom Endbenutzer oder Computer zurück zu einer Vertrauensstellung führt, in der Regel die Stamm Zertifizierungsstelle (Certification Authority, ca) einer Organisation.</span><span class="sxs-lookup"><span data-stu-id="082f2-104">A certificate chain is a hierarchal collection of certificates that leads from the end user or computer back to a root of trust, typically the root certification authority (CA) of an organization.</span></span> <span data-ttu-id="082f2-105">Da alle Parteien das Stamm Zertifikat wahrscheinlich als vertrauenswürdig einstufen, kann eine Partei durch Überprüfen der Zertifikat Kette eine Vertrauensstellung in einem Endentitäts Zertifikat erlangen.</span><span class="sxs-lookup"><span data-stu-id="082f2-105">Because all parties presumably trust the root certificate, a party can gain trust in an end-entity certificate by verifying the certificate chain.</span></span> <span data-ttu-id="082f2-106">Die Überprüfung erfordert in der Regel die Einrichtung der einzelnen Zertifikate in der Kette:</span><span class="sxs-lookup"><span data-stu-id="082f2-106">Verification typically requires establishing that each certificate in the chain:</span></span>

-   <span data-ttu-id="082f2-107">Wird vom öffentlichen Schlüssel im vorherigen Zertifikat signiert.</span><span class="sxs-lookup"><span data-stu-id="082f2-107">Is signed by the public key in the prior certificate.</span></span>
-   <span data-ttu-id="082f2-108">Ist nicht abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="082f2-108">Has not expired.</span></span>
-   <span data-ttu-id="082f2-109">Wurde nicht widerrufen.</span><span class="sxs-lookup"><span data-stu-id="082f2-109">Has not been revoked.</span></span>
-   <span data-ttu-id="082f2-110">Entspricht den Richtlinien, die von vorherigen Zertifikaten festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="082f2-110">Conforms to the policies specified by prior certificates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="082f2-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="082f2-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="082f2-112">Zertifikat Hierarchie</span><span class="sxs-lookup"><span data-stu-id="082f2-112">Certificate Hierarchy</span></span>](about-certificate-hierarchy.md)
</dt> <dt>

[<span data-ttu-id="082f2-113">Kreuz Zertifizierung</span><span class="sxs-lookup"><span data-stu-id="082f2-113">Cross Certification</span></span>](about-cross-certification.md)
</dt> <dt>

[<span data-ttu-id="082f2-114">Trust-Modelle</span><span class="sxs-lookup"><span data-stu-id="082f2-114">Trust Models</span></span>](about-trust-models.md)
</dt> </dl>

 

 



