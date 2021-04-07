---
title: usesgetlasterror-Attribut
description: Das Attribut \ "\"-GetLastError \ "signalisiert dem Aufrufer, dass GetLastError aufgerufen werden kann, um den Fehlercode abzurufen.
ms.assetid: 8e9ab8b5-f446-4aab-bb40-b6f78799e18e
keywords:
- attributgetlasterror-Attribut (Mittel l)
topic_type:
- apiref
api_name:
- usesgetlasterror
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0f403430f70fde71696ec2a35a34161f08bada9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725137"
---
# <a name="usesgetlasterror-attribute"></a><span data-ttu-id="dc52e-104">usesgetlasterror-Attribut</span><span class="sxs-lookup"><span data-stu-id="dc52e-104">usesgetlasterror attribute</span></span>

<span data-ttu-id="dc52e-105">Das Attribut "$ **\[ GetLastError \]** " signalisiert dem Aufrufer, dass es [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) aufrufen kann, um den Fehlercode abzurufen.</span><span class="sxs-lookup"><span data-stu-id="dc52e-105">The **\[usesgetlasterror\]** attribute signals the caller that it can call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to retrieve the error code.</span></span>

``` syntax
[
    module-attributes
]
module module-name
{
    [entry(entry-id), usesgetlasterror [, other-attributes]] return-type function-name(param-list);
};
```

## <a name="parameters"></a><span data-ttu-id="dc52e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc52e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc52e-107">*Module-Attribute*</span><span class="sxs-lookup"><span data-stu-id="dc52e-107">*module-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="dc52e-108">NULL oder mehr mittlere Attribute, die auf das [**Modul**](module.md)angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="dc52e-108">Zero or more MIDL attributes that will be applied to the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc52e-109">*Modulname*</span><span class="sxs-lookup"><span data-stu-id="dc52e-109">*module-name*</span></span> 
</dt> <dd>

<span data-ttu-id="dc52e-110">Der Bezeichnername des [**Moduls**](module.md).</span><span class="sxs-lookup"><span data-stu-id="dc52e-110">The identifier name of the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc52e-111">*Eintrags-ID*</span><span class="sxs-lookup"><span data-stu-id="dc52e-111">*entry-id*</span></span> 
</dt> <dd>

<span data-ttu-id="dc52e-112">Gibt den Einstiegspunkt des Moduls an – Funktionsname oder ganzzahlige Identifikationsnummer.</span><span class="sxs-lookup"><span data-stu-id="dc52e-112">Specifies the module entry point–function name or integer-identification number.</span></span>

</dd> <dt>

<span data-ttu-id="dc52e-113">*andere-Attribute*</span><span class="sxs-lookup"><span data-stu-id="dc52e-113">*other-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="dc52e-114">NULL oder mehr mittlere Attribute, die auf die Remote Prozedur angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="dc52e-114">Zero or more MIDL attributes that will be applied to the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="dc52e-115">*Rückgabetyp*</span><span class="sxs-lookup"><span data-stu-id="dc52e-115">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="dc52e-116">Der Typ der Daten, die von der Remote Prozedur bei Abschluss zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="dc52e-116">The type of the data that the remote procedure will return upon completion.</span></span>

</dd> <dt>

<span data-ttu-id="dc52e-117">*function-name*</span><span class="sxs-lookup"><span data-stu-id="dc52e-117">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="dc52e-118">Der Name der Remote Prozedur, wie in der IDL-Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="dc52e-118">The name of the remote procedure as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="dc52e-119">*param-Liste*</span><span class="sxs-lookup"><span data-stu-id="dc52e-119">*param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="dc52e-120">NULL oder mehr Parameter für die Remote Prozedur.</span><span class="sxs-lookup"><span data-stu-id="dc52e-120">Zero or more parameters to the remote procedure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc52e-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc52e-121">Remarks</span></span>

<span data-ttu-id="dc52e-122">Das **\[ usesgetlasterror \]** -Attribut kann für einen Modul Einstiegspunkt festgelegt werden, wenn der Einstiegspunkt die Windows-Funktion [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) zum Zurückgeben von Fehlercodes verwendet.</span><span class="sxs-lookup"><span data-stu-id="dc52e-122">The **\[usesgetlasterror\]** attribute can be set on a module entry point, if that entry point uses the Windows function [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to return error codes.</span></span> <span data-ttu-id="dc52e-123">Das-Attribut teilt dem Aufrufer mit, dass der Aufrufer dann [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) aufrufen kann, um den Fehlercode abzurufen, wenn beim Aufrufen der Funktion ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="dc52e-123">The attribute tells the caller that, if there is an error when calling that function, the caller can then call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to retrieve the error code.</span></span>

## <a name="examples"></a><span data-ttu-id="dc52e-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc52e-124">Examples</span></span>

``` syntax
[
    dllname("MyOwn.dll")
] 
module MyModule
{
    [entry("One"), usesgetlasterror, bindable, requestedit,
     propputref, defaultbind] HRESULT Func1(
         [in]IUnknown * iParam1, 
         [out] long * Param2) ;
    [entry("TwentyOne"), usesgetlasterror, 
     hidden, vararg] SAFEARRAY (int) Func2(
         [in, out] SAFEARRAY (variant) *varP) ;

    // Other module definition statements.
};
```

## <a name="see-also"></a><span data-ttu-id="dc52e-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="dc52e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc52e-126">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="dc52e-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="dc52e-127">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="dc52e-127">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="dc52e-128">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="dc52e-128">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 