---
title: Geräte Erweiterungen für die beschleunigte metadatenübertragung
description: Geräte Erweiterungen für die beschleunigte metadatenübertragung
ms.assetid: a79b54d4-dad5-411b-aaff-b58bb549d4d1
keywords:
- Windows Media Player, Geräte Erweiterungen
- Windows-Media Player, Erweiterungen
- Windows Media Player, beschleunigte metadatenübertragung
- Windows Media Player, beschleunigte metadatenübertragung
- beschleunigte metadatenübertragung
- Metadaten, beschleunigte Übertragung
- Geräte Erweiterungen, beschleunigte metadatenübertragung
- Erweiterungen, beschleunigte metadatenübertragung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe661dff0750f2ad46bef96e537b0852d480db8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037213"
---
# <a name="device-extensions-for-accelerated-metadata-transfer"></a><span data-ttu-id="3d679-111">Geräte Erweiterungen für die beschleunigte metadatenübertragung</span><span class="sxs-lookup"><span data-stu-id="3d679-111">Device Extensions for Accelerated Metadata Transfer</span></span>

<span data-ttu-id="3d679-112">In Windows Media Player 10 wurden neue und erweiterte Funktionen für die Synchronisierung digitaler Mediendateien mit tragbaren Geräten eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3d679-112">Windows Media Player 10 introduced new and extended functionality for synchronizing digital media files with portable devices.</span></span> <span data-ttu-id="3d679-113">Benutzer können ein Gerät mit einem Computer verbinden, Inhalte auf das Gerät übertragen und dann die Verbindung des Geräts trennen, um Inhalte vom Computer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3d679-113">Users can connect a device to a computer, transfer content to the device, and then disconnect the device to enjoy content away from the computer.</span></span>

<span data-ttu-id="3d679-114">Wenn der Benutzer das Gerät erneut mit dem Computer verbindet, ist es möglich, dass sich der auf dem Gerät gespeicherte Inhalt seit der vorherigen Verbindung geändert hat.</span><span class="sxs-lookup"><span data-stu-id="3d679-114">When the user reconnects the device to the computer, it is possible that the content stored on the device changed since the previous connection.</span></span> <span data-ttu-id="3d679-115">Wenn Sie z. b. eine bestimmte digitale Mediendatei abspielen, wird die Wiedergabe Anzahl für dieses Element geändert.</span><span class="sxs-lookup"><span data-stu-id="3d679-115">For example, simply playing a particular digital media file causes the play count for that item to change.</span></span> <span data-ttu-id="3d679-116">Da aktuelle portable Geräte große Mengen an digitalen Medieninhalten speichern können, wäre der Prozess der Ermittlung von Änderungen zu zeitaufwändig, wenn Windows Media Player die einzelnen digitalen Medienelemente auflisten und überprüfen müssten.</span><span class="sxs-lookup"><span data-stu-id="3d679-116">Because current portable devices can store large quantities of digital media content, the process of discovering changes would be too time consuming if Windows Media Player were required to enumerate and inspect each digital media item.</span></span> <span data-ttu-id="3d679-117">Stattdessen können tragbare Gerätehersteller besondere Funktionen implementieren, damit Windows Media Player 10 oder höher Informationen zu Änderungen, die an den auf einem Gerät gespeicherten Inhalt vorgenommen wurden, effizient abrufen können.</span><span class="sxs-lookup"><span data-stu-id="3d679-117">Instead, portable device manufacturers can implement special functionality to enable Windows Media Player 10 or later to efficiently retrieve information about changes made to the content stored on a device.</span></span>

<span data-ttu-id="3d679-118">In den folgenden Abschnitten werden die Konventionen beschrieben, die zum Implementieren dieser Funktionalität verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d679-118">The following sections describe the conventions used to implement this functionality.</span></span>

-   [<span data-ttu-id="3d679-119">Informationen zu den Metadaten</span><span class="sxs-lookup"><span data-stu-id="3d679-119">About the Metadata</span></span>](about-the-metadata.md)
-   [<span data-ttu-id="3d679-120">MTP-Geräte Erweiterungen für die metadatenübertragung</span><span class="sxs-lookup"><span data-stu-id="3d679-120">MTP Device Extensions for Metadata Transfer</span></span>](mtp-device-extensions-for-metadata-transfer.md)
-   [<span data-ttu-id="3d679-121">Windows Media Device Manager-Geräte Erweiterungen für die metadatenübertragung</span><span class="sxs-lookup"><span data-stu-id="3d679-121">Windows Media Device Manager Device Extensions for Metadata Transfer</span></span>](windows-media-device-manager-device-extensions-for-metadata-transfer.md)

## <a name="related-topics"></a><span data-ttu-id="3d679-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3d679-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d679-123">**Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="3d679-123">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 




