---
title: Validierungs Tests für den onboardingtyp 2 Online Stores
description: In diesem Thema werden Tests beschrieben, die von Microsoft zum Überprüfen des Online Store vom Typ 2 durchgeführt werden. Microsoft erfordert, dass Sie diese Tests ausführen, bevor Sie eine Release Candidate senden. Ihr Online Shop muss die zu veröffentlichenden Tests erfolgreich durchlaufen.
ms.assetid: 1da51772-9711-4913-b05d-830fabe49da2
keywords:
- Windows Media Player Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beefd0945f9d1a9ae61e61f8be74beada1695baf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388360"
---
# <a name="validation-tests-for-on-boarding-type-2-online-stores"></a><span data-ttu-id="3a8cb-106">Validierungs Tests für den onboardingtyp 2 Online Stores</span><span class="sxs-lookup"><span data-stu-id="3a8cb-106">Validation Tests for On-boarding Type 2 Online Stores</span></span>

<span data-ttu-id="3a8cb-107">In diesem Thema werden Tests beschrieben, die von Microsoft zum Überprüfen des Online Store vom Typ 2 durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-107">This topic describes tests that Microsoft will perform to validate your Type 2 online store.</span></span> <span data-ttu-id="3a8cb-108">Microsoft erfordert, dass Sie diese Tests ausführen, bevor Sie eine Release Candidate senden.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-108">Microsoft requires that you run these tests before you submit a release candidate.</span></span> <span data-ttu-id="3a8cb-109">Ihr Online Shop muss die zu veröffentlichenden Tests erfolgreich durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-109">Your online store must successfully pass these tests to be published.</span></span>

> [!Note]  
> <span data-ttu-id="3a8cb-110">Wenn Ihr Speicher vom Typ 1 und nicht vom Typ 2 ist, können Sie dieses Thema als Richtlinie verwenden, um den Umfang der für den Speicher vom Typ 1 behandelten Zertifizierungstests zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-110">If your store is Type 1 rather than Type 2, you can use this topic as a guideline to understand the scope of the certification testing that is covered for Type 1 stores.</span></span> <span data-ttu-id="3a8cb-111">Wenden Sie sich an [Microsoft-Support](https://support.microsoft.com/ph/7763#tab0), um einen umfassenden Satz von Tests für Speicher vom Typ 1 zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-111">For the complete set of tests for Type 1 stores, contact [Microsoft Support](https://support.microsoft.com/ph/7763#tab0).</span></span>

 

<span data-ttu-id="3a8cb-112">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-112">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3a8cb-113">Test Checkliste</span><span class="sxs-lookup"><span data-stu-id="3a8cb-113">Test Checklist</span></span>](#test-checklist)
    -   [<span data-ttu-id="3a8cb-114">Test Durchlauf Vorbereitung</span><span class="sxs-lookup"><span data-stu-id="3a8cb-114">Test Pass Preparation</span></span>](#test-pass-preparation)
-   [<span data-ttu-id="3a8cb-115">Test Umgebung</span><span class="sxs-lookup"><span data-stu-id="3a8cb-115">Test Environment</span></span>](#test-environment)
-   [<span data-ttu-id="3a8cb-116">Konfiguration und Einrichtung</span><span class="sxs-lookup"><span data-stu-id="3a8cb-116">Configuration and Setup</span></span>](#configuration-and-setup)
    -   [<span data-ttu-id="3a8cb-117">Einrichten eines Test Computers</span><span class="sxs-lookup"><span data-stu-id="3a8cb-117">Setting Up a Test Machine</span></span>](#setting-up-a-test-machine)
    -   [<span data-ttu-id="3a8cb-118">Einrichten eines Stores</span><span class="sxs-lookup"><span data-stu-id="3a8cb-118">Setting Up a Store</span></span>](#setting-up-a-store)
    -   [<span data-ttu-id="3a8cb-119">Erstellen eines Kontos</span><span class="sxs-lookup"><span data-stu-id="3a8cb-119">Creating an Account</span></span>](#creating-an-account)
    -   [<span data-ttu-id="3a8cb-120">Einrichten der Zwischenspeicherung von Anmelde Informationen</span><span class="sxs-lookup"><span data-stu-id="3a8cb-120">Setting Up Credential Caching</span></span>](#setting-up-credential-caching)
-   [<span data-ttu-id="3a8cb-121">Inhalts Erfassung</span><span class="sxs-lookup"><span data-stu-id="3a8cb-121">Content Acquisition</span></span>](#content-acquisition)
    -   [<span data-ttu-id="3a8cb-122">Streaming von Inhalten</span><span class="sxs-lookup"><span data-stu-id="3a8cb-122">Streaming Content</span></span>](#streaming-content)
    -   [<span data-ttu-id="3a8cb-123">Abrufen von Inhalten</span><span class="sxs-lookup"><span data-stu-id="3a8cb-123">Obtaining Content</span></span>](#obtaining-content)
    -   [<span data-ttu-id="3a8cb-124">Brennen von Inhalten</span><span class="sxs-lookup"><span data-stu-id="3a8cb-124">Burning Content</span></span>](#burning-content)
    -   [<span data-ttu-id="3a8cb-125">Inhalt wird übertragen</span><span class="sxs-lookup"><span data-stu-id="3a8cb-125">Transferring Content</span></span>](#transferring-content)
-   [<span data-ttu-id="3a8cb-126">Store-Features</span><span class="sxs-lookup"><span data-stu-id="3a8cb-126">Store Features</span></span>](#store-features)
    -   [<span data-ttu-id="3a8cb-127">Verwalten eines Kontos</span><span class="sxs-lookup"><span data-stu-id="3a8cb-127">Managing an Account</span></span>](#managing-an-account)
    -   [<span data-ttu-id="3a8cb-128">Verwalten des Info Centers</span><span class="sxs-lookup"><span data-stu-id="3a8cb-128">Managing the Info Center</span></span>](#managing-the-info-center)
-   [<span data-ttu-id="3a8cb-129">Speichern der Interaktion</span><span class="sxs-lookup"><span data-stu-id="3a8cb-129">Store Interaction</span></span>](#store-interaction)
    -   [<span data-ttu-id="3a8cb-130">Ergebnis des aktiven Stores</span><span class="sxs-lookup"><span data-stu-id="3a8cb-130">Yielding to the Active Store</span></span>](#yielding-to-the-active-store)
    -   [<span data-ttu-id="3a8cb-131">Verhindern, dass der getestete Speicher den aktiven Speicher übernimmt</span><span class="sxs-lookup"><span data-stu-id="3a8cb-131">Preventing the Tested Store From Taking Over the Active Store</span></span>](#preventing-the-tested-store-from-taking-over-the-active-store)
    -   [<span data-ttu-id="3a8cb-132">Zugreifen auf einen Speicher im High-Contrast Modus</span><span class="sxs-lookup"><span data-stu-id="3a8cb-132">Accessing a Store in High-Contrast Mode</span></span>](#accessing-a-store-in-high-contrast-mode)
    -   [<span data-ttu-id="3a8cb-133">Sichern eines Stores</span><span class="sxs-lookup"><span data-stu-id="3a8cb-133">Securing a Store</span></span>](#securing-a-store)

## <a name="test-checklist"></a><span data-ttu-id="3a8cb-134">Test Checkliste</span><span class="sxs-lookup"><span data-stu-id="3a8cb-134">Test Checklist</span></span>

<span data-ttu-id="3a8cb-135">Verwenden Sie die Prüfliste in der folgenden Tabelle, um den Typ 2-Online Shop zu validieren, den Sie in die Platine bringen möchten.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-135">Use the checklist in the following table to validate your Type 2 online store that you wish to bring on board.</span></span>



<span data-ttu-id="3a8cb-136">Test</span><span class="sxs-lookup"><span data-stu-id="3a8cb-136">Test</span></span>

<span data-ttu-id="3a8cb-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3a8cb-137">Windows XP</span></span>

<span data-ttu-id="3a8cb-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a8cb-138">Windows Vista</span></span>

<span data-ttu-id="3a8cb-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3a8cb-139">Windows 7</span></span>

<span data-ttu-id="3a8cb-140">Ergebnis (erfolgreich/Fehler/nicht zutreffend)</span><span class="sxs-lookup"><span data-stu-id="3a8cb-140">Result (pass/fail/not applicable)</span></span>

<span data-ttu-id="3a8cb-141">32</span><span class="sxs-lookup"><span data-stu-id="3a8cb-141">32</span></span>

<span data-ttu-id="3a8cb-142">64</span><span class="sxs-lookup"><span data-stu-id="3a8cb-142">64</span></span>

<span data-ttu-id="3a8cb-143">32</span><span class="sxs-lookup"><span data-stu-id="3a8cb-143">32</span></span>

<span data-ttu-id="3a8cb-144">64</span><span class="sxs-lookup"><span data-stu-id="3a8cb-144">64</span></span>

<span data-ttu-id="3a8cb-145">32</span><span class="sxs-lookup"><span data-stu-id="3a8cb-145">32</span></span>

<span data-ttu-id="3a8cb-146">64</span><span class="sxs-lookup"><span data-stu-id="3a8cb-146">64</span></span>

1. <span data-ttu-id="3a8cb-147">Überprüfen Sie die Installation von Software.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-147">Verify that software installs.</span></span>

2. <span data-ttu-id="3a8cb-148">Überprüfen Sie, ob Software deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-148">Verify that software uninstalls.</span></span>

3. <span data-ttu-id="3a8cb-149">Vergewissern Sie sich, dass die Software nicht in der Taskleiste ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-149">Verify that software does not run in the tray.</span></span>

4. <span data-ttu-id="3a8cb-150">Überprüfen Sie, ob die Registerkarte Store funktioniert.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-150">Verify that the store tab operates.</span></span>

5. <span data-ttu-id="3a8cb-151">Vergewissern Sie sich, dass der Speicher über eine Option zum Erstellen eines neuen Kontos verfügt.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-151">Verify that the store has an option to create a new account.</span></span>

6. <span data-ttu-id="3a8cb-152">Vergewissern Sie sich, dass sich das erstellte Konto anmelden kann.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-152">Verify that the created account can sign in.</span></span>

7. <span data-ttu-id="3a8cb-153">Vergewissern Sie sich, dass der Speicher über eine Option zum Speichern von Benutzerinformationen verfügt.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-153">Verify that the store has an option to save user information.</span></span>

8. <span data-ttu-id="3a8cb-154">Überprüfen Sie, ob das Zwischenspeichern von Anmelde Informationen vorhanden ist und funktioniert</span><span class="sxs-lookup"><span data-stu-id="3a8cb-154">Verify that credential caching is present and working.</span></span>

9. <span data-ttu-id="3a8cb-155">Vergewissern Sie sich, dass der Benutzer zur Eingabe von Anmelde Informationen aufgefordert wird</span><span class="sxs-lookup"><span data-stu-id="3a8cb-155">Verify that the user is prompted for credentials if they are not cached.</span></span>

10. <span data-ttu-id="3a8cb-156">Überprüfen Sie, ob alle verfügbaren Typen von Inhaltsstream vorhanden</span><span class="sxs-lookup"><span data-stu-id="3a8cb-156">Verify that all available types of content stream.</span></span>

11. <span data-ttu-id="3a8cb-157">Überprüfen Sie, ob die Inhalte in Microsoft Windows Media Player abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-157">Verify that content plays in Microsoft Windows Media Player.</span></span>

12. <span data-ttu-id="3a8cb-158">Überprüfen Sie, ob ein berechneter Preis richtig ist.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-158">Verify that a calculated price is correct.</span></span>

13. <span data-ttu-id="3a8cb-159">Überprüfen Sie, ob erworbene Inhalte in die Bibliothek heruntergeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-159">Verify that purchased content is downloaded to the library.</span></span>

14. <span data-ttu-id="3a8cb-160">Vergewissern Sie sich, dass die Metadaten für den Einkauf heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-160">Verify that metadata is downloaded for the purchase.</span></span>

15. <span data-ttu-id="3a8cb-161">Überprüfen Sie, ob die Medien Nutzungsrechte für den Kauf korrekt sind.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-161">Verify that media usage rights are correct for the purchase.</span></span>

16. <span data-ttu-id="3a8cb-162">Überprüfen Sie, ob die erworbenen Inhalte wiedergegeben werden können</span><span class="sxs-lookup"><span data-stu-id="3a8cb-162">Verify that the purchased content can play.</span></span>

17. <span data-ttu-id="3a8cb-163">Vergewissern Sie sich, dass durch Klicken auf **die Schaltfläche** **kaufen oder kaufen** zum Store gewechselt wird.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-163">Verify that clicking the **Buy** or **Shop** button switches to the store.</span></span>

18. <span data-ttu-id="3a8cb-164">Überprüfen Sie, ob erworbene Inhalte heruntergeladen wurden</span><span class="sxs-lookup"><span data-stu-id="3a8cb-164">Verify that purchased content downloaded.</span></span>

19. <span data-ttu-id="3a8cb-165">Überprüfen Sie, ob erworbene Inhalte gebrannt werden können.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-165">Verify that purchased content can be burned.</span></span>

20. <span data-ttu-id="3a8cb-166">Vergewissern Sie sich, dass die Anzahl der Verbrennungen verringert wird.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-166">Verify that the burn count is decremented.</span></span>

21. <span data-ttu-id="3a8cb-167">Überprüfen Sie, ob Inhalt auf einen anderen Computer übertragen werden kann.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-167">Verify that content can be transferred to another computer.</span></span>

22. <span data-ttu-id="3a8cb-168">Überprüfen Sie, ob Inhalt an ein Gerät übertragen wird</span><span class="sxs-lookup"><span data-stu-id="3a8cb-168">Verify that content transfers to a device.</span></span>

23. <span data-ttu-id="3a8cb-169">Vergewissern Sie sich, dass die Synchronisierungs Anzahl dekrementiert wird.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-169">Verify that the sync count is decremented.</span></span>

24. <span data-ttu-id="3a8cb-170">Vergewissern Sie sich, dass der Kaufverlauf vorherige Käufe nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-170">Verify that the purchase history tracks prior purchases.</span></span>

25. <span data-ttu-id="3a8cb-171">Überprüfen Sie, ob ein vorheriger Kauf wieder hergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-171">Verify that a prior purchase can be restored.</span></span>

26. <span data-ttu-id="3a8cb-172">Überprüfen Sie die Funktionalität eines Stores, um mehrere Computer zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-172">Verify a store's functionality to manage multiple computers.</span></span>

27. <span data-ttu-id="3a8cb-173">Vergewissern Sie sich, dass das Info Center standardmäßig deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-173">Verify that the Info Center is off by default.</span></span>

28. <span data-ttu-id="3a8cb-174">Überprüfen Sie, ob das Info Center über Medieninformationen im Bereich der nun Wiedergabe verfügt.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-174">Verify that the Info Center has media information in the now-playing area.</span></span>

29. <span data-ttu-id="3a8cb-175">Überprüfen Sie, ob die Links zum Speicher navigieren.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-175">Verify that links navigate to the store.</span></span>

30. <span data-ttu-id="3a8cb-176">Vergewissern Sie sich, dass der getestete Speicher den aktiven Speicher liefert.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-176">Verify that the tested store yields to the active store.</span></span>

31. <span data-ttu-id="3a8cb-177">Vergewissern Sie sich, dass der getestete Speicher den aktuellen Speicher nicht übernehmen kann.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-177">Verify that the tested store does not take over the current store.</span></span>

32. <span data-ttu-id="3a8cb-178">Vergewissern Sie sich, dass der Speicher im Modus mit hohem Kontrast verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-178">Verify that the store is accessible in high-contrast mode.</span></span>

33. <span data-ttu-id="3a8cb-179">Vergewissern Sie sich, dass der Speicher sicher ist.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-179">Verify that the store is secure.</span></span>



 

### <a name="test-pass-preparation"></a><span data-ttu-id="3a8cb-180">Test Durchlauf Vorbereitung</span><span class="sxs-lookup"><span data-stu-id="3a8cb-180">Test Pass Preparation</span></span>

<span data-ttu-id="3a8cb-181">Bevor Sie einen Test Durchlauf ausführen, sollten Sie sicherstellen, dass die Speicher-und Testkonten zum Testen bereit sind.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-181">Before you run a test pass, you should ensure that the store and the test accounts are ready for testing.</span></span> <span data-ttu-id="3a8cb-182">Sie sollten die folgenden Informationen bestimmen, bevor der Pass gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-182">You should determine the following information before the pass starts.</span></span> <span data-ttu-id="3a8cb-183">Wenn Sie die Informationen einige Tage vor dem Test Durchlauf ermitteln können, wird der Durchlauf effizienter ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-183">If you can determine the information some days in advance of the test pass, the pass will run more efficiently.</span></span>

-   <span data-ttu-id="3a8cb-184">Bestimmen Sie die folgenden Informationen zu Testkonten, die vom Speicher bereitgestellt werden:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-184">Determine the following information about test accounts that are supplied by the store:</span></span>
    -   <span data-ttu-id="3a8cb-185">Konten und Kenn Wörter funktionieren, damit sich ein Benutzer anmelden kann</span><span class="sxs-lookup"><span data-stu-id="3a8cb-185">Accounts and passwords work to allow a user to sign in</span></span>
    -   <span data-ttu-id="3a8cb-186">Konten werden für jeden Typ von Geschäfts Modus, den der Store anbietet, ordnungsgemäß und angemessen finanziert.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-186">Accounts are correctly and adequately funded for each type of business mode the store offers</span></span>
    -   <span data-ttu-id="3a8cb-187">Konten sind für alle zu testenden Gebiets Schemas gültig, oder für jedes Gebiets Schema sind Konten vorhanden, wenn Konten keine Gebiets Schema übergreifende</span><span class="sxs-lookup"><span data-stu-id="3a8cb-187">Accounts are valid for all locales to be tested, or accounts exist for each locale if accounts cannot cross locales</span></span>
-   <span data-ttu-id="3a8cb-188">Bestimmen Sie, welche Gebiets Schemata getestet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-188">Determine which locales to test.</span></span>
-   <span data-ttu-id="3a8cb-189">Bestimmen Sie, welche Sprachen getestet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-189">Determine which languages to test.</span></span>
-   <span data-ttu-id="3a8cb-190">Bestimmen Sie die folgenden Informationen zur Testumgebung:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-190">Determine the following information about the test environment:</span></span>

    -   <span data-ttu-id="3a8cb-191">Live Stores, die mit Windows XP, Windows Vista und Windows 7 zusammenarbeiten</span><span class="sxs-lookup"><span data-stu-id="3a8cb-191">Live stores that work with Windows XP, Windows Vista, and Windows 7</span></span>
    -   <span data-ttu-id="3a8cb-192">Der zu testende nicht-Live Store</span><span class="sxs-lookup"><span data-stu-id="3a8cb-192">The non-live store to test</span></span>
    -   <span data-ttu-id="3a8cb-193">Vergewissern Sie sich, dass der zu testende Non-Live Store in allen Versionen des Betriebssystems und allen Versionen der Windows Media Player-Plattform sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-193">Verify that the non-live store to test is visible in all versions of the operating system and all versions of the Windows Media Player platform.</span></span>

-   <span data-ttu-id="3a8cb-194">Bestimmen Sie die folgenden Informationen zum zu testenden Speicher:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-194">Determine the following information about the store to test:</span></span>

    -   <span data-ttu-id="3a8cb-195">Name des Datenspeichers</span><span class="sxs-lookup"><span data-stu-id="3a8cb-195">Store name</span></span>
    -   <span data-ttu-id="3a8cb-196">Erwartete Logo Grafiken und Bezeichnung für Store-Registerkarten</span><span class="sxs-lookup"><span data-stu-id="3a8cb-196">Expected store tab logo graphics and label</span></span>
    -   <span data-ttu-id="3a8cb-197">Ist der Speicher für alle Betriebssystemversionen Live?</span><span class="sxs-lookup"><span data-stu-id="3a8cb-197">Is the store live for all operating system versions?</span></span>
    -   <span data-ttu-id="3a8cb-198">Handelt es sich hierbei um eine neue Version des zu testenden Stores?</span><span class="sxs-lookup"><span data-stu-id="3a8cb-198">Is this is a new version of the store under test?</span></span>
    -   <span data-ttu-id="3a8cb-199">Wird der zu testende Speicher vom Typ 1 oder vom Typ 2 gespeichert?</span><span class="sxs-lookup"><span data-stu-id="3a8cb-199">Is the store under test a Type 1 or Type 2 store?</span></span>
    -   <span data-ttu-id="3a8cb-200">Hat sich der Store-Typ geändert?</span><span class="sxs-lookup"><span data-stu-id="3a8cb-200">Has the store type changed?</span></span>

-   <span data-ttu-id="3a8cb-201">Bestimmen Sie, auf welchen Betriebssystemversionen und Plattformen Sie den Speicher testen möchten.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-201">Determine on which operating system versions and platforms you plan to test the store.</span></span>
-   <span data-ttu-id="3a8cb-202">Stellen Sie fest, dass das Installationsprogramm und das Plug-in auf allen zu testenden Betriebssystemversionen und-Plattformen funktionieren.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-202">Determine that the installer and plug-in works on all operating system versions and platforms to be tested.</span></span>
-   <span data-ttu-id="3a8cb-203">Stellen Sie fest, ob ein Navigations Dokument erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-203">Determine if a navigation document is required.</span></span>
-   <span data-ttu-id="3a8cb-204">Bestimmen Sie die folgenden Informationen zu den Medien, die im Store angeboten werden:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-204">Determine the following information about the media that the store offers:</span></span>

    -   <span data-ttu-id="3a8cb-205">Formate</span><span class="sxs-lookup"><span data-stu-id="3a8cb-205">Formats</span></span>
    -   <span data-ttu-id="3a8cb-206">Ist eine proprietäre Software erforderlich?</span><span class="sxs-lookup"><span data-stu-id="3a8cb-206">Is any proprietary software required?</span></span>
    -   <span data-ttu-id="3a8cb-207">Müssen Sie alle Medientypen oder nur eine Teilmenge der Medientypen testen?</span><span class="sxs-lookup"><span data-stu-id="3a8cb-207">Must you test all media types, or only a subset of media types?</span></span>

-   <span data-ttu-id="3a8cb-208">Bestimmen Sie die folgenden Informationen zu den Medien Nutzungsrechten:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-208">Determine the following information about media usage rights:</span></span>

    -   <span data-ttu-id="3a8cb-209">Verfügen die Store-Medien über Inhalts Schutz?</span><span class="sxs-lookup"><span data-stu-id="3a8cb-209">Does the store media have content protection?</span></span>
    -   <span data-ttu-id="3a8cb-210">Wenn dies der Fall ist, bestimmen Sie den Typ des Inhalts Schutzes, den die Medien besitzen.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-210">If so, determine the type of content protection that the media have.</span></span>
    -   <span data-ttu-id="3a8cb-211">Wenn dies der Fall ist, bestimmen Sie das erwartete geschützte Verhalten.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-211">If so, determine the expected protected behavior.</span></span>
    -   <span data-ttu-id="3a8cb-212">Beinhalten die Nutzungsrechte für die Medien die Computer-zu-Computer-Freigabe?</span><span class="sxs-lookup"><span data-stu-id="3a8cb-212">Do the media usage rights include computer-to-computer sharing?</span></span>
    -   <span data-ttu-id="3a8cb-213">Die Synchronisierungs Rechte</span><span class="sxs-lookup"><span data-stu-id="3a8cb-213">The sync rights</span></span>
    -   <span data-ttu-id="3a8cb-214">Die Verbrauchs Rechte</span><span class="sxs-lookup"><span data-stu-id="3a8cb-214">The burn rights</span></span>
    -   <span data-ttu-id="3a8cb-215">Die Wiedergabe Rechte</span><span class="sxs-lookup"><span data-stu-id="3a8cb-215">The play rights</span></span>
    -   <span data-ttu-id="3a8cb-216">Die Ablaufdatums Angaben (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="3a8cb-216">The expiration dates, if any</span></span>

-   <span data-ttu-id="3a8cb-217">Stellen Sie fest, ob Sie über ausreichend Medien (einen ausreichend großen Katalog) verfügen, um ein aussagekräftiges Beispiel zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-217">Determine if you have sufficient media (a large enough catalog) to provide a meaningful sample.</span></span>
-   <span data-ttu-id="3a8cb-218">Bestimmen Sie, was der Phasen Durchlauf ist: RC 0, Compliance usw.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-218">Determine what the stage pass is: RC 0, compliance, and so on.</span></span>
-   <span data-ttu-id="3a8cb-219">Bestimmen Sie, ob es sich bei dem Test Durchlauf um einen bestimmten Typ handelt: Regression, Rauch usw.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-219">Determine if the test pass is a certain type: regression, smoke, and so on.</span></span>

## <a name="test-environment"></a><span data-ttu-id="3a8cb-220">Testumgebung</span><span class="sxs-lookup"><span data-stu-id="3a8cb-220">Test Environment</span></span>

<span data-ttu-id="3a8cb-221">Sie müssen Tests für die folgenden Konfigurationen durchführen:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-221">You must conduct testing on the following configurations:</span></span>

-   <span data-ttu-id="3a8cb-222">Microsoft Windows Media Player 11 unter Windows XP mit Service Pack 3 (SP3) 32-Bit-und 64-Bit-Betriebssystemen</span><span class="sxs-lookup"><span data-stu-id="3a8cb-222">Microsoft Windows Media Player 11 on Windows XP with Service Pack 3 (SP3) 32-bit and 64-bit operating systems</span></span>
-   <span data-ttu-id="3a8cb-223">Windows Media Player 11 unter Windows Vista 32-Bit-und 64-Bit-Betriebssysteme (32-Bit Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="3a8cb-223">Windows Media Player 11 on Windows Vista 32-bit and 64-bit (32-bit Windows Media Player) operating systems</span></span>
-   <span data-ttu-id="3a8cb-224">Betriebssysteme Microsoft Windows Media Player 12 auf Windows 7 32-Bit und 64-Bit (32-Bit Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="3a8cb-224">Microsoft Windows Media Player 12 on Windows 7 32-bit and 64-bit (32-bit Windows Media Player) operating systems</span></span>

<span data-ttu-id="3a8cb-225">Obwohl Sie Tests für alle aufgeführten Betriebssystemversionen und Plattformen durchführen müssen, sind die 32-Bit-Versionen von Windows Vista und Windows 7 die Prioritäts orientierten Betriebssystemversionen.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-225">Although you must perform testing on all the operating system versions and platforms listed, 32-bit versions of Windows Vista and Windows 7 are the priority targeted operating system versions.</span></span> <span data-ttu-id="3a8cb-226">Sie müssen die Installation von Software auf allen Plattformen testen.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-226">You must test the installation of any software on all platforms.</span></span>

<span data-ttu-id="3a8cb-227">In den Screenshots in diesem Thema wird die Verwendung der Benutzeroberfläche mithilfe eines fiktiven Stores (Proseware) veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-227">Screen shots in this topic use a fictitious store, Proseware, to demonstrate the usage of the user interface.</span></span>

## <a name="configuration-and-setup"></a><span data-ttu-id="3a8cb-228">Konfiguration und Setup</span><span class="sxs-lookup"><span data-stu-id="3a8cb-228">Configuration and Setup</span></span>

<span data-ttu-id="3a8cb-229">In den folgenden Abschnitten wird beschrieben, wie Sie Validierungstests für den Online Shop eines Typs 2 konfigurieren und einrichten.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-229">The following sections describe how to configure and set up validation testing to on-board a Type 2 online store.</span></span>

### <a name="setting-up-a-test-machine"></a><span data-ttu-id="3a8cb-230">Einrichten eines Test Computers</span><span class="sxs-lookup"><span data-stu-id="3a8cb-230">Setting Up a Test Machine</span></span>

<span data-ttu-id="3a8cb-231">Führen Sie die folgenden Schritte aus, um einen Testcomputer einzurichten:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-231">Perform the following steps to set up a test machine:</span></span>

1.  <span data-ttu-id="3a8cb-232">Zeigen Sie den Testcomputer auf Inhalts Testserver, indem Sie einen Speicher spezifischen Registrierungsschlüssel hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-232">Point the test computer to content test servers by adding a store-specific registry key.</span></span>
2.  <span data-ttu-id="3a8cb-233">Legen Sie die Werte im Dialogfeld Regions **-und Sprachoptionen** auf die richtigen sprach-und Gebiets Schema Einstellungen fest.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-233">Set values in the **Regional and Language Options** dialog box to the proper language and locale settings.</span></span> <span data-ttu-id="3a8cb-234">Um die Sprache festzulegen, wählen Sie die Registerkarte **Formate** aus, und wählen Sie dann die Sprache aus dem Kombinations Feld **Aktuelles Format** aus.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-234">To set the language, select the **Formats** tab and then select the language from the **Current format** combo box.</span></span> <span data-ttu-id="3a8cb-235">Um den Bereich festzulegen, wählen Sie die Registerkarte **Speicherort** aus, und wählen Sie dann die Region im Kombinations Feld **Aktueller Speicherort** aus.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-235">To set the region, select the **Location** tab and then select the region from the **Current location** combo box.</span></span> <span data-ttu-id="3a8cb-236">Außerdem müssen Sie für Speicher, die eine Installation eines Plug-ins oder einer Speicher spezifischen, benutzerdefinierten Software erfordern, möglicherweise das System Gebiets Schema in die Sprache des Gebiets Schemas des Speichers ändern, um die Installation zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-236">Additionally, for stores that require installation of a plug-in or store-specific custom software, you might need to change the system locale to the language of the store's locale to facilitate installation.</span></span> <span data-ttu-id="3a8cb-237">Das Software Installationsprogramm muss sowohl Einzel-als auch Doppelbyte-Zeichen unterstützen und muss in jedem Gebiets Schema ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-237">The software installer must support both single and double byte characters and must run on any locale.</span></span> <span data-ttu-id="3a8cb-238">Sie müssen im systemeigenen Gebiets Schema testen.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-238">You must test in the native locale.</span></span> <span data-ttu-id="3a8cb-239">Um das Native Gebiets Schema festzulegen, öffnen Sie das Dialogfeld **Region und Sprache** , wählen Sie die Registerkarte **Verwaltung** aus, und klicken Sie dann auf die Schaltfläche System Gebiets Schema **ändern** , wie im folgenden Screenshot gezeigt.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-239">To set the native locale, open the **Region and Language** dialog box, select the **Administrative** tab, and then click the **Change system locale** button as shown in the following screen shot.</span></span> <span data-ttu-id="3a8cb-240">Durch Klicken auf diese Schaltfläche wird das Dialogfeld **Regions-und Spracheinstellungen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-240">Clicking this button displays the **Region and Language Settings** dialog box.</span></span> <span data-ttu-id="3a8cb-241">Das **aktuelle System** Gebiets Schema-Kombinations Feld in diesem Dialogfeld ändert das System Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-241">The **Current system locale** combo box in that dialog box changes the system locale.</span></span>

    <span data-ttu-id="3a8cb-242">Die folgenden Screenshots zeigen die Registerkarten, auf denen Sie Region und Sprache festlegen können:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-242">The following screen shots show the tabs on which you can set region and language:</span></span>

    ![Screenshot des Dialog Felds "Regions-und Sprachoptionen"](images/reg-lang-opt.png)

    ![Screenshot, der zeigt, wie das aktuelle System Gebiets Schema geändert wird](images/reg-lang-settings.png)

3.  <span data-ttu-id="3a8cb-245">Deaktivieren Sie die Ansicht des Informations Centers eines Informations Centers, indem Sie Windows Media Player festlegen, um eine Visualisierung wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-245">Turn off the view of a store's Info Center by setting Windows Media Player to play a visualization.</span></span> <span data-ttu-id="3a8cb-246">Der Hauptunterschied zwischen den Plattformen besteht darin, dass Sie in Windows Media Player 11 zunächst auf " **abspielen**" klicken, während Sie in Windows Media Player 12 zunächst mit der rechten Maustaste auf das Hauptfenster klicken.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-246">The main difference between the platforms is that in Windows Media Player 11, you start by clicking **Now Playing**, whereas in Windows Media Player 12, you start by right-clicking the main window.</span></span>

    <span data-ttu-id="3a8cb-247">Der folgende Screenshot zeigt die Reihenfolge der Menü Optionen, die eine Visualisierung in Windows Media Player 11 wieder gibt:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-247">The following screen shot shows the sequence of menu options that plays a visualization in Windows Media Player 11:</span></span>

    ![Screenshot, der zeigt, wie Sie eine Visualisierung in Windows Media Player 11 abspielen](images/wmp11-visual.png)

    <span data-ttu-id="3a8cb-249">Der folgende Screenshot zeigt die Reihenfolge der Menü Optionen, die eine Visualisierung in Windows Media Player 12 wieder gibt:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-249">The following screen shot shows the sequence of menu options that plays a visualization in Windows Media Player 12:</span></span>

    ![Screenshot, der zeigt, wie Sie eine Visualisierung in Windows Media Player 12 abspielen](images/wmp12-visual.png)

### <a name="setting-up-a-store"></a><span data-ttu-id="3a8cb-251">Einrichten eines Stores</span><span class="sxs-lookup"><span data-stu-id="3a8cb-251">Setting Up a Store</span></span>

<span data-ttu-id="3a8cb-252">Führen Sie zuerst die folgenden Schritte aus, um einen Speicher einzurichten, und führen Sie dann die Schritte aus, die die ersten Schritte zum Überprüfen der Speicher Einrichtung ausführen:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-252">First perform the following steps to set up a store, and then perform the steps that follow the initial steps to verify the store setup:</span></span>

1.  <span data-ttu-id="3a8cb-253">Starten Sie Windows Media Player, und warten Sie einige Sekunden, bis die aktuelle AllServices.xml Datei abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-253">Launch Windows Media Player and wait several seconds to acquire the latest AllServices.xml file.</span></span>
2.  <span data-ttu-id="3a8cb-254">Wenn Sie für Windows XP und Windows Vista einen Online Shop auswählen möchten, klicken Sie zuerst auf die Registerkarte, die zwischen der Medien Leit Faden Ansicht und der Ansicht der Online Filialen aufgeteilt wird.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-254">For Windows XP and Windows Vista, to select an online store, first click the tab that splits between the Media Guide view and the Online Stores view.</span></span> <span data-ttu-id="3a8cb-255">Klicken Sie dann im Menü auf **alle Online Stores durchsuchen**, und wählen Sie den Store aus, indem Sie in der Liste der Filialen auf das entsprechende Symbol klicken.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-255">Then, from the menu click **Browse all Online Stores**, and select the store by clicking its icon in the list of stores.</span></span> <span data-ttu-id="3a8cb-256">Klicken Sie für Windows 7 im Navigationsbereich der Bibliothek auf die Schaltfläche, die zwischen der Schaltfläche **Medienhandbuch** und der Schaltfläche **Online Stores** aufgeteilt wird.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-256">For Windows 7, click the button in the library-navigation pane that splits between the **Media Guide** button and the **Online Stores** button.</span></span> <span data-ttu-id="3a8cb-257">Klicken Sie dann im Menü auf **alle Online Stores durchsuchen**, und wählen Sie den Store aus, indem Sie in der Liste der Filialen auf das entsprechende Symbol klicken.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-257">Then, from the menu click **Browse all online stores**, and select the store by clicking its icon in the list of stores.</span></span>

    <span data-ttu-id="3a8cb-258">Der folgende Screenshot zeigt, wie ein Online Store in Windows Media Player 11 ausgewählt wird:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-258">The following screen shot shows how to select an online store in Windows Media Player 11:</span></span>

    ![Screenshot, der zeigt, wie Sie einen Online Shop in Windows Media Player 11 auswählen](images/wmp11-set-store.png)

    <span data-ttu-id="3a8cb-260">Der folgende Screenshot zeigt, wie Sie einen Online Shop in Windows Media Player 12 auswählen:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-260">The following screen shot shows how to select an Online Store in Windows Media Player 12:</span></span>

    ![Screenshot, der zeigt, wie Sie einen Online Shop in Windows Media Player 12 auswählen](images/wmp12-set-store.png)

3.  <span data-ttu-id="3a8cb-262">Befolgen Sie die Anweisungen aus dem Store, um zusätzliche Software zu installieren, die für die Verwendung des Stores benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-262">Follow instructions from the store to install any additional software that is needed to use the store.</span></span>

<span data-ttu-id="3a8cb-263">**So überprüfen Sie die Speicher Einrichtung**</span><span class="sxs-lookup"><span data-stu-id="3a8cb-263">**To verify store setup**</span></span>

1.  <span data-ttu-id="3a8cb-264">Überprüfen Sie, ob die Software installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-264">Verify that the software installs.</span></span>

    <span data-ttu-id="3a8cb-265">Vergewissern Sie sich, dass das OCX-Plug-in oder eine beliebige andere Software aus dem Store ohne Fehler heruntergeladen und installiert wird.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-265">Verify that the OCX plug-in or any other software from the store downloads and installs without error.</span></span>

2.  <span data-ttu-id="3a8cb-266">Überprüfen Sie, ob die Software deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-266">Verify that the software uninstalls.</span></span>

    <span data-ttu-id="3a8cb-267">Überprüfen Sie, ob in der Systemsteuerung unter **Programme und Funktionen** die Software, die der Speicher installiert, in der Liste **Programm deinstallieren oder ändern** angezeigt wird, und vergewissern Sie sich, dass Sie Sie ohne Fehler aus dieser Liste deinstallieren können.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-267">Verify that in Control Panel, in the **Programs and Features** item, the software that the store installs appears in the **Uninstall or change a program** list, and verify that you can uninstall it from this list without error.</span></span>

3.  <span data-ttu-id="3a8cb-268">Vergewissern Sie sich, dass die Software nicht in der Taskleiste ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-268">Verify that software does not run in the system tray.</span></span>

    <span data-ttu-id="3a8cb-269">Stellen Sie sicher, dass keine der Software aus dem Store Symbole zum Programm Benachrichtigungsbereich hinzufügt (auf der Taskleiste auf der linken Seite der Uhr), bevor die Kunden Zustimmung zum Herunterladen von Store-Software hat.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-269">Verify that none of the software from the store adds icons to the program notification area (on the Taskbar to the left of the clock) prior to customer consent to download store software.</span></span>

    <span data-ttu-id="3a8cb-270">Für den grundlegenden Speicherbedarf sollte die Installation zusätzlicher Software nicht erforderlich sein.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-270">The basic store experience should not require installation of additional software.</span></span> <span data-ttu-id="3a8cb-271">Es sollte eine grundlegende Mediendarstellung (z. b. Streaming-Medien) verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-271">A basic media experience, such as streaming media, should be available.</span></span> <span data-ttu-id="3a8cb-272">Einige Geschäfte installieren zusätzliche Software, z. b. Download-Manager für die Premier-Medien. Diese Speicher können Symbole in der Taskleiste aufweisen, wenn die Symbole Anwendungen darstellen, die von Windows Media Player getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-272">Some stores install additional software such as download managers for a premier media experience; these stores can have icons in the system tray if the icons represent applications that are separate from Windows Media Player.</span></span>

4.  <span data-ttu-id="3a8cb-273">Überprüfen Sie, ob die Registerkarte Store funktioniert.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-273">Verify that the store tab operates.</span></span>

    <span data-ttu-id="3a8cb-274">Überprüfen Sie, ob sich die Registerkarte "Store" ändert, um den ausgewählten Speicher</span><span class="sxs-lookup"><span data-stu-id="3a8cb-274">Verify that the store tab changes to indicate the selected store.</span></span>

    <span data-ttu-id="3a8cb-275">Stellen Sie für Windows XP und Windows Vista mit Windows Media Player 11 sicher, dass der Name und das Symbol des Stores für den dunklen Fenster Media Player 11-Hintergrund sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-275">For Windows XP and Windows Vista with Windows Media Player 11, verify that the store name and icon are visible against the dark Windows Media Player 11 background.</span></span>

    <span data-ttu-id="3a8cb-276">Vergewissern Sie sich bei Windows 7 mit Windows Media Player 12, dass der Name und das Symbol des Geschäfts im Navigationsbereich der Bibliothek im Kontextmenü für die Dienst Auswahl angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-276">For Windows 7 with Windows Media Player 12, verify the store name and icon are visible in the library-navigation pane, in the service-selector context menu.</span></span>

    <span data-ttu-id="3a8cb-277">Vergewissern Sie sich, dass der Speicher im Menü am oberen Rand der Liste der Store-Selektoren aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-277">Verify that the store is listed at the top of the store selector list in the menu.</span></span>

    > [!Note]  
    > <span data-ttu-id="3a8cb-278">Es wird keine Menüoption " **aktuellen Dienst hinzufügen** " angezeigt, wenn der Typ 2-Speicher der für die Region vorgestellte (Standard-) Speicher ist.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-278">There will be no **Add current service to menu** option if the Type 2 store is the featured (default) store for the region.</span></span>

     

    <span data-ttu-id="3a8cb-279">Der folgende Screenshot zeigt das Menü, das angezeigt wird, wenn Sie auf die Registerkarte in der oberen rechten Ecke von Windows Media Player 11 klicken:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-279">The following screen shot shows the menu that appears when you click the tab at the top right corner of Windows Media Player 11:</span></span>

    ![Screenshot mit der Registerkarte "Store" in Windows Media Player 11](images/wmp11-verify-store.png)

    <span data-ttu-id="3a8cb-281">Der folgende Screenshot zeigt das Menü, das angezeigt wird, wenn Sie in der unteren linken Ecke von Windows Media Player 12 auf die unterteilte Schaltfläche klicken:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-281">The following screen shot shows the menu that appears when you click the split button at the lower left corner of Windows Media Player 12:</span></span>

    ![Screenshot mit der Registerkarte "Store" in Windows Media Player 12](images/wmp12-verify-store.png)

### <a name="creating-an-account"></a><span data-ttu-id="3a8cb-283">Erstellen eines Kontos</span><span class="sxs-lookup"><span data-stu-id="3a8cb-283">Creating an Account</span></span>

<span data-ttu-id="3a8cb-284">**So überprüfen Sie die Konto Einrichtung**</span><span class="sxs-lookup"><span data-stu-id="3a8cb-284">**To verify account setup**</span></span>

1.  <span data-ttu-id="3a8cb-285">Vergewissern Sie sich, dass der Speicher über eine Option zum Erstellen eines neuen Kontos verfügt, und befolgen Sie dann die Anweisungen im Store, um ein neues Konto zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-285">Verify that the store has an option to create a new account, and then follow the store instructions to create a new account.</span></span>

    <span data-ttu-id="3a8cb-286">Der folgende Screenshot zeigt die Schaltfläche **Neues Konto erstellen** , wie Sie in Windows Media Player 11 angezeigt werden kann:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-286">The following screen shot highlights a **Create New Account** button as it might appear in Windows Media Player 11:</span></span>

    ![Screenshot, der zeigt, wie Sie die Konto Einrichtung für Windows Media Player 11 überprüfen](images/wmp11-verify-account.png)

    <span data-ttu-id="3a8cb-288">Der folgende Screenshot zeigt die Schaltfläche **Neues Konto erstellen** , wie Sie in Windows Media Player 12 angezeigt werden kann:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-288">The following screen shot highlights a **Create New Account** button as it might appear in Windows Media Player 12:</span></span>

    ![Screenshot, der zeigt, wie Sie die Konto Einrichtung für Windows Media Player 12 überprüfen](images/wmp12-verify-account.png)

2.  <span data-ttu-id="3a8cb-290">Vergewissern Sie sich, dass Sie sich bei dem Konto anmelden können, das Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-290">Verify that you can sign in to the account that you created.</span></span>

### <a name="setting-up-credential-caching"></a><span data-ttu-id="3a8cb-291">Einrichten der Zwischenspeicherung von Anmelde Informationen</span><span class="sxs-lookup"><span data-stu-id="3a8cb-291">Setting Up Credential Caching</span></span>

<span data-ttu-id="3a8cb-292">Führen Sie zuerst die folgenden Schritte aus, um das Zwischenspeichern von Anmelde Informationen einzurichten, und führen Sie dann die Schritte aus, die den ersten Schritten folgen, um die Einrichtung der Anmelde Informationen zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-292">First perform the following steps to set up credential caching, and then perform the steps that follow the initial steps to verify the credential-caching setup:</span></span>

1.  <span data-ttu-id="3a8cb-293">Geben Sie auf der Anmeldeseite die Anmelde Informationen ein, und wählen Sie die Option zum Speichern von Benutzerinformationen aus.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-293">At the sign-in page, enter credentials and select the option to save user information.</span></span>
2.  <span data-ttu-id="3a8cb-294">Vergewissern Sie sich, dass auf der Anmeldeseite ein Kontrollkästchen für den Benutzer zum Zwischenspeichern von Anmelde Informationen zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-294">Verify that the sign-in page has a check box that allows the user to cache credentials.</span></span>
3.  <span data-ttu-id="3a8cb-295">Die optionale Zwischenspeicherung von Anmelde Informationen ist ein wichtiger Sicherheitsaspekt.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-295">Optional credential caching is an important security point.</span></span> <span data-ttu-id="3a8cb-296">Das automatische Zwischenspeichern von Anmelde Informationen kann personenbezogene Informationen von Benutzern verfügbar machen, die sich bei einem freigegebenen oder öffentlichen Computer anmelden.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-296">Automatic credential caching can expose personally identifiable information of users who sign into a shared or public computer.</span></span> <span data-ttu-id="3a8cb-297">Sie sollten Kundeninformationen schützen, indem Sie ein Kontrollkästchen anbieten, das das Caching optional rendert.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-297">You should protect customer information by offering a check box that renders the caching optional.</span></span>

<span data-ttu-id="3a8cb-298">**Überprüfen der Zwischenspeicherung von Anmelde Informationen**</span><span class="sxs-lookup"><span data-stu-id="3a8cb-298">**To verify credential caching**</span></span>

1.  <span data-ttu-id="3a8cb-299">Vergewissern Sie sich, dass der Speicher über ein Kontrollkästchen für die Option **meine Benutzerinformationen speichern** verfügt.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-299">Verify that the store has a check box for a **Save my user information** option.</span></span>

    1.  <span data-ttu-id="3a8cb-300">Schließen Sie Windows-Media Player.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-300">Close Windows Media Player.</span></span>
    2.  <span data-ttu-id="3a8cb-301">Öffnen Sie Windows Media Player erneut, und versuchen Sie, Inhalte herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-301">Reopen Windows Media Player and attempt to download some content.</span></span>

2.  <span data-ttu-id="3a8cb-302">Überprüfen Sie, ob das Zwischenspeichern von Anmelde Informationen vorhanden ist und funktioniert</span><span class="sxs-lookup"><span data-stu-id="3a8cb-302">Verify that credential caching is present and working.</span></span>

    1.  <span data-ttu-id="3a8cb-303">Melden Sie sich beim Store ab.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-303">Sign out of the store.</span></span>
    2.  <span data-ttu-id="3a8cb-304">Schließen Sie Windows-Media Player.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-304">Close Windows Media Player.</span></span>
    3.  <span data-ttu-id="3a8cb-305">Öffnen Sie Windows Media Player erneut, und versuchen Sie, Inhalte herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-305">Reopen Windows Media Player and attempt to download some content.</span></span>

3.  <span data-ttu-id="3a8cb-306">Vergewissern Sie sich, dass der Benutzer zur Eingabe von Anmelde Informationen aufgefordert wird</span><span class="sxs-lookup"><span data-stu-id="3a8cb-306">Verify that the user is prompted for credentials if they are not cached.</span></span>

    <span data-ttu-id="3a8cb-307">Nach der Abmeldung und dem anschließenden Versuch, den Speicher zu verwenden, sollte der Kunde zur Eingabe von Anmelde Informationen aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-307">After signing out and then trying to use the store, the customer should be prompted for credentials.</span></span>

## <a name="content-acquisition"></a><span data-ttu-id="3a8cb-308">Inhalts Erfassung</span><span class="sxs-lookup"><span data-stu-id="3a8cb-308">Content Acquisition</span></span>

<span data-ttu-id="3a8cb-309">In diesem Abschnitt werden die verschiedenen Möglichkeiten zum Abrufen von Inhalten beschrieben und erläutert, wie Sie überprüfen können, ob dieser Inhalt abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-309">This section describes the various ways to acquire content and how to verify that that content was acquired.</span></span>

### <a name="streaming-content"></a><span data-ttu-id="3a8cb-310">Streaming von Inhalten</span><span class="sxs-lookup"><span data-stu-id="3a8cb-310">Streaming Content</span></span>

<span data-ttu-id="3a8cb-311">Streamen Sie alle verfügbaren Inhaltstypen aus dem Speicher.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-311">Stream all available types of content from the store.</span></span> <span data-ttu-id="3a8cb-312">Beispiel: Streamen von Radio-, Video-, Audio-und Vorschau Inhalt.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-312">For example, stream radio, video, audio, and previews content.</span></span>

<span data-ttu-id="3a8cb-313">**So überprüfen Sie Streaminginhalte**</span><span class="sxs-lookup"><span data-stu-id="3a8cb-313">**To verify streaming content**</span></span>

1.  <span data-ttu-id="3a8cb-314">Überprüfen Sie, ob alle verfügbaren Typen von Inhaltsstream vorhanden</span><span class="sxs-lookup"><span data-stu-id="3a8cb-314">Verify that all available types of content stream.</span></span>

2.  <span data-ttu-id="3a8cb-315">Überprüfen Sie, ob der Inhalt in Windows Media Player und nicht in einem anderen Player oder Steuerelement abgespielt wird.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-315">Verify that content plays in Windows Media Player and not some other player or control.</span></span>

### <a name="obtaining-content"></a><span data-ttu-id="3a8cb-316">Abrufen von Inhalten</span><span class="sxs-lookup"><span data-stu-id="3a8cb-316">Obtaining Content</span></span>

<span data-ttu-id="3a8cb-317">Führen Sie zuerst die folgenden Schritte aus, um den Inhalt zu erwerben, und führen Sie dann die Schritte aus, die die ersten Schritte ausführen, um den Kauf zu überprüfen</span><span class="sxs-lookup"><span data-stu-id="3a8cb-317">First perform the following steps to purchase content, and then perform the steps that follow the initial steps to verify the purchase and verify that the content downloaded:</span></span>

1.  <span data-ttu-id="3a8cb-318">Starten Sie Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-318">Launch Windows Media Player.</span></span>
2.  <span data-ttu-id="3a8cb-319">Melden Sie sich beim Testkonto an.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-319">Sign in to the test account.</span></span>
3.  <span data-ttu-id="3a8cb-320">Navigieren Sie zu dem zu Erwerb-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-320">Navigate to the content to purchase.</span></span>
4.  <span data-ttu-id="3a8cb-321">Befolgen Sie das Speicher spezifische Verfahren, um Inhalte zu erwerben.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-321">Follow the store-specific procedure to purchase content.</span></span>

<span data-ttu-id="3a8cb-322">**So überprüfen Sie den erworbenen und heruntergeladenen Inhalt**</span><span class="sxs-lookup"><span data-stu-id="3a8cb-322">**To verify purchased and downloaded content**</span></span>

1.  <span data-ttu-id="3a8cb-323">Vergewissern Sie sich, dass der berechnete Preis richtig ist.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-323">Verify that the calculated price is correct.</span></span>

    <span data-ttu-id="3a8cb-324">Überprüfen Sie, ob der Preis korrekt ist, insbesondere, wenn Sie mehrere Inhaltselemente gleichzeitig erwerben, und überprüfen Sie, ob die Informationen zum Konto Saldo nach dem Kauf ordnungsgemäß aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-324">Verify that the price is correct, especially when purchasing multiple pieces of content at once, and verify that any account balance information is updated correctly after purchase.</span></span> <span data-ttu-id="3a8cb-325">Einige Inhalte können als einzelne Spuren und nur als Alben erworben werden.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-325">Some content can be purchased as single tracks and some as albums only.</span></span> <span data-ttu-id="3a8cb-326">Vergewissern Sie sich, dass der albumpreis nicht größer als die Summe der einzelnen Spuren ist.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-326">Verify that the album price is not larger than the sum of the individual tracks.</span></span>

2.  <span data-ttu-id="3a8cb-327">Überprüfen Sie, ob die erworbenen Inhalte in die Bibliothek heruntergeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-327">Verify that the purchased content downloads to the library.</span></span>

    <span data-ttu-id="3a8cb-328">Wenn der Download abgeschlossen ist, navigieren Sie zu dem heruntergeladenen Inhalt in der Windows Media Player-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-328">When the download completes, navigate to the downloaded content in the Windows Media Player library.</span></span> <span data-ttu-id="3a8cb-329">Der heruntergeladene Inhalt befindet sich in der Bibliothek des aktuellen Benutzers.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-329">The downloaded content is located in the current user's library.</span></span>

    -   <span data-ttu-id="3a8cb-330">Für Windows XP und Windows Vista mit Windows Media Player 11 wird heruntergeladener Inhalt im Navigationsbereich Bibliothek unter **Bibliothek** Pivot und dann unter **Lieder** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-330">For Windows XP and Windows Vista with Windows Media Player 11, downloaded content appears in the library navigation pane, under **Library** pivot, and then under **Songs**.</span></span>
    -   <span data-ttu-id="3a8cb-331">Für Windows 7 mit Windows Media Player 12 wird der Inhalt, der in die Windows Media Player Bibliothek heruntergeladen wird, im Navigationsbereich Windows Media Player unter " **Musik**" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-331">For Windows 7 with Windows Media Player 12, content that is downloaded to the Windows Media Player library appears in the Windows Media Player navigation pane under **Music**.</span></span>

3.  <span data-ttu-id="3a8cb-332">Überprüfen Sie, ob für den Kauf Metadaten heruntergeladen wurden</span><span class="sxs-lookup"><span data-stu-id="3a8cb-332">Verify that metadata downloads for the purchase.</span></span>

    <span data-ttu-id="3a8cb-333">Stellen Sie sicher, dass die folgenden Spalten in der Windows Media Player-Bibliothek angezeigt werden (fügen Sie Sie andernfalls hinzu):</span><span class="sxs-lookup"><span data-stu-id="3a8cb-333">Ensure that the following columns appear in the Windows Media Player library (add them if not):</span></span>

    -   <span data-ttu-id="3a8cb-334">Album-Künstlerin</span><span class="sxs-lookup"><span data-stu-id="3a8cb-334">Album Artist</span></span>
    -   <span data-ttu-id="3a8cb-335">Titel</span><span class="sxs-lookup"><span data-stu-id="3a8cb-335">Title</span></span>
    -   <span data-ttu-id="3a8cb-336">Titel des Albums</span><span class="sxs-lookup"><span data-stu-id="3a8cb-336">Album Title</span></span>
    -   <span data-ttu-id="3a8cb-337">Inhaltsanbieter</span><span class="sxs-lookup"><span data-stu-id="3a8cb-337">Content Provider</span></span>
    -   <span data-ttu-id="3a8cb-338">Genre</span><span class="sxs-lookup"><span data-stu-id="3a8cb-338">Genre</span></span>

    <span data-ttu-id="3a8cb-339">Die vorangehenden Spalten müssen ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-339">The preceding columns must be populated.</span></span> <span data-ttu-id="3a8cb-340">Der Inhalt sollte über eine Albumgrafik verfügen.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-340">Content should have album art.</span></span> <span data-ttu-id="3a8cb-341">Es ist jedoch nicht erforderlich, dass Albumkunst Validierungstests bestanden hat.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-341">However, album art is not required to pass validation testing.</span></span>

4.  <span data-ttu-id="3a8cb-342">Überprüfen Sie, ob die Medien Nutzungsrechte für den Kauf korrekt sind.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-342">Verify that media usage rights are correct for the purchase.</span></span>

    <span data-ttu-id="3a8cb-343">Klicken Sie für jede heruntergeladene Spur mit der rechten Maustaste auf den Titel, und wählen Sie **Eigenschaften**, und wählen Sie dann die Registerkarte **Medien Verwendungs Rechte** aus.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-343">For each downloaded track, right-click the track and select **Properties**, and then select the **Media Usage Rights** tab.</span></span>

    <span data-ttu-id="3a8cb-344">Der Speicher kann seinen Inhalt mit Medien Nutzungsrechten schützen oder den Inhalt nicht schützen.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-344">The store can choose to protect its content with media usage rights, or can choose to not protect the content.</span></span> <span data-ttu-id="3a8cb-345">Auf der Registerkarte **Medien Verwendungs Rechte** wird der Status entweder durch Auflisten der Einschränkungen oder durch Angabe, dass der Inhalt nicht geschützt ist, angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-345">The **Media Usage Rights** tab reflects that status either by listing the restrictions, or by stating that the content is not protected.</span></span> <span data-ttu-id="3a8cb-346">Der Speicher muss seinen aktuellen Plan für die Medien Nutzungsrechte kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-346">The store must communicate its most current plan for media usage rights.</span></span> <span data-ttu-id="3a8cb-347">Sie müssen tatsächliche Ergebnisse anhand dieses erwarteten Verhaltens überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-347">You must verify actual results against this expected behavior.</span></span>

    <span data-ttu-id="3a8cb-348">Die Lizenzen für Medienrechte müssen vorab zugestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-348">Media rights licenses must be pre-delivered.</span></span> <span data-ttu-id="3a8cb-349">Der Kunde darf den Inhalt nicht wiedergeben oder einen anderen Prozess zum erhalten der Lizenz durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-349">The customer must not be required to play the content or go through some other process to get the license.</span></span> <span data-ttu-id="3a8cb-350">Sie müssen die jeweiligen Medien Nutzungsrechte mit den Anforderungen vergleichen, die der Speicher dem Kunden nach Bedarf mitgeteilt hat.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-350">You must compare the specific media usage rights to what the store has communicated to the customer as appropriate.</span></span> <span data-ttu-id="3a8cb-351">Rechte müssen auf mindestens zwei andere Computer übertragbar sein.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-351">Rights must be transferable to at least two other computers.</span></span> <span data-ttu-id="3a8cb-352">Kunden müssen in der Lage sein, Ihre Medien zu brennen und zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-352">Customers must be able to burn and synchronize their media.</span></span>

    <span data-ttu-id="3a8cb-353">Der folgende Screenshot zeigt die Medien Nutzungsrechte einer geschützten Datei:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-353">The following screen shot shows the media usage rights of a protected file:</span></span>

    ![Screenshot mit den Medien Verwendungs rechten für eine geschützte Datei](images/media-rights-protected.png)

    <span data-ttu-id="3a8cb-355">Wenn der Inhalt nicht geschützt ist, wird auf der Registerkarte " **Medien Nutzungsrechte** " Dieser Fakt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-355">If the content is not protected, the **Media Usage Rights** tab indicates this fact.</span></span>

    <span data-ttu-id="3a8cb-356">Der folgende Screenshot zeigt die Medien Nutzungsrechte einer ungeschützten Datei:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-356">The following screen shot shows the media usage rights of an unprotected file:</span></span>

    ![Screenshot mit den Medien Verwendungs rechten für eine ungeschützte Datei](images/media-rights-not-protected.png)

5.  <span data-ttu-id="3a8cb-358">Überprüfen Sie, ob die erworbenen Inhalte abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-358">Verify that the purchased content plays.</span></span>

    <span data-ttu-id="3a8cb-359">Überprüfen Sie, ob heruntergeladene Inhalte in Windows Media Player abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-359">Verify that downloaded content plays in Windows Media Player.</span></span>

    <span data-ttu-id="3a8cb-360">Wiedergeben jeglichen Inhalts, der aus dem Store gekauft wurde und der sich in der lokalen Bibliothek befindet, oder Streamen einer Vorschau.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-360">Play any content that was purchased from the store and that resides in the local library, or stream a preview.</span></span>

    <span data-ttu-id="3a8cb-361">Führen Sie die folgenden Schritte aus, um Inhalte in Windows XP und Windows Vista mit Windows Media Player 11 zu erwerben:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-361">Perform the following steps to purchase content in Windows XP and Windows Vista with Windows Media Player 11:</span></span>

    1.  <span data-ttu-id="3a8cb-362">Klicken Sie auf die Registerkarte **jetzt Wiedergabe** .</span><span class="sxs-lookup"><span data-stu-id="3a8cb-362">Click the **Now Playing** tab.</span></span>
    2.  <span data-ttu-id="3a8cb-363">Positionieren Sie den Mauszeiger im Listen Bereich mit dem Mauszeiger auf Album Art, um den Link zum **kaufen** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-363">In the list pane, position the mouse pointer to hover over album art in order to show the **Buy** link.</span></span>
    3.  <span data-ttu-id="3a8cb-364">Klicken Sie auf **kaufen**.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-364">Click **Buy**.</span></span>

    <span data-ttu-id="3a8cb-365">Der folgende Screenshot zeigt den Speicherort des **Kaufs** Links in Windows Media Player 11:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-365">The following screen shot shows the location of the **Buy** link in Windows Media Player 11:</span></span>

    ![Screenshot, der zeigt, wie Sie Inhalte in Windows Media Player 11 kaufen](images/wmp11-verify-buy-play.png)

    <span data-ttu-id="3a8cb-367">Führen Sie die folgenden Schritte aus, um Inhalte in Windows 7 mit Windows Media Player 12 zu erwerben:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-367">Perform the following steps to purchase content in Windows 7 with Windows Media Player 12:</span></span>

    1.  <span data-ttu-id="3a8cb-368">Klicken Sie im Bibliotheks Modus auf die Registerkarte wieder **Gabe** .</span><span class="sxs-lookup"><span data-stu-id="3a8cb-368">In library mode, click the **Play** tab.</span></span>
    2.  <span data-ttu-id="3a8cb-369">Klicken Sie in der Wiedergabeliste unter der Albumgrafik auf **Shop** .</span><span class="sxs-lookup"><span data-stu-id="3a8cb-369">In the playlist, under the album art, click **Shop**</span></span>

    <span data-ttu-id="3a8cb-370">Der folgende Screenshot zeigt, wie Sie Inhalte in Windows Media Player 12 kaufen:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-370">The following screen shot shows how to buy content in Windows Media Player 12:</span></span>

    ![Screenshot, der zeigt, wie Sie Inhalte in Windows Media Player 12 kaufen](images/wmp12-verify-buy-play.png)

6.  <span data-ttu-id="3a8cb-372">Vergewissern Sie sich, dass Sie auf **kaufen** **oder auf** den Store wechseln.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-372">Verify that clicking **Buy** or **Shop** switches to the store.</span></span>

    <span data-ttu-id="3a8cb-373">Der Windows-Media Player sollte zum Store in der Bibliotheks Ansicht wechseln und die Einkaufsmöglichkeiten des Stores laden.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-373">The Windows Media Player should switch to the store in library view and load the purchasing experience of the store.</span></span>

    <span data-ttu-id="3a8cb-374">Sie müssen dann den Titel weiter kaufen.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-374">You must then continue to purchase the track.</span></span>

7.  <span data-ttu-id="3a8cb-375">Vergewissern Sie sich, dass nach dem Klicken auf **kaufen** oder **Einkaufen** die Inhalte heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-375">Verify that after clicking **Buy** or **Shop**, the content downloads.</span></span>

    <span data-ttu-id="3a8cb-376">Überprüfen Sie, ob die Medien Nutzungsrechte für den erworbenen Inhalt und seine Metadaten geeignet sind, und überprüfen Sie, ob die Nachverfolgung abgespielt wird.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-376">Verify that the media usage rights are appropriate for the purchased content and its metadata, and verify that the track plays.</span></span> <span data-ttu-id="3a8cb-377">Im Allgemeinen sollte diese Kaufmethode dieselben Ergebnisse aufweisen wie andere Methoden.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-377">In general, this method of purchase should have the same results as other methods.</span></span>

### <a name="burning-content"></a><span data-ttu-id="3a8cb-378">Brennen von Inhalten</span><span class="sxs-lookup"><span data-stu-id="3a8cb-378">Burning Content</span></span>

<span data-ttu-id="3a8cb-379">Führen Sie zuerst die folgenden Schritte aus, um erworbene Inhalte zu brennen (Kopieren Sie erworbene Inhalte auf eine beschreibbare CD oder DVD), und führen Sie dann die Schritte aus, die den ersten Schritten folgen, um zu überprüfen, ob der Inhalt brennt:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-379">First perform the following steps to burn purchased content (copy purchased content to a writeable CD or DVD), and then perform the steps that follow the initial steps to verify that the content burns:</span></span>

> [!Note]  
> <span data-ttu-id="3a8cb-380">Beachten Sie vor dem Brennen eines erworbenen Titels seine Verbrauchs Anzahl, damit Sie später überprüfen können, ob die Anzahl nach dem Brennen des Titels Dekremente.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-380">Before you burn a purchased track, note its burn count so you can later verify whether the count decrements after you burn the track.</span></span>

 

1.  <span data-ttu-id="3a8cb-381">Klicken Sie auf die Registerkarte **Brennen**</span><span class="sxs-lookup"><span data-stu-id="3a8cb-381">Click the **Burn** tab</span></span>
2.  <span data-ttu-id="3a8cb-382">Ziehen Sie erworbene Spuren in die **Liste der Verbrennungen**.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-382">Drag purchased tracks to the **Burn List**.</span></span>
3.  <span data-ttu-id="3a8cb-383">Klicken Sie auf die Schaltfläche **Start brennen** .</span><span class="sxs-lookup"><span data-stu-id="3a8cb-383">Click the **Start Burn** button.</span></span>

<span data-ttu-id="3a8cb-384">Der folgende Screenshot zeigt die **Burn-Liste** auf der rechten Seite des Bildschirms und die Schaltfläche " **Brennen starten** " unterhalb der **Verbrennungs Liste** in Windows Media Player 11:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-384">The following screen shot shows the **Burn List** on the right side of the screen and the **Start Burn** button below the **Burn List** in Windows Media Player 11:</span></span>

![Screenshot, der zeigt, wie Sie Inhalte in Windows Media Player 11 brennen](images/wmp11-verify-burn.png)

<span data-ttu-id="3a8cb-386">Der folgende Screenshot zeigt, wie die Verbrauchs Liste in Windows Media Player 12 angezeigt wird, nachdem Sie eine Spur in die Liste mit den Ausbrennen gezogen haben und die Schaltfläche **Start brennen** am oberen Rand der Registerkarte **Brennen** anzeigt:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-386">The following screen shot shows how the burn list appears in Windows Media Player 12 after you drag a track to the burn list, and it shows the **Start Burn** button at the top of the **Burn** tab:</span></span>

![Screenshot, der zeigt, wie Sie Inhalte in Windows Media Player 12 brennen](images/wmp12-verify-burn.png)

<span data-ttu-id="3a8cb-388">**So überprüfen Sie, ob erworbene Inhalte gebrannt werden können**</span><span class="sxs-lookup"><span data-stu-id="3a8cb-388">**To verify that purchased content can be burned**</span></span>

1.  <span data-ttu-id="3a8cb-389">Überprüfen Sie, ob der erworbene Inhalt durch Abspielen der CD oder DVD nach Abschluss des Vorgangs gebrannt wird.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-389">Verify that the purchased content burns by playing the CD or DVD after burning completes.</span></span>

2.  <span data-ttu-id="3a8cb-390">Vergewissern Sie sich, dass die Anzahl der Verbrennungen verringert wird.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-390">Verify that the burn count is decremented.</span></span>

    <span data-ttu-id="3a8cb-391">Navigieren Sie zu der Bibliothek, und öffnen Sie die Medien Nutzungsrechte für einen erworbenen Titel, der gebrannt wurde.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-391">Navigate to the library and open the media usage rights for a purchased track that was burned.</span></span>

    <span data-ttu-id="3a8cb-392">Wenn die Anzahl der verbrannten Vorkommen eines Titels begrenzt ist, überprüfen Sie, ob diese Zahl nach dem Brennen des Titels abnimmt.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-392">If the number of times a track can be burned is limited, verify that this number decreases after the track is burned.</span></span>

### <a name="transferring-content"></a><span data-ttu-id="3a8cb-393">Inhalt wird übertragen</span><span class="sxs-lookup"><span data-stu-id="3a8cb-393">Transferring Content</span></span>

<span data-ttu-id="3a8cb-394">Übertragen von Inhalt auf einen anderen Computer.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-394">Transfer content to another computer.</span></span>

<span data-ttu-id="3a8cb-395">**So überprüfen Sie, ob erworbene Inhalte auf einen anderen Computer übertragen werden können**</span><span class="sxs-lookup"><span data-stu-id="3a8cb-395">**To verify that purchased content can be transferred to another computer**</span></span>

-   <span data-ttu-id="3a8cb-396">Wenn der Speicher die Übertragung von Inhalt an einen anderen Computer zulässt, übertragen Sie den Inhalt auf mindestens zwei Computer.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-396">If the store allows transferring content to another computer, transfer the content to at least two computers.</span></span>

<span data-ttu-id="3a8cb-397">Führen Sie zuerst die folgenden Schritte aus, um eine Synchronisierung mit einem Gerät durchzuführen und erworbene Inhalte an dieses Gerät zu übertragen. führen Sie dann die Schritte aus, die den ersten Schritten folgen, um zu überprüfen, ob der</span><span class="sxs-lookup"><span data-stu-id="3a8cb-397">First perform the following steps to sync to a device and transfer purchased content to that device, and then perform the steps that follow the initial steps to verify that the content is transferred:</span></span>

> [!Note]  
> <span data-ttu-id="3a8cb-398">Beachten Sie vor der Übertragung eines erworbenen Titels seine Synchronisierungs Anzahl, damit Sie später überprüfen können, ob die Anzahl nach der Übertragung des Titels Dekremente.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-398">Before you transfer a purchased track, note its sync count so you can later verify whether the count decrements after you transfer the track.</span></span>

 

1.  <span data-ttu-id="3a8cb-399">Verbinden Sie ein Gerät mit einer sicheren Uhr.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-399">Connect a device with a secure clock.</span></span> <span data-ttu-id="3a8cb-400">Beispiele hierfür sind Geräte, die Windows Media DRM für tragbare Geräte verwenden, z. b. ein portables Medien Center wie z. b. iRiver H10, Creative Zen usw.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-400">Examples include devices that use Windows Media DRM for Portable Devices, such as a Portable Media Center like the iRiver H10, the Creative Zen, and so on.</span></span>
2.  <span data-ttu-id="3a8cb-401">Klicken Sie unter Windows Media Player auf die Registerkarte **Synchronisieren** .</span><span class="sxs-lookup"><span data-stu-id="3a8cb-401">In Windows Media Player, click the **Sync** tab.</span></span>
3.  <span data-ttu-id="3a8cb-402">Ziehen Sie Inhalt aus der Bibliothek auf der Registerkarte **Synchronisieren** in den Bereich **Synchronisierungs Liste** .</span><span class="sxs-lookup"><span data-stu-id="3a8cb-402">Drag content from the library to the **Sync list** area on the **Sync** tab.</span></span>
4.  <span data-ttu-id="3a8cb-403">Klicken Sie auf die Schaltfläche **Synchronisierung starten** .</span><span class="sxs-lookup"><span data-stu-id="3a8cb-403">Click the **Start Sync** button.</span></span>

<span data-ttu-id="3a8cb-404">Der folgende Screenshot zeigt Track 1 im Bereich **Synchronisierungs Liste** und zeigt die Schaltfläche **Synchronisierung starten** in Windows Media Player 11 an:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-404">The following screen shot shows Track 1 in the **Sync list** area and shows the **Start Sync** button in Windows Media Player 11:</span></span>

![Screenshot, der zeigt, wie Inhalt in Windows Media Player 11 übertragen wird](images/wmp11-verify-transfer.png)

<span data-ttu-id="3a8cb-406">Der folgende Screenshot zeigt Track 1 im Bereich **Synchronisierungs Liste** und zeigt die Schaltfläche **Synchronisierung starten** in Windows Media Player 12 an:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-406">The following screen shot shows Track 1 in the **Sync list** area and shows the **Start Sync** button in Windows Media Player 12:</span></span>

![Screenshot, der zeigt, wie Inhalt in Windows Media Player 12 übertragen wird](images/wmp12-verify-transfer.png)

<span data-ttu-id="3a8cb-408">**So überprüfen Sie, ob erworbene Inhalte auf ein anderes Gerät übertragen werden können**</span><span class="sxs-lookup"><span data-stu-id="3a8cb-408">**To verify that purchased content can be transferred to another device**</span></span>

1.  <span data-ttu-id="3a8cb-409">Überprüfen Sie, ob der erworbene Inhalt auf das Gerät übertragen wird, indem Sie den Inhalt auf dem Gerät abspielen.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-409">Verify that the purchased content is transferred to the device by playing the content on the device.</span></span> <span data-ttu-id="3a8cb-410">Der übertragene Inhalt muss auch über die entsprechenden Metadaten verfügen.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-410">The transferred content must also have appropriate metadata.</span></span>

2.  <span data-ttu-id="3a8cb-411">Vergewissern Sie sich, dass die Synchronisierungs Anzahl dekrementiert wird.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-411">Verify that the sync count is decremented.</span></span>

    <span data-ttu-id="3a8cb-412">Navigieren Sie zu der Bibliothek, und öffnen Sie die Medien Nutzungsrechte für eine übertragene Spur.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-412">Navigate to the library and open the media usage rights for a transferred track.</span></span>

    <span data-ttu-id="3a8cb-413">Wenn die Anzahl der Synchronisierungs Versuche für eine Nachverfolgung begrenzt ist, überprüfen Sie, ob diese Zahl bei der Übertragung des Titels abnimmt.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-413">If the number of times a track can sync is limited, verify that this number decreases when the track is transferred.</span></span>

## <a name="store-features"></a><span data-ttu-id="3a8cb-414">Store-Features</span><span class="sxs-lookup"><span data-stu-id="3a8cb-414">Store Features</span></span>

<span data-ttu-id="3a8cb-415">In den folgenden Abschnitten wird beschrieben, wie Sie verschiedene Features eines integrierten Online Stores testen.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-415">The following sections describe how to test various features of an on-boarded online store.</span></span>

### <a name="managing-an-account"></a><span data-ttu-id="3a8cb-416">Verwalten eines Kontos</span><span class="sxs-lookup"><span data-stu-id="3a8cb-416">Managing an Account</span></span>

<span data-ttu-id="3a8cb-417">Melden Sie sich mit einem Konto an, das einige Einkäufe getätigt hat, und öffnen Sie den Kauf Verlauf.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-417">Sign in with an account that has made some purchases and open the purchase history.</span></span>

<span data-ttu-id="3a8cb-418">**So überprüfen Sie den Kauf Verlauf**</span><span class="sxs-lookup"><span data-stu-id="3a8cb-418">**To verify purchase history**</span></span>

-   <span data-ttu-id="3a8cb-419">Vergewissern Sie sich, dass der Kaufverlauf vorherige Käufe nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-419">Verify that the purchase history tracks prior purchases.</span></span>

<span data-ttu-id="3a8cb-420">Wenn der Speicher-oder Kontotyp dieses Feature unterstützt, versuchen Sie, einen gelöschten Kauf wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-420">If the store or account type supports this feature, attempt to restore a deleted purchase.</span></span>

<span data-ttu-id="3a8cb-421">**So überprüfen Sie, ob vorherige Käufe erneut erworben werden können**</span><span class="sxs-lookup"><span data-stu-id="3a8cb-421">**To verify that prior purchases can be reacquired**</span></span>

-   <span data-ttu-id="3a8cb-422">Überprüfen Sie, ob ein vorheriger Kauf wieder hergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-422">Verify that a prior purchase can be restored.</span></span>

<span data-ttu-id="3a8cb-423">Wenn der Speicher die Verwendung mehrerer Computer mit dem Konto unterstützt, überprüfen Sie alle Funktionen, die diese Funktion bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-423">If the store supports using multiple computers with the account, verify any functionality that this feature provides.</span></span>

<span data-ttu-id="3a8cb-424">**So überprüfen Sie die Verwaltung mehrerer Computer mit einem einzelnen Konto**</span><span class="sxs-lookup"><span data-stu-id="3a8cb-424">**To verify multiple computer management with a single account**</span></span>

-   <span data-ttu-id="3a8cb-425">Überprüfen Sie die Funktionalität des Stores, um mehrere Computer zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-425">Verify the store's functionality to manage multiple computers.</span></span>

### <a name="managing-a-store-specific-account"></a><span data-ttu-id="3a8cb-426">Verwalten eines Store-Specific Kontos</span><span class="sxs-lookup"><span data-stu-id="3a8cb-426">Managing a Store-Specific Account</span></span>

<span data-ttu-id="3a8cb-427">Der Speicher hat möglicherweise keine typischen Konto Typen, Einschränkungen oder Inhalte.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-427">The store might not have typical account types, restrictions, or content.</span></span> <span data-ttu-id="3a8cb-428">Ein Speicher, der Streaming-Videos mietet, benötigt z. b. eine Benutzeroberfläche, um aktive Vermietungen anzuzeigen, und die Benutzeroberfläche muss getestet werden.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-428">For example, a store that rents streaming video would need some user interface to display active rentals and that user interface would need to be tested.</span></span>

> [!Note]  
> <span data-ttu-id="3a8cb-429">Obwohl Microsoft keine Speicher spezifischen Kontofunktionen zertifizieren kann, sollten Sie diese Funktionalität testen, um eine gute Kundenfreundlichkeit zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-429">Although Microsoft cannot certify store-specific account functionality, to ensure a good customer experience, you should test that functionality.</span></span>

 

### <a name="managing-the-info-center"></a><span data-ttu-id="3a8cb-430">Verwalten des Info Centers</span><span class="sxs-lookup"><span data-stu-id="3a8cb-430">Managing the Info Center</span></span>

<span data-ttu-id="3a8cb-431">Führen Sie zuerst die folgenden Schritte aus, um das Testen des Standardstatus vorzubereiten, und führen Sie dann den nächsten Schritt aus, der den ersten Schritten folgt, um zu überprüfen, ob das Info Center standardmäßig deaktiviert ist:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-431">First perform the following steps to prepare for testing the default state, and then perform the next step that follows the initial steps to verify that the Info Center is off by default:</span></span>

1.  <span data-ttu-id="3a8cb-432">Wiedergabe von Inhalten aus dem Store.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-432">Play some content from the store.</span></span>
2.  <span data-ttu-id="3a8cb-433">Wechseln Sie zum jetzt Wiedergabe-Modus.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-433">Switch to Now Playing mode.</span></span> <span data-ttu-id="3a8cb-434">Klicken Sie unter Windows XP oder Windows Vista mit Windows Media Player 11 auf die Registerkarte **jetzt Wiedergabe** . Klicken Sie in Windows 7 mit Windows Media Player 12 in der unteren rechten Ecke auf die Schaltfläche **zum jetzt abspielen wechseln** .</span><span class="sxs-lookup"><span data-stu-id="3a8cb-434">In Windows XP or Windows Vista with Windows Media Player 11, click the **Now Playing** tab. In Windows 7 with Windows Media Player 12, click the **Switch to Now Playing** button at the lower right corner.</span></span>

<span data-ttu-id="3a8cb-435">**So überprüfen Sie, ob das Info Center standardmäßig deaktiviert ist**</span><span class="sxs-lookup"><span data-stu-id="3a8cb-435">**To verify that the Info Center is off by default**</span></span>

-   <span data-ttu-id="3a8cb-436">Vergewissern Sie sich, dass das Info Center standardmäßig deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-436">Verify that the Info Center is off by default.</span></span>

<span data-ttu-id="3a8cb-437">Wenn das Geschäft eine Info Center-Ansicht bietet, geben Sie Inhalte aus dem Store wieder, während der Inhalt wiedergegeben wird, wechseln Sie in den Modus jetzt wiedergeben, und schalten Sie Info Center ein.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-437">If the store offers an Info Center view, play some content from the store, and while the content is playing, switch to Now Playing mode and turn Info Center on.</span></span>

<span data-ttu-id="3a8cb-438">Unter Windows XP oder Windows Vista mit Windows Media Player 11 Klicken Sie mit der rechten Maustaste auf das Fenster jetzt Wiedergabe und wählen dann im Kontextmenü **Info Center-Ansicht** aus.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-438">In Windows XP or Windows Vista with Windows Media Player 11, right-click the now-playing window, and then from the context menu select **Info Center View**.</span></span>

<span data-ttu-id="3a8cb-439">Der folgende Screenshot zeigt das Kontextmenü in Windows Media Player 11:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-439">The following screen shot shows the context menu in Windows Media Player 11:</span></span>

![Screenshot, der zeigt, wie Sie auf das InfoCenter eines Stores in Windows Media Player 11 zugreifen](images/wmp11-info-center.png)

<span data-ttu-id="3a8cb-441">Klicken Sie unter Windows 7 mit Windows Media Player 12 mit der rechten Maustaste auf das Fenster jetzt Wiedergabe, wählen Sie im Kontextmenü die Option **Visualisierungen** aus, und klicken Sie dann auf **Info Center-Ansicht**.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-441">In Windows 7 with Windows Media Player 12, right-click the now-playing window, on the context menu select **Visualizations**, and then click **Info Center View**.</span></span>

<span data-ttu-id="3a8cb-442">Der folgende Screenshot zeigt das Kontextmenü in Windows Media Player 12:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-442">The following screen shot shows the context menu in Windows Media Player 12:</span></span>

![Screenshot, der zeigt, wie Sie auf das InfoCenter eines Stores in Windows Media Player 12 zugreifen](images/wmp12-info-center.png)

<span data-ttu-id="3a8cb-444">**So überprüfen Sie, ob das Info Center funktionsfähig ist**</span><span class="sxs-lookup"><span data-stu-id="3a8cb-444">**To verify that the Info Center is functional**</span></span>

-   <span data-ttu-id="3a8cb-445">Vergewissern Sie sich, dass im Bereich jetzt Wiedergabe im Info Center Medieninformationen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-445">Verify that the Info Center shows media information in the now-playing area.</span></span> <span data-ttu-id="3a8cb-446">Der folgende Screenshot zeigt ein Beispiel für Medieninformationen:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-446">The following screen shot shows an example of such media information:</span></span>

    ![Screenshot mit der Funktionalität eines Informations Centers für das Geschäft](images/media-information.png)

<span data-ttu-id="3a8cb-448">Wenn auf der Seite ein Kauf Verknüpfungen oder andere Links angezeigt werden, klicken Sie auf die Links.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-448">If any buy links or other links appear on the page, click the links.</span></span>

<span data-ttu-id="3a8cb-449">**So überprüfen Sie die Links in der Info Center-Ansicht**</span><span class="sxs-lookup"><span data-stu-id="3a8cb-449">**To verify links in the Info Center view**</span></span>

-   <span data-ttu-id="3a8cb-450">Überprüfen Sie, ob die Links den Speicher anzeigen.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-450">Verify that the links show the store.</span></span>

    <span data-ttu-id="3a8cb-451">Der Windows-Media Player sollte in seiner Bibliothek zum Speicher wechseln.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-451">The Windows Media Player should switch to the store in its library.</span></span>

## <a name="store-interaction"></a><span data-ttu-id="3a8cb-452">Speichern der Interaktion</span><span class="sxs-lookup"><span data-stu-id="3a8cb-452">Store Interaction</span></span>

<span data-ttu-id="3a8cb-453">In den folgenden Abschnitten wird beschrieben, wie Sie die Interaktion zwischen den anderen Stores und dem zu testenden Speicher testen.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-453">The following sections describe how to test interaction between the other stores and the store that you are testing.</span></span>

### <a name="yielding-to-the-active-store"></a><span data-ttu-id="3a8cb-454">Ergebnis des aktiven Stores</span><span class="sxs-lookup"><span data-stu-id="3a8cb-454">Yielding to the Active Store</span></span>

<span data-ttu-id="3a8cb-455">Wechseln Sie zu einem anderen Speicher als dem zu testenden Speicher.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-455">Switch to a store other than the store being tested.</span></span>

<span data-ttu-id="3a8cb-456">**So überprüfen Sie das Ergebnis im aktiven Speicher**</span><span class="sxs-lookup"><span data-stu-id="3a8cb-456">**To verify yielding to the active store**</span></span>

-   <span data-ttu-id="3a8cb-457">Vergewissern Sie sich, dass der getestete Speicher den aktiven Speicher liefert.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-457">Verify that the tested store yields to the active store.</span></span>

### <a name="preventing-the-tested-store-from-taking-over-the-active-store"></a><span data-ttu-id="3a8cb-458">Verhindern, dass der getestete Speicher den aktiven Speicher übernimmt</span><span class="sxs-lookup"><span data-stu-id="3a8cb-458">Preventing the Tested Store From Taking Over the Active Store</span></span>

-   <span data-ttu-id="3a8cb-459">Wenn ein anderer Speicher ausgewählt ist, schließen Sie Windows Media Player und starten Sie den Computer neu.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-459">With another store selected, close Windows Media Player and restart the computer.</span></span>
-   <span data-ttu-id="3a8cb-460">Starten Sie Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-460">Launch Windows Media Player.</span></span>

<span data-ttu-id="3a8cb-461">**So überprüfen Sie, ob der getestete Speicher**</span><span class="sxs-lookup"><span data-stu-id="3a8cb-461">**To verify that the tested store does not take over**</span></span>

-   <span data-ttu-id="3a8cb-462">Vergewissern Sie sich, dass der zuletzt aktive Speicher angezeigt wird und dass der getestete Speicher nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-462">Verify that the most recently active store appears and that the tested store does not appear.</span></span>

### <a name="accessing-a-store-in-high-contrast-mode"></a><span data-ttu-id="3a8cb-463">Zugreifen auf einen Speicher im High-Contrast Modus</span><span class="sxs-lookup"><span data-stu-id="3a8cb-463">Accessing a Store in High-Contrast Mode</span></span>

<span data-ttu-id="3a8cb-464">Aktivieren Sie zuerst den Modus für hohe Kontraste durch Drücken von Left Shift + Left Alt + Print, und führen Sie dann die folgenden Schritte aus, um die Barrierefreiheit mit hohem Kontrast zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-464">First enable high-contrast mode by pressing LEFT SHIFT+LEFT ALT+PRINT SCREEN, and then perform the following steps to verify high-contrast accessibility:</span></span>

<span data-ttu-id="3a8cb-465">**So überprüfen Sie, ob der Speicher im Modus mit hohem Kontrast verfügbar ist**</span><span class="sxs-lookup"><span data-stu-id="3a8cb-465">**To verify that the store is accessible in high-contrast mode**</span></span>

1.  <span data-ttu-id="3a8cb-466">Überprüfen Sie, ob die Anmelde Benutzeroberfläche intakt und funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-466">Verify that the log-in user interface is intact and functional.</span></span>
2.  <span data-ttu-id="3a8cb-467">Vergewissern Sie sich, dass alle Fenster und Dialogfelder ordnungsgemäß angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-467">Verify that all windows and dialog boxes appear correctly.</span></span>
3.  <span data-ttu-id="3a8cb-468">Medien erwerben.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-468">Purchase media.</span></span> <span data-ttu-id="3a8cb-469">Überprüfen Sie, ob die Schaltflächen "kaufen" und "herunterladen", "Downloads", "Preisinformationen" usw.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-469">Verify that purchase and download buttons, download managers, price information, and so on is visible.</span></span>
4.  <span data-ttu-id="3a8cb-470">Überprüfen Sie, ob Sie streamen, brennen und synchronisieren können.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-470">Verify that you can stream, burn, and synchronize.</span></span>
5.  <span data-ttu-id="3a8cb-471">Suchen Sie nach ausgeschnittenen Text-und Benutzeroberflächen Elementen, Text, der nicht lesbar ist, und anderen sichtbaren Fehlern.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-471">Look for clipped text and user-interface elements, text that is not legible, and other visible defects.</span></span>

### <a name="securing-a-store"></a><span data-ttu-id="3a8cb-472">Sichern eines Stores</span><span class="sxs-lookup"><span data-stu-id="3a8cb-472">Securing a Store</span></span>

<span data-ttu-id="3a8cb-473">Führen Sie folgende Schritte aus, um die Kontosicherheit zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="3a8cb-473">Perform the following steps to verify account security:</span></span>

<span data-ttu-id="3a8cb-474">**So überprüfen Sie die Kontosicherheit**</span><span class="sxs-lookup"><span data-stu-id="3a8cb-474">**To verify account security**</span></span>

1.  <span data-ttu-id="3a8cb-475">Geben Sie falsch formatierte Kontoinformationen in die Anmeldeseite und das Dialogfeld ein, und überprüfen Sie, ob Sie vom Speicher abgelehnt werden.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-475">Enter malformed account information into the log-in page and dialog box and verify that the store rejects it.</span></span>
2.  <span data-ttu-id="3a8cb-476">Melden Sie sich an, zeigen Sie die Kontoseite an, und melden Sie sich ab.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-476">Sign in, view the account page, and sign out.</span></span>
3.  <span data-ttu-id="3a8cb-477">Klicken Sie in Windows Media Player auf die Schaltfläche zurück, und vergewissern Sie sich, dass die vorherigen Benutzerkontoinformationen nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3a8cb-477">Click the back button in Windows Media Player, and verify that you do not see the previous user account information.</span></span>

 

 




