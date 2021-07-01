---
title: IAgentBalloon GetFontCharSet
description: IAgentBalloon GetFontCharSet
ms.assetid: 1ab5767a-31e3-449c-b242-f20b11336ca0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f809fbd83e44259c96184c9f364a85151ec9ddde
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120405"
---
# <a name="iagentballoongetfontcharset"></a><span data-ttu-id="4af86-103">IAgentBalloon::GetFontCharSet</span><span class="sxs-lookup"><span data-stu-id="4af86-103">IAgentBalloon::GetFontCharSet</span></span>

<span data-ttu-id="4af86-104">\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="4af86-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontCharSet(
   short * psFontCharSet  // character set displayed in word balloon
); 
```

<span data-ttu-id="4af86-105">Gibt den Zeichensatz der Schriftart an, die in einer Wortsprechblase angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4af86-105">Indicates the character set of the font displayed in a word balloon.</span></span>

-   <span data-ttu-id="4af86-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="4af86-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="4af86-107"><span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psFontCharSet*</span><span class="sxs-lookup"><span data-stu-id="4af86-107"><span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psFontCharSet*</span></span>
</dt> <dd>

<span data-ttu-id="4af86-108">Die Adresse eines Werts, der den Zeichensatz der Schriftart empfängt.</span><span class="sxs-lookup"><span data-stu-id="4af86-108">The address of a value that receives the font's character set.</span></span> <span data-ttu-id="4af86-109">Im Folgenden finden Sie einige allgemeine Einstellungen für value:</span><span class="sxs-lookup"><span data-stu-id="4af86-109">The following are some common settings for value:</span></span>



| <span data-ttu-id="4af86-110">Wert</span><span class="sxs-lookup"><span data-stu-id="4af86-110">Value</span></span>    | <span data-ttu-id="4af86-111">Zeichensatz</span><span class="sxs-lookup"><span data-stu-id="4af86-111">Character set</span></span>                                                                                       |
|-----|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4af86-112">0</span><span class="sxs-lookup"><span data-stu-id="4af86-112">0</span></span>   | <span data-ttu-id="4af86-113">Standard-Windows-Zeichen (ANSI).</span><span class="sxs-lookup"><span data-stu-id="4af86-113">Standard Windows characters (ANSI).</span></span>                                                    |
| <span data-ttu-id="4af86-114">1</span><span class="sxs-lookup"><span data-stu-id="4af86-114">1</span></span>   | <span data-ttu-id="4af86-115">Standardzeichensatz.</span><span class="sxs-lookup"><span data-stu-id="4af86-115">Default character set.</span></span>                                                                 |
| <span data-ttu-id="4af86-116">2</span><span class="sxs-lookup"><span data-stu-id="4af86-116">2</span></span>   | <span data-ttu-id="4af86-117">Der Symbolzeichensatz.</span><span class="sxs-lookup"><span data-stu-id="4af86-117">The symbol character set.</span></span>                                                              |
| <span data-ttu-id="4af86-118">128</span><span class="sxs-lookup"><span data-stu-id="4af86-118">128</span></span> | <span data-ttu-id="4af86-119">Doppel-Byte-Zeichensatz (DBCS), der für die japanische Version von Windows eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="4af86-119">Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span>            |
| <span data-ttu-id="4af86-120">129</span><span class="sxs-lookup"><span data-stu-id="4af86-120">129</span></span> | <span data-ttu-id="4af86-121">Doppel-Byte-Zeichensatz (DBCS), der für die koreanische Version von Windows eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="4af86-121">Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span>              |
| <span data-ttu-id="4af86-122">134</span><span class="sxs-lookup"><span data-stu-id="4af86-122">134</span></span> | <span data-ttu-id="4af86-123">Doppel-Byte-Zeichensatz (Double-Byte Character Set, DBCS), der für die vereinfachte chinesische Version von Windows eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="4af86-123">Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span>  |
| <span data-ttu-id="4af86-124">136</span><span class="sxs-lookup"><span data-stu-id="4af86-124">136</span></span> | <span data-ttu-id="4af86-125">Doppel-Byte-Zeichensatz (DBCS), der für die traditionelle chinesische Version von Windows eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="4af86-125">Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span> |
| <span data-ttu-id="4af86-126">255</span><span class="sxs-lookup"><span data-stu-id="4af86-126">255</span></span> | <span data-ttu-id="4af86-127">Erweiterte Zeichen werden in der Regel von MS-DOS-Anwendungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4af86-127">Extended characters usually displayed by MS-DOS applications.</span></span>                          |



 

</dd> </dl>

<span data-ttu-id="4af86-128">Weitere Zeichensatzwerte finden Sie in der Dokumentation zum Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="4af86-128">For other character set values, consult the Platform SDK documentation.</span></span>

<span data-ttu-id="4af86-129">Der Standardzeichensatz, der in der Wortsprechblase eines Zeichens verwendet wird, wird im Microsoft Agent-Zeichen-Editor definiert.</span><span class="sxs-lookup"><span data-stu-id="4af86-129">The default character set used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="4af86-130">Sie können es mithilfe von [**IAgentBalloon::SetFontCharSet ändern.**](iagentballoon--setfontcharset.md)</span><span class="sxs-lookup"><span data-stu-id="4af86-130">You can change it using [**IAgentBalloon::SetFontCharSet**](iagentballoon--setfontcharset.md).</span></span> <span data-ttu-id="4af86-131">Der Benutzer kann jedoch die Zeichensatzeinstellung für alle Zeichen mithilfe des Microsoft Agent-Eigenschaftenblatts überschreiben.</span><span class="sxs-lookup"><span data-stu-id="4af86-131">However, the user can override the character set setting for all characters using the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="4af86-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4af86-132">See Also</span></span>

[<span data-ttu-id="4af86-133">**IAgentBalloon::SetFontCharSet**</span><span class="sxs-lookup"><span data-stu-id="4af86-133">**IAgentBalloon::SetFontCharSet**</span></span>](iagentballoon--setfontcharset.md)


 

 




