---
title: einfacher processtokensidtype-Typ
description: Definiert die möglichen Werte für das processtokensidtype (principaltype)-Element.
ms.assetid: 9db3e113-c525-4cbf-88c2-be256d641e92
keywords:
- Dateityp "processtokensidtype" Taskplaner
topic_type:
- apiref
api_name:
- processTokenSidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 13cf70534510e1aed8def9005d0c2d1eafab2a5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391760"
---
# <a name="processtokensidtype-simple-type"></a><span data-ttu-id="07272-104">einfacher processtokensidtype-Typ</span><span class="sxs-lookup"><span data-stu-id="07272-104">processTokenSidType Simple Type</span></span>

<span data-ttu-id="07272-105">Definiert die möglichen Werte für das [**processtokensidtype (principaltype)**](taskschedulerschema-processtokensidtype-principaltype-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="07272-105">Defines the possible values for the [**ProcessTokenSidType (principalType)**](taskschedulerschema-processtokensidtype-principaltype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="processTokenSidType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="None"
         />
        <xs:enumeration
            value="Unrestricted"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="07272-106">Enumerationswerte</span><span class="sxs-lookup"><span data-stu-id="07272-106">Enumeration values</span></span>

<span data-ttu-id="07272-107">Der einfache Typ **processtokensidtype** definiert die folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="07272-107">The **processTokenSidType** simple type defines the following values.</span></span>



| <span data-ttu-id="07272-108">Wert</span><span class="sxs-lookup"><span data-stu-id="07272-108">Value</span></span>        | <span data-ttu-id="07272-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07272-109">Description</span></span>                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07272-110">Keine</span><span class="sxs-lookup"><span data-stu-id="07272-110">None</span></span>         | <span data-ttu-id="07272-111">Tasks werden in einem Prozess ausgeführt, der keine Prozess Token-sid enthält (es werden keine Änderungen an der Liste der prozesstokengruppen vorgenommen).</span><span class="sxs-lookup"><span data-stu-id="07272-111">Tasks are run in a process that does not contain a process token SID (no changes will be made to the process token groups list).</span></span><br/> |
| <span data-ttu-id="07272-112">Nicht eingeschränkt</span><span class="sxs-lookup"><span data-stu-id="07272-112">Unrestricted</span></span> | <span data-ttu-id="07272-113">Eine Task-sid wird vom vollständigen Aufgaben Pfad abgeleitet und der Liste der prozesstokengruppen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="07272-113">A task SID will be derived from the full task path and will be added to the process token groups list.</span></span><br/>                           |



## <a name="requirements"></a><span data-ttu-id="07272-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07272-114">Requirements</span></span>



| <span data-ttu-id="07272-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07272-115">Requirement</span></span> | <span data-ttu-id="07272-116">Wert</span><span class="sxs-lookup"><span data-stu-id="07272-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="07272-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="07272-117">Minimum supported client</span></span><br/> | <span data-ttu-id="07272-118">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07272-118">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="07272-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="07272-119">Minimum supported server</span></span><br/> | <span data-ttu-id="07272-120">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07272-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





