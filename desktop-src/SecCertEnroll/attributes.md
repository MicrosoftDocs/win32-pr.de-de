---
description: Attribute können einer Zertifikat Anforderung hinzugefügt werden, um eine Zertifizierungsstelle (Certification Authority, ca) mit zusätzlichen Informationen bereitzustellen, die Sie beim Erstellen und Ausstellen eines Zertifikats verwenden kann.
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
ms.openlocfilehash: e7a00c30be8bacf5593d78e21fb420c8a899dc7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753481"
---
# <a name="attributes-certificate-enrollment-api"></a><span data-ttu-id="1b5c9-103">Attribute (Zertifikatregistrierungs-API)</span><span class="sxs-lookup"><span data-stu-id="1b5c9-103">Attributes (Certificate Enrollment API)</span></span>

<span data-ttu-id="1b5c9-104">Attribute können einer Zertifikat Anforderung hinzugefügt werden, um eine Zertifizierungsstelle (Certification Authority, ca) mit zusätzlichen Informationen bereitzustellen, die Sie beim Erstellen und Ausstellen eines Zertifikats verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="1b5c9-104">Attributes can be added to a certificate request to provide a certification authority (CA) with additional information that it can use when creating and issuing a certificate.</span></span> <span data-ttu-id="1b5c9-105">Jedes Attribut ist eine [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der) codierte [*abstrakte Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN. 1)-Struktur, die einen Objekt Bezeichner (OID) und NULL oder mehr Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="1b5c9-105">Each attribute is a [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER) encoded [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) structure that contains an object identifier (OID) and zero or more values.</span></span> <span data-ttu-id="1b5c9-106">Attribute werden mithilfe von Schnittstellen definiert, die in der Zertifikatregistrierungs-API enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="1b5c9-106">Attributes are defined by using interfaces included with the Certificate Enrollment API.</span></span> <span data-ttu-id="1b5c9-107">In den folgenden Themen werden Attribute ausführlicher erläutert:</span><span class="sxs-lookup"><span data-stu-id="1b5c9-107">The following topics discuss attributes in more detail:</span></span>

-   [<span data-ttu-id="1b5c9-108">Unterstützte Attribute</span><span class="sxs-lookup"><span data-stu-id="1b5c9-108">Supported Attributes</span></span>](supported-attributes.md)
-   [<span data-ttu-id="1b5c9-109">Attribut Architektur</span><span class="sxs-lookup"><span data-stu-id="1b5c9-109">Attribute Architecture</span></span>](attribute-architecture.md)
-   [<span data-ttu-id="1b5c9-110">PKCS \# 7-Attribute</span><span class="sxs-lookup"><span data-stu-id="1b5c9-110">PKCS \#7 Attributes</span></span>](pkcs--7-attributes.md)
-   [<span data-ttu-id="1b5c9-111">PKCS \# 10-Attribute</span><span class="sxs-lookup"><span data-stu-id="1b5c9-111">PKCS \#10 Attributes</span></span>](pkcs--10-attributes.md)
-   [<span data-ttu-id="1b5c9-112">CMC-Attribute</span><span class="sxs-lookup"><span data-stu-id="1b5c9-112">CMC Attributes</span></span>](cmc-attributes.md)

 

 
