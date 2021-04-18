---
title: Erstellen eines Benutzeroberflächen-Plug-Ins für Windows Media Player 10 Mobile
description: Erstellen eines Benutzeroberflächen-Plug-Ins für Windows Media Player 10 Mobile
ms.assetid: 050418b7-d99c-49ab-8ce6-6511b194ffe6
keywords:
- Windows Media Player Mobile, Plug-ins
- Windows Media Player Mobile, Benutzerschnittstellen-Plug-ins
- Mobile Windows Media Player-Plug-ins
- Plug-ins, Benutzeroberfläche
- Plug-ins, Windows Media Player Mobile
- Plug-Ins für Benutzeroberflächen, Windows Media Player Mobile
- UI-Plug-ins, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d649ef1d8ed1b8fb1e1b54dc7eed106f798b1ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338997"
---
# <a name="creating-a-user-interface-plug-in-for-windows-media-player-10-mobile"></a><span data-ttu-id="cbc55-110">Erstellen eines Benutzeroberflächen-Plug-Ins für Windows Media Player 10 Mobile</span><span class="sxs-lookup"><span data-stu-id="cbc55-110">Creating a User Interface Plug-in for Windows Media Player 10 Mobile</span></span>

<span data-ttu-id="cbc55-111">Windows Media Player 10 Mobile verwendet das gleiche Benutzeroberflächen-Plug-in-Modell wie das Windows-Desktop Media Player.</span><span class="sxs-lookup"><span data-stu-id="cbc55-111">Windows Media Player 10 Mobile uses the same UI plug-in model as the desktop Windows Media Player.</span></span> <span data-ttu-id="cbc55-112">Windows Media Player 10 Mobile kann jedoch nur mit Plug-Ins für die Benutzeroberfläche von background interagieren. Aufgrund der ähnlichen Plug-in-Modelle gelten die gleichen API-Aufrufe, die für Plug-Ins für die Background-Benutzeroberfläche auf dem Desktop gelten, auch für Plug-ins der Background-Benutzeroberfläche auf einem Windows Mobile-Gerät.</span><span class="sxs-lookup"><span data-stu-id="cbc55-112">However, Windows Media Player 10 Mobile can only interact with background UI plug-ins. Because of the similar plug-in models, the same API calls that apply to background UI plug-ins on the desktop also apply to background UI plug-ins on a Windows Mobile device.</span></span>

<span data-ttu-id="cbc55-113">In den folgenden Abschnitten wird beschrieben, wie Sie ein Plug-in für die Background-Benutzeroberfläche mithilfe des vom Assistenten generierten Codes im Assistenten für Windows-Media Player-Plug-ins erstellen.</span><span class="sxs-lookup"><span data-stu-id="cbc55-113">The following sections describe how to create a background UI plug-in by using wizard-generated code from the Windows Media Player Plug-in Wizard.</span></span>



| <span data-ttu-id="cbc55-114">`Section`</span><span class="sxs-lookup"><span data-stu-id="cbc55-114">Section</span></span>                                                                | <span data-ttu-id="cbc55-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cbc55-115">Description</span></span>                                                                                                                                            |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbc55-116">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="cbc55-116">Getting Started</span></span>](getting-started.md)                                 | <span data-ttu-id="cbc55-117">Beschreibt, was Sie installieren müssen, und wie Sie den Windows Media Player-Plug-in-Assistenten verwenden, um die Erstellung eines Plug-Ins für die Benutzeroberfläche zu automatisieren.</span><span class="sxs-lookup"><span data-stu-id="cbc55-117">Describes what you need to install and how to use the Windows Media Player Plug-in Wizard to help automate the creation of a background UI plug-in.</span></span>    |
| [<span data-ttu-id="cbc55-118">Ändern des vom Assistenten generierten Codes</span><span class="sxs-lookup"><span data-stu-id="cbc55-118">Modifying Wizard-generated Code</span></span>](modifying-wizard-generated-code.md) | <span data-ttu-id="cbc55-119">Beschreibt, was Sie aus dem vom Assistenten generierten Code ändern müssen, der im vorherigen Abschnitt erstellt wurde, sodass er mit Windows Media Player 10 Mobile funktioniert.</span><span class="sxs-lookup"><span data-stu-id="cbc55-119">Describes what you need to modify from the wizard-generated code created in the previous section so that it works with Windows Media Player 10 Mobile.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="cbc55-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cbc55-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbc55-121">**Programmier Handbuch für Benutzeroberflächen-Plug-ins**</span><span class="sxs-lookup"><span data-stu-id="cbc55-121">**User Interface Plug-ins Programming Guide**</span></span>](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




