---
title: Auswählen der Funktionen
description: Auswählen der Funktionen
ms.assetid: ded3c578-5087-4e4f-bf21-2149cf72719d
keywords:
- Windows Media Player Mobile Skins, Funktionen für Audiodaten
- Skins, Funktionen für Audiodaten
- Erstellen von Skins, Funktionen für Audiodaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a139dc21a7d10847a7920955988ec2b02fced0f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388662"
---
# <a name="choosing-the-functions"></a><span data-ttu-id="70cbd-106">Auswählen der Funktionen</span><span class="sxs-lookup"><span data-stu-id="70cbd-106">Choosing the Functions</span></span>

<span data-ttu-id="70cbd-107">Der Zweck dieser Skin besteht darin, grundlegende Funktionen für die Wiedergabe von Audiodaten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="70cbd-107">The purpose of this skin is to provide basic functionality for playing audio.</span></span> <span data-ttu-id="70cbd-108">Die folgenden Funktionen werden verwendet:</span><span class="sxs-lookup"><span data-stu-id="70cbd-108">The following functions will be used:</span></span>



| <span data-ttu-id="70cbd-109">Funktion</span><span class="sxs-lookup"><span data-stu-id="70cbd-109">Function</span></span>                     | <span data-ttu-id="70cbd-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="70cbd-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70cbd-111">PLAYPAUSE oder playpausestoppt\*</span><span class="sxs-lookup"><span data-stu-id="70cbd-111">PlayPause or PlayPauseStop\*</span></span> | <span data-ttu-id="70cbd-112">Das Starten des Medien Elements ist von höchster Wichtigkeit.</span><span class="sxs-lookup"><span data-stu-id="70cbd-112">Starting the media item is of prime importance.</span></span> <span data-ttu-id="70cbd-113">Wenn Sie ein Skin für Windows Media Player 10 Mobile oder höher erstellen, sollten Sie playpaust-Stopps verwenden.</span><span class="sxs-lookup"><span data-stu-id="70cbd-113">If you are creating a skin for Windows Media Player 10 Mobile or later, then you should use PlayPauseStop.</span></span> <span data-ttu-id="70cbd-114">Wenn Sie mit einer früheren Version von Windows Media Player Mobile arbeiten, müssen Sie PLAYPAUSE verwenden.</span><span class="sxs-lookup"><span data-stu-id="70cbd-114">If you are working with an earlier version of Windows Media Player Mobile, then you must use PlayPause.</span></span> <span data-ttu-id="70cbd-115">Beide Funktionen geben Ihnen die zusätzlichen Funktionen, die angehalten werden, aber nur playpausestoppt ermöglicht es Ihnen, eine Liveübertragung zu beenden, wenn keine Pause-Funktionalität verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="70cbd-115">Both functions give you the added functionality of pausing, but only PlayPauseStop allows you to stop a live broadcast when pause functionality is not available.</span></span> |
| <span data-ttu-id="70cbd-116">Stop</span><span class="sxs-lookup"><span data-stu-id="70cbd-116">Stop</span></span>                         | <span data-ttu-id="70cbd-117">Sie möchten "Ende" hinzufügen, um die Wiedergabe des Elements zu unterbinden.</span><span class="sxs-lookup"><span data-stu-id="70cbd-117">You will want to add Stop to stop playing the item.</span></span> <span data-ttu-id="70cbd-118">Wenn Sie ein Skin für Windows Media Player 10 Mobile oder höher erstellen, bietet die Funktion "playpausstoppt" diese Funktionalität bereits.</span><span class="sxs-lookup"><span data-stu-id="70cbd-118">If you are creating a skin for Windows Media Player 10 Mobile or later, the PlayPauseStop function already provides this functionality.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="70cbd-119">Nächste</span><span class="sxs-lookup"><span data-stu-id="70cbd-119">Next</span></span>                         | <span data-ttu-id="70cbd-120">Wenn Sie über eine Wiedergabeliste verfügen, sollten Sie in der Lage sein, das nächste Element auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="70cbd-120">If you have a playlist, you will want to be able to choose the next item.</span></span> <span data-ttu-id="70cbd-121">Dies ist für die grundlegende Navigation digitaler Medien erforderlich.</span><span class="sxs-lookup"><span data-stu-id="70cbd-121">You need this for basic navigation of digital media.</span></span>                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="70cbd-122">Prev (Vorheriger)</span><span class="sxs-lookup"><span data-stu-id="70cbd-122">Prev</span></span>                         | <span data-ttu-id="70cbd-123">Obwohl Sie neben dem Anfang die Wiedergabeliste durchlaufen könnten, können Sie mit dem Hinzufügen von Prev ganz einfach rückwärts und vorwärts navigieren, wenn Sie in der Wiedergabeliste navigieren.</span><span class="sxs-lookup"><span data-stu-id="70cbd-123">While you could use Next to cycle through the playlist until you came to the beginning, adding Prev will make it easy for the user to go backward as well as forward when navigating the playlist.</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="70cbd-124">Volumeup oder volumedown\*</span><span class="sxs-lookup"><span data-stu-id="70cbd-124">VolumeUp or VolumeDown\*</span></span>     | <span data-ttu-id="70cbd-125">Sie sollten dem Benutzer die Möglichkeit geben, das Volume zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="70cbd-125">You will want to provide the user with the ability to turn the volume up or down.</span></span>                                                                                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="70cbd-126">\*Verfügbar für Windows Media Player 10 Mobile oder höher.</span><span class="sxs-lookup"><span data-stu-id="70cbd-126">\*Available for Windows Media Player 10 Mobile or later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="70cbd-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="70cbd-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70cbd-128">**Skin Guide**</span><span class="sxs-lookup"><span data-stu-id="70cbd-128">**Skin Guide**</span></span>](skin-guide.md)
</dt> </dl>

 

 




