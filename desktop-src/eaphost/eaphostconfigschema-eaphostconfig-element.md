---
title: Eaphostconfig-Element
description: Enthält das EapMethod-Element und das config-oder configblob-Element. Die Elemente config und configblob können nicht gleichzeitig verwendet werden.
ms.assetid: 6c42d71e-0c61-48e4-a447-cfd1eae90297
keywords:
- Eaphostconfig-Element EAPHost
topic_type:
- apiref
api_name:
- EapHostConfig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 125b5fa2cab8bf3f9da12bd842a1a102beee3fb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040030"
---
# <a name="eaphostconfig-element"></a><span data-ttu-id="46a31-105">Eaphostconfig-Element</span><span class="sxs-lookup"><span data-stu-id="46a31-105">EapHostConfig Element</span></span>

<span data-ttu-id="46a31-106">Das **eaphostconfig** -Element enthält das [**EapMethod**](eaphostconfigschema-eapmethod-eaphostconfig-element.md) -Element und das [**config**](eaphostconfigschema-config-eaphostconfig-element.md) -oder [**configblob**](eaphostconfigschema-configblob-eaphostconfig-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="46a31-106">The **EapHostConfig** element contains the [**EapMethod**](eaphostconfigschema-eapmethod-eaphostconfig-element.md) element and [**Config**](eaphostconfigschema-config-eaphostconfig-element.md) or [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) element.</span></span>

<span data-ttu-id="46a31-107">Die Elemente [**config**](eaphostconfigschema-config-eaphostconfig-element.md) und [**configblob**](eaphostconfigschema-configblob-eaphostconfig-element.md) können nicht gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="46a31-107">The [**Config**](eaphostconfigschema-config-eaphostconfig-element.md) and [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) elements cannot both be used simultaneously.</span></span>

``` syntax
<xs:element name="EapHostConfig">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="EapMethod"
                type="EapMethodType"
             />
            <xs:choice>
                <xs:element name="Config"
                    type="BaseEapMethodConfig"
                 />
                <xs:element name="ConfigBlob"
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

## <a name="child-elements"></a><span data-ttu-id="46a31-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="46a31-108">Child elements</span></span>



| <span data-ttu-id="46a31-109">Element</span><span class="sxs-lookup"><span data-stu-id="46a31-109">Element</span></span>                                                                    | <span data-ttu-id="46a31-110">type</span><span class="sxs-lookup"><span data-stu-id="46a31-110">Type</span></span>                                                                                     | <span data-ttu-id="46a31-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46a31-111">Description</span></span>                                                                                          |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46a31-112">**Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="46a31-112">**Config**</span></span>](eaphostconfigschema-config-eaphostconfig-element.md)         | [<span data-ttu-id="46a31-113">**Baseeapmethodconfig**</span><span class="sxs-lookup"><span data-stu-id="46a31-113">**BaseEapMethodConfig**</span></span>](baseeapmethodconfigschema-baseeapmethodconfig-complextype.md) | <span data-ttu-id="46a31-114">Wird verwendet, wenn die Methoden Konfiguration im XML-Textformular statt in einem binären BLOB erfolgt.</span><span class="sxs-lookup"><span data-stu-id="46a31-114">Is used when the method configuration is in XML text form instead of a binary BLOB.</span></span><br/>       |
| [<span data-ttu-id="46a31-115">**Configblob**</span><span class="sxs-lookup"><span data-stu-id="46a31-115">**ConfigBlob**</span></span>](eaphostconfigschema-configblob-eaphostconfig-element.md) | <span data-ttu-id="46a31-116">hexBinary</span><span class="sxs-lookup"><span data-stu-id="46a31-116">hexBinary</span></span>                                                                                | <span data-ttu-id="46a31-117">Wird verwendet, wenn die Methoden Konfiguration im binären BLOB-Formular statt im Textformat der Zeichenfolge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="46a31-117">Is used when the method configuration is in binary BLOB form instead of string text form.</span></span><br/> |
| [<span data-ttu-id="46a31-118">**EapMethod**</span><span class="sxs-lookup"><span data-stu-id="46a31-118">**EapMethod**</span></span>](eaphostconfigschema-eapmethod-eaphostconfig-element.md)   | [<span data-ttu-id="46a31-119">**Eapmethodtype**</span><span class="sxs-lookup"><span data-stu-id="46a31-119">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)                       | <span data-ttu-id="46a31-120">Identifiziert die Methode, auf die verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="46a31-120">Identifies the method being referred to.</span></span> <br/>                                                 |



## <a name="remarks"></a><span data-ttu-id="46a31-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46a31-121">Remarks</span></span>

<span data-ttu-id="46a31-122">Das Element **processContents** ermöglicht zukünftige Erweiterungen des Schemas.</span><span class="sxs-lookup"><span data-stu-id="46a31-122">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="46a31-123">Das **processContents** -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="46a31-123">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="46a31-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46a31-124">Requirements</span></span>



| <span data-ttu-id="46a31-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46a31-125">Requirement</span></span> | <span data-ttu-id="46a31-126">Wert</span><span class="sxs-lookup"><span data-stu-id="46a31-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="46a31-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="46a31-127">Minimum supported client</span></span><br/> | <span data-ttu-id="46a31-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46a31-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="46a31-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="46a31-129">Minimum supported server</span></span><br/> | <span data-ttu-id="46a31-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46a31-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="46a31-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46a31-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46a31-132">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="46a31-132">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="46a31-133">eaphostconfig-Schema</span><span class="sxs-lookup"><span data-stu-id="46a31-133">eaphostconfig Schema</span></span>](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





