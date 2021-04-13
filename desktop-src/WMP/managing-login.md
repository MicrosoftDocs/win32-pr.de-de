---
title: Verwalten der Anmeldung
description: Verwalten der Anmeldung
ms.assetid: 5cafcd3a-e819-4524-b7a9-580ff36fc4f8
keywords:
- Windows Media Player Online Stores, Verwalten von Anmeldungen
- Online Stores, Verwalten von Anmeldungen
- Geben Sie 1 Online Stores ein, und verwalten Sie Anmeldungen.
- Windows Media Player Online Stores, Anmeldungen
- Online Stores, Anmeldungen
- Typ 1 Online Stores, Anmeldungen
- Windows Media Player Online Stores, standardmäßiger Anmeldevorgang
- Online Stores, Standard-Anmeldeprozess
- Typ 1 Online Stores, Standard-Anmeldeprozess
- Windows Media Player Online Stores, ABMELDEPROZESS
- Online Stores, ABMELDEPROZESS
- Typ 1 Online Stores, ABMELDEPROZESS
- standardmäßiger Anmeldevorgang
- ABMELDEPROZESS
- Anmeldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633042692ab9193f46ab83415df13237d3a279e8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389886"
---
# <a name="managing-login"></a><span data-ttu-id="32091-118">Verwalten der Anmeldung</span><span class="sxs-lookup"><span data-stu-id="32091-118">Managing Login</span></span>

<span data-ttu-id="32091-119">Windows Media Player unterstützt eine Vielzahl von Methoden, mit denen sich der Benutzer bei einem Online Store vom Typ 1 anmelden können.</span><span class="sxs-lookup"><span data-stu-id="32091-119">Windows Media Player supports a variety of methods for the user to log in to a type 1 online store.</span></span> <span data-ttu-id="32091-120">Der Player stellt ein Standard Dialogfeld für die Anmeldung bereit, aber der Online Shop kann eine Webseite bereitstellen, die als Alternative zum Standard Dialogfeld fungiert.</span><span class="sxs-lookup"><span data-stu-id="32091-120">The Player provides a standard log-in dialog box, but the online store can provide a webpage that serves as an alternative to the standard dialog box.</span></span>

<span data-ttu-id="32091-121">Der Benutzer kann einen Anmeldeversuch initiieren, indem er mit der Windows Media Player-Benutzeroberfläche interagiert oder mit einer Ermittlungs Seite interagiert, die im Online Store bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="32091-121">The user can initiate a log-in attempt by interacting with the Windows Media Player user interface or by interacting with a discovery page provided by the online store.</span></span> <span data-ttu-id="32091-122">Wenn der Benutzer einen Anmeldeversuch durch Interaktion mit einer Ermittlungs Seite initiiert, ruft das Skript auf der Ermittlungs Seite die [externe.-Anmelde](external-attemptlogin.md) Methode auf.</span><span class="sxs-lookup"><span data-stu-id="32091-122">If the user initiates a log-in attempt by interacting with a discovery page, script on the discovery page calls the [External.attemptLogin](external-attemptlogin.md) method.</span></span>

<span data-ttu-id="32091-123">Der Anmelde Zustand des Benutzers wird vom Online Store verwaltet.</span><span class="sxs-lookup"><span data-stu-id="32091-123">The user's log-in state is maintained by the online store.</span></span> <span data-ttu-id="32091-124">Wenn sich der Anmelde Zustand des Benutzers ändert, oder wenn ein Anmeldeversuch fehlschlägt, benachrichtigt das Plug-in des Online Stores Windows Media Player durch Aufrufen von [iwmpcontentpartnercallback:: notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify)und übergibt dabei wmpcnloginstatechange im *Typparameter* .</span><span class="sxs-lookup"><span data-stu-id="32091-124">When the user's log-in state changes, or if a log-in attempt fails, the online store's plug-in notifies Windows Media Player by calling [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passing wmpcnLoginStateChange in the *type* parameter.</span></span> <span data-ttu-id="32091-125">Der Player übergibt die Benachrichtigung an die Ermittlungs Seite, indem er das [externe. onloginchange](external-onloginchange-event.md) -Ereignis aufhebt.</span><span class="sxs-lookup"><span data-stu-id="32091-125">The Player passes the notification along to the discovery page by raising the [External.OnLoginChange](external-onloginchange-event.md) event.</span></span>

<span data-ttu-id="32091-126">Ein **onloginchange** -aufrufswert bedeutet nicht notwendigerweise, dass sich der Anmelde Zustand des Benutzers geändert hat. Dies könnte bedeuten, dass ein Anmeldeversuch fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="32091-126">A call to **OnLoginChange** does not necessarily mean that the user's log-in state changed; it could mean that an attempt to log in failed.</span></span> <span data-ttu-id="32091-127">Um den Anmeldestatus des Benutzers zu bestimmen, kann der **onloginchange** -Ereignishandler die [externe. userloggedin](external-userloggedin.md) -Eigenschaft überprüfen.</span><span class="sxs-lookup"><span data-stu-id="32091-127">To determine the user's log-in state, the **OnLoginChange** event handler can inspect the [External.userLoggedIn](external-userloggedin.md) property.</span></span>

<span data-ttu-id="32091-128">In den folgenden Abschnitten werden der standardmäßige Anmeldevorgang, der Alternative Anmeldevorgang und der Abmeldevorgang beschrieben.</span><span class="sxs-lookup"><span data-stu-id="32091-128">The following sections describe the standard log-in process, the alternative log-in process, and the log-out process.</span></span>

## <a name="standard-log-in"></a><span data-ttu-id="32091-129">Standard Anmeldung</span><span class="sxs-lookup"><span data-stu-id="32091-129">Standard Log-in</span></span>

<span data-ttu-id="32091-130">Der standardmäßige Anmeldevorgang umfasst die folgenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="32091-130">The standard log-in process involves the following steps:</span></span>

1.  <span data-ttu-id="32091-131">Der Benutzer initiiert einen Anmeldeversuch, indem er mit der Windows Media Player-Benutzeroberfläche interagiert oder mit einer Ermittlungs Seite interagiert.</span><span class="sxs-lookup"><span data-stu-id="32091-131">The user initiates a log-in attempt by interacting with the Windows Media Player user interface or by interacting with a discovery page.</span></span>
2.  <span data-ttu-id="32091-132">In Windows Media Player wird ein Dialogfeld angezeigt, in dem der Benutzer zur Eingabe eines Benutzernamens und Kennworts aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="32091-132">Windows Media Player displays a dialog box that prompts the user for a user-name and password.</span></span>
3.  <span data-ttu-id="32091-133">Wenn der Benutzer im Dialogfeld auf die Schaltfläche " **Anmelden** " klickt, ruft Windows Media Player [iwmpcontentpartner:: Login](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)auf, das durch das Plug-in des Online Stores implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="32091-133">When the user clicks the **Sign In** button in the dialog box, Windows Media Player calls [IWMPContentPartner::Login](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login), which is implemented by the online store's plug-in.</span></span>
4.  <span data-ttu-id="32091-134">Das Plug-in kommuniziert mit dem Online Store und ist entweder erfolgreich oder kann nicht in den Benutzer protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="32091-134">The plug-in communicates with the online store and either succeeds or fails to log in the user.</span></span>
5.  <span data-ttu-id="32091-135">Wenn der Anmeldeversuch erfolgreich ist, benachrichtigt das Plug-in Windows Media Player durch Aufrufen von **iwmpcontentpartnercallback:: notify** und übergibt Variant \_ true in den **boolVal** -Member des *pContext* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="32091-135">If the log-in attempt succeeds, the plug-in notifies Windows Media Player by calling **IWMPContentPartnerCallback::Notify**, passing VARIANT\_TRUE in the **boolVal** member of the *pContext* parameter.</span></span> <span data-ttu-id="32091-136">Wenn der Anmeldeversuch fehlschlägt, benachrichtigt das Plug-in Windows Media Player durch Aufrufen von **iwmpcontentpartnercallback:: notify** und übergibt einen 32-Bit-Wert im **ulVal** -Member des *pContext* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="32091-136">If the log-in attempt fails, the plug-in notifies Windows Media Player by calling **IWMPContentPartnerCallback::Notify**, passing a 32-bit value in the **ulVal** member of the *pContext* parameter.</span></span> <span data-ttu-id="32091-137">Der Spieler übergibt dann diesen 32-Bit-Wert an [iwmpcontentpartner:: getiteminfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) , um die URL einer Webseite zu erhalten, die den Fehler behandeln kann.</span><span class="sxs-lookup"><span data-stu-id="32091-137">The Player then passes that 32-bit value to [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) to get the URL of a webpage that can handle the failure.</span></span>

## <a name="alternative-login"></a><span data-ttu-id="32091-138">Alternativer Anmelde Name</span><span class="sxs-lookup"><span data-stu-id="32091-138">Alternative Login</span></span>

<span data-ttu-id="32091-139">Wenn das Abonnement \_ Cap- \_ altanmeldungs-Flag im Registrierungs Eintrag " **Funktionen** " für das Plug-in des Online Stores festgelegt ist, verwendet Windows Media Player nicht das Standard Dialogfeld "Anmelden".</span><span class="sxs-lookup"><span data-stu-id="32091-139">If the SUBSCRIPTION\_CAP\_ALTLOGIN flag is set in the **Capabilities** registry entry for the online store's plug-in, Windows Media Player does not use the standard log-in dialog box.</span></span> <span data-ttu-id="32091-140">Stattdessen ruft Windows Media Player **iwmpcontentpartner:: getiteminfo** auf, um die URL einer Webseite abzurufen, die den Anmeldevorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="32091-140">Instead, Windows Media Player calls **IWMPContentPartner::GetItemInfo** to retrieve the URL of a webpage that performs the log-in process.</span></span> <span data-ttu-id="32091-141">Weitere Informationen zum Registrierungs Eintrag " **Funktionen** " finden Sie unter [Registrierungsschlüssel und Einträge für den Online Store des Typs 1](registry-keys-and-entries-for-a-type-1-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="32091-141">For more information about the **Capabilities** registry entry, see [Registry Keys and Entries for a Type 1 Online Store](registry-keys-and-entries-for-a-type-1-online-store.md).</span></span>

<span data-ttu-id="32091-142">Der Player ruft " **getiteminfo** " zweimal auf: übergeben Sie "g \_ sziteminfo \_ altloginurl", um die URL der Anmelde Webseite abzurufen, und übergeben Sie "g \_ sziteminfo \_ altlogincaption", um die Beschriftung für das Fenster abzurufen, das die Webseite hostet.</span><span class="sxs-lookup"><span data-stu-id="32091-142">The Player calls **GetItemInfo** twice: once passing g\_szItemInfo\_ALTLoginURL to retrieve the URL of the log-in webpage and once passing g\_szItemInfo\_ALTLoginCaption to retrieve the caption for the window that hosts the webpage.</span></span> <span data-ttu-id="32091-143">Wenn **getiteminfo** die URL der Anmelde Webseite zurückgibt, kann Sie die Größe des Anmelde Fensters angeben, indem die folgende Parameter Zeichenfolge an die URL angehängt wird:</span><span class="sxs-lookup"><span data-stu-id="32091-143">When **GetItemInfo** returns the URL of the log-in webpage, it can specify the size of the log-in window by appending the following parameter string to the URL:</span></span>

<span data-ttu-id="32091-144">? Dlgx =*Width*&dlgy =*height*</span><span class="sxs-lookup"><span data-stu-id="32091-144">?DlgX=*width*&DlgY=*height*</span></span>

<span data-ttu-id="32091-145">In der Parameter Zeichenfolge sind " *Width* " und " *height* " die Breite und Höhe des Fensters in Pixel.</span><span class="sxs-lookup"><span data-stu-id="32091-145">In the parameter string, *width* and *height* are the width and height of the window in pixels.</span></span> <span data-ttu-id="32091-146">Beispielsweise könnte **getiteminfo** die folgende Zeichenfolge zurückgeben, um anzugeben, dass AltLogin.htm in einem Fenster mit einer Breite von 800 Pixeln und einer Höhe von 400 Pixel angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="32091-146">For example **GetItemInfo** could return the following string to specify that AltLogin.htm should be displayed in a window that has a width of 800 pixels and a height of 400 pixels</span></span>


```C++
https://proseware.com/AltLogin.htm?DlgX=800&DlgY=400
```



<span data-ttu-id="32091-147">Der Alternative Anmeldevorgang umfasst die folgenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="32091-147">The alternative log-in process involves the following steps:</span></span>

1.  <span data-ttu-id="32091-148">Der Benutzer initiiert einen Anmeldeversuch, indem er mit der Windows Media Player-Benutzeroberfläche interagiert oder mit einer Ermittlungs Seite interagiert.</span><span class="sxs-lookup"><span data-stu-id="32091-148">The user initiates a log-in attempt by interacting with the Windows Media Player user interface or by interacting with a discovery page.</span></span>
2.  <span data-ttu-id="32091-149">Windows Media Player öffnet ein modales Fenster, in dem die vom Online Store bereitgestellte Anmelde Webseite angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="32091-149">Windows Media Player opens a modal window that displays the log-in webpage provided by the online store.</span></span>
3.  <span data-ttu-id="32091-150">Die Webseite kommuniziert mit dem Online Store und ist entweder erfolgreich oder kann nicht in den Benutzer protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="32091-150">The webpage communicates with the online store and either succeeds or fails to log in the user.</span></span>
4.  <span data-ttu-id="32091-151">Wenn der Anmeldeversuch erfolgreich ist, benachrichtigt die Webseite das Plug-in des Online Stores durch Aufrufen von " [extern. SendMessage](external-sendmessage.md)", was zu einem Aufruf von " [iwmpcontentpartner:: SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)" führt.</span><span class="sxs-lookup"><span data-stu-id="32091-151">If the log-in attempt succeeds, the webpage notifies the online store's plug-in by calling [External.sendMessage](external-sendmessage.md), which results in a call to [IWMPContentPartner::SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage).</span></span> <span data-ttu-id="32091-152">Das Plug-in für den Online Store ermittelt, dass der Anmeldeversuch erfolgreich war, indem er die an **iwmpcontentpartner:: SendMessage** über gebenden Parameter überprüft.</span><span class="sxs-lookup"><span data-stu-id="32091-152">The online store's plug-in determines that the log-in attempt succeeded by inspecting the parameters passed to **IWMPContentPartner::SendMessage**.</span></span> <span data-ttu-id="32091-153">Diese Parameter werden von Windows Media Player nicht interpretiert. Sie sind nur für den Online Shop von Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="32091-153">Those parameters are not interpreted by Windows Media Player; they have meaning only to the online store.</span></span> <span data-ttu-id="32091-154">Das Plug-in ruft **iwmpcontentpartnercallback:: notify** auf und übergibt Variant \_ true im **boolVal** -Member des *pContext* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="32091-154">The plug-in calls **IWMPContentPartnerCallback::Notify**, passing VARIANT\_TRUE in the **boolVal** member of the *pContext* parameter.</span></span> <span data-ttu-id="32091-155">Wenn bei der Anmeldung ein Fehler auftritt, muss der Online Shop festlegen, wie der Benutzer unterstützt werden soll.</span><span class="sxs-lookup"><span data-stu-id="32091-155">If the log-in fails, the online store must determine how to assist the user.</span></span> <span data-ttu-id="32091-156">Eine Möglichkeit besteht darin, eine neue Webseite im modalen Fenster anzuzeigen, das die Alternative Anmelde Webseite hostet.</span><span class="sxs-lookup"><span data-stu-id="32091-156">One possibility is to display a new webpage in the modal window that hosts the alternative log-in webpage.</span></span>

## <a name="log-out"></a><span data-ttu-id="32091-157">Abmelden</span><span class="sxs-lookup"><span data-stu-id="32091-157">Log-out</span></span>

<span data-ttu-id="32091-158">Der Abmeldevorgang umfasst die folgenden Schritte.</span><span class="sxs-lookup"><span data-stu-id="32091-158">The log-out process involves the following steps.</span></span>

1.  <span data-ttu-id="32091-159">Der Benutzer initiiert einen Abmelde Versuch durch Interaktion mit der Windows Media Player-Benutzeroberfläche oder durch interagieren mit einer Suchseite.</span><span class="sxs-lookup"><span data-stu-id="32091-159">The user initiates a log-out attempt by interacting with the Windows Media Player user interface or by interacting with a discovery page.</span></span>
2.  <span data-ttu-id="32091-160">Windows Media Player ruft [iwmpcontentpartner:: Logout](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout)auf, das durch das Plug-in des Online Stores implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="32091-160">Windows Media Player calls [IWMPContentPartner::Logout](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout), which is implemented by the online store's plug-in.</span></span>
3.  <span data-ttu-id="32091-161">Das Plug-in kommuniziert mit dem Online Store und ist entweder erfolgreich oder kann den Benutzer nicht abmelden.</span><span class="sxs-lookup"><span data-stu-id="32091-161">The plug-in communicates with the online store and either succeeds or fails to log out the user.</span></span>
4.  <span data-ttu-id="32091-162">Wenn der Abmelde Versuch erfolgreich ist, benachrichtigt das Plug-in Windows Media Player durch Aufrufen von **iwmpcontentpartnercallback:: notify** und übergibt Variant \_ false im **boolVal** -Member des *pContext* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="32091-162">If the log-out attempt succeeds, the plug-in notifies Windows Media Player by calling **IWMPContentPartnerCallback::Notify**, passing VARIANT\_FALSE in the **boolVal** member of the *pContext* parameter.</span></span>

<span data-ttu-id="32091-163">Wenn ein Anmeldeversuch erfolgreich war, ruft das Plug-in des Online Stores **iwmpcontentpartnercallback:: notify** auf und übergibt dabei wmpcnloginstatechange im *Typparameter* .</span><span class="sxs-lookup"><span data-stu-id="32091-163">When an attempt to log in or out is successful, the online store's plug-in calls **IWMPContentPartnerCallback::Notify**, passing wmpcnLoginStateChange in the *type* parameter.</span></span> <span data-ttu-id="32091-164">Das Plug-in verwendet den *pContext* -Parameter, um den aktuellen Anmelde Zustand des Benutzers anzugeben.</span><span class="sxs-lookup"><span data-stu-id="32091-164">The plug-in uses the *pContext* parameter to specify the user's current log-in state.</span></span> <span data-ttu-id="32091-165">Wenn das Plug-in *pContext* -> **boolVal** auf Variant \_ true festlegt, wird der Benutzer angemeldet.</span><span class="sxs-lookup"><span data-stu-id="32091-165">If the plug-in sets *pContext*->**boolVal** to VARIANT\_TRUE, the user is logged in.</span></span> <span data-ttu-id="32091-166">Wenn das Plug-in *pContext* -> **boolVal** auf Variant \_ false festlegt, wird der Benutzer abgemeldet. Beachten Sie, dass *pContext* nicht angibt, ob der Versuch erfolgreich war oder fehlgeschlagen ist. Stattdessen gibt Sie den aktuellen Anmelde Zustand des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="32091-166">If the plug-in sets *pContext*->**boolVal** to VARIANT\_FALSE, the user is logged out. Note that *pContext* does not indicate the success or failure of the attempt; rather, it indicates user's current log-in state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32091-167">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="32091-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32091-168">**Extern.-Anmelde Name**</span><span class="sxs-lookup"><span data-stu-id="32091-168">**External.attemptLogin**</span></span>](external-attemptlogin.md)
</dt> <dt>

[<span data-ttu-id="32091-169">**Externes. onloginchange-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="32091-169">**External.OnLoginChange Event**</span></span>](external-onloginchange-event.md)
</dt> <dt>

[<span data-ttu-id="32091-170">**Extern. userloggedin**</span><span class="sxs-lookup"><span data-stu-id="32091-170">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> <dt>

[<span data-ttu-id="32091-171">**Iwmpcontentpartner:: Login**</span><span class="sxs-lookup"><span data-stu-id="32091-171">**IWMPContentPartner::Login**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[<span data-ttu-id="32091-172">**Iwmpcontentpartner:: Logout**</span><span class="sxs-lookup"><span data-stu-id="32091-172">**IWMPContentPartner::Logout**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout)
</dt> <dt>

[<span data-ttu-id="32091-173">**Programmier Handbuch für den Typ 1 Online Stores**</span><span class="sxs-lookup"><span data-stu-id="32091-173">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




