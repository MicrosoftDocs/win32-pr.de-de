---
title: Richtlinien für die Dateinamenerweiterung
description: Richtlinien für die Dateinamenerweiterung
ms.assetid: 71189ed8-4140-446f-a765-d72f35dd3d88
keywords:
- Windows Media-Format-SDK, Dateinamen Erweiterungen
- Advanced Systems Format (ASF), Dateinamen Erweiterungen
- ASF (Advanced Systems Format), Dateinamen Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bed1fb59379644711a3954dc5eb82707e0e42f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947670"
---
# <a name="file-name-extension-guidelines"></a><span data-ttu-id="0ace5-106">Richtlinien für die Dateinamenerweiterung</span><span class="sxs-lookup"><span data-stu-id="0ace5-106">File Name Extension Guidelines</span></span>

<span data-ttu-id="0ace5-107">Eine Dateinamenerweiterung bietet einem unabhängigen Softwarehersteller Informationen zu den Renderinganforderungen einer Anwendung, die diese spezielle Erweiterung verwendet.</span><span class="sxs-lookup"><span data-stu-id="0ace5-107">A file name extension provides an independent software vendor with information about the rendering requirements of an application that uses that particular extension.</span></span>

<span data-ttu-id="0ace5-108">Die Dateinamenerweiterung, die Sie für eine Datei verwenden müssen, die von einer Anwendung basierend auf dem Windows Media Format SDK erstellt wurde, hängt vom Typ des Inhalts in der Datei ab.</span><span class="sxs-lookup"><span data-stu-id="0ace5-108">The file name extension you must use for a file created by an application based on the Windows Media Format SDK is determined by the type of content in the file.</span></span> <span data-ttu-id="0ace5-109">Verwenden Sie die folgende Logik, um die Dateinamenerweiterung zu bestimmen, die Sie verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="0ace5-109">Use the following logic to determine the file name extension you must use.</span></span>

<span data-ttu-id="0ace5-110">Wenn die Datei Datenströme enthält, die von Drittanbietern oder nicht unterstützten unkomprimierten Daten (einschließlich beliebiger Daten) codiert sind, muss die Datei die. asf-Erweiterung verwenden.</span><span class="sxs-lookup"><span data-stu-id="0ace5-110">If the file contains any streams encoded with third-party codecs or any unsupported uncompressed data (including arbitrary data), the file must use the .asf extension.</span></span>

<span data-ttu-id="0ace5-111">Wenn die Datei keine nicht unterstützten Streams enthält und mindestens einen Videostream enthält, der entweder unkomprimiert ist oder mit einem beliebigen Windows Media-Videocodec codiert ist, muss die Datei die Erweiterung. wmv verwenden.</span><span class="sxs-lookup"><span data-stu-id="0ace5-111">If the file contains no unsupported streams and contains one or more video streams either uncompressed or encoded with any Windows Media video codec, the file must use the .wmv extension.</span></span> <span data-ttu-id="0ace5-112">Diese Dateien können auch PCM-Audiostreams, Audiostreams enthalten, die mit beliebigen Windows Media-Audiocodecs, Skript Datenströmen und Webstreams codiert sind.</span><span class="sxs-lookup"><span data-stu-id="0ace5-112">These files may also include PCM audio streams, audio streams encoded with any Windows Media audio codec, script streams, and Web streams.</span></span>

<span data-ttu-id="0ace5-113">Wenn die Datei keine nicht unterstützten Streams und keine unterstützten Videostreams enthält und mindestens ein Audiodatenstrom entweder unkomprimiertes PCM oder codiert mit einem beliebigen Windows Media-Audiocodec enthält, muss die Datei die. wma-Erweiterung verwenden.</span><span class="sxs-lookup"><span data-stu-id="0ace5-113">If the file contains no unsupported streams and no supported video streams, and contains one or more audio streams either uncompressed PCM or encoded with any Windows Media audio codec, the file must use the .wma extension.</span></span> <span data-ttu-id="0ace5-114">Diese Dateien können auch Skript Datenströme und Webstreams enthalten.</span><span class="sxs-lookup"><span data-stu-id="0ace5-114">These files may also contain script streams, and Web streams.</span></span>

<span data-ttu-id="0ace5-115">Wenn die Datei nur Datenströme enthält, die weder Audiodaten noch Video enthalten, muss Sie die Erweiterung ". ASF" verwenden.</span><span class="sxs-lookup"><span data-stu-id="0ace5-115">If the file contains only streams that are neither audio nor video, it must use the .asf extension.</span></span>

<span data-ttu-id="0ace5-116">Unterstützte unkomprimierte Video Typen sind RGB8, RGB565, RGB555, RGB24, RGB32, I420, IYUV, YV12, im YUY2, UYVY, yvyu und YVU9.</span><span class="sxs-lookup"><span data-stu-id="0ace5-116">Supported uncompressed video types include RGB8, RGB565, RGB555, RGB24, RGB32, I420, IYUV, YV12, YUY2, UYVY, YVYU, and YVU9.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ace5-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0ace5-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ace5-118">**Überlegungen zu Projekten**</span><span class="sxs-lookup"><span data-stu-id="0ace5-118">**Project Considerations**</span></span>](project-considerations.md)
</dt> </dl>

 

 




