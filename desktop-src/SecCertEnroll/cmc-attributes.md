---
description: In der Praxis ist die Struktur einer von der folgenden Syntax gezeigten CMC-Anforderung relativ komplex, da Sie häufig eine Struktur von Anforderungen enthält.
ms.assetid: faeee338-bce4-4b35-9be9-72a6568fa259
title: CMC-Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e6778575a9359ad5b8764528fb0351b68efc1e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758071"
---
# <a name="cmc-attributes"></a>CMC-Attribute

In der Praxis ist die Struktur einer von der folgenden Syntax gezeigten CMC-Anforderung relativ komplex, da Sie häufig eine Struktur von Anforderungen enthält. Beispielsweise kann eine CMC-Anforderung NULL oder eine PKCS \# 10-Anforderung in einer **taggedrequest** -Sequenz enthalten, und Sie kann 0 (null) oder eine PKCS \# 7-Nachricht in einer **taggedcontentinfo** -Sequenz enthalten. Jede geduckte PKCS \# 7-Nachricht kann eine CMC-Anforderung enthalten, die wiederum mehr Anforderungen enthalten kann. Die Anzahl der Schachtelungs Ebenen ist theoretisch unbegrenzt, aber die Zertifizierungsstelle (Certification Authority, ca) ist in der Regel so konfiguriert, dass die Größe einer Anforderung beschränkt wird. Attribute können auf die Anforderungen der obersten Ebene oder auf die in der Anforderung verwendeten Anforderungen angewendet werden. Dies wird in den folgenden Abschnitten erläutert.

## <a name="cmcdata-structure"></a>Cmcdata-Struktur

Eine CMC-Anforderung enthält Sequenzen von **taggedattribute**-, **taggedrequest**-und **taggedcontentinfo** ASN. 1-Strukturen.

``` syntax
CmcData ::= SEQUENCE 
{
   controlSequence         ControlSequence,
   reqSequence             ReqSequence,
   cmsSequence             CmsSequence,
   otherMsgSequence        OtherMsgSequence
}


ControlSequence  ::=    SEQUENCE OF TaggedAttribute
ReqSequence      ::=    SEQUENCE OF TaggedRequest
CmsSequence      ::=    SEQUENCE OF TaggedContentInfo

TaggedAttribute ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   type                    EncodedObjectID,
   values                  AttributeSetValue
}

TaggedRequest ::= CHOICE 
{
   tcr                     [0] IMPLICIT TaggedCertificationRequest
}

TaggedContentInfo ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   contentInfo             ANY
}

BodyPartID ::= INTEGER (0..4294967295)
EncodedObjectID ::= OBJECT IDENTIFIER
AttributeSetValue ::= SET OF ANY
```

## <a name="taggedattribute-structure"></a>Taggedattribute-Struktur

Attribute werden in eine Anforderung eines CMC-Zertifikats eingefügt, indem Sie der **taggedattribute-Auflistung** hinzugefügt werden. Jede Struktur in der Auflistung enthält eine ganzzahlige ID, eine ASN. 1-Objekt Kennung (OID) und einen Satz von Werten. Folgende Werte sind möglich:

``` syntax
CmcAddAttributes ::= SEQUENCE 
{
   pkiDataReference        BodyPartID,
   certReferences          BodyPartIDSequence,
   attributes              Attributes
}

Attributes ::= SET OF Attribute
Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}

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

SenderNonce ::= OCTET STRING

TransactID ::= OCTET STRING

RegInfo ::= OCTET STRING
```

## <a name="cmcaddattributes"></a>Cmcaddattributes

Wenn die Attribute in dieser Struktur auf eine geduckte PKCS \# 10-Anforderung zutreffen, enthält das Feld **certreferences** die **bodypartid** , die die Anforderung identifiziert. Wenn die Attribute auf eine schsted CMC-Anforderung angewendet werden, enthält das Feld " **pkidatareferenzierung** " die **bodypartid** der Anforderung. Derzeit darf nur eines dieser Felder ungleich NULL sein. Die Attribute, die eingeschlossen werden können, sind im Thema [unterstützte Attribute](supported-attributes.md) aufgeführt.

## <a name="cmcaddextensions"></a>Cmcaddextensions

Diese Struktur kann X. 509 Version 3-Erweiterungen und Erweiterungen enthalten, die von Microsoft definiert werden. Dieses Attribut wird mithilfe der [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) -Schnittstelle definiert. Wenn die Erweiterungen auf eine geduckte PKCS \# 10-Anforderung angewendet werden, enthält das Feld **certreferences** die **bodypartid** , die die Anforderung identifiziert. Wenn die Erweiterungen auf eine schsted CMC-Anforderung angewendet werden, enthält das Feld " **pkidatareferenzierung** " die **bodypartid** der Anforderung. Derzeit darf nur eines dieser Felder ungleich NULL sein.

## <a name="sendernonce"></a>Sendernonce

Bei Nonce handelt es sich um zufällige oder pseudo zufällige Binärdaten, die in eine Zertifikat Anforderungs-und Antwort Transaktion eingeschlossen werden können, um sicherzustellen, dass es sich bei der Antwort oder Anforderung nicht um eine Wiederholung einer vorherigen Nachricht handelt. Weitere Informationen finden Sie unter der [**Sendernonce**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_sendernonce) -Eigenschaft.

## <a name="transactid"></a>Transactid

Eine Roundtrip-Zertifikatanforderungs-und-Antwort Transaktion kann mithilfe eines Bezeichners nachverfolgt werden. Der Client generiert eine Transaktions-ID und behält sie bei, bis das Zertifikat oder die Registrierungsstelle mit einer Nachricht antwortet, mit der die Transaktion abgeschlossen wird. Die Antwort enthält den Bezeichner. Weitere Informationen finden Sie unter der [**transaktionid**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_transactionid) -Eigenschaft.

## <a name="reginfo"></a>Reginfo

Dieses Attribut kann verwendet werden, um alle Registrierungsinformationen zu enthalten, die vom Client in der CMC-Anforderung abgelegt werden. Der Attribut Wert ist eine Zeichenfolge, die verketteten Name-Wert-Paaren enthält. Weitere Informationen finden Sie unter der [**NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) -Eigenschaft.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterstützte Attribute](supported-attributes.md)
</dt> </dl>

 

 



