---
title: propget-Attribut
description: Das Attribut \ Propget \ gibt eine eigenschaftenaccessorfunktion an. Die-Eigenschaft muss den gleichen Namen wie die Funktion aufweisen.
ms.assetid: 0b76ece3-e19b-4c80-883c-ff414bc2e435
keywords:
- Propget-Attribut-Mittel l
topic_type:
- apiref
api_name:
- propget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6337409e021670c282400d38b97543687fa81c2a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038834"
---
# <a name="propget-attribute"></a><span data-ttu-id="683e0-105">propget-Attribut</span><span class="sxs-lookup"><span data-stu-id="683e0-105">propget attribute</span></span>

<span data-ttu-id="683e0-106">Das **\[ propget \]** -Attribut gibt eine eigenschaftenaccessorfunktion an.</span><span class="sxs-lookup"><span data-stu-id="683e0-106">The **\[propget\]** attribute specifies a property accessor function.</span></span> <span data-ttu-id="683e0-107">Die-Eigenschaft muss den gleichen Namen wie die Funktion aufweisen.</span><span class="sxs-lookup"><span data-stu-id="683e0-107">The property must have the same name as the function.</span></span>

``` syntax
[propget [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a><span data-ttu-id="683e0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="683e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="683e0-109">*optionale-Property-Attribute*</span><span class="sxs-lookup"><span data-stu-id="683e0-109">*optional-property-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="683e0-110">NULL oder mehr Eigenschafts Attribute.</span><span class="sxs-lookup"><span data-stu-id="683e0-110">Zero or more property attributes.</span></span>

</dd> <dt>

<span data-ttu-id="683e0-111">*Rückgabetyp*</span><span class="sxs-lookup"><span data-stu-id="683e0-111">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="683e0-112">Der Typ der Daten, die von der Remote Prozedur zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="683e0-112">The type of the data returned by the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="683e0-113">*function-name*</span><span class="sxs-lookup"><span data-stu-id="683e0-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="683e0-114">Der Name der Remote Prozedur.</span><span class="sxs-lookup"><span data-stu-id="683e0-114">The name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="683e0-115">*parameters*</span><span class="sxs-lookup"><span data-stu-id="683e0-115">*parameters*</span></span> 
</dt> <dd>

<span data-ttu-id="683e0-116">NULL oder mehr Parameter für die Remote Prozedur.</span><span class="sxs-lookup"><span data-stu-id="683e0-116">Zero or more parameters to the remote procedure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="683e0-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="683e0-117">Remarks</span></span>

<span data-ttu-id="683e0-118">Eine Funktion, die über das Propget-Attribut verfügt, sollte auch, als letzten Parameter, einen Zeigertyp mit den Attributen " **\[** [**out**](out-idl.md) " **\]** und " **\[** [**retval**](retval.md) **\]** " aufweisen.</span><span class="sxs-lookup"><span data-stu-id="683e0-118">A function that has the propget attribute should also have, as its last parameter, a pointer type with the **\[**[**out**](out-idl.md)**\]** and **\[**[**retval**](retval.md)**\]** attributes.</span></span> <span data-ttu-id="683e0-119">Wenn der letzte Parameter nicht die \[ Attribute out, retval hat \] , wird der Rückgabewert der Funktion als " \[ out", "retval"-Parameter behandelt \] .</span><span class="sxs-lookup"><span data-stu-id="683e0-119">If the last parameter does not have the \[out, retval\] attributes, the return value of the function is treated as an \[out, retval\] parameter.</span></span> <span data-ttu-id="683e0-120">Beispielsweise eine Funktion mit dem Prototyp</span><span class="sxs-lookup"><span data-stu-id="683e0-120">For example, a function with the prototype</span></span>

``` syntax
[propget] short MyFunction([in] long aLongValue);
```

<span data-ttu-id="683e0-121">wird behandelt als</span><span class="sxs-lookup"><span data-stu-id="683e0-121">is treated as</span></span>

``` syntax
[propget] HRESULT MyFunction([in] long aLongValue, [out,retval] short *outValue);
```

<span data-ttu-id="683e0-122">Für eine Funktion kann höchstens ein **\[ propget \]**-, **\[** [**PROPPUT**](propput.md) **\]** -und **\[** [**PROPPUTREF**](propputref.md) -Konstruktor **\]** angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="683e0-122">At most, one of **\[propget\]**, **\[**[**propput**](propput.md)**\]**, and **\[**[**propputref**](propputref.md)**\]** can be specified for a function.</span></span>

<span data-ttu-id="683e0-123">Wenn das **\[** [**LCID**](lcid.md) - **\]** Attribut in der Parameterliste einer Funktion verwendet wird, die einen Parameter mit dem **\[** [**PROPPUT**](propput.md) - **\]** Attribut enthält, muss der **\[ LCID \]** -Parameter den Wert Second bis The Last aufweisen.</span><span class="sxs-lookup"><span data-stu-id="683e0-123">If the **\[**[**lcid**](lcid.md)**\]** attribute is used in the parameter list of a function that contains a parameter with the **\[**[**propput**](propput.md)**\]** attribute, the **\[lcid\]** parameter must be second to the last.</span></span>

### <a name="flags"></a><span data-ttu-id="683e0-124">Flags</span><span class="sxs-lookup"><span data-stu-id="683e0-124">Flags</span></span>

<span data-ttu-id="683e0-125">\_PropertyGet aufrufen</span><span class="sxs-lookup"><span data-stu-id="683e0-125">INVOKE\_PROPERTYGET</span></span>

## <a name="examples"></a><span data-ttu-id="683e0-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="683e0-126">Examples</span></span>

``` syntax
interface MyInterface : IDispatch                         
{                
    [propget, 
     helpstring("A meaningful comment.")] HRESULT Method1(
         [out, retval] int* ReturnVal); 

    [propput, 
     helpstring("Another meaningful comment.")] HRESULT Method1(
         [in] int Value);
        
    [propget, 
     helpstring("A meaningful comment."), id(1)] HRESULT Method2(
         [out, retval] YourInterface** ReturnVal); 

    [propputref, 
     helpstring("Another meaningful comment."), 
     id(1)] HRESULT Method2([in] YourPoint* Point);
}                 
```

## <a name="see-also"></a><span data-ttu-id="683e0-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="683e0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="683e0-128">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="683e0-128">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="683e0-129">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="683e0-129">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="683e0-130">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="683e0-130">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="683e0-131">**vorgenommen**</span><span class="sxs-lookup"><span data-stu-id="683e0-131">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="683e0-132">**retval**</span><span class="sxs-lookup"><span data-stu-id="683e0-132">**retval**</span></span>](retval.md)
</dt> <dt>

[<span data-ttu-id="683e0-133">**propput**</span><span class="sxs-lookup"><span data-stu-id="683e0-133">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="683e0-134">**propputref**</span><span class="sxs-lookup"><span data-stu-id="683e0-134">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="683e0-135">**FUNCFLAGS**</span><span class="sxs-lookup"><span data-stu-id="683e0-135">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 