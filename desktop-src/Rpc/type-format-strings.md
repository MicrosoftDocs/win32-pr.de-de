---
title: Typformatzeichenfolgen
description: Formatierungszeichen bezeichnen Objekte, die für die NDR-Engine von Interesse sind.
ms.assetid: 71117082-07b0-4ba4-a920-09be8d8427ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f618d857e487f86e2d28ed18300d82e94b76e3a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037326"
---
# <a name="type-format-strings"></a><span data-ttu-id="f7722-103">Typformatzeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="f7722-103">Type Format Strings</span></span>

<span data-ttu-id="f7722-104">Formatierungszeichen bezeichnen Objekte, die für die NDR-Engine von Interesse sind.</span><span class="sxs-lookup"><span data-stu-id="f7722-104">Format characters denote objects of interest to the NDR engine.</span></span> <span data-ttu-id="f7722-105">Es gibt ein Formatzeichen für jeden Basistyp, für verschiedene komplexe Typen und für Beschreibungen von Zeigern, packen, Ausrichtungen und anderen verschiedenen Objekten.</span><span class="sxs-lookup"><span data-stu-id="f7722-105">There is a format character for each basic type, for various complex types, and for descriptions of pointers, packing, alignment, and other miscellaneous objects.</span></span> <span data-ttu-id="f7722-106">Für Verbund Typen werden verschiedene Kategorien von Strukturen und Arrays basierend auf Ihren Leistungseigenschaften erkannt.</span><span class="sxs-lookup"><span data-stu-id="f7722-106">For compound types, several categories of structures and arrays are recognized based on their performance properties.</span></span> <span data-ttu-id="f7722-107">Eine Format Zeichenfolge für jede Kategorie beginnt mit einem FC-Token, das die jeweilige Format Zeichenfolge identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f7722-107">A format string for each category starts with an FC token identifying the particular format string.</span></span> <span data-ttu-id="f7722-108">Format Zeichen für Strukturen und Array Kategorien können die in-Fixes in den Namen des führenden FC-Tokens freigeben, das in der folgenden Tabelle gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f7722-108">Format characters for structures and arrays categories may share the in-fixes in the name of the leading FC token shown in the following table.</span></span>



| <span data-ttu-id="f7722-109">Zeichen formatieren</span><span class="sxs-lookup"><span data-stu-id="f7722-109">Format character</span></span> | <span data-ttu-id="f7722-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f7722-110">Description</span></span>                                    |
|------------------|------------------------------------------------|
| <span data-ttu-id="f7722-111">C</span><span class="sxs-lookup"><span data-stu-id="f7722-111">C</span></span>                | <span data-ttu-id="f7722-112">Gibt Konformitäts Informationen im Typ an.</span><span class="sxs-lookup"><span data-stu-id="f7722-112">Indicates conformance information in the type.</span></span> |
| <span data-ttu-id="f7722-113">V</span><span class="sxs-lookup"><span data-stu-id="f7722-113">V</span></span>                | <span data-ttu-id="f7722-114">Gibt Varianz Informationen im Typ an.</span><span class="sxs-lookup"><span data-stu-id="f7722-114">Indicates variance information in the type.</span></span>    |
| <span data-ttu-id="f7722-115">P</span><span class="sxs-lookup"><span data-stu-id="f7722-115">P</span></span>                | <span data-ttu-id="f7722-116">Gibt an, dass Zeiger ein Teil des Typs sind.</span><span class="sxs-lookup"><span data-stu-id="f7722-116">Indicates pointers are a part of the type.</span></span>     |



 

<span data-ttu-id="f7722-117">Beispielsweise identifizieren FC \_ cstruct und FC \_ CArray die konforme Struktur bzw. die konformen Array Deskriptoren.</span><span class="sxs-lookup"><span data-stu-id="f7722-117">For example, FC\_CSTRUCT and FC\_CARRAY identify the conformant structure and conformant array descriptors, respectively.</span></span>

<span data-ttu-id="f7722-118">Im folgenden sind Formatzeichen mit besonderer Bedeutung aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f7722-118">The following are format characters with special meanings.</span></span>



| <span data-ttu-id="f7722-119">Zeichen formatieren</span><span class="sxs-lookup"><span data-stu-id="f7722-119">Format character</span></span> | <span data-ttu-id="f7722-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f7722-120">Description</span></span>                                                                         |
|------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f7722-121">FC- \_ PP</span><span class="sxs-lookup"><span data-stu-id="f7722-121">FC\_PP</span></span>           | <span data-ttu-id="f7722-122">Gibt den Anfang des Zeiger Beschreibungs Abschnitts einer Struktur oder eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="f7722-122">Indicates the beginning of the pointer description section of a structure or array.</span></span> |



 

<span data-ttu-id="f7722-123">Die Format Zeichenfolgen für den RPC-NDR-Typ werden in den folgenden Themen ausführlicher beschrieben:</span><span class="sxs-lookup"><span data-stu-id="f7722-123">RPC NDR type format strings are described in more detail in the following topics:</span></span>

-   [<span data-ttu-id="f7722-124">Einfache Typen</span><span class="sxs-lookup"><span data-stu-id="f7722-124">Simple Types</span></span>](simple-types-tfs.md)
-   [<span data-ttu-id="f7722-125">Zeiger</span><span class="sxs-lookup"><span data-stu-id="f7722-125">Pointers</span></span>](pointers-tfs.md)
-   [<span data-ttu-id="f7722-126">Arrays</span><span class="sxs-lookup"><span data-stu-id="f7722-126">Arrays</span></span>](arrays-tfs.md)
-   [<span data-ttu-id="f7722-127">Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="f7722-127">Strings</span></span>](strings-tfs.md)
-   [<span data-ttu-id="f7722-128">Korrelations Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="f7722-128">Correlation Descriptors</span></span>](correlation-descriptors-tfs.md)
-   [<span data-ttu-id="f7722-129">Strukturen</span><span class="sxs-lookup"><span data-stu-id="f7722-129">Structures</span></span>](structures-tfs.md)
-   [<span data-ttu-id="f7722-130">Zeiger Layout</span><span class="sxs-lookup"><span data-stu-id="f7722-130">Pointer Layout</span></span>](pointer-layout-tfs.md)
-   [<span data-ttu-id="f7722-131">Unions</span><span class="sxs-lookup"><span data-stu-id="f7722-131">Unions</span></span>](unions-tfs.md)
-   [<span data-ttu-id="f7722-132">Übertragen \_ als und Darstellung \_ als</span><span class="sxs-lookup"><span data-stu-id="f7722-132">Transmit\_as and Represent\_as</span></span>](transmit-as-and-represent-as-tfs.md)
-   [<span data-ttu-id="f7722-133">Benutzer Mars Hallen</span><span class="sxs-lookup"><span data-stu-id="f7722-133">User-marshal</span></span>](user-marshal-tfs.md)

 

 




