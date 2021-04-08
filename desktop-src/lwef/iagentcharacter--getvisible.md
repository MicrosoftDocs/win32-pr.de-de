---
title: Iagentcharacter getVisible
description: Iagentcharacter getVisible
ms.assetid: 6e8e3a68-a7bb-4afb-a753-836fe82a0b24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0593b9b3a193b9d5910888b81b4ecba90469b1e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101486"
---
# <a name="iagentcharactergetvisible"></a><span data-ttu-id="63243-103">Iagentcharacter:: getVisible</span><span class="sxs-lookup"><span data-stu-id="63243-103">IAgentCharacter::GetVisible</span></span>

<span data-ttu-id="63243-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="63243-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for character Visible setting
);
```

<span data-ttu-id="63243-105">Bestimmt, ob der Animations Rahmen des Zeichens momentan sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="63243-105">Determines whether the character's animation frame is currently visible.</span></span>

-   <span data-ttu-id="63243-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="63243-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="63243-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbvisible*</span><span class="sxs-lookup"><span data-stu-id="63243-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="63243-108">Adresse einer Variablen, die **true** empfängt, wenn der Rahmen des Zeichens sichtbar ist, und **false** , wenn Sie ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="63243-108">Address of a variable that receives **True** if the character's frame is visible and **False** if hidden.</span></span>

</dd> </dl>

<span data-ttu-id="63243-109">Sie können diese Methode verwenden, um zu bestimmen, ob der Rahmen des Zeichens momentan sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="63243-109">You can use this method to determine whether the character's frame is currently visible.</span></span> <span data-ttu-id="63243-110">Verwenden Sie die [**Show**](/windows/desktop/lwef/iagentcharacter--show) -Methode, um ein Zeichen sichtbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="63243-110">To make a character visible, use the [**Show**](/windows/desktop/lwef/iagentcharacter--show) method.</span></span> <span data-ttu-id="63243-111">Um ein Zeichen auszublenden, verwenden Sie die [**Hide**](/windows/desktop/lwef/iagentcharacter--hide) -Methode.</span><span class="sxs-lookup"><span data-stu-id="63243-111">To hide a character, use the [**Hide**](/windows/desktop/lwef/iagentcharacter--hide) method.</span></span>

 

 