---
title: Iagentcommandsex getvoicecaption
description: Iagentcommandsex getvoicecaption
ms.assetid: 0e505295-386a-421f-a43c-6da03c8a2b6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a757e1c841afd62b9b6ae13f1ef34178f133ca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337646"
---
# <a name="iagentcommandsexgetvoicecaption"></a><span data-ttu-id="6c0c2-103">Iagentcommandsex:: getvoicecaption</span><span class="sxs-lookup"><span data-stu-id="6c0c2-103">IAgentCommandsEx::GetVoiceCaption</span></span>

<span data-ttu-id="6c0c2-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="6c0c2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVoiceCaption(
   BSTR * pbszVoiceCaption  // address of command's voice caption
);
```

<span data-ttu-id="6c0c2-105">Ruft die [**voicecaption**](voicecaption-property.md) für ein [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="6c0c2-105">Retrieves the [**VoiceCaption**](voicecaption-property.md) for a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="6c0c2-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="6c0c2-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="6c0c2-107"><span id="pbszVoiceCaption"></span><span id="pbszvoicecaption"></span><span id="PBSZVOICECAPTION"></span>*pbszvoicecaption*</span><span class="sxs-lookup"><span data-stu-id="6c0c2-107"><span id="pbszVoiceCaption"></span><span id="pbszvoicecaption"></span><span id="PBSZVOICECAPTION"></span>*pbszVoiceCaption*</span></span>
</dt> <dd>

<span data-ttu-id="6c0c2-108">Die Adresse eines BSTR-Werts, der den Wert des [**Beschriftungs**](caption-property.md) Texts empfängt, der für einen [**Befehl**](/windows/desktop/lwef/the-command-object)angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6c0c2-108">The address of a BSTR that receives the value of the [**Caption**](caption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="6c0c2-109">Der zurückgegebene Text ist, der für das [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt festgelegt wird und im Fenster "Sprachbefehle" angezeigt wird, wenn die Client Anwendung aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="6c0c2-109">The text returned is that set for your [**Command**](/windows/desktop/lwef/the-command-object) object and appears in the Voice Commands window when your client application is input-active.</span></span>

<span data-ttu-id="6c0c2-110">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="6c0c2-110">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c0c2-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6c0c2-111">See Also</span></span>

[<span data-ttu-id="6c0c2-112">**Iagentcommandsex:: setvoicecaption**</span><span class="sxs-lookup"><span data-stu-id="6c0c2-112">**IAgentCommandsEx::SetVoiceCaption**</span></span>](iagentcommandsex--setvoicecaption.md)


 

 