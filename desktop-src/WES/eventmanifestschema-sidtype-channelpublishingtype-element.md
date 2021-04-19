---
title: SIDType (channelpublishingtype)-Element
description: Bestimmt, ob eine Sicherheits-ID (SID) des Prinzipals mit jedem Ereignis eingeschlossen werden soll, das in den Kanal geschrieben wird.
ms.assetid: 3ce176a3-9e21-4646-8c99-7beb687e6847
keywords:
- SIDType-Element EventLog
topic_type:
- apiref
api_name:
- sidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5d65e1ade4ded95b070b45de9462f6aee2c60ac0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342218"
---
# <a name="sidtype-channelpublishingtype-element"></a><span data-ttu-id="25ff1-104">SIDType (channelpublishingtype)-Element</span><span class="sxs-lookup"><span data-stu-id="25ff1-104">sidType (ChannelPublishingType) Element</span></span>

<span data-ttu-id="25ff1-105">Bestimmt, ob eine Sicherheits-ID (SID) des Prinzipals mit jedem Ereignis eingeschlossen werden soll, das in den Kanal geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="25ff1-105">Determines whether to include a security identifier (SID) of the principal with each event written to the channel.</span></span>

``` syntax
<xs:element name="sidType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="None"
             />
            <xs:enumeration
                value="Publishing"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="25ff1-106">Das Element " **SIDType** " wird vom komplexen Typ " [**channelpublishingtype**](eventmanifestschema-channelpublishingtype-complextype.md) " definiert.</span><span class="sxs-lookup"><span data-stu-id="25ff1-106">The **sidType** element is defined by the [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="25ff1-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25ff1-107">Requirements</span></span>



| <span data-ttu-id="25ff1-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25ff1-108">Requirement</span></span> | <span data-ttu-id="25ff1-109">Wert</span><span class="sxs-lookup"><span data-stu-id="25ff1-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="25ff1-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="25ff1-110">Minimum supported client</span></span><br/> | <span data-ttu-id="25ff1-111">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25ff1-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="25ff1-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="25ff1-112">Minimum supported server</span></span><br/> | <span data-ttu-id="25ff1-113">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25ff1-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="25ff1-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25ff1-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="25ff1-115">**Übergeordnetes Element**</span><span class="sxs-lookup"><span data-stu-id="25ff1-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="25ff1-116">**Veröffentlichung (channelType)**</span><span class="sxs-lookup"><span data-stu-id="25ff1-116">**publishing (ChannelType)**</span></span>](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





