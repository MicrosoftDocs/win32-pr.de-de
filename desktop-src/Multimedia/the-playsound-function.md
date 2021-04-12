---
title: Die PlaySound-Funktion
description: Die PlaySound-Funktion
ms.assetid: ce405a13-c4ab-4c9a-bcfe-8d4427b3d2d8
keywords:
- Multimedia-Audio, PlaySound-Funktion
- Audio, PlaySound-Funktion
- Wellenform-Audio, PlaySound-Funktion
- PlaySound-Funktion, Informationen zu
- SndPlaySound-Funktion
- PlaySound-Funktion im Vergleich zur SndPlaySound-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5723b1937c974e6c622c1f2010e8d2129e787cdd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104208866"
---
# <a name="the-playsound-function"></a><span data-ttu-id="45d08-109">Die PlaySound-Funktion</span><span class="sxs-lookup"><span data-stu-id="45d08-109">The PlaySound Function</span></span>

<span data-ttu-id="45d08-110">Sie können die [**PlaySound**](/previous-versions//dd743680(v=vs.85)) -Funktion verwenden, um Wellenform-Audio wiederzugeben, wenn der Sound in den verfügbaren Arbeitsspeicher passt.</span><span class="sxs-lookup"><span data-stu-id="45d08-110">You can use the [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function to play waveform audio if the sound fits into available memory.</span></span> <span data-ttu-id="45d08-111">(Die Funktion [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) bietet eine Teilmenge der Funktionen von PlaySound.</span><span class="sxs-lookup"><span data-stu-id="45d08-111">(The [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) function offers a subset of the capabilities of PlaySound.</span></span> <span data-ttu-id="45d08-112">Verwenden Sie " **PlaySound**", nicht " **sndPlaySound**", um die Portabilität Ihrer Win32-basierten Anwendung zu maximieren.)</span><span class="sxs-lookup"><span data-stu-id="45d08-112">To maximize the portability of your Win32-based application, use **PlaySound**, not **sndPlaySound**.)</span></span>

<span data-ttu-id="45d08-113">Mit der Funktion " **PlaySound** " können Sie einen Sound auf eine von drei Arten angeben:</span><span class="sxs-lookup"><span data-stu-id="45d08-113">The **PlaySound** function allows you to specify a sound in one of three ways:</span></span>

-   <span data-ttu-id="45d08-114">Als Systemwarnung mit dem Alias, der in der WIN.INI-Datei oder der Registrierung gespeichert ist</span><span class="sxs-lookup"><span data-stu-id="45d08-114">As a system alert, using the alias stored in the WIN.INI file or the registry</span></span>
-   <span data-ttu-id="45d08-115">Als Dateiname</span><span class="sxs-lookup"><span data-stu-id="45d08-115">As a filename</span></span>
-   <span data-ttu-id="45d08-116">Als Ressourcen Bezeichner</span><span class="sxs-lookup"><span data-stu-id="45d08-116">As a resource identifier</span></span>

<span data-ttu-id="45d08-117">Mit der Funktion " [**PlaySound**](/previous-versions//dd743680(v=vs.85)) " können Sie einen Sound in einer kontinuierlichen Schleife wiedergeben. Dies wird nur beendet, wenn Sie " **PlaySound** " erneut aufrufen, indem Sie entweder **null** oder den Sound Bezeichner eines anderen Sounds für den *pszsound* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="45d08-117">The [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function allows you to play a sound in a continuous loop, ending only when you call **PlaySound** again, specifying either **NULL** or the sound identifier of another sound for the *pszSound* parameter.</span></span>

<span data-ttu-id="45d08-118">Mit **PlaySound** können Sie den Sound synchron oder asynchron abspielen und das Verhalten der Funktion auf andere Weise steuern, wenn Sie Systemressourcen freigeben muss.</span><span class="sxs-lookup"><span data-stu-id="45d08-118">You can use **PlaySound** to play the sound synchronously or asynchronously, and to control the behavior of the function in other ways when it must share system resources.</span></span>

<span data-ttu-id="45d08-119">Weitere Informationen zur Verwendung von PlaySound finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="45d08-119">For more information about using PlaySound, see the following topics:</span></span>

-   [<span data-ttu-id="45d08-120">Verwenden von PlaySound zum Abspielen von Waveform-Audio Dateien</span><span class="sxs-lookup"><span data-stu-id="45d08-120">Using PlaySound to Play Waveform-Audio Files</span></span>](using-playsound-to-play-waveform-audio-files.md)
-   [<span data-ttu-id="45d08-121">Verwenden von PlaySound für Schleifen Klänge</span><span class="sxs-lookup"><span data-stu-id="45d08-121">Using PlaySound to Loop Sounds</span></span>](using-playsound-to-loop-sounds.md)
-   [<span data-ttu-id="45d08-122">Verwenden von PlaySound zum Abspielen von System Sounds</span><span class="sxs-lookup"><span data-stu-id="45d08-122">Using PlaySound to Play System Sounds</span></span>](using-playsound-to-play-system-sounds.md)

<span data-ttu-id="45d08-123">Weitere Beispiele für die Verwendung von **PlaySound** in ihren Win32-basierten Anwendungen finden Sie unter [spielen von Wave-Ressourcen](playing-wave-resources.md).</span><span class="sxs-lookup"><span data-stu-id="45d08-123">For more examples of how to use **PlaySound** in your Win32-based applications, see [Playing WAVE Resources](playing-wave-resources.md).</span></span>

 

 