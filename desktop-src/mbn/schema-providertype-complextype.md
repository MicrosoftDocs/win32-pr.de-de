---
description: Gibt Informationen über ein Mobilfunknetz an.
ms.assetid: 52d07b64-7939-4f1c-9793-be07af098053
title: komplexer ProviderType-Typ (mobiles Breitband)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerType
api_type:
- Schema
ms.openlocfilehash: 1520425cf6ec1bc246f26f2db2d75f79f45a3dae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356783"
---
# <a name="providertype-complex-type"></a><span data-ttu-id="f9af6-103">komplexer ProviderType-Typ</span><span class="sxs-lookup"><span data-stu-id="f9af6-103">providerType Complex Type</span></span>

<span data-ttu-id="f9af6-104">Der komplexe Typ **ProviderType** gibt Informationen zu einem Mobilfunknetz an.</span><span class="sxs-lookup"><span data-stu-id="f9af6-104">The **providerType** complex type specifies information about a cellular network.</span></span>

``` syntax
<xs:complexType name="providerType">
    <xs:sequence>
        <xs:element name="ProviderID"
            type="providerIdType"
         />
        <xs:element name="ProviderName"
            type="providerNameType"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="f9af6-105">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f9af6-105">Child elements</span></span>



| <span data-ttu-id="f9af6-106">Element</span><span class="sxs-lookup"><span data-stu-id="f9af6-106">Element</span></span>                                                          | <span data-ttu-id="f9af6-107">type</span><span class="sxs-lookup"><span data-stu-id="f9af6-107">Type</span></span>                                                           | <span data-ttu-id="f9af6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9af6-108">Description</span></span>               |
|------------------------------------------------------------------|----------------------------------------------------------------|---------------------------|
| [<span data-ttu-id="f9af6-109">**ProviderID**</span><span class="sxs-lookup"><span data-stu-id="f9af6-109">**ProviderID**</span></span>](schema-providerid-providertype-element.md)     | [<span data-ttu-id="f9af6-110">**provideridtype**</span><span class="sxs-lookup"><span data-stu-id="f9af6-110">**providerIdType**</span></span>](schema-provideridtype-simpletype.md)     | <span data-ttu-id="f9af6-111">Anbieter-ID.</span><span class="sxs-lookup"><span data-stu-id="f9af6-111">Provider ID.</span></span><br/>   |
| [<span data-ttu-id="f9af6-112">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="f9af6-112">**ProviderName**</span></span>](schema-providername-providertype-element.md) | [<span data-ttu-id="f9af6-113">**providernametype**</span><span class="sxs-lookup"><span data-stu-id="f9af6-113">**providerNameType**</span></span>](schema-providernametype-simpletype.md) | <span data-ttu-id="f9af6-114">Der Anbieter Name.</span><span class="sxs-lookup"><span data-stu-id="f9af6-114">Provider name.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f9af6-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9af6-115">Requirements</span></span>



| <span data-ttu-id="f9af6-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9af6-116">Requirement</span></span> | <span data-ttu-id="f9af6-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f9af6-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="f9af6-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9af6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f9af6-119">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="f9af6-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="f9af6-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9af6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f9af6-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f9af6-121">None supported</span></span><br/>                         |



 

 




