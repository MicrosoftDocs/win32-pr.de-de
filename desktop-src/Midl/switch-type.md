---
title: switch_type-Attribut
description: Das Attribut \ Switch \_ Type \ gibt den Typ der Variablen an, die als Union-diskriminant verwendet wird. Der Switchtyp kann ein Integer-, Zeichen-, boolescher oder Enumerationstyp sein.
ms.assetid: e4c6d33b-d4db-42b7-9d18-fd14bf1fb530
keywords:
- Switch_type Attribut-Mittel l
topic_type:
- apiref
api_name:
- switch_type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14184c5838d9f671f75536714d73c3f6ebf00a0a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857455"
---
# <a name="switch_type-attribute"></a><span data-ttu-id="2d3ce-105">Switch \_ Type-Attribut</span><span class="sxs-lookup"><span data-stu-id="2d3ce-105">switch\_type attribute</span></span>

<span data-ttu-id="2d3ce-106">Das **\[ \_ SwitchType \]** -Attribut identifiziert den Typ der Variablen, die als uniondiskriminant verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2d3ce-106">The **\[switch\_type\]** attribute identifies the type of the variable used as the union discriminant.</span></span> <span data-ttu-id="2d3ce-107">Der Switchtyp kann ein Integer-, Zeichen-, boolescher oder Enumerationstyp sein.</span><span class="sxs-lookup"><span data-stu-id="2d3ce-107">The switch type can be an integer, character, Boolean, or enumeration type.</span></span>

``` syntax
switch_type(switch-type-specifier)
```

## <a name="parameters"></a><span data-ttu-id="2d3ce-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d3ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d3ce-109">*Switch-Type-Spezifizierer*</span><span class="sxs-lookup"><span data-stu-id="2d3ce-109">*switch-type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="2d3ce-110">Gibt einen [**int**](int.md)-, [**char**](char-idl.md)-, [**Boolean**](boolean.md)-oder [**Enumeration**](enum.md) -Typ oder einen Bezeichner eines solchen Typs an.</span><span class="sxs-lookup"><span data-stu-id="2d3ce-110">Specifies an [**int**](int.md), [**char**](char-idl.md), [**Boolean**](boolean.md), or [**enum**](enum.md) type, or an identifier of such a type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2d3ce-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d3ce-111">Remarks</span></span>

<span data-ttu-id="2d3ce-112">Während das **\[ \_ SwitchType \]** -Attribut den Variablentyp identifiziert, gibt der **\[** [**Switch \_ is**](switch-is.md) - **\]** Attribut den Namen des Parameters an, der die Union-Diskriminante ist.</span><span class="sxs-lookup"><span data-stu-id="2d3ce-112">While the **\[switch\_type\]** attribute identifies the variable type, the **\[**[**switch\_is**](switch-is.md)**\]** attribute specifies the name of the parameter that is the union discriminant.</span></span> <span data-ttu-id="2d3ce-113">Das **\[ Switch \_ Type \]** -Attribut gilt für Parameter oder Member von Strukturen oder Unions.</span><span class="sxs-lookup"><span data-stu-id="2d3ce-113">The **\[switch\_type\]** attribute applies to parameters or members of structures or unions.</span></span>

<span data-ttu-id="2d3ce-114">Die Union und ihre Diskriminante müssen auf derselben logischen Ebene angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2d3ce-114">The union and its discriminant must be specified at the same logical level.</span></span> <span data-ttu-id="2d3ce-115">Wenn die Union ein Parameter ist, muss der Union-diskriminant ein anderer Parameter sein.</span><span class="sxs-lookup"><span data-stu-id="2d3ce-115">When the union is a parameter, the union discriminant must be another parameter.</span></span> <span data-ttu-id="2d3ce-116">Wenn die Union ein Feld einer Struktur ist, muss die Diskriminante ein weiteres Feld der Struktur auf derselben Ebene wie das Union-Feld sein.</span><span class="sxs-lookup"><span data-stu-id="2d3ce-116">When the union is a field of a structure, the discriminant must be another field of the structure at the same level as the union field.</span></span>

## <a name="examples"></a><span data-ttu-id="2d3ce-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d3ce-117">Examples</span></span>

``` syntax
typedef [switch_type(short)] union _WILLIE_UNION_TYPE 
{ 
    [case(24)] 
        float fMays; 
    [case(25)] 
        double dMcCovey; 
    [default] 
        ; 
} WILLIE_UNION_TYPE; 
 
typedef struct _WINNER_TYPE 
{ 
    [switch_is(sUniformNumber)] WILLIE_UNION_TYPE w; 
    short sUniformNumber; 
} WINNER_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="2d3ce-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2d3ce-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d3ce-119">**Booleschen**</span><span class="sxs-lookup"><span data-stu-id="2d3ce-119">**Boolean**</span></span>](boolean.md)
</dt> <dt>

[<span data-ttu-id="2d3ce-120">**Char**</span><span class="sxs-lookup"><span data-stu-id="2d3ce-120">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="2d3ce-121">Gekapselt Unions</span><span class="sxs-lookup"><span data-stu-id="2d3ce-121">Encapsulated Unions</span></span>](encapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="2d3ce-122">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="2d3ce-122">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="2d3ce-123">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="2d3ce-123">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="2d3ce-124">**INT**</span><span class="sxs-lookup"><span data-stu-id="2d3ce-124">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="2d3ce-125">Nicht gekapselt Unions</span><span class="sxs-lookup"><span data-stu-id="2d3ce-125">Nonencapsulated Unions</span></span>](nonencapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="2d3ce-126">**Switch \_ ist**</span><span class="sxs-lookup"><span data-stu-id="2d3ce-126">**switch\_is**</span></span>](switch-is.md)
</dt> <dt>

[<span data-ttu-id="2d3ce-127">**Union**</span><span class="sxs-lookup"><span data-stu-id="2d3ce-127">**union**</span></span>](union.md)
</dt> </dl>

 

 




