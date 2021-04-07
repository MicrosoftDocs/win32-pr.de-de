---
description: In diesem Thema wird beschrieben, wie eine Anwendung das Bild und die Kameraeinstellungen auf einem Video Erfassungsgerät Programm gesteuert ändern kann.
ms.assetid: f789db78-292e-4092-a5dc-1906845fb1dd
title: Konfigurieren der Video Qualität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cb8d2d28e39f0083aac521f1953ebbb1ca8d5b6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746056"
---
# <a name="configure-the-video-quality"></a><span data-ttu-id="b2315-103">Konfigurieren der Video Qualität</span><span class="sxs-lookup"><span data-stu-id="b2315-103">Configure the Video Quality</span></span>

<span data-ttu-id="b2315-104">In diesem Thema wird beschrieben, wie eine Anwendung das Bild und die Kameraeinstellungen auf einem Video Erfassungsgerät Programm gesteuert ändern kann.</span><span class="sxs-lookup"><span data-stu-id="b2315-104">This topic describes how an application can programmatically change the image and camera settings on a video capture device.</span></span>

-   [<span data-ttu-id="b2315-105">ProcAmp-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b2315-105">ProcAmp Settings</span></span>](#procamp-settings)
-   [<span data-ttu-id="b2315-106">Kameraeinstellungen</span><span class="sxs-lookup"><span data-stu-id="b2315-106">Camera Settings</span></span>](#camera-settings)
-   [<span data-ttu-id="b2315-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b2315-107">Related topics</span></span>](#related-topics)

## <a name="procamp-settings"></a><span data-ttu-id="b2315-108">ProcAmp-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b2315-108">ProcAmp Settings</span></span>

<span data-ttu-id="b2315-109">WDM-Videokameras (Windows-Treibermodell) können Eigenschaften unterstützen, die die Qualität des Bilds Steuern:</span><span class="sxs-lookup"><span data-stu-id="b2315-109">Windows Driver Model (WDM) video cameras can support properties that control the quality of the image:</span></span>

-   <span data-ttu-id="b2315-110">Backlight-Kompensierung</span><span class="sxs-lookup"><span data-stu-id="b2315-110">Backlight compensation</span></span>
-   <span data-ttu-id="b2315-111">Brightness</span><span class="sxs-lookup"><span data-stu-id="b2315-111">Brightness</span></span>
-   <span data-ttu-id="b2315-112">Vergleichen Sie</span><span class="sxs-lookup"><span data-stu-id="b2315-112">Contrast</span></span>
-   <span data-ttu-id="b2315-113">Erzielen</span><span class="sxs-lookup"><span data-stu-id="b2315-113">Gain</span></span>
-   <span data-ttu-id="b2315-114">Gamma</span><span class="sxs-lookup"><span data-stu-id="b2315-114">Gamma</span></span>
-   <span data-ttu-id="b2315-115">Farbton</span><span class="sxs-lookup"><span data-stu-id="b2315-115">Hue</span></span>
-   <span data-ttu-id="b2315-116">Sättigung</span><span class="sxs-lookup"><span data-stu-id="b2315-116">Saturation</span></span>
-   <span data-ttu-id="b2315-117">Schärfe</span><span class="sxs-lookup"><span data-stu-id="b2315-117">Sharpness</span></span>
-   <span data-ttu-id="b2315-118">Weißabgleich</span><span class="sxs-lookup"><span data-stu-id="b2315-118">White balance</span></span>

<span data-ttu-id="b2315-119">Diese Eigenschaften werden über die [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) -Schnittstelle gesteuert.</span><span class="sxs-lookup"><span data-stu-id="b2315-119">These properties are controlled through the [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) interface.</span></span> <span data-ttu-id="b2315-120">Verwenden Sie diese Schnittstelle wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b2315-120">Use this interface as follows:</span></span>

1.  <span data-ttu-id="b2315-121">Aufrufen von [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für den Erfassungs Filter für die [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b2315-121">Call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the capture filter for the [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) interface.</span></span>
2.  <span data-ttu-id="b2315-122">Aufrufen Sie für jede Eigenschaft, die Sie festlegen möchten, die [**IAMVideoProcAmp:: GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b2315-122">For each property that you want to set, call the [**IAMVideoProcAmp::GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) method.</span></span> <span data-ttu-id="b2315-123">Eigenschaften werden von der [**videoprocampproperty**](/windows/win32/api/strmif/ne-strmif-videoprocampproperty) -Enumeration angegeben.</span><span class="sxs-lookup"><span data-stu-id="b2315-123">Properties are specified by the [**VideoProcAmpProperty**](/windows/win32/api/strmif/ne-strmif-videoprocampproperty) enumeration.</span></span> <span data-ttu-id="b2315-124">Wenn die **GetRange** -Methode fehlschlägt, bedeutet dies, dass die Kamera diese bestimmte Eigenschaft nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b2315-124">If the **GetRange** method fails, it means the camera does not support that particular property.</span></span>
3.  <span data-ttu-id="b2315-125">Wenn [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) erfolgreich ist, wird der Bereich der unterstützten Werte für die Eigenschaft, den Standardwert und das minimale Inkrement zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b2315-125">If [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) succeeds, it returns the range of supported values for the property, the default value, and the minimum increment.</span></span>
4.  <span data-ttu-id="b2315-126">Um den aktuellen Wert einer Eigenschaft abzurufen, nennen Sie [**IAMVideoProcAmp:: Get**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-get).</span><span class="sxs-lookup"><span data-stu-id="b2315-126">To get the current value of a property, call [**IAMVideoProcAmp::Get**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-get).</span></span>
5.  <span data-ttu-id="b2315-127">Um eine Eigenschaft festzulegen, müssen Sie die [**IAMVideoProcAmp:: Set**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-set) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b2315-127">To set a property, call the [**IAMVideoProcAmp::Set**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-set) method.</span></span> <span data-ttu-id="b2315-128">Um eine Eigenschaft auf ihren Standardwert wiederherzustellen, müssen Sie [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) aufrufen, um den Standardwert zu ermitteln und diesen Wert an die **set** -Methode zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="b2315-128">To restore a property to its default value, call [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) to find the default and pass that value to the **Set** method.</span></span>

<span data-ttu-id="b2315-129">Sie müssen das Filter Diagramm nicht beenden, wenn Sie die Eigenschaften festlegen.</span><span class="sxs-lookup"><span data-stu-id="b2315-129">You do not have to stop the filter graph when you set the properties.</span></span>

<span data-ttu-id="b2315-130">Mit dem folgenden Code wird ein TrackBar-Steuerelement so konfiguriert, dass es zum Festlegen der Helligkeit verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b2315-130">The following code configures a trackbar control so that it can be used to set the brightness.</span></span> <span data-ttu-id="b2315-131">Der Bereich der TrackBar entspricht dem Gültigkeitsbereich, der vom Gerät unterstützt wird, und die Position der TrackBar entspricht der Einstellung für die anfängliche Helligkeit des Geräts.</span><span class="sxs-lookup"><span data-stu-id="b2315-131">The range of the trackbar corresponds to the brightness range that the device supports, and position of the trackbar corresponds to the device's initial brightness setting.</span></span>


```C++
HWND hTrackbar; // Handle to the trackbar control. 
// Initialize hTrackbar (not shown).

// Query the capture filter for the IAMVideoProcAmp interface.
IAMVideoProcAmp *pProcAmp = 0;
hr = pCap->QueryInterface(IID_IAMVideoProcAmp, (void**)&pProcAmp);
if (FAILED(hr))
{
    // The device does not support IAMVideoProcAmp, so disable the control.
    EnableWindow(hTrackbar, FALSE);
}
else
{
    long Min, Max, Step, Default, Flags, Val;

    // Get the range and default value. 
    hr = m_pProcAmp->GetRange(VideoProcAmp_Brightness, &Min, &Max, &Step,
        &Default, &Flags);
    if (SUCCEEDED(hr))
    {
        // Get the current value.
        hr = m_pProcAmp->Get(VideoProcAmp_Brightness, &Val, &Flags);
    }
    if (SUCCEEDED(hr))
    {
        // Set the trackbar range and position.
        SendMessage(hTrackbar, TBM_SETRANGE, TRUE, MAKELONG(Min, Max));
        SendMessage(hTrackbar, TBM_SETPOS, TRUE, Val);
        EnableWindow(hTrackbar, TRUE);
    }
    else
    {
        // This property is not supported, so disable the control.
        EnableWindow(hTrackbar, FALSE);
    }
}
```



## <a name="camera-settings"></a><span data-ttu-id="b2315-132">Kameraeinstellungen</span><span class="sxs-lookup"><span data-stu-id="b2315-132">Camera Settings</span></span>

<span data-ttu-id="b2315-133">Die [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) -Schnittstelle ähnelt [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp), steuert jedoch verschiedene Einstellungen auf der Kamera selbst:</span><span class="sxs-lookup"><span data-stu-id="b2315-133">The [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) interface is similar to [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp), but controls various setttings on the camera itself:</span></span>

-   <span data-ttu-id="b2315-134">Belichtung</span><span class="sxs-lookup"><span data-stu-id="b2315-134">Exposure</span></span>
-   <span data-ttu-id="b2315-135">Fokus</span><span class="sxs-lookup"><span data-stu-id="b2315-135">Focus</span></span>
-   <span data-ttu-id="b2315-136">Iris</span><span class="sxs-lookup"><span data-stu-id="b2315-136">Iris</span></span>
-   <span data-ttu-id="b2315-137">Schwenken</span><span class="sxs-lookup"><span data-stu-id="b2315-137">Pan</span></span>
-   <span data-ttu-id="b2315-138">N</span><span class="sxs-lookup"><span data-stu-id="b2315-138">Roll</span></span>
-   <span data-ttu-id="b2315-139">Til</span><span class="sxs-lookup"><span data-stu-id="b2315-139">Tilt</span></span>
-   <span data-ttu-id="b2315-140">Zoom</span><span class="sxs-lookup"><span data-stu-id="b2315-140">Zoom</span></span>

<span data-ttu-id="b2315-141">Um diese Schnittstelle zu verwenden, führen Sie dieselben Schritte aus, die für [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="b2315-141">To use this interface, follow the same steps used for [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp):</span></span>

1.  <span data-ttu-id="b2315-142">Fragen Sie den Erfassungs Filter nach [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol)ab.</span><span class="sxs-lookup"><span data-stu-id="b2315-142">Query the capture filter for the [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol).</span></span>
2.  <span data-ttu-id="b2315-143">Aufrufen von [**IAMCameraControl:: GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-getrange) , um zu ermitteln, welche Einstellungen unterstützt werden, und den möglichen Bereich für jede Einstellung.</span><span class="sxs-lookup"><span data-stu-id="b2315-143">Call [**IAMCameraControl::GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-getrange) to find which settings are supported, and the possible range for each settings.</span></span>
3.  <span data-ttu-id="b2315-144">Ruft [**IAMCameraControl:: Get**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-get) auf, um den aktuellen Wert einer Einstellung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b2315-144">Call [**IAMCameraControl::Get**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-get) to get the current value of a setting.</span></span>
4.  <span data-ttu-id="b2315-145">Nennen Sie [**IAMCameraControl:: Set**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-set) , um den Wert festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b2315-145">Call [**IAMCameraControl::Set**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-set) to set the value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2315-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b2315-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2315-147">Konfigurieren eines Video Erfassungs Geräts</span><span class="sxs-lookup"><span data-stu-id="b2315-147">Configuring a Video Capture Device</span></span>](configuring-a-video-capture-device.md)
</dt> </dl>

 

 
