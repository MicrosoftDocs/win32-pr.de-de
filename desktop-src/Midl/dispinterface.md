---
title: dispinterface-Attribut
description: Die dispinterface-Anweisung definiert einen Satz von Eigenschaften und Methoden, auf die Sie IDispatch aufrufen können.
ms.assetid: d85a8e2b-0155-4d68-bb38-e86f4807e7de
keywords:
- Attribut für Dispinterface-Attribut
topic_type:
- apiref
api_name:
- dispinterface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7cc2b6087b53ff81aa7270a209266dd8248884
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858241"
---
# <a name="dispinterface-attribute"></a><span data-ttu-id="229cd-104">dispinterface-Attribut</span><span class="sxs-lookup"><span data-stu-id="229cd-104">dispinterface attribute</span></span>

<span data-ttu-id="229cd-105">Die **dispinterface** -Anweisung definiert einen Satz von Eigenschaften und Methoden, auf die Sie **IDispatch:: Aufrufen** aufrufen können.</span><span class="sxs-lookup"><span data-stu-id="229cd-105">The **dispinterface** statement defines a set of properties and methods on which you can call **IDispatch::Invoke**.</span></span> <span data-ttu-id="229cd-106">Eine dispinterface kann definiert werden, indem der Satz unterstützter Methoden und Eigenschaften (Syntax 1) explizit aufgelistet oder eine einzelne Schnittstelle aufgelistet wird (Syntax 2).</span><span class="sxs-lookup"><span data-stu-id="229cd-106">A dispinterface may be defined by explicitly listing the set of supported methods and properties (Syntax 1), or by listing a single interface (Syntax 2).</span></span>

``` syntax
[
    [attributes]
]
dispinterface dispinterface-name
{
    properties:
        property-list
    methods:
        method-list
};

[
  [attributes]
]
dispinterface dispinterface-name
{
    interface interface-name
};
```

## <a name="parameters"></a><span data-ttu-id="229cd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="229cd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="229cd-108">*attributes*</span><span class="sxs-lookup"><span data-stu-id="229cd-108">*attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="229cd-109">Gibt Attribute an, die auf die gesamte **dispinterface** angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="229cd-109">Specifies attributes that apply to the entire **dispinterface**.</span></span> <span data-ttu-id="229cd-110">Die folgenden Attribute werden akzeptiert: **\[** [**HelpString**](helpstring.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**HelpFile**](helpfile.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** , **\[** [**nonextensible**](nonextensible.md) **\]** , **\[** [**oleautomation**](oleautomation.md) **\]** , **\[** [**restricted**](restricted.md) **\]** , **\[** [**UUID**](uuid.md) **\]** und **\[** [**Version**](version.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="229cd-110">The following attributes are accepted: **\[**[**helpstring**](helpstring.md)**\]**, **\[**[**helpcontext**](helpcontext.md)**\]**, **\[**[**helpfile**](helpfile.md)**\]**, **\[**[**hidden**](hidden.md)**\]**, **\[**[**nonextensible**](nonextensible.md)**\]**, **\[**[**oleautomation**](oleautomation.md)**\]**, **\[**[**restricted**](restricted.md)**\]**, **\[**[**uuid**](uuid.md)**\]**, and **\[**[**version**](version.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="229cd-111">*dispinterface-Name*</span><span class="sxs-lookup"><span data-stu-id="229cd-111">*dispinterface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="229cd-112">Der Name, mit dem die **dispinterface** in der Typbibliothek bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="229cd-112">The name by which the **dispinterface** is known in the type library.</span></span> <span data-ttu-id="229cd-113">Dieser Name muss innerhalb der Typbibliothek eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="229cd-113">This name must be unique within the type library.</span></span>

</dd> <dt>

<span data-ttu-id="229cd-114">*Eigenschaften Liste*</span><span class="sxs-lookup"><span data-stu-id="229cd-114">*property-list*</span></span> 
</dt> <dd>

<span data-ttu-id="229cd-115">(Syntax 1) Eine optionale Liste der Eigenschaften, die vom-Objekt unterstützt und in Form von Variablen deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="229cd-115">(Syntax 1) An optional list of properties supported by the object, declared in the form of variables.</span></span> <span data-ttu-id="229cd-116">Dies ist die Kurzform zum Deklarieren der Eigenschafts Funktionen in der Methoden Liste.</span><span class="sxs-lookup"><span data-stu-id="229cd-116">This is the short form for declaring the property functions in the methods list.</span></span> <span data-ttu-id="229cd-117">Weitere Informationen finden Sie im Abschnitt "Kommentare".</span><span class="sxs-lookup"><span data-stu-id="229cd-117">See the comments section for details.</span></span>

</dd> <dt>

<span data-ttu-id="229cd-118">*Methoden Liste*</span><span class="sxs-lookup"><span data-stu-id="229cd-118">*method-list*</span></span> 
</dt> <dd>

<span data-ttu-id="229cd-119">(Syntax 1) Eine Liste, die einen Funktionsprototyp für jede Methode und Eigenschaft in der **dispinterface** enthält.</span><span class="sxs-lookup"><span data-stu-id="229cd-119">(Syntax 1) A list comprising a function prototype for each method and property in the **dispinterface**.</span></span> <span data-ttu-id="229cd-120">Eine beliebige Anzahl von Funktionsdefinitionen kann in " *methlist*" angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="229cd-120">Any number of function definitions can appear in *methlist*.</span></span> <span data-ttu-id="229cd-121">Eine Funktion in " *methlist* " weist die folgende Form auf:</span><span class="sxs-lookup"><span data-stu-id="229cd-121">A function in *methlist* has the following form:</span></span>

<span data-ttu-id="229cd-122">**\[  Attribute \]** *returnType methname Type paramName ***(*** Parametern \* \* *);**</span><span class="sxs-lookup"><span data-stu-id="229cd-122">**\[***attributes***\]** *returntype methname type paramname ***(*** params\*\*\*);*\*</span></span>

<span data-ttu-id="229cd-123">Die folgenden Attribute werden für eine Methode in einer " **dispinterface**"-Methode akzeptiert: **\[ HelpString \]**, **\[ HelpContext \]**, **\[** [**propget**](propget.md) **\]** , **\[** [**PROPPUT**](propput.md) **\]** , **\[** [**PROPPUTREF**](propputref.md) **\]** , **\[** [**String**](string.md) **\]** und **\[** [**vararg**](vararg.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="229cd-123">The following attributes are accepted on a method in a **dispinterface**: **\[helpstring\]**, **\[helpcontext\]**, **\[**[**propget**](propget.md)**\]**, **\[**[**propput**](propput.md)**\]**, **\[**[**propputref**](propputref.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**vararg**](vararg.md)**\]**.</span></span> <span data-ttu-id="229cd-124">Wenn **\[ vararg \]** angegeben ist, muss der letzte Parameter ein sicheres Array vom **Variant** -Typ sein.</span><span class="sxs-lookup"><span data-stu-id="229cd-124">If **\[vararg\]** is specified, the last parameter must be a safe array of **VARIANT** type.</span></span>

<span data-ttu-id="229cd-125">Die Parameterliste ist eine durch Trennzeichen getrennte Liste, von der jedes Element die folgende Form aufweist:</span><span class="sxs-lookup"><span data-stu-id="229cd-125">The parameter list is a comma-delimited list, each element of which has the following form:</span></span>

<span data-ttu-id="229cd-126">**\[***legt***\]**</span><span class="sxs-lookup"><span data-stu-id="229cd-126">**\[***attributes***\]**</span></span>

<span data-ttu-id="229cd-127">Der *Typ* kann ein beliebiger deklarierter oder integrierter Typ oder ein Zeiger auf einen beliebigen Typ sein.</span><span class="sxs-lookup"><span data-stu-id="229cd-127">The *type* can be any declared or built-in type, or a pointer to any type.</span></span> <span data-ttu-id="229cd-128">Attribute für Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="229cd-128">Attributes on parameters are:</span></span>

<span data-ttu-id="229cd-129">**\[**[**in**](in.md) **\]** , **\[** [**out**](out-idl.md) **\]** , **\[** [**optional**](optional.md) **\]** , **\[ Zeichen \] Folge**</span><span class="sxs-lookup"><span data-stu-id="229cd-129">**\[**[**in**](in.md)**\]**, **\[**[**out**](out-idl.md)**\]**, **\[**[**optional**](optional.md)**\]**, **\[string\]**</span></span>

</dd> <dt>

<span data-ttu-id="229cd-130">*Schnittstellen Name*</span><span class="sxs-lookup"><span data-stu-id="229cd-130">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="229cd-131">(Syntax 2) Der Name der Schnittstelle, die als IDispatch-Schnittstelle deklariert werden soll.</span><span class="sxs-lookup"><span data-stu-id="229cd-131">(Syntax 2) The name of the interface to declare as an IDispatch interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="229cd-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="229cd-132">Remarks</span></span>

<span data-ttu-id="229cd-133">Der mittlerer l-Compiler akzeptiert die folgende Parameter Reihenfolge (von links nach rechts):</span><span class="sxs-lookup"><span data-stu-id="229cd-133">The MIDL compiler accepts the following parameter ordering (from left-to-right):</span></span>

1.  <span data-ttu-id="229cd-134">Erforderliche Parameter (Parameter, die nicht über das \[ DefaultValue \] - \[ Attribut oder optionale \] Attribute verfügen)</span><span class="sxs-lookup"><span data-stu-id="229cd-134">Required parameters (parameters that do not have the \[defaultvalue\] or \[optional\] attributes),</span></span>
2.  <span data-ttu-id="229cd-135">optionale Parameter mit oder ohne das \[ DefaultValue- \] Attribut</span><span class="sxs-lookup"><span data-stu-id="229cd-135">optional parameters with or without the \[defaultvalue\] attribute,</span></span>
3.  <span data-ttu-id="229cd-136">Parameter mit dem \[ optionalen \] -Attribut und ohne das \[ DefaultValue- \] Attribut</span><span class="sxs-lookup"><span data-stu-id="229cd-136">parameters with the \[optional\] attribute and without the \[defaultvalue\] attribute,</span></span>
4.  <span data-ttu-id="229cd-137">\[[**LCID**](lcid.md) - \] Parameter (falls vorhanden)</span><span class="sxs-lookup"><span data-stu-id="229cd-137">\[ [**lcid**](lcid.md)\] parameter, if any,</span></span>
5.  <span data-ttu-id="229cd-138">\[[**retval**](retval.md) \] Parame</span><span class="sxs-lookup"><span data-stu-id="229cd-138">\[ [**retval**](retval.md)\] parameter</span></span>

<span data-ttu-id="229cd-139">Methoden Funktionen werden genau so angegeben, wie Sie auf der Referenzseite für das [**Modul**](module.md) beschrieben werden, außer dass das \[ Attribut [**Entry**](entry.md) \] nicht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="229cd-139">Method functions are specified exactly as described in the reference page for [**module**](module.md) except that the \[ [**entry**](entry.md)\] attribute is not allowed.</span></span> <span data-ttu-id="229cd-140">Beachten Sie, dass STDOLE32. TLB (stdole). TLB auf 16-Bit-Systemen) muss importiert werden, da eine **dispinterface** von IDispatch erbt.</span><span class="sxs-lookup"><span data-stu-id="229cd-140">Note that STDOLE32.TLB (STDOLE.TLB on 16-bit systems) must be imported, because a **dispinterface** inherits from IDispatch.</span></span>

<span data-ttu-id="229cd-141">Sie können Eigenschaften in den Listen Eigenschaften oder Methoden deklarieren.</span><span class="sxs-lookup"><span data-stu-id="229cd-141">You can declare properties in either the properties or methods lists.</span></span> <span data-ttu-id="229cd-142">Das Deklarieren von Eigenschaften in der Eigenschaften Liste gibt nicht den Zugriffstyp an, den die Eigenschaft unterstützt (d. h. Get, Put oder PutRef).</span><span class="sxs-lookup"><span data-stu-id="229cd-142">Declaring properties in the properties list does not indicate the type of access the property supports (that is, get, put, or putref).</span></span> <span data-ttu-id="229cd-143">Geben Sie das Attribut "schreibgeschützt" \[ [](readonly.md) \] für Eigenschaften an, die Put oder PutRef nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="229cd-143">Specify the \[ [**readonly**](readonly.md)\] attribute for properties that don't support put or putref.</span></span> <span data-ttu-id="229cd-144">Wenn Sie die Eigenschaften Funktionen in der Liste der Methoden deklarieren, haben Funktionen für eine Eigenschaft alle denselben Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="229cd-144">If you declare the property functions in the methods list, functions for one property all have the same identifier.</span></span>

<span data-ttu-id="229cd-145">Mithilfe der ersten Syntax sind die-und-Methoden: Tags erforderlich.</span><span class="sxs-lookup"><span data-stu-id="229cd-145">Using the first syntax, the properties: and methods: tags are required.</span></span> <span data-ttu-id="229cd-146">Das \[ [**ID**](id.md) - \] Attribut ist auch für jedes Element erforderlich.</span><span class="sxs-lookup"><span data-stu-id="229cd-146">The \[ [**id**](id.md)\] attribute is also required on each member.</span></span> <span data-ttu-id="229cd-147">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="229cd-147">For example:</span></span>

``` syntax
properties: 
    [id(0)] int Value;    // Default property. 
methods: 
    [id(1)] HRESULT Show();
```

<span data-ttu-id="229cd-148">Anders als bei Schnittstellenmembern können dispinterface-Member das [**retval**](retval.md) -Attribut nicht verwenden, um einen Wert zusätzlich zu einem HRESULT-Fehlercode zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="229cd-148">Unlike interface members, dispinterface members cannot use the [**retval**](retval.md) attribute to return a value in addition to an HRESULT error code.</span></span> <span data-ttu-id="229cd-149">Das \[ [**LCID**](lcid.md) - \] Attribut ist für dispinterfaces ebenso ungültig, da IDispatch:: Aufrufen eine LCID übergibt.</span><span class="sxs-lookup"><span data-stu-id="229cd-149">The \[ [**lcid**](lcid.md)\] attribute is likewise invalid for dispinterfaces, because IDispatch::Invoke passes an LCID.</span></span> <span data-ttu-id="229cd-150">Es ist jedoch möglich, eine Schnittstelle, die diese Attribute verwendet, erneut zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="229cd-150">However, it is possible to redeclare an interface that uses these attributes.</span></span>

<span data-ttu-id="229cd-151">Mithilfe der zweiten Syntax können Schnittstellen, die IDispatch unterstützen und zuvor in einem ODL-Skript deklariert wurden, wie folgt als IDispatch-Schnittstellen neu deklariert werden:</span><span class="sxs-lookup"><span data-stu-id="229cd-151">Using the second syntax, interfaces that support IDispatch and are declared earlier in an ODL script can be redeclared as IDispatch interfaces as follows:</span></span>

``` syntax
dispinterface helloPro 
{ 
    interface hello; 
};
```

<span data-ttu-id="229cd-152">Im vorherigen Beispiel werden alle Member von Hello und alle Member deklariert, die Hello als Unterstützung von IDispatch erbt.</span><span class="sxs-lookup"><span data-stu-id="229cd-152">The preceding example declares all the members of hello and all the members that hello inherits as supporting IDispatch.</span></span> <span data-ttu-id="229cd-153">In diesem Fall \[ \] \[ \] würde MkTypLib jeden \[ LCID- \] Parameter und den HRESULT-Rückgabetyp entfernen und stattdessen den Rückgabetyp als den \[ retval- \] Parameter markieren, wenn Hello früher mit LCID-und retval-Membern deklariert wurde, die HRESULTs zurückgegeben haben.</span><span class="sxs-lookup"><span data-stu-id="229cd-153">In this case, if hello were declared earlier with \[lcid\] and \[retval\] members that returned HRESULTs, MkTypLib would remove each \[lcid\] parameter and HRESULT return type, and instead mark the return type as that of the \[retval\] parameter.</span></span>

> [!Note]  
> <span data-ttu-id="229cd-154">Das Mktyplib.exe Tool ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="229cd-154">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="229cd-155">Verwenden Sie stattdessen den Mittel l-Compiler.</span><span class="sxs-lookup"><span data-stu-id="229cd-155">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="229cd-156">Die Eigenschaften und Methoden einer dispinterface sind nicht Teil der VTBL von dispinterface.</span><span class="sxs-lookup"><span data-stu-id="229cd-156">The properties and methods of a dispinterface are not part of the VTBL of the dispinterface.</span></span> <span data-ttu-id="229cd-157">Folglich können [](/windows/win32/api/oleauto/nf-oleauto-createstddispatch) mit "" "" " [](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) " "" "" "" "" "" "" mit "" "" "" "</span><span class="sxs-lookup"><span data-stu-id="229cd-157">Consequently, [CreateStdDispatch](/windows/win32/api/oleauto/nf-oleauto-createstddispatch) and [DispInvoke](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) cannot be used to implement IDispatch::Invoke.</span></span> <span data-ttu-id="229cd-158">Die dispinterface wird verwendet, wenn eine Anwendung vorhandene nicht-VTBL-Funktionen über Automation verfügbar machen muss.</span><span class="sxs-lookup"><span data-stu-id="229cd-158">The dispinterface is used when an application needs to expose existing non-VTBL functions through Automation.</span></span> <span data-ttu-id="229cd-159">Diese Anwendungen können IDispatch:: Call implementieren, indem Sie den dispidmember-Parameter untersuchen und die entsprechende Funktion direkt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="229cd-159">These applications can implement IDispatch::Invoke by examining the dispidMember parameter and directly calling the corresponding function.</span></span>

## <a name="examples"></a><span data-ttu-id="229cd-160">Beispiele</span><span class="sxs-lookup"><span data-stu-id="229cd-160">Examples</span></span>

``` syntax
[ 
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    version(1.0), 
    helpstring("Useful help string."), 
    helpcontext(2480)
] 
dispinterface MyDispatchObject 
{ 
    properties: 
        [id(1)] int x;    //An integer property named x 
        [id(2)] BSTR y;   //A string property named y 
    methods: 
        [id(3)] HRESULT show();    //No arguments, no result 
        [id(11)] int computeit(int inarg, double *outarg); 
}; 
 
[
    uuid(1e123456-1f3c-1069-996b-00dd010fe676)
] 
dispinterface MyObject 
{ 
    properties: 
    methods: 
        [id(1), propget, bindable, defaultbind, displaybind] long x(); 
 
        [id(1), propput, bindable, defaultbind, 
         displaybind] HRESULT x(long rhs); 
}
```

## <a name="see-also"></a><span data-ttu-id="229cd-161">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="229cd-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="229cd-162">**bindable**</span><span class="sxs-lookup"><span data-stu-id="229cd-162">**bindable**</span></span>](bindable.md)
</dt> <dt>

[<span data-ttu-id="229cd-163">**defaultbind**</span><span class="sxs-lookup"><span data-stu-id="229cd-163">**defaultbind**</span></span>](defaultbind.md)
</dt> <dt>

[<span data-ttu-id="229cd-164">**displaybind**</span><span class="sxs-lookup"><span data-stu-id="229cd-164">**displaybind**</span></span>](displaybind.md)
</dt> <dt>

[<span data-ttu-id="229cd-165">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="229cd-165">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="229cd-166">**helpfile**</span><span class="sxs-lookup"><span data-stu-id="229cd-166">**helpfile**</span></span>](helpfile.md)
</dt> <dt>

[<span data-ttu-id="229cd-167">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="229cd-167">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="229cd-168">**verbirgt**</span><span class="sxs-lookup"><span data-stu-id="229cd-168">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="229cd-169">**in**</span><span class="sxs-lookup"><span data-stu-id="229cd-169">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="229cd-170">**berfläche**</span><span class="sxs-lookup"><span data-stu-id="229cd-170">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="229cd-171">FUNCFLAGS</span><span class="sxs-lookup"><span data-stu-id="229cd-171">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="229cd-172">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="229cd-172">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="229cd-173">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="229cd-173">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="229cd-174">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="229cd-174">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="229cd-175">**optionale**</span><span class="sxs-lookup"><span data-stu-id="229cd-175">**optional**</span></span>](optional.md)
</dt> <dt>

[<span data-ttu-id="229cd-176">**vorgenommen**</span><span class="sxs-lookup"><span data-stu-id="229cd-176">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="229cd-177">**nonextensible**</span><span class="sxs-lookup"><span data-stu-id="229cd-177">**nonextensible**</span></span>](nonextensible.md)
</dt> <dt>

[<span data-ttu-id="229cd-178">**propget**</span><span class="sxs-lookup"><span data-stu-id="229cd-178">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="229cd-179">**propput**</span><span class="sxs-lookup"><span data-stu-id="229cd-179">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="229cd-180">**propputref**</span><span class="sxs-lookup"><span data-stu-id="229cd-180">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="229cd-181">**oleautomation**</span><span class="sxs-lookup"><span data-stu-id="229cd-181">**oleautomation**</span></span>](oleautomation.md)
</dt> <dt>

[<span data-ttu-id="229cd-182">**begrenz**</span><span class="sxs-lookup"><span data-stu-id="229cd-182">**restricted**</span></span>](restricted.md)
</dt> <dt>

[<span data-ttu-id="229cd-183">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="229cd-183">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="229cd-184">**UUID**</span><span class="sxs-lookup"><span data-stu-id="229cd-184">**uuid**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="229cd-185">**vararg**</span><span class="sxs-lookup"><span data-stu-id="229cd-185">**vararg**</span></span>](vararg.md)
</dt> <dt>

[<span data-ttu-id="229cd-186">**version**</span><span class="sxs-lookup"><span data-stu-id="229cd-186">**version**</span></span>](version.md)
</dt> </dl>

 

 