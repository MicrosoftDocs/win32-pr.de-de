---
description: Definiert einen Zeichen foltentyp für den Namen oder die Beschreibung eines Drahtlos-LAN-Richtlinien Profils.
ms.assetid: a01e8789-3401-4e58-b733-2ec95fc895b6
title: einfacher nametype-Typ (LAN_policy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8a2c0bdf281e27ba7a85271fe7777076ada9ff2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363751"
---
# <a name="nametype-simple-type-lan_policy"></a><span data-ttu-id="a4763-103">einfacher nametype-Typ (LAN_policy)</span><span class="sxs-lookup"><span data-stu-id="a4763-103">nameType Simple Type (LAN_policy)</span></span>

<span data-ttu-id="a4763-104">Der einfache nametype-Typ definiert einen Zeichen foltentyp für den Namen oder die Beschreibung eines Drahtlos-LAN-Richtlinien Profils.</span><span class="sxs-lookup"><span data-stu-id="a4763-104">The nameType simple type defines a string type for either the name or the description of a wireless LAN policy profile.</span></span> <span data-ttu-id="a4763-105">Namen und Beschreibungen sind Zeichen folgen, die mindestens ein Zeichen lang und höchstens 255 Zeichen lang sind.</span><span class="sxs-lookup"><span data-stu-id="a4763-105">Names and descriptions are strings that are at least one character long and at most 255 characters long.</span></span>

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="string"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="255"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="a4763-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4763-106">Requirements</span></span>



| <span data-ttu-id="a4763-107">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4763-107">Requirement</span></span> | <span data-ttu-id="a4763-108">Wert</span><span class="sxs-lookup"><span data-stu-id="a4763-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a4763-109">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a4763-109">Minimum supported client</span></span><br/> | <span data-ttu-id="a4763-110">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a4763-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a4763-111">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a4763-111">Minimum supported server</span></span><br/> | <span data-ttu-id="a4763-112">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a4763-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




