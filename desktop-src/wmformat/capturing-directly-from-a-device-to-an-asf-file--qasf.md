---
title: Direkte Erfassung von einem Gerät in eine ASF-Datei (qasf)
description: Direkte Erfassung von einem Gerät in eine ASF-Datei (qasf)
ms.assetid: 684a11e3-d507-4219-bc0b-6dfe5e85dad1
keywords:
- Windows Media-Format-SDK, Erfassen von Geräten in ASF-Dateien (qasf)
- Windows Media-Format-SDK, DirectShow
- Advanced Systems Format (ASF), Erfassung von Geräten (qasf)
- ASF (Advanced Systems Format), Erfassung von Geräten (qasf)
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow, Erfassen von Geräten in ASF-Dateien (qasf)
- Windows Media-Format-SDK, qasf
- Advanced Systems Format (ASF), qasf
- ASF (Advanced Systems Format), qasf
- DirectShow, qasf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faaf5ba8df3cffbb2121451d3bd1b456fc994078
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339217"
---
# <a name="capturing-directly-from-a-device-to-an-asf-file-qasf"></a><span data-ttu-id="4e8eb-114">Direkte Erfassung von einem Gerät in eine ASF-Datei (qasf)</span><span class="sxs-lookup"><span data-stu-id="4e8eb-114">Capturing Directly from a Device to an ASF File (QASF)</span></span>

<span data-ttu-id="4e8eb-115">Wenn Sie Audiodaten oder Videos direkt in einer ASF-Datei erfassen, sieht das Filter Diagramm in etwa wie das folgende Diagramm aus, abhängig vom Typ des verwendeten Erfassungs Geräts.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-115">When capturing audio or video directly to an ASF file, the filter graph looks something like the following diagram, depending on the type of capture device being used.</span></span>

![Grafik zur WMV-Erfassung](images/asf-webcam.png)

<span data-ttu-id="4e8eb-117">In der DirectShow-SDK-Dokumentation wird ausführlich beschrieben, wie Aufzeichnungs Diagramme erstellt werden. es gibt jedoch einen wichtigen Punkt beim Erstellen von Erfassungs Diagrammen mit dem WM-ASF-Writer: der WM-ASF-Writer wird nicht ausgeführt, es sei denn, alle seine Pins sind verbunden.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-117">The DirectShow SDK documentation describes in detail how to create capture graphs, but there is one important point to remember when creating capture graphs using the WM ASF Writer: the WM ASF Writer will not run unless all of its pins are connected.</span></span> <span data-ttu-id="4e8eb-118">Wenn Sie den WM-ASF-Writer mit dem Standardsystem Profil (nicht empfohlen) oder einem beliebigen Profil mit Audio-und Videostreams konfigurieren, wird eine Eingabe-PIN für jeden Stream erstellt, und jeder dieser Pins muss verbunden sein.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-118">If you configure the WM ASF Writer with the default system profile (not recommended), or any profile with audio and video streams, then it will create an input pin for each stream and each of those pins must be connected.</span></span> <span data-ttu-id="4e8eb-119">Wenn Sie z. b. keine Audiodaten erfassen möchten, stellen Sie sicher, dass Sie den Filter mit einem nur-Video-Profil konfigurieren, sodass keine audiopin erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-119">If you do not intend to capture audio, for example, then be sure to configure the filter with a video-only profile so that no audio pin is created.</span></span>

 

 




