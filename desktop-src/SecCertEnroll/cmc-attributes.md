---
description: In der Praxis ist die Struktur einer CMC-Anforderung, die in der folgenden Syntax dargestellt wird, relativ komplex, da sie häufig geschachtelte Anforderungen enthält.
ms.assetid: faeee338-bce4-4b35-9be9-72a6568fa259
title: CMC-Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b98e30c257234ebee864a1749ceecee7b79e25a9e11c9f1f190c60f3154ef64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902063"
---
# <a name="cmc-attributes"></a>CMC-Attribute

In der Praxis ist die Struktur einer CMC-Anforderung, die in der folgenden Syntax dargestellt wird, relativ komplex, da sie häufig geschachtelte Anforderungen enthält. Beispielsweise kann eine CMC-Anforderung null oder eine PKCS \# 10-Anforderung in einer **TaggedRequest-Sequenz** enthalten, und sie kann null oder eine PKCS \# 7-Nachricht in einer **TaggedContentInfo-Sequenz** enthalten. Jede geschachtelte PKCS \# 7-Nachricht kann eine CMC-Anforderung enthalten, die wiederum weitere Anforderungen enthalten kann. Die Anzahl der Schachtelungsebenen ist theoretisch unbegrenzt, aber die Zertifizierungsstelle ist in der Regel so konfiguriert, dass die Größe einer Anforderung begrenzt wird. Attribute können auf die Anforderung der obersten Ebene oder auf die geschachtelten Anforderungen angewendet werden. Dies wird in den folgenden Abschnitten erläutert.

## <a name="cmcdata-structure"></a>CMCData-Struktur

Eine CMC-Anforderung enthält Sequenzen der ASN.1-Strukturen **TaggedAttribute,** **TaggedRequest** und **TaggedContentInfo.**

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

## <a name="taggedattribute-structure"></a>TaggedAttribute-Struktur

Attribute werden in eine CMC-Zertifikatanforderung eingeschlossen, indem sie der **TaggedAttribute-Auflistung** hinzugefügt werden. Jede Struktur in der Auflistung enthält eine ganzzahlige ID, einen ASN.1-Objektbezeichner (OID) und einen Satz von Werten. Die möglichen Werte können wie folgt sein.

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

## <a name="cmcaddattributes"></a>CMCAddAttributes

Wenn die Attribute in dieser Struktur für eine geschachtelte PKCS \# 10-Anforderung gelten, enthält das Feld **certReferences** die **BodyPartID,** die die Anforderung identifiziert. Wenn die Attribute für eine geschachtelte CMC-Anforderung gelten, enthält das Feld **pkiDataReference** die **BodyPartID** der Anforderung. Derzeit kann nur eines dieser Felder ungleich 0 (null) sein. Die Attribute, die eingeschlossen werden können, sind im Thema [Unterstützte Attribute](supported-attributes.md) aufgeführt.

## <a name="cmcaddextensions"></a>CmcAddExtensions

Diese Struktur kann X.509 Version 3-Erweiterungen sowie von Microsoft definierte Erweiterungen enthalten. Dieses Attribut wird mithilfe der [**IX509AttributeExtensions-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) definiert. Wenn die Erweiterungen für eine geschachtelte PKCS \# 10-Anforderung gelten, enthält das Feld **certReferences** die **BodyPartID,** die die Anforderung identifiziert. Wenn die Erweiterungen für eine geschachtelte CMC-Anforderung gelten, enthält das Feld **pkiDataReference** die **BodyPartID** der Anforderung. Derzeit kann nur eines dieser Felder ungleich 0 (null) sein.

## <a name="sendernonce"></a>SenderNonce

Eine Nonce sind zufällige oder pseudozufallsfreie binäre Daten, die in eine Zertifikatanforderung und eine Antworttransaktion eingeschlossen werden können, um sicherzustellen, dass die Antwort oder Anforderung keine Wiederholung einer vorherigen Nachricht ist. Weitere Informationen finden Sie in der [**SenderNonce-Eigenschaft.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_sendernonce)

## <a name="transactid"></a>TransactID

Eine Roundtrip-Zertifikatanforderung und eine Antworttransaktion können mithilfe eines Bezeichners nachverfolgt werden. Der Client generiert eine Transaktions-ID und behält sie bei, bis das Zertifikat oder die Registrierungsstelle mit einer Meldung antwortet, die die Transaktion abschließt. Die Antwort enthält den Bezeichner. Weitere Informationen finden Sie in der [**TransactionId-Eigenschaft.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_transactionid)

## <a name="reginfo"></a>RegInfo

Dieses Attribut kann verwendet werden, um alle Registrierungsinformationen zu enthalten, die der Client für die CMC-Anforderung ausschließt. Der Attributwert ist eine Zeichenfolge, die verkettete Name-Wert-Paare enthält. Weitere Informationen finden Sie unter der [**NameValuePairs-Eigenschaft.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterstützte Attribute](supported-attributes.md)
</dt> </dl>

 

 



