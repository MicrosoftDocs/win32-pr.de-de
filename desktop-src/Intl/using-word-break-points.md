---
description: Wenn die Anwendung mit ganzen Wörtern umgeht, werden gültige Positionen für die Einfügemarke durch den Wert des fwordstopp-Members der \_ logattr-Skript Struktur gekennzeichnet. Dieser Wert wird abgerufen, indem scriptbreak aufgerufen wird.
ms.assetid: c9bbfb51-727a-45ff-8450-774bc106f9f7
title: Verwenden von Wort Break Points
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9cf68d5c90b6e93a6e6f15706ec357c7a33b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218684"
---
# <a name="using-word-break-points"></a><span data-ttu-id="00550-104">Verwenden von Wort Break Points</span><span class="sxs-lookup"><span data-stu-id="00550-104">Using Word Break Points</span></span>

<span data-ttu-id="00550-105">Wenn die Anwendung mit ganzen Wörtern umgeht, werden gültige Positionen für die Einfügemarke durch den Wert des **fwordstopp** -Members der [**\_ logattr-Skript**](/windows/win32/api/usp10/ns-usp10-script_logattr) Struktur gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="00550-105">When the application is dealing with whole words, valid positions for the caret are marked by the value of the **fWordStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure.</span></span> <span data-ttu-id="00550-106">Dieser Wert wird abgerufen, indem [**scriptbreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="00550-106">This value is retrieved by making a call to [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).</span></span>

<span data-ttu-id="00550-107">Gültige Positionen für den Umbruch von Zeilen zwischen Wörtern werden durch den von [**scriptbreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)abgerufenen **fsoft Break** -Wert markiert.</span><span class="sxs-lookup"><span data-stu-id="00550-107">Valid positions for breaking lines between words are marked by the **fSoftBreak** value retrieved by [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).</span></span>

## <a name="related-topics"></a><span data-ttu-id="00550-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="00550-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00550-109">Verwenden von uniscri</span><span class="sxs-lookup"><span data-stu-id="00550-109">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 



