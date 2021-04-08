---
title: Zertifizierung Ihrer Desktop Anwendung
description: Führen Sie die folgenden Schritte aus, um Ihre Desktop-App für Windows 7, Windows 8, Windows 8.1 und Windows 10 zu zertifizieren. Wenn Sie Ihre Desktop-App so konvertieren möchten, dass Sie mit der universelle Windows-Plattform und dem Windows Store kompatibel ist, verwenden Sie die Windows-Desktop Bridge. in diesem Fall sollten Sie die Desktop Bridge Anleitung für die Zertifizierungs Schritte befolgen. Wenn Sie eine UWP-APP von Anfang an entwickeln und zertifizieren, finden Sie unter Leitfaden zur Zertifizierung von Windows-apps in UWP Weitere Informationen zur Zertifizierung.
ms.assetid: d77d9f1c-1738-4f44-a351-1985ffc21707
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52eb0f1040c438cb61f4729923c8928116447e8
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734560"
---
# <a name="certify-your-desktop-application"></a><span data-ttu-id="4b91d-103">Zertifizierung Ihrer Desktop Anwendung</span><span class="sxs-lookup"><span data-stu-id="4b91d-103">Certify your desktop application</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4b91d-104">Die Zertifizierung für Win32-Desktop-Apps ist [veraltet](https://techcommunity.microsoft.com/t5/windows-hardware-certification/win32-logo-certification-deprecation/ba-p/364920).</span><span class="sxs-lookup"><span data-stu-id="4b91d-104">Certification for Win32 desktop apps is [deprecated](https://techcommunity.microsoft.com/t5/windows-hardware-certification/win32-logo-certification-deprecation/ba-p/364920).</span></span> <span data-ttu-id="4b91d-105">Senden Sie stattdessen Dateien an dieser [Stelle](https://www.microsoft.com/wdsi/filesubmission/).</span><span class="sxs-lookup"><span data-stu-id="4b91d-105">Instead, [submit files here](https://www.microsoft.com/wdsi/filesubmission/).</span></span>

<span data-ttu-id="4b91d-106">Führen Sie die folgenden Schritte aus, um Ihre Desktop-App für Windows 7, Windows 8, Windows 8.1 und Windows 10 zertifizieren zu lassen.</span><span class="sxs-lookup"><span data-stu-id="4b91d-106">Follow these steps to get your desktop app certified for Windows 7, Windows 8, Windows 8.1, and Windows 10.</span></span>

<span data-ttu-id="4b91d-107">Wenn Sie Ihre Desktop-App so konvertieren möchten, dass Sie mit dem universelle Windows-Plattform und Windows Store kompatibel ist, verwenden Sie die [Windows-Desktop Bridge](https://developer.microsoft.com/windows/bridges/desktop). in diesem Fall sollten Sie die Anleitungen für die [Desktop Bridge](/windows/uwp/porting/desktop-to-uwp-root) für die Zertifizierungs Schritte befolgen.</span><span class="sxs-lookup"><span data-stu-id="4b91d-107">If you wish to convert your desktop app to be compatible with the Universal Windows Platform and Windows Store, you will use the [Windows Desktop Bridge](https://developer.microsoft.com/windows/bridges/desktop), in which case you should follow the [Desktop Bridge](/windows/uwp/porting/desktop-to-uwp-root) guidance for certification steps.</span></span>

<span data-ttu-id="4b91d-108">Wenn Sie eine UWP-APP von Anfang an entwickeln und zertifizieren, finden Sie unter [Leitfaden zur Zertifizierung von Windows-apps in UWP](/windows/uwp/debug-test-perf/windows-app-certification-kit) Weitere Informationen zur Zertifizierung.</span><span class="sxs-lookup"><span data-stu-id="4b91d-108">If you are developing and certifying a UWP app from the start, see [Guidance for Windows App Certification in UWP](/windows/uwp/debug-test-perf/windows-app-certification-kit) for info on certification.</span></span>

## <a name="step-1-prepare-for-certification"></a><span data-ttu-id="4b91d-109">Schritt 1: Vorbereiten der Zertifizierung</span><span class="sxs-lookup"><span data-stu-id="4b91d-109">Step 1: Prepare for certification</span></span>



| <span data-ttu-id="4b91d-110">Thema</span><span class="sxs-lookup"><span data-stu-id="4b91d-110">Topic</span></span>                                                                                       | <span data-ttu-id="4b91d-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b91d-111">Description</span></span>                                                                                    |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b91d-112">Was sind die Vorteile?</span><span class="sxs-lookup"><span data-stu-id="4b91d-112">What are the benefits?</span></span>](what-are-the-benefits-.md)<br/>                             | <span data-ttu-id="4b91d-113">Die Zertifizierung Ihrer Desktop-App bietet Ihnen und ihren Kunden eine Reihe von Vorteilen.</span><span class="sxs-lookup"><span data-stu-id="4b91d-113">Certifying your desktop app provides several benefits for you and your customers.</span></span>              |
| [<span data-ttu-id="4b91d-114">Lesen der Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b91d-114">Read the requirements</span></span>](certification-requirements-for-windows-desktop-apps.md)<br/> | <span data-ttu-id="4b91d-115">Überprüfen Sie die technischen Anforderungen und Berechtigungs Qualifizierungen, die eine Desktop-App erfüllen muss.</span><span class="sxs-lookup"><span data-stu-id="4b91d-115">Review the technical requirements and eligibility qualifications that a desktop app must meet.</span></span> |



 

## <a name="step-2-test-your-app-with-the-windows-app-certification-kit"></a><span data-ttu-id="4b91d-116">Schritt 2: Testen der APP mit dem zertifizierungskit für Windows-apps</span><span class="sxs-lookup"><span data-stu-id="4b91d-116">Step 2: Test your app with the Windows App Certification Kit</span></span>



| <span data-ttu-id="4b91d-117">Thema</span><span class="sxs-lookup"><span data-stu-id="4b91d-117">Topic</span></span>                                                          | <span data-ttu-id="4b91d-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b91d-118">Description</span></span>                                                                                                                                                                           |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b91d-119">Holen Sie sich das Kit</span><span class="sxs-lookup"><span data-stu-id="4b91d-119">Get the Kit</span></span>](https://developer.microsoft.com/windows/downloads/app-certification-kit/) | <span data-ttu-id="4b91d-120">Um die APP zu zertifizieren, müssen Sie das zertifizierungskit für Windows-apps installieren und ausführen (enthalten im Windows SDK).</span><span class="sxs-lookup"><span data-stu-id="4b91d-120">To certify your app, you have to install and run the Windows App Certification Kit (included in the Windows SDK).</span></span>                                                                     |
| [<span data-ttu-id="4b91d-121">Verwenden des Kits</span><span class="sxs-lookup"><span data-stu-id="4b91d-121">Using the Kit</span></span>](using-the-windows-app-certification-kit.md)   | <span data-ttu-id="4b91d-122">Bevor Sie Ihre APP übermitteln können, müssen Sie Sie auf Bereitschaft testen.</span><span class="sxs-lookup"><span data-stu-id="4b91d-122">Before you can submit your app, you must test it for readiness.</span></span> <span data-ttu-id="4b91d-123">Sie können auch eine Kopie des [Whitepaper zur Zertifizierung der APP](https://www.microsoft.com/download/details.aspx?id=27414)herunterladen.</span><span class="sxs-lookup"><span data-stu-id="4b91d-123">You can also download a copy of the [app certification white paper](https://www.microsoft.com/download/details.aspx?id=27414).</span></span> |
| [<span data-ttu-id="4b91d-124">Testdetails prüfen</span><span class="sxs-lookup"><span data-stu-id="4b91d-124">Review test details</span></span>](windows-app-certification-kit-tests.md) | <span data-ttu-id="4b91d-125">Holen Sie sich die Liste der Tests, die Ihre APP durchlaufen muss, um die Kompatibilität mit dem neuesten Windows-Betriebssystem zu qualifizieren.</span><span class="sxs-lookup"><span data-stu-id="4b91d-125">Get the list of the tests your app needs to pass to qualify for compatibility with the latest Windows operating system.</span></span>                                                               |



 

<span data-ttu-id="4b91d-126">Hinweis: Filter Treiber müssen auch das [hardwarezertifizierungskit](https://download.microsoft.com/download/1/8/B/18BC088A-537D-4386-9334-687747A602E6/hlk/hlksetup.exe)bestehen.</span><span class="sxs-lookup"><span data-stu-id="4b91d-126">Note: Filter drivers must also pass the [Hardware Certification Kit](https://download.microsoft.com/download/1/8/B/18BC088A-537D-4386-9334-687747A602E6/hlk/hlksetup.exe).</span></span> <span data-ttu-id="4b91d-127">(Siehe [Zertifizierungsanforderungen für Windows-Desktop-Apps, Abschnitt 6,2](certification-requirements-for-windows-desktop-apps.md).)</span><span class="sxs-lookup"><span data-stu-id="4b91d-127">(See [Certification requirements for Windows desktop apps, section 6.2](certification-requirements-for-windows-desktop-apps.md).)</span></span>

## <a name="step-3-use-the-windows-certification-dashboard"></a><span data-ttu-id="4b91d-128">Schritt 3: Verwenden des Windows-Zertifizierungs Dashboards</span><span class="sxs-lookup"><span data-stu-id="4b91d-128">Step 3: Use the Windows Certification Dashboard</span></span>

<span data-ttu-id="4b91d-129">Um Ihre APP zur Zertifizierung zu übermitteln, müssen Sie sich auf dem [Windows-zertifizierungdashboard](/previous-versions/hh833792(v=msdn.10))anmelden oder ein Unternehmens Konto registrieren.</span><span class="sxs-lookup"><span data-stu-id="4b91d-129">To submit your app for certification, you'll need to log in or register a company account on the [Windows Certification Dashboard](/previous-versions/hh833792(v=msdn.10)).</span></span> <span data-ttu-id="4b91d-130">Wenn Sie dies tun, können Sie nicht nur Ihre APP zertifizieren, sondern erhalten auch Zugriff auf Tools, mit denen Sie Ihre APP in allen Phasen des Prozesses überprüfen und verwalten können.</span><span class="sxs-lookup"><span data-stu-id="4b91d-130">Once you do, not only will you be able to get your app certified, but you'll also gain access to tools to review and manage your app at all stages of the process.</span></span>



| <span data-ttu-id="4b91d-131">Thema</span><span class="sxs-lookup"><span data-stu-id="4b91d-131">Topic</span></span>                                                                                                                   | <span data-ttu-id="4b91d-132">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b91d-132">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b91d-133">Einrichten Ihres Kontos</span><span class="sxs-lookup"><span data-stu-id="4b91d-133">Set up your account</span></span>](/windows-hardware/drivers/dashboard/)                 | <span data-ttu-id="4b91d-134">Wenn Ihr Unternehmen nicht bereits registriert ist, müssen Sie es über das Windows-zertifizierungsdashboard registrieren.</span><span class="sxs-lookup"><span data-stu-id="4b91d-134">If your company isn't already registered, you must register it through the Windows Certification Dashboard.</span></span>                                        |
| [<span data-ttu-id="4b91d-135">Abrufen eines Codesignaturzertifikats</span><span class="sxs-lookup"><span data-stu-id="4b91d-135">Get a code signing certificate</span></span>](/windows-hardware/drivers/dashboard/)      | <span data-ttu-id="4b91d-136">Bevor Sie ein Windows-zertifizierungdashboard einrichten können, müssen Sie ein Code Signaturzertifikat erhalten, um Ihre digitalen Informationen zu sichern.</span><span class="sxs-lookup"><span data-stu-id="4b91d-136">Before you can establish a Windows Certification Dashboard account, you need to get a code signing certificate to secure your digital information.</span></span> |
| [<span data-ttu-id="4b91d-137">Lokales Testen und Hochladen der Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="4b91d-137">Test locally and upload the results</span></span>](/windows-hardware/drivers/dashboard/) | <span data-ttu-id="4b91d-138">Laden Sie die Ergebnisse nach dem Ausführen der Tests für Windows-zertifizierungskit auf das Windows-zertifizierungskit hoch</span><span class="sxs-lookup"><span data-stu-id="4b91d-138">After your run the Windows App Certification Kit tests, upload the results to the Windows Certification Dashboard.</span></span>                                 |
| [<span data-ttu-id="4b91d-139">Verwalten Ihrer Übermittlung</span><span class="sxs-lookup"><span data-stu-id="4b91d-139">Manage your submission</span></span>](/windows-hardware/drivers/dashboard/)              | <span data-ttu-id="4b91d-140">Nachdem Sie Ihre APP zur Zertifizierung eingereicht haben, können Sie Ihre Übermittlung über das Windows-zertifizierungsdashboard überprüfen.</span><span class="sxs-lookup"><span data-stu-id="4b91d-140">After you submit your app for certification, you can review your submission through the Windows Certification Dashboard.</span></span>                           |



 

## <a name="step-4-promote-your-desktop-app"></a><span data-ttu-id="4b91d-141">Schritt 4: herauf Stufen ihrer Desktop-App</span><span class="sxs-lookup"><span data-stu-id="4b91d-141">Step 4: Promote your desktop app</span></span>



| <span data-ttu-id="4b91d-142">Thema</span><span class="sxs-lookup"><span data-stu-id="4b91d-142">Topic</span></span>                                                                      | <span data-ttu-id="4b91d-143">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b91d-143">Description</span></span>                                                                                                               |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b91d-144">APP-Kompatibilität überprüfen</span><span class="sxs-lookup"><span data-stu-id="4b91d-144">Check app compatibility</span></span>](/windows/compatibility/windows-8-1-introduction) | <span data-ttu-id="4b91d-145">Wenn Sie eine APP für Windows 8.1 entwickeln, untersuchen Sie Kompatibilitätsprobleme.</span><span class="sxs-lookup"><span data-stu-id="4b91d-145">If you are building an app for Windows 8.1, investigate compatibility concerns.</span></span>                                           |
| [<span data-ttu-id="4b91d-146">Verwenden Sie das Logo mit Ihrer APP.</span><span class="sxs-lookup"><span data-stu-id="4b91d-146">Use the logo with your app</span></span>](https://techcommunity.microsoft.com/t5/windows-hardware-certification/bg-p/WindowsHardwareCertification)                  | <span data-ttu-id="4b91d-147">Zeigen Sie das Logo auf Verpacken und Werbematerialien entsprechend den Richtlinien an.</span><span class="sxs-lookup"><span data-stu-id="4b91d-147">Display the logo on packaging and in ads and other promotional materials according to the guidelines.</span></span> <span data-ttu-id="4b91d-148">Nur für Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4b91d-148">For Windows 7 only.</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="4b91d-149">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="4b91d-149">See also:</span></span>

<span data-ttu-id="4b91d-150">[App-Kompatibilitäts Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowscompatibility): finden Sie Unterstützung von der Community zur Kompatibilität und Logo Zertifizierung.</span><span class="sxs-lookup"><span data-stu-id="4b91d-150">[App compatibility forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowscompatibility): Find support from the community about compatibility and logo certification.</span></span>

<span data-ttu-id="4b91d-151">[Windows SDK Blog](https://blogs.msdn.com/b/winsdk/archive/tags/certification/): Hier finden Sie Tipps und Neuigkeiten im Zusammenhang mit der APP-Zertifizierung.</span><span class="sxs-lookup"><span data-stu-id="4b91d-151">[Windows SDK blog](https://blogs.msdn.com/b/winsdk/archive/tags/certification/): Find tips and news related to app certification.</span></span>

<span data-ttu-id="4b91d-152">[Windows Server-Forum]( https://social.technet.microsoft.com/Forums/windowsserver/home?forum=WSAppCompat): Besuchen Sie das Zertifizierungs Forum, um Antworten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4b91d-152">[Windows Server forum]( https://social.technet.microsoft.com/Forums/windowsserver/home?forum=WSAppCompat): Visit the Certification forum to get answers.</span></span>

<span data-ttu-id="4b91d-153">[Compatibility Cookbook](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal): Hier erhalten Sie Informationen zu Neuerungen oder Änderungen in der neuesten Version von Windows.</span><span class="sxs-lookup"><span data-stu-id="4b91d-153">[Compatibility cookbook](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal): Get info about what's new or changed in the latest version of Windows.</span></span>

 

