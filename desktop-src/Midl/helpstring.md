---
title: HelpString-Attribut
description: Das Attribut \ HelpString \ gibt eine Zeichenfolge an, mit der das Element beschrieben wird, auf das es angewendet wird.
ms.assetid: f05d3fdd-d975-4f0e-8181-07e16288ff48
keywords:
- HelpString-Attribut-Mittel l
topic_type:
- apiref
api_name:
- helpstring
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c58bbe61b10e2f223cf9f662f10d95ca72819b02
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948630"
---
# <a name="helpstring-attribute"></a><span data-ttu-id="b3d43-104">HelpString-Attribut</span><span class="sxs-lookup"><span data-stu-id="b3d43-104">helpstring attribute</span></span>

<span data-ttu-id="b3d43-105">Das **\[ HelpString \]** -Attribut gibt eine Zeichenfolge an, die verwendet wird, um das Element zu beschreiben, auf das es angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="b3d43-105">The **\[helpstring\]** attribute specifies a character string that is used to describe the element to which it applies.</span></span> <span data-ttu-id="b3d43-106">Sie können das **\[ HelpString \]** -Attribut auf die Anweisungen Library, importlib, Interface, dispinterface, Module oder Co-Klasse, Typedefs, Properties und Methods anwenden.</span><span class="sxs-lookup"><span data-stu-id="b3d43-106">You can apply the **\[helpstring\]** attribute to library, importlib, interface, dispinterface, module, or coclass statements, typedefs, properties, and methods.</span></span>

``` syntax
[
    helpstring(help-text-string)
    [, optional-attribute-list]
] 
element element-name
{
    definition
}

[idl-statement, helpstring(help-text-string)]
```

## <a name="parameters"></a><span data-ttu-id="b3d43-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3d43-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3d43-108">*Hilfe-Text Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="b3d43-108">*help-text-string*</span></span> 
</dt> <dd>

<span data-ttu-id="b3d43-109">Eine mit NULL endend beendete Zeichenfolge, die Hilfetext enthält.</span><span class="sxs-lookup"><span data-stu-id="b3d43-109">A zero-terminated string of characters containing help text.</span></span>

</dd> <dt>

<span data-ttu-id="b3d43-110">*optional-Attribut-List*</span><span class="sxs-lookup"><span data-stu-id="b3d43-110">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b3d43-111">NULL oder mehr Mittelwert-Attribut Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="b3d43-111">Zero or more MIDL attribute statements.</span></span>

</dd> <dt>

<span data-ttu-id="b3d43-112">*gewisses*</span><span class="sxs-lookup"><span data-stu-id="b3d43-112">*element*</span></span> 
</dt> <dd>

<span data-ttu-id="b3d43-113">Eine der folgenden Direktiven: [**Library**](library.md), **\[** [**importlib**](importlib.md) **\]** , [**Interface**](interface.md), [**dispinterface**](dispinterface.md), [**Module**](module.md), [**typedef**](typedef.md), **method**, **Property** oder [**Co-Klasse**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="b3d43-113">One of the following directives: [**library**](library.md), **\[**[**importlib**](importlib.md)**\]**, [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **method**, **property**, or [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3d43-114">*Elementname*</span><span class="sxs-lookup"><span data-stu-id="b3d43-114">*element-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b3d43-115">Der Name, den andere Softwarekomponenten verwenden können, um das aktuelle Element zu definieren.</span><span class="sxs-lookup"><span data-stu-id="b3d43-115">The name that other software components can use to delineate the current element</span></span>

</dd> <dt>

<span data-ttu-id="b3d43-116">*Definition*</span><span class="sxs-lookup"><span data-stu-id="b3d43-116">*definition*</span></span> 
</dt> <dd>

<span data-ttu-id="b3d43-117">Gibt die-Anweisungen an, die die Element Definition bilden.</span><span class="sxs-lookup"><span data-stu-id="b3d43-117">Specifies statements that make up the element definition.</span></span>

</dd> <dt>

<span data-ttu-id="b3d43-118">*IDL-Anweisung*</span><span class="sxs-lookup"><span data-stu-id="b3d43-118">*idl-statement*</span></span> 
</dt> <dd>

<span data-ttu-id="b3d43-119">Eine Anweisung der Mittell-Schnittstellen Definition, z. b. [**propget**](propget.md) oder [**PROPPUT**](propput.md).</span><span class="sxs-lookup"><span data-stu-id="b3d43-119">A MIDL interface definition statement such as [**propget**](propget.md) or [**propput**](propput.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3d43-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3d43-120">Remarks</span></span>

<span data-ttu-id="b3d43-121">Verwenden Sie die [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) -Funktionen in den Schnittstellen [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) und [**itypeingefo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) , um die Hilfe Zeichenfolge abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b3d43-121">Use the [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) functions in the [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) and [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) interfaces to retrieve the help string.</span></span>

## <a name="examples"></a><span data-ttu-id="b3d43-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b3d43-122">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("Lines 1.0 Type Library"),
    version(1.0)
]
library Lines
{
     [
         uuid(1e123456-1f3c-1069-996b-00dd010fe676), 
         helpstring("Line object."),
         oleautomation,
         dual
     ]
     interface ILine : IDispatch                         
     {
         [propget, helpstring("Returns and sets RGB color.")]
         HRESULT Color([out, retval] long* ReturnVal); 
         [propput, helpstring("Returns and sets RGB color.")]
         HRESULT Color([in] long rgb);
     }
};
```

## <a name="see-also"></a><span data-ttu-id="b3d43-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b3d43-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3d43-124">**Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="b3d43-124">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="b3d43-125">**importlib**</span><span class="sxs-lookup"><span data-stu-id="b3d43-125">**importlib**</span></span>](importlib.md)
</dt> <dt>

[<span data-ttu-id="b3d43-126">**berfläche**</span><span class="sxs-lookup"><span data-stu-id="b3d43-126">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="b3d43-127">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="b3d43-127">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="b3d43-128">**Mond**</span><span class="sxs-lookup"><span data-stu-id="b3d43-128">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="b3d43-129">**coclass**</span><span class="sxs-lookup"><span data-stu-id="b3d43-129">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="b3d43-130">**typedef**</span><span class="sxs-lookup"><span data-stu-id="b3d43-130">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="b3d43-131">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="b3d43-131">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="b3d43-132">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="b3d43-132">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="b3d43-133">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="b3d43-133">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 