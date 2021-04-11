---
title: propputref-Attribut
description: Das Attribut \ propputref \ gibt eine Eigenschafts Einstellungs Funktion an, die einen Verweis anstelle eines Werts verwendet.
ms.assetid: 84f1cd08-3c42-4a6d-bb1d-0bfd3f4c33f2
keywords:
- propputref-Attribut-Mittel l
topic_type:
- apiref
api_name:
- propputref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead5ccf7f9dc6a59580b7c3e3576f3c7503ccafc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948617"
---
# <a name="propputref-attribute"></a><span data-ttu-id="0c6d8-104">propputref-Attribut</span><span class="sxs-lookup"><span data-stu-id="0c6d8-104">propputref attribute</span></span>

<span data-ttu-id="0c6d8-105">Das **\[ PROPPUTREF \]** -Attribut gibt eine Eigenschafts Einstellungs Funktion an, die einen Verweis anstelle eines Werts verwendet.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-105">The **\[propputref\]** attribute specifies a property-setting function that uses a reference instead of a value.</span></span>

``` syntax
[propputref [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a><span data-ttu-id="0c6d8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c6d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c6d8-107">*optionale-Property-Attribute*</span><span class="sxs-lookup"><span data-stu-id="0c6d8-107">*optional-property-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="0c6d8-108">NULL oder mehr Eigenschafts Attribute.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-108">Zero or more property attributes.</span></span>

</dd> <dt>

<span data-ttu-id="0c6d8-109">*Rückgabetyp*</span><span class="sxs-lookup"><span data-stu-id="0c6d8-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="0c6d8-110">Der Typ der Daten, die von der Remote Prozedur zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-110">The type of the data returned by the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="0c6d8-111">*function-name*</span><span class="sxs-lookup"><span data-stu-id="0c6d8-111">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="0c6d8-112">Der Name der Remote Prozedur.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-112">The name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="0c6d8-113">*parameters*</span><span class="sxs-lookup"><span data-stu-id="0c6d8-113">*parameters*</span></span> 
</dt> <dd>

<span data-ttu-id="0c6d8-114">NULL oder mehr Parameter für die Remote Prozedur.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-114">Zero or more parameters to the remote procedure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c6d8-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c6d8-115">Remarks</span></span>

<span data-ttu-id="0c6d8-116">Eine Funktion, die über das **\[ PROPPUTREF \]** -Attribut verfügt, muss auch, als letzten Parameter, einen Zeiger **\[** [**mit dem in**](in.md) -Attribut aufweisen **\]** .</span><span class="sxs-lookup"><span data-stu-id="0c6d8-116">A function that has the **\[propputref\]** attribute must also have, as its last parameter, a pointer that has the **\[**[**in**](in.md)**\]** attribute.</span></span>

<span data-ttu-id="0c6d8-117">Die-Eigenschaft muss den gleichen Namen wie die Funktion aufweisen.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-117">The property must have the same name as the function.</span></span> <span data-ttu-id="0c6d8-118">**\[** Für eine Funktion kann höchstens ein [**propget**](propget.md) **\]** -, **\[** [**PROPPUT**](propput.md) **\]** -und **\[ PROPPUTREF \]** -Attribut angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-118">At most, one of **\[**[**propget**](propget.md)**\]**, **\[**[**propput**](propput.md)**\]** and **\[propputref\]** attributes can be specified for a function.</span></span>

### <a name="flags"></a><span data-ttu-id="0c6d8-119">Flags</span><span class="sxs-lookup"><span data-stu-id="0c6d8-119">Flags</span></span>

<span data-ttu-id="0c6d8-120">\_propertyputref aufrufen</span><span class="sxs-lookup"><span data-stu-id="0c6d8-120">INVOKE\_PROPERTYPUTREF</span></span>

## <a name="examples"></a><span data-ttu-id="0c6d8-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0c6d8-121">Examples</span></span>

``` syntax
interface InMyFace : IDispatch 
{
    [propget, 
     helpstring("A meaningful comment."), 
     id(1)] HRESULT Method2([out, retval] YourInterface** ReturnVal); 
    [propputref, 
     helpstring("Another meaningful comment."), 
     id(1)] HRESULT Method2([in] YourPoint* Point);
}
```

## <a name="see-also"></a><span data-ttu-id="0c6d8-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0c6d8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c6d8-123">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="0c6d8-123">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="0c6d8-124">**in**</span><span class="sxs-lookup"><span data-stu-id="0c6d8-124">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="0c6d8-125">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="0c6d8-125">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="0c6d8-126">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="0c6d8-126">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="0c6d8-127">**propget**</span><span class="sxs-lookup"><span data-stu-id="0c6d8-127">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="0c6d8-128">**propput**</span><span class="sxs-lookup"><span data-stu-id="0c6d8-128">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="0c6d8-129">**FUNCFLAGS**</span><span class="sxs-lookup"><span data-stu-id="0c6d8-129">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 