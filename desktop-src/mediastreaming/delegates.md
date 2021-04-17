---
title: Delegaten
description: Die Media Streaming-API stellt die folgenden Ereignishandlerfunktionen bereit.
ms.assetid: CDE7B829-D0D1-479D-9B35-4445E711AF58
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23fbf0f44a0822fd0c8914833b0696fcb9aacad
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516742"
---
# <a name="delegates"></a><span data-ttu-id="5825f-103">Delegaten</span><span class="sxs-lookup"><span data-stu-id="5825f-103">Delegates</span></span>

<span data-ttu-id="5825f-104">Die [Media Streaming-API](media-streaming-api-portal.md) stellt die folgenden Ereignishandlerfunktionen bereit.</span><span class="sxs-lookup"><span data-stu-id="5825f-104">The [Media Streaming API](media-streaming-api-portal.md) provides the following event handler functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5825f-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="5825f-105">In this section</span></span>



| <span data-ttu-id="5825f-106">Thema</span><span class="sxs-lookup"><span data-stu-id="5825f-106">Topic</span></span>                                                                                   | <span data-ttu-id="5825f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5825f-107">Description</span></span>                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5825f-108">[**Connectionstatushandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5825f-108">[**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85))</span></span><br/>                   | <span data-ttu-id="5825f-109">Stellt die Funktion dar, die das [**connectionstatuschangi-Ereignis**](connectionstatuschanged.md) behandelt, mit dem der Client über Änderungen im Netzwerk Verbindungsstatus des Geräts benachrichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="5825f-109">Represents the function that will handle the [**ConnectionStatusChanged**](connectionstatuschanged.md) event which notifies the client of changes in the device s network connection status.</span></span><br/>               |
| <span data-ttu-id="5825f-110">[**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5825f-110">[**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85))</span></span><br/>       | <span data-ttu-id="5825f-111">Stellt die Funktion dar, die die [**devicearrival**](devicearrival.md) -und [**devicedeparture**](devicedeparture.md) -Ereignisse behandelt, die den Client über Änderungen in der Liste der zwischengespeicherten Geräte benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="5825f-111">Represents the function that will handle the [**DeviceArrival**](devicearrival.md) and [**DeviceDeparture**](devicedeparture.md) events which notify the client of changes in the list of cached devices.</span></span><br/> |
| <span data-ttu-id="5825f-112">[**Renderingparametersupdatehandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5825f-112">[**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85))</span></span><br/> | <span data-ttu-id="5825f-113">Stellt die Funktion dar, die das [**renderingparametersupdate**](renderingparametersupdate.md) -Ereignis behandelt, das den Client über ein Update für einen der DMR-renderingsteuerungsparameter benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="5825f-113">Represents the function that will handle the [**RenderingParametersUpdate**](renderingparametersupdate.md) event which notifies the client of an update to any of the DMR s rendering control parameters.</span></span><br/>  |
| <span data-ttu-id="5825f-114">[**Transportparametersupdatehandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5825f-114">[**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85))</span></span><br/> | <span data-ttu-id="5825f-115">Stellt die Funktion dar, die das [**transportparametersupdate**](transportparametersupdate.md) -Ereignis behandelt, das den Client über ein Update der DMR-Transport Parameter benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="5825f-115">Represents the function that will handle the [**TransportParametersUpdate**](transportparametersupdate.md) event which notifies the client of an update to any of the DMR s transport parameters.</span></span><br/>          |



 

 

