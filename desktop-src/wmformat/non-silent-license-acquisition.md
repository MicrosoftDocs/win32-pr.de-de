---
title: Nicht automatische Lizenz Beschaffung
description: Nicht automatische Lizenz Beschaffung
ms.assetid: 3b3fce53-9202-4e55-82d5-7c70ea833087
keywords:
- Windows Media-Format-SDK, nicht automatischer Lizenzerwerb
- Windows Media-Format-SDK, Lizenzen
- Digital Rights Management (DRM), nicht automatische Lizenz Beschaffung
- DRM (Digital Rights Management), nicht automatische Lizenz Beschaffung
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Erweiterte APIs für den DRM-Client, nicht automatische Lizenz Beschaffung
- Erweiterte Client-APIs, nicht automatische Lizenz Beschaffung
- nicht automatische Lizenz Beschaffung
- Lizenzen, nicht automatische Lizenz Beschaffung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb8d7c4865e74fd5ce383cff8317de905828afe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516058"
---
# <a name="non-silent-license-acquisition"></a><span data-ttu-id="93ed9-113">Nicht automatische Lizenz Beschaffung</span><span class="sxs-lookup"><span data-stu-id="93ed9-113">Non-Silent License Acquisition</span></span>

<span data-ttu-id="93ed9-114">Der nicht automatische Lizenz Abruf ermöglicht dem Lizenz Anbieter die Interaktion mit dem Endbenutzer über eine Webseite als Zwischenschritt im Lizenz Erwerbs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="93ed9-114">Non-silent license acquisition enables the license provider to interact with the end user through a Web page, as an intermediate step in the license acquisition process.</span></span> <span data-ttu-id="93ed9-115">Der nicht automatische Lizenzerwerb wird als Reaktion auf einen Benutzer initiiert, der versucht, auf geschützte Inhalte zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="93ed9-115">Non-silent license acquisition is initiated in response to a user trying to access protected content.</span></span>

<span data-ttu-id="93ed9-116">Führen Sie die folgenden Schritte aus, um einen nicht automatischen Lizenzerwerb durchzuführen:</span><span class="sxs-lookup"><span data-stu-id="93ed9-116">To perform non-silent license acquisition, use the following steps:</span></span>

1.  <span data-ttu-id="93ed9-117">Nennen Sie die [**iwmdrmlicenabmanagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="93ed9-117">Call the [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) method.</span></span> <span data-ttu-id="93ed9-118">Übergeben Sie den DRM-Header aus der geschützten Datei als *bstrinheaderdata* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="93ed9-118">Pass in the DRM header from the protected file as the *bstrHeaderData* parameter.</span></span> <span data-ttu-id="93ed9-119">Geben Sie an, welche Rechte von der Lizenz im *bstractions* -Parameter erteilt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="93ed9-119">Specify what rights you want the license to grant in the *bstrActions* parameter.</span></span> <span data-ttu-id="93ed9-120">Legen Sie abschließend den *dwFlags* -Parameter auf "WMDRM-Lizenz abrufen" nicht automatisch fest \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="93ed9-120">Finally, set the *dwFlags* parameter to WMDRM\_ACQUIRE\_LICENSE\_NONSILENT.</span></span>
2.  <span data-ttu-id="93ed9-121">Trap Ereignisse für die **iwmdrmlicentsmanagement** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="93ed9-121">Trap events for the **IWMDRMLicenseManagement** interface.</span></span> <span data-ttu-id="93ed9-122">Wenn Sie das **mewmdrmlicenabacquisitionabgeschlossene** -Ereignis empfangen, rufen Sie den zugehörigen Wert durch Aufrufen von **imfmediaevent:: GetValue** ab.</span><span class="sxs-lookup"><span data-stu-id="93ed9-122">When you receive the **MEWMDRMLicenseAcquisitionCompleted** event, get its associated value by calling **IMFMediaEvent::GetValue**.</span></span> <span data-ttu-id="93ed9-123">Der Wert muss vom Typ "VT \_ unknown" sein, einem Zeiger auf eine **IUnknown** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="93ed9-123">The value should be of type VT\_UNKNOWN, a pointer to an **IUnknown** interface.</span></span>
3.  <span data-ttu-id="93ed9-124">Nennen Sie die **QueryInterface** -Methode der **IUnknown** -Schnittstelle, die Sie in Schritt 2 abgerufen haben, um die [**iwmdrmnonsilentlicenseaquisition**](iwmdrmnonsilentlicenseaquisition.md) -Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="93ed9-124">Call the **QueryInterface** method of the **IUnknown** interface retrieved in step 2 to get the [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) interface.</span></span>
4.  <span data-ttu-id="93ed9-125">Rufen Sie [**iwmdrmnonsilentlicenseaquisition:: getchallenge**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) auf, um die Lizenz Herausforderung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="93ed9-125">Call [**IWMDRMNonSilentLicenseAquisition::GetChallenge**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) to retrieve the license challenge.</span></span> <span data-ttu-id="93ed9-126">Nennen Sie auch [**iwmdrmnonsilentlicenseaquisition:: getURL**](iwmdrmnonsilentlicenseaquisition-geturl.md) , wenn Sie nicht bereits über die URL des Lizenzservers verfügen.</span><span class="sxs-lookup"><span data-stu-id="93ed9-126">Also call [**IWMDRMNonSilentLicenseAquisition::GetURL**](iwmdrmnonsilentlicenseaquisition-geturl.md) if you do not have the URL of the license server already.</span></span>
5.  <span data-ttu-id="93ed9-127">Sendet die Abfrage an die durch die URL angegebene Webseite.</span><span class="sxs-lookup"><span data-stu-id="93ed9-127">Send the challenge to the Web page specified by the URL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93ed9-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="93ed9-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93ed9-129">**Erwerben von Lizenzen**</span><span class="sxs-lookup"><span data-stu-id="93ed9-129">**Acquiring Licenses**</span></span>](acquiring-licenses.md)
</dt> <dt>

[<span data-ttu-id="93ed9-130">**Verwenden des Media Foundation-Ereignis Modells**</span><span class="sxs-lookup"><span data-stu-id="93ed9-130">**Using the Media Foundation Event Model**</span></span>](using-the-media-foundation-model.md)
</dt> </dl>

 

 




