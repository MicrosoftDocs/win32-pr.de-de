---
description: Dialog Felder zur VFW-Erfassung anzeigen
ms.assetid: 708212ca-d148-4079-8052-3bf6696a33ab
title: Dialog Felder zur VFW-Erfassung anzeigen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45b8b51b164630a8fa6e91b2e68ca8a9a3a875b6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745649"
---
# <a name="display-vfw-capture-dialog-boxes"></a><span data-ttu-id="1f381-103">Dialog Felder zur VFW-Erfassung anzeigen</span><span class="sxs-lookup"><span data-stu-id="1f381-103">Display VFW Capture Dialog Boxes</span></span>

<span data-ttu-id="1f381-104">Ein Erfassungsgerät, das weiterhin einen VFW-Treiber (Video for Windows) verwendet, kann eines der folgenden drei Dialogfelder unterstützen, die zum Konfigurieren des Geräts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1f381-104">A capture device that still uses a Video for Windows (VFW) driver can support any of the following three dialog boxes, which are used to configure the device.</span></span>



| <span data-ttu-id="1f381-105">Dialogfeld</span><span class="sxs-lookup"><span data-stu-id="1f381-105">Dialog box</span></span>    | <span data-ttu-id="1f381-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1f381-106">Description</span></span>                                                                                           |
|---------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f381-107">Video Quelle</span><span class="sxs-lookup"><span data-stu-id="1f381-107">Video Source</span></span>  | <span data-ttu-id="1f381-108">Wird verwendet, um die Videoeingabe auszuwählen und Geräteeinstellungen wie Bildhelligkeit oder Kontrast anzupassen.</span><span class="sxs-lookup"><span data-stu-id="1f381-108">Used to select the video input and to adjust device settings, such as picture brightness or contrast.</span></span> |
| <span data-ttu-id="1f381-109">Video Format</span><span class="sxs-lookup"><span data-stu-id="1f381-109">Video Format</span></span>  | <span data-ttu-id="1f381-110">Wird verwendet, um die Bild Dimensionen und die Bittiefe auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="1f381-110">Used to select the image dimensions and bit depth.</span></span>                                                    |
| <span data-ttu-id="1f381-111">Video Anzeige</span><span class="sxs-lookup"><span data-stu-id="1f381-111">Video Display</span></span> | <span data-ttu-id="1f381-112">Wird verwendet, um die Darstellung des gerenderten Videos zu steuern.</span><span class="sxs-lookup"><span data-stu-id="1f381-112">Used to control the appearance of the rendered video.</span></span>                                                 |



 

<span data-ttu-id="1f381-113">Gehen Sie folgendermaßen vor, um eines dieser Dialogfelder anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="1f381-113">To show one of these dialog boxes, do the following:</span></span>

1.  <span data-ttu-id="1f381-114">Stoppt das Filter Diagramm.</span><span class="sxs-lookup"><span data-stu-id="1f381-114">Stop the filter graph.</span></span>
2.  <span data-ttu-id="1f381-115">Fragen Sie den Erfassungs Filter nach der [**iamvfwcapturedialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="1f381-115">Query the capture filter for the [**IAMVfwCaptureDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs) interface.</span></span> <span data-ttu-id="1f381-116">Wenn **QueryInterface** erfolgreich ist, bedeutet dies, dass das Erfassungsgerät ein VFW-Gerät ist.</span><span class="sxs-lookup"><span data-stu-id="1f381-116">If **QueryInterface** succeeds, it means the capture device is a VFW device.</span></span>
3.  <span data-ttu-id="1f381-117">Aufrufen von [**iamvfwcapturedialoge:: hasdialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-hasdialog) zum Überprüfen, ob der Treiber das Dialogfeld unterstützt, das Sie anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="1f381-117">Call [**IAMVfwCaptureDialogs::HasDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-hasdialog) to check if the driver supports the dialog box that you wish to display.</span></span> <span data-ttu-id="1f381-118">Die [**vfwcapturedialogs**](/windows/desktop/api/strmif/ne-strmif-vfwcapturedialogs) -Enumeration definiert Flags für jedes der Vfw-Dialogfelder.</span><span class="sxs-lookup"><span data-stu-id="1f381-118">The [**VfwCaptureDialogs**](/windows/desktop/api/strmif/ne-strmif-vfwcapturedialogs) enumeration defines flags for each of the VFW dialog boxes.</span></span> <span data-ttu-id="1f381-119">**Hasdialog** gibt S \_ OK zurück, wenn das Dialogfeld unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="1f381-119">**HasDialog** returns S\_OK if the dialog box is supported.</span></span> <span data-ttu-id="1f381-120">Andernfalls wird ' false ' zurückgegeben \_ . Überprüfen Sie, ob der Wert ' ' \_ OK ist, anstatt das Makro ' **erfolgreich** ' zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1f381-120">It returns S\_FALSE otherwise, so check for the value S\_OK directly, rather than using the **SUCCEEDED** macro.</span></span>
4.  <span data-ttu-id="1f381-121">Wenn das Dialogfeld unterstützt wird, müssen Sie [**iamvfwcapturedialoge:: ShowDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-showdialog) aufrufen, um das Dialogfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1f381-121">If the dialog box is supported, call [**IAMVfwCaptureDialogs::ShowDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-showdialog) to display the dialog box.</span></span>
5.  <span data-ttu-id="1f381-122">Starten Sie das Diagramm neu.</span><span class="sxs-lookup"><span data-stu-id="1f381-122">Restart the graph.</span></span>

<span data-ttu-id="1f381-123">Der folgende Code zeigt die folgenden Schritte für das Dialogfeld Video Quelle:</span><span class="sxs-lookup"><span data-stu-id="1f381-123">The following code shows these steps for the Video Source dialog box:</span></span>


```C++
pControl->Stop(); // Stop the graph.

// Query the capture filter for the IAMVfwCaptureDialogs interface.
IAMVfwCaptureDialogs *pVfw = 0;
hr = pCap->QueryInterface(IID_IAMVfwCaptureDialogs, (void**)&pVfw);
if (SUCCEEDED(hr))
{
    // Check if the device supports this dialog box.
    if (S_OK == pVfw->HasDialog(VfwCaptureDialog_Source))
    {
        // Show the dialog box.
        hr = pVfw->ShowDialog(VfwCaptureDialog_Source, hwndParent);
    }
}
pControl->Run();
```



## <a name="related-topics"></a><span data-ttu-id="1f381-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1f381-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f381-125">Konfigurieren eines Video Erfassungs Geräts</span><span class="sxs-lookup"><span data-stu-id="1f381-125">Configuring a Video Capture Device</span></span>](configuring-a-video-capture-device.md)
</dt> </dl>

 

 



