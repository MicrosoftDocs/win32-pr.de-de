---
title: Switch-Attribut
description: Das Schlüsselwort Switch wählt die Diskriminante für eine gekapselte \_ Union aus.
ms.assetid: 66179b68-852f-4943-9105-e9fb310f3c2e
keywords:
- Attribut-Mittel l wechseln
topic_type:
- apiref
api_name:
- switch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cdf9342789d5603a3b64d778bd60364eebde50e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103948221"
---
# <a name="switch-attribute"></a><span data-ttu-id="5a6ea-104">Switch-Attribut</span><span class="sxs-lookup"><span data-stu-id="5a6ea-104">switch attribute</span></span>

<span data-ttu-id="5a6ea-105">Das Schlüsselwort **Switch** wählt die Diskriminante für eine [**gekapselte \_ Union**](encapsulated-unions.md)aus.</span><span class="sxs-lookup"><span data-stu-id="5a6ea-105">The **switch** keyword selects the discriminant for an [**encapsulated\_union**](encapsulated-unions.md).</span></span>

``` syntax
switch (switch-type switch-name)
```

## <a name="parameters"></a><span data-ttu-id="5a6ea-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a6ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a6ea-107">*Switch-Type*</span><span class="sxs-lookup"><span data-stu-id="5a6ea-107">*switch-type*</span></span> 
</dt> <dd>

<span data-ttu-id="5a6ea-108">Gibt einen [**int**](int.md)-, [**char**](-char.md)-, [**Enumeration**](enum.md) -Typ oder einen Bezeichner an, der zu einem dieser Typen aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="5a6ea-108">Specifies an [**int**](int.md), [**char**](-char.md), [**enum**](enum.md) type, or an identifier that resolves to one of these types.</span></span>

</dd> <dt>

<span data-ttu-id="5a6ea-109">*SwitchName*</span><span class="sxs-lookup"><span data-stu-id="5a6ea-109">*switch-name*</span></span> 
</dt> <dd>

<span data-ttu-id="5a6ea-110">Gibt den Namen der Variablen vom Typ *Switch-Type* an, der als Union-diskriminant fungiert.</span><span class="sxs-lookup"><span data-stu-id="5a6ea-110">Specifies the name of the variable of type *switch-type* that acts as the union discriminant.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="5a6ea-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a6ea-111">Examples</span></span>

``` syntax
typedef union _S1_TYPE switch (long l1) U1_TYPE 
{ 
    case 1024: 
        float f1; 
    case 2048: 
        double d2; 
} S1_TYPE; 
 
/* in generated header file */ 
typedef struct _S1_TYPE 
{ 
    long l1; 
    union 
    { 
        float f1; 
        double d2; 
    } U1_TYPE; 
} S1_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="5a6ea-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5a6ea-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a6ea-113">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="5a6ea-113">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="5a6ea-114">Nicht gekapselt Unions</span><span class="sxs-lookup"><span data-stu-id="5a6ea-114">Nonencapsulated Unions</span></span>](nonencapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="5a6ea-115">**Switch \_ ist**</span><span class="sxs-lookup"><span data-stu-id="5a6ea-115">**switch\_is**</span></span>](switch-is.md)
</dt> <dt>

[<span data-ttu-id="5a6ea-116">**\_Switchtyp**</span><span class="sxs-lookup"><span data-stu-id="5a6ea-116">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="5a6ea-117">**Union**</span><span class="sxs-lookup"><span data-stu-id="5a6ea-117">**union**</span></span>](union.md)
</dt> </dl>

 

 




