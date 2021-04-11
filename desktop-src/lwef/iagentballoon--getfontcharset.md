---
title: Iagentballoon getfontcharset
description: Iagentballoon getfontcharset
ms.assetid: 1ab5767a-31e3-449c-b242-f20b11336ca0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f544df6c09fb00d346015b610751dd23738820
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206932"
---
# <a name="iagentballoongetfontcharset"></a><span data-ttu-id="159cb-103">Iagentballoon:: getfontcharset</span><span class="sxs-lookup"><span data-stu-id="159cb-103">IAgentBalloon::GetFontCharSet</span></span>

<span data-ttu-id="159cb-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="159cb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontCharSet(
   short * psFontCharSet  // character set displayed in word balloon
); 
```

<span data-ttu-id="159cb-105">Gibt den Zeichensatz der Schriftart an, die in einer Wort Sprechblase angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="159cb-105">Indicates the character set of the font displayed in a word balloon.</span></span>

-   <span data-ttu-id="159cb-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="159cb-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="159cb-107"><span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psfontcharset*</span><span class="sxs-lookup"><span data-stu-id="159cb-107"><span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psFontCharSet*</span></span>
</dt> <dd>

<span data-ttu-id="159cb-108">Die Adresse eines Werts, der den Zeichensatz der Schriftart empfängt.</span><span class="sxs-lookup"><span data-stu-id="159cb-108">The address of a value that receives the font's character set.</span></span> <span data-ttu-id="159cb-109">Im folgenden finden Sie einige allgemeine Einstellungen für Value:</span><span class="sxs-lookup"><span data-stu-id="159cb-109">The following are some common settings for value:</span></span>



|     |                                                                                        |
|-----|----------------------------------------------------------------------------------------|
| <span data-ttu-id="159cb-110">0</span><span class="sxs-lookup"><span data-stu-id="159cb-110">0</span></span>   | <span data-ttu-id="159cb-111">Standard mäßige Windows-Zeichen (ANSI).</span><span class="sxs-lookup"><span data-stu-id="159cb-111">Standard Windows characters (ANSI).</span></span>                                                    |
| <span data-ttu-id="159cb-112">1</span><span class="sxs-lookup"><span data-stu-id="159cb-112">1</span></span>   | <span data-ttu-id="159cb-113">Standardzeichensatz.</span><span class="sxs-lookup"><span data-stu-id="159cb-113">Default character set.</span></span>                                                                 |
| <span data-ttu-id="159cb-114">2</span><span class="sxs-lookup"><span data-stu-id="159cb-114">2</span></span>   | <span data-ttu-id="159cb-115">Der Symbol Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="159cb-115">The symbol character set.</span></span>                                                              |
| <span data-ttu-id="159cb-116">128</span><span class="sxs-lookup"><span data-stu-id="159cb-116">128</span></span> | <span data-ttu-id="159cb-117">Doppelbyte-Zeichensatz (DBCS), der für die japanische Version von Windows eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="159cb-117">Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span>            |
| <span data-ttu-id="159cb-118">129</span><span class="sxs-lookup"><span data-stu-id="159cb-118">129</span></span> | <span data-ttu-id="159cb-119">Doppelbyte-Zeichensatz (DBCS), der für die koreanische Version von Windows eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="159cb-119">Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span>              |
| <span data-ttu-id="159cb-120">134</span><span class="sxs-lookup"><span data-stu-id="159cb-120">134</span></span> | <span data-ttu-id="159cb-121">Doppelbyte-Zeichensatz (DBCS), der für die vereinfachte chinesische Version von Windows eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="159cb-121">Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span>  |
| <span data-ttu-id="159cb-122">136</span><span class="sxs-lookup"><span data-stu-id="159cb-122">136</span></span> | <span data-ttu-id="159cb-123">Doppelbyte-Zeichensatz (DBCS), der für die traditionelle chinesische Version von Windows eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="159cb-123">Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span> |
| <span data-ttu-id="159cb-124">255</span><span class="sxs-lookup"><span data-stu-id="159cb-124">255</span></span> | <span data-ttu-id="159cb-125">Erweiterte Zeichen, die normalerweise von MS-DOS-Anwendungen angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="159cb-125">Extended characters usually displayed by MS-DOS applications.</span></span>                          |



 

</dd> </dl>

<span data-ttu-id="159cb-126">Weitere Zeichensatz Werte finden Sie in der Platform SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="159cb-126">For other character set values, consult the Platform SDK documentation.</span></span>

<span data-ttu-id="159cb-127">Der Standardzeichensatz, der in der Wort Sprechblase eines Zeichens verwendet wird, wird im Microsoft-Agent-Zeichen-Editor definiert.</span><span class="sxs-lookup"><span data-stu-id="159cb-127">The default character set used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="159cb-128">Sie können es mit [**iagentballoon:: setfontcharset**](iagentballoon--setfontcharset.md)ändern.</span><span class="sxs-lookup"><span data-stu-id="159cb-128">You can change it using [**IAgentBalloon::SetFontCharSet**](iagentballoon--setfontcharset.md).</span></span> <span data-ttu-id="159cb-129">Der Benutzer kann jedoch die Zeichensatz Einstellung für alle Zeichen überschreiben, indem er das Eigenschaften Blatt Microsoft-Agent verwendet.</span><span class="sxs-lookup"><span data-stu-id="159cb-129">However, the user can override the character set setting for all characters using the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="159cb-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="159cb-130">See Also</span></span>

[<span data-ttu-id="159cb-131">**Iagentballoon:: setfontcharset**</span><span class="sxs-lookup"><span data-stu-id="159cb-131">**IAgentBalloon::SetFontCharSet**</span></span>](iagentballoon--setfontcharset.md)


 

 




