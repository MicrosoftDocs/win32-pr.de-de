---
title: pfadtype simple-Typ
description: Definiert die minimale und maximale Anzahl von Zeichen für eine Zeichenfolge, die einen Dateipfad definiert.
ms.assetid: 09908f75-ba7b-4e31-877e-80fabea6bd27
keywords:
- pfadtype-Typ "Simple" Taskplaner
topic_type:
- apiref
api_name:
- pathType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a75ef7d85eba2aa39e0c3c768fec0908c7ea16b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342880"
---
# <a name="pathtype-simple-type"></a><span data-ttu-id="da38b-104">pfadtype simple-Typ</span><span class="sxs-lookup"><span data-stu-id="da38b-104">pathType Simple Type</span></span>

<span data-ttu-id="da38b-105">Definiert die minimale und maximale Anzahl von Zeichen für eine Zeichenfolge, die einen Dateipfad definiert.</span><span class="sxs-lookup"><span data-stu-id="da38b-105">Defines the minimum and maximum number of characters for a string that defines a file path.</span></span> <span data-ttu-id="da38b-106">Der Pfad darf keine leere Zeichenfolge sein und muss weniger als 260 Zeichen umfassen.</span><span class="sxs-lookup"><span data-stu-id="da38b-106">The path cannot be an empty string, and must be less than 260 characters.</span></span>

``` syntax
<xs:simpleType name="pathType">
    <xs:restriction
        base="nonEmptyString"
    >
        <xs:maxLength
            value="260"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="da38b-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da38b-107">Requirements</span></span>



| <span data-ttu-id="da38b-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da38b-108">Requirement</span></span> | <span data-ttu-id="da38b-109">Wert</span><span class="sxs-lookup"><span data-stu-id="da38b-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="da38b-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da38b-110">Minimum supported client</span></span><br/> | <span data-ttu-id="da38b-111">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da38b-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="da38b-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da38b-112">Minimum supported server</span></span><br/> | <span data-ttu-id="da38b-113">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da38b-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





