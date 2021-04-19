---
description: ICE65 prüft, ob die Umgebungs Tabelle Ungültige Präfix-oder anfügewerte enthält.
ms.assetid: 95d4e618-9a19-40db-910a-daab105559ae
title: ICE65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3d2b7bcd844c970ccc7fddf376b27c2ec54f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373275"
---
# <a name="ice65"></a><span data-ttu-id="85a91-103">ICE65</span><span class="sxs-lookup"><span data-stu-id="85a91-103">ICE65</span></span>

<span data-ttu-id="85a91-104">ICE65 prüft, ob die [Umgebungs Tabelle](environment-table.md) Ungültige Präfix-oder anfügewerte enthält.</span><span class="sxs-lookup"><span data-stu-id="85a91-104">ICE65 checks that the [Environment table](environment-table.md) does not have invalid prefix or append values.</span></span>

<span data-ttu-id="85a91-105">Wenn eine Warnung oder ein Fehler, der von ICE65 gemeldet wird, nicht behoben wird, führt dies im Allgemeinen zu Problemen beim Installieren, deinstallieren oder Reparieren der Umgebungsvariablen.</span><span class="sxs-lookup"><span data-stu-id="85a91-105">Failure to fix a warning or error reported by ICE65 generally leads to problems in install, uninstall, or repair of the environment variable.</span></span> <span data-ttu-id="85a91-106">Beispielsweise können nur einige Werte einer bestimmten Variablen entfernt werden, wenn mindestens einer der Werte für diese Variable ein nachfolgendes Trennzeichen hat.</span><span class="sxs-lookup"><span data-stu-id="85a91-106">For example, only some values of a particular variable may be removed if one or more of the values for that variable have a trailing separator.</span></span>

## <a name="result"></a><span data-ttu-id="85a91-107">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="85a91-107">Result</span></span>

<span data-ttu-id="85a91-108">ICE65 gibt eine Warnung oder einen Fehler aus, wenn die Umgebungs Tabelle Ungültige Präfix-oder anfügewerte aufweist.</span><span class="sxs-lookup"><span data-stu-id="85a91-108">ICE65 posts a warning or an error if the environment table has invalid prefix or append values.</span></span>

## <a name="example"></a><span data-ttu-id="85a91-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="85a91-109">Example</span></span>

<span data-ttu-id="85a91-110">ICE65 meldet den folgenden Fehler und die Warnung für das gezeigte Beispiel.</span><span class="sxs-lookup"><span data-stu-id="85a91-110">ICE65 reports the following error and warning for the example shown.</span></span>

``` syntax
The environment variable 'Var3' has a separator beginning or ending its value.
```

<span data-ttu-id="85a91-111">Der nachfolgende NULL am Ende des Werts ( \[ ~ \] ) markiert diesen Wert, der einem vorhandenen Wert vorangestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="85a91-111">The trailing null at the end of the value (\[~\]) marks this value to be prepended to any existing value.</span></span> <span data-ttu-id="85a91-112">Das Zeichen unmittelbar vor dem NULL-Zeichen (ein Semikolon) wird das Trennzeichen für diesen Wert.</span><span class="sxs-lookup"><span data-stu-id="85a91-112">The character immediately before the null (a semicolon) becomes the separator for this value.</span></span> <span data-ttu-id="85a91-113">Dieser Wert enthält auch ein Semikolon am Anfang der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="85a91-113">This value has a semicolon at the beginning of the string as well.</span></span>

<span data-ttu-id="85a91-114">Um diesen Fehler zu beheben, löschen Sie einfach das vorangehende Semikolon.</span><span class="sxs-lookup"><span data-stu-id="85a91-114">To fix this error, simply delete the leading semicolon.</span></span>

``` syntax
WARNING: The environment variable 'Var2' has an alphanumeric separator
```

<span data-ttu-id="85a91-115">Der führende Null-Wert im-Wert ( \[ ~ \] ) markiert diesen Wert, der an einen beliebigen vorhandenen Wert angehängt werden soll.</span><span class="sxs-lookup"><span data-stu-id="85a91-115">The leading null in the value (\[~\]) marks this value to be appended to any existing value.</span></span> <span data-ttu-id="85a91-116">Das Zeichen direkt nach dem NULL-Wert wird das Trennzeichen für diesen Wert.</span><span class="sxs-lookup"><span data-stu-id="85a91-116">The character immediately after the null becomes the separator for this value.</span></span> <span data-ttu-id="85a91-117">In diesem Fall handelt es sich bei diesem Zeichen um den Buchstaben "e", der auch in der Mitte der anzufügenden Zeichenfolge vorkommt.</span><span class="sxs-lookup"><span data-stu-id="85a91-117">In this case, that character is the letter "e", which also occurs in the middle of the string to be appended.</span></span> <span data-ttu-id="85a91-118">Diese Bedingung (mit einem Trennzeichen, das mit einem Zeichen innerhalb der anzufügenden Zeichenfolge identisch ist) kann zu unvorhersehbaren Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="85a91-118">This condition (having a separator that is the same as a character within the string to be appended) can cause unpredictable results.</span></span>

<span data-ttu-id="85a91-119">Der Buchstabe "e", bei dem es sich um einen gemeinsamen Buchstaben handelt, wird wahrscheinlich im Wert gefunden.</span><span class="sxs-lookup"><span data-stu-id="85a91-119">The letter "e", being a common letter, is likely to be found in the value.</span></span> <span data-ttu-id="85a91-120">Eine bessere Wahl wäre ";" oder ein anderes nicht alphanumerisches Zeichen.</span><span class="sxs-lookup"><span data-stu-id="85a91-120">A better choice would be ";" or some other non-alphanumeric character.</span></span> <span data-ttu-id="85a91-121">(Wenn der Wert jedoch ein Pfad ist, sind ":" und " \\ " und "." riskante Entscheidungen.)</span><span class="sxs-lookup"><span data-stu-id="85a91-121">(However, if the value is a path, then ":" and "\\" and "." are risky choices.)</span></span>

<span data-ttu-id="85a91-122">Um diese Warnung zu beheben, verwenden Sie ein anderes Trennzeichen.</span><span class="sxs-lookup"><span data-stu-id="85a91-122">To fix this warning, use a different separator character.</span></span>

[<span data-ttu-id="85a91-123">Umgebungs Tabelle</span><span class="sxs-lookup"><span data-stu-id="85a91-123">Environment Table</span></span>](environment-table.md)



| <span data-ttu-id="85a91-124">Komponente</span><span class="sxs-lookup"><span data-stu-id="85a91-124">Component</span></span> | <span data-ttu-id="85a91-125">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="85a91-125">Directory</span></span> | <span data-ttu-id="85a91-126">Attribute</span><span class="sxs-lookup"><span data-stu-id="85a91-126">Attributes</span></span>         | <span data-ttu-id="85a91-127">KEYPATH</span><span class="sxs-lookup"><span data-stu-id="85a91-127">KeyPath</span></span>       |
|-----------|-----------|--------------------|---------------|
| <span data-ttu-id="85a91-128">Var1</span><span class="sxs-lookup"><span data-stu-id="85a91-128">Var1</span></span>      | <span data-ttu-id="85a91-129">TestVar</span><span class="sxs-lookup"><span data-stu-id="85a91-129">TestVar</span></span>   | <span data-ttu-id="85a91-130">\[~\]; Appendthis</span><span class="sxs-lookup"><span data-stu-id="85a91-130">\[~\];AppendThis</span></span>   | <span data-ttu-id="85a91-131">Testcomponent</span><span class="sxs-lookup"><span data-stu-id="85a91-131">TestComponent</span></span> |
| <span data-ttu-id="85a91-132">Var2</span><span class="sxs-lookup"><span data-stu-id="85a91-132">Var2</span></span>      | <span data-ttu-id="85a91-133">TestVar</span><span class="sxs-lookup"><span data-stu-id="85a91-133">TestVar</span></span>   | <span data-ttu-id="85a91-134">\[~\]eappendthis</span><span class="sxs-lookup"><span data-stu-id="85a91-134">\[~\]eAppendThis</span></span>   | <span data-ttu-id="85a91-135">Testcomponent</span><span class="sxs-lookup"><span data-stu-id="85a91-135">TestComponent</span></span> |
| <span data-ttu-id="85a91-136">Var3</span><span class="sxs-lookup"><span data-stu-id="85a91-136">Var3</span></span>      | <span data-ttu-id="85a91-137">TestVar</span><span class="sxs-lookup"><span data-stu-id="85a91-137">TestVar</span></span>   | <span data-ttu-id="85a91-138">; Prepdthis;\[~\]</span><span class="sxs-lookup"><span data-stu-id="85a91-138">;PrependThis;\[~\]</span></span> | <span data-ttu-id="85a91-139">Testcomponent</span><span class="sxs-lookup"><span data-stu-id="85a91-139">TestComponent</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="85a91-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="85a91-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85a91-141">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="85a91-141">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



