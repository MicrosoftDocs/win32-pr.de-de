---
description: Ein &\# 0034;-Zeichensatz&\# 0034; ist eine Zuordnung von Zeichen zu ihren identifizierenden Codewerten.
ms.assetid: 0a055c02-c5ed-4790-83e4-183bc3cc6b51
title: Zeichensätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8e62a0afbe9e5b2b3ab596a8129db833477e53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347744"
---
# <a name="character-sets"></a><span data-ttu-id="282cf-103">Zeichensätze</span><span class="sxs-lookup"><span data-stu-id="282cf-103">Character Sets</span></span>

<span data-ttu-id="282cf-104">Ein "Zeichensatz" ist eine Zuordnung von Zeichen zu ihren identifizierenden Codewerten.</span><span class="sxs-lookup"><span data-stu-id="282cf-104">A "character set" is a mapping of characters to their identifying code values.</span></span> <span data-ttu-id="282cf-105">Der Zeichensatz, der am häufigsten in Computern verwendet wird, ist [Unicode](unicode.md), ein globaler Standard für die Zeichencodierung.</span><span class="sxs-lookup"><span data-stu-id="282cf-105">The character set most commonly used in computers today is [Unicode](unicode.md), a global standard for character encoding.</span></span> <span data-ttu-id="282cf-106">Intern verwenden Windows-Anwendungen die UTF-16-Implementierung von Unicode.</span><span class="sxs-lookup"><span data-stu-id="282cf-106">Internally, Windows applications use the UTF-16 implementation of Unicode.</span></span> <span data-ttu-id="282cf-107">In UTF-16 werden die meisten Zeichen durch zwei Byte-Codes identifiziert.</span><span class="sxs-lookup"><span data-stu-id="282cf-107">In UTF-16, most characters are identified by two-byte codes.</span></span> <span data-ttu-id="282cf-108">Die weniger häufig verwendeten ergänzenden Zeichen werden jeweils durch ein Ersatz Zeichenpaar dargestellt, das ein paar von 2-Byte-Codes ist.</span><span class="sxs-lookup"><span data-stu-id="282cf-108">The less commonly used supplementary characters are each represented by a surrogate pair, which is a pair of two-byte codes.</span></span> <span data-ttu-id="282cf-109">Weitere Informationen finden Sie unter [Surrogates und ergänzende Zeichen](surrogates-and-supplementary-characters.md).</span><span class="sxs-lookup"><span data-stu-id="282cf-109">For more information, see [Surrogates and Supplementary Characters](surrogates-and-supplementary-characters.md).</span></span>

<span data-ttu-id="282cf-110">Einige Windows-Anwendungen müssen mit den älteren Zeichensätzen arbeiten, die für Windows Me/98/95 einheitlich sind.</span><span class="sxs-lookup"><span data-stu-id="282cf-110">Some Windows applications must work with the older character sets that are native to Windows Me/98/95.</span></span> <span data-ttu-id="282cf-111">[Windows-Codepages](code-pages.md) ermöglichen es Ihrer Anwendung, mit diesen Zeichensätzen zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="282cf-111">[Windows code pages](code-pages.md) allow your application to work with these character sets.</span></span> <span data-ttu-id="282cf-112">Diese Zeichensätze können in Folgendes unterteilt werden:</span><span class="sxs-lookup"><span data-stu-id="282cf-112">These character sets can be divided into:</span></span>

-   <span data-ttu-id="282cf-113">[Einzel Byte-Zeichensätze](single-byte-character-sets.md) (SBCS).</span><span class="sxs-lookup"><span data-stu-id="282cf-113">[Single-byte character sets](single-byte-character-sets.md) (SBCS).</span></span> <span data-ttu-id="282cf-114">In einer SBCS wird jedes Zeichen durch einen Wert von einem Byte breit identifiziert.</span><span class="sxs-lookup"><span data-stu-id="282cf-114">In an SBCS, each character is identified by a value one byte wide.</span></span>
-   <span data-ttu-id="282cf-115">Multibyte-Zeichensätze, insbesondere die [Doppelbyte-Zeichensätze](double-byte-character-sets.md) (DBCS).</span><span class="sxs-lookup"><span data-stu-id="282cf-115">Multibyte character sets, in particular the [double-byte character sets](double-byte-character-sets.md) (DBCS).</span></span> <span data-ttu-id="282cf-116">Multibyte-Zeichensätze bieten eine Möglichkeit, die große Anzahl von Zeichen in vielen asiatischen Sprachen darzustellen.</span><span class="sxs-lookup"><span data-stu-id="282cf-116">Multibyte character sets provide a means to represent the large number of characters in many Asian languages.</span></span>

<span data-ttu-id="282cf-117">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="282cf-117">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="282cf-118">Codepages</span><span class="sxs-lookup"><span data-stu-id="282cf-118">Code Pages</span></span>](code-pages.md)
-   [<span data-ttu-id="282cf-119">Doppelbyte-Zeichensätze</span><span class="sxs-lookup"><span data-stu-id="282cf-119">Double-byte Character Sets</span></span>](double-byte-character-sets.md)
-   [<span data-ttu-id="282cf-120">Einzel Byte-Zeichensätze</span><span class="sxs-lookup"><span data-stu-id="282cf-120">Single-byte Character Sets</span></span>](single-byte-character-sets.md)
-   [<span data-ttu-id="282cf-121">Surrogate und ergänzende Zeichen</span><span class="sxs-lookup"><span data-stu-id="282cf-121">Surrogates and Supplementary Characters</span></span>](surrogates-and-supplementary-characters.md)
-   [<span data-ttu-id="282cf-122">Unicode</span><span class="sxs-lookup"><span data-stu-id="282cf-122">Unicode</span></span>](unicode.md)

## <a name="related-topics"></a><span data-ttu-id="282cf-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="282cf-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="282cf-124">Informationen zu Unicode und Zeichensätzen</span><span class="sxs-lookup"><span data-stu-id="282cf-124">About Unicode and Character Sets</span></span>](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



