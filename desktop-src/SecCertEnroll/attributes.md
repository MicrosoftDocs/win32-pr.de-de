---
description: 'Attribute (Zertifikatregistrierungs-API): Attribute können einer Zertifikatanforderung hinzugefügt werden, um einer Zertifizierungsstelle zusätzliche Informationen bereitzustellen, die sie beim Erstellen und Ausstellen eines Zertifikats verwenden kann.'
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Attribute (Zertifikatregistrierungs-API)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 93414156c7fa6e46fe80995d8d01eadc28796ec2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118428"
---
# <a name="attributes-certificate-enrollment-api"></a><span data-ttu-id="d97b9-103">Attribute (Zertifikatregistrierungs-API)</span><span class="sxs-lookup"><span data-stu-id="d97b9-103">Attributes (Certificate Enrollment API)</span></span>

<span data-ttu-id="d97b9-104">Attribute können einer Zertifikatanforderung hinzugefügt werden, um einer Zertifizierungsstelle zusätzliche Informationen bereitzustellen, die sie beim Erstellen und Ausstellen eines Zertifikats verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="d97b9-104">Attributes can be added to a certificate request to provide a certification authority (CA) with additional information that it can use when creating and issuing a certificate.</span></span> <span data-ttu-id="d97b9-105">Jedes Attribut ist eine [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER)-codierte ASN.1-Struktur [*(Abstract Syntax Notation One),*](/windows/desktop/SecGloss/a-gly) die einen Objektbezeichner (Object Identifier, OID) und 0 (null) oder mehr Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="d97b9-105">Each attribute is a [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER) encoded [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) structure that contains an object identifier (OID) and zero or more values.</span></span> <span data-ttu-id="d97b9-106">Attribute werden mithilfe von Schnittstellen definiert, die in der Zertifikatregistrierungs-API enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d97b9-106">Attributes are defined by using interfaces included with the Certificate Enrollment API.</span></span> <span data-ttu-id="d97b9-107">In den folgenden Themen werden Attribute ausführlicher erläutert:</span><span class="sxs-lookup"><span data-stu-id="d97b9-107">The following topics discuss attributes in more detail:</span></span>

-   [<span data-ttu-id="d97b9-108">Unterstützte Attribute</span><span class="sxs-lookup"><span data-stu-id="d97b9-108">Supported Attributes</span></span>](supported-attributes.md)
-   [<span data-ttu-id="d97b9-109">Attributarchitektur</span><span class="sxs-lookup"><span data-stu-id="d97b9-109">Attribute Architecture</span></span>](attribute-architecture.md)
-   [<span data-ttu-id="d97b9-110">PKCS \# 7-Attribute</span><span class="sxs-lookup"><span data-stu-id="d97b9-110">PKCS \#7 Attributes</span></span>](pkcs--7-attributes.md)
-   [<span data-ttu-id="d97b9-111">PKCS \# 10-Attribute</span><span class="sxs-lookup"><span data-stu-id="d97b9-111">PKCS \#10 Attributes</span></span>](pkcs--10-attributes.md)
-   [<span data-ttu-id="d97b9-112">CMC-Attribute</span><span class="sxs-lookup"><span data-stu-id="d97b9-112">CMC Attributes</span></span>](cmc-attributes.md)

 

 
