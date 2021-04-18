---
title: Bibliotheks Attribut
description: Die Library-Anweisung enthält alle Informationen, die vom-Mittelwert Compiler zum Generieren einer Typbibliothek verwendet werden.
ms.assetid: d73acb17-abe4-4c31-a264-a131d1f9fa51
keywords:
- Bibliotheks Attribut-Mittel l
topic_type:
- apiref
api_name:
- library
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 100c901c6b5d86ed3420d51e459627bdb5b461b8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106338659"
---
# <a name="library-attribute"></a><span data-ttu-id="7cdbe-104">Bibliotheks Attribut</span><span class="sxs-lookup"><span data-stu-id="7cdbe-104">library attribute</span></span>

<span data-ttu-id="7cdbe-105">Die **Library** -Anweisung enthält alle Informationen, die vom-Mittelwert Compiler zum Generieren einer Typbibliothek verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7cdbe-105">The **library** statement contains all the information that the MIDL compiler uses to generate a type library.</span></span>

``` syntax
[
    uuid(uuid-number), 
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
}
```

## <a name="parameters"></a><span data-ttu-id="7cdbe-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7cdbe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cdbe-107">*UUID-Nummer*</span><span class="sxs-lookup"><span data-stu-id="7cdbe-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="7cdbe-108">Gibt eine universell eindeutige Identifikationsnummer für die Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="7cdbe-108">Specifies a universally unique identification number for the library.</span></span>

</dd> <dt>

<span data-ttu-id="7cdbe-109">*optional-Attribut-List*</span><span class="sxs-lookup"><span data-stu-id="7cdbe-109">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7cdbe-110">Gibt zusätzliche Attribute an, die auf die gesamte **Bibliotheks** Anweisung angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="7cdbe-110">Specifies additional attributes that apply to the entire **library** statement.</span></span> <span data-ttu-id="7cdbe-111">Zulässige Attribute sind **\[** [**Control**](control.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**HelpFile**](helpfile.md) **\]** , **\[** [**HelpString**](helpstring.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** , **\[** [**LCID**](lcid.md) **\]** , **\[** [**restricted**](restricted.md) **\]** und **\[** [**Version**](version.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="7cdbe-111">Allowable attributes include **\[**[**control**](control.md)**\]**, **\[**[**helpcontext**](helpcontext.md)**\]**, **\[**[**helpfile**](helpfile.md)**\]**, **\[**[**helpstring**](helpstring.md)**\]**, **\[**[**hidden**](hidden.md)**\]**, **\[**[**lcid**](lcid.md)**\]**, **\[**[**restricted**](restricted.md)**\]**, and **\[**[**version**](version.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="7cdbe-112">*Bibliotheksname*</span><span class="sxs-lookup"><span data-stu-id="7cdbe-112">*library-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7cdbe-113">Der Name, mit dem Softwarekomponenten auf die **Bibliothek** verweisen.</span><span class="sxs-lookup"><span data-stu-id="7cdbe-113">The name by which software components refer to the **library**.</span></span>

</dd> <dt>

<span data-ttu-id="7cdbe-114">*Library-Definition-Anweisungen*</span><span class="sxs-lookup"><span data-stu-id="7cdbe-114">*library-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="7cdbe-115">Eine oder mehrere-Mittell-Anweisungen, die den Inhalt der **Bibliothek** definieren.</span><span class="sxs-lookup"><span data-stu-id="7cdbe-115">One or more MIDL statements which define the contents of the **library**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7cdbe-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7cdbe-116">Remarks</span></span>

<span data-ttu-id="7cdbe-117">-Anweisungen innerhalb des Bibliotheks Blocks können Elemente verwenden, die innerhalb oder außerhalb des Bibliotheks Blocks deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="7cdbe-117">Statements inside the library block can use elements that are declared inside or outside of the library block.</span></span> <span data-ttu-id="7cdbe-118">Bibliotheks Anweisungen können diese Elemente als Basis Typen verwenden, von diesen Elementen erben oder einfach in einer Zeile auf Sie verweisen, wie im folgenden dargestellt:</span><span class="sxs-lookup"><span data-stu-id="7cdbe-118">Library statements can use those elements as base types, inheriting from those elements, or by simply referencing them on a line, as follows:</span></span>

``` syntax
interface MyFace 
{
    // Interface definition statements
};

[
    // library attributes
] 
library
{
    interface MyFace;

    // Other library definition statements.
};
```

<span data-ttu-id="7cdbe-119">Der mittlerer l-Compiler erstellt eine Typbibliothek, die Definitionen für jedes Element innerhalb des Bibliotheks Blocks sowie Definitionen für alle Elemente enthält, die außerhalb des Bibliotheks Blocks definiert sind und auf die verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7cdbe-119">The MIDL compiler will create a type library that includes definitions for every element inside the library block, plus definitions for any elements defined outside and referenced from within the library block.</span></span>

<span data-ttu-id="7cdbe-120">Informationen zum Erstellen eines Typbibliothek-und proxystubys und von Headern aus einer einzelnen IDL-Datei finden Sie unter [Erstellen einer Proxy-dll und einer Typbibliothek aus einer einzelnen IDL-Datei](generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file-2.md).</span><span class="sxs-lookup"><span data-stu-id="7cdbe-120">For information on generating both a type library and proxy stubs and headers from a single IDL file see [Generating a Proxy DLL and a Type Library From a Single IDL File](generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file-2.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7cdbe-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7cdbe-121">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("Hello 2.0 Type Library"), 
    lcid(0x0409), 
    version(2.0)
] 
library Hello 
{
    /* Library definition statements */
};
```

## <a name="see-also"></a><span data-ttu-id="7cdbe-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7cdbe-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cdbe-123">Inhalt einer Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="7cdbe-123">Contents of a Type Library</span></span>](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[<span data-ttu-id="7cdbe-124">**Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="7cdbe-124">**control**</span></span>](control.md)
</dt> <dt>

[<span data-ttu-id="7cdbe-125">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="7cdbe-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="7cdbe-126">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="7cdbe-126">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="7cdbe-127">**helpfile**</span><span class="sxs-lookup"><span data-stu-id="7cdbe-127">**helpfile**</span></span>](helpfile.md)
</dt> <dt>

[<span data-ttu-id="7cdbe-128">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="7cdbe-128">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="7cdbe-129">**verbirgt**</span><span class="sxs-lookup"><span data-stu-id="7cdbe-129">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="7cdbe-130">**LCID**</span><span class="sxs-lookup"><span data-stu-id="7cdbe-130">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="7cdbe-131">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="7cdbe-131">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="7cdbe-132">**begrenz**</span><span class="sxs-lookup"><span data-stu-id="7cdbe-132">**restricted**</span></span>](restricted.md)
</dt> <dt>

[<span data-ttu-id="7cdbe-133">**version**</span><span class="sxs-lookup"><span data-stu-id="7cdbe-133">**version**</span></span>](version.md)
</dt> </dl>

 

 