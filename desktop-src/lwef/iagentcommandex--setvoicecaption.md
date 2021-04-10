---
title: Iagentcommandex setvoicecaption
description: Iagentcommandex setvoicecaption
ms.assetid: 672fdc13-25d3-4ced-b295-2b687767c17f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 358514dd33fc97a98f9b63107eabc98e0387bab8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038824"
---
# <a name="iagentcommandexsetvoicecaption"></a><span data-ttu-id="ca4d4-103">Iagentcommandex:: setvoicecaption</span><span class="sxs-lookup"><span data-stu-id="ca4d4-103">IAgentCommandEx::SetVoiceCaption</span></span>

<span data-ttu-id="ca4d4-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="ca4d4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

<span data-ttu-id="ca4d4-105">Legt den für einen [**Befehl**](/windows/desktop/lwef/the-command-object)angezeigten [**voicecaption**](voicecaption-property.md) -Text fest.</span><span class="sxs-lookup"><span data-stu-id="ca4d4-105">Sets the [**VoiceCaption**](voicecaption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="ca4d4-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="ca4d4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="ca4d4-107"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszvoicecaption*</span><span class="sxs-lookup"><span data-stu-id="ca4d4-107"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*</span></span>
</dt> <dd>

<span data-ttu-id="ca4d4-108">Ein BSTR, der den Text für die [**voicecaption**](voicecaption-property.md) -Eigenschaft für einen [**Befehl**](/windows/desktop/lwef/the-command-object)angibt.</span><span class="sxs-lookup"><span data-stu-id="ca4d4-108">A BSTR that specifies the text for the [**VoiceCaption**](voicecaption-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="ca4d4-109">Wenn Sie ein [**Command**](/windows/desktop/lwef/the-command-object) -Objekt in einer [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung definieren und seine [**Voice**](voice-property.md) -Eigenschaft festlegen, legen Sie in der Regel auch seine [**voicecaption**](voicecaption-property.md) -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="ca4d4-109">If you define a [**Command**](/windows/desktop/lwef/the-command-object) object in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection and set its [**Voice**](voice-property.md) property, you will typically also set its [**VoiceCaption**](voicecaption-property.md) property.</span></span> <span data-ttu-id="ca4d4-110">Dieser Text wird im Fenster "Sprachbefehle" angezeigt, wenn die Client Anwendung aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="ca4d4-110">This text will appear in the Voice Commands Window when your client application is input active.</span></span> <span data-ttu-id="ca4d4-111">Wenn diese Eigenschaft nicht festgelegt ist, bestimmt die-Einstellung für die [**Caption**](caption-property.md) -Eigenschaft den angezeigten Text.</span><span class="sxs-lookup"><span data-stu-id="ca4d4-111">If this property is not set, the setting for the [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="ca4d4-112">Wenn weder die **voicecaption** -Eigenschaft noch die-Eigenschaft festgelegt ist, wird der Befehl nicht im Fenster "Sprachbefehle" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ca4d4-112">When neither the **VoiceCaption** or property is set, the command does not appear in the Voice Commands Window.</span></span>

[<span data-ttu-id="ca4d4-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ca4d4-113">**Caption**</span></span>](caption-property.md)

## <a name="see-also"></a><span data-ttu-id="ca4d4-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ca4d4-114">See Also</span></span>

<span data-ttu-id="ca4d4-115">[**Iagentcommand:: getcaption**](iagentcommand--getcaption.md), [**iagentcommand:: SetEnabled**](iagentcommand--setenabled.md), [**iagentcommand:: setVisible**](iagentcommand--setvisible.md), [**iagentcommand:: setvoice**](iagentcommand--setvoice.md), [**iagentcommandsex:: Addex**](iagentcommandsex--addex.md), [**iagentcommandsex:: insertex**](iagentcommandsex--insertex.md), [**iagentcommands:: Add**](iagentcommands--add.md), [**iagentcommands:: Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="ca4d4-115">[**IAgentCommand::GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommandsEx::AddEx**](iagentcommandsex--addex.md), [**IAgentCommandsEx::InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 