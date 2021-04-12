---
description: Erweiterungen sind in einer CMC-Anforderung enthalten, indem Sie der taggedattributes-Struktur hinzugefügt werden, wie im folgenden ASN. 1-Syntax Beispiel gezeigt. Weitere Informationen finden Sie im Thema Attribute.
ms.assetid: 3aa9175b-f889-4d5d-8eb2-a8a42f9fe750
title: CMC-Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b104af2b28470627ea593321627ae5e5076b1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217157"
---
# <a name="cmc-extensions"></a>CMC-Erweiterungen

Erweiterungen sind in einer CMC-Anforderung enthalten, indem Sie der **taggedattributes** -Struktur hinzugefügt werden, wie im folgenden ASN. 1-Syntax Beispiel gezeigt. Weitere Informationen finden Sie im Thema [Attribute](attributes.md) .

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

Jede Struktur in der **taggedattributes-Auflistung** enthält eine ganzzahlige ID, eine ASN. 1-Objekt Kennung (OID) und einen Satz von Werten. Erweiterungen werden in eine Anforderung eingefügt, indem dem Feld **Werte** eine **cmcaddextensions** -Struktur hinzugefügt wird. Die ASN. 1-Struktur Syntax wird im folgenden Beispiel gezeigt. Der Objekt Bezeichner ist **XCN \_ OID \_ CMC \_ Add \_ Extensions** (1.3.6.1.5.5.7.7.8).

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

Im folgenden Verfahren wird erläutert, wie Sie die Zertifikatregistrierungs-API verwenden, um einer CMC-Zertifikat Anforderung Erweiterungen hinzuzufügen.

**So verwenden Sie die Zertifikatregistrierungs-API zum Hinzufügen von Erweiterungen zu einer CMC-Zertifikat Anforderung**

1.  Erstellen Sie eine Erweiterung mithilfe einer der verfügbaren Schnittstellen, die von der [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) -Schnittstelle abgeleitet werden, oder verwenden Sie das **IX509Extension** -Objekt direkt zum Erstellen benutzerdefinierter Erweiterungen.
2.  Rufen Sie die [**X509Extensions**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_x509extensions) -Eigenschaft des [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) -Objekts auf, um eine [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) -Auflistung abzurufen.
3.  Fügen Sie die in Schritt 1 erstellten Erweiterungen der [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) -Auflistung hinzu.
4.  Melden [**Sie sich**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) an, um automatisch die folgenden Aktionen auszuführen:
    -   Rufen Sie ein [**icryptattributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) -Objekt aus dem [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) -Objekt ab.
    -   Erstellen und initialisieren Sie ein [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) -Objekt mithilfe der [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) -Auflistung, die Sie in Schritt 2 abgerufen haben.
    -   Erstellen Sie eine [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) -Sammlung, und fügen Sie Ihr das [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) -Objekt hinzu.
    -   Verwenden Sie die [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) -Auflistung, um ein [**icryptattribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) -Objekt zu initialisieren.
    -   Fügen Sie das [**icryptattribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) -Objekt der [**icryptattributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) -Auflistung hinzu.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Attribute](attributes.md)
</dt> <dt>

[Attribut Architektur](attribute-architecture.md)
</dt> <dt>

[CMC-Attribute](cmc-attributes.md)
</dt> <dt>

[Extensions (Erweiterungen)](extensions.md)
</dt> </dl>

 

 



