---
title: LCID-Attribut
description: Das Attribut \ LCID \ gibt einen Gebiets Schema Bezeichner an und ermöglicht Gebiets Schema spezifische Unterstützung für den-Compiler.
ms.assetid: 40457a1a-251c-41cd-bfa6-9d506601ff5e
keywords:
- LCID-Attribut-Mittel l
topic_type:
- apiref
api_name:
- lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa22b231c63583c6d16e6a50f3e9987c5b61128
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725096"
---
# <a name="lcid-attribute"></a><span data-ttu-id="dd062-104">LCID-Attribut</span><span class="sxs-lookup"><span data-stu-id="dd062-104">lcid attribute</span></span>

<span data-ttu-id="dd062-105">Das **\[ LCID \]** -Attribut gibt einen Gebiets Schema Bezeichner an und ermöglicht Gebiets Schema spezifische Unterstützung für den Mittelwert Compiler.</span><span class="sxs-lookup"><span data-stu-id="dd062-105">The **\[lcid\]** attribute specifies a locale identifier and enables locale-specific MIDL compiler support.</span></span>

``` syntax
[
    uuid(uuid-number), 
    lcid(localeID)
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
}

function-name([parameter-attribute-list, lcid] long  parameter-name,. . .);
```

## <a name="parameters"></a><span data-ttu-id="dd062-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd062-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd062-107">*UUID-Nummer*</span><span class="sxs-lookup"><span data-stu-id="dd062-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="dd062-108">Gibt eine universell eindeutige Identifikationsnummer für die [**Bibliothek**](library.md)an.</span><span class="sxs-lookup"><span data-stu-id="dd062-108">Specifies a universally unique identification number for the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd062-109">*LocaleID*</span><span class="sxs-lookup"><span data-stu-id="dd062-109">*localeID*</span></span> 
</dt> <dd>

<span data-ttu-id="dd062-110">Gibt den 32-Bit-Gebiets Schema Bezeichner an, der in der Unterstützung von Windows-</span><span class="sxs-lookup"><span data-stu-id="dd062-110">Specifies the 32-bit locale identifier used in Windows National Language Support.</span></span> <span data-ttu-id="dd062-111">In der Regel wird der Gebiets Schema Bezeichner in hexadezimal angegeben.</span><span class="sxs-lookup"><span data-stu-id="dd062-111">Typically the locale identifier is given in hexadecimal.</span></span>

</dd> <dt>

<span data-ttu-id="dd062-112">*optional-Attribut-List*</span><span class="sxs-lookup"><span data-stu-id="dd062-112">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="dd062-113">NULL oder mehr Attribute, die auf die [**Bibliothek**](library.md)angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dd062-113">Zero or more attributes to apply to the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd062-114">*Bibliotheksname*</span><span class="sxs-lookup"><span data-stu-id="dd062-114">*library-name*</span></span> 
</dt> <dd>

<span data-ttu-id="dd062-115">Der Name, mit dem Softwarekomponenten auf die [**Bibliothek**](library.md)verweisen.</span><span class="sxs-lookup"><span data-stu-id="dd062-115">The name by which software components refer to the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd062-116">*Library-Definition-Anweisungen*</span><span class="sxs-lookup"><span data-stu-id="dd062-116">*library-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="dd062-117">Eine oder mehrere-Mittell-Anweisungen, die den Inhalt der [**Bibliothek**](library.md)definieren.</span><span class="sxs-lookup"><span data-stu-id="dd062-117">One or more MIDL statements which define the contents of the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd062-118">*function-name*</span><span class="sxs-lookup"><span data-stu-id="dd062-118">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="dd062-119">Gibt den Namen der Funktion in der IDL-Datei an.</span><span class="sxs-lookup"><span data-stu-id="dd062-119">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="dd062-120">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="dd062-120">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="dd062-121">NULL oder mehr mittlere Attribute, die auf den Funktionsparameter angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd062-121">Zero or more MIDL attributes that will be applied to the function parameter.</span></span>

</dd> <dt>

<span data-ttu-id="dd062-122">*Parameter Name*</span><span class="sxs-lookup"><span data-stu-id="dd062-122">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="dd062-123">Gibt den Namen des Parameters in der IDL-Datei an.</span><span class="sxs-lookup"><span data-stu-id="dd062-123">Specifies the name of the parameter in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd062-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd062-124">Remarks</span></span>

<span data-ttu-id="dd062-125">Die **\[ LCID \]** -Syntax verfügt über zwei verschiedene Formen: die Auswirkung des Attributs hängt davon ab, welche Syntax Sie verwenden – entweder der Syntax der [**Bibliotheks**](library.md) Anweisung oder der Parameter Syntax.</span><span class="sxs-lookup"><span data-stu-id="dd062-125">The **\[lcid\]** syntax has two different forms; the effect of the attribute depends on which syntax you use — either the [**library**](library.md) statement syntax or the parameter syntax.</span></span>

<span data-ttu-id="dd062-126">Wenn das LCID-Attribut, wie im ersten Beispiel gezeigt, zusammen mit einem LocaleID-Argument auf die [**Library**](library.md) -Anweisung angewendet wird, identifiziert das **\[ LCID \]** -Attribut das Gebiets Schema für eine Typbibliothek oder für ein Funktions Argument und ermöglicht die Verwendung internationaler Zeichen innerhalb des Bibliotheks Blocks.</span><span class="sxs-lookup"><span data-stu-id="dd062-126">When applied to the [**library**](library.md) statement, along with a localeID argument, as shown in the first example, the **\[lcid\]** attribute identifies the locale for a type library or for a function argument and lets you use international characters inside the library block.</span></span>

<span data-ttu-id="dd062-127">Mit der Version 3.01.75 des mittlerer l-Compilers wird der von diesem Attribut bereitgestellte Gebiets Schema Bezeichner nicht nur die resultierende Typbibliothek, sondern das Verhalten des Compilers geändert.</span><span class="sxs-lookup"><span data-stu-id="dd062-127">Effective with version 3.01.75 of the MIDL compiler, the locale identifier supplied by this attribute not only decorates the resulting type library, but actually changes the behavior of the compiler.</span></span> <span data-ttu-id="dd062-128">Innerhalb einer [**Library**](library.md) -Anweisung akzeptiert die Mittel Stelle ab dem Zeitpunkt, an dem das **\[ LCID \]** -Attribut verwendet wird, die nach dem angegebenen Gebiets Schema lokalisierte Eingabe.</span><span class="sxs-lookup"><span data-stu-id="dd062-128">Within a [**library**](library.md) statement, from the point where the **\[lcid\]** attribute is used, MIDL will accept input localized according to the specified locale.</span></span> <span data-ttu-id="dd062-129">Insbesondere ist eine vollständige Unterstützung für asiatische Sprachen wie Japanisch, Chinesisch und Koreanisch (vollständige DBCS-Unterstützung) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dd062-129">In particular, full support for Asian languages such as Japanese, Chinese and Korean (full DBCS support) is available.</span></span> <span data-ttu-id="dd062-130">Die von der Lokalisierung unterstützten Funktionen sind: Kommentare, Zeichen folgen, helpstrings und Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="dd062-130">Features supported by the localization are: comments, strings, helpstrings and identifiers.</span></span>

<span data-ttu-id="dd062-131">Verwenden Sie den [**/LCID**](-lcid.md) -Compilerschalter, um diese Lokalisierungsunterstützung für die gesamte Eingabedatei, einschließlich Dateiname und Verzeichnispfad, anstelle des Bibliotheks Blocks verfügbar zu lassen.</span><span class="sxs-lookup"><span data-stu-id="dd062-131">Use the [**/lcid**](-lcid.md) compiler switch to have this localization support available to the entire input file, including file name and directory path, rather than just inside the library block.</span></span>

<span data-ttu-id="dd062-132">Wenn das **\[ LCID \]** -Attribut auf einen Parameter angewendet wird, können Sie einen Gebiets Schema Bezeichner an eine Funktion übergeben, wie im zweiten Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="dd062-132">When applied to a parameter, the **\[lcid\]** attribute lets you pass a locale identifier to a function, as shown in the second example.</span></span> <span data-ttu-id="dd062-133">Für **\[ LCID \]** -Parameter gelten die folgenden Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="dd062-133">The following restrictions apply to **\[lcid\]** parameters:</span></span>

-   <span data-ttu-id="dd062-134">Eine Funktion kann höchstens einen **\[ LCID \]** -Parameter aufweisen.</span><span class="sxs-lookup"><span data-stu-id="dd062-134">A function can have at most one **\[lcid\]** parameter.</span></span>
-   <span data-ttu-id="dd062-135">Der Datentyp des-Parameters muss [**lang**](long.md)sein.</span><span class="sxs-lookup"><span data-stu-id="dd062-135">The data type of the parameter must be [**long**](long.md).</span></span>
-   <span data-ttu-id="dd062-136">Die Richtung des-Parameters darf **\[** nur [**in**](in.md) sein **\]** .</span><span class="sxs-lookup"><span data-stu-id="dd062-136">The direction of the parameter must be **\[**[**in**](in.md)**\]** only.</span></span>
-   <span data-ttu-id="dd062-137">Der **\[ LCID \]** -Parameter muss mit Ausnahme eines **\[** [**retval**](retval.md) -Parameters allen anderen Parametern folgen **\]** .</span><span class="sxs-lookup"><span data-stu-id="dd062-137">The **\[lcid\]** parameter must follow any other parameters, except a **\[**[**retval**](retval.md)**\]** parameter.</span></span>
-   <span data-ttu-id="dd062-138">Sie können das **\[ LCID \]** -Attribut nicht auf einen [**dispinterface**](dispinterface.md) -oder einen [**Co-Klasse**](coclass.md) -Parameter anwenden.</span><span class="sxs-lookup"><span data-stu-id="dd062-138">You cannot apply the **\[lcid\]** attribute to a [**dispinterface**](dispinterface.md) or [**coclass**](coclass.md) parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="dd062-139">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd062-139">Examples</span></span>

``` syntax
[  
    uuid(12345678-1234-1234-1234-123456789ABC),
    lcid(0x09),
    version(1.0)
] 
library MyLibrary
{
    /* Library definition statements */
};

interface IMyFace : IDispatch
{
    [propget] HRESULT MyFunc([in, lcid] long LocaleID,
                          [out, retval] BSTR * ReturnVal);
    // Other interface definition statements
}
```

## <a name="see-also"></a><span data-ttu-id="dd062-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="dd062-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd062-141">**coclass**</span><span class="sxs-lookup"><span data-stu-id="dd062-141">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="dd062-142">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="dd062-142">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="dd062-143">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="dd062-143">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="dd062-144">**/LCID**</span><span class="sxs-lookup"><span data-stu-id="dd062-144">**/lcid**</span></span>](-lcid.md)
</dt> <dt>

[<span data-ttu-id="dd062-145">**Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="dd062-145">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="dd062-146">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="dd062-146">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="dd062-147">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="dd062-147">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="dd062-148">**retval**</span><span class="sxs-lookup"><span data-stu-id="dd062-148">**retval**</span></span>](retval.md)
</dt> </dl>

 

 