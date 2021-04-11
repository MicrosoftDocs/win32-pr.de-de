---
title: Eaphustuser-Anmelde Informationen-Element
description: Enthält das EapMethod-Element und die-Anmelde Informationen oder das-Element für das-Element.
ms.assetid: 6d0d41c8-560c-4d42-83c9-865053aef47a
keywords:
- Eaphostuser-Anmelde Informationen-Element EAPHost
topic_type:
- apiref
api_name:
- EapHostUserCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 690770091219e51b3ebb550a1a72e50f76b20542
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104871"
---
# <a name="eaphostusercredentials-element"></a><span data-ttu-id="cedb9-104">Eaphustuser-Anmelde Informationen-Element</span><span class="sxs-lookup"><span data-stu-id="cedb9-104">EapHostUserCredentials Element</span></span>

<span data-ttu-id="cedb9-105">Das **eapanstuseranmelde** -Element enthält das [**EapMethod**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md) -Element und die [**Anmelde**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) [**Informationen oder das**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) Element "-Element".</span><span class="sxs-lookup"><span data-stu-id="cedb9-105">The **EapHostUserCredentials** element contains the [**EapMethod**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md) element, and [**Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) or [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) element.</span></span>

``` syntax
<xs:element name="EapHostUserCredentials">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="EapMethod"
                type="EapMethodType"
             />
            <xs:choice>
                <xs:element name="Credentials"
                    type="BaseEapMethodUserCredentials"
                 />
                <xs:element name="CredentialsBlob"
                    type="hexBinary"
                 />
            </xs:choice>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="cedb9-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cedb9-106">Child elements</span></span>



| <span data-ttu-id="cedb9-107">Element</span><span class="sxs-lookup"><span data-stu-id="cedb9-107">Element</span></span>                                                                                                | <span data-ttu-id="cedb9-108">type</span><span class="sxs-lookup"><span data-stu-id="cedb9-108">Type</span></span>                                                                                                                | <span data-ttu-id="cedb9-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cedb9-109">Description</span></span>                                                                                      |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cedb9-110">**Daten**</span><span class="sxs-lookup"><span data-stu-id="cedb9-110">**Credentials**</span></span>](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md)         | [<span data-ttu-id="cedb9-111">**Baseeapmethoduseranmeldeinformationen**</span><span class="sxs-lookup"><span data-stu-id="cedb9-111">**BaseEapMethodUserCredentials**</span></span>](baseeapmethodusercredentialsschema-baseeapmethodusercredentials-complextype.md) | <span data-ttu-id="cedb9-112">Wird verwendet, wenn die Methoden Konfiguration im XML-Textformular statt in einem binären BLOB erfolgt.</span><span class="sxs-lookup"><span data-stu-id="cedb9-112">Is used when the method configuration is in XML text form instead of a binary BLOB.</span></span><br/>   |
| [<span data-ttu-id="cedb9-113">**"Kredentialsblob"**</span><span class="sxs-lookup"><span data-stu-id="cedb9-113">**CredentialsBlob**</span></span>](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) | <span data-ttu-id="cedb9-114">hexBinary</span><span class="sxs-lookup"><span data-stu-id="cedb9-114">hexBinary</span></span>                                                                                                           | <span data-ttu-id="cedb9-115">Wird verwendet, wenn die Methoden Konfiguration ein binäres Blob anstelle von im XML-Textformat ist.</span><span class="sxs-lookup"><span data-stu-id="cedb9-115">Is used when the method configuration is a binary BLOB instead of in XML text format.</span></span><br/> |
| [<span data-ttu-id="cedb9-116">**EapMethod**</span><span class="sxs-lookup"><span data-stu-id="cedb9-116">**EapMethod**</span></span>](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md)             | [<span data-ttu-id="cedb9-117">**Eapmethodtype**</span><span class="sxs-lookup"><span data-stu-id="cedb9-117">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)                                                  | <span data-ttu-id="cedb9-118">Identifiziert die Methode, auf die verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="cedb9-118">Identifies the method being referred to.</span></span> <br/>                                             |



## <a name="remarks"></a><span data-ttu-id="cedb9-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cedb9-119">Remarks</span></span>

<span data-ttu-id="cedb9-120">Die Elemente " [**Anmelde**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) Informationen" und " [**kredentialsblob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) " können nicht gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cedb9-120">The [**Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) and [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) elements cannot be both be used simultaneously.</span></span>

<span data-ttu-id="cedb9-121">Es gibt einen Erweiterungs Punkt für andere Namespaces.</span><span class="sxs-lookup"><span data-stu-id="cedb9-121">There is an extension point for other namespaces.</span></span>

<span data-ttu-id="cedb9-122">Das Element **processContents** ermöglicht zukünftige Erweiterungen des Schemas.</span><span class="sxs-lookup"><span data-stu-id="cedb9-122">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="cedb9-123">Das **processContents** -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="cedb9-123">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="cedb9-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cedb9-124">Requirements</span></span>



| <span data-ttu-id="cedb9-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cedb9-125">Requirement</span></span> | <span data-ttu-id="cedb9-126">Wert</span><span class="sxs-lookup"><span data-stu-id="cedb9-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cedb9-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cedb9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="cedb9-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cedb9-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cedb9-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cedb9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="cedb9-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cedb9-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cedb9-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cedb9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cedb9-132">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="cedb9-132">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="cedb9-133">eaphustuseranmelde-Schema</span><span class="sxs-lookup"><span data-stu-id="cedb9-133">eaphostusercredentials Schema</span></span>](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





