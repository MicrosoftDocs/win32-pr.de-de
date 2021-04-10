---
description: Ein X.509-Zertifikat der Version 2 enthält die grundlegenden Felder, die in Version 1 definiert sind, sowie zusätzlich die folgenden Felder.
ms.assetid: 533d43d7-0c49-4461-8ba8-368c103feb4f
title: Felder der Version 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48e66d66d9c5d92f7c3a0436ae828b60d285edce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214373"
---
# <a name="version-2-fields"></a><span data-ttu-id="d02da-103">Felder der Version 2</span><span class="sxs-lookup"><span data-stu-id="d02da-103">Version 2 Fields</span></span>

<span data-ttu-id="d02da-104">Ein X.509-Zertifikat der Version 2 enthält die grundlegenden Felder, die in Version 1 definiert sind, sowie zusätzlich die folgenden Felder.</span><span class="sxs-lookup"><span data-stu-id="d02da-104">An X.509 version 2 certificate contains the basic fields defined in version 1 and adds the following fields.</span></span>

## <a name="issuer-unique-identifier"></a><span data-ttu-id="d02da-105">Issuer Unique Identifier</span><span class="sxs-lookup"><span data-stu-id="d02da-105">Issuer Unique Identifier</span></span>

<span data-ttu-id="d02da-106">Enthält einen eindeutigen Wert, mit dem der X.500-Name der Zertifizierungsstelle eindeutig festgelegt werden kann, wenn dieser im Lauf der Zeit von verschiedenen Entitäten wiederverwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d02da-106">Contains a unique value that can be used to make the X.500 name of the CA unambiguous when reused by different entities over time.</span></span>

``` syntax
---------------------------------------------------------------------
-- Issuer Unique identifier
---------------------------------------------------------------------
issuerUniqueIdentifier ::= [1] IMPLICIT UniqueIdentifier OPTIONAL

UniqueIdentifier ::= BITSTRING
```

## <a name="subject-unique-identifier"></a><span data-ttu-id="d02da-107">Issuer Unique Identifier</span><span class="sxs-lookup"><span data-stu-id="d02da-107">Subject Unique Identifier</span></span>

<span data-ttu-id="d02da-108">Enthält einen eindeutigen Wert, mit dem der X.500-Name des Zertifikatantragstellers eindeutig festgelegt werden kann, wenn dieser im Lauf der Zeit von verschiedenen Entitäten wiederverwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d02da-108">Contains a unique value that can be used to make the X.500 name of the certificate subject unambiguous when reused by different entities over time.</span></span>

``` syntax
---------------------------------------------------------------------
-- Issuer Unique identifier
---------------------------------------------------------------------
subjectUniqueIdentifier ::= [2] IMPLICIT UniqueIdentifier OPTIONAL

UniqueIdentifier ::= BITSTRING
```

## <a name="related-topics"></a><span data-ttu-id="d02da-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d02da-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d02da-110">Grundlegende Felder</span><span class="sxs-lookup"><span data-stu-id="d02da-110">Basic Fields</span></span>](about-basic-fields.md)
</dt> <dt>

[<span data-ttu-id="d02da-111">Erweiterungen der Version 3</span><span class="sxs-lookup"><span data-stu-id="d02da-111">Version 3 Extensions</span></span>](about-version-3-extensions.md)
</dt> <dt>

[<span data-ttu-id="d02da-112">X. 509-Zertifikate für öffentliche Schlüssel</span><span class="sxs-lookup"><span data-stu-id="d02da-112">X.509 Public Key Certificates</span></span>](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 



