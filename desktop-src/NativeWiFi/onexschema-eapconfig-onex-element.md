---
description: Gibt die EAPHost-Konfiguration an.
ms.assetid: 71ec3ed6-3670-46fc-a24b-580d15297437
title: Eapconfig-Element (Onex)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EAPConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 955b3647aca787097495b6051407b718dfa91f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347562"
---
# <a name="eapconfig-onex-element"></a><span data-ttu-id="ddd91-103">Eapconfig-Element (Onex)</span><span class="sxs-lookup"><span data-stu-id="ddd91-103">EAPConfig (OneX) Element</span></span>

<span data-ttu-id="ddd91-104">Das **eapconfig** (Onex)-Element gibt die EAPHost-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="ddd91-104">The **EAPConfig** (OneX) element specifies the EAPHost configuration.</span></span>

<span data-ttu-id="ddd91-105">Im Gegensatz zu den meisten Elementen im 802.1 x-Profil Schema befindet sich dieses Element im- `https://www.microsoft.com/provisioning/EapHostConfig` Namespace.</span><span class="sxs-lookup"><span data-stu-id="ddd91-105">Unlike most elements in the 802.1X profile schema, this element is in the `https://www.microsoft.com/provisioning/EapHostConfig` namespace.</span></span> <span data-ttu-id="ddd91-106">Die untergeordneten Elemente werden im [eaphostconfig-Schema](../eaphost/eaphostconfigschema-schema.md)definiert.</span><span class="sxs-lookup"><span data-stu-id="ddd91-106">Its child elements are defined in the [eaphostconfig schema](../eaphost/eaphostconfigschema-schema.md).</span></span> <span data-ttu-id="ddd91-107">Das [**eaphostconfig**](../eaphost/eaphostconfigschema-eaphostconfig-element.md) -Element ist ein untergeordnetes Element des **eapconfig** -Elements.</span><span class="sxs-lookup"><span data-stu-id="ddd91-107">The [**EapHostConfig**](../eaphost/eaphostconfigschema-eaphostconfig-element.md) element is a child of the **EAPConfig** element.</span></span>

``` syntax
<xs:element name="EAPConfig">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                minOccurs="1"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="ddd91-108">Das **eapconfig** -Element wird durch das [**Onex**](onexschema-onex-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="ddd91-108">The **EAPConfig** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddd91-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ddd91-109">Requirements</span></span>



| <span data-ttu-id="ddd91-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ddd91-110">Requirement</span></span> | <span data-ttu-id="ddd91-111">Wert</span><span class="sxs-lookup"><span data-stu-id="ddd91-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ddd91-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ddd91-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ddd91-113">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ddd91-113">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ddd91-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ddd91-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ddd91-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ddd91-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="ddd91-116">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="ddd91-116">Redistributable</span></span><br/>          | <span data-ttu-id="ddd91-117">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="ddd91-117">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="ddd91-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ddd91-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="ddd91-119">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="ddd91-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ddd91-120">**Onex**</span><span class="sxs-lookup"><span data-stu-id="ddd91-120">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="ddd91-121">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="ddd91-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ddd91-122">**Onex**</span><span class="sxs-lookup"><span data-stu-id="ddd91-122">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 
