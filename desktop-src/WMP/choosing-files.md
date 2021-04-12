---
title: Auswählen von Dateien
description: Auswählen von Dateien
ms.assetid: dfa44a32-7d72-47f7-a872-33b823a34798
keywords:
- Erstellen von Skins, auswählen von Dateien
- Windows Media Player Skins, auswählen von Dateien
- Skins, auswählen von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0098a37635c52ba3e48fb77f07a5868ceb957239
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207205"
---
# <a name="choosing-files"></a><span data-ttu-id="da695-106">Auswählen von Dateien</span><span class="sxs-lookup"><span data-stu-id="da695-106">Choosing Files</span></span>

<span data-ttu-id="da695-107">Wenn Sie eine Datei auswählen möchten, können Sie Code verwenden, der dem Beispiel für die Wiedergabeliste ähnelt, aber Folgendes für den Abschnitt "playelement" ersetzen:</span><span class="sxs-lookup"><span data-stu-id="da695-107">If you want to choose a file, you can use code similar to the Playlist example, but substitute the following for the PLAYELEMENT section:</span></span>


```C++
<PLAYELEMENT
  mappingColor = "#00FF00"
  onClick = "JScript:player.URL=theme.openDialog('FILE_OPEN','FILES_ALL');"
  />

```



<span data-ttu-id="da695-108">In dieser Zeile wird die **OpenDialog** -Methode von **Theme** verwendet, um eine **URL** für den Player zu definieren.</span><span class="sxs-lookup"><span data-stu-id="da695-108">This line will use the **openDialog** method of **THEME** to define a **URL** for the player.</span></span> <span data-ttu-id="da695-109">Sie können dies verwenden, um Dateien auszuwählen, die nicht in Wiedergabelisten vorliegen.</span><span class="sxs-lookup"><span data-stu-id="da695-109">You can use this to choose files that are not in playlists.</span></span>

<span data-ttu-id="da695-110">Ein ähnliches Funktions **offenes OpenDialog** -Beispiel finden Sie im Beispiel Abschnitt des SDK.</span><span class="sxs-lookup"><span data-stu-id="da695-110">You can see a similar working **openDialog** example in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da695-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="da695-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da695-112">**Leitfaden zum Erstellen von Skin**</span><span class="sxs-lookup"><span data-stu-id="da695-112">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




