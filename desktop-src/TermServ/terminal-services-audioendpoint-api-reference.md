---
title: Remotedesktopdienste audioendpoint-API-Referenz
description: Unterstützt Schnittstellen für die audioendpunkt Registrierung und den Datentransport.
ms.assetid: 0e3ea0e7-8c61-400e-b8ef-8a0403aedafa
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste Remotedesktopdienste, audioendpoint-API-Referenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1958b21643083a14110ddad77f68024cc464dd36
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388559"
---
# <a name="remote-desktop-services-audioendpoint-api-reference"></a><span data-ttu-id="9d870-104">Remotedesktopdienste audioendpoint-API-Referenz</span><span class="sxs-lookup"><span data-stu-id="9d870-104">Remote Desktop Services AudioEndpoint API reference</span></span>

<span data-ttu-id="9d870-105">Ein *audioendpunkt* stellt ein Audiogerät, eine audioapi oder eine beliebige andere Audioquelle oder-Senke dar und wird verwendet, um Daten an die Audioengine zu senden oder Sie zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="9d870-105">An *audio endpoint* represents an audio device, audio API, or any other audio source or sink, and is used to send data to or consume data from the audio engine.</span></span> <span data-ttu-id="9d870-106">Ein audioendpunkt muss über eine *Verbindung* mit dem Audiomodul verbunden sein, und jede Verbindung kann nur einen Endpunkt haben.</span><span class="sxs-lookup"><span data-stu-id="9d870-106">An audio endpoint must be connected to the audio engine through a *connection*, and each connection can have only one endpoint connected to it.</span></span> <span data-ttu-id="9d870-107">Nachdem ein Endpunkt registriert wurde, fügt die Audioengine den Endpunkt an die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="9d870-107">After an endpoint is registered, the audio engine attaches the endpoint to the connection.</span></span>

<span data-ttu-id="9d870-108">Jedes Endpunkt Objekt muss die folgenden Schnittstellen implementieren:</span><span class="sxs-lookup"><span data-stu-id="9d870-108">Each endpoint object must implement the following interfaces:</span></span>

-   <span data-ttu-id="9d870-109">[**Iaudioendpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint) , um dem Audiomodul zu ermöglichen, Informationen zum Endpunkt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9d870-109">[**IAudioEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint) to enable the audio engine to get information about the endpoint.</span></span>
-   <span data-ttu-id="9d870-110">[**Iaudioendpointrt**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt) , um Informationen über den Datenpuffer zu erhalten, bevor ein Verarbeitungs Durchlauf durchgeführt und der Endpunkt benachrichtigt wird, wenn der Durchlauf abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="9d870-110">[**IAudioEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt) to get information about the data buffer before performing a processing pass and notifying the endpoint when the pass is complete.</span></span>
-   <span data-ttu-id="9d870-111">Entweder die [**iaudioinputendpointrt**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt) -oder die [**iaudiooutputendpointrt**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) -Schnittstelle, abhängig davon, ob das Endpunkt Objekt Audiodaten erfasst oder rendert.</span><span class="sxs-lookup"><span data-stu-id="9d870-111">Either the [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt) or [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) interface, depending on whether the endpoint object is capturing or rendering audio.</span></span>
-   [<span data-ttu-id="9d870-112">**Iaudiodeviceendpoint**</span><span class="sxs-lookup"><span data-stu-id="9d870-112">**IAudioDeviceEndpoint**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
-   [<span data-ttu-id="9d870-113">**Iaudioendpointcontrol**</span><span class="sxs-lookup"><span data-stu-id="9d870-113">**IAudioEndpointControl**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)

<span data-ttu-id="9d870-114">Die Audioengine verwendet diese Schnittstellen, um Informationen zu den Endpunkten zu erhalten, die an die Engine angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="9d870-114">The audio engine uses these interfaces to get information about the endpoints that are attached to the engine.</span></span> <span data-ttu-id="9d870-115">Die Endpunkt Implementierung muss den Mechanismus bereitstellen, mit dem Daten an die Engine übertragen werden können, wie von diesen Schnittstellen angegeben.</span><span class="sxs-lookup"><span data-stu-id="9d870-115">The endpoint implementation must provide the mechanism to deliver data to or consume data from the engine as specified by these interfaces.</span></span>

<span data-ttu-id="9d870-116">Die Remotedesktopdienste audioendpoint-API unterstützt Enumerationstypen, Schnittstellen und Strukturen.</span><span class="sxs-lookup"><span data-stu-id="9d870-116">The Remote Desktop Services AudioEndpoint API supports enumeration types, interfaces, and structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9d870-117">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="9d870-117">In this section</span></span>

-   [<span data-ttu-id="9d870-118">Remotedesktopdienste audioendpoint-Enumerationstypen</span><span class="sxs-lookup"><span data-stu-id="9d870-118">Remote Desktop Services AudioEndpoint Enumeration Types</span></span>](terminal-services-audioendpoint-enumeration-types.md)
-   [<span data-ttu-id="9d870-119">Remotedesktopdienste audioendpoint-Funktionen</span><span class="sxs-lookup"><span data-stu-id="9d870-119">Remote Desktop Services AudioEndpoint Functions</span></span>](remote-desktop-services-audioendpoint-functions.md)
-   [<span data-ttu-id="9d870-120">Remotedesktopdienste audioendpoint-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="9d870-120">Remote Desktop Services AudioEndpoint Interfaces</span></span>](terminal-services-audioendpoint-interfaces.md)
-   [<span data-ttu-id="9d870-121">Remotedesktopdienste audioendpoint-Strukturen</span><span class="sxs-lookup"><span data-stu-id="9d870-121">Remote Desktop Services AudioEndpoint Structures</span></span>](terminal-services-audioendpoint-structures.md)

## <a name="remarks"></a><span data-ttu-id="9d870-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d870-122">Remarks</span></span>

<span data-ttu-id="9d870-123">Die Remotedesktopdienste audioendpoint-API ist für die Verwendung in Remotedesktop Szenarien vorgesehen. Es handelt sich nicht um Client Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="9d870-123">The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.</span></span>

 

 




