---
title: id-Attribut
description: Das Attribut \ ID \ gibt eine DISPID für eine Element Funktion an (entweder eine Eigenschaft oder eine Methode in einer Schnittstelle oder einer dispinterface).
ms.assetid: 6f1be049-81b4-4aa2-a893-5dd79bb4d63c
keywords:
- ID-Attribut-Mittel l
topic_type:
- apiref
api_name:
- id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07c57d8ea818bbd7b8fd5bd35816e6b7227eb917
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390175"
---
# <a name="id-attribute"></a><span data-ttu-id="8034f-104">id-Attribut</span><span class="sxs-lookup"><span data-stu-id="8034f-104">id attribute</span></span>

<span data-ttu-id="8034f-105">Das **\[ ID \]** -Attribut gibt eine DISPID für eine Element Funktion an (entweder eine Eigenschaft oder eine Methode in einer Schnittstelle oder einer dispinterface).</span><span class="sxs-lookup"><span data-stu-id="8034f-105">The **\[id\]** attribute specifies a DISPID for a member function (either a property or a method, in an interface or dispinterface).</span></span>

``` syntax
[id(id-num) [,optional-attribute-list]] return-type function-name(optional-parameter-list)
```

## <a name="parameters"></a><span data-ttu-id="8034f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8034f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8034f-107">*ID-num*</span><span class="sxs-lookup"><span data-stu-id="8034f-107">*id-num*</span></span> 
</dt> <dd>

<span data-ttu-id="8034f-108">DISPID für die Funktion.</span><span class="sxs-lookup"><span data-stu-id="8034f-108">DISPID for the function.</span></span>

</dd> <dt>

<span data-ttu-id="8034f-109">*optional-Attribut-List*</span><span class="sxs-lookup"><span data-stu-id="8034f-109">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="8034f-110">Gibt eine Liste von 0 (null) oder mehr Attributen der Mittelwert Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="8034f-110">Specifies a list of zero or more MIDL interface attributes.</span></span>

</dd> <dt>

<span data-ttu-id="8034f-111">*Rückgabetyp*</span><span class="sxs-lookup"><span data-stu-id="8034f-111">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="8034f-112">Gibt den Rückgabetyp der Funktion an.</span><span class="sxs-lookup"><span data-stu-id="8034f-112">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="8034f-113">*function-name*</span><span class="sxs-lookup"><span data-stu-id="8034f-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="8034f-114">Gibt den Namen der Funktion in der IDL-Datei an.</span><span class="sxs-lookup"><span data-stu-id="8034f-114">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="8034f-115">*Optional-Parameter-List*</span><span class="sxs-lookup"><span data-stu-id="8034f-115">*optional-parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="8034f-116">NULL oder mehr Funktionsparameter.</span><span class="sxs-lookup"><span data-stu-id="8034f-116">Zero or more function parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8034f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8034f-117">Remarks</span></span>

<span data-ttu-id="8034f-118">Verwenden Sie das **\[ ID \]** -Attribut, wenn Sie einer Methode oder Eigenschaft eine Standard-DISPID (z. b. DISPID- \_ Wert, DISPID-Diagramm \_ usw.) zuweisen möchten, oder wenn Sie einen eigenen **IDispatch::** -Aufruf implementieren, anstatt zu delegieren, um / **ITypeInfo:: Aufrufen** zu lösen.</span><span class="sxs-lookup"><span data-stu-id="8034f-118">Use the **\[id\]** attribute when you want to assign a standard DISPID (like DISPID\_VALUE, DISPID\_NEWENUM etc.) to a method or property, or when you implement your own **IDispatch::Invoke** instead of delegating to **DispInvoke**/**ITypeInfo::Invoke**.</span></span>

<span data-ttu-id="8034f-119">Wenn Sie das **\[ ID \]** -Attribut nicht für eine Schnittstelle verwenden, weist der mittlerer l-Compiler eine "DISPID" zu.</span><span class="sxs-lookup"><span data-stu-id="8034f-119">If you do not use the **\[id\]** attribute on an interface, the MIDL compiler will assign a DISPID for you.</span></span> <span data-ttu-id="8034f-120">Wenn Sie jedoch eine dispinterface mithilfe von Eigenschaften und Methoden angeben, müssen Sie für jede Eigenschaft und Methode eine DISPID angeben.</span><span class="sxs-lookup"><span data-stu-id="8034f-120">However, when you specify a dispinterface by using properties and methods, you must specify a DISPID for every property and method.</span></span>

<span data-ttu-id="8034f-121">Die *ID-num* ist ein positiver ganzzahliger Wert von 32 Bit.</span><span class="sxs-lookup"><span data-stu-id="8034f-121">The *id-num* is a 32-bit positive integral value.</span></span> <span data-ttu-id="8034f-122">Negative IDs sind für die Verwendung durch Automation reserviert.</span><span class="sxs-lookup"><span data-stu-id="8034f-122">Negative IDs are reserved for use by Automation.</span></span>

## <a name="examples"></a><span data-ttu-id="8034f-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8034f-123">Examples</span></span>

``` syntax
interface IKnown : IUnknown
{
    properties:
        [id(90), propget, 
         helpstring("A meaningful comment."] long Func1(void);

    /* Other interface statements */
}
```

## <a name="see-also"></a><span data-ttu-id="8034f-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8034f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8034f-125">**berfläche**</span><span class="sxs-lookup"><span data-stu-id="8034f-125">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="8034f-126">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="8034f-126">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="8034f-127">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="8034f-127">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="8034f-128">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="8034f-128">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="8034f-129">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="8034f-129">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 