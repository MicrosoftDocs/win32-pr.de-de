---
description: Definiert einen Globally Unique Identifier Typ im Registrierungs Format.
ms.assetid: 2be73c57-b6b6-46ab-93e1-d70f8655c30e
title: Guidtype Simple Type (Leistungsindikatoren)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 758509a564c26db493fa2e9ed971aba71878cdbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865099"
---
# <a name="guidtype-simple-type-performance-counters"></a><span data-ttu-id="2d0ad-103">Guidtype Simple Type (Leistungsindikatoren)</span><span class="sxs-lookup"><span data-stu-id="2d0ad-103">GUIDType Simple Type (Performance Counters)</span></span>

<span data-ttu-id="2d0ad-104">Definiert einen Globally Unique Identifier Typ im Registrierungs Format.</span><span class="sxs-lookup"><span data-stu-id="2d0ad-104">Defines a globally unique identifier type, in Registry format.</span></span>

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="2d0ad-105">Muster</span><span class="sxs-lookup"><span data-stu-id="2d0ad-105">Patterns</span></span>

<span data-ttu-id="2d0ad-106">Der einfache **guidtype** -Typ ist eine **xs: String** , die durch das folgende Muster eingeschränkt ist:</span><span class="sxs-lookup"><span data-stu-id="2d0ad-106">The **GUIDType** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    <span data-ttu-id="2d0ad-107">Der Wert muss ein Globally Unique Identifier Typ im Registrierungs Format sein.</span><span class="sxs-lookup"><span data-stu-id="2d0ad-107">The value must be a globally unique identifier type in Registry format.</span></span> <span data-ttu-id="2d0ad-108">Beispiel: {5b2fc63a-8af4-44cb-960c-aefdced908d6}.</span><span class="sxs-lookup"><span data-stu-id="2d0ad-108">For example, {5b2fc63a-8af4-44cb-960c-aefdced908d6}.</span></span> <span data-ttu-id="2d0ad-109">Verwenden Sie GUIDGen.exe oder UUIDGen.exe, um eine GUID zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2d0ad-109">Use GUIDGen.exe or UUIDGen.exe to create a GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d0ad-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d0ad-110">Requirements</span></span>



| <span data-ttu-id="2d0ad-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d0ad-111">Requirement</span></span> | <span data-ttu-id="2d0ad-112">Wert</span><span class="sxs-lookup"><span data-stu-id="2d0ad-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2d0ad-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2d0ad-113">Minimum supported client</span></span><br/> | <span data-ttu-id="2d0ad-114">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d0ad-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2d0ad-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2d0ad-115">Minimum supported server</span></span><br/> | <span data-ttu-id="2d0ad-116">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d0ad-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




