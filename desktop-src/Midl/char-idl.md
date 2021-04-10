---
title: char-Attribut
description: Das Char-Schlüsselwort gibt ein 8-Bit-Datenelement an.
ms.assetid: 3c9ba8bb-5aea-4166-acf6-b251377e5384
keywords:
- char-Attribut-Mittel l
topic_type:
- apiref
api_name:
- char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eab719f6f8ea6e21ccc5b389b12a66b617d5773
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857592"
---
# <a name="char-attribute"></a><span data-ttu-id="4e1e7-104">char-Attribut</span><span class="sxs-lookup"><span data-stu-id="4e1e7-104">char attribute</span></span>

<span data-ttu-id="4e1e7-105">Das **char** -Schlüsselwort gibt ein 8-Bit-Datenelement an.</span><span class="sxs-lookup"><span data-stu-id="4e1e7-105">The **char** keyword specifies an 8-bit data item.</span></span>

``` syntax
char identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="4e1e7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e1e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e1e7-107">*Bezeichnername*</span><span class="sxs-lookup"><span data-stu-id="4e1e7-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4e1e7-108">Gibt einen gültigen Mittell-Bezeichner an.</span><span class="sxs-lookup"><span data-stu-id="4e1e7-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="4e1e7-109">Gültige Mittell-Bezeichner bestehen aus bis zu 31 alphanumerischen Zeichen und/oder unterstrichen und müssen mit einem Buchstaben oder einem Unterstrich beginnen.</span><span class="sxs-lookup"><span data-stu-id="4e1e7-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e1e7-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e1e7-110">Remarks</span></span>

<span data-ttu-id="4e1e7-111">Das Schlüsselwort **char** identifiziert ein Datenelement, das über 8 Bits verfügt.</span><span class="sxs-lookup"><span data-stu-id="4e1e7-111">The keyword **char** identifies a data item that has 8 bits.</span></span> <span data-ttu-id="4e1e7-112">Für den mittlerer l-Compiler ist ein **char** standardmäßig **unsigniert und** mit Vorzeichen [**ohne**](unsigned.md) Vorzeichen Synonym.</span><span class="sxs-lookup"><span data-stu-id="4e1e7-112">To the MIDL compiler, a **char** is unsigned by default and is synonymous with [**unsigned**](unsigned.md) **char**.</span></span>

<span data-ttu-id="4e1e7-113">In dieser Version von Microsoft RPC werden die Zeichen Übersetzungstabellen, die zwischen ASCII und EBCDIC konvertiert werden, in die Laufzeitbibliotheken integriert und können vom Benutzer nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="4e1e7-113">In this version of Microsoft RPC, the character translation tables that convert between ASCII and EBCDIC are built into the run-time libraries and cannot be changed by the user.</span></span>

<span data-ttu-id="4e1e7-114">Der **char** -Typ ist einer der Basis Typen der IDL (Interface Definition Language).</span><span class="sxs-lookup"><span data-stu-id="4e1e7-114">The **char** type is one of the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="4e1e7-115">Der **char** -Typ kann als Typspezifizierer in [**Konstanten**](const.md) Deklarationen, [**typedef**](typedef.md) -Deklarationen, allgemeinen Deklarationen und Funktions Deklaratoren (als Funktions Rückgabetyp-Spezifizierer und Parameter-Typspezifizierer) vorkommen.</span><span class="sxs-lookup"><span data-stu-id="4e1e7-115">The **char** type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and a parameter-type specifier).</span></span> <span data-ttu-id="4e1e7-116">Informationen zu dem Kontext, in dem typspezifier angezeigt wird, finden Sie unter [Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="4e1e7-116">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="4e1e7-117">DCE-IDL-Compiler akzeptieren das auf **char** - [**Typen angewendete**](signed.md) Schlüsselwort nicht.</span><span class="sxs-lookup"><span data-stu-id="4e1e7-117">DCE IDL compilers do not accept the keyword [**signed**](signed.md) applied to **char** types.</span></span> <span data-ttu-id="4e1e7-118">Diese Funktion ist daher nicht verfügbar, wenn Sie den [**/OSF**](-osf.md) -Schalter für den Mittelwert Compiler verwenden.</span><span class="sxs-lookup"><span data-stu-id="4e1e7-118">Therefore, this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

## <a name="see-also"></a><span data-ttu-id="4e1e7-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e1e7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e1e7-120">Mittel l-Basis Typen</span><span class="sxs-lookup"><span data-stu-id="4e1e7-120">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="4e1e7-121">**Hobby**</span><span class="sxs-lookup"><span data-stu-id="4e1e7-121">**byte**</span></span>](byte.md)
</dt> <dt>

[<span data-ttu-id="4e1e7-122">**/Char**</span><span class="sxs-lookup"><span data-stu-id="4e1e7-122">**/char**</span></span>](-char.md)
</dt> <dt>

[<span data-ttu-id="4e1e7-123">**const**</span><span class="sxs-lookup"><span data-stu-id="4e1e7-123">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="4e1e7-124">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="4e1e7-124">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="4e1e7-125">**/osf**</span><span class="sxs-lookup"><span data-stu-id="4e1e7-125">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="4e1e7-126">**ebenes**</span><span class="sxs-lookup"><span data-stu-id="4e1e7-126">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="4e1e7-127">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4e1e7-127">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="4e1e7-128">**typedef**</span><span class="sxs-lookup"><span data-stu-id="4e1e7-128">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="4e1e7-129">**Ganzzahl ohne Vorzeichen**</span><span class="sxs-lookup"><span data-stu-id="4e1e7-129">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="4e1e7-130">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="4e1e7-130">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 




