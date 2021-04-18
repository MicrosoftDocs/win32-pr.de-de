---
title: Helpstringcontext-Attribut
description: Das Attribut \ helpstringcontext \ gibt einen 32-Bit-Hilfe Kontext Bezeichner in der Hilfedatei an. Sie können das Attribut \ helpstringcontext \ auf die Anweisungen Library, Interface, dispinterface, Module, Coclass, typedef, Properties, Parameters und Methods anwenden.
ms.assetid: 0ac41bd9-ccc6-4b5c-b925-63bff9254eed
keywords:
- Helpstringcontext-Attribut-Mittel l
topic_type:
- apiref
api_name:
- helpstringcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72ddded3beb768543f2f990aa9d656fba1fa8b98
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106340662"
---
# <a name="helpstringcontext-attribute"></a><span data-ttu-id="f44e3-105">Helpstringcontext-Attribut</span><span class="sxs-lookup"><span data-stu-id="f44e3-105">helpstringcontext attribute</span></span>

<span data-ttu-id="f44e3-106">Das **\[ helpstringcontext \]** -Attribut gibt einen 32-Bit-Hilfe Kontext Bezeichner in der Hilfedatei an.</span><span class="sxs-lookup"><span data-stu-id="f44e3-106">The **\[helpstringcontext\]** attribute specifies a 32-bit Help context identifier in the Help file.</span></span> <span data-ttu-id="f44e3-107">Sie können das **\[ helpstringcontext \]** -Attribut auf [**Library**](library.md), [**Interface**](interface.md), [**dispinterface**](dispinterface.md), [**Module**](module.md), [**Co-Klasse**](coclass.md), [**typedef**](typedef.md) -Anweisungen,-Eigenschaften,-Parameter und-Methoden anwenden.</span><span class="sxs-lookup"><span data-stu-id="f44e3-107">You can apply the **\[helpstringcontext\]** attribute to [**library**](library.md), [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**coclass**](coclass.md), [**typedef**](typedef.md) statements, properties, parameters and methods.</span></span>

``` syntax
[  helpstringcontext(contextid)[, optional-attribute-list]] idl-statement
```

## <a name="parameters"></a><span data-ttu-id="f44e3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f44e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f44e3-109">*ContextId*</span><span class="sxs-lookup"><span data-stu-id="f44e3-109">*contextid*</span></span> 
</dt> <dd>

<span data-ttu-id="f44e3-110">Eine eindeutige ganze Zahl, die den Hilfetext identifiziert, der der aktuellen Mittel l-Anweisung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f44e3-110">A unique integer that identifies the help text associated with the current MIDL statement.</span></span>

</dd> <dt>

<span data-ttu-id="f44e3-111">*optional-Attribut-List*</span><span class="sxs-lookup"><span data-stu-id="f44e3-111">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f44e3-112">NULL oder mehr mittlere Attribute.</span><span class="sxs-lookup"><span data-stu-id="f44e3-112">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="f44e3-113">*IDL-Anweisung*</span><span class="sxs-lookup"><span data-stu-id="f44e3-113">*idl-statement*</span></span> 
</dt> <dd>

<span data-ttu-id="f44e3-114">Die Mittell-Anweisung, auf die das **\[ helpstringcontext \]** -Attribut angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="f44e3-114">The MIDL statement to which the **\[helpstringcontext\]** attribute will be applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f44e3-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f44e3-115">Remarks</span></span>

<span data-ttu-id="f44e3-116">Verwenden Sie die **GetDocumentation2** -Funktionen in den Schnittstellen **ITypeLib2** und **ITypeInfo2** , um die Hilfe Zeichenfolge abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f44e3-116">Use the **GetDocumentation2** functions in the **ITypeLib2** and **ITypeInfo2** interfaces to retrieve the help string.</span></span>

## <a name="examples"></a><span data-ttu-id="f44e3-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f44e3-117">Examples</span></span>

``` syntax
[
    uuid(. . .),
    helpstringcontext(103),
    version(1.0)
]
library Lines
{
    [
        uuid(. . .), 
        helpstringcontext(102),
        oleautomation,
        dual
    ]
    interface ILine : IDispatch
    {
        [propget, helpstringcontext(100)] HRESULT Color([out, retval] long* ReturnVal); 
        [propput, helpstringcontext(101)] HRESULT Color([in] long rgb);
    }
};
```

 

 




