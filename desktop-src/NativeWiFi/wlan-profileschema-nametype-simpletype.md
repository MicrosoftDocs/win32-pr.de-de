---
description: Enthalten entweder den Namen oder die Beschreibung eines WLAN-Profils.
ms.assetid: cb30d76f-051f-4b90-a0e0-24088a99ca9b
title: einfacher nametype-Typ (LAN_policy) (Profil)
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
ms.openlocfilehash: e73e8bd013836767e2a943616407aea9f563fea2
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106360470"
---
# <a name="nametype-simple-type-lan_policy-for-profileschema"></a><span data-ttu-id="08869-103">nametype Simple Type (LAN_policy) für profileschema</span><span class="sxs-lookup"><span data-stu-id="08869-103">nameType Simple Type (LAN_policy) for profileschema</span></span>

<span data-ttu-id="08869-104">Der einfache nametype-Typ kann entweder den Namen oder eine Beschreibung eines WLAN-Profils enthalten.</span><span class="sxs-lookup"><span data-stu-id="08869-104">The nameType simple type can contain either the name or a description of a wireless LAN profile.</span></span> <span data-ttu-id="08869-105">Dieser Zeichen folgen Wert muss zwischen 1 und 255 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="08869-105">This string value must be between 1 and 255 characters long.</span></span>

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

## <a name="requirements"></a><span data-ttu-id="08869-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08869-106">Requirements</span></span>



| <span data-ttu-id="08869-107">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08869-107">Requirement</span></span> | <span data-ttu-id="08869-108">Wert</span><span class="sxs-lookup"><span data-stu-id="08869-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="08869-109">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="08869-109">Minimum supported client</span></span><br/> | <span data-ttu-id="08869-110">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08869-110">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="08869-111">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="08869-111">Minimum supported server</span></span><br/> | <span data-ttu-id="08869-112">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08869-112">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="08869-113">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="08869-113">Redistributable</span></span><br/>          | <span data-ttu-id="08869-114">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="08869-114">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



 

 




