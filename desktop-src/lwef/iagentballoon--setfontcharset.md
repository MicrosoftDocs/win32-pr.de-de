---
title: Iagentballoon setfontcharset
description: Iagentballoon setfontcharset
ms.assetid: ce1b152d-c8af-47ec-9e6b-5768dbcf3566
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6202aa144d13c3c7435be03721a3f8fd4878b93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340652"
---
# <a name="iagentballoonsetfontcharset"></a><span data-ttu-id="8e80f-103">Iagentballoon:: setfontcharset</span><span class="sxs-lookup"><span data-stu-id="8e80f-103">IAgentBalloon::SetFontCharSet</span></span>

<span data-ttu-id="8e80f-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="8e80f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontCharSet(
   short sFontCharSet  // character set displayed in word balloon
); 
```

<span data-ttu-id="8e80f-105">Legt den Zeichensatz der Schriftart fest, die in der Word-Sprechblase angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8e80f-105">Sets the character set of the font displayed in the word balloon.</span></span>

-   <span data-ttu-id="8e80f-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="8e80f-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="8e80f-107"><span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sfontcharset*</span><span class="sxs-lookup"><span data-stu-id="8e80f-107"><span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sFontCharSet*</span></span>
</dt> <dd>

<span data-ttu-id="8e80f-108">Der Zeichensatz der Schriftart.</span><span class="sxs-lookup"><span data-stu-id="8e80f-108">The character set of the font.</span></span> <span data-ttu-id="8e80f-109">Im folgenden finden Sie einige allgemeine Einstellungen für Value:</span><span class="sxs-lookup"><span data-stu-id="8e80f-109">The following are some common settings for value:</span></span>



|     |                                                                                        |
|-----|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e80f-110">0</span><span class="sxs-lookup"><span data-stu-id="8e80f-110">0</span></span>   | <span data-ttu-id="8e80f-111">Standard mäßige Windows-Zeichen (ANSI).</span><span class="sxs-lookup"><span data-stu-id="8e80f-111">Standard Windows characters (ANSI).</span></span>                                                    |
| <span data-ttu-id="8e80f-112">1</span><span class="sxs-lookup"><span data-stu-id="8e80f-112">1</span></span>   | <span data-ttu-id="8e80f-113">Standardzeichensatz.</span><span class="sxs-lookup"><span data-stu-id="8e80f-113">Default character set.</span></span>                                                                 |
| <span data-ttu-id="8e80f-114">2</span><span class="sxs-lookup"><span data-stu-id="8e80f-114">2</span></span>   | <span data-ttu-id="8e80f-115">Der Symbol Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="8e80f-115">The symbol character set.</span></span>                                                              |
| <span data-ttu-id="8e80f-116">128</span><span class="sxs-lookup"><span data-stu-id="8e80f-116">128</span></span> | <span data-ttu-id="8e80f-117">Doppelbyte-Zeichensatz (DBCS), der für die japanische Version von Windows eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="8e80f-117">Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span>            |
| <span data-ttu-id="8e80f-118">129</span><span class="sxs-lookup"><span data-stu-id="8e80f-118">129</span></span> | <span data-ttu-id="8e80f-119">Doppelbyte-Zeichensatz (DBCS), der für die koreanische Version von Windows eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="8e80f-119">Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span>              |
| <span data-ttu-id="8e80f-120">134</span><span class="sxs-lookup"><span data-stu-id="8e80f-120">134</span></span> | <span data-ttu-id="8e80f-121">Doppelbyte-Zeichensatz (DBCS), der für die vereinfachte chinesische Version von Windows eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="8e80f-121">Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span>  |
| <span data-ttu-id="8e80f-122">136</span><span class="sxs-lookup"><span data-stu-id="8e80f-122">136</span></span> | <span data-ttu-id="8e80f-123">Doppelbyte-Zeichensatz (DBCS), der für die traditionelle chinesische Version von Windows eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="8e80f-123">Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span> |
| <span data-ttu-id="8e80f-124">255</span><span class="sxs-lookup"><span data-stu-id="8e80f-124">255</span></span> | <span data-ttu-id="8e80f-125">Erweiterte Zeichen, die normalerweise von MS-DOS-Anwendungen angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="8e80f-125">Extended characters usually displayed by MS-DOS applications.</span></span>                          |



 

</dd> </dl>

<span data-ttu-id="8e80f-126">Weitere Zeichensatz Werte finden Sie in der Platform SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="8e80f-126">For other character set values, consult the Platform SDK documentation.</span></span>

<span data-ttu-id="8e80f-127">Der Standardzeichensatz, der in der Wort Sprechblase eines Zeichens verwendet wird, wird im Microsoft-Agent-Zeichen-Editor definiert.</span><span class="sxs-lookup"><span data-stu-id="8e80f-127">The default character set used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="8e80f-128">Sie können es mit [**iagentballoon:: setfontcharset**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**)ändern.</span><span class="sxs-lookup"><span data-stu-id="8e80f-128">You can change it with [**IAgentBalloon::SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**).</span></span> <span data-ttu-id="8e80f-129">Der Benutzer kann jedoch die Zeichensatz Einstellung für alle Zeichen überschreiben, indem er das Eigenschaften Blatt Microsoft-Agent verwendet.</span><span class="sxs-lookup"><span data-stu-id="8e80f-129">However, the user can override the character set setting for all characters using the Microsoft Agent property sheet.</span></span> <span data-ttu-id="8e80f-130">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="8e80f-130">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="8e80f-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8e80f-131">See Also</span></span>

[<span data-ttu-id="8e80f-132">**Iagentballoon:: getfontcharset**</span><span class="sxs-lookup"><span data-stu-id="8e80f-132">**IAgentBalloon::GetFontCharSet**</span></span>](iagentballoon--getfontcharset.md)


 

 




