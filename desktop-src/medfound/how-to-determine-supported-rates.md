---
description: Bestimmen der unterstützten Tarife
ms.assetid: 7f2b64e1-1062-4f77-b8e0-62b6d962ae8b
title: Bestimmen der unterstützten Tarife
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f67e9753604f51e85c641e616e8b69944b96618
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214964"
---
# <a name="how-to-determine-supported-rates"></a><span data-ttu-id="1d706-103">Bestimmen der unterstützten Tarife</span><span class="sxs-lookup"><span data-stu-id="1d706-103">How to Determine Supported Rates</span></span>

<span data-ttu-id="1d706-104">Vor dem Ändern der Wiedergabe Rate sollte eine Anwendung überprüfen, ob die Wiedergabe Rate von den Objekten in der Pipeline unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="1d706-104">Before changing the playback rate, an application should check whether the playback rate is supported by the objects in the pipeline.</span></span> <span data-ttu-id="1d706-105">Die [**imfresupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) -Schnittstelle stellt Methoden zum erzielen der maximalen Forward-und Reverse-Raten, die unterstützte Rate, die der angeforderten Rate am nächsten liegt, und die langsamste Rate bereit.</span><span class="sxs-lookup"><span data-stu-id="1d706-105">The [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) interface provides methods to get the maximum forward and reverse rates, the supported rate nearest to a requested rate, and the slowest rate.</span></span> <span data-ttu-id="1d706-106">Jede dieser Raten Abfragen kann die Wiedergabe Richtung angeben und angeben, ob die Verdünnung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1d706-106">Each of these rate queries can specify the playback direction and whether to use thinning.</span></span> <span data-ttu-id="1d706-107">Die genaue Wiedergabe Rate wird mithilfe der [**imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) -Schnittstelle abgefragt.</span><span class="sxs-lookup"><span data-stu-id="1d706-107">The exact playback rate is queried by using the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interface.</span></span>

<span data-ttu-id="1d706-108">Weitere Informationen zum Ändern der Wiedergabe Raten finden [Sie unter Festlegen der Wiedergabe Rate für die Medien Sitzung](how-to-set-the-playback-rate-on-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="1d706-108">For information about changing playback rates, see [How to Set the Playback Rate on the Media Session](how-to-set-the-playback-rate-on-the-media-session.md).</span></span>

<span data-ttu-id="1d706-109">Allgemeine Informationen zu den Wiedergabe Raten finden Sie unter [Informationen zur Raten Kontrolle](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="1d706-109">For general information about playback rates, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="to-determine-the-current-playback-rate"></a><span data-ttu-id="1d706-110">So bestimmen Sie die aktuelle Wiedergabe Rate</span><span class="sxs-lookup"><span data-stu-id="1d706-110">To determine the current playback rate</span></span>

1.  <span data-ttu-id="1d706-111">Holen Sie sich den Raten Steuerungs Dienst aus der Medien Sitzung.</span><span class="sxs-lookup"><span data-stu-id="1d706-111">Get the rate control service from the Media Session.</span></span>

    ```C++
    IMFRateControl *pRateControl = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateControl, 
           (void**) &pRateControl );
    ```

    

    <span data-ttu-id="1d706-112">Übergeben Sie einen initialisierten [**imfmediasession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) -Schnittstellen Zeiger im *punkObject* -Parameter von [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span><span class="sxs-lookup"><span data-stu-id="1d706-112">Pass an initialized [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface pointer in the *punkObject* parameter of [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span></span>

    <span data-ttu-id="1d706-113">Die Anwendung muss den Raten Steuerungs Dienst über die Medien Sitzung Abfragen.</span><span class="sxs-lookup"><span data-stu-id="1d706-113">The application must query for the rate control service through the Media Session.</span></span> <span data-ttu-id="1d706-114">Intern fragt die Medien Sitzung die Objekte in der Topologie ab.</span><span class="sxs-lookup"><span data-stu-id="1d706-114">Internally, the Media Session queries the objects in the topology.</span></span>

2.  <span data-ttu-id="1d706-115">Ruft die [**imfratecontrol:: getrate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) -Methode auf, um die aktuelle Wiedergabe Rate zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1d706-115">Call the [**IMFRateControl::GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) method to get the current playback rate.</span></span>

    ```C++
    hr = pRateControl->GetRate(&bThin, &rate);
    ```

    

    <span data-ttu-id="1d706-116">Der *pfthin* -Parameter von [**getrate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) empfängt einen **booleschen** Wert, der angibt, ob der Stream gerade schlank ist.</span><span class="sxs-lookup"><span data-stu-id="1d706-116">The *pfThin* parameter of [**GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) receives a **BOOL** value that indicates whether the stream is currently being thinned.</span></span> <span data-ttu-id="1d706-117">Die Anwendung muss **null** übergeben, wenn Sie keine Unterstützung für die Unterstützung des Datenstroms Abfragen möchte.</span><span class="sxs-lookup"><span data-stu-id="1d706-117">The application must pass **NULL** if it does not want to query thinning support for the stream.</span></span> <span data-ttu-id="1d706-118">Der *pflrate* -Parameter empfängt die aktuelle Wiedergabe Rate.</span><span class="sxs-lookup"><span data-stu-id="1d706-118">The *pflRate* parameter receives the current playback rate.</span></span>

## <a name="to-determine-the-nearest-supported-rate"></a><span data-ttu-id="1d706-119">So bestimmen Sie die nächstgelegene unterstützte Rate</span><span class="sxs-lookup"><span data-stu-id="1d706-119">To determine the nearest supported rate</span></span>

1.  <span data-ttu-id="1d706-120">Holen Sie sich den Dienst zur Gebühren Unterstützung aus der Medien Sitzung.</span><span class="sxs-lookup"><span data-stu-id="1d706-120">Get the rate support service from the Media Session.</span></span>

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    <span data-ttu-id="1d706-121">Übergeben Sie einen initialisierten [**imfmediasession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) -Schnittstellen Zeiger im *punkObject* -Parameter von [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span><span class="sxs-lookup"><span data-stu-id="1d706-121">Pass an initialized [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface pointer in the *punkObject* parameter of [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span></span>

2.  <span data-ttu-id="1d706-122">Rufen Sie die [**imfratesupport:: isratesupportiert**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) -Methode auf, um die unterstützte Rate abzurufen, die der angeforderten Wiedergabe Rate am nächsten liegt.</span><span class="sxs-lookup"><span data-stu-id="1d706-122">Call the [**IMFRateSupport::IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) method to retrieve the supported rate nearest to a requested playback rate.</span></span>

    ```C++
    float rateRequested = 4.0;
    float actualRate = 0;
    hr = pRateSupport->IsRateSupported(
           TRUE, 
           rateRequested, 
           &actualRate );
    ```

    

    <span data-ttu-id="1d706-123">Im Beispiel wird abgefragt, ob eine Wiedergabe Rate von 4,0 bei der Verdünnung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="1d706-123">The example queries whether a playback rate of 4.0 is supported with thinning.</span></span> <span data-ttu-id="1d706-124">Dies wird durch Übergeben von " **true** " im Parameter " *f* " von [**isratesupportiert**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported)angegeben.</span><span class="sxs-lookup"><span data-stu-id="1d706-124">This is indicated by passing **TRUE** in the *fThin* parameter of [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported).</span></span> <span data-ttu-id="1d706-125">Wenn diese Rate unterstützt wird, enthält *actualrate* die Wiedergabe Rate 4,0, und der-Befehl wird mit dem Rückgabewert S \_ OK erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1d706-125">If this rate is supported, *actualRate* contains the playback rate of 4.0, and the call succeeds with a return value of S\_OK.</span></span> <span data-ttu-id="1d706-126">Wenn die genaue Wiedergabe Rate nicht unterstützt wird, wird die nächste unterstützte Rate in *actualrate* empfangen.</span><span class="sxs-lookup"><span data-stu-id="1d706-126">If the exact playback rate is not supported, the nearest supported rate is received in *actualRate*.</span></span> <span data-ttu-id="1d706-127">Wenn die Rate nicht unterstützt wird und keine verfügbare nächste Wiedergabe Rate verfügbar ist, gibt der-Rückruf einen entsprechenden Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="1d706-127">If the rate is not supported and there is no available nearest playback rate, the call returns an appropriate error code.</span></span>

    <span data-ttu-id="1d706-128">Diese Werte können sich abhängig davon ändern, welche Pipeline Komponenten geladen werden.</span><span class="sxs-lookup"><span data-stu-id="1d706-128">These values can change depending on which pipeline components are loaded.</span></span> <span data-ttu-id="1d706-129">Daher sollten Sie die Werte erneut Abfragen, wenn Sie eine neue topolgy laden.</span><span class="sxs-lookup"><span data-stu-id="1d706-129">Therefore, you should query the values again whenever you load a new topololgy.</span></span>

    <span data-ttu-id="1d706-130">Wenn die gewünschte Wiedergabe Rate nicht unterstützt wird, besteht eine Möglichkeit darin, jedes Objekt in der Topologie einzeln abzufragen, um herauszufinden, ob eine bestimmte Komponente die Rate nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1d706-130">If the desired playback rate is not supported, one option is to query each object in the topology individually, to find out if a particular component does not support the rate.</span></span> <span data-ttu-id="1d706-131">Möglicherweise sind Sie in der Lage, die Topologie ohne diese Komponente neu zu erstellen und dann die gewünschte Rate zu spielen.</span><span class="sxs-lookup"><span data-stu-id="1d706-131">You might be able to rebuild the topology without this component and then play at the desired rate.</span></span> <span data-ttu-id="1d706-132">Wenn z. b. jede Komponente außer dem audiorenderer eine bestimmte Rate unterstützt, können Sie die Topologie ohne den audiobranch neu erstellen und ohne Audiodaten mit der gewünschten Geschwindigkeit wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="1d706-132">For example, if every component except the audio renderer supports a given rate, you could rebuild the topology without the audio branch and play at the desired rate without audio.</span></span>

## <a name="to-determine-the-slowest-supported-rate"></a><span data-ttu-id="1d706-133">So bestimmen Sie die langsamste unterstützte Rate</span><span class="sxs-lookup"><span data-stu-id="1d706-133">To determine the slowest supported rate</span></span>

1.  <span data-ttu-id="1d706-134">Holen Sie sich den Dienst zur Gebühren Unterstützung aus der Medien Sitzung.</span><span class="sxs-lookup"><span data-stu-id="1d706-134">Get the rate support service from the Media Session.</span></span>

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    <span data-ttu-id="1d706-135">Übergeben Sie einen initialisierten [**imfmediasession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) -Schnittstellen Zeiger im *punkObject* -Parameter von [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span><span class="sxs-lookup"><span data-stu-id="1d706-135">Pass an initialized [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface pointer in the *punkObject* parameter of [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span></span>

2.  <span data-ttu-id="1d706-136">Rufen Sie die [**imfratesupport:: gezlowestrate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate) -Methode auf, um die langsamste unterstützte Rate abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1d706-136">Call the [**IMFRateSupport::GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate) method to retrieve the slowest supported rate.</span></span>

    ```C++
    float slowestRate = 0;
    hr = pRateSupport->GetSlowestRate(
           MFRATE_REVERSE, 
           TRUE, 
           &slowestRate);
    ```

    

    <span data-ttu-id="1d706-137">Im Beispiel wird die langsamste umgekehrte Wiedergabe Rate bei der Verdünnung abgefragt.</span><span class="sxs-lookup"><span data-stu-id="1d706-137">The example queries for the slowest reverse playback rate with thinning.</span></span> <span data-ttu-id="1d706-138">Die untere Grenze wird im *slowestrate* -Parameter von [**gesorlowestrate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate)empfangen.</span><span class="sxs-lookup"><span data-stu-id="1d706-138">The lower bound rate is received in *slowestRate* parameter of [**GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate).</span></span>

    <span data-ttu-id="1d706-139">Wenn die umgekehrte Wiedergabe oder die Verdünnung nicht unterstützt wird, gibt der-Rückruf einen entsprechenden Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="1d706-139">If reverse playback or thinning is not supported, the call returns an appropriate error code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d706-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1d706-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d706-141">Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="1d706-141">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="1d706-142">Raten Steuerung</span><span class="sxs-lookup"><span data-stu-id="1d706-142">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="1d706-143">Suchen, schnelles vorwärts und umgekehrtes spielen</span><span class="sxs-lookup"><span data-stu-id="1d706-143">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



