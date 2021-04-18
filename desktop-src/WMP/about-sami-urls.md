---
title: Informationen zu Sami-URLs
description: Informationen zu Sami-URLs
ms.assetid: 6898a0d5-cfd0-4ba5-8cd1-907cf110667c
keywords:
- Windows Media Player, synchronisierter zugänglicher Medienaustausch (Sami)
- Windows Media Player-Objektmodell, synchronisierter zugänglicher Medienaustausch (Sami)
- Objektmodell, synchronisierter, zugänglicher Medienaustausch (Sami)
- Windows Media Player Mobile, synchronisierter verfügbarer Medienaustausch (Sami)
- Windows Media Player ActiveX-Steuerelement, synchronisierter barrierefreier Medienaustausch (Sami)
- Windows Media Player Mobile ActiveX-Steuerelement, synchronisierter barrierefreier Medienaustausch (Sami)
- ActiveX-Steuerelement, synchronisierter, zugänglicher Medienaustausch (Sami)
- Synchronisierter, barrierefreier Medienaustausch (Sami), Dateien
- Samisch (synchronisierter, zugänglicher Medienaustausch), Dateien
- Synchronisierter, barrierefreier Medienaustausch (Sami), URLs
- Samisch (synchronisierter, zugänglicher Medienaustausch), URLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a7a41e70d0239b9bdac7d12f9a2dd2f75be15b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206575"
---
# <a name="about-sami-urls"></a><span data-ttu-id="c2ab8-114">Informationen zu Sami-URLs</span><span class="sxs-lookup"><span data-stu-id="c2ab8-114">About SAMI URLs</span></span>

<span data-ttu-id="c2ab8-115">Sami-Dateien können mithilfe einer einzelnen URL digitalen Mediendateien zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="c2ab8-115">SAMI files can be associated with digital media files by using a single URL.</span></span> <span data-ttu-id="c2ab8-116">Dies erfolgt mithilfe *des Sami* URL-Parameters.</span><span class="sxs-lookup"><span data-stu-id="c2ab8-116">This is accomplished by using *the sami* URL parameter.</span></span> <span data-ttu-id="c2ab8-117">Dem URL-Parameter sind die Basis-URL und eine vorangestellt?</span><span class="sxs-lookup"><span data-stu-id="c2ab8-117">The URL parameter is preceded by the base URL and a ?</span></span> <span data-ttu-id="c2ab8-118">befinden.</span><span class="sxs-lookup"><span data-stu-id="c2ab8-118">character.</span></span> <span data-ttu-id="c2ab8-119">Eine URL mit einem *Sami* -Parameter folgt der folgenden Syntax:</span><span class="sxs-lookup"><span data-stu-id="c2ab8-119">A URL with a *sami* parameter follows this syntax:</span></span>

<span data-ttu-id="c2ab8-120">*URL*? *Samisch* = *captionsurl*.</span><span class="sxs-lookup"><span data-stu-id="c2ab8-120">*URL*?*sami*=*captionsURL*.</span></span>

<span data-ttu-id="c2ab8-121">Der Wert des URL-Parameters folgt dem Parameternamen und einem Gleichheitszeichen, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="c2ab8-121">The value of the URL parameter follows the parameter name and an equals sign, as in the following example:</span></span>


```C++
https://proseware.com/samitest.wma?sami=https://acc.proseware.com/test.smi

```



<span data-ttu-id="c2ab8-122">Diese URL-Syntax wird häufig in einem Hyperlink oder einer Windows Media-Metadatendatei verwendet, um direkt mit den Speicherorten der digitalen Mediendatei und der Sami-Datei zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="c2ab8-122">This URL syntax is commonly used in a hyperlink or a Windows Media metafile to link directly to the locations of both the digital media file and the SAMI file.</span></span> <span data-ttu-id="c2ab8-123">Wenn der Benutzer auf den Link klickt, wird Windows Media Player im vollständigen Modus gestartet und die digitalen Medieninhalte wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="c2ab8-123">When the user clicks on the hyperlink, Windows Media Player launches in full mode and plays the digital media content.</span></span>

<span data-ttu-id="c2ab8-124">Wenn der *Sami* URL-Parameter nicht angegeben ist, sucht Windows Media Player nach einer Sami-Datei, die sich am gleichen Speicherort wie die digitale Mediendatei befindet und den gleichen Dateinamen hat, mit Ausnahme der Dateinamenerweiterung, die SMI lauten muss.</span><span class="sxs-lookup"><span data-stu-id="c2ab8-124">If the *sami* URL parameter is not specified, Windows Media Player will look for a SAMI file that is in the same location as the digital media file and that has the same file name except for the file name extension, which must be .smi.</span></span> <span data-ttu-id="c2ab8-125">Wenn eine solche Datei vorhanden ist, wird Sie automatisch geöffnet, wenn die Beschriftungs Anzeige im Player aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c2ab8-125">If such a file is present, it will be opened automatically if caption display has been enabled in the Player.</span></span>

<span data-ttu-id="c2ab8-126">Untertitel werden in Windows Media Player aktiviert, indem Sie auf das Menü wieder **Gabe** klicken, dann auf **Beschriftungen und Untertitel** klicken und dann **auf** klicken.</span><span class="sxs-lookup"><span data-stu-id="c2ab8-126">Closed captions are enabled in Windows Media Player by clicking the **Play** menu, then clicking **Captions and Subtitles**, and then clicking **On**.</span></span> <span data-ttu-id="c2ab8-127">Wenn Untertitel aktiviert sind, werden die in der Sami-Datei enthaltenen Beschriftungen angezeigt, während das Medien Element abgespielt wird.</span><span class="sxs-lookup"><span data-stu-id="c2ab8-127">If closed captions are enabled, the captions contained in the SAMI file will display while the media item plays.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2ab8-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c2ab8-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2ab8-129">**Hinzufügen von Untertiteln zu digitalen Medien**</span><span class="sxs-lookup"><span data-stu-id="c2ab8-129">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




