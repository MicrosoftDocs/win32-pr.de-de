---
title: Streampriorisierung
description: Streampriorisierung
ms.assetid: 6b3e9b03-62ef-422b-97ab-197d1cd15beb
keywords:
- Windows Media-Format-SDK, streampriorisierung
- Advanced Systems Format (ASF), streampriorisierung
- ASF (Advanced Systems Format), streampriorisierung
- Windows Media-Format-SDK, Prioritäts Reihenfolge für Streams
- Advanced Systems Format (ASF), Prioritäts Reihenfolge für Streams
- ASF (Advanced Systems Format), Prioritäts Reihenfolge für Streams
- Streams, Priorisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe1628ef050d393cd2d98e73708d5a9ad6c3be4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038572"
---
# <a name="stream-prioritization"></a><span data-ttu-id="cc422-110">Streampriorisierung</span><span class="sxs-lookup"><span data-stu-id="cc422-110">Stream Prioritization</span></span>

<span data-ttu-id="cc422-111">Wenn Sie eine ASF-Datei erstellen, können Sie eine Prioritäts Reihenfolge für die zugehörigen Datenströme angeben.</span><span class="sxs-lookup"><span data-stu-id="cc422-111">When you create an ASF file, you can specify a priority order for its constituent streams.</span></span> <span data-ttu-id="cc422-112">Wenn Sie eine priorisierte Datei streamen und die verfügbare Bandbreite nicht ausreicht, um alle Streams zu übermitteln, löscht der Reader Datenströme in umgekehrter Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="cc422-112">If you stream a prioritized file and the available bandwidth is not enough to deliver all of the streams, the reader will drop streams in reverse priority order.</span></span> <span data-ttu-id="cc422-113">Auf diese Weise können Sie sicherstellen, dass die wichtigsten Datenströme in Ihrer Datei aufgrund von Netzwerkproblemen nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="cc422-113">In this way you can guarantee that the most important streams in your file will not be dropped due to network difficulties.</span></span>

<span data-ttu-id="cc422-114">Die streampriorisierung wird mit einem streampriorisierungsobjekt konfiguriert und dem Profil hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cc422-114">Stream prioritization is configured with a stream prioritization object and added to the profile.</span></span> <span data-ttu-id="cc422-115">Ein Profil kann nur ein Datenstrom Priorisierungs Objekt enthalten.</span><span class="sxs-lookup"><span data-stu-id="cc422-115">A profile can contain only one stream prioritization object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc422-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cc422-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc422-117">**Funktionen der ASF-Datei**</span><span class="sxs-lookup"><span data-stu-id="cc422-117">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="cc422-118">**IWMProfile3:: kreatenewstreampriorisierung**</span><span class="sxs-lookup"><span data-stu-id="cc422-118">**IWMProfile3::CreateNewStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization)
</dt> <dt>

[<span data-ttu-id="cc422-119">**IWMProfile3:: getstreamprioritisierung**</span><span class="sxs-lookup"><span data-stu-id="cc422-119">**IWMProfile3::GetStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)
</dt> <dt>

[<span data-ttu-id="cc422-120">**IWMProfile3:: removestreamprioritisierung**</span><span class="sxs-lookup"><span data-stu-id="cc422-120">**IWMProfile3::RemoveStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-removestreamprioritization)
</dt> <dt>

[<span data-ttu-id="cc422-121">**IWMProfile3:: setstreampriorisierung**</span><span class="sxs-lookup"><span data-stu-id="cc422-121">**IWMProfile3::SetStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization)
</dt> <dt>

[<span data-ttu-id="cc422-122">**Iwmstreampriorisierungsschnittstelle**</span><span class="sxs-lookup"><span data-stu-id="cc422-122">**IWMStreamPrioritization Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization)
</dt> <dt>

[<span data-ttu-id="cc422-123">**Verwenden der streampriorisierung**</span><span class="sxs-lookup"><span data-stu-id="cc422-123">**Using Stream Prioritization**</span></span>](using-stream-prioritization.md)
</dt> </dl>

 

 




