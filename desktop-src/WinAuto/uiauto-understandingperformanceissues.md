---
title: Grundlegendes zu Leistungsproblemen
description: In diesem Thema werden Leistungsprobleme im Zusammenhang mit Text-und TextRange-Steuerelement Mustern beschrieben.
ms.assetid: D78BFFA8-E303-441D-9D32-AD22E1B1A249
keywords:
- Clients, Grundlegendes zu Leistungsproblemen
- Clients, textbasierte Steuerelemente
- Clients, Textbereiche
- Clients, Text-Steuerelement Muster
- Clients, TextRange-Steuerelement Muster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d8d9b9b6c5cb0ef3ed34c6960e5aeafa623068
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316826"
---
# <a name="understanding-performance-issues"></a><span data-ttu-id="4babc-108">Grundlegendes zu Leistungsproblemen</span><span class="sxs-lookup"><span data-stu-id="4babc-108">Understanding Performance Issues</span></span>

<span data-ttu-id="4babc-109">In diesem Thema werden Leistungsprobleme im Zusammenhang mit [Text-und TextRange-](uiauto-implementingtextandtextrange.md) Steuerelement Mustern beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4babc-109">This topic describes performance issues associated with using the [Text and TextRange](uiauto-implementingtextandtextrange.md) control patterns.</span></span>


<span data-ttu-id="4babc-110">Die [**iuiautomationtextpattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) -Schnittstelle und die [**iuiautomationtextrange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) -Schnittstelle basieren auf prozessübergreifenden aufrufen – Sie bieten keinen Cachingmechanismus, um die Leistung beim Abrufen oder Verarbeiten von Textinhalten zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="4babc-110">The [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) and [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) interfaces rely on cross-process calls—they do not provide a caching mechanism to improve performance when retrieving or processing textual content.</span></span>

<span data-ttu-id="4babc-111">Eine Client Anwendung kann die Leistung verbessern, indem die [**iuiautomationtextrange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) -Methode verwendet wird, um Textblöcke mit mittlerer Größe abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4babc-111">A client application can improve performance by using the [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) method to retrieve moderately sized blocks of text.</span></span> <span data-ttu-id="4babc-112">Wenn Sie z. b. **gettext** zum Abrufen von einzelnen Zeichen verwenden, wird für jedes Zeichen eine prozessübergreifende Leistungs Einbuße ausgelöst, während beim Aufrufen von **gettext** keine maximale Länge angegeben wird. Dies kann je nach Größe des Text Bereichs eine hohe Latenz verursachen.</span><span class="sxs-lookup"><span data-stu-id="4babc-112">For example, using **GetText** to retrieve single characters will incur a cross-process performance hit for each character, whereas not specifying a maximum length when calling **GetText** will incur one cross-process hit, but can have high latency depending on the size of the text range.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4babc-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4babc-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4babc-114">Text-und TextRange-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="4babc-114">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[<span data-ttu-id="4babc-115">Benutzeroberflächenautomatisierungs-Unterstützung für Textinhalte</span><span class="sxs-lookup"><span data-stu-id="4babc-115">UI Automation Support for Textual Content</span></span>](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[<span data-ttu-id="4babc-116">Arbeiten mit Text basierten Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="4babc-116">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




