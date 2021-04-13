---
title: Iagentcommands setCaption
description: Iagentcommands setCaption
ms.assetid: 042f7366-0071-40a5-a47c-81c02cdbe3a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8c472bfbfd82235e21c28e24e7e0ce03223ff8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390177"
---
# <a name="iagentcommandssetcaption"></a><span data-ttu-id="0341c-103">Iagentcommands:: setCaption</span><span class="sxs-lookup"><span data-stu-id="0341c-103">IAgentCommands::SetCaption</span></span>

<span data-ttu-id="0341c-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="0341c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetCaption(
   BSTR bszCaption  // Caption setting for Commands collection
);
```

<span data-ttu-id="0341c-105">Legt den [**Beschriftungs**](caption-property.md) Text fest, der für eine [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0341c-105">Sets the [**Caption**](caption-property.md) text displayed for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="0341c-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="0341c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0341c-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszcaption*</span><span class="sxs-lookup"><span data-stu-id="0341c-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span></span>
</dt> <dd>

<span data-ttu-id="0341c-108">Ein BSTR, der den Wert für die [**Caption**](caption-property.md) -Eigenschaft für eine [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung angibt.</span><span class="sxs-lookup"><span data-stu-id="0341c-108">A BSTR that specifies the value for the [**Caption**](caption-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

<span data-ttu-id="0341c-109">Wenn Sie die [**Caption**](caption-property.md) -Eigenschaft für eine [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung festlegen, wird definiert, wie diese im Popup Menü des Zeichens angezeigt wird, wenn die [**sichtbare**](visible-property.md) Eigenschaft auf **true** festgelegt ist und die Anwendung nicht der Input-Active-Client ist.</span><span class="sxs-lookup"><span data-stu-id="0341c-109">Setting the [**Caption**](caption-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection defines how it will appear on the character's pop-up menu when its [**Visible**](visible-property.md) property is set to **True** and your application is not the input-active client.</span></span> <span data-ttu-id="0341c-110">Um einen Zugriffsschlüssel (unline-mnetmonic) für Ihre **Beschriftung** anzugeben, fügen Sie vor diesem Zeichen ein kaufmännisches und-Zeichen (&) ein.</span><span class="sxs-lookup"><span data-stu-id="0341c-110">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="0341c-111">Wenn Sie Befehle für eine [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung definieren, deren [**Beschriftung**](caption-property.md) festgelegt ist, definieren Sie in der Regel auch eine **Beschriftung** für die zugehörige **Commands** -Auflistung.</span><span class="sxs-lookup"><span data-stu-id="0341c-111">If you define commands for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection that has its [**Caption**](caption-property.md) set, you typically also define a **Caption** for its **Commands** collection.</span></span>

## <a name="see-also"></a><span data-ttu-id="0341c-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0341c-112">See Also</span></span>

<span data-ttu-id="0341c-113">[**Iagentcommands:: getcaption**](iagentcommands--getcaption.md), [**iagentcommands:: setVisible**](iagentcommands--setvisible.md), [**iagentcommands:: setvoice**](iagentcommands--setvoice.md)</span><span class="sxs-lookup"><span data-stu-id="0341c-113">[**IAgentCommands::GetCaption**](iagentcommands--getcaption.md), [**IAgentCommands::SetVisible**](iagentcommands--setvisible.md), [**IAgentCommands::SetVoice**](iagentcommands--setvoice.md)</span></span>


 

 