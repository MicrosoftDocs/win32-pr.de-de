---
title: Iagentcommandsex setvoicecaption
description: Iagentcommandsex setvoicecaption
ms.assetid: f13c9ca5-70c9-42d0-b53c-45dc8980a24c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19fcc0f3ce98ff0187b7ed2f01b7131cc8e101bd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106339269"
---
# <a name="iagentcommandsexsetvoicecaption"></a><span data-ttu-id="1e647-103">Iagentcommandsex:: setvoicecaption</span><span class="sxs-lookup"><span data-stu-id="1e647-103">IAgentCommandsEx::SetVoiceCaption</span></span>

<span data-ttu-id="1e647-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="1e647-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

<span data-ttu-id="1e647-105">Legt den für das [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt angezeigten [**voicecaption**](voicecaption-property.md) -Text fest.</span><span class="sxs-lookup"><span data-stu-id="1e647-105">Sets the [**VoiceCaption**](voicecaption-property.md) text displayed for the [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="1e647-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="1e647-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="1e647-107"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszvoicecaption*</span><span class="sxs-lookup"><span data-stu-id="1e647-107"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*</span></span>
</dt> <dd>

<span data-ttu-id="1e647-108">Ein BSTR, der den Text für die [**voicecaption**](voicecaption-property.md) -Eigenschaft für einen [**Befehl**](/windows/desktop/lwef/the-command-object)angibt.</span><span class="sxs-lookup"><span data-stu-id="1e647-108">A BSTR that specifies the text for the [**VoiceCaption**](voicecaption-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="1e647-109">Wenn Sie ein [**Command**](/windows/desktop/lwef/the-command-object) -Objekt in einer [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung definieren und seine [**Voice**](voice-property.md) -Eigenschaft festlegen, legen Sie in der Regel auch seine [**voicecaption**](voicecaption-property.md) -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="1e647-109">If you define a [**Command**](/windows/desktop/lwef/the-command-object) object in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection and set its [**Voice**](voice-property.md) property, you will typically also set its [**VoiceCaption**](voicecaption-property.md) property.</span></span> <span data-ttu-id="1e647-110">Dieser Text wird im Fenster "Sprachbefehle" angezeigt, wenn die Client Anwendung aktiv ist und das Zeichen sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="1e647-110">This text will appear in the Voice Commands Window when your client application is input-active and the character is visible.</span></span> <span data-ttu-id="1e647-111">Wenn diese Eigenschaft nicht festgelegt ist, bestimmt die-Einstellung für die [**Caption**](caption-property.md) -Eigenschaft den angezeigten Text.</span><span class="sxs-lookup"><span data-stu-id="1e647-111">If this property is not set, the setting for the [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="1e647-112">Wenn weder die **voicecaption** -Eigenschaft noch die **Caption** -Eigenschaft festgelegt ist, wird der Befehl nicht im Fenster "Sprachbefehle" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1e647-112">When neither the **VoiceCaption** or **Caption** property is set, the command does not appear in the Voice Commands Window.</span></span>

## <a name="see-also"></a><span data-ttu-id="1e647-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1e647-113">See Also</span></span>

[<span data-ttu-id="1e647-114">**Iagentcommandsex:: getvoicecaption**</span><span class="sxs-lookup"><span data-stu-id="1e647-114">**IAgentCommandsEx::GetVoiceCaption**</span></span>](iagentcommandsex--getvoicecaption.md)


 

 