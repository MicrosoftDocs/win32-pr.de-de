---
description: Der FORMSOF-Begriff führt Übereinstimmungen mit anderen linguistischen Formen des Worts aus.
ms.assetid: b705b8bc-dc2c-4cee-8306-f494b0f96cbf
title: FORMSOF-Begriff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20504a7a36c7f0cb9c69b9513f33446501641bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345015"
---
# <a name="formsof-term"></a><span data-ttu-id="39cae-103">FORMSOF-Begriff</span><span class="sxs-lookup"><span data-stu-id="39cae-103">FORMSOF Term</span></span>

<span data-ttu-id="39cae-104">Der FORMSOF-Begriff führt Übereinstimmungen mit anderen linguistischen Formen des Worts aus.</span><span class="sxs-lookup"><span data-stu-id="39cae-104">The FORMSOF term performs matches using other linguistic forms of the word.</span></span> <span data-ttu-id="39cae-105">Im folgenden finden Sie die Begriffs Syntax für FORMSOF:</span><span class="sxs-lookup"><span data-stu-id="39cae-105">The following is the FORMSOF term syntax:</span></span>


```
FORMSOF (<generation_type>,<match_words>)
```



<span data-ttu-id="39cae-106">Der generierungstyp gibt an, wie Microsoft Windows Search die alternativen Word-Formulare auswählt.</span><span class="sxs-lookup"><span data-stu-id="39cae-106">The generation type specifies how Microsoft Windows Search chooses the alternative word forms.</span></span> <span data-ttu-id="39cae-107">Der Flexions Wert wählt Alternative Wende-Formulare für die **Übereinstimmungs** Wörter aus.</span><span class="sxs-lookup"><span data-stu-id="39cae-107">The **INFLECTIONAL** value chooses alternative inflection forms for the match words.</span></span> <span data-ttu-id="39cae-108">Wenn das Wort ein Verb ist, werden alternative Mandanten verwendet.</span><span class="sxs-lookup"><span data-stu-id="39cae-108">If the word is a verb, alternative tenses are used.</span></span> <span data-ttu-id="39cae-109">Wenn es sich bei dem Wort um ein Substantiv handelt, werden die Formen Singular, Plural und possessiv verwendet, um Übereinstimmungen zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="39cae-109">If the word is a noun, the singular, plural, and possessive forms are used to detect matches.</span></span>

<span data-ttu-id="39cae-110">Der \_ Wert für die Übereinstimmungs Wörter ist ein oder mehrere Wörter, die durch Kommas getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="39cae-110">The match\_words value is one or more words, separated by commas.</span></span>

## <a name="examples"></a><span data-ttu-id="39cae-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="39cae-111">Examples</span></span>

<span data-ttu-id="39cae-112">Im folgenden Beispiel wird nach Flexions Übereinstimmungen für das Wort "Run" gesucht.</span><span class="sxs-lookup"><span data-stu-id="39cae-112">The following example searches for inflectional matches for the word "run".</span></span> <span data-ttu-id="39cae-113">Dieses Beispiel entspricht Dokumenten, die "Run", "Running" oder "ran" enthalten.</span><span class="sxs-lookup"><span data-stu-id="39cae-113">This example matches documents containing "run", "running", or "ran".</span></span>


```
...CONTAINS('FORMSOF(INFLECTIONAL,"run")')
```



## <a name="related-topics"></a><span data-ttu-id="39cae-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="39cae-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="39cae-115">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="39cae-115">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="39cae-116">Frei Text Prädikat</span><span class="sxs-lookup"><span data-stu-id="39cae-116">FREETEXT Predicate</span></span>](-search-sql-freetext.md)
</dt> <dt>

[<span data-ttu-id="39cae-117">WHERE-Klausel</span><span class="sxs-lookup"><span data-stu-id="39cae-117">WHERE Clause</span></span>](-search-sql-where.md)
</dt> </dl>

 

 



