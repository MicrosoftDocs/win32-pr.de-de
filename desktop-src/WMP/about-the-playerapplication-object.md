---
title: Informationen zum playerapplication-Objekt
description: Informationen zum playerapplication-Objekt
ms.assetid: 4b77bf16-d7e1-4119-91c2-46136db13e81
keywords:
- Windows Media Player, playerapplication-Objekt
- Windows Media Player-Objektmodell, playerapplication-Objekt
- Objektmodell, playerapplication-Objekt
- Windows Media Player ActiveX-Steuerelement, playerapplication-Objekt
- ActiveX-Steuerelement, playerapplication-Objekt
- Windows Media Player Mobile ActiveX-Steuerelement, playerapplication-Objekt
- Windows Media Player Mobile, playerapplication-Objekt
- Playerapplication-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d197614ba75a51bdc8ec5398ca757e410f918a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856596"
---
# <a name="about-the-playerapplication-object"></a><span data-ttu-id="1eebe-111">Informationen zum playerapplication-Objekt</span><span class="sxs-lookup"><span data-stu-id="1eebe-111">About the PlayerApplication Object</span></span>

<span data-ttu-id="1eebe-112">Das **playerapplication** -Objekt wird für Remoting-Windows-Media Player verwendet.</span><span class="sxs-lookup"><span data-stu-id="1eebe-112">The **PlayerApplication** object is used for remoting Windows Media Player.</span></span> <span data-ttu-id="1eebe-113">Es stellt die Funktionalität bereit, die erforderlich ist, um zwischen einem remoten Windows Media Player-Steuerelement und dem vollständigen Modus des Players zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="1eebe-113">It provides the functionality required to switch between a remoted Windows Media Player control and the full mode of the Player.</span></span>

<span data-ttu-id="1eebe-114">Mithilfe von Remoting kann ein Windows Media Player-Steuerelement, das in einer C++-Anwendung eingebettet ist, dieselbe Wiedergabe-Engine wie der Player verwenden.</span><span class="sxs-lookup"><span data-stu-id="1eebe-114">Remoting enables a Windows Media Player control embedded in a C++ application to use the same playback engine as the Player.</span></span> <span data-ttu-id="1eebe-115">Dies bedeutet normalerweise, dass Sie das **playerapplication** -Objekt in C++-Code verwenden, indem Sie die COM-Schnittstellen verwenden.</span><span class="sxs-lookup"><span data-stu-id="1eebe-115">This means that usually you will use the **PlayerApplication** object in C++ code using the COM interfaces.</span></span> <span data-ttu-id="1eebe-116">Es gibt jedoch einen Sonderfall, in dem Sie das Windows Media Player-Steuerelement einbetten können, das eine Windows Media Player Skin als Benutzeroberfläche anzeigt.</span><span class="sxs-lookup"><span data-stu-id="1eebe-116">There is a special case, however, where you can embed the Windows Media Player control that displays a Windows Media Player skin as its user interface.</span></span> <span data-ttu-id="1eebe-117">In diesem Fall kann **playerapplication** mithilfe von JScript im Skin-Code programmiert werden.</span><span class="sxs-lookup"><span data-stu-id="1eebe-117">In this case, **PlayerApplication** can be programmed using JScript in the skin code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1eebe-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1eebe-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1eebe-119">**Player-Objektmodell für Skriptsprachen**</span><span class="sxs-lookup"><span data-stu-id="1eebe-119">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> <dt>

[<span data-ttu-id="1eebe-120">**Playerapplication-Objekt**</span><span class="sxs-lookup"><span data-stu-id="1eebe-120">**PlayerApplication Object**</span></span>](playerapplication-object.md)
</dt> </dl>

 

 




