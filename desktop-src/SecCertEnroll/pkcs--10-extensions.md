---
description: Erweiterungen sind in einer PKCS \# 10-Zertifikat Anforderung enthalten, indem Sie dem Feld Attribute der certificationrequestinfo-Struktur hinzugefügt werden, die im folgenden ASN. 1-Syntax Beispiel gezeigt wird. Weitere Informationen finden Sie im Thema Attribute.
ms.assetid: 26fa8476-a0ad-4114-a1e7-ed3d4fc9d30e
title: PKCS \# 10-Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba71f0a24f50503fd92b3b9670b787dea3b9ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362999"
---
# <a name="pkcs-10-extensions"></a><span data-ttu-id="0d02d-104">PKCS \# 10-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="0d02d-104">PKCS \#10 Extensions</span></span>

<span data-ttu-id="0d02d-105">Erweiterungen sind in einer PKCS \# 10-Zertifikat Anforderung enthalten, indem Sie dem Feld **Attribute** der **certificationrequestinfo** -Struktur hinzugefügt werden, die im folgenden ASN. 1-Syntax Beispiel gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0d02d-105">Extensions are included in a PKCS \#10 certificate request by adding them to the **attributes** field of the **CertificationRequestInfo** structure shown in the following ASN.1 syntax example.</span></span> <span data-ttu-id="0d02d-106">Weitere Informationen finden Sie im Thema [Attribute](attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="0d02d-106">For more information, see the [Attributes](attributes.md) topic.</span></span>

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

<span data-ttu-id="0d02d-107">Im folgenden Verfahren wird erläutert, wie Sie mit der Zertifikatregistrierungs-API Erweiterungen zu einer PKCS \# 10-Zertifikat Anforderung hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="0d02d-107">The following procedure discusses how to use the Certificate Enrollment API to add extensions to a PKCS \#10 certificate request:</span></span>

1.  <span data-ttu-id="0d02d-108">Rufen Sie eine [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) -Auflistung ab, indem Sie die [**X509Extension**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_x509extensions) -Eigenschaft des [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -Objekts aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0d02d-108">Retrieve an [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection by calling the [**X509Extension**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_x509extensions) property on the [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object.</span></span>
2.  <span data-ttu-id="0d02d-109">Erstellen Sie eine Erweiterung mithilfe einer der verfügbaren Schnittstellen, die von der [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) -Schnittstelle abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="0d02d-109">Create an extension by using any of the available interfaces that derive from the [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) interface.</span></span>
3.  <span data-ttu-id="0d02d-110">Fügen Sie die in Schritt 2 erstellten Erweiterungen der [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) -Auflistung hinzu, die Sie in Schritt 1 abgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="0d02d-110">Add the extensions created in step 2 to the [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection retrieved in step 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d02d-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0d02d-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d02d-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="0d02d-112">Attributes</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="0d02d-113">Attribut Architektur</span><span class="sxs-lookup"><span data-stu-id="0d02d-113">Attribute Architecture</span></span>](attribute-architecture.md)
</dt> <dt>

[<span data-ttu-id="0d02d-114">PKCS \# 10-Attribute</span><span class="sxs-lookup"><span data-stu-id="0d02d-114">PKCS \#10 Attributes</span></span>](pkcs--10-attributes.md)
</dt> <dt>

[<span data-ttu-id="0d02d-115">Extensions (Erweiterungen)</span><span class="sxs-lookup"><span data-stu-id="0d02d-115">Extensions</span></span>](extensions.md)
</dt> </dl>

 

 



