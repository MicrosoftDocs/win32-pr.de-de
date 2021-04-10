---
description: Dmuerum-Beispiel
ms.assetid: afd7853e-b0ab-42f6-8c2e-c2b0b40d989b
title: Dmuerum-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c413b7787ba12785758cffed89be15229373643d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213981"
---
# <a name="dmoenum-sample"></a><span data-ttu-id="8fdfe-103">Dmuerum-Beispiel</span><span class="sxs-lookup"><span data-stu-id="8fdfe-103">DMOEnum Sample</span></span>

## <a name="description"></a><span data-ttu-id="8fdfe-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8fdfe-104">Description</span></span>

<span data-ttu-id="8fdfe-105">In dieser Beispielanwendung werden alle im System des Benutzers registrierten [DirectX Media Objects](directx-media-objects.md) (DMOs) aufgelistet, und es werden Informationen darüber angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8fdfe-105">This sample application enumerates all of the [DirectX Media Objects](directx-media-objects.md) (DMOs) registered in the user's system, and displays information about them.</span></span>

<span data-ttu-id="8fdfe-106">Im Beispiel werden die DMOS mithilfe der [**dmoenum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) -Funktion und der [**ienumdmo**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-ienumdmo) -Schnittstelle aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8fdfe-106">The sample uses the [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function and the [**IEnumDMO**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-ienumdmo) interface to enumerate the DMOs.</span></span> <span data-ttu-id="8fdfe-107">Er verwendet die [**imediaobject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) -Schnittstelle und andere DMO-Schnittstellen zum Abrufen von Informationen zu jedem DMO.</span><span class="sxs-lookup"><span data-stu-id="8fdfe-107">It uses the [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) interface and other DMO interfaces to retrieve information about each DMO.</span></span>

## <a name="usage"></a><span data-ttu-id="8fdfe-108">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="8fdfe-108">Usage</span></span>

<span data-ttu-id="8fdfe-109">Beim Starten der Anwendung werden alle installierten DMOS aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8fdfe-109">When the application launches, it enumerates all of the installed DMOs.</span></span> <span data-ttu-id="8fdfe-110">Wenn Sie eine bestimmte DMO-Kategorie auswählen, werden in der Anwendung nur die DMOS in dieser Kategorie angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8fdfe-110">If you select a specific DMO category, the application displays only the DMOs in that category.</span></span> <span data-ttu-id="8fdfe-111">Wenn Sie Informationen zu einem DMO anzeigen möchten, wählen Sie in der Liste den DMO aus.</span><span class="sxs-lookup"><span data-stu-id="8fdfe-111">To view information about a DMO, select the DMO from the list.</span></span> <span data-ttu-id="8fdfe-112">Die Anwendung zeigt die Anzahl der Streams, die bevorzugten Medientypen, den DLL-Server für den DMO und weitere Informationen zum DMO an.</span><span class="sxs-lookup"><span data-stu-id="8fdfe-112">The application displays the number of streams, the preferred media types, the DLL server for that DMO, and other information about the DMO.</span></span> <span data-ttu-id="8fdfe-113">Wenn Sie verschlüsselte DMOS einschließen oder ausschließen möchten, aktivieren Sie das Kontrollkästchen "Schlüssel **einschließen** ".</span><span class="sxs-lookup"><span data-stu-id="8fdfe-113">To include or exclude keyed DMOs, toggle the **Include Keyed DMOs?** checkbox.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="8fdfe-114">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="8fdfe-114">Downloading the Sample</span></span>

<span data-ttu-id="8fdfe-115">Zum Herunterladen der DirectShow SDK-Beispiele installieren Sie die neueste Version der [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8fdfe-115">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="8fdfe-116">Dieses Beispiel wird unter folgendem Pfad installiert: *\[ SDK Root \]* \\ Samples \\ Multimedia \\ DirectShow \\ misc \\ dmuenum.</span><span class="sxs-lookup"><span data-stu-id="8fdfe-116">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Misc\\DMOEnum.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8fdfe-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8fdfe-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fdfe-118">DirectShow-Beispiele</span><span class="sxs-lookup"><span data-stu-id="8fdfe-118">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



