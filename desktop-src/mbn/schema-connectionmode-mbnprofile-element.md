---
description: Gibt die Einstellung für die automatische Verbindung an, die für ein mobiles Breitband Gerät verwendet werden soll.
ms.assetid: 789016d5-47f1-4506-bcb9-1a4019d236fd
title: ConnectionMode (mbnprofile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConnectionMode
api_type:
- Schema
ms.openlocfilehash: d9c92227e26bb8858aef28d2f030ac2f84bed06d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958909"
---
# <a name="connectionmode-mbnprofile-element"></a><span data-ttu-id="96905-103">ConnectionMode (mbnprofile)-Element</span><span class="sxs-lookup"><span data-stu-id="96905-103">ConnectionMode (MBNProfile) Element</span></span>

<span data-ttu-id="96905-104">Das **ConnectionMode (mbnprofile)** -Element gibt die Einstellung für die automatische Verbindung an, die für ein mobiles Breitband Gerät verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="96905-104">The **ConnectionMode (MBNProfile)** element specifies the auto connection setting to be used for a Mobile Broadband device.</span></span>

<span data-ttu-id="96905-105">Dieses Element kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="96905-105">This element can have one of the following values.</span></span>



| <span data-ttu-id="96905-106">Wert</span><span class="sxs-lookup"><span data-stu-id="96905-106">Value</span></span>       | <span data-ttu-id="96905-107">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="96905-107">Meaning</span></span>                                                                |
|-------------|------------------------------------------------------------------------|
| <span data-ttu-id="96905-108">Manual</span><span class="sxs-lookup"><span data-stu-id="96905-108">"manual"</span></span>    | <span data-ttu-id="96905-109">Nie automatisch eine Verbindung mit dem Netzwerk herstellen.</span><span class="sxs-lookup"><span data-stu-id="96905-109">Never automatically connect to the network.</span></span>                            |
| <span data-ttu-id="96905-110">automatisch</span><span class="sxs-lookup"><span data-stu-id="96905-110">"auto"</span></span>      | <span data-ttu-id="96905-111">Immer automatisch eine Verbindung mit dem Netzwerk herstellen.</span><span class="sxs-lookup"><span data-stu-id="96905-111">Always automatically connect to the network.</span></span>                           |
| <span data-ttu-id="96905-112">"Auto-Home"</span><span class="sxs-lookup"><span data-stu-id="96905-112">"auto-home"</span></span> | <span data-ttu-id="96905-113">Automatische Verbindung mit dem Netzwerk, außer wenn es sich um ein roamingnetzwerk handelt.</span><span class="sxs-lookup"><span data-stu-id="96905-113">Automatically connect to the network except when in a roaming network.</span></span> |



 

<span data-ttu-id="96905-114">Dieses Element kann maximal ein Vorkommen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="96905-114">This element can have a maximum of one occurrence.</span></span>

<span data-ttu-id="96905-115">Dies ist ein erforderliches Element.</span><span class="sxs-lookup"><span data-stu-id="96905-115">This is a required element.</span></span>

``` syntax
<xs:element name="ConnectionMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="manual"
             />
            <xs:enumeration
                value="auto"
             />
            <xs:enumeration
                value="auto-home"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="96905-116">Das **ConnectionMode** -Element wird durch das [**mbnprofile**](schema-mbnprofile-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="96905-116">The **ConnectionMode** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="96905-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96905-117">Requirements</span></span>



| <span data-ttu-id="96905-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96905-118">Requirement</span></span> | <span data-ttu-id="96905-119">Wert</span><span class="sxs-lookup"><span data-stu-id="96905-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="96905-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="96905-120">Minimum supported client</span></span><br/> | <span data-ttu-id="96905-121">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="96905-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="96905-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="96905-122">Minimum supported server</span></span><br/> | <span data-ttu-id="96905-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="96905-123">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="96905-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96905-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="96905-125">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="96905-125">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="96905-126">**Mbnprofile**</span><span class="sxs-lookup"><span data-stu-id="96905-126">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="96905-127">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="96905-127">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="96905-128">**Mbnprofile**</span><span class="sxs-lookup"><span data-stu-id="96905-128">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




