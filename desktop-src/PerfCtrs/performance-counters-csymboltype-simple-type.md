---
description: 'Einfacher CSymbolType-Typ (Leistungsindikatoren): Definiert einen gültigen C/C++-Symbolnamen.'
ms.assetid: 75f74a16-0be4-466b-a88d-247c8c94f4ce
title: Einfacher CSymbolType-Typ (Leistungsindikatoren)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0771bb1dffc006abf8e02e6c391278f7d0b03f11
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084228"
---
# <a name="csymboltype-simple-type-performance-counters"></a><span data-ttu-id="9a167-103">Einfacher CSymbolType-Typ (Leistungsindikatoren)</span><span class="sxs-lookup"><span data-stu-id="9a167-103">CSymbolType Simple Type (Performance Counters)</span></span>

<span data-ttu-id="9a167-104">Definiert einen gültigen C/C++-Symbolnamen.</span><span class="sxs-lookup"><span data-stu-id="9a167-104">Defines a valid C/C++ symbol name.</span></span>

``` syntax
<xs:simpleType name="CSymbolType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="()|([_a-zA-Z][_0-9a-zA-Z]*)"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="9a167-105">Muster</span><span class="sxs-lookup"><span data-stu-id="9a167-105">Patterns</span></span>

<span data-ttu-id="9a167-106">Der einfache **CSymbolType-Typ** ist eine **xs:string-Zeichenfolge,** die durch das folgende Muster eingeschränkt ist:</span><span class="sxs-lookup"><span data-stu-id="9a167-106">The **CSymbolType** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    <span data-ttu-id="9a167-107">Der Symbolname kann leer sein oder alphanumerische Zeichen und Unterstriche enthalten.</span><span class="sxs-lookup"><span data-stu-id="9a167-107">The symbol name can be empty or contain alphanumeric characters and underscores.</span></span> <span data-ttu-id="9a167-108">Wenn Sie einen Namen angeben, muss der Name mit einem Unterstrich \_ () oder einem alphabetischen Zeichen beginnen.</span><span class="sxs-lookup"><span data-stu-id="9a167-108">If you specify a name, the name must begin with an underscore (\_) or an alphabetical character.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a167-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a167-109">Requirements</span></span>



| <span data-ttu-id="9a167-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a167-110">Requirement</span></span> | <span data-ttu-id="9a167-111">Wert</span><span class="sxs-lookup"><span data-stu-id="9a167-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9a167-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9a167-112">Minimum supported client</span></span><br/> | <span data-ttu-id="9a167-113">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a167-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9a167-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9a167-114">Minimum supported server</span></span><br/> | <span data-ttu-id="9a167-115">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a167-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




