---
title: Debuggen von Code
description: Debuggen von Code
ms.assetid: 315bc692-86bc-481e-abe4-f35309807a58
keywords:
- Windows Media Player Skins, Debuggen von Code
- Skins, Debuggen von Code
- Debuggen von Code für Skins
- Windows Media Player Skins, Protokollierung
- Skins, Protokollierung
- Protokollierungs Funktionalität in Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77e2305020b945d90adc1a47387ab2a13a3536e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311056"
---
# <a name="debugging-code"></a><span data-ttu-id="af759-109">Debuggen von Code</span><span class="sxs-lookup"><span data-stu-id="af759-109">Debugging Code</span></span>

<span data-ttu-id="af759-110">Häufig möchten Sie sehen, was in der Skin passiert.</span><span class="sxs-lookup"><span data-stu-id="af759-110">You often will want to see what is happening inside your skin.</span></span> <span data-ttu-id="af759-111">Hierfür können Sie ein Text Steuerelement oder eine Protokolldatei verwenden.</span><span class="sxs-lookup"><span data-stu-id="af759-111">You can do this through a text control or through a log file.</span></span>

<span data-ttu-id="af759-112">Sie können ein **Text** Element erstellen und es temporär in einem Teil der Skin platzieren.</span><span class="sxs-lookup"><span data-stu-id="af759-112">You can create a **TEXT** element and place it on a part of your skin temporarily.</span></span> <span data-ttu-id="af759-113">Beispielsweise können Sie den folgenden Code verwenden, um das **Text** -Element zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="af759-113">For example, you could use the following code to create your **TEXT** element:</span></span>


```C++
<!-- debugging control -- remove later -->        
<TEXT
    id = "debug"
    foregroundColor = "white"
    backgroundColor = "black"
    value = "debug"
    top = "100"
    left = "50"
    height = "15"
    width = "100" 
    z-order = "5" />
<!-- end debugging control -->
```



<span data-ttu-id="af759-114">Wenn Sie z. b. die aktuelle Position des Inhalts digitaler Medien in Windows Media Player anzeigen möchten, können Sie Code wie den folgenden verwenden, um die aktuelle Position im Textfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="af759-114">Then, for example, if you want to see the current position of the digital media content in Windows Media Player, you could use code similar to the following to display the current position in the text box.</span></span>


```C++
<PLAYER
    id = "myplayer">
    <CONTROLS
        id = "mycontrols"
        currentPosition_onchange="value=player.controls.currentPosition"/>
</PLAYER>

```



## <a name="to-write-debugging-information-to-a-log-file"></a><span data-ttu-id="af759-115">So schreiben Sie Debuginformationen in eine Protokolldatei</span><span class="sxs-lookup"><span data-stu-id="af759-115">To Write Debugging Information to a Log File</span></span>

<span data-ttu-id="af759-116">Um das Debuggen zu aktivieren oder zu deaktivieren, ändern Sie den Wert des folgenden Registrierungsschlüssels:</span><span class="sxs-lookup"><span data-stu-id="af759-116">To enable or disable debugging, change the value of the following registry key:</span></span>

<span data-ttu-id="af759-117">**HKEY \_ Current \_ User \\ Software \\ Microsoft \\ Media Player \\ Preferences \\ scriptdebugging**</span><span class="sxs-lookup"><span data-stu-id="af759-117">**HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\MediaPlayer\\Preferences\\ScriptDebugging**</span></span>

<span data-ttu-id="af759-118">Wenn Sie den Wert auf 1 festlegen, wird die Protokollierung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="af759-118">When you set the value to 1, logging is enabled.</span></span> <span data-ttu-id="af759-119">Wenn Sie den Wert auf 0 (Standardeinstellung) festlegen, wird die Protokollierung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="af759-119">When you set the value to 0 (the default), logging is disabled.</span></span>

<span data-ttu-id="af759-120">Wenn die Protokollierung aktiviert ist, wird eine Datei auf dem Computer des Benutzers in demselben Ordner wie die-Skin abgelegt.</span><span class="sxs-lookup"><span data-stu-id="af759-120">If logging is enabled, a file will be placed on the user's computer in the same folder as the skin.</span></span> <span data-ttu-id="af759-121">Die Datei erhält den Namen "*filename* \_ 0 \_log.txt", wobei *filename* für den Namen der Skin-Datei steht.</span><span class="sxs-lookup"><span data-stu-id="af759-121">The file will be named "*filename*\_0\_log.txt", where *filename* is the name of the skin file.</span></span> <span data-ttu-id="af759-122">Mit dem-Design kann der Code in der Skin Text in diese Datei *schreiben.* **logstring** -Methode.</span><span class="sxs-lookup"><span data-stu-id="af759-122">The code in your skin can write text to this file by using the *Theme*.**logString** method.</span></span> <span data-ttu-id="af759-123">Dies kann hilfreich sein, wenn Sie bestimmen möchten, was innerhalb Ihres Codes passiert, während er ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="af759-123">This can be useful if you want to determine what is going on inside your code while it is running.</span></span> <span data-ttu-id="af759-124">Beachten Sie, dass die Textdatei mit Unicode-Zeichen codiert ist.</span><span class="sxs-lookup"><span data-stu-id="af759-124">Note that the text file is encoded with Unicode characters.</span></span>

<span data-ttu-id="af759-125">Wenn die Protokollierung aktiviert ist und Sie ein Entwicklungssystem installiert haben, das Debuggingfunktionen bereitstellt (z. b. Microsoft Visual Studio), bewirken Ausnahmen, die nicht von Ihrem Skriptcode behandelt werden, dass ein Debugger-Dialogfeld für jede Ausnahme geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="af759-125">When logging is enabled and you have installed a development system that provides debugging capabilities (such as Microsoft Visual Studio), exceptions that are not handled by your script code will cause a debugger warning dialog box to open for each exception.</span></span> <span data-ttu-id="af759-126">Dies ist ein nützliches Feature, das Sie beim Debuggen Ihres Skriptcodes unterstützt.</span><span class="sxs-lookup"><span data-stu-id="af759-126">This is a useful feature to help you debug your script code.</span></span> <span data-ttu-id="af759-127">Außerdem können Sie den Windows-Media Player Prozess manuell an den Debugger anfügen, wenn die Protokollierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="af759-127">Also, you can manually attach the Windows Media Player process to your debugger when logging is enabled.</span></span>

<span data-ttu-id="af759-128">Dieses SDK enthält eine Beispiel-Skin namens "Logging", die die Protokollierungs Funktionalität in Skins veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="af759-128">This SDK includes a sample skin, called "logging", that demonstrates logging functionality in skins.</span></span> <span data-ttu-id="af759-129">Weitere Informationen zum Verwenden der Beispiele finden Sie unter [Beispiele](samples.md).</span><span class="sxs-lookup"><span data-stu-id="af759-129">To learn more about using the samples, see [Samples](samples.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="af759-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="af759-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af759-131">**Informationen zu Skins**</span><span class="sxs-lookup"><span data-stu-id="af759-131">**About Skins**</span></span>](about-skins.md)
</dt> </dl>

 

 




