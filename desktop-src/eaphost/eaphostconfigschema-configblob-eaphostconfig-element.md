---
title: Configblob-Element (eaphostconfig)
description: Wird verwendet, wenn sich die Methoden Konfiguration im binären BLOB-Formular statt in Form einer Text Zeichenfolge befindet.
ms.assetid: 2820e0b8-2cd1-40e8-ac0c-a62e73ac3847
keywords:
- Configblob-Element EAPHost
topic_type:
- apiref
api_name:
- ConfigBlob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b220c74c6439b4b2cbb0d05a1d540d673e1bd17b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739696"
---
# <a name="configblob-eaphostconfig-element"></a><span data-ttu-id="b458e-104">Configblob-Element (eaphostconfig)</span><span class="sxs-lookup"><span data-stu-id="b458e-104">ConfigBlob (EapHostConfig) Element</span></span>

<span data-ttu-id="b458e-105">Das **configblob-Element (eaphostconfig)** wird verwendet, wenn sich die Methoden Konfiguration im binären BLOB-Formular statt in Form einer Text Zeichenfolge befindet.</span><span class="sxs-lookup"><span data-stu-id="b458e-105">The **ConfigBlob (EapHostConfig)** element is used when the method configuration is in binary BLOB form instead of text string form.</span></span>

``` syntax
<xs:element name="ConfigBlob"
    type="hexBinary"
 />
```

<span data-ttu-id="b458e-106">Das **configblob** -Element wird durch das [**eaphostconfig**](eaphostconfigschema-eaphostconfig-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="b458e-106">The **ConfigBlob** element is defined by the [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="b458e-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b458e-107">Remarks</span></span>

<span data-ttu-id="b458e-108">Die Elemente [**config**](eaphostconfigschema-config-eaphostconfig-element.md) und **configblob** können nicht gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b458e-108">The [**Config**](eaphostconfigschema-config-eaphostconfig-element.md) and **ConfigBlob** elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="b458e-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b458e-109">Requirements</span></span>



| <span data-ttu-id="b458e-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b458e-110">Requirement</span></span> | <span data-ttu-id="b458e-111">Wert</span><span class="sxs-lookup"><span data-stu-id="b458e-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b458e-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b458e-112">Minimum supported client</span></span><br/> | <span data-ttu-id="b458e-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b458e-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b458e-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b458e-114">Minimum supported server</span></span><br/> | <span data-ttu-id="b458e-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b458e-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b458e-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b458e-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="b458e-117">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="b458e-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b458e-118">**Eaphostconfig**</span><span class="sxs-lookup"><span data-stu-id="b458e-118">**EapHostConfig**</span></span>](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

<span data-ttu-id="b458e-119">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="b458e-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b458e-120">**Eaphostconfig**</span><span class="sxs-lookup"><span data-stu-id="b458e-120">**EapHostConfig**</span></span>](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

[<span data-ttu-id="b458e-121">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="b458e-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="b458e-122">eaphostconfig-Schema</span><span class="sxs-lookup"><span data-stu-id="b458e-122">eaphostconfig Schema</span></span>](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





