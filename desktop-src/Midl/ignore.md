---
title: Attribut ignorieren
description: Das Attribut \ Ignore \ gibt an, dass ein in einer Struktur oder Union enthaltener Zeiger und das vom Zeiger festgestellte Objekt nicht übertragen werden. Das Attribut \ Ignore \ ist auf Zeiger Elemente von Strukturen oder Unions beschränkt.
ms.assetid: 9c2fc71a-4fac-4a59-95f5-2121067b326f
keywords:
- Attribut-Mittel l ignorieren
topic_type:
- apiref
api_name:
- ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e82b9525dd6de316087db8fdfd55181118d3adc6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858189"
---
# <a name="ignore-attribute"></a><span data-ttu-id="55da9-105">Attribut ignorieren</span><span class="sxs-lookup"><span data-stu-id="55da9-105">ignore attribute</span></span>

<span data-ttu-id="55da9-106">Das **\[ Ignore \]** -Attribut gibt an, dass ein in einer Struktur oder Union enthaltener Zeiger und das vom Zeiger festgestellte Objekt nicht übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="55da9-106">The **\[ignore\]** attribute designates that a pointer contained in a structure or union and the object indicated by the pointer is not transmitted.</span></span> <span data-ttu-id="55da9-107">Das **\[ Ignore \]** -Attribut ist auf Zeiger Elemente von Strukturen oder Unions beschränkt.</span><span class="sxs-lookup"><span data-stu-id="55da9-107">The **\[ignore\]** attribute is restricted to pointer members of structures or unions.</span></span>

``` syntax
[ignore] pointer-member-type pointer-name;
```

## <a name="parameters"></a><span data-ttu-id="55da9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="55da9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55da9-109">*Pointer-Member-Type*</span><span class="sxs-lookup"><span data-stu-id="55da9-109">*pointer-member-type*</span></span> 
</dt> <dd>

<span data-ttu-id="55da9-110">Gibt den Typ des Zeiger Elements der Struktur oder Union an.</span><span class="sxs-lookup"><span data-stu-id="55da9-110">Specifies the type of the pointer member of the structure or union.</span></span>

</dd> <dt>

<span data-ttu-id="55da9-111">*Zeiger Name*</span><span class="sxs-lookup"><span data-stu-id="55da9-111">*pointer-name*</span></span> 
</dt> <dd>

<span data-ttu-id="55da9-112">Gibt den Namen des Zeiger Elements an, das beim Marshalling ignoriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="55da9-112">Specifies the name of the pointer member that is to be ignored during marshaling.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55da9-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55da9-113">Remarks</span></span>

<span data-ttu-id="55da9-114">Der Wert eines Strukturmembers mit dem **\[ Ignore \]** -Attribut ist am Ziel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="55da9-114">The value of a structure member with the **\[ignore\]** attribute is undefined at the destination.</span></span> <span data-ttu-id="55da9-115">Ein **\[** [**in**](in.md) - **\]** Parameter ist nicht auf dem Remote Computer definiert.</span><span class="sxs-lookup"><span data-stu-id="55da9-115">An **\[**[**in**](in.md)**\]** parameter is not defined at the remote computer.</span></span> <span data-ttu-id="55da9-116">Ein **\[** [**out**](out-idl.md) - **\]** Parameter ist nicht auf dem lokalen Computer definiert.</span><span class="sxs-lookup"><span data-stu-id="55da9-116">An **\[**[**out**](out-idl.md)**\]** parameter is not defined at the local computer.</span></span>

<span data-ttu-id="55da9-117">Mit dem Attribut " **\[ Ignore \]** " können Sie die Übertragung von Daten verhindern.</span><span class="sxs-lookup"><span data-stu-id="55da9-117">The **\[ignore\]** attribute allows you to prevent transmission of data.</span></span> <span data-ttu-id="55da9-118">Dies ist in Situationen hilfreich, z. b. in einer doppelt verknüpften Liste.</span><span class="sxs-lookup"><span data-stu-id="55da9-118">This is useful in situations such as a double-linked list.</span></span> <span data-ttu-id="55da9-119">Das folgende Beispiel enthält eine doppelt verknüpfte Liste, die das datenaliasing einführt:</span><span class="sxs-lookup"><span data-stu-id="55da9-119">The following example includes a double-linked list that introduces data aliasing:</span></span>

``` syntax
/* IDL file */ 
typedef struct _DBL_LINK_NODE_TYPE 
{ 
    long value; 
    struct _DBL_LINK_NODE_TYPE * next; 
    struct _DBL_LINK_NODE_TYPE * previous; 
} DBL_LINK_NODE_TYPE; 
 
HRESULT remote_op([in] DBL_LINK_NODE_TYPE * list_head); 
 
/* application */ 
DBL_LINK_NODE_TYPE * p, * q 
 
p = (DBL_LINK_NODE_TYPE *) midl_user_allocate(
        sizeof(DBL_LINK_NODE_TYPE)); 
q = (DBL_LINK_NODE_TYPE *) midl_user_allocate(
        sizeof(DBL_LINK_NODE_TYPE)); 
 
p->next = q;  
q->previous = p; 
p->previous = q->next = NULL; 
.. 
remote_op(p);
```

<span data-ttu-id="55da9-120">Aliasing tritt im vorangehenden Beispiel auf, weil derselbe Speicherbereich von zwei verschiedenen Zeigern in der Funktion **p** und **p->Next->Previous** verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="55da9-120">Aliasing occurs in the preceding example because the same memory area is available from two different pointers in the function **p** and **p->next->previous**.</span></span>

<span data-ttu-id="55da9-121">Beachten Sie, dass **\[ Ignore \]** nicht als Type-Attribut verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="55da9-121">Note that **\[ignore\]** cannot be used as a type attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="55da9-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="55da9-122">Examples</span></span>

``` syntax
typedef struct _DBL_LINK_NODE_TYPE 
{ 
    long value; 
    struct _DBL_LINK_NODE_TYPE * next; 
    [ignore] struct _DBL_LINK_NODE_TYPE * previous; 
} DBL_LINK_NODE_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="55da9-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="55da9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55da9-124">Array-und Sized-Pointer Attribute</span><span class="sxs-lookup"><span data-stu-id="55da9-124">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="55da9-125">**Mikro**</span><span class="sxs-lookup"><span data-stu-id="55da9-125">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="55da9-126">Arrays und Zeiger</span><span class="sxs-lookup"><span data-stu-id="55da9-126">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="55da9-127">**in**</span><span class="sxs-lookup"><span data-stu-id="55da9-127">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="55da9-128">**vorgenommen**</span><span class="sxs-lookup"><span data-stu-id="55da9-128">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="55da9-129">**ptr**</span><span class="sxs-lookup"><span data-stu-id="55da9-129">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="55da9-130">**ref**</span><span class="sxs-lookup"><span data-stu-id="55da9-130">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="55da9-131">**gem**</span><span class="sxs-lookup"><span data-stu-id="55da9-131">**unique**</span></span>](unique.md)
</dt> </dl>

 

 