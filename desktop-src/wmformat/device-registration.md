---
title: Geräteregistrierung
description: Geräteregistrierung
ms.assetid: 64a6f366-1317-47b6-94a2-ca2ef14d1f88
keywords:
- Windows Media-Format-SDK, Geräteregistrierung
- Windows Media-Format-SDK, Registrierung von Geräten
- Advanced Systems Format (ASF), Geräteregistrierung
- ASF (Advanced Systems Format), Geräteregistrierung
- Advanced Systems Format (ASF), Registrierung von Geräten
- ASF (Advanced Systems Format), Registrierung von Geräten
- Digital Rights Management (DRM), Geräteregistrierung
- DRM (Digital Rights Management), Geräteregistrierung
- Digital Rights Management (DRM), Registrierung von Geräten
- DRM (Digital Rights Management), Registrierung von Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcf4954d9b59abfb62f3a86127a387299d45cb4a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038554"
---
# <a name="device-registration"></a><span data-ttu-id="9ff0a-113">Geräteregistrierung</span><span class="sxs-lookup"><span data-stu-id="9ff0a-113">Device Registration</span></span>

<span data-ttu-id="9ff0a-114">Das Windows Media-Format-SDK ermöglicht den Zugriff auf die Geräte Registrierungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="9ff0a-114">The Windows Media Format SDK provides access to the device registration database.</span></span> <span data-ttu-id="9ff0a-115">Diese Datenbank ist auf dem Client Computer gesichert und wird zum Registrieren von Geräten verwendet, von denen Windows Media DRM 10 für Netzwerkgeräte unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="9ff0a-115">This database is secured on the client computer and is used to register devices that support Windows Media DRM 10 for Network Devices.</span></span>

<span data-ttu-id="9ff0a-116">Wenn ein Gerät zu einem Netzwerk hinzugefügt wird, mit dem der Client Computer verbunden ist, versucht das Gerät, eine Verbindung mit einer Windows Media DRM 10 for Network Devices-Sender Anwendung aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="9ff0a-116">When a device is added to a network to which the client computer is connected, the device attempts to contact a Windows Media DRM 10 for Network Devices transmitter application.</span></span> <span data-ttu-id="9ff0a-117">Nach dem Einrichten der Kommunikation sendet das Gerät eine Registrierungs Anforderungs Nachricht.</span><span class="sxs-lookup"><span data-stu-id="9ff0a-117">After establishing communications, the device sends a registration request message.</span></span>

<span data-ttu-id="9ff0a-118">Die Anwendung sollte die folgenden Schritte ausführen, wenn eine Registrierungs Anforderungs Nachricht empfangen wird:</span><span class="sxs-lookup"><span data-stu-id="9ff0a-118">Your application should perform the following steps when it receives a registration request message:</span></span>

1.  <span data-ttu-id="9ff0a-119">Analysieren Sie die Nachricht, indem Sie die [**iwmdrmmessageparser::P arseregistrationreqmsg**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parseregistrationreqmsg) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9ff0a-119">Parse the message by calling the [**IWMDRMMessageParser::ParseRegistrationReqMsg**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parseregistrationreqmsg) method.</span></span> <span data-ttu-id="9ff0a-120">Diese Methode ruft das Gerätezertifikat und die Seriennummer des Geräts ab, die beide zum Identifizieren des Geräts benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="9ff0a-120">This method retrieves the device certificate and the device serial number, both of which are needed to identify the device.</span></span>
2.  <span data-ttu-id="9ff0a-121">Nennen Sie die [**iwmdeviceregistration:: getregistereddevicebyid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) -Methode, und übergeben Sie das Zertifikat und die Geräteserien Nummer, die Sie in Schritt 1 abgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="9ff0a-121">Call the [**IWMDeviceRegistration::GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) method, passing in the certificate and device serial number retrieved in step 1.</span></span> <span data-ttu-id="9ff0a-122">Wenn das Gerät gefunden wurde, ist es bereits registriert, und Sie können den nächsten Schritt überspringen.</span><span class="sxs-lookup"><span data-stu-id="9ff0a-122">If the device is found, it is already registered and you can skip the next step.</span></span>
3.  <span data-ttu-id="9ff0a-123">Wenden Sie die [**iwmdeviceregistration:: registerdevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-registerdevice) -Methode an, um das Gerät der Geräte Registrierungsdatenbank hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9ff0a-123">Call the [**IWMDeviceRegistration::RegisterDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-registerdevice) method to add the device to the device registration database.</span></span>

<span data-ttu-id="9ff0a-124">Sie können auf Informationen zu jedem Gerät in der Registrierungsdatenbank zugreifen, indem Sie das registrierte Geräte Objekt abrufen, das diesem zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9ff0a-124">You can access information about any device in the registration database by retrieving the registered device object associated with it.</span></span> <span data-ttu-id="9ff0a-125">Es gibt zwei Möglichkeiten, ein registriertes Geräte Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9ff0a-125">There are two ways to get a registered device object.</span></span> <span data-ttu-id="9ff0a-126">Wenn Sie über das Zertifikat und die Seriennummer des Geräts verfügen, können Sie die [**iwmdeviceregistration:: getregistereddevicebyid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9ff0a-126">If you have the certificate and serial number of the device, you can call the [**IWMDeviceRegistration::GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) method.</span></span> <span data-ttu-id="9ff0a-127">Wenn Sie nicht über das Zertifikat und die Seriennummer des Geräts verfügen, können Sie alle Geräte in der Datenbank auflisten, indem Sie [**iwmdeviceregistration:: getfirstregistereddevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getfirstregistereddevice) aufrufen, gefolgt von wiederholten Aufrufen von [**iwmdeviceregistration:: getnextregistereddevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getnextregistereddevice) , bis ein Aufruf S false zurückgibt \_ .</span><span class="sxs-lookup"><span data-stu-id="9ff0a-127">If you do not have the certificate and serial number of the device, you can enumerate all the devices in the database by calling [**IWMDeviceRegistration::GetFirstRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getfirstregistereddevice) followed by repeated calls to [**IWMDeviceRegistration::GetNextRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getnextregistereddevice) until a call returns S\_FALSE.</span></span>

<span data-ttu-id="9ff0a-128">Bevor die Anwendung Daten an ein Gerät senden kann, müssen Sie sicherstellen, dass das Gerät genehmigt, überprüft und geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="9ff0a-128">Before your application can send data to a device, you must ensure that the device is approved, validated, and open.</span></span>

<span data-ttu-id="9ff0a-129">Die Geräte Genehmigung sollte eine Interaktion mit dem Benutzer beinhalten.</span><span class="sxs-lookup"><span data-stu-id="9ff0a-129">Device approval should involve interaction with the user.</span></span> <span data-ttu-id="9ff0a-130">Wenn ein Gerät eine Registrierungsmeldung sendet, kann die Anwendung den Benutzer auffordern, zu entscheiden, ob es sich bei dem Gerät um ein Gerät handelt, das die Daten des Benutzers erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="9ff0a-130">When a device sends a registration message, your application can prompt the user to decide whether the device is one that should receive that user's data.</span></span> <span data-ttu-id="9ff0a-131">Aktualisieren Sie dann die Geräte Registrierungsdatenbank, indem Sie die [**iwmregistereddevice:: genehmigen**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-approve) -Methode aufrufen, und übergeben Sie nach Bedarf **true** oder **false** .</span><span class="sxs-lookup"><span data-stu-id="9ff0a-131">Then update the device registration database by calling the [**IWMRegisteredDevice::Approve**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-approve) method, passing **TRUE** or **FALSE** as appropriate.</span></span>

<span data-ttu-id="9ff0a-132">Die Validierung wird auch als near-Erkennung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9ff0a-132">Validation is also called proximity detection.</span></span> <span data-ttu-id="9ff0a-133">Hierbei handelt es sich um einen Prozess, mit dem die internen DRM-Objekte des Windows Media-SDK ermitteln, ob das Gerät "nah" ist, bis der Computer, auf dem Ihre Anwendung ausgeführt wird, auf sichere Weise Medien überträgt.</span><span class="sxs-lookup"><span data-stu-id="9ff0a-133">This is a process by which the internal DRM objects of the Windows Media Format SDK determine whether the device is "near" enough to the computer running your application to securely transmit media.</span></span> <span data-ttu-id="9ff0a-134">Die Nähe wird durch die Zeit bestimmt, die benötigt wird, um eine Antwort auf eine Nachricht zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9ff0a-134">Nearness is determined by the time it takes to get a response to a message.</span></span> <span data-ttu-id="9ff0a-135">Diese Funktion soll verhindern, dass nicht autorisierte Benutzer auf Ihr Netzwerk zugreifen und Ihre gesicherten Medien erhalten.</span><span class="sxs-lookup"><span data-stu-id="9ff0a-135">This feature is intended to prevent unauthorized users from accessing your network and obtaining your secured media.</span></span> <span data-ttu-id="9ff0a-136">Weitere Informationen finden Sie unter [Durchführen der Near-Erkennung](performing-proximity-detection.md).</span><span class="sxs-lookup"><span data-stu-id="9ff0a-136">For more information, see [Performing Proximity Detection](performing-proximity-detection.md).</span></span>

<span data-ttu-id="9ff0a-137">Um ein Gerät zu öffnen, nennen Sie [**iwmregistereddevice:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open).</span><span class="sxs-lookup"><span data-stu-id="9ff0a-137">To open a device, call [**IWMRegisteredDevice::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open).</span></span>

> [!Note]  
> <span data-ttu-id="9ff0a-138">DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9ff0a-138">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9ff0a-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9ff0a-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ff0a-140">**Iwmregistereddevice**</span><span class="sxs-lookup"><span data-stu-id="9ff0a-140">**IWMRegisteredDevice**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice)
</dt> <dt>

[<span data-ttu-id="9ff0a-141">**Verwenden des Protokolls "Windows Media DRM 10 for Network Devices"**</span><span class="sxs-lookup"><span data-stu-id="9ff0a-141">**Using the Windows Media DRM 10 for Network Devices Protocol**</span></span>](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




