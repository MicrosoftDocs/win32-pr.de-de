---
title: Iagentcharakteriex-Ansicht
description: Iagentcharakteriex-Ansicht
ms.assetid: 64bfa388-0db7-423c-a4af-64a9f7351e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd1bedfc2665c80d522ccb38c7c3073580136db
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038894"
---
# <a name="iagentcharacterexthink"></a><span data-ttu-id="66163-103">Iagentcharakteriex:: Think</span><span class="sxs-lookup"><span data-stu-id="66163-103">IAgentCharacterEx::Think</span></span>

<span data-ttu-id="66163-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="66163-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Think(
   BSTR bszText,    // text to think
   long * pdwReqID  // address of a request ID
);
```

<span data-ttu-id="66163-105">Zeigt die gedachte Word-Sprechblase des Zeichens mit dem angegebenen Text an.</span><span class="sxs-lookup"><span data-stu-id="66163-105">Displays the character's thought word balloon with the specified text.</span></span>

-   <span data-ttu-id="66163-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="66163-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="66163-107"><span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bsztext*</span><span class="sxs-lookup"><span data-stu-id="66163-107"><span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*</span></span>
</dt> <dd>

<span data-ttu-id="66163-108">Der Text, der in der Gedanken Sprechblase des Zeichens angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="66163-108">The text to appear in the character's thought balloon.</span></span>

</dd> <dt>

<span data-ttu-id="66163-109"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwreqid*</span><span class="sxs-lookup"><span data-stu-id="66163-109"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="66163-110">Adresse einer Variablen **, die die Anforderungs Anforderungs** -ID empfängt.</span><span class="sxs-lookup"><span data-stu-id="66163-110">Address of a variable that receives the **Think** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="66163-111">Wie die [**iagentcharacter:: Speak**](iagentcharacter--speak.md) -Methode ist die Methode " **Think** " eine Anforderung in der Warteschlange, die Text in einer Wort Sprechblase anzeigt, mit dem Unterschied, dass die Gedanken in einer speziellen Sprechblase angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="66163-111">Like the [**IAgentCharacter::Speak**](iagentcharacter--speak.md) method, the **Think** method is a queued request that displays text in a word balloon, except that thoughts display in a special thought balloon.</span></span> <span data-ttu-id="66163-112">Die Sprechblase unterstützt nur das Lesezeichen-Steuerelement Tag (**\\ MRK**) und ignoriert alle anderen sprachkontrolltags.</span><span class="sxs-lookup"><span data-stu-id="66163-112">The thought balloon supports only the Bookmark speech control tag (**\\Mrk**) and ignores any other speech control tags.</span></span> <span data-ttu-id="66163-113">Anders als bei **iagentcharacter:: Speak** ändert die " **Think** "-Methode nicht den Animations Zustand des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="66163-113">Unlike **IAgentCharacter::Speak**, the **Think** method does not change the character's animation state.</span></span>

<span data-ttu-id="66163-114">Die [**iagentballoon**](/windows/desktop/lwef/iagentballoon) -Einstellungen gelten auch für den Darstellungsstil der Gedanken Sprechblase.</span><span class="sxs-lookup"><span data-stu-id="66163-114">The [**IAgentBalloon**](/windows/desktop/lwef/iagentballoon) settings also apply to the appearance style of the thought balloon.</span></span> <span data-ttu-id="66163-115">Beispielsweise muss die [**aktivierte**](enabled-property.md) Eigenschaft der Sprechblase auch **true** sein, damit der Text angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="66163-115">For example, the balloon's [**Enabled**](enabled-property.md) property must also be **True** for the text to display.</span></span>

<span data-ttu-id="66163-116">Das automatische Wörter brechen des Microsoft-Agents in der Word-Sprechblase unterbricht Wörter mit Leerzeichen (z. b. Leerzeichen und Tab).</span><span class="sxs-lookup"><span data-stu-id="66163-116">Microsoft Agent's automatic word breaking in the word balloon breaks words using white-space characters (for example, space and tab).</span></span> <span data-ttu-id="66163-117">Es kann jedoch sein, dass ein Wort auch an die Sprechblase angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="66163-117">However, it may break a word to fit the balloon as well.</span></span> <span data-ttu-id="66163-118">Fügen Sie in Sprachen wie Japanisch, Chinesisch und Thailändisch, in denen Leerzeichen nicht zum Abbrechen von Wörtern verwendet werden, ein Unicode-Zeichen mit 0 (null) Zeichen (0x200b) zwischen Zeichen ein, um logische Wort Umbrüche zu definieren.</span><span class="sxs-lookup"><span data-stu-id="66163-118">In languages like Japanese, Chinese, and Thai, where spaces are not used to break words, insert a Unicode zero width space character (0x200B) between characters to define logical word breaks.</span></span>

> [!Note]  
> <span data-ttu-id="66163-119">Legen Sie die Sprach-ID des Zeichens (mit [**iagentcharakteriex:: setlanguageid**](iagentcharacterex--setlanguageid.md) ) fest, bevor Sie die [**iagentcharacter:: Speak**](iagentcharacter--speak.md) -Methode verwenden, um die entsprechende Textanzeige innerhalb der Word-Sprechblase sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="66163-119">Set the character's language ID (using [**IAgentCharacterEx::SetLanguageID**](iagentcharacterex--setlanguageid.md) before using the [**IAgentCharacter::Speak**](iagentcharacter--speak.md) method to ensure appropriate text display within the word balloon.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="66163-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="66163-120">See Also</span></span>

<span data-ttu-id="66163-121">[**Iagentballoon:: GetEnabled**](iagentballoon--getenabled.md), [**iagentballoonex:: SetStyle**](iagentballoonex--setstyle.md), [**iagentcharacter:: Speak**](iagentcharacter--speak.md)</span><span class="sxs-lookup"><span data-stu-id="66163-121">[**IAgentBalloon::GetEnabled**](iagentballoon--getenabled.md), [**IAgentBalloonEx::SetStyle**](iagentballoonex--setstyle.md), [**IAgentCharacter::Speak**](iagentcharacter--speak.md)</span></span>


 

 