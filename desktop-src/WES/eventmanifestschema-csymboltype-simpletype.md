---
title: Einfacher CSymbolType-Typ (Windows-Ereignisprotokoll)
description: 'Einfacher CSymbolType-Typ (Windows-Ereignisprotokoll): Definiert einen gültigen C/C++-Symbolnamen.'
ms.assetid: d19827b6-2b61-4d75-ac9d-56a384b0cc4b
keywords:
- Einfacher CSymbolType-Typ EventLog
topic_type:
- apiref
api_name:
- CSymbolType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e0c8c17a9f4bb7e86b573d60187ffffd55c6cb96
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090618"
---
# <a name="csymboltype-simple-type-windows-event-log"></a><span data-ttu-id="167ce-104">Einfacher CSymbolType-Typ (Windows-Ereignisprotokoll)</span><span class="sxs-lookup"><span data-stu-id="167ce-104">CSymbolType Simple Type (Windows Event Log)</span></span>

<span data-ttu-id="167ce-105">Definiert einen gültigen C/C++-Symbolnamen.</span><span class="sxs-lookup"><span data-stu-id="167ce-105">Defines a valid C/C++ symbol name.</span></span>

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

## <a name="patterns"></a><span data-ttu-id="167ce-106">Muster</span><span class="sxs-lookup"><span data-stu-id="167ce-106">Patterns</span></span>

<span data-ttu-id="167ce-107">Der **einfache CSymbolType-Typ** ist ein **xs:string-Objekt,** das durch das folgende Muster eingeschränkt ist:</span><span class="sxs-lookup"><span data-stu-id="167ce-107">The **CSymbolType** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    <span data-ttu-id="167ce-108">Der Symbolname kann leer sein oder alphanumerische Zeichen und Unterstriche enthalten.</span><span class="sxs-lookup"><span data-stu-id="167ce-108">The symbol name can be empty or contain alphanumeric characters and underscores.</span></span> <span data-ttu-id="167ce-109">Wenn der Name leer ist, generiert der Nachrichtencompiler den Symbolnamen.</span><span class="sxs-lookup"><span data-stu-id="167ce-109">If the name is empty, the message compiler will generate the symbol name.</span></span> <span data-ttu-id="167ce-110">Wenn Sie einen Namen angeben, muss der Name mit einem Unterstrich ( ) oder einem \_ alphabetischen Zeichen beginnen.</span><span class="sxs-lookup"><span data-stu-id="167ce-110">If you specify a name, the name must begin with an underscore (\_) or an alphabetical character.</span></span>

## <a name="remarks"></a><span data-ttu-id="167ce-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="167ce-111">Remarks</span></span>

<span data-ttu-id="167ce-112">Wenn der Symbolname leer ist, verwendet der Nachrichtencompiler das **Name-Attribut** des Elements, das Sie definieren, um den Symbolnamen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="167ce-112">If the symbol name is empty, the message compiler uses the **name** attribute of the element that you are defining to generate the symbol name.</span></span> <span data-ttu-id="167ce-113">Der Compiler ersetzt alle nicht alphanumerischen Zeichen und führenden Ziffern durch Unterstriche.</span><span class="sxs-lookup"><span data-stu-id="167ce-113">The compiler replaces any non-alphanumeric characters and leading digits with underscores.</span></span> <span data-ttu-id="167ce-114">Wenn das Name-Attribut  des Kanals beispielsweise Microsoft-Windows-SampleProvider/Operational ist, verwendet der Compiler Microsoft Windows SampleProvider Operational als \_ \_ \_ Symbolnamen.</span><span class="sxs-lookup"><span data-stu-id="167ce-114">For example, if the channel's **name** attribute is Microsoft-Windows-SampleProvider/Operational, the compiler would use Microsoft\_Windows\_SampleProvider\_Operational as the symbol name.</span></span>

## <a name="requirements"></a><span data-ttu-id="167ce-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="167ce-115">Requirements</span></span>



| <span data-ttu-id="167ce-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="167ce-116">Requirement</span></span> | <span data-ttu-id="167ce-117">Wert</span><span class="sxs-lookup"><span data-stu-id="167ce-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="167ce-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="167ce-118">Minimum supported client</span></span><br/> | <span data-ttu-id="167ce-119">Nur Windows \[ 7-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="167ce-119">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="167ce-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="167ce-120">Minimum supported server</span></span><br/> | <span data-ttu-id="167ce-121">Nur Windows Server 2008 \[ R2-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="167ce-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





