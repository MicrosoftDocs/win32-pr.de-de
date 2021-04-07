---
title: in-Attribut
description: Das Attribut \ in \ gibt an, dass ein Parameter von der aufrufenden Prozedur an die aufgerufene Prozedur übergeben werden soll.
ms.assetid: 85d5617e-8b73-449a-9627-2c8d5ab2b629
keywords:
- in attributmittell
topic_type:
- apiref
api_name:
- in
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b606a834b394197960777fa485d112a94212ec45
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726968"
---
# <a name="in-attribute"></a><span data-ttu-id="4067c-104">in-Attribut</span><span class="sxs-lookup"><span data-stu-id="4067c-104">in attribute</span></span>

<span data-ttu-id="4067c-105">Das **\[ in \]** -Attribut gibt an, dass ein Parameter von der aufrufenden Prozedur an die aufgerufene Prozedur übergeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="4067c-105">The **\[in\]** attribute indicates that a parameter is to be passed from the calling procedure to the called procedure.</span></span>

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ in [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="4067c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4067c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4067c-107">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="4067c-107">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4067c-108">Gibt 0 (null) oder mehr Attribute an, die für die Funktion gelten.</span><span class="sxs-lookup"><span data-stu-id="4067c-108">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="4067c-109">Gültige Funktions Attribute sind **\[ Callback \]**, **\[ local \]**, das Zeiger Attribut **\[ ref \]**, **\[ Unique \]** oder **\[ ptr \]** und die Verwendungs Attribute **\[ Zeichenfolge \]**, **\[ Ignore \]** und **\[ Kontext \_ handle \]**.</span><span class="sxs-lookup"><span data-stu-id="4067c-109">Valid function attributes are **\[callback\]**, **\[local\]**, the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**, and the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="4067c-110">*Typspezifizierer*</span><span class="sxs-lookup"><span data-stu-id="4067c-110">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="4067c-111">Gibt einen **\_ Basistyp**, eine [**Struktur**](struct.md), eine [**Union**](union.md)oder einen Aufzählungstyp [**oder einen**](enum.md) Typbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="4067c-111">Specifies a **base\_type**, [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="4067c-112">Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4067c-112">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="4067c-113">*Zeiger-Deklarator*</span><span class="sxs-lookup"><span data-stu-id="4067c-113">*pointer-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="4067c-114">Gibt 0 (null) oder mehr Zeiger Deklaratoren an.</span><span class="sxs-lookup"><span data-stu-id="4067c-114">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="4067c-115">Ein zeigerdeklarator ist derselbe wie der in C verwendete zeigerdeklarator. Sie wird aus dem Kenn \* Zeichner, den Modifizierern, z. b. **weit**, und dem Qualifizierer " [**Konstanten**](const.md)" erstellt.</span><span class="sxs-lookup"><span data-stu-id="4067c-115">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="4067c-116">*function-name*</span><span class="sxs-lookup"><span data-stu-id="4067c-116">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4067c-117">Gibt den Namen der Remote Prozedur an.</span><span class="sxs-lookup"><span data-stu-id="4067c-117">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="4067c-118">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="4067c-118">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4067c-119">Gibt NULL oder mehr Attribute an, die für den angegebenen Parametertyp geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="4067c-119">Specifies zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="4067c-120">Parameter Attribute mit dem **\[ in \]** -Attribut können auch **\[ \]** das **\[ \]** **\[ \]** direktionale Attribut übernehmen. die **\[ \]** **\[ \_ \]** Feld Attribute **\[ \_ sind \] zuerst** **\[ \_ \]** **\[ \_ \]** **\[ \_ \]** **\[ \]**, "Last", "length", "Max is", "size" und "Switch Type", das Zeiger Attribut "ref", "Unique" oder "PTR" und das **\[ Kontext \_ handle \]** für Verwendungs Attribute **\[ \_ \]**</span><span class="sxs-lookup"><span data-stu-id="4067c-120">Parameter attributes with the **\[in\]** attribute can also take the directional attribute **\[out\]**; the field attributes **\[first\_is\]**, **\[last\_is\]**, **\[length\_is\]**, **\[max\_is\]**, **\[size\_is\]** and **\[switch\_type\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[context\_handle\]** and **\[string\]**.</span></span> <span data-ttu-id="4067c-121">Das Usage-Attribut " **\[ Ignore \]** " kann nicht als Parameter Attribut verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4067c-121">The usage attribute **\[ignore\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="4067c-122">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="4067c-122">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="4067c-123">*Deklarator*</span><span class="sxs-lookup"><span data-stu-id="4067c-123">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="4067c-124">Gibt Standard-C-Deklaratoren an, z. b. Bezeichner, Zeiger Deklaratoren und Array Deklaratoren.</span><span class="sxs-lookup"><span data-stu-id="4067c-124">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="4067c-125">Weitere Informationen finden Sie unter [Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**Arrays**](arrays-1.md)und [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="4067c-125">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="4067c-126">Der parameterdeklarator im funktionsdedeclarator (z. b. der Parameter Name) ist optional.</span><span class="sxs-lookup"><span data-stu-id="4067c-126">The parameter declarator in the function declarator, such as the parameter name, is optional.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4067c-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4067c-127">Remarks</span></span>

<span data-ttu-id="4067c-128">Das **\[ in \]** -Attribut verfügt über ein umgekehrter Attribut, **\[** [](out-idl.md) **\]** das angibt, dass ein Parameter von der aufgerufenen Prozedur an die aufrufende Prozedur zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="4067c-128">The **\[in\]** attribute has a converse attribute, **\[**[**out**](out-idl.md)**\]**, which indicates that a parameter is to be returned from the called procedure to the calling procedure.</span></span> <span data-ttu-id="4067c-129">Die Attribute " **\[ in \]** " und " **\[ out \]** " werden als direktionale Parameter Attribute bezeichnet, da Sie die Richtung angeben, in der Parameter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="4067c-129">The **\[in\]** and **\[out\]** attributes are known as directional parameter attributes because they specify the direction in which parameters are passed.</span></span> <span data-ttu-id="4067c-130">Ein Parameter kann als " **\[ in \]**", " **\[ out \]**" oder " **\[ in**" oder " **out \]**" definiert werden.</span><span class="sxs-lookup"><span data-stu-id="4067c-130">A parameter can be defined as **\[in\]**, **\[out\]**, or **\[in**, **out\]**.</span></span>

<span data-ttu-id="4067c-131">Das **\[ in \]** -Attribut identifiziert Parameter, die vom Clientstub für die Übertragung an den Server gemarshallt werden.</span><span class="sxs-lookup"><span data-stu-id="4067c-131">The **\[in\]** attribute identifies parameters that are marshaled by the client stub for transmission to the server.</span></span>

<span data-ttu-id="4067c-132">Das **\[ in \]** -Attribut wird standardmäßig auf einen Parameter angewendet, wenn kein direktionales Parameter Attribut angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4067c-132">The **\[in\]** attribute is applied to a parameter by default when no directional parameter attribute is specified.</span></span>

## <a name="examples"></a><span data-ttu-id="4067c-133">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4067c-133">Examples</span></span>

``` syntax
HRESULT MyFunction([in] short count);
```

## <a name="see-also"></a><span data-ttu-id="4067c-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4067c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4067c-135">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="4067c-135">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="4067c-136">**mittlere Benutzer Zuordnungen \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4067c-136">**midl\_user\_allocate**</span></span>](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[<span data-ttu-id="4067c-137">**vorgenommen**</span><span class="sxs-lookup"><span data-stu-id="4067c-137">**out**</span></span>](out-idl.md)
</dt> </dl>

 

 