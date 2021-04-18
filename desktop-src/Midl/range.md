---
title: Bereichsattribut
description: Mit dem Attribut \ Range \ können Sie einen Bereich zulässiger Werte für Argumente oder Felder angeben, deren Werte zur Laufzeit festgelegt werden. Bei Verwendung mit einem Pipetyp gibt das-Attribut den zulässigen Bereich für die Anzahl von Elementen in den pipesegmenten an.
ms.assetid: 1609fea5-e82c-4389-b4f4-2cd8d0622cde
keywords:
- Bereichs Attribut-Mittel l
topic_type:
- apiref
api_name:
- range
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e095d420afc433c1f01a63dff51868e57efc50f4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106339475"
---
# <a name="range-attribute"></a><span data-ttu-id="de3e4-105">Bereichsattribut</span><span class="sxs-lookup"><span data-stu-id="de3e4-105">range attribute</span></span>

<span data-ttu-id="de3e4-106">Mit dem **\[ Range \]** -Attribut können Sie einen Bereich zulässiger Werte für Argumente oder Felder angeben, deren Werte zur Laufzeit festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="de3e4-106">The **\[range\]** attribute lets you specify a range of allowable values for arguments or fields whose values are set at run time.</span></span> <span data-ttu-id="de3e4-107">Bei Verwendung mit einem Pipetyp gibt das-Attribut den zulässigen Bereich für die Anzahl von Elementen in den pipesegmenten an.</span><span class="sxs-lookup"><span data-stu-id="de3e4-107">When used with a pipe type, the attribute specifies the allowable range for the count of elements in the pipe chunks.</span></span>

``` syntax
[range(low-val,high-val)] type-specifier declarator
```

## <a name="parameters"></a><span data-ttu-id="de3e4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="de3e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de3e4-109">*niedrig-Val*</span><span class="sxs-lookup"><span data-stu-id="de3e4-109">*low-val*</span></span> 
</dt> <dd>

<span data-ttu-id="de3e4-110">Der niedrigste zulässige Wert, den der-Parameter oder das-Feld enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="de3e4-110">The lowest allowable value that the parameter or field can hold.</span></span>

</dd> <dt>

<span data-ttu-id="de3e4-111">*High-Val*</span><span class="sxs-lookup"><span data-stu-id="de3e4-111">*high-val*</span></span> 
</dt> <dd>

<span data-ttu-id="de3e4-112">Der höchste zulässige Wert, den der-Parameter oder das-Feld enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="de3e4-112">The highest allowable value that the parameter or field can hold.</span></span>

</dd> <dt>

<span data-ttu-id="de3e4-113">*Typspezifizierer*</span><span class="sxs-lookup"><span data-stu-id="de3e4-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="de3e4-114">Ein ganzzahliger Typ, der nicht [**Hyper**](hyper.md) oder [**\_ \_ Int64**](--int64.md), ein Typbezeichner für einen ganzzahligen Typ, ein [**Enumeration**](enum.md) -Typ oder ein pipetypname ist.</span><span class="sxs-lookup"><span data-stu-id="de3e4-114">An integral type other than [**hyper**](hyper.md) or [**\_\_int64**](--int64.md), a type identifier to an integral type, an [**enum**](enum.md) type, or a pipe type name.</span></span>

</dd> <dt>

<span data-ttu-id="de3e4-115">*Deklarator*</span><span class="sxs-lookup"><span data-stu-id="de3e4-115">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="de3e4-116">Ein standardmäßiger C-Deklarator, z. b. ein Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="de3e4-116">A standard C declarator, such as an identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de3e4-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de3e4-117">Remarks</span></span>

<span data-ttu-id="de3e4-118">Verwenden Sie das **\[ Range \]** -Attribut, um die Bedeutung von sensiblen Parametern oder Feldern zu ändern, z. b. für die Größe oder Länge, mit konformen oder variierenden Arrays, oder wenn Sie einen Parameter-oder Feldwert auf einen Bereich gültiger Werte überprüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="de3e4-118">Use the **\[range\]** attribute to modify the meaning of sensitive parameters or fields, such as those used for size or length, with conformant or varying arrays; or whenever you want to check a parameter or field value against a range of valid values.</span></span> <span data-ttu-id="de3e4-119">Das-Attribut gilt sowohl für Parameter der obersten Ebene als auch für Parameter und Felder auf niedrigerer Ebene.</span><span class="sxs-lookup"><span data-stu-id="de3e4-119">The attribute is applicable to top-level parameters as well as lower-level parameters and fields.</span></span> <span data-ttu-id="de3e4-120">Durch das Hinzufügen des **\[ Range \]** -Attributs zu einem Typ wird das Wire-Format nicht geändert, und die Abwärtskompatibilität wird daher nicht beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="de3e4-120">Adding the **\[range\]** attribute to a type does not change its wire format, thus does not affect backward compatibility.</span></span>

<span data-ttu-id="de3e4-121">Das **\[ Range \]** -Attribut kann auch für konforme Daten wie z. b. Puffer oder Arrays mit einem Konformitäts Attribut verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="de3e4-121">The **\[range\]** attribute can also be used on conformant data such as buffers or arrays with a conformance attribute.</span></span> <span data-ttu-id="de3e4-122">Der Effekt besteht darin, alle Konformitäts Größen für die konformen Daten auf den angegebenen Bereich zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="de3e4-122">The effect is to limit all conformance sizes for the conformant data to the specified range.</span></span> <span data-ttu-id="de3e4-123">Wenn es sich bei den überein kompatiblen Daten um ein mehrdimensionales Array handelt, ist jede Array Dimension auf den angegebenen Bereich beschränkt.</span><span class="sxs-lookup"><span data-stu-id="de3e4-123">If the conformant data is a multi-dimensional array, each array dimension is limited to the specified range.</span></span>

<span data-ttu-id="de3e4-124">Die Verwendung des **\[ Bereichs \]** für konforme Daten erfordert, dass das Kompilierungs Ziel den Wert "nt60" oder höher hat.</span><span class="sxs-lookup"><span data-stu-id="de3e4-124">Use of **\[range\]** on conformant data requires that the compilation target be â€“target NT60 or higher.</span></span>

<span data-ttu-id="de3e4-125">Beachten Sie, dass Sie die [**/robust**](-robust.md) -Compileroption verwenden müssen, wenn Sie Ihre IDL-Datei kompilieren, um den Stub-Code zu generieren, der diese Überprüfungen durchführt.</span><span class="sxs-lookup"><span data-stu-id="de3e4-125">Note that you must use the [**/robust**](-robust.md) compiler option when you compile your IDL file in order to generate the stub code that will perform these checks.</span></span> <span data-ttu-id="de3e4-126">Ohne den Schalter **/robust** ignoriert der Mittell-Compiler dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="de3e4-126">Without the **/robust** switch, the MIDL compiler ignores this attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="de3e4-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="de3e4-127">Examples</span></span>

``` syntax
HRESULT Method1(
    [in, range(0,100)] ULONG m,
    [in, range(0,100)] ULONG n,
    [size_is(m,n)] ULONG **pplong);

void InPipe(
    [in, range(0, MAX_CHUNK) LONG_PIPE pipe_date);
```

## <a name="see-also"></a><span data-ttu-id="de3e4-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="de3e4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de3e4-129">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="de3e4-129">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="de3e4-130">Arrays</span><span class="sxs-lookup"><span data-stu-id="de3e4-130">arrays</span></span>](/windows/desktop/Rpc/arrays)
</dt> <dt>

[<span data-ttu-id="de3e4-131">**der erste \_ ist**</span><span class="sxs-lookup"><span data-stu-id="de3e4-131">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="de3e4-132">**Letzter \_ ist**</span><span class="sxs-lookup"><span data-stu-id="de3e4-132">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="de3e4-133">**Länge \_ ist**</span><span class="sxs-lookup"><span data-stu-id="de3e4-133">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="de3e4-134">**Max \_ ist**</span><span class="sxs-lookup"><span data-stu-id="de3e4-134">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="de3e4-135">**/robust**</span><span class="sxs-lookup"><span data-stu-id="de3e4-135">**/robust**</span></span>](-robust.md)
</dt> <dt>

[<span data-ttu-id="de3e4-136">**Größe \_ :**</span><span class="sxs-lookup"><span data-stu-id="de3e4-136">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="de3e4-137">**Switch \_ ist**</span><span class="sxs-lookup"><span data-stu-id="de3e4-137">**switch\_is**</span></span>](switch-is.md)
</dt> </dl>

 

 