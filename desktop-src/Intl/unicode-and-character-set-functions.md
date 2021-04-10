---
description: Die folgenden Funktionen werden mit Zeichensätzen verwendet.
ms.assetid: 1799f5da-1391-4b6e-ac13-718017a77557
title: Unicode-und Zeichensatz Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6996139d8a9bb426c21a460ac2bcb1358e6c8e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050323"
---
# <a name="unicode-and-character-set-functions"></a><span data-ttu-id="67cf1-103">Unicode-und Zeichensatz Funktionen</span><span class="sxs-lookup"><span data-stu-id="67cf1-103">Unicode and Character Set Functions</span></span>

<span data-ttu-id="67cf1-104">Die folgenden Funktionen werden mit Zeichensätzen verwendet.</span><span class="sxs-lookup"><span data-stu-id="67cf1-104">The following functions are used with character sets.</span></span>



| <span data-ttu-id="67cf1-105">Funktion</span><span class="sxs-lookup"><span data-stu-id="67cf1-105">Function</span></span>                                                       | <span data-ttu-id="67cf1-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="67cf1-106">Description</span></span>                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67cf1-107">**Gettextcharset**</span><span class="sxs-lookup"><span data-stu-id="67cf1-107">**GetTextCharset**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharset)                       | <span data-ttu-id="67cf1-108">Ruft einen Zeichensatz Bezeichner für die Schriftart ab, die derzeit in einem angegebenen Gerätekontext ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="67cf1-108">Retrieves a character set identifier for the font that is currently selected into a specified device context.</span></span>         |
| [<span data-ttu-id="67cf1-109">**Gettextcharctinfo**</span><span class="sxs-lookup"><span data-stu-id="67cf1-109">**GetTextCharsetInfo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharsetinfo)               | <span data-ttu-id="67cf1-110">Ruft Informationen über den Zeichensatz der Schriftart ab, die derzeit in einem angegebenen Gerätekontext ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="67cf1-110">Retrieves information about the character set of the font that is currently selected into a specified device context.</span></span> |
| [<span data-ttu-id="67cf1-111">**Isdbcsleadbyte**</span><span class="sxs-lookup"><span data-stu-id="67cf1-111">**IsDBCSLeadByte**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyte)                       | <span data-ttu-id="67cf1-112">Bestimmt, ob ein angegebenes Zeichen ein führendes Byte für die standardmäßige Windows-ANSI-Codepage (CP \_ ACP) ist.</span><span class="sxs-lookup"><span data-stu-id="67cf1-112">Determines if a specified character is a lead byte for the system default Windows ANSI code page (CP\_ACP).</span></span>           |
| [<span data-ttu-id="67cf1-113">**Isdbcsleadbyteex**</span><span class="sxs-lookup"><span data-stu-id="67cf1-113">**IsDBCSLeadByteEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyteex)                   | <span data-ttu-id="67cf1-114">Bestimmt, ob ein angegebenes Zeichen potenziell ein führendes Byte ist.</span><span class="sxs-lookup"><span data-stu-id="67cf1-114">Determines if a specified character is potentially a lead byte.</span></span>                                                       |
| [<span data-ttu-id="67cf1-115">**IsTextUnicode**</span><span class="sxs-lookup"><span data-stu-id="67cf1-115">**IsTextUnicode**</span></span>](/windows/desktop/api/Winbase/nf-winbase-istextunicode)                         | <span data-ttu-id="67cf1-116">Bestimmt, ob ein Puffer wahrscheinlich eine Form von Unicode-Text enthält.</span><span class="sxs-lookup"><span data-stu-id="67cf1-116">Determines if a buffer is likely to contain a form of Unicode text.</span></span>                                                   |
| [<span data-ttu-id="67cf1-117">**MultiByteToWideChar muss**</span><span class="sxs-lookup"><span data-stu-id="67cf1-117">**MultiByteToWideChar**</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar)             | <span data-ttu-id="67cf1-118">Ordnet eine Zeichenfolge einer UTF-16-Zeichenfolge (breit Zeichen) zu.</span><span class="sxs-lookup"><span data-stu-id="67cf1-118">Maps a character string to a UTF-16 (wide character) string.</span></span>                                                          |
| [<span data-ttu-id="67cf1-119">**Translatecharltinfo**</span><span class="sxs-lookup"><span data-stu-id="67cf1-119">**TranslateCharsetInfo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-translatecharsetinfo)           | <span data-ttu-id="67cf1-120">Übersetzt Zeichensatz Informationen und legt alle Elemente einer Zielstruktur auf entsprechende Werte fest.</span><span class="sxs-lookup"><span data-stu-id="67cf1-120">Translates character set information and sets all members of a destination structure to appropriate values.</span></span>           |
| [<span data-ttu-id="67cf1-121">**WideCharToMultiByte**</span><span class="sxs-lookup"><span data-stu-id="67cf1-121">**WideCharToMultiByte**</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte)             | <span data-ttu-id="67cf1-122">Ordnet eine UTF-16-Zeichenfolge (breit Zeichen) einer neuen Zeichenfolge zu.</span><span class="sxs-lookup"><span data-stu-id="67cf1-122">Maps a UTF-16 (wide character) string to a new character string.</span></span>                                                      |
| <span data-ttu-id="67cf1-123">[**BytesToUnicode**](/previous-versions/dd317724(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="67cf1-123">[**BytesToUnicode**](/previous-versions/dd317724(v=vs.85))</span></span>                       | <span data-ttu-id="67cf1-124">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="67cf1-124">Do not use.</span></span>                                                                                                           |
| [<span data-ttu-id="67cf1-125">**Nlsdllcodepagetranslation**</span><span class="sxs-lookup"><span data-stu-id="67cf1-125">**NlsDllCodePageTranslation**</span></span>](/windows/desktop/api/Gb18030/nf-gb18030-nlsdllcodepagetranslation) | <span data-ttu-id="67cf1-126">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="67cf1-126">Do not use.</span></span>                                                                                                           |
| <span data-ttu-id="67cf1-127">[**Unicodebybytes**](/previous-versions/windows/desktop/legacy/dd374082(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="67cf1-127">[**UnicodeToBytes**](/previous-versions/windows/desktop/legacy/dd374082(v=vs.85))</span></span>                       | <span data-ttu-id="67cf1-128">Nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="67cf1-128">Do not use.</span></span>                                                                                                           |



 

 

 
