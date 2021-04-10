---
title: Schnittstellenattribut
description: Das Interface-Schlüsselwort gibt den Namen der Schnittstelle an. Der Schnittstellen Name muss sowohl in der IDL-Datei als auch in der ACF angegeben werden.
ms.assetid: 239b782e-57de-493c-b2f4-310d1859a9ae
keywords:
- Schnittstellen Attribut-Mittel l
topic_type:
- apiref
api_name:
- interface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852c29b2ba7b43e9d8b15863e60db8ad2fbde33f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858186"
---
# <a name="interface-attribute"></a><span data-ttu-id="2754e-105">Schnittstellenattribut</span><span class="sxs-lookup"><span data-stu-id="2754e-105">interface attribute</span></span>

<span data-ttu-id="2754e-106">Das **Interface** -Schlüsselwort gibt den Namen der Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="2754e-106">The **interface** keyword specifies the name of the interface.</span></span> <span data-ttu-id="2754e-107">Der Schnittstellen Name muss sowohl in der IDL-Datei als auch in der ACF angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2754e-107">The interface name must be provided in both the IDL file and the ACF.</span></span>

``` syntax
[ 
    interface-attribute-list 
] 
interface interface-name [ : base-interface ]
{
}

typedef interface interface-name declarator-list
```

## <a name="parameters"></a><span data-ttu-id="2754e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2754e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2754e-109">*Interface-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="2754e-109">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="2754e-110">Gibt Attribute an, die auf die gesamte Schnittstelle angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="2754e-110">Specifies attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="2754e-111">Gültige Schnittstellen Attribute für eine IDL-Datei sind **\[** [**EndPoint**](endpoint.md) **\]** , **\[** [**local**](local.md) **\]** , **\[** [**Object**](object.md) **\]** , **\[** [**Zeiger \_ Standard**](pointer-default.md) **\]** , **\[** [**UUID**](uuid.md) **\]** und **\[** [**Version**](version.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="2754e-111">Valid interface attributes for an IDL file include **\[**[**endpoint**](endpoint.md)**\]**, **\[**[**local**](local.md)**\]**, **\[**[**object**](object.md)**\]**, **\[**[**pointer\_default**](pointer-default.md)**\]**, **\[**[**uuid**](uuid.md)**\]**, and **\[**[**version**](version.md)**\]**.</span></span> <span data-ttu-id="2754e-112">Gültige Schnittstellen Attribute für eine ACF sind z **\[** . b. [**Codieren**](encode.md) **\]** , **\[** [**decodieren**](decode.md) **\]** , entweder **\[** [**Automatisches \_ handle**](auto-handle.md) **\]** oder **\[** [**implizites \_ handle**](implicit-handle.md) **\]** und entweder **\[** [**Code**](code.md) **\]** oder **\[** [**NoCode**](nocode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="2754e-112">Valid interface attributes for an ACF include **\[**[**encode**](encode.md)**\]**, **\[**[**decode**](decode.md)**\]**, either **\[**[**auto\_handle**](auto-handle.md)**\]** or **\[**[**implicit\_handle**](implicit-handle.md)**\]**, and either **\[**[**code**](code.md)**\]** or **\[**[**nocode**](nocode.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="2754e-113">*Schnittstellen Name*</span><span class="sxs-lookup"><span data-stu-id="2754e-113">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="2754e-114">Gibt den Namen der Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="2754e-114">Specifies the name of the interface.</span></span> <span data-ttu-id="2754e-115">Der Schnittstellen Name muss ein eindeutiger Name sein und muss mit einem Buchstaben oder einem Unterstrich beginnen.</span><span class="sxs-lookup"><span data-stu-id="2754e-115">The interface name must be a unique name and must start with an alphabetic or underscore character.</span></span>

</dd> <dt>

<span data-ttu-id="2754e-116">*Basisschnittstelle*</span><span class="sxs-lookup"><span data-stu-id="2754e-116">*base-interface*</span></span> 
</dt> <dd>

<span data-ttu-id="2754e-117">Gibt den Namen einer Schnittstelle an, von der diese abgeleitete Schnittstelle Member-Funktionen, Statuscodes und Schnittstellen Attribute erbt.</span><span class="sxs-lookup"><span data-stu-id="2754e-117">Specifies the name of an interface from which this derived interface inherits member functions, status codes, and interface attributes.</span></span> <span data-ttu-id="2754e-118">Die abgeleitete Schnittstelle erbt keine Typdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="2754e-118">The derived interface does not inherit type definitions.</span></span> <span data-ttu-id="2754e-119">Verwenden Sie hierzu das Schlüsselwort [**Import**](import.md) , um die IDL-Datei der Basisschnittstelle zu importieren.</span><span class="sxs-lookup"><span data-stu-id="2754e-119">To do this, use the [**import**](import.md) keyword to import the IDL file of the base interface.</span></span>

</dd> <dt>

<span data-ttu-id="2754e-120">*Deklarator-List*</span><span class="sxs-lookup"><span data-stu-id="2754e-120">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="2754e-121">Gibt Standard-C-Deklaratoren an, z. b. Bezeichner, Zeiger Deklaratoren und Array Deklaratoren.</span><span class="sxs-lookup"><span data-stu-id="2754e-121">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="2754e-122">Weitere Informationen finden Sie unter [Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**Arrays**](arrays-1.md)und [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="2754e-122">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="2754e-123">Die *declarator-List* besteht aus einem oder mehreren Deklaratoren, die durch Kommas getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="2754e-123">The *declarator-list* consists of one or more declarators, separated by commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2754e-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2754e-124">Remarks</span></span>

<span data-ttu-id="2754e-125">Die Schnittstellennamen in der IDL-Datei und der ACF müssen identisch sein, es sei denn, Sie verwenden den Mittelwert des Compilerschalters [**/ACF**](-acf.md).</span><span class="sxs-lookup"><span data-stu-id="2754e-125">The interface names in the IDL file and ACF must be the same, except when you use the MIDL compiler switch [**/acf**](-acf.md).</span></span>

<span data-ttu-id="2754e-126">Der Schnittstellen Name bildet den ersten Teil des Namens von Schnittstellen handle-Datenstrukturen, die Parameter für die RPC-Lauf Zeitfunktionen sind.</span><span class="sxs-lookup"><span data-stu-id="2754e-126">The interface name forms the first part of the name of interface-handle data structures that are parameters to the RPC run-time functions.</span></span> <span data-ttu-id="2754e-127">Weitere Informationen finden Sie unter [**RPC- \_ if- \_ handle**](/windows/desktop/Rpc/rpc-if-handle).</span><span class="sxs-lookup"><span data-stu-id="2754e-127">For more information, see [**RPC\_IF\_HANDLE**](/windows/desktop/Rpc/rpc-if-handle).</span></span>

<span data-ttu-id="2754e-128">Wenn der Schnittstellen Header das Object-Attribut enthält, **\[** [](object.md) **\]** um eine COM-Schnittstelle anzugeben, muss er auch das **\[** [**UUID**](uuid.md) **\]** -Attribut enthalten und muss die Basis-com-Schnittstelle angeben, von der er abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="2754e-128">If the interface header includes the **\[**[**object**](object.md)**\]** attribute to indicate a COM interface, it must also include the **\[**[**uuid**](uuid.md)**\]** attribute and must specify the base COM interface from which it is derived.</span></span> <span data-ttu-id="2754e-129">Weitere Informationen zu COM-Schnittstellen finden Sie unter **\[** [**Object**](object.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="2754e-129">For more information about COM interfaces, see **\[**[**object**](object.md)**\]**.</span></span>

<span data-ttu-id="2754e-130">Sie können auch das **Interface** -Schlüsselwort mit dem [**typedef**](typedef.md) -Schlüsselwort verwenden, um einen Schnittstellen Datentyp zu definieren.</span><span class="sxs-lookup"><span data-stu-id="2754e-130">You can also use the **interface** keyword with the [**typedef**](typedef.md) keyword to define an interface data type.</span></span>

## <a name="examples"></a><span data-ttu-id="2754e-131">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2754e-131">Examples</span></span>

``` syntax
/* use of interface keyword in IDL file for an RPC interface */ 
[ 
    uuid (00000000-0000-0000-0000-000000000000), 
    version (1.0) 
] 
interface remote_if_2 
{  
    // Interface definition statements.
} 
 
/* use of interface keyword in ACF for an RPC interface */ 
[
    implicit_handle( handle_t xa_bhandle ) 
] 
interface remote_if_2 
{ 
    // Attribute configuration statements.
} 
 
/* use of interface keyword in IDL file for a COM interface */ 
[ 
    object, uuid (00000000-0000-0000-0000-000000000000) 
] 
interface IDerivedInterface : IBaseInterface 
{  
    import "base.idl" 
    Save(); 
} 
 
/* use of interface keyword to define an interface pointer type */ 
typedef interface IStorage *LPSTORAGE;
```

## <a name="see-also"></a><span data-ttu-id="2754e-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2754e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2754e-133">Anwendungs Konfigurationsdatei (ACF)</span><span class="sxs-lookup"><span data-stu-id="2754e-133">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="2754e-134">**Dreher**</span><span class="sxs-lookup"><span data-stu-id="2754e-134">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="2754e-135">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="2754e-135">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="2754e-136">**nah**</span><span class="sxs-lookup"><span data-stu-id="2754e-136">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="2754e-137">**Objekt (object)**</span><span class="sxs-lookup"><span data-stu-id="2754e-137">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="2754e-138">**Zeiger \_ Standard**</span><span class="sxs-lookup"><span data-stu-id="2754e-138">**pointer\_default**</span></span>](pointer-default.md)
</dt> <dt>

[<span data-ttu-id="2754e-139">**RPC- \_ if- \_ handle**</span><span class="sxs-lookup"><span data-stu-id="2754e-139">**RPC\_IF\_HANDLE**</span></span>](/windows/desktop/Rpc/rpc-if-handle)
</dt> <dt>

[<span data-ttu-id="2754e-140">**typedef**</span><span class="sxs-lookup"><span data-stu-id="2754e-140">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="2754e-141">**UUID**</span><span class="sxs-lookup"><span data-stu-id="2754e-141">**uuid**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="2754e-142">**version**</span><span class="sxs-lookup"><span data-stu-id="2754e-142">**version**</span></span>](version.md)
</dt> </dl>

 

 