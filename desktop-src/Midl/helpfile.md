---
title: helpfile-Attribut
description: Das Attribut \ HelpFile \ legt den Namen der Hilfedatei für eine Typbibliothek fest. Alle Typen in einer Bibliothek verwenden dieselbe Hilfedatei.
ms.assetid: caa248b1-a1a7-4c36-886a-079a66a01907
keywords:
- HelpFile-Attribut-Mittel l
topic_type:
- apiref
api_name:
- helpfile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0b4283b0285631a710af774d364a01b82c9d44b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725161"
---
# <a name="helpfile-attribute"></a><span data-ttu-id="6e562-105">helpfile-Attribut</span><span class="sxs-lookup"><span data-stu-id="6e562-105">helpfile attribute</span></span>

<span data-ttu-id="6e562-106">Das **\[ HelpFile \]** -Attribut legt den Namen der Hilfedatei für eine Typbibliothek fest.</span><span class="sxs-lookup"><span data-stu-id="6e562-106">The **\[helpfile\]** attribute sets the name of the Help file for a type library.</span></span> <span data-ttu-id="6e562-107">Alle Typen in einer Bibliothek verwenden dieselbe Hilfedatei.</span><span class="sxs-lookup"><span data-stu-id="6e562-107">All types in a library share the same Help file.</span></span>

``` syntax
[
    uuid(uuid-number), 
    helpfile("filename") 
    [, optional-attribute-list]
] 
library 
{
    library statements
};
```

## <a name="parameters"></a><span data-ttu-id="6e562-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e562-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e562-109">*UUID-Nummer*</span><span class="sxs-lookup"><span data-stu-id="6e562-109">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="6e562-110">Gibt eine universell eindeutige Identifikationsnummer für die [**Bibliothek**](library.md)an.</span><span class="sxs-lookup"><span data-stu-id="6e562-110">Specifies a universally unique identification number for the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e562-111">*filename*</span><span class="sxs-lookup"><span data-stu-id="6e562-111">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="6e562-112">Gibt den Namen der Datei an, die den Hilfetext enthält.</span><span class="sxs-lookup"><span data-stu-id="6e562-112">Specifies the name of the file containing the help text.</span></span>

</dd> <dt>

<span data-ttu-id="6e562-113">*optional-Attribut-List*</span><span class="sxs-lookup"><span data-stu-id="6e562-113">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="6e562-114">Gibt 0 (null) oder mehr Attribute an, die der mittlerer l-Compiler auf die [**Bibliothek**](library.md)anwendet.</span><span class="sxs-lookup"><span data-stu-id="6e562-114">Specifies zero or more attributes that the MIDL compiler will apply to the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e562-115">*Bibliotheks Anweisungen*</span><span class="sxs-lookup"><span data-stu-id="6e562-115">*library statements*</span></span> 
</dt> <dd>

<span data-ttu-id="6e562-116">Gibt eine oder mehrere Mittell-Anweisungen an, die die Bibliotheks Schnittstelle definieren.</span><span class="sxs-lookup"><span data-stu-id="6e562-116">Specifies one or more MIDL statements that define the library interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e562-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e562-117">Remarks</span></span>

<span data-ttu-id="6e562-118">Verwenden Sie die **GetDocumentation** -Funktionen in den Schnittstellen **ITypeLib** und **ITypeInfo** , um den Dateinamen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6e562-118">Use the **GetDocumentation** functions in the **ITypeLib** and **ITypeInfo** interfaces to retrieve the file name.</span></span>

## <a name="examples"></a><span data-ttu-id="6e562-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e562-119">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpfile("filename.hlp"),
    lcid(0x0409), 
    version(2.0)
]
library Hello
{
    /* Library definition statements here. */
};
```

## <a name="see-also"></a><span data-ttu-id="6e562-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6e562-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e562-121">**Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="6e562-121">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="6e562-122">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="6e562-122">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="6e562-123">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="6e562-123">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="6e562-124">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="6e562-124">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 