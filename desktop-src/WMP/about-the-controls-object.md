---
title: Informationen zum Steuerelement Objekt
description: Informationen zum Steuerelement Objekt
ms.assetid: 1678c931-af47-42c9-a8a5-b6b775aebda8
keywords:
- Windows Media Player, Steuerelemente-Objekt
- Objektmodell für Windows Media Player, Steuerelemente (Objekt)
- Objektmodell, Steuerelement Objekt
- Windows Media Player ActiveX-Steuerelement, Steuerelemente-Objekt
- ActiveX-Steuerelement, Steuerelement Objekt
- Windows Media Player Mobile ActiveX-Steuerelement, Steuerelemente Objekt
- Windows Media Player Mobile, Steuerelemente (Objekt)
- Controls-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f064ef65401876dedb4181ba788788f5e5d9676c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104387989"
---
# <a name="about-the-controls-object"></a><span data-ttu-id="93918-111">Informationen zum Steuerelement Objekt</span><span class="sxs-lookup"><span data-stu-id="93918-111">About the Controls Object</span></span>

<span data-ttu-id="93918-112">Das Steuer **Element Objekt steuert den Transport** von Inhalten digitaler Medien über das-Steuerelement mithilfe von Methoden wie wieder **Gabe** und **Beendigung**.</span><span class="sxs-lookup"><span data-stu-id="93918-112">The **Controls** object governs the transport of digital media content through the control by using methods such as **Play** and **Stop**.</span></span> <span data-ttu-id="93918-113">Der Zugriff erfolgt nur über die **Controls** -Eigenschaft des **Player** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="93918-113">It is accessed only through the **Controls** property of the **Player** object.</span></span> <span data-ttu-id="93918-114">Die **Controls** -Eigenschaft gibt das Steuer **Element Objekt zurück** .</span><span class="sxs-lookup"><span data-stu-id="93918-114">The **Controls** property returns the **Controls** object.</span></span> <span data-ttu-id="93918-115">Sie können nur auf die Eigenschaften des Steuer Elements "Steuer **Elemente** " zugreifen, nachdem Sie es erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="93918-115">You can only access the properties of the **Controls** object after you have created it.</span></span> <span data-ttu-id="93918-116">Wenn Sie z. b. die **Play** -Methode verwenden möchten, müssen Sie den folgenden Code verwenden:</span><span class="sxs-lookup"><span data-stu-id="93918-116">For example, to use the **Play** method, you must use the following code:</span></span>


```C++
player.controls.play();

```



## <a name="related-topics"></a><span data-ttu-id="93918-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="93918-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93918-118">**Controls-Objekt**</span><span class="sxs-lookup"><span data-stu-id="93918-118">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="93918-119">**Player-Objektmodell für Skriptsprachen**</span><span class="sxs-lookup"><span data-stu-id="93918-119">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




