---
title: Einfacher csymboltype-Typ (Windows-Ereignisprotokoll)
description: Definiert einen gültigen C/C++-Symbolnamen.
ms.assetid: d19827b6-2b61-4d75-ac9d-56a384b0cc4b
keywords:
- Csymboltype Simple Event Log-Typ
topic_type:
- apiref
api_name:
- CSymbolType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 67b0ccb7c573aa4d71c038f9133cea7c95cdfbd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340328"
---
# <a name="csymboltype-simple-type-windows-event-log"></a><span data-ttu-id="834e1-104">Einfacher csymboltype-Typ (Windows-Ereignisprotokoll)</span><span class="sxs-lookup"><span data-stu-id="834e1-104">CSymbolType Simple Type (Windows Event Log)</span></span>

<span data-ttu-id="834e1-105">Definiert einen gültigen C/C++-Symbolnamen.</span><span class="sxs-lookup"><span data-stu-id="834e1-105">Defines a valid C/C++ symbol name.</span></span>

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

## <a name="patterns"></a><span data-ttu-id="834e1-106">Muster</span><span class="sxs-lookup"><span data-stu-id="834e1-106">Patterns</span></span>

<span data-ttu-id="834e1-107">Der einfache **csymboltype** -Typ ist eine **xs: String** , die durch das folgende Muster eingeschränkt ist:</span><span class="sxs-lookup"><span data-stu-id="834e1-107">The **CSymbolType** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    <span data-ttu-id="834e1-108">Der Symbol Name kann leer sein oder alphanumerische Zeichen und Unterstriche enthalten.</span><span class="sxs-lookup"><span data-stu-id="834e1-108">The symbol name can be empty or contain alphanumeric characters and underscores.</span></span> <span data-ttu-id="834e1-109">Wenn der Name leer ist, generiert der Nachrichten Compiler den Symbolnamen.</span><span class="sxs-lookup"><span data-stu-id="834e1-109">If the name is empty, the message compiler will generate the symbol name.</span></span> <span data-ttu-id="834e1-110">Wenn Sie einen Namen angeben, muss der Name mit einem Unterstrich ( \_ ) oder einem alphabetischen Zeichen beginnen.</span><span class="sxs-lookup"><span data-stu-id="834e1-110">If you specify a name, the name must begin with an underscore (\_) or an alphabetical character.</span></span>

## <a name="remarks"></a><span data-ttu-id="834e1-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="834e1-111">Remarks</span></span>

<span data-ttu-id="834e1-112">Wenn der Symbol Name leer ist, verwendet der Nachrichten Compiler das **Name** -Attribut des-Elements, das Sie definieren, um den Symbolnamen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="834e1-112">If the symbol name is empty, the message compiler uses the **name** attribute of the element that you are defining to generate the symbol name.</span></span> <span data-ttu-id="834e1-113">Der Compiler ersetzt alle nicht alphanumerischen Zeichen und vorangestellten Ziffern durch Unterstriche.</span><span class="sxs-lookup"><span data-stu-id="834e1-113">The compiler replaces any non-alphanumeric characters and leading digits with underscores.</span></span> <span data-ttu-id="834e1-114">Wenn das **Name** -Attribut des Kanals z. b. Microsoft-Windows-SampleProvider/Operational ist, verwendet der Compiler Microsoft \_ Windows \_ Sample Provider \_ Operational als Symbolnamen.</span><span class="sxs-lookup"><span data-stu-id="834e1-114">For example, if the channel's **name** attribute is Microsoft-Windows-SampleProvider/Operational, the compiler would use Microsoft\_Windows\_SampleProvider\_Operational as the symbol name.</span></span>

## <a name="requirements"></a><span data-ttu-id="834e1-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="834e1-115">Requirements</span></span>



| <span data-ttu-id="834e1-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="834e1-116">Requirement</span></span> | <span data-ttu-id="834e1-117">Wert</span><span class="sxs-lookup"><span data-stu-id="834e1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="834e1-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="834e1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="834e1-119">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="834e1-119">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="834e1-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="834e1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="834e1-121">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="834e1-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





