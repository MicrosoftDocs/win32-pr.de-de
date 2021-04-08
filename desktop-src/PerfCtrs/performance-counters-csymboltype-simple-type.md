---
description: Definiert einen gültigen C/C++-Symbolnamen.
ms.assetid: 75f74a16-0be4-466b-a88d-247c8c94f4ce
title: Einfacher csymboltype-Typ (Leistungsindikatoren)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 418b5119046a89d93814ed8ac8bd427dc554bf26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959754"
---
# <a name="csymboltype-simple-type-performance-counters"></a><span data-ttu-id="48702-103">Einfacher csymboltype-Typ (Leistungsindikatoren)</span><span class="sxs-lookup"><span data-stu-id="48702-103">CSymbolType Simple Type (Performance Counters)</span></span>

<span data-ttu-id="48702-104">Definiert einen gültigen C/C++-Symbolnamen.</span><span class="sxs-lookup"><span data-stu-id="48702-104">Defines a valid C/C++ symbol name.</span></span>

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

## <a name="patterns"></a><span data-ttu-id="48702-105">Muster</span><span class="sxs-lookup"><span data-stu-id="48702-105">Patterns</span></span>

<span data-ttu-id="48702-106">Der einfache **csymboltype** -Typ ist eine **xs: String** , die durch das folgende Muster eingeschränkt ist:</span><span class="sxs-lookup"><span data-stu-id="48702-106">The **CSymbolType** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    <span data-ttu-id="48702-107">Der Symbol Name kann leer sein oder alphanumerische Zeichen und Unterstriche enthalten.</span><span class="sxs-lookup"><span data-stu-id="48702-107">The symbol name can be empty or contain alphanumeric characters and underscores.</span></span> <span data-ttu-id="48702-108">Wenn Sie einen Namen angeben, muss der Name mit einem Unterstrich ( \_ ) oder einem alphabetischen Zeichen beginnen.</span><span class="sxs-lookup"><span data-stu-id="48702-108">If you specify a name, the name must begin with an underscore (\_) or an alphabetical character.</span></span>

## <a name="requirements"></a><span data-ttu-id="48702-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48702-109">Requirements</span></span>



| <span data-ttu-id="48702-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48702-110">Requirement</span></span> | <span data-ttu-id="48702-111">Wert</span><span class="sxs-lookup"><span data-stu-id="48702-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="48702-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48702-112">Minimum supported client</span></span><br/> | <span data-ttu-id="48702-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48702-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="48702-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48702-114">Minimum supported server</span></span><br/> | <span data-ttu-id="48702-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48702-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




