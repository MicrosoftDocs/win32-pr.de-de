---
description: Definiert den Typ, der gültige Werte für das Type-Attribut für das Margin-Element enthält.
ms.assetid: 5448ead5-0249-4cc7-9f2a-d2181e2af734
title: Margintypetype simple-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MarginTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4e8a09e98611fabc54a029c9cac9cb37dfc1373f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218044"
---
# <a name="margintypetype-simple-type"></a><span data-ttu-id="28a0d-103">Margintypetype simple-Typ</span><span class="sxs-lookup"><span data-stu-id="28a0d-103">MarginTypeType Simple Type</span></span>

<span data-ttu-id="28a0d-104">Definiert den Typ, der gültige Werte für das **Type** -Attribut für das [Margin-Element](margin-element.md)enthält.</span><span class="sxs-lookup"><span data-stu-id="28a0d-104">Defines the type that contains valid values for the **Type** attribute for the [Margin element](margin-element.md).</span></span>

``` syntax
<xs:simpleType name="MarginTypeType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="Left|Right"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="28a0d-105">Muster</span><span class="sxs-lookup"><span data-stu-id="28a0d-105">Patterns</span></span>

<span data-ttu-id="28a0d-106">Der einfache Typ von **margintypetype** ist eine **Zeichenfolge** , die durch das folgende Muster eingeschränkt ist:</span><span class="sxs-lookup"><span data-stu-id="28a0d-106">The **MarginTypeType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `Left|Right`

## <a name="remarks"></a><span data-ttu-id="28a0d-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28a0d-107">Remarks</span></span>

<span data-ttu-id="28a0d-108">Gültige Werte für das **Type** -Attribut für das [Margin-Element](margin-element.md) sind "Left" und "Right".</span><span class="sxs-lookup"><span data-stu-id="28a0d-108">The valid values for the **Type** attribute for the [Margin element](margin-element.md) are "Left" and "Right".</span></span>

## <a name="requirements"></a><span data-ttu-id="28a0d-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28a0d-109">Requirements</span></span>



| <span data-ttu-id="28a0d-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28a0d-110">Requirement</span></span> | <span data-ttu-id="28a0d-111">Wert</span><span class="sxs-lookup"><span data-stu-id="28a0d-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="28a0d-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="28a0d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="28a0d-113">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="28a0d-113">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="28a0d-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="28a0d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="28a0d-115">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="28a0d-115">None supported</span></span><br/>                                     |



 

 




