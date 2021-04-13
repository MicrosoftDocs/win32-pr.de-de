---
title: Behandeln von Lizenz Erwerbs Ereignissen
description: Behandeln von Lizenz Erwerbs Ereignissen
ms.assetid: e118bf09-1fa6-41b6-a6bb-3e8cb6097994
keywords:
- Windows Media-Format-SDK, behandeln von Lizenz Erwerbs Ereignissen
- Windows Media-Format-SDK, Lizenz Erwerbs Ereignisse
- Advanced Systems Format (ASF), behandeln von Lizenz Erwerbs Ereignissen
- ASF (Advanced Systems Format), behandeln von Lizenz Erwerbs Ereignissen
- Advanced Systems Format (ASF), Lizenz Erwerbs Ereignisse
- ASF (Advanced Systems Format), Lizenz Erwerbs Ereignisse
- Digital Rights Management (DRM), behandeln von Lizenz Erwerbs Ereignissen
- DRM (Digital Rights Management), behandeln von Lizenz Erwerbs Ereignissen
- Digital Rights Management (DRM), Lizenz Erwerbs Ereignisse
- DRM (Digital Rights Management), Lizenz Erwerbs Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e31fd5b108f41d5b0925918fdf1c83764bcf7e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389884"
---
# <a name="handling-license-acquisition-events"></a><span data-ttu-id="cc5e8-113">Behandeln von Lizenz Erwerbs Ereignissen</span><span class="sxs-lookup"><span data-stu-id="cc5e8-113">Handling License Acquisition Events</span></span>

<span data-ttu-id="cc5e8-114">Eine DRM-fähige Reader-Anwendung in der [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Rückruf Methode behandelt die folgenden vier Ereignisse im Zusammenhang mit dem Lizenz Erwerbs Vorgang:</span><span class="sxs-lookup"><span data-stu-id="cc5e8-114">A DRM-enabled reader application, in its [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method, handles the following four events related to the license acquisition process:</span></span>

-   <span data-ttu-id="cc5e8-115">**WMT \_ licengurl- \_ Signatur \_ Status**</span><span class="sxs-lookup"><span data-stu-id="cc5e8-115">**WMT\_LICENSEURL\_SIGNATURE\_STATE**</span></span>
-   <span data-ttu-id="cc5e8-116">**WMT \_ keine \_ Rechte**</span><span class="sxs-lookup"><span data-stu-id="cc5e8-116">**WMT\_NO\_RIGHTS**</span></span>
-   <span data-ttu-id="cc5e8-117">**WMT \_ keine \_ Rechte \_ Ex**</span><span class="sxs-lookup"><span data-stu-id="cc5e8-117">**WMT\_NO\_RIGHTS\_EX**</span></span>
-   <span data-ttu-id="cc5e8-118">**WMT-Abruf \_ \_ Lizenz**</span><span class="sxs-lookup"><span data-stu-id="cc5e8-118">**WMT\_ACQUIRE\_LICENSE**</span></span>

<span data-ttu-id="cc5e8-119">**WMT \_ licengurl- \_ Signatur \_ Status**</span><span class="sxs-lookup"><span data-stu-id="cc5e8-119">**WMT\_LICENSEURL\_SIGNATURE\_STATE**</span></span>

<span data-ttu-id="cc5e8-120">Wenn von der DRM-Komponente Inhalte erkannt werden, die von DRM-Version 7 geschützt werden, wird zuerst nach einer gültigen Lizenz auf dem lokalen System gesucht.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-120">When the DRM component detects content protected by DRM version 7, it first looks for a valid license on the local system.</span></span> <span data-ttu-id="cc5e8-121">Wenn keines vorhanden ist, wertet es die Lizenz Erwerbs-URL im DRM-Header der Datei aus und sendet ein **WMT \_ licenseurl- \_ Signatur \_ Zustands** Ereignis mit *pValue* , das auf einen der [**WMT- \_ drmla- \_ Vertrauensstellungs**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_drmla_trust) Werte festgelegt ist und angibt, ob die URL vertrauenswürdig oder nicht vertrauenswürdig ist oder manipuliert wurde.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-121">If none exists, it then evaluates the license acquisition URL in the file's DRM header and sends a **WMT\_LICENSEURL\_SIGNATURE\_STATE** event with *pValue* set to one of the [**WMT\_DRMLA\_TRUST**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_drmla_trust) values, indicating whether the URL is trusted, untrusted, or has been tampered with.</span></span> <span data-ttu-id="cc5e8-122">Wenn die URL nicht vertrauenswürdig ist, sollte die Anwendung den Benutzer warnen.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-122">If the URL is not trusted, then the application should warn the user.</span></span> <span data-ttu-id="cc5e8-123">Wenn die URL manipuliert wurde, sollte die Datei als beschädigt angesehen werden, und die Anwendung sollte nicht zur URL navigieren, ohne dass eine Warnung für den Benutzer ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-123">If the URL has been tampered with, then the file should be considered corrupted, and the application should not navigate to the URL without issuing a strong warning the user.</span></span>

<span data-ttu-id="cc5e8-124">**WMT \_ keine \_ Rechte**</span><span class="sxs-lookup"><span data-stu-id="cc5e8-124">**WMT\_NO\_RIGHTS**</span></span>

<span data-ttu-id="cc5e8-125">Das Ereignis **WMT \_ No \_ Rights** wird nur für den Inhalt der DRM-Version 1 gesendet, was bedeutet, dass die Lizenz nicht im Hintergrund erworben werden muss.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-125">The **WMT\_NO\_RIGHTS** event is sent only for DRM version 1 content, which means that the license must be acquired non-silently.</span></span> <span data-ttu-id="cc5e8-126">Das heißt, der Benutzer muss zu einer Webseite navigieren, um eine Lizenz zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-126">In other words, the user must navigate to a Web page to acquire a license.</span></span> <span data-ttu-id="cc5e8-127">Die URL für die Seite wird als breit Zeichen-NULL-terminierte Zeichenfolge aus dem *pValue* -Parameter in der **OnStatus** -Methode abgerufen.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-127">The URL for the page is retrieved as a wide-character null-terminated string from the *pValue* parameter in the **OnStatus** method.</span></span>

<span data-ttu-id="cc5e8-128">Wenn dies der Fall ist, kann eine Anwendung die Navigation zu der Webseite vereinfachen, indem Sie entweder Internet Explorer in einem separaten Prozess öffnen oder das WebBrowser-Steuerelement als Host verwenden.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-128">If appropriate, an application can make it easier for the user to navigate to the Web page, either by opening up Internet Explorer in a separate process or else by hosting the Web Browser control.</span></span> <span data-ttu-id="cc5e8-129">Dies ist jedoch nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-129">This is not required, however.</span></span> <span data-ttu-id="cc5e8-130">Mindestens eine Anwendung könnte einfach die URL für den Benutzer in einem Meldungs Feld anzeigen und Sie auffordern, Sie in die Adressleiste von Internet Explorer einzufügen.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-130">At the very least, an application could simply display the URL to the user in a message box and prompt them to paste it into the address bar of Internet Explorer.</span></span> <span data-ttu-id="cc5e8-131">Das Audioplayer-Beispiel veranschaulicht die ordnungsgemäße Behandlung des **WMT-Ereignisses \_ ohne \_ Rechte** , einschließlich der Formatierung der URL-Zeichenfolge und der Verwendung **der Methode "** Methode", um Internet Explorer zu öffnen und zur angegebenen URL zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-131">The Audioplayer sample demonstrates proper handling of the **WMT\_NO\_RIGHTS** event, including how to format the URL string, and how to use the **CreateProcess** method to open Internet Explorer and navigate to the specified URL.</span></span>

<span data-ttu-id="cc5e8-132">Da die Anwendung nicht weiß, wann eine DRM-Lizenz der Version 1 abgerufen wurde, kann der Benutzer versuchen, die Datei nach dem Erwerb der Lizenz erneut zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-132">Because the application has no way of knowing when a DRM version 1 license has been acquired, it is up to the user to attempt to open the file again after acquiring the license.</span></span>

<span data-ttu-id="cc5e8-133">Dieser nicht automatische Lizenz Erwerbsprozess kann auch für Lizenzen der Version 7 verwendet werden. in diesem Fall kann die Anwendung jedoch zuerst [**iwmdrmreader:: monitorlicenseacquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition)anrufen.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-133">This same non-silent license acquisition process can also be used for version 7 licenses, but in this case the application can first call [**IWMDRMReader::MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition).</span></span> <span data-ttu-id="cc5e8-134">Diese Methode bewirkt, dass der lokale Lizenz Speicher wiederholt geprüft wird, bis die Lizenz für die neue Datei gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-134">This method will cause the local license store to be checked repeatedly until the license for the new file is found.</span></span> <span data-ttu-id="cc5e8-135">An diesem Punkt empfängt die Anwendung ein **WMT-Abruf \_ \_ Lizenz** Ereignis.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-135">At that point, the application will receive a **WMT\_ACQUIRE\_LICENSE** event.</span></span> <span data-ttu-id="cc5e8-136">Für alle Lizenzen der Version 7 empfiehlt es sich, dass Anwendungen Benutzern die Option zum automatischen Abrufen von Lizenzen oder nicht im Hintergrund zukommen lassen.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-136">For all version 7 licenses, it is recommended that applications give users the option to obtain licenses silently or non-silently.</span></span>

<span data-ttu-id="cc5e8-137">**WMT \_ keine \_ Rechte \_ Ex**</span><span class="sxs-lookup"><span data-stu-id="cc5e8-137">**WMT\_NO\_RIGHTS\_EX**</span></span>

<span data-ttu-id="cc5e8-138">Das Ereignis **WMT \_ No \_ Rights \_ Ex** gibt an, dass der Inhalt durch DRM-Version 7 geschützt ist. Daher kann der Lizenz Erwerbsprozess entweder unbeaufsichtigt oder nicht im Hintergrund fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-138">The **WMT\_NO\_RIGHTS\_EX** event indicates that the content is protected by DRM version 7, and therefore the license acquisition process can proceed either silently or non-silently.</span></span> <span data-ttu-id="cc5e8-139">Im Allgemeinen ist der automatische Erwerb von Lizenzen für Endbenutzer bequemer, auch wenn es für einige Benutzer vorzuziehen ist, alle Lizenzen nicht im Hintergrund zu erwerben.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-139">In general, silent license acquisition is more convenient for end users, although some people prefer to acquire all licenses non-silently.</span></span> <span data-ttu-id="cc5e8-140">Wenn der Lizenzerwerb erfordert, dass der Benutzer Zahlungs-oder persönliche Informationen sendet, sollte der Prozess immer ohne Hintergrund ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-140">When license acquisition requires the user to submit payment or personal information, the process should always be performed non-silently.</span></span> <span data-ttu-id="cc5e8-141">Der nicht automatische Lizenzerwerb wird oben unter der Überschrift " **WMT \_ No \_ Rights** " beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-141">Non-silent license acquisition is described above under the **WMT\_NO\_RIGHTS** heading.</span></span> <span data-ttu-id="cc5e8-142">Der automatische Erwerb erfolgt wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc5e8-142">Silent acquisition proceeds as follows:</span></span>

1.  <span data-ttu-id="cc5e8-143">Wandeln Sie den *pValue* -Parameter in eine [**WM- \_ \_ Lizenz \_ Daten**](wm-get-license-data.md) Struktur um, und speichern Sie die Struktur für den Fall, dass Sie später für den nicht automatischen Lizenzerwerb benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-143">Cast the *pValue* parameter to a [**WM\_GET\_LICENSE\_DATA**](wm-get-license-data.md) structure and store the structure in case it is needed later for non-silent license acquisition.</span></span>
2.  <span data-ttu-id="cc5e8-144">Rufen Sie **QueryInterface** für das Reader-Objekt auf, um die [**iwmdrmreader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-144">Call **QueryInterface** on the reader object to obtain the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface.</span></span>
3.  <span data-ttu-id="cc5e8-145">Nennen Sie [**iwmdrmreader:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) , und geben Sie im *dwFlags* -Parameter 0x1 an, um den automatischen Abruf der Sprache anzugeben.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-145">Call [**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) and specify 0x1 in the *dwFlags* parameter to indicate silent language acquisition.</span></span> <span data-ttu-id="cc5e8-146">Dies ist ein asynchroner Rückruf, der sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-146">This is an asynchronous call that returns immediately.</span></span>
4.  <span data-ttu-id="cc5e8-147">Warten Sie, bis das **WMT- \_ \_ Lizenz** Ereignis abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-147">Wait for the **WMT\_ACQUIRE\_LICENSE** event.</span></span>

<span data-ttu-id="cc5e8-148">**WMT-Abruf \_ \_ Lizenz**</span><span class="sxs-lookup"><span data-stu-id="cc5e8-148">**WMT\_ACQUIRE\_LICENSE**</span></span>

<span data-ttu-id="cc5e8-149">Das **WMT \_ \_** -Ereignis zum Abrufen einer Lizenz wird gesendet, nachdem der Lizenz Erwerbs Vorgang für eine DRM-Lizenz Version 7 abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-149">The **WMT\_ACQUIRE\_LICENSE** event is sent after the license acquisition process is completed for a DRM version 7 license.</span></span> <span data-ttu-id="cc5e8-150">[**Iwmdrmreader:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) bewirkt, dass dieses Ereignis für die automatische Übernahme gesendet wird, und [**monitorlicenseacquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition) bewirkt, dass es für einen nicht automatischen Erwerb gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-150">[**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) causes this event to be sent for silent acquisition, and [**MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition) causes it to be sent for non-silent acquisition.</span></span> <span data-ttu-id="cc5e8-151">Wandeln Sie in Ihrem Ereignishandler *pValue* in einen Zeiger auf eine [**WM-Lizenz für die \_ \_ Lizenz \_ Daten**](wm-get-license-data.md) Struktur um, und untersuchen Sie das **HR** -Element, um zu bestimmen, ob die Lizenz erfolgreich abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-151">In your event handler, cast *pValue* to a pointer to a [**WM\_GET\_LICENSE\_DATA**](wm-get-license-data.md) structure and examine the **hr** member to determine whether the license was successfully acquired.</span></span> <span data-ttu-id="cc5e8-152">Wenn **HR** dem NS \_ E \_ DRM \_ keine \_ Rechte zuweist, weist dies darauf hin, dass die Lizenz nicht im Hintergrund erworben werden muss.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-152">If **hr** equals NS\_E\_DRM\_NO\_RIGHTS, it indicates that the license must be acquired non-silently.</span></span> <span data-ttu-id="cc5e8-153">Anwendungen sollten es Benutzern ermöglichen, den Lizenz Erwerbsprozess jederzeit abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-153">Applications should enable users to cancel the license acquisition process at any time.</span></span> <span data-ttu-id="cc5e8-154">Dies erfolgt durch Aufrufen von [**iwmdrmreader:: cancellicenabacquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancellicenseacquisition).</span><span class="sxs-lookup"><span data-stu-id="cc5e8-154">This is done by calling [**IWMDRMReader::CancelLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancellicenseacquisition).</span></span> <span data-ttu-id="cc5e8-155">Wenn Sie diese Methode aufrufen, wird ein **WMT-Abruf \_ \_ Lizenz** Ereignis mit einem **HRESULT** -Wert des NS-DRM-Abruf Abrufs gesendet \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cc5e8-155">Calling this method will send a **WMT\_ACQUIRE\_LICENSE** event with an **HRESULT** value of NS\_S\_DRM\_ACQUIRE\_CANCELLED.</span></span>

<span data-ttu-id="cc5e8-156">Wenn **HR** gleich \_ \_ \_ \_ der erworbenen NS-DRM-Lizenz ist, wurde die Lizenz abgerufen, und die Anwendung kann versuchen, die Datei wiederzugeben oder Sie auf ein Gerät zu kopieren oder eine beliebige Aktion auszuführen, für die Sie Rechte angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-156">If **hr** equals NS\_S\_DRM\_LICENSE\_ACQUIRED, then the license has been acquired and the application can attempt to play the file, or copy it to a device or perform whatever action it had requested rights for.</span></span>

<span data-ttu-id="cc5e8-157">Unter Windows XP wurde ein neuer Fehlercode eingeführt: NS \_ E \_ DRM- \_ Lizenz \_ noterworben.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-157">On Windows XP, a new error code was introduced: NS\_E\_DRM\_LICENSE\_NOTACQUIRED.</span></span> <span data-ttu-id="cc5e8-158">Dieser Fehlercode wird generiert, wenn die Laufzeitkomponenten des Windows Media-Formats unter Windows XP während des automatischen oder nicht automatischen Lizenz Erwerbs keine Lizenz erhalten.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-158">This error code is generated whenever the Windows Media Format run-time components on Windows XP fail to acquire a license during silent or non-silent license acquisition.</span></span> <span data-ttu-id="cc5e8-159">Auf anderen Plattformen \_ \_ wird der NS E DRM- \_ Lizenz \_ Speicher \_ Fehler normalerweise zurückgegeben, wenn der Lizenzerwerb fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-159">On other platforms, NS\_E\_DRM\_LICENSE\_STORE\_ERROR is usually returned when license acquisition fails.</span></span> <span data-ttu-id="cc5e8-160">Mit dem neuen Fehlercode soll der Lizenz Erwerbs Fehler von anderen Fehlerbedingungen unterschieden werden, bei denen der Fehler "NS \_ E \_ DRM- \_ Lizenz \_ Speicher" \_ generiert wird.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-160">The new error code is intended to distinguish license acquisition failure from other failure conditions where NS\_E\_DRM\_LICENSE\_STORE\_ERROR is generated.</span></span>

<span data-ttu-id="cc5e8-161">Die empfohlene Methode, diese Fehler zu behandeln, wenn Sie nach einem automatischen Lizenz Erwerbs Versuch zurückgegeben wird, wird im folgenden Code Ausschnitt gezeigt:</span><span class="sxs-lookup"><span data-stu-id="cc5e8-161">The recommended way to handle these errors when they are returned after a silent license acquisition attempt is shown in the following code snippet:</span></span>


```C++
if( hrStatus == NS_E_DRM_LICENSE_NOTACQUIRED || 
    hrStatus == NS_E_DRM_LICENSE_STORE_ERROR )
{
  // Attempt non-silent license acquisition.
}
else if( hrStatus == NS_E_DRM_NEEDS_INDIVIDUALIZATION )
{
  // Individualize and then retry.
}
else if( FAILED(hrStatus) )
{
  // Display a helpful error message.
}
else
{
  // Success. Play content.
}
```



> [!Note]  
> <span data-ttu-id="cc5e8-162">DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-162">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="cc5e8-163">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cc5e8-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc5e8-164">**Geschützte Dateien werden gelesen.**</span><span class="sxs-lookup"><span data-stu-id="cc5e8-164">**Reading Protected Files**</span></span>](reading-protected-files.md)
</dt> </dl>

 

 




