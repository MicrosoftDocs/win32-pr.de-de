---
title: Formatzeichenfolgen
description: Eine Format Zeichenfolge ist ein interpretiertes Token, das die NDR-Engine versteht. Format Zeichenfolgen werden oft als Mops bezeichnet. in dieser Dokumentation wird der Begriff "Format Zeichenfolge" verwendet.
ms.assetid: 548283bd-023a-41dd-b1d0-661305d019e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 563dd9e4145a7d83b2e49f180329c05c1d55155d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711429"
---
# <a name="format-strings"></a><span data-ttu-id="f4a6f-104">Formatzeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="f4a6f-104">Format Strings</span></span>

<span data-ttu-id="f4a6f-105">Eine Format Zeichenfolge ist ein interpretiertes Token, das die NDR-Engine versteht.</span><span class="sxs-lookup"><span data-stu-id="f4a6f-105">A format string is an interpreted token that the NDR engine understands.</span></span> <span data-ttu-id="f4a6f-106">Format Zeichenfolgen werden oft als Mops bezeichnet. in dieser Dokumentation wird der Begriff "Format Zeichenfolge" verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4a6f-106">Format strings are often referred to as MOPs; this documentation uses the term format string throughout.</span></span>

<span data-ttu-id="f4a6f-107">Genauer gesagt ist ein Formatzeichen ein einzelnes (atomarische) Interpretier bares Token.</span><span class="sxs-lookup"><span data-stu-id="f4a6f-107">To be more precise, a format character is an individual (atomic) interpretable token.</span></span> <span data-ttu-id="f4a6f-108">Jedes Formatzeichen ist ein Byte groß.</span><span class="sxs-lookup"><span data-stu-id="f4a6f-108">Each format character is one byte in size.</span></span> <span data-ttu-id="f4a6f-109">Eine Format Zeichenfolge ist eine Sequenz von Formatzeichen oder Formatierungszeichen und numerischen Daten.</span><span class="sxs-lookup"><span data-stu-id="f4a6f-109">A format string is a sequence of format characters or format characters and numerical data.</span></span> <span data-ttu-id="f4a6f-110">Der Begriff Deskriptor wird auch zum Benennen allgemeiner Sequenzen verwendet. Beispielsweise ist eine Parameter Format Zeichenfolge oder ein Parameter Deskriptor eine Format Zeichenfolge, die verwendet wird, um einen Parameter einer Routine zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="f4a6f-110">The term descriptor is also used for naming common sequences; for example, a parameter format string or a parameter descriptor is a format string used to describe a parameter of a routine.</span></span>

<span data-ttu-id="f4a6f-111">Format Zeichen haben eindrucksvolle symbolische Namen wie FC \_ Long oder FC \_ struct.</span><span class="sxs-lookup"><span data-stu-id="f4a6f-111">Format characters have suggestive symbolic names like FC\_LONG or FC\_STRUCT.</span></span> <span data-ttu-id="f4a6f-112">Alle von der Mittel l und der NDR-Engine verwendeten Zeichen folgen Zeichen werden in der Datei "ndrtypes. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="f4a6f-112">All format string characters used by MIDL and the NDR engine are defined in the Ndrtypes.h file.</span></span>

## <a name="format-string-tables"></a><span data-ttu-id="f4a6f-113">Zeichen folgen Tabellen formatieren</span><span class="sxs-lookup"><span data-stu-id="f4a6f-113">Format String Tables</span></span>

<span data-ttu-id="f4a6f-114">Zwei primäre Format Zeichenfolgen-Tabellen werden von der-Engine verwendet: die Format Zeichenfolgen-Tabelle des Prozedur Formats, die- **\_ \_ Klasse \_**, die die Prozedur Deskriptoren beibehält, und die typformatzeichenfolgen- **Tabelle, die \_ \_ \_** die Datentyp Deskriptoren beibehält.</span><span class="sxs-lookup"><span data-stu-id="f4a6f-114">Two primary format string tables are used by the engine: the procedure format string table, **\_\_MIDL\_ProcFormatString**, that keeps the procedure descriptors; and the type format string table, **\_\_MIDL\_TypeFormatString**, that keeps the data type descriptors.</span></span> <span data-ttu-id="f4a6f-115">Der Compiler generiert beide in den hauptstub-Dateien ( \* \_ c. c, \* \_ s. c, \* \_ p. c).</span><span class="sxs-lookup"><span data-stu-id="f4a6f-115">The compiler generates both into the main stub files (\*\_c.c, \*\_s.c, \*\_p.c).</span></span> <span data-ttu-id="f4a6f-116">Die Prozedur Format-Zeichen folgen Tabelle wird größtenteils von verschiedenen Interpretern verwendet, Sie wird jedoch auch für die Puffer Konvertierung verwendet, unabhängig vom Compilermodus.</span><span class="sxs-lookup"><span data-stu-id="f4a6f-116">The procedure format string table is used mostly by various interpreters but it is also used for the buffer conversion regardless of the compiler mode.</span></span> <span data-ttu-id="f4a6f-117">Die typformatzeichenfolgen-Tabelle wird beim Aufrufen der Kern-NDR-Engine verwendet, um bestimmte Datentypen anzugeben, an denen gearbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4a6f-117">The type format string table is used when calling the core NDR engine to indicate specific data types to be worked on.</span></span>

## <a name="format-string-notation"></a><span data-ttu-id="f4a6f-118">Format Zeichen folgen Notation</span><span class="sxs-lookup"><span data-stu-id="f4a6f-118">Format String Notation</span></span>

<span data-ttu-id="f4a6f-119">Die in diesem Dokument verwendete Notation befolgt allgemeine Richtlinien für die Programmier Beschreibung, wobei ein Balken ( \| ) verwendet wird, um alternative Konstrukte und eckige Klammern ( \[ \] ) anzugeben, die zum Angeben optionaler Elemente verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f4a6f-119">The notation used in this document follows common programming description guidelines, with a bar ( \| ) used to denote alternative constructs and square brackets ( \[ \] ) used to indicate optional elements.</span></span> <span data-ttu-id="f4a6f-120">Format Zeichenfolgen werden häufig zur besseren Lesbarkeit (Verantwortlichkeit) gestapelt.</span><span class="sxs-lookup"><span data-stu-id="f4a6f-120">Format strings are frequently stacked up for readability (accountability).</span></span> <span data-ttu-id="f4a6f-121">In diesem Dokument bezeichnet FC ein einzelnes Formatierungszeichen.</span><span class="sxs-lookup"><span data-stu-id="f4a6f-121">Throughout this document, FC denotes a single format character.</span></span> <span data-ttu-id="f4a6f-122">Format Zeichen werden in allen Caps mithilfe ihrer eigentlichen symbolischen Namen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f4a6f-122">Format characters are presented in all CAPS, using their actual symbolic names.</span></span> <span data-ttu-id="f4a6f-123">Andere beliebige Felder werden durch einen Namen und eine Größe dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f4a6f-123">Other arbitrary fields are represented by a name and a size.</span></span>

<span data-ttu-id="f4a6f-124">Spitzen Klammern ( <> ) werden verwendet, um die Größe der Deskriptoren anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f4a6f-124">Angle brackets ( <> ) are used to denote sizes of the descriptors.</span></span> <span data-ttu-id="f4a6f-125">Die in der folgenden Tabelle dargestellten Konventionen werden verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4a6f-125">The conventions shown in the following table are employed.</span></span>



| <span data-ttu-id="f4a6f-126">Notation</span><span class="sxs-lookup"><span data-stu-id="f4a6f-126">Notation</span></span>     | <span data-ttu-id="f4a6f-127">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f4a6f-127">Meaning</span></span>                                                   |
|--------------|-----------------------------------------------------------|
| <span data-ttu-id="f4a6f-128"><*Nr*></span><span class="sxs-lookup"><span data-stu-id="f4a6f-128"><*n*></span></span>  | <span data-ttu-id="f4a6f-129">Die Größe des Deskriptors beträgt n Bytes.</span><span class="sxs-lookup"><span data-stu-id="f4a6f-129">The size of descriptor is n bytes.</span></span>                        |
| <>     | <span data-ttu-id="f4a6f-130">Die Größe des Deskriptors variiert.</span><span class="sxs-lookup"><span data-stu-id="f4a6f-130">The size of descriptor varies.</span></span>                            |
| <span data-ttu-id="f4a6f-131">{<>}\*</span><span class="sxs-lookup"><span data-stu-id="f4a6f-131">{<>}\*</span></span> | <span data-ttu-id="f4a6f-132">Der Deskriptor wird beliebig oft wiederholt (0, 1, 2...).</span><span class="sxs-lookup"><span data-stu-id="f4a6f-132">The descriptor is repeated any number of times (0,1,2 …).</span></span> |



 

<span data-ttu-id="f4a6f-133">Die folgenden Formatzeichen haben eine besondere Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="f4a6f-133">The following format characters have a special meaning.</span></span>



| <span data-ttu-id="f4a6f-134">Zeichen</span><span class="sxs-lookup"><span data-stu-id="f4a6f-134">Character</span></span> | <span data-ttu-id="f4a6f-135">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f4a6f-135">Meaning</span></span>                                   |
|-----------|-------------------------------------------|
| <span data-ttu-id="f4a6f-136">FC- \_ Ende</span><span class="sxs-lookup"><span data-stu-id="f4a6f-136">FC\_END</span></span>   | <span data-ttu-id="f4a6f-137">Gibt das Ende einiger Format Zeichenfolgen an.</span><span class="sxs-lookup"><span data-stu-id="f4a6f-137">Indicates the end of some format strings.</span></span> |
| <span data-ttu-id="f4a6f-138">FC- \_ Pad</span><span class="sxs-lookup"><span data-stu-id="f4a6f-138">FC\_PAD</span></span>   | <span data-ttu-id="f4a6f-139">Nicht interpretiertes Auffüll Zeichen.</span><span class="sxs-lookup"><span data-stu-id="f4a6f-139">Uninterpreted pad character.</span></span>              |



 

 

 




