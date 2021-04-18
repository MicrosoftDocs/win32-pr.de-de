---
description: Zeitachse
ms.assetid: 6cc36034-224c-4126-873b-0cfeceec9781
title: Zeitachse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d1f802f12df6ca3469b8283bd4fe8b27e22412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351593"
---
# <a name="timeline"></a><span data-ttu-id="1d44a-103">Zeitachse</span><span class="sxs-lookup"><span data-stu-id="1d44a-103">Timeline</span></span>

> [!Note]  
> <span data-ttu-id="1d44a-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="1d44a-104">\[Deprecated.</span></span> <span data-ttu-id="1d44a-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="1d44a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1d44a-106">Das Timeline-Objekt verwaltet alle-Objekte in einem Video Bearbeitungs Projekt.</span><span class="sxs-lookup"><span data-stu-id="1d44a-106">The timeline object manages all of the objects in a video editing project.</span></span> <span data-ttu-id="1d44a-107">Um dieses Objekt zu erstellen, rufen Sie **cokreateinstance** auf.</span><span class="sxs-lookup"><span data-stu-id="1d44a-107">To create this object, call **CoCreateInstance**.</span></span> <span data-ttu-id="1d44a-108">Der Klassen Bezeichner ist CLSID \_ amtimeline.</span><span class="sxs-lookup"><span data-stu-id="1d44a-108">The class identifier is CLSID\_AMTimeline.</span></span>

<span data-ttu-id="1d44a-109">Um Windows Media™-Dateien zu lesen, muss die Anwendung ein Software Zertifikat bereitstellen, das auch als Schlüssel bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="1d44a-109">To read Windows Media™ files, the application must provide a software certificate, also called a key.</span></span> <span data-ttu-id="1d44a-110">Registrieren Sie die Anwendung als Schlüssel Anbieter über die **IObjectWithSite** -Schnittstelle der Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="1d44a-110">Register the application as a key provider through the timeline's **IObjectWithSite** interface.</span></span> <span data-ttu-id="1d44a-111">Weitere Informationen finden Sie unter [Entsperren des Windows Media-Format](unlocking-the-windows-media-format-sdk.md)-SDKs.</span><span class="sxs-lookup"><span data-stu-id="1d44a-111">For more information, see [Unlocking the Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).</span></span>

<span data-ttu-id="1d44a-112">Das Timeline-Objekt macht die folgenden Schnittstellen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="1d44a-112">The timeline object exposes the following interfaces:</span></span>

-   [<span data-ttu-id="1d44a-113">**Iameinterrorlog**</span><span class="sxs-lookup"><span data-stu-id="1d44a-113">**IAMSetErrorLog**</span></span>](iamseterrorlog.md)
-   [<span data-ttu-id="1d44a-114">**Iamtimeline**</span><span class="sxs-lookup"><span data-stu-id="1d44a-114">**IAMTimeline**</span></span>](iamtimeline.md)
-   <span data-ttu-id="1d44a-115">**IObjectWithSite**</span><span class="sxs-lookup"><span data-stu-id="1d44a-115">**IObjectWithSite**</span></span>
-   <span data-ttu-id="1d44a-116">**IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="1d44a-116">**IPersistStream**</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d44a-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1d44a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d44a-118">Das Zeitachsen Modell</span><span class="sxs-lookup"><span data-stu-id="1d44a-118">The Timeline Model</span></span>](the-timeline-model.md)
</dt> <dt>

[<span data-ttu-id="1d44a-119">Erstellen einer Zeitachse</span><span class="sxs-lookup"><span data-stu-id="1d44a-119">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



