---
description: Eine sprach Kennung ist eine standardmäßige internationale numerische Abkürzung für die Sprache in einem Land oder einer geografischen Region.
ms.assetid: 076e2a43-256a-4646-a5c8-1d48ab08ce1a
title: Sprachen-IDs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e3e8f88a64d49d04402c0e72a3946bcddc41e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349031"
---
# <a name="language-identifiers"></a><span data-ttu-id="fef03-103">Sprachen-IDs</span><span class="sxs-lookup"><span data-stu-id="fef03-103">Language Identifiers</span></span>

<span data-ttu-id="fef03-104">Eine sprach Kennung ist eine standardmäßige internationale numerische Abkürzung für die [Sprache](locales-and-languages.md) in einem Land oder einer geografischen Region.</span><span class="sxs-lookup"><span data-stu-id="fef03-104">A language identifier is a standard international numeric abbreviation for the [language](locales-and-languages.md) in a country or geographical region.</span></span> <span data-ttu-id="fef03-105">Jede Sprache verfügt über einen eindeutigen sprach Bezeichner (Datentyp-langid), einen 16-Bit-Wert, der aus einer primär Sprachen-ID und einer unter Sprachen-ID besteht.</span><span class="sxs-lookup"><span data-stu-id="fef03-105">Each language has a unique language identifier (data type LANGID), a 16-bit value that consists of a primary language identifier and a sublanguage identifier.</span></span> <span data-ttu-id="fef03-106">Ausführliche Informationen zu sprach Bezeichnern finden Sie unter [sprach Bezeichner-Konstanten und-](language-identifier-constants-and-strings.md)Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="fef03-106">For details of language identifiers, see [Language Identifier Constants and Strings](language-identifier-constants-and-strings.md).</span></span>

<span data-ttu-id="fef03-107">Eine Sprach-ID wird mit dem [**-Makro makelangid**](/windows/desktop/api/Winnt/nf-winnt-makelangid) erstellt.</span><span class="sxs-lookup"><span data-stu-id="fef03-107">A language identifier is constructed using the [**MAKELANGID**](/windows/desktop/api/Winnt/nf-winnt-makelangid) macro.</span></span> <span data-ttu-id="fef03-108">In der folgenden Abbildung wird das Format der Bits in einem sprach Bezeichner dargestellt.</span><span class="sxs-lookup"><span data-stu-id="fef03-108">The following illustration shows the format of the bits in a language identifier.</span></span>

``` syntax
+-------------------------+-------------------------+
|     SubLanguage ID      |   Primary Language ID   |
+-------------------------+-------------------------+
15                    10  9                         0   bit
```

<span data-ttu-id="fef03-109">Im folgenden sind vordefinierte sprach Bezeichner aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="fef03-109">The following are predefined language identifiers:</span></span>

-   <span data-ttu-id="fef03-110">LANG \_ System \_ Standard.</span><span class="sxs-lookup"><span data-stu-id="fef03-110">LANG\_SYSTEM\_DEFAULT.</span></span> <span data-ttu-id="fef03-111">Die Standardsprache des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="fef03-111">The operating system default language.</span></span>
-   <span data-ttu-id="fef03-112">LANG \_ Benutzer \_ Standard.</span><span class="sxs-lookup"><span data-stu-id="fef03-112">LANG\_USER\_DEFAULT.</span></span> <span data-ttu-id="fef03-113">Sprache des aktuellen Benutzers.</span><span class="sxs-lookup"><span data-stu-id="fef03-113">The language of the current user.</span></span>

<span data-ttu-id="fef03-114">Die Anwendung kann die aktuellen sprach Bezeichner mithilfe der [mehrsprachigen Benutzeroberflächen](multilingual-user-interface.md) Funktionen abrufen.</span><span class="sxs-lookup"><span data-stu-id="fef03-114">Your application can retrieve the current language identifiers by using the [Multilingual User Interface](multilingual-user-interface.md) functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fef03-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fef03-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fef03-116">Gebiets Schemas und Sprachen</span><span class="sxs-lookup"><span data-stu-id="fef03-116">Locales and Languages</span></span>](locales-and-languages.md)
</dt> <dt>

[<span data-ttu-id="fef03-117">Sprach Bezeichner-Konstanten und Zeichen folgen</span><span class="sxs-lookup"><span data-stu-id="fef03-117">Language Identifier Constants and Strings</span></span>](language-identifier-constants-and-strings.md)
</dt> <dt>

[<span data-ttu-id="fef03-118">Multilingual User Interface</span><span class="sxs-lookup"><span data-stu-id="fef03-118">Multilingual User Interface</span></span>](multilingual-user-interface.md)
</dt> <dt>

[<span data-ttu-id="fef03-119">**Makelangid**</span><span class="sxs-lookup"><span data-stu-id="fef03-119">**MAKELANGID**</span></span>](/windows/desktop/api/Winnt/nf-winnt-makelangid)
</dt> </dl>

 

 



