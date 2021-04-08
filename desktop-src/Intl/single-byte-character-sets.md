---
description: Bei einem Einzel Byte-Zeichensatz (SBCS) handelt es sich um eine Zuordnung von 256 einzelnen Zeichen zu ihren identifizierenden Codewerten, die als Codepage implementiert werden.
ms.assetid: 53f74132-91aa-4257-846a-f6e1f2f9ae0b
title: Einzel Byte-Zeichensätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5618b191b83e33333dce2a290d8c9a7181233df4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960841"
---
# <a name="single-byte-character-sets"></a><span data-ttu-id="3edea-103">Einzel Byte-Zeichensätze</span><span class="sxs-lookup"><span data-stu-id="3edea-103">Single-byte Character Sets</span></span>

<span data-ttu-id="3edea-104">Bei einem Einzel Byte-Zeichensatz (SBCS) handelt es sich um eine Zuordnung von 256 einzelnen Zeichen zu ihren identifizierenden Codewerten, die als Codepage implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="3edea-104">A single-byte character set (SBCS) is a mapping of 256 individual characters to their identifying code values, implemented as a code page.</span></span> <span data-ttu-id="3edea-105">SBCS können entweder einer Windows-Codepage oder einer OEM-Codepage entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3edea-105">An SBCS can correspond either to a Windows code page or an OEM code page.</span></span> <span data-ttu-id="3edea-106">Eine SBCS-Codepage kann auch eine nicht systemeigene Codepage einschließen, z. b. eine EBCDIC-Codepage.</span><span class="sxs-lookup"><span data-stu-id="3edea-106">An SBCS code page can also include a non-native code page, for example, an EBCDIC code page.</span></span> <span data-ttu-id="3edea-107">Definitionen dieser Codepages finden Sie unter [Codepages](code-pages.md).</span><span class="sxs-lookup"><span data-stu-id="3edea-107">For definitions of these code pages, see [Code Pages](code-pages.md).</span></span>

> [!Note]  
> <span data-ttu-id="3edea-108">Neue Windows-Anwendungen sollten [Unicode](unicode.md) verwenden, um die Inkonsistenzen von unterschiedlichen Codepages und eine einfache Lokalisierung zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="3edea-108">New Windows applications should use [Unicode](unicode.md) to avoid the inconsistencies of varied code pages and for ease of localization.</span></span> <span data-ttu-id="3edea-109">Einige Legacy Protokolle erfordern jedoch die Verwendung eines SBCS.</span><span class="sxs-lookup"><span data-stu-id="3edea-109">However, some legacy protocols require the use of an SBCS.</span></span> <span data-ttu-id="3edea-110">Jede SBCS-Codepage unterstützt unterschiedliche Zeichen, aber keine Seite unterstützt die vollständige Breite von Zeichen, die von Unicode bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3edea-110">Each SBCS code page supports different characters, but no page supports the full breadth of characters provided by Unicode.</span></span> <span data-ttu-id="3edea-111">Jede SBCS-Codepage unterstützt eine andere Teilmenge, unterschiedlich codiert.</span><span class="sxs-lookup"><span data-stu-id="3edea-111">Each SBCS code page supports a different subset, differently encoded.</span></span> <span data-ttu-id="3edea-112">Daten, die von einer SBCS-Codepage in eine andere konvertiert werden, unterliegen Beschädigungen, da der gleiche Datenwert auf unterschiedlichen Codepages ein anderes Zeichen codieren kann.</span><span class="sxs-lookup"><span data-stu-id="3edea-112">Data converted from one SBCS code page to another is subject to corruption, because the same data value on different code pages can encode a different character.</span></span> <span data-ttu-id="3edea-113">Daten, die von Unicode in SBCS konvertiert werden, unterliegen Datenverlusten, da eine bestimmte Codepage nicht jedes Zeichen darstellen kann, das in den einzelnen Unicode-Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3edea-113">Data converted from Unicode to SBCS is subject to data loss because a given code page might not be able to represent every character used in that particular Unicode data.</span></span>

 

<span data-ttu-id="3edea-114">Ihre Anwendungen verwenden SBCS-Windows-Codepage mit den "A"-Versionen von Windows Functions.</span><span class="sxs-lookup"><span data-stu-id="3edea-114">Your applications use SBCS Windows code pages with the "A" versions of Windows functions.</span></span> <span data-ttu-id="3edea-115">Weitere Informationen finden Sie unter [Konventionen für Funktionsprototypen](conventions-for-function-prototypes.md) und [Codepages](code-pages.md).</span><span class="sxs-lookup"><span data-stu-id="3edea-115">See [Conventions for Function Prototypes](conventions-for-function-prototypes.md) and [Code Pages](code-pages.md).</span></span> <span data-ttu-id="3edea-116">Um eine SBCS-Codepage zu identifizieren, kann eine Anwendung die [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) -Funktion oder die [**getcpinfoex**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="3edea-116">To help identify an SBCS code page, an application can use the [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) or [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) function.</span></span> <span data-ttu-id="3edea-117">Außerdem kann eine Anwendung die Funktionen [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) und [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) zum Zuordnen zwischen Unicode-und SBCS-Zeichen folgen verwenden.</span><span class="sxs-lookup"><span data-stu-id="3edea-117">In addition, an application can use the [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) and [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) functions to map between Unicode and SBCS strings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3edea-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3edea-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3edea-119">Zeichensätze</span><span class="sxs-lookup"><span data-stu-id="3edea-119">Character Sets</span></span>](character-sets.md)
</dt> <dt>

[<span data-ttu-id="3edea-120">Doppelbyte-Zeichensätze</span><span class="sxs-lookup"><span data-stu-id="3edea-120">Double-byte Character Sets</span></span>](double-byte-character-sets.md)
</dt> </dl>

 

 



