---
description: In Windows 7 implementieren allgemeine Plattform-APIs, die kernaudio-APIs wie Media Foundation-, DirectSound-und Wave-APIs verwenden, das streamrouting-Feature, indem Sie den Datenstrom Wechsel von einem vorhandenen Gerät zu einem neuen standardaudioendpunkt verarbeiten.
ms.assetid: 4f36710c-c5a8-4f31-9b77-5253475c0715
title: Der Geräte Endpunkt für das streamrouting wird erhalten.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed8c7546c2bd7437ed9705dc93c2a736bbb64e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861207"
---
# <a name="getting-the-device-endpoint-for-stream-routing"></a><span data-ttu-id="04bd0-103">Der Geräte Endpunkt für das streamrouting wird erhalten.</span><span class="sxs-lookup"><span data-stu-id="04bd0-103">Getting the Device Endpoint for Stream Routing</span></span>

<span data-ttu-id="04bd0-104">In Windows 7 implementieren allgemeine Plattform-APIs, die kernaudio-APIs wie Media Foundation-, DirectSound-und Wave-APIs verwenden, das streamrouting-Feature, indem Sie den Datenstrom Wechsel von einem vorhandenen Gerät zu einem neuen standardaudioendpunkt verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="04bd0-104">In Windows 7, high-level platform APIs that use Core Audio APIs such as Media Foundation, DirectSound, and Wave APIs, implement the stream routing feature by handling stream switching from an existing device to a new default audio endpoint.</span></span> <span data-ttu-id="04bd0-105">Medienanwendungen, die diese APIs verwenden (z. b. eine Anwendung, die ein **idirectsound** -oder **ibasefilter** -Objekt auf einem [**immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) -Objekt aktiviert), verwenden das Datenstrom-Routing Verhalten ohne Änderungen an der Quelle.</span><span class="sxs-lookup"><span data-stu-id="04bd0-105">Media applications that use these APIs (for example, an application activating an **IDirectSound** or **IBaseFilter** object on an [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) object) use the stream routing behavior without any modifications to the source.</span></span>

<span data-ttu-id="04bd0-106">Die High-Level-APIs implementieren das Datenstrom Routing für den Geräte Endpunkt, der über [**immdeviceenumerator:: getdefaultaudioendpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint)abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="04bd0-106">The high-level APIs implement stream routing for the device endpoint that is obtained through [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span></span> <span data-ttu-id="04bd0-107">Wenn eine Anwendung auf das Standardgerät gestreamt wird, wird die streamweiterleitungs Funktion wie definiert angewendet.</span><span class="sxs-lookup"><span data-stu-id="04bd0-107">If an application streams to the default device, the stream routing feature operates as defined.</span></span> <span data-ttu-id="04bd0-108">Streams werden nicht auf das neue Gerät umgestellt, wenn Sie von einem anderen Mechanismus abgerufen werden, auch wenn Sie mit dem Standardgerät identisch sind.</span><span class="sxs-lookup"><span data-stu-id="04bd0-108">Streams are not switched to the new device if it is retrieved by any other mechanism even if it is the same as the default device.</span></span>

<span data-ttu-id="04bd0-109">Eine Medien Anwendung, die Core-audioapis direkt (WASAPI-Client) verwendet, kann eine benutzerdefinierte streamweiterleitungs-Implementierung für jedes Rendering oder jedes Erfassungsgerät bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="04bd0-109">A media application that uses Core Audio APIs directly (WASAPI client) can provide a custom stream routing implementation for any rendering or capture device.</span></span> <span data-ttu-id="04bd0-110">Ein WASAPI-Client kann die von den APIs auf hoher Ebene bereitgestellte Implementierung replizieren, indem er auf Datenströme beschränkt wird, die auf Geräten geöffnet sind, die als Standardgerät festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="04bd0-110">A WASAPI client can replicate the implemetation provided by the high-level APIs by restricting it to streams that are opened on devices that are set as the default device.</span></span> <span data-ttu-id="04bd0-111">Zum Abrufen eines Verweises auf den Endpunkt des Standard Geräts muss der Client " [**immdeviceenumerator:: getdefaultaudioendpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint)" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="04bd0-111">To get a reference to the default device's endpoint, the client must call [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span></span> <span data-ttu-id="04bd0-112">In diesem-Befehl muss der Client angeben, ob ein Zeiger auf das renderingstandardgerät oder das Erfassungs Standardgerät durch Angabe des *DataFlow* -Parameters erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="04bd0-112">In this call, the client must indicate whether it requires a pointer to the rendering default device or the capture default device by specifying the *dataFlow* parameter.</span></span> <span data-ttu-id="04bd0-113">Der Client muss auch die entsprechende Rolle für den Endpunkt im **erole** -Attribut angeben (**econsole** oder **eCommunications**).</span><span class="sxs-lookup"><span data-stu-id="04bd0-113">The client must also specify the appropriate role for the endpoint in the **ERole** attribute (**eConsole** or **eCommunications**).</span></span> <span data-ttu-id="04bd0-114">Verwenden Sie **emultimedia** nicht.</span><span class="sxs-lookup"><span data-stu-id="04bd0-114">Do not use **eMultimedia**.</span></span>

<span data-ttu-id="04bd0-115">Wenn die Anwendung zu einem beliebigen anderen Gerät streamt, kann die Anwendung das Gerät abrufen, indem eine Endpunkt-ID-Zeichenfolge angegeben wird (durch den Aufruf von [**immdeviceenumerator:: getdevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)).</span><span class="sxs-lookup"><span data-stu-id="04bd0-115">If the application streams to any other device, the application can get the device by specifying an endpoint ID string (by calling [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)).</span></span>

<span data-ttu-id="04bd0-116">Nachdem das Gerät identifiziert wurde, kann der WASAPI-Client die Implementierung für das streamrouting bereitstellen, indem er die Geräte-und audiositzungsbenachrichtigungen verarbeitet, die für das Gerät gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="04bd0-116">After the device is identified, the WASAPI client can provide the implementation for stream routing by handling the device and audio session notifications sent for the device.</span></span> <span data-ttu-id="04bd0-117">Weitere Informationen zu diesen Benachrichtigungen finden Sie unter [relevante Benachrichtigungen für das Datenstrom Routing](relevant-device-notifications-for-stream-routing.md).</span><span class="sxs-lookup"><span data-stu-id="04bd0-117">For more information about these notifications, see [Relevant Notifications for Stream Routing](relevant-device-notifications-for-stream-routing.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="04bd0-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="04bd0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04bd0-119">Informationen über die mmdevice-API</span><span class="sxs-lookup"><span data-stu-id="04bd0-119">About MMDevice API</span></span>](mmdevice-api.md)
</dt> <dt>

[<span data-ttu-id="04bd0-120">Informationen zu WASAPI</span><span class="sxs-lookup"><span data-stu-id="04bd0-120">About WASAPI</span></span>](wasapi.md)
</dt> <dt>

[<span data-ttu-id="04bd0-121">Streamrouting</span><span class="sxs-lookup"><span data-stu-id="04bd0-121">Stream Routing</span></span>](stream-routing.md)
</dt> </dl>

 

 



