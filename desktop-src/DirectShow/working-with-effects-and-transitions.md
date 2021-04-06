---
description: Arbeiten mit Effekten und Übergängen
ms.assetid: 00e97d02-ff43-4e1f-9806-abaeb9288058
title: Arbeiten mit Effekten und Übergängen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99029269ac86e17246fd641341b071654582bc4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960936"
---
# <a name="working-with-effects-and-transitions"></a><span data-ttu-id="24b92-103">Arbeiten mit Effekten und Übergängen</span><span class="sxs-lookup"><span data-stu-id="24b92-103">Working with Effects and Transitions</span></span>

<span data-ttu-id="24b92-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="24b92-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="24b92-105">Auswirkungen Ändern eines einzelnen Clips, nach Titels oder einer Komposition.</span><span class="sxs-lookup"><span data-stu-id="24b92-105">Effects modify a single clip, track, or composition.</span></span> <span data-ttu-id="24b92-106">Mithilfe von Übergängen werden sequenen aus einer Spur erstellt, oder es wird eine andere erstellt.</span><span class="sxs-lookup"><span data-stu-id="24b92-106">Transitions create seques from one track or compositionsto another.</span></span>

<span data-ttu-id="24b92-107">[DirectShow-Bearbeitungs Dienste](directshow-editing-services.md) verwenden DirectX-Transformations Objekte für Video Übergänge und Video Effekte.</span><span class="sxs-lookup"><span data-stu-id="24b92-107">[DirectShow Editing Services](directshow-editing-services.md) uses DirectX Transform objects for its video transitions and video effects.</span></span> <span data-ttu-id="24b92-108">Verwenden Sie für Video Übergänge ein beliebiges 2-D-DirectX-Transformations Objekt mit zwei Eingaben.</span><span class="sxs-lookup"><span data-stu-id="24b92-108">For video transitions, use any 2-D two-input DirectX Transform object.</span></span> <span data-ttu-id="24b92-109">Verwenden Sie für Video Effekte ein beliebiges 2D-Einzel Eingabe-DirectX-Transformations Objekt.</span><span class="sxs-lookup"><span data-stu-id="24b92-109">For video effects, use any 2-D one-input DirectX Transform object.</span></span> <span data-ttu-id="24b92-110">Microsoft unterstützt die Entwicklung von DirectX-Transformations Objekten von Drittanbietern nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="24b92-110">Microsoft no longer supports the development of third-party DirectX Transform objects.</span></span> <span data-ttu-id="24b92-111">Mit DirectShow werden jedoch mehrere bereitgestellt, und andere werden mit Microsoft Internet Explorer bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="24b92-111">However, several are provided with DirectShow and others are provided with Microsoft Internet Explorer.</span></span> <span data-ttu-id="24b92-112">Weitere Informationen zu den Übergängen, die mit Internet Explorer bereitgestellt werden, finden Sie unter [visuelle Filter und Übergänge-Referenz](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms532853(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="24b92-112">For more information about the transitions provided with Internet Explorer, see [Visual Filters and Transitions Reference](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms532853(v=vs.85)).</span></span>

<span data-ttu-id="24b92-113">Für Audioeffekte können Sie einen beliebigen DirectShow-Audioeffekt-Filter verwenden.</span><span class="sxs-lookup"><span data-stu-id="24b92-113">For audio effects, you can use any DirectShow audio effect filter.</span></span> <span data-ttu-id="24b92-114">Der stellt außerdem einen [volumeumschlags Effekt](volume-envelope-effect.md) für das Festlegen des Volumes auf einem Track-oder Clip-Wert bereit.</span><span class="sxs-lookup"><span data-stu-id="24b92-114">DES also provides a [Volume Envelope Effect](volume-envelope-effect.md) for setting the volume on a track or clip.</span></span> <span data-ttu-id="24b92-115">DES unterstützt keine audioübergänge.</span><span class="sxs-lookup"><span data-stu-id="24b92-115">DES does not support audio transitions.</span></span>

<span data-ttu-id="24b92-116">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="24b92-116">This section contains the following topics:</span></span>

-   [<span data-ttu-id="24b92-117">Hinzufügen von Effekt-und Übergangs Objekten</span><span class="sxs-lookup"><span data-stu-id="24b92-117">Adding Effect and Transition Objects</span></span>](adding-effect-and-transition-objects.md)
-   [<span data-ttu-id="24b92-118">Vorschau von Effekten und Übergängen</span><span class="sxs-lookup"><span data-stu-id="24b92-118">Previewing Effects and Transitions</span></span>](previewing-effects-and-transitions.md)
-   [<span data-ttu-id="24b92-119">Aufzählen von Effekten und Übergängen</span><span class="sxs-lookup"><span data-stu-id="24b92-119">Enumerating Effects and Transitions</span></span>](enumerating-effects-and-transitions.md)
-   [<span data-ttu-id="24b92-120">Festlegen von Eigenschaften für Effekte und Übergänge</span><span class="sxs-lookup"><span data-stu-id="24b92-120">Setting Properties on Effects and Transitions</span></span>](setting-properties-on-effects-and-transitions.md)
-   [<span data-ttu-id="24b92-121">Übergangs Richtung</span><span class="sxs-lookup"><span data-stu-id="24b92-121">Transition Direction</span></span>](transition-direction.md)

## <a name="related-topics"></a><span data-ttu-id="24b92-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="24b92-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24b92-123">Verwenden von DirectShow-Bearbeitungs Diensten</span><span class="sxs-lookup"><span data-stu-id="24b92-123">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 
