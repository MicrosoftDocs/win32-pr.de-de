---
title: importlib-Attribut
description: Die "\ importlib \"-Direktive macht Typen, die bereits in einer anderen Typbibliothek kompiliert wurden, für die zu erstellende Typbibliothek verfügbar.
ms.assetid: d5f15a77-c6b1-4918-be86-07d2995ca2d4
keywords:
- importlib-Attribut-Mittel l
topic_type:
- apiref
api_name:
- importlib
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b9c233103330e9f8ae7318a613cbc5103315a74
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472765"
---
# <a name="importlib-attribute"></a><span data-ttu-id="6cc48-104">importlib-Attribut</span><span class="sxs-lookup"><span data-stu-id="6cc48-104">importlib attribute</span></span>

<span data-ttu-id="6cc48-105">Die **\[ importlib \]** -Direktive macht Typen, die bereits in einer anderen Typbibliothek kompiliert wurden, für die zu erstellende Typbibliothek verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6cc48-105">The **\[importlib\]** directive makes types that have already been compiled into another type library available to the type library being created.</span></span>

``` syntax
[
    library-attributes
]
library (library-name)
{
    importlib(file-to-import); 
    ... 
}
```

## <a name="parameters"></a><span data-ttu-id="6cc48-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6cc48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cc48-107">*Bibliothek-Attribute*</span><span class="sxs-lookup"><span data-stu-id="6cc48-107">*library-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="6cc48-108">0 (null) oder mehr Attribute, die auf die Bibliothek angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="6cc48-108">Zero or more attributes that will be applied to the library.</span></span>

</dd> <dt>

<span data-ttu-id="6cc48-109">*Bibliotheksname*</span><span class="sxs-lookup"><span data-stu-id="6cc48-109">*library-name*</span></span> 
</dt> <dd>

<span data-ttu-id="6cc48-110">Der Bezeichner, der von Softwarekomponenten verwendet wird, um diese [**Bibliothek**](library.md)zu kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="6cc48-110">The identifier that software components will use to denote this [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cc48-111">*zu importierende Datei*</span><span class="sxs-lookup"><span data-stu-id="6cc48-111">*file-to-import*</span></span> 
</dt> <dd>

<span data-ttu-id="6cc48-112">Der Name und Speicherort der importierten Datei zur mittleren Kompilierzeit.</span><span class="sxs-lookup"><span data-stu-id="6cc48-112">The name and location of the imported file at MIDL compile-time.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6cc48-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6cc48-113">Remarks</span></span>

<span data-ttu-id="6cc48-114">Alle **\[ importlib \]** -Direktiven müssen den anderen Typbeschreibungen in der Bibliothek vorangestellt sein.</span><span class="sxs-lookup"><span data-stu-id="6cc48-114">All **\[importlib\]** directives must precede the other type descriptions in the library.</span></span> <span data-ttu-id="6cc48-115">Beachten Sie, dass sowohl die importierte Bibliothek als auch die generierte Bibliothek mit der Anwendung verteilt werden müssen, damit Sie zur Laufzeit verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6cc48-115">Note that the imported library, as well as the generated library, must be distributed with the application so that it is available at run time.</span></span>

<span data-ttu-id="6cc48-116">In den meisten Fällen sollten Sie die **\[** [](import.md) **\]** Direktive Import Direktive verwenden, um auf Definitionen von einem anderen zu verweisen. IDL-Datei in Ihrem. IDL-Datei.</span><span class="sxs-lookup"><span data-stu-id="6cc48-116">In most cases you should use the MIDL **\[**[**import**](import.md)**\]** directive to reference definitions from another .IDL file in your .IDL file.</span></span> <span data-ttu-id="6cc48-117">Diese Methode stellt die Typbibliothek mit allen Informationen aus der ursprünglichen Datei bereit, während **\[ importlib \]** nur den Inhalt der Typbibliothek enthält.</span><span class="sxs-lookup"><span data-stu-id="6cc48-117">This method provides your type library with all the information from the original file, whereas **\[importlib\]** only brings in the contents of the type library.</span></span>

> [!Note]  
> <span data-ttu-id="6cc48-118">Die **\[ importlib \]** -Direktive macht den in der importierten Bibliothek definierten Typ innerhalb der zu kompilierende Bibliothek zugänglich.</span><span class="sxs-lookup"><span data-stu-id="6cc48-118">The **\[importlib\]** directive makes any type defined in the imported library accessible from within the library being compiled.</span></span> <span data-ttu-id="6cc48-119">Um Mehrdeutigkeit zu vermeiden, wenn doppelte Verweise vorhanden sind, wird empfohlen, dass Sie jeden Verweis mit dem entsprechenden Bibliotheksnamen wie folgt qualifizieren:</span><span class="sxs-lookup"><span data-stu-id="6cc48-119">To avoid ambiguity when there are duplicate references, we recommend that you qualify each such reference with the appropriate library name, as follows:</span></span>

 

``` syntax
library_name.type
```

<span data-ttu-id="6cc48-120">Wenn diese Qualifizierung nicht vorhanden ist, löst die Mittel l die doppelte Verweis Mehrdeutigkeit wie folgt auf:</span><span class="sxs-lookup"><span data-stu-id="6cc48-120">In the absence of such qualification, MIDL resolves duplicate reference ambiguity as follows:</span></span>

-   <span data-ttu-id="6cc48-121">Ab Version 3,1 verwendet die Mittel l den ersten gefundenen Verweis.</span><span class="sxs-lookup"><span data-stu-id="6cc48-121">Effective with version 3.1, MIDL uses the first reference it finds.</span></span>
-   <span data-ttu-id="6cc48-122">In Version 3,0 von "Mittel l", der ersten Version von "Mittel l", die Typbibliotheken generieren konnte, wird der letzte gefundene Verweis verwendet.</span><span class="sxs-lookup"><span data-stu-id="6cc48-122">Version 3.0 of MIDL, the first version of MIDL that could generate type libraries, uses the last reference it found.</span></span>

## <a name="examples"></a><span data-ttu-id="6cc48-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6cc48-123">Examples</span></span>

``` syntax
library BrowseHelper 
{ 
    importlib("stdole32.tlb"); 
    importlib("mydisp.tlb"); 
    //Remainder of library definition 
};
```

## <a name="see-also"></a><span data-ttu-id="6cc48-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6cc48-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cc48-125">**Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="6cc48-125">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="6cc48-126">**Importieren**</span><span class="sxs-lookup"><span data-stu-id="6cc48-126">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="6cc48-127">Importieren von System-Headerdateien</span><span class="sxs-lookup"><span data-stu-id="6cc48-127">Importing System Header Files</span></span>](importing-system-header-files.md)
</dt> <dt>

[<span data-ttu-id="6cc48-128">Importieren von Dateien und Typbibliotheken</span><span class="sxs-lookup"><span data-stu-id="6cc48-128">Importing Files and Type Libraries</span></span>](importing-files-and-type-libraries.md)
</dt> <dt>

[<span data-ttu-id="6cc48-129">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="6cc48-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="6cc48-130">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="6cc48-130">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="6cc48-131">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="6cc48-131">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 