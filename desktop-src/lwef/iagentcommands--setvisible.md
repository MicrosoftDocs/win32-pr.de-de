---
title: Iagentcommands setVisible
description: Iagentcommands setVisible
ms.assetid: 4b99989a-29bb-4e0e-8155-cf734cc667fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a4bdb3c1a7f1e11c9548eb1e1af415d0f5d18f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106338252"
---
# <a name="iagentcommandssetvisible"></a><span data-ttu-id="3c97a-103">Iagentcommands:: setVisible</span><span class="sxs-lookup"><span data-stu-id="3c97a-103">IAgentCommands::SetVisible</span></span>

<span data-ttu-id="3c97a-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="3c97a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVisible(
   long bVisible  // the Visible setting for Commands collection
);
```

<span data-ttu-id="3c97a-105">Legt den Wert der [**Visible**](visible-property.md) -Eigenschaft für eine [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung fest.</span><span class="sxs-lookup"><span data-stu-id="3c97a-105">Sets the value of the [**Visible**](visible-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="3c97a-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="3c97a-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="3c97a-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bvisible*</span><span class="sxs-lookup"><span data-stu-id="3c97a-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="3c97a-108">Ein boolescher Wert, der die [**sichtbare**](visible-property.md) Eigenschaft einer [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung bestimmt.</span><span class="sxs-lookup"><span data-stu-id="3c97a-108">A Boolean value that determines the [**Visible**](visible-property.md) property of a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="3c97a-109">**True** legt fest, dass die [**Beschriftung**](caption-property.md) der **Befehle** Auflistung sichtbar ist, wenn das Popupmenü des Zeichens angezeigt wird. *False* zeigt ihn nicht an.</span><span class="sxs-lookup"><span data-stu-id="3c97a-109">**True** sets the **Commands** collection's [**Caption**](caption-property.md) to be visible when the character's pop-up menu is displayed; *False* does not display it.</span></span>

</dd> </dl>

<span data-ttu-id="3c97a-110">Für eine [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung muss die [**Caption**](caption-property.md) -Eigenschaft festgelegt sein und deren [**Visible**](visible-property.md) -Eigenschaft auf **true** festgelegt sein, damit Sie im Popupmenü des Zeichens angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3c97a-110">A [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection must have its [**Caption**](caption-property.md) property set and its [**Visible**](visible-property.md) property set to **True** to appear on the character's pop-up menu.</span></span> <span data-ttu-id="3c97a-111">Die **Visible** -Eigenschaft muss auch auf **true** festgelegt werden, damit Befehle in der Auflistung angezeigt werden, wenn die Client Anwendung aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="3c97a-111">The **Visible** property must also be set to **True** for commands in the collection to appear when your client application is input-active.</span></span>

## <a name="see-also"></a><span data-ttu-id="3c97a-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3c97a-112">See Also</span></span>

<span data-ttu-id="3c97a-113">[**Iagentcommands:: getVisible**](iagentcommands--getvisible.md), [ **iagentcommand:: setCaption**](iagentcommand--setcaption.md)</span><span class="sxs-lookup"><span data-stu-id="3c97a-113">[**IAgentCommands::GetVisible**](iagentcommands--getvisible.md), [**IAgentCommand::SetCaption**](iagentcommand--setcaption.md)</span></span>


 

 