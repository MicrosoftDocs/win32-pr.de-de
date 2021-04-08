---
title: Unterstützung für mehrere Sprachen
description: Unterstützung für mehrere Sprachen
ms.assetid: f46efb7f-73d1-4f64-aa44-cb50170a2245
keywords:
- Windows Media Metadatei-Wiedergabelisten, Unterstützung für mehrere Sprachen
- Metadatei-Wiedergabelisten, Unterstützung für mehrere Sprachen
- Wiedergabelisten, Unterstützung für mehrere Sprachen
- Windows Media Metadatei-Wiedergabelisten, Unterstützung mehrerer Sprachen
- Metadatei-Wiedergabelisten, Unterstützung mehrerer Sprachen
- Wiedergabelisten, Unterstützung mehrerer Sprachen
- Windows Media Metadatei-Wiedergabelisten, Sprachunterstützung
- Metadatei-Wiedergabelisten, Sprachunterstützung
- Wiedergabelisten, Sprachunterstützung
- Unterstützung für mehrere Sprachen
- Unterstützung mehrerer Sprachen
- Sprachenunterstützung
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d8855aeb798e4243182a6f82479289ccccbd97d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037443"
---
# <a name="support-for-multiple-languages"></a><span data-ttu-id="98bb4-115">Unterstützung für mehrere Sprachen</span><span class="sxs-lookup"><span data-stu-id="98bb4-115">Support for Multiple Languages</span></span>

<span data-ttu-id="98bb4-116">Windows Media Player 9 oder höher unterstützt Windows Media-Metadateien, die mit dem Unicode-Zeichensatz erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="98bb4-116">Windows Media Player 9 Series or later supports Windows Media metafiles created using the Unicode character set.</span></span> <span data-ttu-id="98bb4-117">Auf diese Weise können Sie mehrsprachige Metadaten in die Metadatei-Wiedergabeliste einschließen.</span><span class="sxs-lookup"><span data-stu-id="98bb4-117">This allows you to include multilingual metadata in your metafile playlist.</span></span> <span data-ttu-id="98bb4-118">Die folgenden Regeln bestimmen die Verwendung mehrsprachiger Metadaten in Windows Media-Metadateien:</span><span class="sxs-lookup"><span data-stu-id="98bb4-118">The following rules govern the use of multilingual metadata in Windows Media metafiles:</span></span>

-   <span data-ttu-id="98bb4-119">Zeichen müssen mithilfe des UTF-8-Codierungs Schemas codiert werden.</span><span class="sxs-lookup"><span data-stu-id="98bb4-119">Characters must be encoded using the UTF-8 encoding scheme.</span></span>
-   <span data-ttu-id="98bb4-120">Die Metadatei-Wiedergabeliste muss **die folgenden Parameter** auf der Wiedergabelisten Ebene enthalten:</span><span class="sxs-lookup"><span data-stu-id="98bb4-120">The metafile playlist must include the following **PARAM** at the playlist level:</span></span>
    ```XML
    <PARAM  NAME = "Encoding"  VALUE = "utf-8">
    
    ```

    

-   <span data-ttu-id="98bb4-121">Diese Funktion wird nur von Windows Media Player 9 oder höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="98bb4-121">Only Windows Media Player 9 Series or later supports this functionality.</span></span>
-   <span data-ttu-id="98bb4-122">Wenn die Metadatei-Wiedergabeliste nicht mit UTF-8-Codierung und dem korrekten **param** -Element gespeichert wird, wird Sie mithilfe der Standard Codepage des System Gebiets Schemas auf dem Computer des Benutzers analysiert.</span><span class="sxs-lookup"><span data-stu-id="98bb4-122">If the metafile playlist is not saved with UTF-8 encoding and the correct **PARAM** element, it will be parsed using the default system locale code page of the user's computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="98bb4-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="98bb4-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98bb4-124">**Param-Element**</span><span class="sxs-lookup"><span data-stu-id="98bb4-124">**PARAM Element**</span></span>](param-element.md)
</dt> <dt>

[<span data-ttu-id="98bb4-125">**Übersicht über Windows Media-Metadatendateien**</span><span class="sxs-lookup"><span data-stu-id="98bb4-125">**Windows Media Metafiles Overview**</span></span>](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




