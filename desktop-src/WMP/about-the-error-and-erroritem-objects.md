---
title: Informationen zu den Fehlern und ErrorItem-Objekten
description: Informationen zu den Fehlern und ErrorItem-Objekten
ms.assetid: 187f6835-3101-45db-87bd-930d222165ce
keywords:
- Windows Media Player, Fehler Objekt
- Windows Media Player-Objektmodell, Fehler Objekt
- Objektmodell, Fehler Objekt
- Windows Media Player ActiveX-Steuerelement, Error-Objekt
- ActiveX-Steuerelement, Error-Objekt
- Windows Media Player Mobile ActiveX-Steuerelement, Error-Objekt
- Windows Media Player Mobile, Fehler Objekt
- Error-Objekt
- Windows Media Player, ErrorItem-Objekt
- Windows Media Player-Objektmodell, ErrorItem-Objekt
- Objektmodell, ErrorItem-Objekt
- Windows Media Player ActiveX-Steuerelement, ErrorItem-Objekt
- ActiveX-Steuerelement, ErrorItem-Objekt
- Windows Media Player Mobile ActiveX-Steuerelement, ErrorItem-Objekt
- Windows Media Player Mobile, ErrorItem-Objekt
- ErrorItem-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23064670f13229aca84ae6dc86cf27cf34abbc56
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310260"
---
# <a name="about-the-error-and-erroritem-objects"></a><span data-ttu-id="caf58-119">Informationen zu den Fehlern und ErrorItem-Objekten</span><span class="sxs-lookup"><span data-stu-id="caf58-119">About the Error and ErrorItem Objects</span></span>

<span data-ttu-id="caf58-120">Die **Fehler-und** **ErrorItem** -Objekte steuern die Fehler Behandlungs Funktionen von Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="caf58-120">The **Error** and **ErrorItem** objects govern the error-handling capabilities of Windows Media Player.</span></span> <span data-ttu-id="caf58-121">Das **Error** -Objekt wird durch die **Error** -Eigenschaft aus dem **Player** -Objekt abgerufen.</span><span class="sxs-lookup"><span data-stu-id="caf58-121">The **Error** object is obtained from the **Player** object through the **error** property.</span></span> <span data-ttu-id="caf58-122">Sie können einen bestimmten Code aus dem **Error** -Objekt mit der **Item** -Eigenschaft des **Error** -Objekts erhalten, um das **ErrorItem** -Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="caf58-122">You can get a specific code from the **Error** object by using the **item** property of the **Error** object to create the **ErrorItem** object.</span></span> <span data-ttu-id="caf58-123">Um z. b. den Fehlercode des ersten Fehler Elements zu erhalten, geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="caf58-123">For example, to get the error code of the first error item, type:</span></span>


```C++
myerrorcode = player.error.item(0).errorCode;

```



<span data-ttu-id="caf58-124">Mithilfe des folgenden Codes können Sie auch die Webhilfe für das **Fehler** Objekt aufrufen:</span><span class="sxs-lookup"><span data-stu-id="caf58-124">You can also invoke Web Help with the **Error** object by using the following code:</span></span>


```C++
player.error.webHelp();

```



## <a name="related-topics"></a><span data-ttu-id="caf58-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="caf58-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="caf58-126">**Error-Objekt**</span><span class="sxs-lookup"><span data-stu-id="caf58-126">**Error Object**</span></span>](error-object.md)
</dt> <dt>

[<span data-ttu-id="caf58-127">**ErrorItem-Objekt**</span><span class="sxs-lookup"><span data-stu-id="caf58-127">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> <dt>

[<span data-ttu-id="caf58-128">**Player-Objektmodell für Skriptsprachen**</span><span class="sxs-lookup"><span data-stu-id="caf58-128">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




