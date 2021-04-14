---
description: Attribute sind in einer PKCS \# 10-Zertifikat Anforderung enthalten, indem Sie zur certificationrequestinfo-Struktur hinzugefügt werden, die im folgenden ASN. 1-Syntax Beispiel gezeigt wird.
ms.assetid: 5f00f638-9edb-474b-a7e4-f6f7b62c89a4
title: PKCS \# 10-Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6c69260fa09b99c4d91fa1f8bcdafeb4b0da285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350188"
---
# <a name="pkcs-10-attributes"></a><span data-ttu-id="ae7d1-103">PKCS \# 10-Attribute</span><span class="sxs-lookup"><span data-stu-id="ae7d1-103">PKCS \#10 Attributes</span></span>

<span data-ttu-id="ae7d1-104">Attribute sind in einer PKCS \# 10-Zertifikat Anforderung enthalten, indem Sie zur **certificationrequestinfo** -Struktur hinzugefügt werden, die im folgenden ASN. 1-Syntax Beispiel gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ae7d1-104">Attributes are included in a PKCS \#10 certificate request by adding them to the **CertificationRequestInfo** structure shown in the following ASN.1 syntax example.</span></span> <span data-ttu-id="ae7d1-105">Weitere Informationen zum Hinzufügen von Attributen zu einer Anforderung finden Sie im Thema [Attribut Architektur](attribute-architecture.md) .</span><span class="sxs-lookup"><span data-stu-id="ae7d1-105">For more information about how you can add attributes to a request, see the [Attribute Architecture](attribute-architecture.md) topic.</span></span>

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 ANY,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}
```

<span data-ttu-id="ae7d1-106">Das Attribut, das am häufigsten einer PKCS \# 10-Anforderung hinzugefügt wird, ist eine Sammlung von Erweiterungen der Version 3, die durch ein [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) -Objekt definiert werden</span><span class="sxs-lookup"><span data-stu-id="ae7d1-106">The attribute most commonly added to a PKCS \#10 request is a collection of version 3 extensions defined by an [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) object.</span></span> <span data-ttu-id="ae7d1-107">Da eine PKCS \# 10-Anforderung kein Feld enthält, dem die Erweiterungen direkt hinzugefügt werden können, müssen Sie als Attribut hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="ae7d1-107">Because a PKCS \#10 request does not contain a field to which the extensions can be directly added, they must be added as an attribute.</span></span> <span data-ttu-id="ae7d1-108">Die Attribute " **ClientID**", " **cspprovider**", " **OSVersion**" und " **renewalcertificate** " können auch einem PKCS-Thema hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="ae7d1-108">The **ClientId**, **CspProvider**, **OSVersion**, and **RenewalCertificate** attributes can also be added to a PKCS ) topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae7d1-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ae7d1-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae7d1-110">Unterstützte Attribute</span><span class="sxs-lookup"><span data-stu-id="ae7d1-110">Supported Attributes</span></span>](supported-attributes.md)
</dt> </dl>

 

 



