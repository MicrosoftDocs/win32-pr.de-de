---
title: Eingabeattribut
description: Das Attribut \ Entry \ gibt eine exportierte Funktion oder Konstante in einem Modul an, indem der Einstiegspunkt in der DLL identifiziert wird.
ms.assetid: 1d2d6429-d828-44ec-8b0a-cefb64c6e706
keywords:
- Eingabe Attribut-Mittel l
topic_type:
- apiref
api_name:
- entry
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e596284a83c48bcfc84ef4f7985aed7c33ba7da
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314744"
---
# <a name="entry-attribute"></a><span data-ttu-id="5de7f-104">Eingabeattribut</span><span class="sxs-lookup"><span data-stu-id="5de7f-104">entry attribute</span></span>

<span data-ttu-id="5de7f-105">Das Attribut **\[ Entry \]** gibt eine exportierte Funktion oder Konstante in einem Modul an, indem der Einstiegspunkt in der DLL identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="5de7f-105">The **\[entry\]** attribute specifies an exported function or constant in a module by identifying the entry point in the DLL.</span></span>

``` syntax
[
    uuid(uuid-number), 
    entry(entry-id)
  [, optional-attribute-list]
]
module modulename 
{
    elementlist
};
```

## <a name="parameters"></a><span data-ttu-id="5de7f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5de7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5de7f-107">*UUID-Nummer*</span><span class="sxs-lookup"><span data-stu-id="5de7f-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="5de7f-108">Gibt eine universell eindeutige ID für das [**Modul**](module.md)an.</span><span class="sxs-lookup"><span data-stu-id="5de7f-108">Specifies a universally unique identification number for the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="5de7f-109">*Eintrags-ID*</span><span class="sxs-lookup"><span data-stu-id="5de7f-109">*entry-id*</span></span> 
</dt> <dd>

<span data-ttu-id="5de7f-110">Gibt den Funktionsnamen oder die ganzzahlige Identifikationsnummer des Modul Einstiegs Punkts an.</span><span class="sxs-lookup"><span data-stu-id="5de7f-110">Specifies the module entry point function name or integer identification number.</span></span>

</dd> <dt>

<span data-ttu-id="5de7f-111">*optional-Attribut-List*</span><span class="sxs-lookup"><span data-stu-id="5de7f-111">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5de7f-112">Gibt 0 (null) oder mehr Attribute an, die der mittlerer l-Compiler auf das [**Modul**](module.md)anwenden soll.</span><span class="sxs-lookup"><span data-stu-id="5de7f-112">Specifies zero or more attributes for the MIDL compiler to apply to the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="5de7f-113">*ModuleName*</span><span class="sxs-lookup"><span data-stu-id="5de7f-113">*modulename*</span></span> 
</dt> <dd>

<span data-ttu-id="5de7f-114">Gibt den Namen an, den andere Softwarekomponenten verwenden, um das [**Modul**](module.md)zu kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="5de7f-114">Specifies the name other software components use to denote the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="5de7f-115">*Elementliste*</span><span class="sxs-lookup"><span data-stu-id="5de7f-115">*elementlist*</span></span> 
</dt> <dd>

<span data-ttu-id="5de7f-116">Gibt mindestens eine Modul Element Definitions-Anweisung an.</span><span class="sxs-lookup"><span data-stu-id="5de7f-116">Specifies one or more module element definition statements.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5de7f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5de7f-117">Remarks</span></span>

<span data-ttu-id="5de7f-118">Wenn die *EntryID* -Variable des **\[ Entry \]** -Attributs eine Zeichenfolge ist, ist dies ein benannter Einstiegspunkt.</span><span class="sxs-lookup"><span data-stu-id="5de7f-118">If the *entryid* variable of the **\[entry\]** attribute is a string, this is a named entry point.</span></span> <span data-ttu-id="5de7f-119">Wenn *EntryID* eine Zahl ist, wird der Einstiegspunkt durch eine Ordinalzahl definiert.</span><span class="sxs-lookup"><span data-stu-id="5de7f-119">If *entryid* is a number, the entry point is defined by an ordinal.</span></span> <span data-ttu-id="5de7f-120">Dieses Attribut bietet eine Möglichkeit zum Abrufen der Adresse einer Funktion in einem Modul.</span><span class="sxs-lookup"><span data-stu-id="5de7f-120">This attribute provides a way to obtain the address of a function in a module.</span></span>

## <a name="examples"></a><span data-ttu-id="5de7f-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5de7f-121">Examples</span></span>

``` syntax
[
    dllname("MyAppsFirst.dll")
] 
module MyModule
{
    [entry(20), bindable, requestedit, 
     propputref, defaultbind ] HRESULT Func1(
         [in]IUnknown * Param1, 
         [out] MyType * Param2);
    [entry("TwentyOne"), hidden, vararg] SAFEARRAY (int) Func2(
        [in, out] SAFEARRAY (variant) *varP) ;
    [entry(22)] Float Func3(
        [in] lpstr pName, [in] double dLevel,
        [out] short * sByte) ;
    } ;
```

## <a name="see-also"></a><span data-ttu-id="5de7f-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5de7f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5de7f-123">**dllname**</span><span class="sxs-lookup"><span data-stu-id="5de7f-123">**dllname**</span></span>](dllname-str-.md)
</dt> <dt>

[<span data-ttu-id="5de7f-124">**Mond**</span><span class="sxs-lookup"><span data-stu-id="5de7f-124">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="5de7f-125">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="5de7f-125">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="5de7f-126">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="5de7f-126">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="5de7f-127">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="5de7f-127">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 