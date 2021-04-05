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
# <a name="cmc-attributes"></a><span data-ttu-id="e457c-103">CMC-Attribute</span><span class="sxs-lookup"><span data-stu-id="e457c-103">CMC Attributes</span></span>

<span data-ttu-id="e457c-104">In der Praxis ist die Struktur einer von der folgenden Syntax gezeigten CMC-Anforderung relativ komplex, da Sie häufig eine Struktur von Anforderungen enthält.</span><span class="sxs-lookup"><span data-stu-id="e457c-104">In practice, the structure of a CMC request, shown by the following syntax, is relatively complex because it often contains nested requests.</span></span> <span data-ttu-id="e457c-105">Beispielsweise kann eine CMC-Anforderung NULL oder eine PKCS \# 10-Anforderung in einer **taggedrequest** -Sequenz enthalten, und Sie kann 0 (null) oder eine PKCS \# 7-Nachricht in einer **taggedcontentinfo** -Sequenz enthalten.</span><span class="sxs-lookup"><span data-stu-id="e457c-105">For example, a CMC request can contain zero or one PKCS \#10 requests in a **TaggedRequest** sequence, and it can contain zero or one PKCS \#7 messages in a **TaggedContentInfo** sequence.</span></span> <span data-ttu-id="e457c-106">Jede geduckte PKCS \# 7-Nachricht kann eine CMC-Anforderung enthalten, die wiederum mehr Anforderungen enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="e457c-106">Each nested PKCS \#7 message can contain a CMC request which can, in turn, contain more requests.</span></span> <span data-ttu-id="e457c-107">Die Anzahl der Schachtelungs Ebenen ist theoretisch unbegrenzt, aber die Zertifizierungsstelle (Certification Authority, ca) ist in der Regel so konfiguriert, dass die Größe einer Anforderung beschränkt wird.</span><span class="sxs-lookup"><span data-stu-id="e457c-107">The number of nesting levels is theoretically unlimited, but the certification authority (CA) is typically configured to limit the size of a request.</span></span> <span data-ttu-id="e457c-108">Attribute können auf die Anforderungen der obersten Ebene oder auf die in der Anforderung verwendeten Anforderungen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="e457c-108">Attributes can be applied to the top level request or to the nested requests.</span></span> <span data-ttu-id="e457c-109">Dies wird in den folgenden Abschnitten erläutert.</span><span class="sxs-lookup"><span data-stu-id="e457c-109">This is discussed in the following sections.</span></span>

## <a name="cmcdata-structure"></a><span data-ttu-id="e457c-110">Cmcdata-Struktur</span><span class="sxs-lookup"><span data-stu-id="e457c-110">CMCData Structure</span></span>

<span data-ttu-id="e457c-111">Eine CMC-Anforderung enthält Sequenzen von **taggedattribute**-, **taggedrequest**-und **taggedcontentinfo** ASN. 1-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="e457c-111">A CMC request contains sequences of **TaggedAttribute**, **TaggedRequest**, and **TaggedContentInfo** ASN.1 structures.</span></span>

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

## <a name="taggedattribute-structure"></a><span data-ttu-id="e457c-112">Taggedattribute-Struktur</span><span class="sxs-lookup"><span data-stu-id="e457c-112">TaggedAttribute Structure</span></span>

<span data-ttu-id="e457c-113">Attribute werden in eine Anforderung eines CMC-Zertifikats eingefügt, indem Sie der **taggedattribute-Auflistung** hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="e457c-113">Attributes are included in a CMC certificate request by adding them to the **TaggedAttribute** collection.</span></span> <span data-ttu-id="e457c-114">Jede Struktur in der Auflistung enthält eine ganzzahlige ID, eine ASN. 1-Objekt Kennung (OID) und einen Satz von Werten.</span><span class="sxs-lookup"><span data-stu-id="e457c-114">Each structure in the collection contains an integer ID, an ASN.1 object identifier (OID), and a set of values.</span></span> <span data-ttu-id="e457c-115">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="e457c-115">The possible values can be any of the following.</span></span>

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

## <a name="cmcaddattributes"></a><span data-ttu-id="e457c-116">Cmcaddattributes</span><span class="sxs-lookup"><span data-stu-id="e457c-116">CMCAddAttributes</span></span>

<span data-ttu-id="e457c-117">Wenn die Attribute in dieser Struktur auf eine geduckte PKCS \# 10-Anforderung zutreffen, enthält das Feld **certreferences** die **bodypartid** , die die Anforderung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e457c-117">If the attributes in this structure apply to a nested PKCS \#10 request, the **certReferences** field will contain the **BodyPartID** that identifies the request.</span></span> <span data-ttu-id="e457c-118">Wenn die Attribute auf eine schsted CMC-Anforderung angewendet werden, enthält das Feld " **pkidatareferenzierung** " die **bodypartid** der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e457c-118">If the attributes apply to a nested CMC request, the **pkiDataReference** field will contain the **BodyPartID** of the request.</span></span> <span data-ttu-id="e457c-119">Derzeit darf nur eines dieser Felder ungleich NULL sein.</span><span class="sxs-lookup"><span data-stu-id="e457c-119">Currently, only one of these fields can be nonzero.</span></span> <span data-ttu-id="e457c-120">Die Attribute, die eingeschlossen werden können, sind im Thema [unterstützte Attribute](supported-attributes.md) aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e457c-120">The attributes that can be included are listed in the [Supported Attributes](supported-attributes.md) topic.</span></span>

## <a name="cmcaddextensions"></a><span data-ttu-id="e457c-121">Cmcaddextensions</span><span class="sxs-lookup"><span data-stu-id="e457c-121">CmcAddExtensions</span></span>

<span data-ttu-id="e457c-122">Diese Struktur kann X. 509 Version 3-Erweiterungen und Erweiterungen enthalten, die von Microsoft definiert werden.</span><span class="sxs-lookup"><span data-stu-id="e457c-122">This structure can contain X.509 version 3 extensions plus extensions defined by Microsoft.</span></span> <span data-ttu-id="e457c-123">Dieses Attribut wird mithilfe der [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="e457c-123">This attribute is defined by using the [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) interface.</span></span> <span data-ttu-id="e457c-124">Wenn die Erweiterungen auf eine geduckte PKCS \# 10-Anforderung angewendet werden, enthält das Feld **certreferences** die **bodypartid** , die die Anforderung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e457c-124">If the extensions apply to a nested PKCS \#10 request, the **certReferences** field will contain the **BodyPartID** that identifies the request.</span></span> <span data-ttu-id="e457c-125">Wenn die Erweiterungen auf eine schsted CMC-Anforderung angewendet werden, enthält das Feld " **pkidatareferenzierung** " die **bodypartid** der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e457c-125">If the extensions apply to a nested CMC request, the **pkiDataReference** field will contain the **BodyPartID** of the request.</span></span> <span data-ttu-id="e457c-126">Derzeit darf nur eines dieser Felder ungleich NULL sein.</span><span class="sxs-lookup"><span data-stu-id="e457c-126">Currently, only one of these fields can be nonzero.</span></span>

## <a name="sendernonce"></a><span data-ttu-id="e457c-127">Sendernonce</span><span class="sxs-lookup"><span data-stu-id="e457c-127">SenderNonce</span></span>

<span data-ttu-id="e457c-128">Bei Nonce handelt es sich um zufällige oder pseudo zufällige Binärdaten, die in eine Zertifikat Anforderungs-und Antwort Transaktion eingeschlossen werden können, um sicherzustellen, dass es sich bei der Antwort oder Anforderung nicht um eine Wiederholung einer vorherigen Nachricht handelt.</span><span class="sxs-lookup"><span data-stu-id="e457c-128">A nonce is random or pseudo-random binary data that can be included in a certificate request and response transaction to help ensure that the response or request is not a repeat of a previous message.</span></span> <span data-ttu-id="e457c-129">Weitere Informationen finden Sie unter der [**Sendernonce**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_sendernonce) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e457c-129">For more information, see the [**SenderNonce**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_sendernonce) property.</span></span>

## <a name="transactid"></a><span data-ttu-id="e457c-130">Transactid</span><span class="sxs-lookup"><span data-stu-id="e457c-130">TransactID</span></span>

<span data-ttu-id="e457c-131">Eine Roundtrip-Zertifikatanforderungs-und-Antwort Transaktion kann mithilfe eines Bezeichners nachverfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="e457c-131">A round trip certificate request and response transaction can be tracked using an identifier.</span></span> <span data-ttu-id="e457c-132">Der Client generiert eine Transaktions-ID und behält sie bei, bis das Zertifikat oder die Registrierungsstelle mit einer Nachricht antwortet, mit der die Transaktion abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="e457c-132">The client generates a transaction ID and retains it until the certificate or registration authority responds with a message that completes the transaction.</span></span> <span data-ttu-id="e457c-133">Die Antwort enthält den Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="e457c-133">The response includes the identifier.</span></span> <span data-ttu-id="e457c-134">Weitere Informationen finden Sie unter der [**transaktionid**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_transactionid) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e457c-134">For more information, see the [**TransactionId**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_transactionid) property.</span></span>

## <a name="reginfo"></a><span data-ttu-id="e457c-135">Reginfo</span><span class="sxs-lookup"><span data-stu-id="e457c-135">RegInfo</span></span>

<span data-ttu-id="e457c-136">Dieses Attribut kann verwendet werden, um alle Registrierungsinformationen zu enthalten, die vom Client in der CMC-Anforderung abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e457c-136">This attribute can be used to contain any registration information that the client chooses to put into the CMC request.</span></span> <span data-ttu-id="e457c-137">Der Attribut Wert ist eine Zeichenfolge, die verketteten Name-Wert-Paaren enthält.</span><span class="sxs-lookup"><span data-stu-id="e457c-137">The attribute value is string that contains concatenated name-value pairs.</span></span> <span data-ttu-id="e457c-138">Weitere Informationen finden Sie unter der [**NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e457c-138">For more information, see the [**NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e457c-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e457c-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e457c-140">Unterstützte Attribute</span><span class="sxs-lookup"><span data-stu-id="e457c-140">Supported Attributes</span></span>](supported-attributes.md)
</dt> </dl>

 

 



