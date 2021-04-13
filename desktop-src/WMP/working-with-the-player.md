---
title: Arbeiten mit dem Player
description: Arbeiten mit dem Player
ms.assetid: 27aff735-2142-4506-b9d0-2c0fbe60fd6b
keywords:
- Windows Media Player Skins, Player-Attribut in JScript
- Skins, Player-Attribut in JScript
- Attribute, Player
- Player-Attribut
- JScript-Dateien für Skins, Player-Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d47ea74b4c91f92ef33106e40e9896b98de6a34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388757"
---
# <a name="working-with-the-player"></a><span data-ttu-id="bb653-108">Arbeiten mit dem Player</span><span class="sxs-lookup"><span data-stu-id="bb653-108">Working with the Player</span></span>

<span data-ttu-id="bb653-109">Wenn Sie Microsoft JScript verwenden, um auf Methoden und Eigenschaften von Windows Media Player zuzugreifen, müssen Sie den Namen "Player" als Namen des Steuer Elements verwenden.</span><span class="sxs-lookup"><span data-stu-id="bb653-109">When using Microsoft JScript to access methods and properties of Windows Media Player, you must use the name "player" for the name of the control.</span></span> <span data-ttu-id="bb653-110">Wenn Sie z. b. auf die Methode zum Abbrechen verweisen möchten, müssen Sie Folgendes eingeben:</span><span class="sxs-lookup"><span data-stu-id="bb653-110">For example, to reference the Stop method, you must type:</span></span>


```C++
player.Controls.Stop()

```



<span data-ttu-id="bb653-111">Das globale Attribut " **Player** " ist der Schlüssel für den Zugriff auf das Windows Media Player-Steuerelement über die Design Skripterstellung</span><span class="sxs-lookup"><span data-stu-id="bb653-111">The **player** global attribute is the key to accessing the Windows Media Player control through skin scripting.</span></span> <span data-ttu-id="bb653-112">Über dieses Attribut werden alle Objekte des Windows Media Player-Steuer Elements für die Lauf Zeitänderung über ihre Eigenschaften und Methoden zugänglich.</span><span class="sxs-lookup"><span data-stu-id="bb653-112">Through this attribute, all the objects of the Windows Media Player control become accessible for run-time modification through their properties and methods.</span></span> <span data-ttu-id="bb653-113">Außerdem ist das **Player** -Element verfügbar, sodass Sie Ereignishandler und das **URL** -Attribut zur Entwurfszeit angeben können.</span><span class="sxs-lookup"><span data-stu-id="bb653-113">Additionally, the **PLAYER** element is available so that you can specify event handlers and the **url** attribute at design time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb653-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bb653-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb653-115">**Verwenden von JScript**</span><span class="sxs-lookup"><span data-stu-id="bb653-115">**Using JScript**</span></span>](using-jscript.md)
</dt> </dl>

 

 




