---
description: Im folgenden finden Sie die imagehlp-Funktionen.
ms.assetid: 926f412e-25ba-4f9c-a118-b5a1bc723379
title: Imagehlp-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16e921707474f68e288f67e84dda9e361922bca0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958503"
---
# <a name="imagehlp-functions"></a><span data-ttu-id="05e8f-103">Imagehlp-Funktionen</span><span class="sxs-lookup"><span data-stu-id="05e8f-103">ImageHlp Functions</span></span>

<span data-ttu-id="05e8f-104">Im folgenden finden Sie die imagehlp-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="05e8f-104">The following are the ImageHlp functions.</span></span>

## <a name="image-access"></a><span data-ttu-id="05e8f-105">Bildzugriff</span><span class="sxs-lookup"><span data-stu-id="05e8f-105">Image Access</span></span>

<span data-ttu-id="05e8f-106">Die Bild Zugriffs Funktionen greifen auf die Daten in einem ausführbaren Image zu.</span><span class="sxs-lookup"><span data-stu-id="05e8f-106">The image access functions access the data in an executable image.</span></span> <span data-ttu-id="05e8f-107">Die-Funktionen bieten Zugriff auf hoher Ebene auf die Basis von Bildern und einen sehr spezifischen Zugriff auf die gängigsten Teile der Daten eines Bilds.</span><span class="sxs-lookup"><span data-stu-id="05e8f-107">The functions provide high-level access to the base of images and very specific access to the most common parts of an image's data.</span></span>

<dl>

[<span data-ttu-id="05e8f-108">**Getimageconfiginformation**</span><span class="sxs-lookup"><span data-stu-id="05e8f-108">**GetImageConfigInformation**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-getimageconfiginformation)  
[<span data-ttu-id="05e8f-109">**Getimageunusedheaderbytes**</span><span class="sxs-lookup"><span data-stu-id="05e8f-109">**GetImageUnusedHeaderBytes**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-getimageunusedheaderbytes)  
[<span data-ttu-id="05e8f-110">**ImageLoad**</span><span class="sxs-lookup"><span data-stu-id="05e8f-110">**ImageLoad**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageload)  
[<span data-ttu-id="05e8f-111">**Image entladen**</span><span class="sxs-lookup"><span data-stu-id="05e8f-111">**ImageUnload**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageunload)  
[<span data-ttu-id="05e8f-112">**Mapandload**</span><span class="sxs-lookup"><span data-stu-id="05e8f-112">**MapAndLoad**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-mapandload)  
[<span data-ttu-id="05e8f-113">**"Contimageconfiginformation"**</span><span class="sxs-lookup"><span data-stu-id="05e8f-113">**SetImageConfigInformation**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-setimageconfiginformation)  
[<span data-ttu-id="05e8f-114">**Fehler bei unmapandload**</span><span class="sxs-lookup"><span data-stu-id="05e8f-114">**UnMapAndLoad**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-unmapandload)  
</dl>

## <a name="image-integrity"></a><span data-ttu-id="05e8f-115">Bildintegrität</span><span class="sxs-lookup"><span data-stu-id="05e8f-115">Image Integrity</span></span>

<span data-ttu-id="05e8f-116">Die Bild Integritäts Funktionen verwalten den Satz von Zertifikaten in einer Bilddatei.</span><span class="sxs-lookup"><span data-stu-id="05e8f-116">The image integrity functions manage the set of certificates in an image file.</span></span>

<dl>

[<span data-ttu-id="05e8f-117">**Digestfunction**</span><span class="sxs-lookup"><span data-stu-id="05e8f-117">**DigestFunction**</span></span>](/windows/desktop/api/Imagehlp/nc-imagehlp-digest_function)  
[<span data-ttu-id="05e8f-118">**Imageaddcertificate**</span><span class="sxs-lookup"><span data-stu-id="05e8f-118">**ImageAddCertificate**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageaddcertificate)  
[<span data-ttu-id="05e8f-119">**Imageenumeratecertificates**</span><span class="sxs-lookup"><span data-stu-id="05e8f-119">**ImageEnumerateCertificates**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageenumeratecertificates)  
[<span data-ttu-id="05e8f-120">**Imagegetcertificatedata**</span><span class="sxs-lookup"><span data-stu-id="05e8f-120">**ImageGetCertificateData**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificatedata)  
[<span data-ttu-id="05e8f-121">**Imagegetcertifialisieheader**</span><span class="sxs-lookup"><span data-stu-id="05e8f-121">**ImageGetCertificateHeader**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificateheader)  
[<span data-ttu-id="05e8f-122">**Imagegetdigeststream**</span><span class="sxs-lookup"><span data-stu-id="05e8f-122">**ImageGetDigestStream**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetdigeststream)  
[<span data-ttu-id="05e8f-123">**Imageremovecertificate**</span><span class="sxs-lookup"><span data-stu-id="05e8f-123">**ImageRemoveCertificate**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageremovecertificate)  
</dl>

## <a name="image-modification"></a><span data-ttu-id="05e8f-124">Bild Änderung</span><span class="sxs-lookup"><span data-stu-id="05e8f-124">Image Modification</span></span>

<span data-ttu-id="05e8f-125">Mit den Funktionen für die Bild Änderung können Sie das ausführbare Image ändern.</span><span class="sxs-lookup"><span data-stu-id="05e8f-125">The image modification functions allow you to change the executable image.</span></span>

<dl>

[<span data-ttu-id="05e8f-126">**BindImage**</span><span class="sxs-lookup"><span data-stu-id="05e8f-126">**BindImage**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-bindimage)  
[<span data-ttu-id="05e8f-127">**BindImageEx**</span><span class="sxs-lookup"><span data-stu-id="05e8f-127">**BindImageEx**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-bindimageex)  
[<span data-ttu-id="05e8f-128">**CheckSumMappedFile**</span><span class="sxs-lookup"><span data-stu-id="05e8f-128">**CheckSumMappedFile**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-checksummappedfile)  
[<span data-ttu-id="05e8f-129">**Mapfileandchecksum**</span><span class="sxs-lookup"><span data-stu-id="05e8f-129">**MapFileAndCheckSum**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-mapfileandchecksuma)  
[<span data-ttu-id="05e8f-130">**Rebaseimage**</span><span class="sxs-lookup"><span data-stu-id="05e8f-130">**ReBaseImage**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-rebaseimage)  
[<span data-ttu-id="05e8f-131">**ReBaseImage64**</span><span class="sxs-lookup"><span data-stu-id="05e8f-131">**ReBaseImage64**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-rebaseimage64)  
[<span data-ttu-id="05e8f-132">**Splitsymbols**</span><span class="sxs-lookup"><span data-stu-id="05e8f-132">**SplitSymbols**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-splitsymbols)  
[<span data-ttu-id="05e8f-133">**Status Routine**</span><span class="sxs-lookup"><span data-stu-id="05e8f-133">**StatusRoutine**</span></span>](/windows/desktop/api/Imagehlp/nc-imagehlp-pimagehlp_status_routine)  
[<span data-ttu-id="05e8f-134">**Touchfiletimes**</span><span class="sxs-lookup"><span data-stu-id="05e8f-134">**TouchFileTimes**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-touchfiletimes)  
[<span data-ttu-id="05e8f-135">**Updatedebuginfofile**</span><span class="sxs-lookup"><span data-stu-id="05e8f-135">**UpdateDebugInfoFile**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-updatedebuginfofile)  
[<span data-ttu-id="05e8f-136">**Updatedebuginfofileex**</span><span class="sxs-lookup"><span data-stu-id="05e8f-136">**UpdateDebugInfoFileEx**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-updatedebuginfofileex)  
</dl>

 

 



