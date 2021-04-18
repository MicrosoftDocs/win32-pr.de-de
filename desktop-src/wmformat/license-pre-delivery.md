---
title: Vorab Bereitstellung von Lizenzen
description: Vorab Bereitstellung von Lizenzen
ms.assetid: 184d9118-5b60-4871-a1e3-75c45153460d
keywords:
- Windows Media-Format-SDK, vorab Bereitstellung von Lizenzen
- Windows Media-Format-SDK, Lizenzen
- Digital Rights Management (DRM), vorab Bereitstellung von Lizenzen
- DRM (Digital Rights Management), vorab Bereitstellung von Lizenzen
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Erweiterte APIs für den DRM-Client, vorab Bereitstellung von Lizenzen
- Erweiterte Client-APIs, vorab Bereitstellung von Lizenzen
- vorab Bereitstellung von Lizenzen
- Lizenzen, vorab Bereitstellung von Lizenzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7691c48233ed986d85c47ae9c99df078d0ed1039
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337667"
---
# <a name="license-pre-delivery"></a><span data-ttu-id="b575c-113">Vorab Bereitstellung von Lizenzen</span><span class="sxs-lookup"><span data-stu-id="b575c-113">License Pre-Delivery</span></span>

<span data-ttu-id="b575c-114">Die vorab Bereitstellung der Lizenz ist der Prozess, der zum vorzeitigen Abrufen von Lizenzen an einen Client Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b575c-114">License pre-delivery is the process used to pull licenses to a client computer preemptively.</span></span> <span data-ttu-id="b575c-115">Ein häufiges Szenario für die Verwendung der vorab Bereitstellung ist, wenn ein Benutzer einen Musikdienst abonniert.</span><span class="sxs-lookup"><span data-stu-id="b575c-115">A common scenario for using pre-delivery is when a user subscribes to a music service.</span></span> <span data-ttu-id="b575c-116">Wenn Sie keine Lizenzen bereitstellen, bevor Sie benötigt werden, muss der Benutzer auf den Lizenzerwerb für jeden neuen Song warten.</span><span class="sxs-lookup"><span data-stu-id="b575c-116">Without delivering licenses before they are needed, the user would have to wait for license acquisition for each new song.</span></span>

<span data-ttu-id="b575c-117">Da die vorab Bereitstellung nicht als Antwort auf den versuchten Zugriff erfolgt, wird Sie in der Regel nur vom Besitzer des Inhalts ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b575c-117">Because pre-delivery is not done as a response to attempted access, it is typically performed only by the content owner.</span></span> <span data-ttu-id="b575c-118">Das heißt, Sie können nur Lizenzen für den von Ihnen kontrollierten Inhalt vorab übermitteln.</span><span class="sxs-lookup"><span data-stu-id="b575c-118">That is, you can only pre-deliver licenses for content that you control.</span></span> <span data-ttu-id="b575c-119">Der Prozess vor der Übermittlung ist eine Koordination zwischen einer Client Komponente und einem Lizenzserver, der mithilfe der Objekte des Windows Media Digital Rights Management SDK erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b575c-119">The pre-delivery process is a coordination between a client component and a license server built by using the objects of the Windows Media Digital Rights Management SDK.</span></span>

<span data-ttu-id="b575c-120">Die vorab Bereitstellung von Lizenzen ähnelt der [nicht automatischen Lizenz Erfassung](non-silent-license-acquisition.md).</span><span class="sxs-lookup"><span data-stu-id="b575c-120">License pre-delivery is similar to [Non-Silent License Acquisition](non-silent-license-acquisition.md).</span></span> <span data-ttu-id="b575c-121">Führen Sie dieselben Schritte aus, mit dem Unterschied, dass Sie nicht über einen DRM-Header verfügen, der an [**iwmdrmlicenabmanagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md)übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="b575c-121">Follow the same steps, except that you don't have a DRM header to pass to [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md).</span></span> <span data-ttu-id="b575c-122">Die-Methode generiert eine Herausforderung, die nicht inhaltsspezifisch ist, die Sie an Ihren Lizenzserver senden können.</span><span class="sxs-lookup"><span data-stu-id="b575c-122">The method will generate a challenge that is not content-specific that you can send to your license server.</span></span>

<span data-ttu-id="b575c-123">Alternativ können Sie den [Windows Media Rights Manager](/previous-versions//bb676133(v=technet.10)) zum vorab übermitteln von Lizenzen verwenden.</span><span class="sxs-lookup"><span data-stu-id="b575c-123">Alternatively you can use the [Windows Media Rights Manager](/previous-versions//bb676133(v=technet.10)) to pre-deliver licenses.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b575c-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b575c-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b575c-125">**Erwerben von Lizenzen**</span><span class="sxs-lookup"><span data-stu-id="b575c-125">**Acquiring Licenses**</span></span>](acquiring-licenses.md)
</dt> <dt>

[<span data-ttu-id="b575c-126">**Verwenden des Media Foundation-Ereignis Modells**</span><span class="sxs-lookup"><span data-stu-id="b575c-126">**Using the Media Foundation Event Model**</span></span>](using-the-media-foundation-model.md)
</dt> </dl>

 

 