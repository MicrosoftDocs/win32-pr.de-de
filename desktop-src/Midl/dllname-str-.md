---
title: dllname (Str)-Attribut
description: Das Attribut \ dllName \ definiert den Namen der dll, die die Einstiegspunkte für ein Modul enthält.
ms.assetid: dbf062ce-9dcc-4cc6-b7cd-cdc5945e399b
keywords:
- dllname (Str)-Attribut (Mittel l)
topic_type:
- apiref
api_name:
- dllname(str)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 990d277db855c2988021d19a0a756c49454546f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038975"
---
# <a name="dllnamestr-attribute"></a><span data-ttu-id="d4d46-104">dllname (Str)-Attribut</span><span class="sxs-lookup"><span data-stu-id="d4d46-104">dllname(str) attribute</span></span>

<span data-ttu-id="d4d46-105">Das **\[ dllName \]** -Attribut definiert den Namen der dll, die die Einstiegspunkte für ein Modul enthält.</span><span class="sxs-lookup"><span data-stu-id="d4d46-105">The **\[dllname\]** attribute defines the name of the DLL that contains the entry points for a module.</span></span>

``` syntax
[
    uuid(uuid-number), 
    dllname("filename")
    [, optional-attribute-list]
]
module modulename
{
    elementlist
};
```

## <a name="parameters"></a><span data-ttu-id="d4d46-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4d46-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4d46-107">*UUID-Nummer*</span><span class="sxs-lookup"><span data-stu-id="d4d46-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="d4d46-108">Gibt eine universell eindeutige ID für das [**Modul**](module.md)an.</span><span class="sxs-lookup"><span data-stu-id="d4d46-108">Specifies a universally unique identification number for the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4d46-109">*filename*</span><span class="sxs-lookup"><span data-stu-id="d4d46-109">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="d4d46-110">Gibt eine NULL-terminierte Zeichenfolge an, die den vollständigen Pfad zur DLL-Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="d4d46-110">Specifies a NULL-terminated string which contains the full path to the Dll file.</span></span>

</dd> <dt>

<span data-ttu-id="d4d46-111">*optional-Attribut-List*</span><span class="sxs-lookup"><span data-stu-id="d4d46-111">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d4d46-112">Gibt eine Liste von 0 (null) oder mehr Attributen der Mittelwert Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="d4d46-112">Specifies a list of zero or more MIDL interface attributes.</span></span>

</dd> <dt>

<span data-ttu-id="d4d46-113">*ModuleName*</span><span class="sxs-lookup"><span data-stu-id="d4d46-113">*modulename*</span></span> 
</dt> <dd>

<span data-ttu-id="d4d46-114">Gibt den Namen an, den andere Softwarekomponenten verwenden können, um auf das Modul zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="d4d46-114">Specifies the name which other software components can use to refer to the module.</span></span>

</dd> <dt>

<span data-ttu-id="d4d46-115">*Elementliste*</span><span class="sxs-lookup"><span data-stu-id="d4d46-115">*elementlist*</span></span> 
</dt> <dd>

<span data-ttu-id="d4d46-116">Gibt mindestens eine Modul Element Definitions-Anweisung an.</span><span class="sxs-lookup"><span data-stu-id="d4d46-116">Specifies one or more module element definition statements.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4d46-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4d46-117">Remarks</span></span>

<span data-ttu-id="d4d46-118">Das **\[ dllName \]** -Attribut ist in einem Modul erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d4d46-118">The **\[dllname\]** attribute is required on a module.</span></span>

## <a name="examples"></a><span data-ttu-id="d4d46-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4d46-119">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("A meaningful comment"),   
    dllname("HANDY.DLL")
] 
module HandyStuff
{
    /* Module content definitions */
};
```

## <a name="see-also"></a><span data-ttu-id="d4d46-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d4d46-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4d46-121">**Mond**</span><span class="sxs-lookup"><span data-stu-id="d4d46-121">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="d4d46-122">**ein**</span><span class="sxs-lookup"><span data-stu-id="d4d46-122">**entry**</span></span>](entry.md)
</dt> <dt>

[<span data-ttu-id="d4d46-123">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="d4d46-123">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="d4d46-124">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="d4d46-124">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="d4d46-125">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="d4d46-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 