---
description: Codec-Verfügbarkeit und Platt Form Unterstützung
ms.assetid: 6b3d09c9-e91f-4c62-92f7-c2643e51987f
title: Codec-Verfügbarkeit und Platt Form Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc485c5f8db9ff7883263cd614578705eccd3fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217375"
---
# <a name="codec-availability-and-platform-support"></a><span data-ttu-id="2a2ea-103">Codec-Verfügbarkeit und Platt Form Unterstützung</span><span class="sxs-lookup"><span data-stu-id="2a2ea-103">Codec Availability and Platform Support</span></span>

<span data-ttu-id="2a2ea-104">Microsoft empfiehlt, dass Kamerahersteller aktualisierte Rohdaten von Windows Imaging Component (WIC) in der Software Verteilung mit neuen Kameras einschließen und dass der aktualisierte Codec mit der Standardinstallation der Hersteller Software Windows 7, Windows Vista und Windows XP installiert wird.</span><span class="sxs-lookup"><span data-stu-id="2a2ea-104">Microsoft recommends that camera vendors include updated RAW Windows Imaging Component (WIC) codecs in the software distribution with new cameras and that the updated codec be installed with the default vendor software installation Windows 7, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="2a2ea-105">Kamerahersteller sollten auch den neuesten WIC-Codec als Download von den Support Websites bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="2a2ea-105">Camera vendors should also provide the latest WIC codec as a download from their support sites.</span></span>

## <a name="codec-discovery"></a><span data-ttu-id="2a2ea-106">Codec-Ermittlung</span><span class="sxs-lookup"><span data-stu-id="2a2ea-106">Codec Discovery</span></span>

<span data-ttu-id="2a2ea-107">Microsoft geht wie folgt vor, um den Benutzern zu helfen, für Codec-Downloads auf die Websites der Anbieter zuzugreifen:</span><span class="sxs-lookup"><span data-stu-id="2a2ea-107">Microsoft is doing the following to help point users to vendors' Web sites for codec downloads:</span></span>

-   <span data-ttu-id="2a2ea-108">Wenn ein Benutzer in Windows-Explorer auf eine nicht erkannte Datei doppelklickt (der Standardfall, wenn sich eine Rohdatendatei auf dem Computer befindet, aber der Codec noch nicht installiert ist), wird in einem Dialogfeld gemeldet, dass die Datei nicht erkannt wird, und es wird gefragt, ob der Benutzer ein Programm suchen möchte, das die Datei versteht.</span><span class="sxs-lookup"><span data-stu-id="2a2ea-108">In Windows Explorer, if a user double-clicks a file that is not recognized (the default case when a RAW file is on the computer, but the codec is not installed yet), a dialog box reports that the file is not recognized and asks whether the user wants to find a program that understands the file.</span></span> <span data-ttu-id="2a2ea-109">Microsoft verwaltet einen vorhandenen Umleitungs Dienst, um Benutzer an die Websites des Anbieters weiterzuleiten, die das Programm bereitstellen können, um die Datei zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="2a2ea-109">Microsoft maintains an existing redirection service to forward users to vendors' Web sites that can supply the program to understand the file.</span></span> <span data-ttu-id="2a2ea-110">Diese Funktion ist in Windows XP und Windows Vista vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2a2ea-110">This facility exists in Windows XP and in Windows Vista.</span></span>
-   <span data-ttu-id="2a2ea-111">Die Windows-Fotogalerie, die Windows Live-Fotogalerie und der Windows 7 Photo Viewer erkennen einen Satz von Dateierweiterungen als Rohdatendateien.</span><span class="sxs-lookup"><span data-stu-id="2a2ea-111">The Windows Photo Gallery, Windows Live Photo Gallery, and the Windows 7 Photo Viewer recognize a set of file extensions as RAW files.</span></span> <span data-ttu-id="2a2ea-112">Wenn Dateien aus diesem Satz in Ordnern gefunden werden, die von einer dieser Anwendungen untersucht werden, und ein Codec für die Datei noch nicht installiert ist, wird ein Dialogfeld angezeigt, wie im vorherigen Abschnitt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2a2ea-112">If files from that set are found in folders that any of these applications are looking at, and a codec for the file is not already installed, then a dialog box appears, as described in the preceding paragraph.</span></span>

<span data-ttu-id="2a2ea-113">Weitere Informationen zur Codec-Ermittlung finden Sie unter Support für Codec-Verfügbarkeit und-Plattform.</span><span class="sxs-lookup"><span data-stu-id="2a2ea-113">For more information about codec discovery, see Codec Availability and Platform Support.</span></span>

## <a name="windows-xp-platform-support"></a><span data-ttu-id="2a2ea-114">Windows XP-Platt Form Unterstützung</span><span class="sxs-lookup"><span data-stu-id="2a2ea-114">Windows XP Platform Support</span></span>

<span data-ttu-id="2a2ea-115">Microsoft hat Windows XP SP3 mit WIC und einen eigenständigen WIC-Installer für Windows XP SP2 veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="2a2ea-115">Microsoft has released Windows XP SP3 with WIC, and a standalone WIC installer for Windows XP SP2.</span></span> <span data-ttu-id="2a2ea-116">Diese verwenden WIC-Codecs, um die Unterstützung für Miniaturansichten und Vorschau auf diesen Plattformen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="2a2ea-116">These use WIC codecs to enable support for thumbnails and previews on those platforms.</span></span> <span data-ttu-id="2a2ea-117">Daher ist es wichtig, dass Codec-Downloads und-Installationen unter Windows 7, Windows Vista und Windows XP unterstützt und getestet werden.</span><span class="sxs-lookup"><span data-stu-id="2a2ea-117">Therefore, it is important that codec download and installation be supported and tested on the Windows 7, Windows Vista, and Windows XP.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a2ea-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2a2ea-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2a2ea-119">**Licher**</span><span class="sxs-lookup"><span data-stu-id="2a2ea-119">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2a2ea-120">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="2a2ea-120">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="2a2ea-121">WIC-Richtlinien für Kamera Rohbild Formate</span><span class="sxs-lookup"><span data-stu-id="2a2ea-121">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="2a2ea-122">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="2a2ea-122">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



