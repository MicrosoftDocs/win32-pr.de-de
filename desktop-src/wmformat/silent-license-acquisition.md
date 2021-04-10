---
title: Automatische Lizenz Beschaffung
description: Automatische Lizenz Beschaffung
ms.assetid: bf88f1bb-0cbb-4c30-92e0-3d342977d67f
keywords:
- Windows Media-Format-SDK, automatische Lizenz Beschaffung
- Windows Media-Format-SDK, Lizenzen
- Digital Rights Management (DRM), automatische Lizenz Beschaffung
- DRM (Digital Rights Management), automatische Lizenz Beschaffung
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Erweiterte APIs für den DRM-Client, automatische Lizenz Beschaffung
- Erweiterte Client-APIs, automatische Lizenz Beschaffung
- Automatische Lizenz Beschaffung
- Lizenzen, automatische Lizenz Beschaffung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ef92eaf4e347e8eb30f56c1111ec5b27f1e62d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037250"
---
# <a name="silent-license-acquisition"></a><span data-ttu-id="8eecc-113">Automatische Lizenz Beschaffung</span><span class="sxs-lookup"><span data-stu-id="8eecc-113">Silent License Acquisition</span></span>

<span data-ttu-id="8eecc-114">Der automatische Erwerb von Lizenzen erfordert nur einen einzigen Methoden Aufrufs, der die gesamte Netzwerkkommunikation mit dem Lizenzserver asynchron verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="8eecc-114">Silent license acquisition requires only a single method call that handles all of the network communications with the license server asynchronously.</span></span>

<span data-ttu-id="8eecc-115">Diese Art der Lizenz Erfassung wird normalerweise als Antwort an den Endbenutzer verwendet, der versucht, auf geschützte Inhalte zuzugreifen – beispielsweise, wenn versucht wird, eine geschützte Datei in einer Media Player-Anwendung wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="8eecc-115">This type of license acquisition is usually used as a response to the end user trying to access protected content—for example, trying to play a protected file in a media player application.</span></span> <span data-ttu-id="8eecc-116">Da der automatische Lizenzerwerb die Lizenz mit einem einzigen-Befehl erhält, kann er nicht verwendet werden, wenn zusätzliche Benutzereingaben, z. b. die Zahlung für den Inhalt, erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="8eecc-116">Because silent license acquisition gets the license with a single call, it cannot be used if additional input from the user, such as payment for the content, is required.</span></span>

<span data-ttu-id="8eecc-117">Führen Sie die folgenden Schritte aus, um eine automatische Lizenz Erfassung durchzuführen:</span><span class="sxs-lookup"><span data-stu-id="8eecc-117">To perform silent license acquisition, use the following steps:</span></span>

1.  <span data-ttu-id="8eecc-118">Nennen Sie die [**iwmdrmlicenabmanagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="8eecc-118">Call the [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) method.</span></span> <span data-ttu-id="8eecc-119">Übergeben Sie den DRM-Header aus der geschützten Datei als *bstrinheaderdata* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="8eecc-119">Pass in the DRM header from the protected file as the *bstrHeaderData* parameter.</span></span> <span data-ttu-id="8eecc-120">Geben Sie an, welche Rechte von der Lizenz im *bstractions* -Parameter erteilt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8eecc-120">Specify what rights you want the license to grant in the *bstrActions* parameter.</span></span> <span data-ttu-id="8eecc-121">Legen Sie schließlich den *dwFlags* -Parameter auf "WMDRM-Lizenz abrufen" automatisch fest \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8eecc-121">Finally, set the *dwFlags* parameter to WMDRM\_ACQUIRE\_LICENSE\_SILENT.</span></span>
2.  <span data-ttu-id="8eecc-122">Trap Ereignisse für die [**iwmdrmlicentsmanagement**](iwmdrmlicensemanagement.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8eecc-122">Trap events for the [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) interface.</span></span> <span data-ttu-id="8eecc-123">Wenn Sie das **mewmdrmlicenseacquisitionabgeschlossene** -Ereignis empfangen, überprüfen Sie seinen Rückgabecode, indem Sie die **imfmediaevent:: GetStatus** -Methode aufrufen, die in der Media Foundation-Dokumentation dokumentiert ist.</span><span class="sxs-lookup"><span data-stu-id="8eecc-123">When you receive the **MEWMDRMLicenseAcquisitionCompleted** event, check its return code by calling the **IMFMediaEvent::GetStatus** method, which is documented in the Media Foundation documentation.</span></span> <span data-ttu-id="8eecc-124">Wenn der abgerufene **HRESULT** -Wert ein Erfolgs Code ist, wurde die Lizenz erfolgreich heruntergeladen und befindet sich im lokalen Lizenz Speicher, der verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8eecc-124">If the retrieved **HRESULT** value is a success code, then the license was successfully downloaded and is in the local license store ready for use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8eecc-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8eecc-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8eecc-126">**Erwerben von Lizenzen**</span><span class="sxs-lookup"><span data-stu-id="8eecc-126">**Acquiring Licenses**</span></span>](acquiring-licenses.md)
</dt> <dt>

[<span data-ttu-id="8eecc-127">**Verwenden des Media Foundation-Ereignis Modells**</span><span class="sxs-lookup"><span data-stu-id="8eecc-127">**Using the Media Foundation Event Model**</span></span>](using-the-media-foundation-model.md)
</dt> </dl>

 

 




