---
description: Gibt den Namen und den Typ eines drahtlos Netzwerks an.
ms.assetid: 839afae0-b8e1-489f-8811-19a82c173627
title: komplexer networkitemtype-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkItemType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5db7c5fc4d9b5227d9cd29c5e2dfc69da6fad139
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362653"
---
# <a name="networkitemtype-complex-type"></a><span data-ttu-id="0a766-103">komplexer networkitemtype-Typ</span><span class="sxs-lookup"><span data-stu-id="0a766-103">networkItemType Complex Type</span></span>

<span data-ttu-id="0a766-104">Der komplexe Typ networkitemtype gibt den Namen und den Typ eines drahtlos Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="0a766-104">The networkItemType complex type specifies the name and type of a wireless network.</span></span>

``` syntax
<xs:complexType name="networkItemType">
    <xs:sequence>
        <xs:element name="networkName"
            type="networkNameType"
         />
        <xs:element name="networkType"
            type="networkTypeType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="0a766-105">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0a766-105">Child elements</span></span>



| <span data-ttu-id="0a766-106">Element</span><span class="sxs-lookup"><span data-stu-id="0a766-106">Element</span></span>                                                                      | <span data-ttu-id="0a766-107">type</span><span class="sxs-lookup"><span data-stu-id="0a766-107">Type</span></span>                                                                    | <span data-ttu-id="0a766-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0a766-108">Description</span></span>                                                   |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="0a766-109">**Network Name**</span><span class="sxs-lookup"><span data-stu-id="0a766-109">**networkName**</span></span>](wlan-policyschema-networkname-networkitemtype-element.md) | [<span data-ttu-id="0a766-110">**networknametype**</span><span class="sxs-lookup"><span data-stu-id="0a766-110">**networkNameType**</span></span>](wlan-policyschema-networknametype-simpletype.md) | <span data-ttu-id="0a766-111">Der Service Set Identifier (SSID) des Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="0a766-111">The service set identifier (SSID) of the network.</span></span> <br/> |
| [<span data-ttu-id="0a766-112">**Network Type**</span><span class="sxs-lookup"><span data-stu-id="0a766-112">**networkType**</span></span>](wlan-policyschema-networktype-networkitemtype-element.md) | [<span data-ttu-id="0a766-113">**Network Typetype**</span><span class="sxs-lookup"><span data-stu-id="0a766-113">**networkTypeType**</span></span>](wlan-policyschema-networktypetype-simpletype.md) | <span data-ttu-id="0a766-114">Der Netzwerktyp.</span><span class="sxs-lookup"><span data-stu-id="0a766-114">The network type.</span></span> <br/>                                 |



## <a name="requirements"></a><span data-ttu-id="0a766-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a766-115">Requirements</span></span>



| <span data-ttu-id="0a766-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a766-116">Requirement</span></span> | <span data-ttu-id="0a766-117">Wert</span><span class="sxs-lookup"><span data-stu-id="0a766-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0a766-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0a766-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0a766-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a766-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0a766-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0a766-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0a766-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a766-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




