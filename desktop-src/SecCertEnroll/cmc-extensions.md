---
description: Erweiterungen sind in einer CMC-Anforderung enthalten, indem sie der Struktur TaggedAttributes hinzugefügt werden, die im folgenden ASN.1-Syntaxbeispiel gezeigt wird. Weitere Informationen finden Sie im Thema Attribute.
ms.assetid: 3aa9175b-f889-4d5d-8eb2-a8a42f9fe750
title: CMC-Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d29873bc43f7a7229b363a7b09cdf03a23127cc5d5e0e738036c6005a6cc7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901843"
---
# <a name="cmc-extensions"></a>CMC-Erweiterungen

Erweiterungen sind in einer CMC-Anforderung enthalten, indem sie der **Struktur TaggedAttributes** hinzugefügt werden, die im folgenden ASN.1-Syntaxbeispiel gezeigt wird. Weitere Informationen finden Sie im [Thema Attribute.](attributes.md)

``` syntax
CmcData ::= SEQUENCE 
{
   controlSequence         ControlSequence,
   reqSequence             ReqSequence,
   cmsSequence             CmsSequence,
   otherMsgSequence        OtherMsgSequence
}


ControlSequence  ::=    SEQUENCE OF TaggedAttribute

TaggedAttribute ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   type                    EncodedObjectID,
   values                  AttributeSetValue
}

BodyPartID ::= INTEGER (0..4294967295)
EncodedObjectID ::= OBJECT IDENTIFIER
AttributeSetValue ::= SET OF ANY
```

Jede Struktur in der **TaggedAttributes-Auflistung** enthält eine ganzzahlige ID, einen ASN.1-Objektbezeichner (OID) und einen Satz von Werten. Erweiterungen werden in eine Anforderung integriert, indem dem Wertefeld eine **CmcAddExtensions-Struktur** **hinzugefügt** wird. Die ASN.1-Struktursyntax wird im folgenden Beispiel gezeigt. Der Objektbezeichner ist **XCN \_ OID \_ CMC \_ ADD \_ EXTENSIONS** (1.3.6.1.5.5.7.7.8).

``` syntax
CmcAddExtensions ::= SEQUENCE 
{
   pkiDataReference        BodyPartID,
   certReferences          BodyPartIDSequence,
   extensions              Extensions
}

Extensions ::= SEQUENCE OF Extension

Extension ::= SEQUENCE 
{
   extnId              EncodedObjectID,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTETSTRING
}
```

Im folgenden Verfahren wird erläutert, wie Sie die Zertifikatregistrierungs-API verwenden, um einer CMC-Zertifikatanforderung Erweiterungen hinzuzufügen.

**So verwenden Sie die Zertifikatregistrierungs-API zum Hinzufügen von Erweiterungen zu einer CMC-Zertifikatanforderung**

1.  Erstellen Sie eine Erweiterung mithilfe einer der verfügbaren Schnittstellen, die von der [**IX509Extension-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) ableiten, oder verwenden Sie das **IX509Extension-Objekt** direkt, um benutzerdefinierte Erweiterungen zu erstellen.
2.  Rufen Sie [**die X509Extensions-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_x509extensions) für das [**IX509CertificateRequestCmc-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) auf, um eine [**IX509Extensions-Auflistung**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) abzurufen.
3.  Fügen Sie die in Schritt 1 erstellten Erweiterungen der [**Collection IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) hinzu.
4.  Rufen Sie [**Registrieren**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) auf, um die folgenden Aktionen automatisch durchzuführen:
    -   Rufen Sie [**ein ICryptAttributes-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) aus dem [**IX509CertificateRequestCmc-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) ab.
    -   Erstellen und initialisieren Sie ein [**IX509AttributeExtensions-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) mithilfe der [**IX509Extensions-Auflistung,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) die in Schritt 2 abgerufen wurde.
    -   Erstellen Sie eine [**IX509Attributes-Auflistung,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) und fügen Sie ihr das [**Objekt IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) hinzu.
    -   Verwenden Sie [**die IX509Attributes-Auflistung,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) um ein [**ICryptAttribute-Objekt zu**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) initialisieren.
    -   Fügen Sie [**das ICryptAttribute-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) der [**ICryptAttributes-Auflistung**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) hinzu.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Attribute](attributes.md)
</dt> <dt>

[Attributarchitektur](attribute-architecture.md)
</dt> <dt>

[CMC-Attribute](cmc-attributes.md)
</dt> <dt>

[Erweiterungen](extensions.md)
</dt> </dl>

 

 



