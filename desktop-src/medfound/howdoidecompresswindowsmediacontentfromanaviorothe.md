---
description: Gewusst wie Datenströme aus einer AVI-Datei oder einer anderen Datei dekomprimieren, über die ich keine Formatinformationen verfüge?
ms.assetid: 980f52f4-17a4-4871-9269-f9e0b97416c6
title: Gewusst wie Datenströme aus einer AVI-Datei oder einer anderen Datei dekomprimieren, über die ich keine Formatinformationen verfüge?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad230c36097a93b3d2d41ddffb35600d0616ea5f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106365226"
---
# <a name="how-do-i-decompress-streams-from-an-avi-file-or-other-file-about-which-i-have-no-format-information"></a><span data-ttu-id="9a8ab-103">Gewusst wie Datenströme aus einer AVI-Datei oder einer anderen Datei dekomprimieren, über die ich keine Formatinformationen verfüge?</span><span class="sxs-lookup"><span data-stu-id="9a8ab-103">How do I decompress streams from an AVI file or other file about which I have no format information?</span></span>

<span data-ttu-id="9a8ab-104">Ohne Formatinformationen, einschließlich erweiterter Formatierungsdaten, ist es nicht möglich, Daten zu dekomprimieren, die mit einem Windows Media-Codec codiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9a8ab-104">Without format information, including extended format data, you cannot decompress data that was encoded with a Windows Media codec.</span></span> <span data-ttu-id="9a8ab-105">Die Codecs wurden entwickelt, um Datenströme für die Verwendung mit dem Datei Container Advanced Systems Format (ASF) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9a8ab-105">The codecs were designed to create data streams for use with the Advanced Systems Format (ASF) file container.</span></span> <span data-ttu-id="9a8ab-106">Im Header Abschnitt einer ASF-Datei werden die Formatinformationen für alle Streams in der Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9a8ab-106">The header section of an ASF file stores the format information for all of the streams in the file.</span></span> <span data-ttu-id="9a8ab-107">Wenn Sie Inhalte verwenden, die mit einem der Windows Media Audio-und Video Codecs außerhalb einer ASF-Datei codiert sind, müssen Sie sicherstellen, dass die Formatinformationen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="9a8ab-107">When you use content encoded using one of the Windows Media Audio and Video codecs outside of an ASF file, you must ensure that the format information is available.</span></span> <span data-ttu-id="9a8ab-108">Die Vorgehensweise unterscheidet sich von einem Container zu einem anderen.</span><span class="sxs-lookup"><span data-stu-id="9a8ab-108">The way to do this varies from one container to another.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a8ab-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9a8ab-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a8ab-110">Häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="9a8ab-110">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 



