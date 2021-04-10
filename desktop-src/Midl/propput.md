---
title: propput-Attribut
description: Das Attribut \ propput \ gibt eine Eigenschafts Einstellungs Funktion an. Die-Eigenschaft muss den gleichen Namen wie die Funktion aufweisen.
ms.assetid: ffd8af15-42a4-4852-a29b-1fc66f673978
keywords:
- propput-Attribut-Mittel l
topic_type:
- apiref
api_name:
- propput
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79bf5520a3f4f4872801145064f49a8108cf602a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101502"
---
# <a name="propput-attribute"></a><span data-ttu-id="3eb2a-105">propput-Attribut</span><span class="sxs-lookup"><span data-stu-id="3eb2a-105">propput attribute</span></span>

<span data-ttu-id="3eb2a-106">Das **\[ PROPPUT \]** -Attribut gibt eine Eigenschafts Einstellungs Funktion an.</span><span class="sxs-lookup"><span data-stu-id="3eb2a-106">The **\[propput\]** attribute specifies a property-setting function.</span></span> <span data-ttu-id="3eb2a-107">Die-Eigenschaft muss den gleichen Namen wie die Funktion aufweisen *.*</span><span class="sxs-lookup"><span data-stu-id="3eb2a-107">The property must have the same name as the function *.*</span></span>

``` syntax
[propput [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a><span data-ttu-id="3eb2a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3eb2a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3eb2a-109">*optionale-Property-Attribute*</span><span class="sxs-lookup"><span data-stu-id="3eb2a-109">*optional-property-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="3eb2a-110">NULL oder mehr Eigenschafts Attribute.</span><span class="sxs-lookup"><span data-stu-id="3eb2a-110">Zero or more property attributes.</span></span>

</dd> <dt>

<span data-ttu-id="3eb2a-111">*Rückgabetyp*</span><span class="sxs-lookup"><span data-stu-id="3eb2a-111">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="3eb2a-112">Der Typ der Daten, die von der Remote Prozedur zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3eb2a-112">The type of the data returned by the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="3eb2a-113">*function-name*</span><span class="sxs-lookup"><span data-stu-id="3eb2a-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="3eb2a-114">Der Name der Remote Prozedur.</span><span class="sxs-lookup"><span data-stu-id="3eb2a-114">The name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="3eb2a-115">*parameters*</span><span class="sxs-lookup"><span data-stu-id="3eb2a-115">*parameters*</span></span> 
</dt> <dd>

<span data-ttu-id="3eb2a-116">NULL oder mehr Parameter für die Remote Prozedur.</span><span class="sxs-lookup"><span data-stu-id="3eb2a-116">Zero or more parameters to the remote procedure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3eb2a-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3eb2a-117">Remarks</span></span>

<span data-ttu-id="3eb2a-118">Eine Funktion, die über das **\[ PROPPUT \]** -Attribut verfügt, muss ebenfalls als letzten Parameter einen Parameter haben, der das **\[** [**in**](in.md) - **\]** Attribut aufweist.</span><span class="sxs-lookup"><span data-stu-id="3eb2a-118">A function that has the **\[propput\]** attribute must also have, as its last parameter, a parameter that has the **\[**[**in**](in.md)**\]** attribute.</span></span>

<span data-ttu-id="3eb2a-119">**\[** Für eine Funktion kann höchstens ein [**propget**](propget.md) **\]** -, **\[ PROPPUT \]** -und **\[** [**PROPPUTREF**](propputref.md) -Konstruktor **\]** angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3eb2a-119">At most, one of **\[**[**propget**](propget.md)**\]**, **\[propput\]** and **\[**[**propputref**](propputref.md)**\]** can be specified for a function.</span></span>

<span data-ttu-id="3eb2a-120">Wenn das **\[** [**LCID**](lcid.md) - **\]** Attribut in der Parameterliste einer Funktion verwendet wird, die einen Parameter mit dem **\[ PROPPUT \]** -Attribut enthält, muss der **\[ LCID \]** -Parameter den Wert Second bis The Last aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3eb2a-120">If the **\[**[**lcid**](lcid.md)**\]** attribute is used in the parameter list of a function that contains a parameter with the **\[propput\]** attribute, the **\[lcid\]** parameter must be second to the last.</span></span>

### <a name="flags"></a><span data-ttu-id="3eb2a-121">Flags</span><span class="sxs-lookup"><span data-stu-id="3eb2a-121">Flags</span></span>

<span data-ttu-id="3eb2a-122">\_PropertyPut aufrufen</span><span class="sxs-lookup"><span data-stu-id="3eb2a-122">INVOKE\_PROPERTYPUT</span></span>

## <a name="examples"></a><span data-ttu-id="3eb2a-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3eb2a-123">Examples</span></span>

``` syntax
interface InMyFace : IDispatch                         
{
    [propget, 
     helpstring("A meaningful comment.")] HRESULT Method1(
         [out, retval] int* ReturnVal); 

    [propput, 
     helpstring("Another meaningful comment.")] HRESULT Method1(
         [in] int Value);
}
```

## <a name="see-also"></a><span data-ttu-id="3eb2a-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3eb2a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3eb2a-125">Unterschiede zwischen "Mittel l" und "MkTypLib"</span><span class="sxs-lookup"><span data-stu-id="3eb2a-125">Differences Between MIDL and MKTYPLIB</span></span>](differences-between-midl-and-mktyplib.md)
</dt> <dt>

[<span data-ttu-id="3eb2a-126">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="3eb2a-126">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="3eb2a-127">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="3eb2a-127">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="3eb2a-128">**propget**</span><span class="sxs-lookup"><span data-stu-id="3eb2a-128">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="3eb2a-129">**propputref**</span><span class="sxs-lookup"><span data-stu-id="3eb2a-129">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="3eb2a-130">**FUNCFLAGS**</span><span class="sxs-lookup"><span data-stu-id="3eb2a-130">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 