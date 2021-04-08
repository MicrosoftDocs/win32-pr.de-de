---
description: Mindestens erforderliche DMO-Anforderungen
ms.assetid: cd342f0f-a3dc-4623-a18f-c45071795ef4
title: Mindestens erforderliche DMO-Anforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c26267f50619062fb8396f93b7578db4d3d8c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957995"
---
# <a name="dmo-minimum-requirements"></a><span data-ttu-id="f99b1-103">Mindestens erforderliche DMO-Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f99b1-103">DMO Minimum Requirements</span></span>

<span data-ttu-id="f99b1-104">Jeder DMO sollte die folgenden Mindestanforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="f99b1-104">Every DMO should meet the following minimum requirements:</span></span>

-   <span data-ttu-id="f99b1-105">Die Aggregation muss unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f99b1-105">It must support aggregation.</span></span>
-   <span data-ttu-id="f99b1-106">Es muss die [**imediaobject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) -Schnittstelle verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="f99b1-106">It must expose the [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) interface.</span></span>
-   <span data-ttu-id="f99b1-107">Das Threading Modell muss "both" lauten.</span><span class="sxs-lookup"><span data-stu-id="f99b1-107">The threading model must be 'both'.</span></span> <span data-ttu-id="f99b1-108">DMOS muss in einer frei Hand Thread Umgebung ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="f99b1-108">DMOs must function correctly in a free-threaded environment.</span></span>

<span data-ttu-id="f99b1-109">Der Audioeffekt-DMOS sollte die [**imediaobjectinplace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) -Schnittstelle unterstützen, die in DirectMusic und DirectSound verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f99b1-109">Audio effect DMOs should support the [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) interface, for use in DirectMusic and DirectSound.</span></span>

<span data-ttu-id="f99b1-110">Die folgenden Schnittstellen sind an anderer Stelle dokumentiert, sind aber für viele DMOS nützlich.</span><span class="sxs-lookup"><span data-stu-id="f99b1-110">The following interfaces are documented elsewhere, but are useful for many DMOs.</span></span> <span data-ttu-id="f99b1-111">Sie sind jedoch nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f99b1-111">They are not required, however.</span></span>

-   <span data-ttu-id="f99b1-112">**ISpecifyPropertyPages**, **IPropertyPage**: Diese Schnittstellen ermöglichen es einem DMO, eine Eigenschaften Seite bereitzustellen, damit Benutzereigenschaften festlegen können.</span><span class="sxs-lookup"><span data-stu-id="f99b1-112">**ISpecifyPropertyPages**, **IPropertyPage**: These interfaces enable a DMO to provide a property page, for the user to set properties.</span></span>
-   <span data-ttu-id="f99b1-113">**IPersistStream**: Diese Schnittstelle ermöglicht es dem DMO, seinen Zustand in einem persistenten Speicher zu speichern.</span><span class="sxs-lookup"><span data-stu-id="f99b1-113">**IPersistStream**: This interface enables the DMO to save its state to persistent storage.</span></span>
-   <span data-ttu-id="f99b1-114">[**Iamstreamconfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression): Diese Schnittstellen ermöglichen es einem Client, das Ausgabeformat und die Komprimierungs Einstellungen eines Encoders zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f99b1-114">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression): These interfaces enable a client to configure an encoder's output format and compression settings.</span></span> <span data-ttu-id="f99b1-115">(Diese beiden Schnittstellen sind Teil der DirectShow-API, werden aber auch für DMOS empfohlen.)</span><span class="sxs-lookup"><span data-stu-id="f99b1-115">(These two interfaces are part of the DirectShow API, but are also recommended for DMOs.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="f99b1-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f99b1-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f99b1-117">Schreiben eines DMO</span><span class="sxs-lookup"><span data-stu-id="f99b1-117">Writing a DMO</span></span>](writing-a-dmo.md)
</dt> </dl>

 

 



