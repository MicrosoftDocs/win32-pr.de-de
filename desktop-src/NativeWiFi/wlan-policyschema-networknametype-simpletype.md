---
description: Definiert einen Zeichen Folgentyp für Service Set Identifier (SSIDs).
ms.assetid: c9e79a3d-7d5c-4320-ade2-40124de00920
title: einfacher networknametype-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkNameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6b6463644e1bd174be256d51b34ae2ae4ad9ce07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960556"
---
# <a name="networknametype-simple-type"></a><span data-ttu-id="7eea9-103">einfacher networknametype-Typ</span><span class="sxs-lookup"><span data-stu-id="7eea9-103">networkNameType Simple Type</span></span>

<span data-ttu-id="7eea9-104">Der einfache Typ networknametype definiert einen Zeichen Folgentyp für Service Set Identifier (SSIDs).</span><span class="sxs-lookup"><span data-stu-id="7eea9-104">The networkNameType simple type defines a string type for service set identifiers (SSIDs).</span></span> <span data-ttu-id="7eea9-105">Eine SSID ist eine Zeichenfolge, die mindestens ein Zeichen lang und höchstens 32 Zeichen lang ist.</span><span class="sxs-lookup"><span data-stu-id="7eea9-105">A SSID is a string that is at least one character long and at most 32 characters long.</span></span>

``` syntax
<xs:simpleType name="networkNameType">
    <xs:restriction
        base="string"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="32"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="7eea9-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7eea9-106">Requirements</span></span>



| <span data-ttu-id="7eea9-107">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7eea9-107">Requirement</span></span> | <span data-ttu-id="7eea9-108">Wert</span><span class="sxs-lookup"><span data-stu-id="7eea9-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7eea9-109">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7eea9-109">Minimum supported client</span></span><br/> | <span data-ttu-id="7eea9-110">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7eea9-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7eea9-111">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7eea9-111">Minimum supported server</span></span><br/> | <span data-ttu-id="7eea9-112">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7eea9-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




