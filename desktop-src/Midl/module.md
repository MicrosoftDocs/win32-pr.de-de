---
title: Module-Attribut
description: Die Module-Anweisung definiert eine Gruppe von Funktionen, in der Regel einen Satz von dll-Einstiegspunkten.
ms.assetid: 4dec207f-98bc-4784-a3c9-506ffe7523fe
keywords:
- Modul Attribut-Mittel l
topic_type:
- apiref
api_name:
- module
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1eb310c3e126caf9b25b8c015b840aea11791d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314877"
---
# <a name="module-attribute"></a><span data-ttu-id="9b4ff-104">Module-Attribut</span><span class="sxs-lookup"><span data-stu-id="9b4ff-104">module attribute</span></span>

<span data-ttu-id="9b4ff-105">Die **Module** -Anweisung definiert eine Gruppe von Funktionen, in der Regel einen Satz von dll-Einstiegspunkten.</span><span class="sxs-lookup"><span data-stu-id="9b4ff-105">The **module** statement defines a group of functions, typically a set of DLL entry points.</span></span>

``` syntax
[
    attributes
]
module modulename 
{
    elementlist
};
```

## <a name="parameters"></a><span data-ttu-id="9b4ff-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b4ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b4ff-107">*attributes*</span><span class="sxs-lookup"><span data-stu-id="9b4ff-107">*attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="9b4ff-108">Die \[ Attribute [**UUID**](uuid.md) \] , \[ [**Version**](version.md) \] , \[ [**HelpString**](helpstring.md) \] , \[ [**HelpContext**](helpcontext.md) \] , \[ [**Hidden**](hidden.md) \] und \[ [**dllName**](dllname-str-.md) \] werden vor einer **Modul** Anweisung akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="9b4ff-108">The \[[**uuid**](uuid.md)\], \[[**version**](version.md)\], \[[**helpstring**](helpstring.md)\], \[[**helpcontext**](helpcontext.md)\], \[[**hidden**](hidden.md)\], and \[[**dllname**](dllname-str-.md)\] attributes are accepted before a **module** statement.</span></span> <span data-ttu-id="9b4ff-109">Weitere Informationen zu den Attributen, die vor einer Modul Definition akzeptiert werden, finden Sie unter [Attribut Beschreibungen](/previous-versions/windows/desktop/automat/attribute-descriptions)im OLE-Automatisierungs Buch.</span><span class="sxs-lookup"><span data-stu-id="9b4ff-109">See [Attribute Descriptions](/previous-versions/windows/desktop/automat/attribute-descriptions), in the OLE Automation book, for more information on the attributes accepted before a module definition.</span></span> <span data-ttu-id="9b4ff-110">Das \[ **dllName** - \] Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9b4ff-110">The \[**dllname**\] attribute is required.</span></span> <span data-ttu-id="9b4ff-111">Wenn das \[ **UUID** - \] Attribut weggelassen wird, wird das Modul im System nicht eindeutig angegeben.</span><span class="sxs-lookup"><span data-stu-id="9b4ff-111">If the \[**uuid**\] attribute is omitted, the module is not uniquely specified in the system.</span></span>

</dd> <dt>

<span data-ttu-id="9b4ff-112">*ModuleName*</span><span class="sxs-lookup"><span data-stu-id="9b4ff-112">*modulename*</span></span> 
</dt> <dd>

<span data-ttu-id="9b4ff-113">Der Name des Moduls.</span><span class="sxs-lookup"><span data-stu-id="9b4ff-113">The name of the module.</span></span>

</dd> <dt>

<span data-ttu-id="9b4ff-114">*Elementliste*</span><span class="sxs-lookup"><span data-stu-id="9b4ff-114">*elementlist*</span></span> 
</dt> <dd>

<span data-ttu-id="9b4ff-115">Liste konstanter Definitionen und Funktionsprototypen für jede Funktion in der dll.</span><span class="sxs-lookup"><span data-stu-id="9b4ff-115">List of constant definitions and function prototypes for each function in the DLL.</span></span> <span data-ttu-id="9b4ff-116">Eine beliebige Anzahl von Funktionsdefinitionen kann in der Funktionsliste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9b4ff-116">Any number of function definitions can appear in the function list.</span></span> <span data-ttu-id="9b4ff-117">Eine Funktion in der Funktionsliste weist die folgende Form auf:</span><span class="sxs-lookup"><span data-stu-id="9b4ff-117">A function in the function list has the following form:</span></span>

<span data-ttu-id="9b4ff-118">\[*Attribute* \] *returnType* \[ funkname der Aufruf *Konvention* \] (*para* Metern);</span><span class="sxs-lookup"><span data-stu-id="9b4ff-118">\[*attributes*\] *returntype* \[*calling convention funcname*\](*params*);</span></span>

<span data-ttu-id="9b4ff-119">\[*Attribute* \] [**const**](const.md) constanttype *constname*  =  *constval*;</span><span class="sxs-lookup"><span data-stu-id="9b4ff-119">\[*attributes*\] [**const**](const.md) constanttype *constname* = *constval*;</span></span>

<span data-ttu-id="9b4ff-120">Nur die \[ [**HelpString**](helpstring.md) \] -und \[ [**HelpContext**](helpcontext.md) - \] Attribute werden für einen [**Konstanten**](const.md)akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="9b4ff-120">Only the \[[**helpstring**](helpstring.md)\] and \[[**helpcontext**](helpcontext.md)\] attributes are accepted for a [**const**](const.md).</span></span>

<span data-ttu-id="9b4ff-121">Die folgenden Attribute werden für eine Funktion in einem Modul akzeptiert: \[ [**HelpString**](helpstring.md) \] , \[ [**HelpContext**](helpcontext.md) \] , \[ [**String**](string.md) \] , \[ [**Entry**](entry.md) \] , \[ [**propget**](propget.md) \] , \[ [**PROPPUT**](propput.md) \] , \[ [**PROPPUTREF**](propputref.md) \] und \[ [**vararg**](vararg.md) \] .</span><span class="sxs-lookup"><span data-stu-id="9b4ff-121">The following attributes are accepted on a function in a module: \[[**helpstring**](helpstring.md)\], \[[**helpcontext**](helpcontext.md)\], \[[**string**](string.md)\], \[[**entry**](entry.md)\], \[[**propget**](propget.md)\], \[[**propput**](propput.md)\], \[[**propputref**](propputref.md)\], and \[[**vararg**](vararg.md)\].</span></span> <span data-ttu-id="9b4ff-122">Wenn \[ **vararg** \] angegeben ist, muss der letzte Parameter ein sicheres Array vom **Variant** -Typ sein.</span><span class="sxs-lookup"><span data-stu-id="9b4ff-122">If \[**vararg**\] is specified, the last parameter must be a safe array of **VARIANT** type.</span></span>

<span data-ttu-id="9b4ff-123">Die optionale Aufruf Konvention kann " \_ \_ Pascal/ \_ Pascal/Pascal", " \_ \_ cdecl/ \_ cdecl/cdecl" oder " \_ \_ StdCall/ \_ StdCall/stdcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="9b4ff-123">The optional calling convention can be one of \_\_pascal/\_pascal/pascal, \_\_cdecl/\_cdecl/cdecl, or \_\_stdcall/\_stdcall/stdcall.</span></span> <span data-ttu-id="9b4ff-124">Der *Typ paramName der Aufruf Konvention* kann bis zu zwei führende Unterstriche enthalten.</span><span class="sxs-lookup"><span data-stu-id="9b4ff-124">The *calling convention type paramname* can include up to two leading underscores.</span></span>

<span data-ttu-id="9b4ff-125">Die Parameterliste ist eine durch Trennzeichen getrennte Liste von:</span><span class="sxs-lookup"><span data-stu-id="9b4ff-125">The parameter list is a comma-delimited list of:</span></span>

<span data-ttu-id="9b4ff-126">\[*legt*\]</span><span class="sxs-lookup"><span data-stu-id="9b4ff-126">\[*attributes*\]</span></span>

<span data-ttu-id="9b4ff-127">Der Typ kann ein beliebiger zuvor deklarierter Typ oder integrierter Typ, ein Zeiger auf einen beliebigen Typ oder ein Zeiger auf einen integrierten Typ sein.</span><span class="sxs-lookup"><span data-stu-id="9b4ff-127">The type can be any previously declared type or built-in type, a pointer to any type, or a pointer to a built-in type.</span></span> <span data-ttu-id="9b4ff-128">Attribute für Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="9b4ff-128">Attributes on parameters are:</span></span>

<span data-ttu-id="9b4ff-129">\[[**in**](in.md) \] , \[ [**out**](out-idl.md) \] , \[ [**optional**](optional.md) \] .</span><span class="sxs-lookup"><span data-stu-id="9b4ff-129">\[[**in**](in.md)\], \[[**out**](out-idl.md)\], \[[**optional**](optional.md)\].</span></span>

<span data-ttu-id="9b4ff-130">Wenn \[ [**optional**](optional.md) \] verwendet wird, müssen die Typen dieser Parameter **Variant** oder Variant sein  \* .</span><span class="sxs-lookup"><span data-stu-id="9b4ff-130">If \[[**optional**](optional.md)\] is used, the types of those parameters must be **VARIANT** or **VARIANT**\*.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b4ff-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b4ff-131">Remarks</span></span>

<span data-ttu-id="9b4ff-132">Die Ausgabe der Header Datei (. h) für Module ist eine Reihe von Funktionsprototypen.</span><span class="sxs-lookup"><span data-stu-id="9b4ff-132">The header file (.h) output for modules is a series of function prototypes.</span></span> <span data-ttu-id="9b4ff-133">Das Schlüsselwort " **Module** " und die umgebenden Klammern werden aus der Ausgabe der Header Datei (. h) entfernt, es wird jedoch ein Kommentar (// **Modul Modul** *Name*) vor den Prototypen eingefügt.</span><span class="sxs-lookup"><span data-stu-id="9b4ff-133">The **module** keyword and surrounding brackets are stripped from the header (.h) file output, but a comment (// **module** *modulename*) is inserted before the prototypes.</span></span> <span data-ttu-id="9b4ff-134">Das Schlüsselwort **extern** wird vor den Deklarationen eingefügt.</span><span class="sxs-lookup"><span data-stu-id="9b4ff-134">The keyword **extern** is inserted before the declarations.</span></span>

## <a name="examples"></a><span data-ttu-id="9b4ff-135">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9b4ff-135">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("This is not GDI.EXE"), 
    helpcontext(190), 
    dllname("MATH.DLL")
] 
module somemodule
{ 
    [helpstring("Color for the frame")] 
            unsigned long const COLOR_FRAME = 0xH80000006; 
    [helpstring("Not a rectangle but a square"), 
     entry(1)] 
            pascal double square([in] double x); 
};
```

## <a name="see-also"></a><span data-ttu-id="9b4ff-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9b4ff-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b4ff-137">**const**</span><span class="sxs-lookup"><span data-stu-id="9b4ff-137">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="9b4ff-138">Inhalt einer Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="9b4ff-138">Contents of a Type Library</span></span>](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[<span data-ttu-id="9b4ff-139">**dllname**</span><span class="sxs-lookup"><span data-stu-id="9b4ff-139">**dllname**</span></span>](dllname-str-.md)
</dt> <dt>

[<span data-ttu-id="9b4ff-140">**ein**</span><span class="sxs-lookup"><span data-stu-id="9b4ff-140">**entry**</span></span>](entry.md)
</dt> <dt>

[<span data-ttu-id="9b4ff-141">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="9b4ff-141">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="9b4ff-142">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="9b4ff-142">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="9b4ff-143">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="9b4ff-143">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="9b4ff-144">**verbirgt**</span><span class="sxs-lookup"><span data-stu-id="9b4ff-144">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="9b4ff-145">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="9b4ff-145">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="9b4ff-146">**propget**</span><span class="sxs-lookup"><span data-stu-id="9b4ff-146">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="9b4ff-147">**propput**</span><span class="sxs-lookup"><span data-stu-id="9b4ff-147">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="9b4ff-148">**propputref**</span><span class="sxs-lookup"><span data-stu-id="9b4ff-148">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="9b4ff-149">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9b4ff-149">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="9b4ff-150">**FUNCFLAGS**</span><span class="sxs-lookup"><span data-stu-id="9b4ff-150">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="9b4ff-151">**UUID**</span><span class="sxs-lookup"><span data-stu-id="9b4ff-151">**uuid**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="9b4ff-152">**vararg**</span><span class="sxs-lookup"><span data-stu-id="9b4ff-152">**vararg**</span></span>](vararg.md)
</dt> <dt>

[<span data-ttu-id="9b4ff-153">**version**</span><span class="sxs-lookup"><span data-stu-id="9b4ff-153">**version**</span></span>](version.md)
</dt> </dl>

 

 