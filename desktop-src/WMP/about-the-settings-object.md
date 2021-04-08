---
title: Informationen zum Einstellungs Objekt
description: Informationen zum Einstellungs Objekt
ms.assetid: 941463e6-7928-438e-824e-e5e281421a4a
keywords:
- Windows Media Player, Einstellungs Objekt
- Windows Media Player-Objektmodell, Einstellungs Objekt
- Objektmodell, Einstellungs Objekt
- Windows Media Player ActiveX-Steuerelement, Einstellungs Objekt
- ActiveX-Steuerelement, Einstellungs Objekt
- Windows Media Player Mobile ActiveX-Steuerelement, Einstellungs Objekt
- Windows Media Player Mobile, Einstellungs Objekt
- Einstellungs Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b20dae51d42e6c67a59ddc23dca19bc7f4180001
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855568"
---
# <a name="about-the-settings-object"></a><span data-ttu-id="793e2-111">Informationen zum Einstellungs Objekt</span><span class="sxs-lookup"><span data-stu-id="793e2-111">About the Settings Object</span></span>

<span data-ttu-id="793e2-112">Das **Einstellungs** Objekt steuert die Einstellungen des Steuer Elements, z. b. Volume, Wiedergabe Anzahl, stumm Schaltung usw.</span><span class="sxs-lookup"><span data-stu-id="793e2-112">The **Settings** object governs the settings of the control such as volume, play count, mute, and so on.</span></span> <span data-ttu-id="793e2-113">Der Zugriff erfolgt nur über die **Settings** -Eigenschaft des **Player** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="793e2-113">It is accessed only through the **Settings** property of the **Player** object.</span></span> <span data-ttu-id="793e2-114">Die **Settings** -Eigenschaft gibt das **Settings** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="793e2-114">The **Settings** property returns the **Settings** object.</span></span> <span data-ttu-id="793e2-115">Sie können nur auf die Eigenschaften des **Einstellungs** Objekts zugreifen, nachdem Sie es erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="793e2-115">You can only access the properties of the **Settings** object after you have created it.</span></span> <span data-ttu-id="793e2-116">Um z. b. den Wert der **Volume** -Eigenschaft zu erhalten, müssen Sie den folgenden Code verwenden:</span><span class="sxs-lookup"><span data-stu-id="793e2-116">For example, to get the value of the **Volume** property, you must use the following code:</span></span>


```C++
myvolume = player.settings.volume;

```



## <a name="related-topics"></a><span data-ttu-id="793e2-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="793e2-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="793e2-118">**Player-Objektmodell für Skriptsprachen**</span><span class="sxs-lookup"><span data-stu-id="793e2-118">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> <dt>

[<span data-ttu-id="793e2-119">**Einstellungs Objekt**</span><span class="sxs-lookup"><span data-stu-id="793e2-119">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 




