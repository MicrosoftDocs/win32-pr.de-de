---
title: Verwenden des Media Foundation-Ereignis Modells
description: Verwenden des Media Foundation-Ereignis Modells
ms.assetid: c07425dc-25d0-430b-a1f6-6373303a0cc7
keywords:
- Windows Media-Format-SDK, DRM Media Foundation-Ereignis Modell
- Windows Media-Format-SDK, Media Foundation-Ereignis Modell
- Windows Media-Format-SDK, DRM-Ereignis Modell
- Digital Rights Management (DRM), Media Foundation-Ereignis Modell
- DRM (Digital Rights Management), Media Foundation-Ereignis Modell
- Digital Rights Management (DRM), Ereignis Modell
- DRM (Digital Rights Management), Ereignis Modell
- Digital Rights Management (DRM), iwmdrmeventgenerator-Schnittstelle
- DRM (Digital Rights Management), iwmdrmeventgenerator-Schnittstelle
- Media Foundation
- Iwmdrmeventgenerator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58d48157072cf8814ff8ac74d97a965f9e772e3
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104038626"
---
# <a name="using-the-media-foundation-event-model"></a><span data-ttu-id="4ab84-114">Verwenden des Media Foundation-Ereignis Modells</span><span class="sxs-lookup"><span data-stu-id="4ab84-114">Using the Media Foundation Event Model</span></span>

<span data-ttu-id="4ab84-115">Die asynchronen Methoden, die von den erweiterten APIs des Windows Media DRM-Clients unterstützt werden, verwenden dasselbe Ereignis Modell, das vom Media Foundation SDK verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4ab84-115">The asynchronous methods supported by the Windows Media DRM Client Extended APIs use the same event model that is used by the Media Foundation SDK.</span></span> <span data-ttu-id="4ab84-116">Jedes Objekt, das asynchrone Methoden unterstützt, implementiert die [**iwmdrmeventgenerator**](iwmdrmeventgenerator.md) -Schnittstelle, die verwendet werden kann, um ein Ereignis abzurufen, wenn ein asynchroner Vorgang beendet ist.</span><span class="sxs-lookup"><span data-stu-id="4ab84-116">Each object that supports asynchronous methods implements the [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md) interface, which can be used to retrieve an event when an asynchronous operation is complete.</span></span>

<span data-ttu-id="4ab84-117">Die **iwmdrmeventgenerator** -Schnittstelle erbt von der **IMF mediaeventgenerator** -Schnittstelle, die in der Media Foundation SDK-Dokumentation dokumentiert ist.</span><span class="sxs-lookup"><span data-stu-id="4ab84-117">The **IWMDRMEventGenerator** interface inherits from the **IMFMediaEventGenerator** interface, which is documented in the Media Foundation SDK documentation.</span></span>

<span data-ttu-id="4ab84-118">Der Beispielcode im Beispiel für eine [DRM-Individualisierung](drm-individualization-example.md) verwendet die **imfmediaeventgenerator:: GetEvent** -Methode, um Ereignisse einzeln aus der Warteschlange abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4ab84-118">The example code in the [DRM Individualization Example](drm-individualization-example.md) uses the **IMFMediaEventGenerator::GetEvent** method to retrieve events from the queue one at a time.</span></span> <span data-ttu-id="4ab84-119">Die Verwendung von **GetEvent** ist einfacher als die Verwendung von **imfmediaeventgenerator:: begingetevent** und **imfmediaeventgenerator:: endgetevent** mit einem Rückruf, wodurch die Codebeispiele leichter verständlich werden.</span><span class="sxs-lookup"><span data-stu-id="4ab84-119">Using **GetEvent** is more straightforward than using **IMFMediaEventGenerator::BeginGetEvent** and **IMFMediaEventGenerator::EndGetEvent** with a callback, which makes the code examples easier to understand.</span></span> <span data-ttu-id="4ab84-120">Unabhängig davon, ob Sie **GetEvent** in Ihrem Code verwenden oder **imfasynccallback** implementieren und **begingetevent** und **endgetevent** verwenden, ist die Logik zum Verarbeiten des Ereignisses nach dem Empfang identisch.</span><span class="sxs-lookup"><span data-stu-id="4ab84-120">Whether you use **GetEvent** in your code or implement **IMFAsyncCallback** and use **BeginGetEvent** and **EndGetEvent**, the logic to handle the event after it has been received is the same.</span></span>

<span data-ttu-id="4ab84-121">Einige der asynchronen Methoden generieren Ereignisse, die Verweise auf Objekte enthalten, die zum Abrufen ausführlicherer Statusinformationen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="4ab84-121">Several of the asynchronous methods generate events that contain references to objects that can be used to obtain more detailed status information.</span></span> <span data-ttu-id="4ab84-122">In diesen Fällen weist das generierte Ereignis einen **IUnknown** -Zeiger als Wert auf, der abgefragt werden kann, um die Status Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4ab84-122">In these cases, the generated event has an **IUnknown** pointer as its value, which can be queried to retrieve the status interface.</span></span> <span data-ttu-id="4ab84-123">In der folgenden Liste werden die Beziehungen zwischen asynchronen Aufrufen, generierten Ereignissen und anderen Schnittstellen zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="4ab84-123">The following list summarizes the relationships between asynchronous calls, generated events, and other interfaces.</span></span>

-   <span data-ttu-id="4ab84-124">Die [**iwmdrmlicensmanagement:: backuplicenses**](iwmdrmlicensemanagement-backuplicenses.md) -Methode generiert **mewmdrmlicenabbackupprogress** -Ereignisse mit zugeordneten [**iwmdrmlicenabbackuprestorestatus**](iwmdrmlicensebackuprestorestatus.md) -Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="4ab84-124">The [**IWMDRMLicenseManagement::BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md) method generates **MEWMDRMLicenseBackupProgress** events with associated [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) interfaces.</span></span>
-   <span data-ttu-id="4ab84-125">Die [**iwmdrmlicensemanagement:: restorelicenses**](iwmdrmlicensemanagement-restorelicenses.md) -Methode generiert **mewmdrmlicenserestoreprogress** -Ereignisse mit zugeordneten [**iwmdrmlicensebackuprestorestatus**](iwmdrmlicensebackuprestorestatus.md) -Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="4ab84-125">The [**IWMDRMLicenseManagement::RestoreLicenses**](iwmdrmlicensemanagement-restorelicenses.md) method generates **MEWMDRMLicenseRestoreProgress** events with associated [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) interfaces.</span></span>
-   <span data-ttu-id="4ab84-126">Die [**iwmdrmsecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) -Methode, wenn Sie zur Durchführung von Individualisierungen verwendet wird, generiert **mewmdrmindividualizationprogress** -Ereignisse mit zugeordneten [**iwmdrmindividualizationstatus**](iwmdrmindividualizationstatus.md) -Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="4ab84-126">The [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) method, when used to perform individualization, generates **MEWMDRMIndividualizationProgress** events with associated [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) interfaces.</span></span>
-   <span data-ttu-id="4ab84-127">Wenn die [**iwmdrmlicensemanagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) -Methode zum Vorbereiten von Daten für den nicht automatischen Lizenz Abruf verwendet wird, wird ein **mewmdrmlicenseacquisitionabgeschlossene** -Ereignis mit einer zugeordneten [**iwmdrmnonsilentlicenseaquisition**](iwmdrmnonsilentlicenseaquisition.md) -Schnittstelle generiert.</span><span class="sxs-lookup"><span data-stu-id="4ab84-127">The [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) method, when used to prepare data for non-silent license acquisition, generates an **MEWMDRMLicenseAcquisitionCompleted** event with an associated [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ab84-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4ab84-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ab84-129">**Beispiel für DRM-Individualisierung**</span><span class="sxs-lookup"><span data-stu-id="4ab84-129">**DRM Individualization Example**</span></span>](drm-individualization-example.md)
</dt> <dt>

[<span data-ttu-id="4ab84-130">**Einstieg**</span><span class="sxs-lookup"><span data-stu-id="4ab84-130">**Getting Started**</span></span>](drm-getting-started.md)
</dt> <dt>

[<span data-ttu-id="4ab84-131">Media Foundation SDK-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="4ab84-131">Media Foundation SDK Documentation</span></span>](https://www.microsoft.com/?ref=go)
</dt> </dl>

 

 




