---
description: Ich verfüge über eine AVI-Datei, die einen Windows Media Video Stream enthält.
ms.assetid: 0b4c5bf2-caa6-4e14-be5f-9e25ec918cf0
title: Ich verfüge über eine AVI-Datei, die einen Windows Media Video Stream enthält. Wie kann ich Sie in eine WMV-Datei konvertieren?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c770a8355e92c6cfe052d86a17c6638a7a9948
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106366543"
---
# <a name="i-have-an-avi-file-containing-a-windows-media-video-stream-how-can-i-convert-it-to-a-wmv-file"></a><span data-ttu-id="d1c60-104">Ich verfüge über eine AVI-Datei, die einen Windows Media Video Stream enthält.</span><span class="sxs-lookup"><span data-stu-id="d1c60-104">I have an AVI file containing a Windows Media Video stream.</span></span> <span data-ttu-id="d1c60-105">Wie kann ich Sie in eine WMV-Datei konvertieren?</span><span class="sxs-lookup"><span data-stu-id="d1c60-105">How can I convert it to a WMV file?</span></span>

<span data-ttu-id="d1c60-106">Die Windows Media Audio-und Video-Codec-Schnittstellen bieten keine Methoden zum Erstellen von Dateien mit dem Advanced Systems-Format (ASF). Dies ist das Format, das für WMV-Dateien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d1c60-106">The Windows Media Audio and Video codec interfaces do not provide methods to create files using the Advanced Systems Format (ASF), which is the format used for WMV files.</span></span> <span data-ttu-id="d1c60-107">Wenn Sie eine Datei (mit einem beliebigen Container) in eine ASF-Datei konvertieren möchten, müssen Sie die Objekte des Windows Media Format SDK verwenden.</span><span class="sxs-lookup"><span data-stu-id="d1c60-107">If you want to convert a file (using any container) to an ASF file, you must use the objects of the Windows Media Format SDK.</span></span>

<span data-ttu-id="d1c60-108">Rufen Sie die komprimierten Windows Media-Beispiele aus der Quelldatei ab, und übergeben Sie Sie als streambeispiele an das Writer-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d1c60-108">Retrieve the compressed Windows Media samples from the source file and pass them to the writer object as stream samples.</span></span> <span data-ttu-id="d1c60-109">Weitere Informationen finden Sie in der SDK-Dokumentation für das Windows Media-Format 9.</span><span class="sxs-lookup"><span data-stu-id="d1c60-109">For more information, see the Windows Media Format 9 Series SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1c60-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d1c60-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1c60-111">Häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="d1c60-111">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 



