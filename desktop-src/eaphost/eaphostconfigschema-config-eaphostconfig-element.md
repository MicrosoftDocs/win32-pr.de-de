---
title: Config-Element (eaphostconfig)
description: Wird verwendet, wenn die Methoden Konfiguration im XML-Textformular statt in einem binären BLOB erfolgt.
ms.assetid: f47bec23-745f-47db-84db-2556beb6a9e9
keywords:
- Config-Element EAPHost
topic_type:
- apiref
api_name:
- Config
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a81c90063a57a9d55d8ab6d9c18486315c187f0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477169"
---
# <a name="config-eaphostconfig-element"></a><span data-ttu-id="b287f-104">Config-Element (eaphostconfig)</span><span class="sxs-lookup"><span data-stu-id="b287f-104">Config (EapHostConfig) Element</span></span>

<span data-ttu-id="b287f-105">Das Element **config (eaphostconfig)** wird verwendet, wenn die Methoden Konfiguration im XML-Textformular statt in einem binären BLOB erfolgt.</span><span class="sxs-lookup"><span data-stu-id="b287f-105">The **Config (EapHostConfig)** element is used when the method configuration is in XML text form instead of a binary BLOB.</span></span>

``` syntax
<xs:element name="Config"
    type="BaseEapMethodConfig"
 />
```

<span data-ttu-id="b287f-106">Das **config** -Element wird durch das [**eaphostconfig**](eaphostconfigschema-eaphostconfig-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="b287f-106">The **Config** element is defined by the [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="b287f-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b287f-107">Remarks</span></span>

<span data-ttu-id="b287f-108">Die Elemente **config** und [**configblob**](eaphostconfigschema-configblob-eaphostconfig-element.md) können nicht gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b287f-108">The **Config** and [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="b287f-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b287f-109">Requirements</span></span>



| <span data-ttu-id="b287f-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b287f-110">Requirement</span></span> | <span data-ttu-id="b287f-111">Wert</span><span class="sxs-lookup"><span data-stu-id="b287f-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b287f-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b287f-112">Minimum supported client</span></span><br/> | <span data-ttu-id="b287f-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b287f-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b287f-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b287f-114">Minimum supported server</span></span><br/> | <span data-ttu-id="b287f-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b287f-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b287f-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b287f-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="b287f-117">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="b287f-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b287f-118">**Eaphostconfig**</span><span class="sxs-lookup"><span data-stu-id="b287f-118">**EapHostConfig**</span></span>](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

<span data-ttu-id="b287f-119">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="b287f-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b287f-120">**Eaphostconfig**</span><span class="sxs-lookup"><span data-stu-id="b287f-120">**EapHostConfig**</span></span>](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

[<span data-ttu-id="b287f-121">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="b287f-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="b287f-122">eaphostconfig-Schema</span><span class="sxs-lookup"><span data-stu-id="b287f-122">eaphostconfig Schema</span></span>](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





