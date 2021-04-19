---
title: Komplexer channelellisttype-Typ
description: Definiert eine Liste von Kanälen, zu denen Anbieter Ereignisse protokollieren können. | Komplexer channelellisttype-Typ
ms.assetid: 01685955-7149-45ce-a47f-6344fcf07826
keywords:
- Das Ereignisprotokoll des komplexen channelellisttype-Typs.
topic_type:
- apiref
api_name:
- ChannelListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 53293687fd4ab0d87155b86edd026189f6d7c925
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106361832"
---
# <a name="channellisttype-complex-type"></a><span data-ttu-id="beed2-105">Komplexer channelellisttype-Typ</span><span class="sxs-lookup"><span data-stu-id="beed2-105">ChannelListType Complex Type</span></span>

<span data-ttu-id="beed2-106">Definiert eine Liste von Kanälen, zu denen Anbieter Ereignisse protokollieren können.</span><span class="sxs-lookup"><span data-stu-id="beed2-106">Defines a list of channels to which providers can log events.</span></span>

``` syntax
<xs:complexType name="ChannelListType">
    <xs:choice
        minOccurs="0"
        maxOccurs="8"
    >
        <xs:element name="importChannel"
            type="ImportChannelType"
         />
        <xs:element name="channel"
            type="ChannelType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:choice>
    <xs:anyAttribute
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="beed2-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="beed2-107">Child elements</span></span>



| <span data-ttu-id="beed2-108">Element</span><span class="sxs-lookup"><span data-stu-id="beed2-108">Element</span></span>                                                                            | <span data-ttu-id="beed2-109">type</span><span class="sxs-lookup"><span data-stu-id="beed2-109">Type</span></span>                                                                           | <span data-ttu-id="beed2-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="beed2-110">Description</span></span>                                                                                                                  |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="beed2-111">**Kanals**</span><span class="sxs-lookup"><span data-stu-id="beed2-111">**channel**</span></span>](eventmanifestschema-channel-channellisttype-element.md)             | [<span data-ttu-id="beed2-112">**ChannelType**</span><span class="sxs-lookup"><span data-stu-id="beed2-112">**ChannelType**</span></span>](eventmanifestschema-channeltype-complextype.md)             | <span data-ttu-id="beed2-113">Definiert einen Kanal, zu dem Ereignisse protokolliert werden können.</span><span class="sxs-lookup"><span data-stu-id="beed2-113">Defines a channel to which events can be logged.</span></span><br/>                                                                  |
| [<span data-ttu-id="beed2-114">**importchannel**</span><span class="sxs-lookup"><span data-stu-id="beed2-114">**importChannel**</span></span>](eventmanifestschema-importchannel-channellisttype-element.md) | [<span data-ttu-id="beed2-115">**Importchanneltype**</span><span class="sxs-lookup"><span data-stu-id="beed2-115">**ImportChannelType**</span></span>](eventmanifestschema-importchanneltype-complextype.md) | <span data-ttu-id="beed2-116">Identifiziert einen Kanal, der von einem anderen Anbieter oder einem Manifest definiert wurde, das einen Metadatenabschnitt enthält.</span><span class="sxs-lookup"><span data-stu-id="beed2-116">Identifies a channel that has been defined by another provider or in a manifest that contains a metadata section.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="beed2-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="beed2-117">Remarks</span></span>

<span data-ttu-id="beed2-118">Sie können bis zu acht Kanäle angeben (eine beliebige Kombination aus importierten Kanälen oder Kanälen, die Sie definieren).</span><span class="sxs-lookup"><span data-stu-id="beed2-118">You can specify up to eight channels (any combination of imported channels or channels that you define).</span></span>

## <a name="requirements"></a><span data-ttu-id="beed2-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="beed2-119">Requirements</span></span>



| <span data-ttu-id="beed2-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="beed2-120">Requirement</span></span> | <span data-ttu-id="beed2-121">Wert</span><span class="sxs-lookup"><span data-stu-id="beed2-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="beed2-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="beed2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="beed2-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="beed2-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="beed2-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="beed2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="beed2-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="beed2-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





