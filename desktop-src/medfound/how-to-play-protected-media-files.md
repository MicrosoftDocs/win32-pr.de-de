---
description: Abspielen von Dateien, die von DRM geschützte Medien enthalten.
ms.assetid: 85d98f49-8af2-42ce-9b36-a025aee93f73
title: Wiedergeben geschützter Mediendateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f8f7af78881e43f2f7f85e8f333ab31b1bc2de
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106364288"
---
# <a name="how-to-play-protected-media-files"></a><span data-ttu-id="776af-103">Wiedergeben geschützter Mediendateien</span><span class="sxs-lookup"><span data-stu-id="776af-103">How to Play Protected Media Files</span></span>

<span data-ttu-id="776af-104">Eine geschützte Mediendatei ist eine beliebige Mediendatei, der Regeln für die Verwendung des Inhalts zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="776af-104">A protected media file is any media file that has associated rules for using the content.</span></span> <span data-ttu-id="776af-105">In einigen Fällen wird eine geschützte Mediendatei in Form der Digital Rights Management Verschlüsselung (DRM) verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="776af-105">In some cases, a protected media file is encrypted using some form of digital rights management (DRM) encryption.</span></span> <span data-ttu-id="776af-106">Zum Wiedergeben einer geschützten Mediendatei muss die Wiedergabe im geschützten Medien Pfad (PMP) erfolgen.</span><span class="sxs-lookup"><span data-stu-id="776af-106">To play a protected media file, playback must occur inside the protected media path (PMP).</span></span> <span data-ttu-id="776af-107">Außerdem muss der Benutzer möglicherweise Rechte für den Inhalt erhalten.</span><span class="sxs-lookup"><span data-stu-id="776af-107">In addition, the user might have to acquire rights to the content.</span></span>

<span data-ttu-id="776af-108">Der Begriff "Rechte Erfassung" bezieht sich auf jede Aktion, die die Anwendung ausführen muss, bevor der Benutzer den Inhalt wiedergeben kann.</span><span class="sxs-lookup"><span data-stu-id="776af-108">The term rights acquisition refers to any action that the application must perform before the user can play the content.</span></span> <span data-ttu-id="776af-109">Das häufigste Beispiel ist das Abrufen einer DRM-Lizenz, Media Foundation jedoch einen generischen Mechanismus definiert, der andere Arten der Rechte Übernahme unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="776af-109">The most common example is obtaining a DRM license, but Media Foundation defines a generic mechanism that can support other types of rights acquisition.</span></span> <span data-ttu-id="776af-110">Die [**IMF contentenabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) -Schnittstelle definiert diesen generischen Mechanismus.</span><span class="sxs-lookup"><span data-stu-id="776af-110">The [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface defines this generic mechanism.</span></span>

<span data-ttu-id="776af-111">Die Rechte Übernahme muss außerhalb des PMP aus dem Anwendungsprozess erfolgen.</span><span class="sxs-lookup"><span data-stu-id="776af-111">Rights acquisition must be done outside of the PMP, from the application process.</span></span> <span data-ttu-id="776af-112">Die Medien Sitzung benachrichtigt die Anwendung über die [**IMF contentprotection Manager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) -Schnittstelle, die von der Anwendung implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="776af-112">The Media Session notifies the application through the [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface, which is implemented by the application.</span></span> <span data-ttu-id="776af-113">Die Medien Sitzung verwendet die **imfcontentschutzmanager** -Schnittstelle zum Weiterleiten eines inhaltsenabler-Objekts an die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="776af-113">The Media Session uses the **IMFContentProtectionManager** interface to forward a content enabler object to the application.</span></span> <span data-ttu-id="776af-114">Inhalts Enabler implementieren die [**IMF contentenabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="776af-114">Content enablers implement the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface.</span></span> <span data-ttu-id="776af-115">Diese Schnittstelle wird von der Anwendung verwendet, um die erforderlichen Rechte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="776af-115">The application uses this interface to acquire the necessary rights.</span></span>

<span data-ttu-id="776af-116">Ein inhaltsenabler unterstützt möglicherweise die automatische Rechte Erfassung. in diesem Fall implementiert der Inhalts-Wegbereiter den gesamten Prozess, und die Anwendung überwacht einfach den Status.</span><span class="sxs-lookup"><span data-stu-id="776af-116">A content enabler might support automatic rights acquisition, in which case the content enabler implements the entire process, and the application simply monitors the status.</span></span> <span data-ttu-id="776af-117">Andernfalls muss die Anwendung eine nicht automatische Rechte Übernahme verwenden. dabei handelt es sich um einen Prozess, bei dem die Anwendung HTTP Post-Daten an eine vom Inhalts-Enabler bereitgestellte URL sendet.</span><span class="sxs-lookup"><span data-stu-id="776af-117">Otherwise, the application must use non-silent rights acquisition, which is a process where the application sends HTTP POST data to a URL provided by the content enabler.</span></span>

<span data-ttu-id="776af-118">Zum Wiedergeben geschützter Medien befolgt eine Anwendung die gleichen Schritte wie im Thema [Abspielen von Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md)mit den folgenden zusätzlichen Schritten:</span><span class="sxs-lookup"><span data-stu-id="776af-118">To play protected media, an application follows the same steps given in the topic [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md), with the following additional steps:</span></span>

1.  <span data-ttu-id="776af-119">Fragen Sie ab, ob die Medienquelle geschützte Inhalte enthält.</span><span class="sxs-lookup"><span data-stu-id="776af-119">Query whether the media source contains protected content.</span></span> <span data-ttu-id="776af-120">(Optional.)</span><span class="sxs-lookup"><span data-stu-id="776af-120">(Optional.)</span></span>
2.  <span data-ttu-id="776af-121">Erstellen Sie die Medien Sitzung im PMP-Prozess anstelle des Anwendungsprozesses.</span><span class="sxs-lookup"><span data-stu-id="776af-121">Create the Media Session in the PMP process, instead of the application process.</span></span>
3.  <span data-ttu-id="776af-122">Durchführen der Rechte Übernahme, wenn dies von der Medien Sitzung benachrichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="776af-122">Perform rights acquisition, if notified to do so by the Media Session.</span></span> <span data-ttu-id="776af-123">Dieser Vorgang wird asynchron von der Anwendung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="776af-123">This operation is performed asynchronously by the application.</span></span>
4.  <span data-ttu-id="776af-124">Schließen Sie den asynchronen Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="776af-124">Complete the asynchronous operation.</span></span>

## <a name="query-for-protected-content"></a><span data-ttu-id="776af-125">Abfragen geschützter Inhalte</span><span class="sxs-lookup"><span data-stu-id="776af-125">Query for Protected Content</span></span>

<span data-ttu-id="776af-126">Um abzufragen, ob eine Medienquelle geschützte Inhalte enthält, nennen Sie die [**mfrequireprotectedenvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) -Funktion im Präsentations Deskriptor der Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="776af-126">To query whether a media source contains protected content, call the [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) function on the media source's presentation descriptor.</span></span> <span data-ttu-id="776af-127">Wenn die Funktion S OK zurückgibt \_ , müssen Sie den Inhalt mit dem PMP wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="776af-127">If the function returns S\_OK, you must use the PMP to play the content.</span></span> <span data-ttu-id="776af-128">Wenn die Funktion S false zurückgibt \_ , ist das PMP nicht erforderlich, und Sie können die Medien Sitzung im Anwendungsprozess erstellen.</span><span class="sxs-lookup"><span data-stu-id="776af-128">If the function returns S\_FALSE, the PMP is not required, and you can create the Media Session in the application process.</span></span> <span data-ttu-id="776af-129">Alternativ können Sie das PMP verwenden, um beide Arten von Inhalten, geschützt und ungeschützt, wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="776af-129">Alternatively, you can use the PMP to play both types of content, protected and unprotected.</span></span> <span data-ttu-id="776af-130">Wenn Sie dies tun, müssen Sie " **mfrequireprotectedenvironment**" nicht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="776af-130">If you do that, you do not need to call **MFRequireProtectedEnvironment**.</span></span>

<span data-ttu-id="776af-131">Weitere Informationen zu Präsentations Deskriptoren finden Sie unter [Präsentations Deskriptoren](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="776af-131">For more information about presentation descriptors, see [Presentation Descriptors](presentation-descriptors.md).</span></span>

## <a name="create-the-pmp-media-session"></a><span data-ttu-id="776af-132">Erstellen der PMP-Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="776af-132">Create the PMP Media Session</span></span>

<span data-ttu-id="776af-133">Um die Medien Sitzung im PMP zu erstellen, rufen Sie [**mfkreatepmpmediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)auf.</span><span class="sxs-lookup"><span data-stu-id="776af-133">To create the Media Session in the PMP, call [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span></span> <span data-ttu-id="776af-134">Diese Funktion ähnelt [**mfkreatemediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession), aber statt die Medien Sitzung im Prozess der Anwendung zu erstellen, wird die Medien Sitzung im PMP-Prozess erstellt.</span><span class="sxs-lookup"><span data-stu-id="776af-134">This function is similar to [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession), but instead of creating the Media Session in the application's process, it creates the Media Session in the PMP process.</span></span> <span data-ttu-id="776af-135">Die Anwendung empfängt einen Zeiger auf ein Proxy Objekt für die Medien Sitzung.</span><span class="sxs-lookup"><span data-stu-id="776af-135">The application receives a pointer to a proxy object for the Media Session.</span></span> <span data-ttu-id="776af-136">Die Anwendung ruft [**imfmediasession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) -Methoden für das Proxy Objekt auf, ebenso wie in der Medien Sitzung.</span><span class="sxs-lookup"><span data-stu-id="776af-136">The application calls [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) methods on the proxy object, just as it would on the Media Session.</span></span> <span data-ttu-id="776af-137">Das Proxy Objekt leitet die Aufrufe an die Medien Sitzung über die Prozess Grenze weiter.</span><span class="sxs-lookup"><span data-stu-id="776af-137">The proxy object forwards the calls to the Media Session across the process boundary.</span></span>

<span data-ttu-id="776af-138">Erstellen Sie die PMP-Medien Sitzung wie folgt:</span><span class="sxs-lookup"><span data-stu-id="776af-138">Create the PMP Media Session as follows:</span></span>

1.  <span data-ttu-id="776af-139">Erstellen Sie einen neuen Attribut Speicher, indem Sie [**mfcreateattribute**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="776af-139">Create a new attribute store by calling [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span></span>
2.  <span data-ttu-id="776af-140">Legen Sie das Attribut " [**MF \_ Session \_ Content \_ Protection \_ Manager**](mf-session-content-protection-manager-attribute.md) " für den Attribut Speicher fest.</span><span class="sxs-lookup"><span data-stu-id="776af-140">Set the [**MF\_SESSION\_CONTENT\_PROTECTION\_MANAGER**](mf-session-content-protection-manager-attribute.md) attribute on the attribute store.</span></span> <span data-ttu-id="776af-141">Der Wert dieses Attributs ist ein Zeiger auf die Implementierung von [**imfcontentprotection Manager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="776af-141">The value of this attribute is a pointer to your application's implementation of [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager).</span></span> <span data-ttu-id="776af-142">Der Befehl [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) wird aufgerufen, um das Attribut festzulegen.</span><span class="sxs-lookup"><span data-stu-id="776af-142">Call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) to set the attribute.</span></span>
3.  <span data-ttu-id="776af-143">Rufen Sie [**mfkreatepmpmediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) auf, um die Medien Sitzung im PMP-Prozess zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="776af-143">Call [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) to create the Media Session in the PMP process.</span></span> <span data-ttu-id="776af-144">Der *pconfiguration* -Parameter ist ein Zeiger auf die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle des Attribut Speicher.</span><span class="sxs-lookup"><span data-stu-id="776af-144">The *pConfiguration* parameter is a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface of the attribute store.</span></span>


```C++
IMFAttributes *pAttributes = NULL;
IMFMediaSession *pSession = NULL;

// Create the attribute store.
hr = MFCreateAttributes(&pAttributes, 1);

// Set the IMFContentProtectionManager pointer.
if (SUCCEEDED(hr))
{
    hr = pAttributes->SetUnknown(
        MF_SESSION_CONTENT_PROTECTION_MANAGER, 
        pCPM  // Your implementation of IMFContentProtectionManager.
        );
}

// Create the Media Session.
if (SUCCEEDED(hr))
{
    hr = MFCreatePMPMediaSession(
        0,
        pAttributes, 
        &pSession,
        NULL
    );
}

SAFE_RELEASE(pAttributes); // Release the attribute store.
// Use the Media Session to control playback (not shown).
```



<span data-ttu-id="776af-145">Erstellen Sie als nächstes eine Wiedergabe Topologie, und stellen Sie Sie in der Medien Sitzung in eine Warteschlange, wie unter [Erstellen von Wiedergabe Topologien](creating-playback-topologies.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="776af-145">Next, create a playback topology and queue it on the Media Session, as described in [Creating Playback Topologies](creating-playback-topologies.md).</span></span>

## <a name="perform-rights-acquisition"></a><span data-ttu-id="776af-146">Durchführen der Rechte Erfassung</span><span class="sxs-lookup"><span data-stu-id="776af-146">Perform Rights Acquisition</span></span>

<span data-ttu-id="776af-147">Wenn die Wiedergabe eine Rechte Übernahme erfordert, ruft die Medien Sitzung [**IMF contentschutzmanager:: beginenablecontent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent)auf.</span><span class="sxs-lookup"><span data-stu-id="776af-147">If playback requires rights acquisition, the Media Session calls [**IMFContentProtectionManager::BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent).</span></span> <span data-ttu-id="776af-148">Der Parameter " *pableraktivierungs* " dieser Methode ist ein Zeiger auf die [**imfactivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="776af-148">The *pEnablerActivate* parameter of this method is a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span> <span data-ttu-id="776af-149">Verwenden Sie diese Schnittstelle zum Erstellen des Content Wegbereiter-Objekts, das die [**imfcontentenabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="776af-149">Use this interface to create the content enabler object, which exposes the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface.</span></span> <span data-ttu-id="776af-150">Verwenden Sie dann den Inhalts-Wegbereiter, um den Schritt für die Rechte Übernahme auszuführen.</span><span class="sxs-lookup"><span data-stu-id="776af-150">Then use the content enabler to perform the rights acquisition step.</span></span>

<span data-ttu-id="776af-151">Rufen Sie zum Erstellen des Inhalts Enablers [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)auf:</span><span class="sxs-lookup"><span data-stu-id="776af-151">To create the content enabler, call [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject):</span></span>


```C++
IMFContentEnabler *pEnabler = NULL;
hr = pEnablerActivate->ActivateObject(
    IID_IMFContentEnabler, 
    (void**)&pEnabler
    );
```



<span data-ttu-id="776af-152">Fragen Sie den zurückgegebenen [**IMF contentenabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) -Zeiger für die [**IMF mediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="776af-152">Query the returned [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) pointer for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="776af-153">Verwenden Sie diese Schnittstelle, um Ereignisse aus dem Content Wegbereiter-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="776af-153">Use this interface to get events from the content enabler object.</span></span> <span data-ttu-id="776af-154">Weitere Informationen zu Ereignissen finden Sie unter [Medienereignis Generatoren](media-event-generators.md).</span><span class="sxs-lookup"><span data-stu-id="776af-154">For more information about events, see [Media Event Generators](media-event-generators.md).</span></span>

<span data-ttu-id="776af-155">Um herauszufinden, ob der Inhalts Wegbereiter die automatische Erfassung unterstützt, nennen Sie [**imfcontentenabler:: isautomaticsupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported).</span><span class="sxs-lookup"><span data-stu-id="776af-155">To find out whether the content enabler supports automatic acquisition, call [**IMFContentEnabler::IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported).</span></span> <span data-ttu-id="776af-156">Wenn diese Methode den Wert **true** zurückgibt, sollte die Anwendung die automatische Erfassung verwenden.</span><span class="sxs-lookup"><span data-stu-id="776af-156">If this method returns the value **TRUE**, the application should use automatic acquisition.</span></span> <span data-ttu-id="776af-157">Andernfalls verwenden Sie den nicht automatischen Erwerb.</span><span class="sxs-lookup"><span data-stu-id="776af-157">Otherwise, use non-silent acquisition.</span></span>

<span data-ttu-id="776af-158">Die [**beginenablecontent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) -Methode ist asynchron.</span><span class="sxs-lookup"><span data-stu-id="776af-158">The [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) method is asynchronous.</span></span> <span data-ttu-id="776af-159">Die Anwendung sollte den Erwerbs Schritt für den Thread der Anwendung ausführen.</span><span class="sxs-lookup"><span data-stu-id="776af-159">The application should perform the acquisition step on the application's thread.</span></span> <span data-ttu-id="776af-160">Ein Ansatz besteht darin, eine private Fenster Meldung an das Hauptfenster der Anwendung zu senden und den Anwendungs Thread zur Durchführung des Erwerbs zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="776af-160">One approach is to post a private window message to the application's main window, notifying the application thread to perform the acquisition.</span></span> <span data-ttu-id="776af-161">Während der Vorgang ausstehend ist, muss die Anwendung den Rückruf Zeiger und das Zustands Objekt speichern, das in den Parametern *pCallback* und *punkstate* von **beginenablecontent** empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="776af-161">While the operation is pending, the application must store the callback pointer and the state object that it received in the *pCallback* and *punkState* parameters of **BeginEnableContent**.</span></span> <span data-ttu-id="776af-162">Diese werden verwendet, um den asynchronen Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="776af-162">These will be used to complete the asynchronous operation.</span></span>

### <a name="automatic-acquisition"></a><span data-ttu-id="776af-163">Automatischer Erwerb</span><span class="sxs-lookup"><span data-stu-id="776af-163">Automatic Acquisition</span></span>

<span data-ttu-id="776af-164">Um die automatische Erfassung durchzuführen, nennen Sie [**imfcontentenabler:: automaticenable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable).</span><span class="sxs-lookup"><span data-stu-id="776af-164">To perform automatic acquisition, call [**IMFContentEnabler::AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable).</span></span> <span data-ttu-id="776af-165">Diese Methode ist asynchron.</span><span class="sxs-lookup"><span data-stu-id="776af-165">This method is asynchronous.</span></span> <span data-ttu-id="776af-166">Wenn der Vorgang abgeschlossen ist, sendet der Inhalts-Wegbereiter ein [meenablerabgeschlossene](meenablercompleted.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="776af-166">When the operation is completed, the content enabler sends an [MEEnablerCompleted](meenablercompleted.md) event.</span></span> <span data-ttu-id="776af-167">Der Statuscode des Ereignisses gibt an, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="776af-167">The event's status code indicates whether the operation was successful.</span></span> <span data-ttu-id="776af-168">Wenn der Statuscode des meenablerabgeschlossene-Ereignisses NS \_ E \_ DRM- \_ Lizenz \_ notbezogen ist, sollte die Anwendung versuchen, den nicht automatischen Erwerb zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="776af-168">If the status code from the MEEnablerCompleted event is NS\_E\_DRM\_LICENSE\_NOTACQUIRED, the application should try using non-silent acquisition.</span></span>

<span data-ttu-id="776af-169">Während der Übernahme Vorgang kann das Wegbereiter-Objekt das [meenablerprogress](meenablerprogress.md) -Ereignis senden, um den Fortschritt des Vorgangs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="776af-169">While the acquisition operation is in progress, the enabler object might send the [MEEnablerProgress](meenablerprogress.md) event to indicate the progress of the operation.</span></span> <span data-ttu-id="776af-170">Rufen Sie [**imfcontentenabler:: Cancel**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-cancel)auf, um den Vorgang abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="776af-170">To cancel the operation, call [**IMFContentEnabler::Cancel**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-cancel).</span></span>

### <a name="non-silent-acquisition"></a><span data-ttu-id="776af-171">Nicht automatische Beschaffung</span><span class="sxs-lookup"><span data-stu-id="776af-171">Non-Silent Acquisition</span></span>

<span data-ttu-id="776af-172">Wenn die [**isautomaticsupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported) -Methode **false** zurückgibt oder die [**automaticenable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) -Methode mit dem Fehlercode NS \_ E \_ DRM- \_ Lizenz notbezogen fehlschlägt \_ , sollte die Anwendung einen nicht automatischen Erwerb durchführen, wie in den folgenden Schritten beschrieben:</span><span class="sxs-lookup"><span data-stu-id="776af-172">If the [**IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported) method returns **FALSE** or the [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) method fails with the error code NS\_E\_DRM\_LICENSE\_NOTACQUIRED, the application should perform non-silent acquisition as described in the following steps:</span></span>

1.  <span data-ttu-id="776af-173">Wenn Sie [**imfcontentenabler:: getenableurl**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenableurl) aufrufen, erhalten Sie die URL für den Erwerb der Rechte.</span><span class="sxs-lookup"><span data-stu-id="776af-173">Call [**IMFContentEnabler::GetEnableURL**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenableurl) to get the URL for the rights acquisition.</span></span> <span data-ttu-id="776af-174">Diese Methode gibt auch ein Flag zurück, das angibt, ob die URL vertrauenswürdig ist.</span><span class="sxs-lookup"><span data-stu-id="776af-174">This method also returns a flag indicating whether the URL is trusted.</span></span>
2.  <span data-ttu-id="776af-175">Aufrufen von [**imfcontentenabler:: getenabledata**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenabledata) zum Abrufen der HTTP Post-Daten.</span><span class="sxs-lookup"><span data-stu-id="776af-175">Call [**IMFContentEnabler::GetEnableData**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenabledata) to get the HTTP POST data.</span></span>
3.  <span data-ttu-id="776af-176">Nennen Sie [**imfcontentenabler:: monitorenable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable).</span><span class="sxs-lookup"><span data-stu-id="776af-176">Call [**IMFContentEnabler::MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable).</span></span> <span data-ttu-id="776af-177">Diese Methode bewirkt, dass der Inhalts-Wegbereiter den Fortschritt der Rechte Erwerbs Aktion überwacht.</span><span class="sxs-lookup"><span data-stu-id="776af-177">This method causes the content enabler to monitor the progress of the rights acquisition action.</span></span>

4.  <span data-ttu-id="776af-178">Übermitteln Sie die Daten mithilfe einer HTTP Post-Aktion an die URL für die Rechte Erfassung.</span><span class="sxs-lookup"><span data-stu-id="776af-178">Submit the data to the rights acquisition URL by using an HTTP POST action.</span></span> <span data-ttu-id="776af-179">Sie können das Internet Explorer-Steuerelement oder die Windows Internet-APIs (WinInet) verwenden.</span><span class="sxs-lookup"><span data-stu-id="776af-179">You can use the Internet Explorer control or the Windows Internet (WinINet) APIs.</span></span>

<span data-ttu-id="776af-180">Der folgende Code zeigt die Schritte 1 – 3.</span><span class="sxs-lookup"><span data-stu-id="776af-180">The following code shows steps 1–3.</span></span> <span data-ttu-id="776af-181">Schritt 4 hängt von den speziellen Anforderungen Ihrer Anwendung ab.</span><span class="sxs-lookup"><span data-stu-id="776af-181">Step 4 depends on your application's particular requirements.</span></span>


```C++
WCHAR   *sURL = NULL;  // URL.
DWORD   cchURL = 0;    // Size of the URL in characters.

// Trust status of the URL.
MF_URL_TRUST_STATUS  trustStatus = MF_LICENSE_URL_UNTRUSTED;

BYTE    *pPostData = NULL;  // Buffer to hold HTTP POST data.
DWORD   cbPostDataSize = 0; // Size of the buffer, in bytes.

HRESULT hr = S_OK;

// Get the URL. 
hr = m_pEnabler->GetEnableURL(&sURL, &cchURL, &trustStatus);

if (SUCCEEDED(hr))
{
    if (trustStatus != MF_LICENSE_URL_TRUSTED)
    {
        // The URL is not trusted. Do not proceed.
        hr = E_FAIL;
    }
}

// Monitor the rights acquisition. 
if (SUCCEEDED(hr))
{
    hr = m_pEnabler->MonitorEnable();
}

// Get the HTTP POST data.
if (SUCCEEDED(hr))
{
    hr = m_pEnabler->GetEnableData(&pPostData, &cbPostDataSize);
}

// Open the URL and send the HTTP POST data. (Not shown.)

// Release the buffers.
CoTaskMemFree(pPostData);
CoTaskMemFree(sURL);
```



<span data-ttu-id="776af-182">Wenn der Vorgang abgeschlossen ist, sendet der Inhalts-Wegbereiter ein [meenablerabgeschlossene](meenablercompleted.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="776af-182">When the operation is completed, the content enabler sends an [MEEnablerCompleted](meenablercompleted.md) event.</span></span>

## <a name="complete-the-asynchronous-operation"></a><span data-ttu-id="776af-183">Asynchronen Vorgang beenden</span><span class="sxs-lookup"><span data-stu-id="776af-183">Complete the Asynchronous Operation</span></span>

<span data-ttu-id="776af-184">Wenn die Rechte Erfassung erfolgreich oder anderweitig abgeschlossen ist, muss die Anwendung die Medien Sitzung Benachrichtigen, indem Sie den Rückruf Zeiger aufruft, der in der [**beginenablecontent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) -Methode angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="776af-184">When the rights acquisition is completed, successfully or otherwise, the application must notify the Media Session, by invoking the callback pointer given in the [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) method.</span></span>

1.  <span data-ttu-id="776af-185">Erstellen Sie ein asynchrones Ergebnis Objekt, indem Sie [**mfcreateasyncresult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="776af-185">Create an asynchronous result object by calling [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult).</span></span>
2.  <span data-ttu-id="776af-186">Rufen Sie den Rückruf der Medien Sitzung auf, indem Sie [**mfinvokecallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="776af-186">Invoke the Media Session's callback by calling [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).</span></span>
3.  <span data-ttu-id="776af-187">In der Medien Sitzung wird [**imfcontentschutzmanager:: erdenablecontent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="776af-187">The Media Session will call [**IMFContentProtectionManager::EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent).</span></span> <span data-ttu-id="776af-188">Geben Sie in ihrer Implementierung dieser Methode alle in [**beginenablecontent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent)zugeordneten Zeiger oder Ressourcen frei.</span><span class="sxs-lookup"><span data-stu-id="776af-188">In your implementation of this method, release any pointers or resources that you allocated inside [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent).</span></span> <span data-ttu-id="776af-189">Gibt ein **HRESULT** zurück, das den Gesamterfolg des Vorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="776af-189">Return an **HRESULT** that indicates the overall success of the operation.</span></span> <span data-ttu-id="776af-190">Wenn die Rechte Beschaffung fehlgeschlagen ist oder der Benutzer vor dem Abschluss abgebrochen wurde, wird ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="776af-190">If the rights acquisition failed or the user canceled before it was completed, return an error code.</span></span>

<span data-ttu-id="776af-191">Der folgende Code zeigt, wie das asynchrone Ergebnis erstellt und der Rückruf aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="776af-191">The following code shows how to create the asynchronous result and invoke the callback.</span></span>


```C++
IMFAsyncResult  *pResult = NULL;

// Create the asynchronous result object.
hr = MFCreateAsyncResult(NULL, pCallback, punkState, &pResult);

// Invoke the callback.
if (SUCCEEDED(hr))
{
    pResult->SetStatus(hrStatus);
    hr = MFInvokeCallback(pResult);
}
SAFE_RELEASE(pResult);
```



## <a name="related-topics"></a><span data-ttu-id="776af-192">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="776af-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="776af-193">Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="776af-193">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="776af-194">Audio-/Videowiedergabe</span><span class="sxs-lookup"><span data-stu-id="776af-194">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 



