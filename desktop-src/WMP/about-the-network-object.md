---
title: Informationen zum Netzwerk Objekt
description: Informationen zum Netzwerk Objekt
ms.assetid: 367a51d4-2db8-4c9e-82b7-85b2b631c721
keywords:
- Windows Media Player, Netzwerk Objekt
- Windows Media Player-Objektmodell, Netzwerk Objekt
- Objektmodell, Netzwerk Objekt
- Windows Media Player ActiveX-Steuerelement, Netzwerk Objekt
- ActiveX-Steuerelement, Netzwerk Objekt
- Windows Media Player Mobile ActiveX-Steuerelement, Netzwerk Objekt
- Windows Media Player Mobile, Netzwerk Objekt
- Netzwerk Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a1f3ff892a4d5b078956c9d126d0efaa844031d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707800"
---
# <a name="about-the-network-object"></a><span data-ttu-id="52752-111">Informationen zum Netzwerk Objekt</span><span class="sxs-lookup"><span data-stu-id="52752-111">About the Network Object</span></span>

<span data-ttu-id="52752-112">Das **Netzwerk** Objekt steuert die Eigenschaften, mit denen Sie bestimmen können, wie gut der Inhalt über das Netzwerk gestreamt wird.</span><span class="sxs-lookup"><span data-stu-id="52752-112">The **Network** object governs the properties that allow you to determine how well the content is streaming through the network.</span></span> <span data-ttu-id="52752-113">Beispielsweise können Sie herausfinden, ob Pakete verloren gehen, und die entsprechende Aktion durchführen.</span><span class="sxs-lookup"><span data-stu-id="52752-113">For example, you can find out whether packets are being lost and take appropriate action.</span></span> <span data-ttu-id="52752-114">Der Zugriff auf das **Netzwerk** Objekt erfolgt nur über die **Network** -Eigenschaft des **Player** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="52752-114">The **Network** object is accessed only through the **network** property of the **Player** object.</span></span> <span data-ttu-id="52752-115">Die **Network** -Eigenschaft gibt das **Netzwerk** Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="52752-115">The **network** property returns the **Network** object.</span></span> <span data-ttu-id="52752-116">Sie können nur auf die Eigenschaften des **Netzwerk** Objekts zugreifen, nachdem Sie es erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="52752-116">You can only access the properties of the **Network** object after you have created it.</span></span> <span data-ttu-id="52752-117">Wenn Sie z. b. die **Bandbreiten** Eigenschaft verwenden möchten, müssen Sie den folgenden Code verwenden:</span><span class="sxs-lookup"><span data-stu-id="52752-117">For example, to use the **Bandwidth** property, you must use the following code:</span></span>


```C++
mybandwidth = player.network.bandwidth;

```



## <a name="related-topics"></a><span data-ttu-id="52752-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="52752-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52752-119">**Netzwerk Objekt**</span><span class="sxs-lookup"><span data-stu-id="52752-119">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="52752-120">**Player-Objektmodell für Skriptsprachen**</span><span class="sxs-lookup"><span data-stu-id="52752-120">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




