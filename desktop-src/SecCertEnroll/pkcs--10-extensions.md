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
# <a name="pkcs-10-extensions"></a>PKCS \# 10-Erweiterungen

Erweiterungen sind in einer PKCS \# 10-Zertifikat Anforderung enthalten, indem Sie dem Feld **Attribute** der **certificationrequestinfo** -Struktur hinzugefügt werden, die im folgenden ASN. 1-Syntax Beispiel gezeigt wird. Weitere Informationen finden Sie im Thema [Attribute](attributes.md) .

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

Im folgenden Verfahren wird erläutert, wie Sie mit der Zertifikatregistrierungs-API Erweiterungen zu einer PKCS \# 10-Zertifikat Anforderung hinzufügen:

1.  Rufen Sie eine [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) -Auflistung ab, indem Sie die [**X509Extension**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_x509extensions) -Eigenschaft des [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -Objekts aufrufen.
2.  Erstellen Sie eine Erweiterung mithilfe einer der verfügbaren Schnittstellen, die von der [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) -Schnittstelle abgeleitet werden.
3.  Fügen Sie die in Schritt 2 erstellten Erweiterungen der [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) -Auflistung hinzu, die Sie in Schritt 1 abgerufen haben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Attribute](attributes.md)
</dt> <dt>

[Attribut Architektur](attribute-architecture.md)
</dt> <dt>

[PKCS \# 10-Attribute](pkcs--10-attributes.md)
</dt> <dt>

[Extensions (Erweiterungen)](extensions.md)
</dt> </dl>

 

 



