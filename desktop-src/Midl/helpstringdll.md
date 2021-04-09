---
title: Helpstringdll-Attribut
description: Mit dem Attribut \ Helpstringdll \ wird der Name der DLL festgelegt, die zum Durchführen einer Suche nach Dokument Zeichenfolgen verwendet werden soll.
ms.assetid: 1b9b962c-c355-4428-b5ea-dc7fd48b50a9
keywords:
- Helpstringdll-Attribut-Mittel l
topic_type:
- apiref
api_name:
- helpstringdll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dace4fb9ddc3908ce637cd2d8521a1ab4671d620
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948640"
---
# <a name="helpstringdll-attribute"></a><span data-ttu-id="1a161-104">Helpstringdll-Attribut</span><span class="sxs-lookup"><span data-stu-id="1a161-104">helpstringdll attribute</span></span>

<span data-ttu-id="1a161-105">Mit dem **\[ Helpstringdll \]** -Attribut wird der Name der DLL festgelegt, die zum Ausführen einer Dokument Zeichenfolgen-Suche verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1a161-105">The **\[helpstringdll\]** attribute sets the name of the DLL to use to perform a document string lookup.</span></span>

``` syntax
[
    helpstringdll(help-text-string)
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
};
```

## <a name="parameters"></a><span data-ttu-id="1a161-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a161-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a161-107">*Hilfe-Text Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="1a161-107">*help-text-string*</span></span> 
</dt> <dd>

<span data-ttu-id="1a161-108">Eine NULL terminierte Zeichenfolge, die den voll qualifizierten Dateinamen einer DLL angibt.</span><span class="sxs-lookup"><span data-stu-id="1a161-108">A zero-terminated string of characters specifying the fully qualified file name of a DLL.</span></span>

</dd> <dt>

<span data-ttu-id="1a161-109">*optional-Attribut-List*</span><span class="sxs-lookup"><span data-stu-id="1a161-109">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="1a161-110">Andere Attribute, die auf die Library-Anweisung als Ganzes angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a161-110">Other attributes that apply to the library statement as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="1a161-111">*Bibliotheksname*</span><span class="sxs-lookup"><span data-stu-id="1a161-111">*library-name*</span></span> 
</dt> <dd>

<span data-ttu-id="1a161-112">Der Bezeichner, der von Softwarekomponenten verwendet wird, um diese [**Bibliothek**](library.md)zu kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="1a161-112">The identifier that software components will use to denote this [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a161-113">*Library-Definition-Anweisungen*</span><span class="sxs-lookup"><span data-stu-id="1a161-113">*library-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="1a161-114">Eine oder mehrere Mittell-Anweisungen, die die-Schnittstelle der [**Bibliothek**](library.md)definieren.</span><span class="sxs-lookup"><span data-stu-id="1a161-114">One or more MIDL statement which define the interface of the [**library**](library.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a161-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a161-115">Remarks</span></span>

<span data-ttu-id="1a161-116">Verwenden Sie das **\[ Helpstringdll \]** -Attribut einer Library-Anweisung, um als Zeichenfolge den voll qualifizierten Dateinamen einer Dynamic Link Library anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1a161-116">Use the **\[helpstringdll\]** attribute on a library statement to specify, as a character string, the fully qualified file name of a dynamic link library.</span></span> <span data-ttu-id="1a161-117">Dies ermöglicht es einem Benutzer, eine Beschreibung der DLL mit dem Objekt-Viewer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1a161-117">This allows a user to view a description of the DLL with the object viewer.</span></span>

<span data-ttu-id="1a161-118">Verwenden Sie die **GetDocumentation2** -Funktionen in den Schnittstellen **ITypeLib2** und **ITypeInfo2** , um die Hilfe Zeichenfolge abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1a161-118">Use the **GetDocumentation2** functions in the **ITypeLib2** and **ITypeInfo2** interfaces to retrieve the help string.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a161-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a161-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a161-120">**Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="1a161-120">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="1a161-121">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="1a161-121">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="1a161-122">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="1a161-122">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="1a161-123">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="1a161-123">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 