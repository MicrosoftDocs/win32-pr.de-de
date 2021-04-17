---
title: Direct3D 9Ex-Verbesserungen
description: In diesem Thema wird die Unterstützung zusätzlicher Windows 7-Unterstützung für den Flip-Modus und die zugehörigen aktuellen Statistiken in Direct3D 9Ex und Desktopfenster-Manager beschrieben.
ms.assetid: cb92a162-57eb-4aee-af7a-c8ece37075a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42eef10b6caaa959cb750f073c97a0f665384463
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390774"
---
# <a name="direct3d-9ex-improvements"></a><span data-ttu-id="3a092-103">Direct3D 9Ex-Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="3a092-103">Direct3D 9Ex improvements</span></span>

<span data-ttu-id="3a092-104">In diesem Thema wird die Unterstützung zusätzlicher Windows 7-Unterstützung für den Flip-Modus und die zugehörigen aktuellen Statistiken in Direct3D 9Ex und Desktopfenster-Manager beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3a092-104">This topic describes Windows 7's added support for Flip Mode Present and its associated present statistics in Direct3D 9Ex and Desktop Window Manager.</span></span> <span data-ttu-id="3a092-105">Zielanwendungen sind Video-oder Frameraten basierte Präsentations Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="3a092-105">Target applications include video or frame rate-based presentation applications.</span></span> <span data-ttu-id="3a092-106">Anwendungen, die den Direct3D 9Ex-Flip-Modus verwenden, verringern die Systemressourcen Auslastung, wenn DWM aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3a092-106">Applications that use Direct3D 9Ex Flip Mode Present reduce the system resource load when DWM is enabled.</span></span> <span data-ttu-id="3a092-107">Aktuelle Statistik Erweiterungen im Zusammenhang mit dem Flip-Modus ermöglichen es Direct3D 9Ex-Anwendungen, die Präsentations Rate besser zu steuern, indem Sie Echtzeitfeedback und Korrekturmechanismen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="3a092-107">Present statistics enhancements associated with Flip Mode Present enable Direct3D 9Ex applications to better control the rate of presentation by providing real-time feedback and correction mechanisms.</span></span> <span data-ttu-id="3a092-108">Ausführliche Erläuterungen und Zeiger auf Beispiel Ressourcen sind enthalten.</span><span class="sxs-lookup"><span data-stu-id="3a092-108">Detailed explanations and pointers to sample resources are included.</span></span>

<span data-ttu-id="3a092-109">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="3a092-109">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3a092-110">Verbesserte Informationen zu Direct3D 9Ex für Windows 7</span><span class="sxs-lookup"><span data-stu-id="3a092-110">What's Improved about Direct3D 9Ex for Windows 7</span></span>](#whats-improved-about-direct3d-9ex-for-windows-7)
-   [<span data-ttu-id="3a092-111">Direct3D 9Ex-Flip-Modus-Präsentation</span><span class="sxs-lookup"><span data-stu-id="3a092-111">Direct3D 9EX Flip Mode Presentation</span></span>](#direct3d-9ex-flip-mode-presentation)
-   [<span data-ttu-id="3a092-112">Programmiermodell und APIs</span><span class="sxs-lookup"><span data-stu-id="3a092-112">Programming Model and APIs</span></span>](#programming-model-and-apis)
    -   [<span data-ttu-id="3a092-113">So abonnieren Sie das Direct3D 9Ex-Flip-Modell</span><span class="sxs-lookup"><span data-stu-id="3a092-113">How to Opt Into the Direct3D 9Ex Flip Model</span></span>](#how-to-opt-into-the-direct3d-9ex-flip-model)
    -   [<span data-ttu-id="3a092-114">Entwurfs Richtlinien für Direct3D 9Ex-Flip Model-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="3a092-114">Design Guidelines for Direct3D 9Ex Flip Model Applications</span></span>](#design-guidelines-for-direct3d-9ex-flip-model-applications)
    -   [<span data-ttu-id="3a092-115">Frame Synchronisierung von Direct3D 9Ex-kippen-Modell Anwendungen</span><span class="sxs-lookup"><span data-stu-id="3a092-115">Frame Synchronization of Direct3D 9Ex Flip Model Applications</span></span>](#frame-synchronization-of-direct3d-9ex-flip-model-applications)
    -   [<span data-ttu-id="3a092-116">Rahmen Synchronisierung für Fenster Anwendungen, wenn DWM deaktiviert ist</span><span class="sxs-lookup"><span data-stu-id="3a092-116">Frame Synchronization for Windowed Applications When DWM is Off</span></span>](#frame-synchronization-for-windowed-applications-when-dwm-is-off)
-   [<span data-ttu-id="3a092-117">Exemplarische Vorgehensweise: Beispiel für ein Direct3D 9Ex-Flip-Modell und eine aktuelle Statistik</span><span class="sxs-lookup"><span data-stu-id="3a092-117">Walk-Through of a Direct3D 9Ex Flip Model and Present Statistics Sample</span></span>](#walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample)
    -   [<span data-ttu-id="3a092-118">Zusammenfassung der Programmier Empfehlungen für die Frame-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="3a092-118">Summary of Programming Recommendations for Frame Synchronization</span></span>](#summary-of-programming-recommendations-for-frame-synchronization)
-   [<span data-ttu-id="3a092-119">Schlussfolgerung zu Direct3D 9Ex-Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="3a092-119">Conclusion about Direct3D 9Ex Improvements</span></span>](#conclusion-about-direct3d-9ex-improvements)
-   [<span data-ttu-id="3a092-120">Aktions Aufrufe</span><span class="sxs-lookup"><span data-stu-id="3a092-120">Call to Action</span></span>](#call-to-action)
-   [<span data-ttu-id="3a092-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3a092-121">Related topics</span></span>](#related-topics)

## <a name="whats-improved-about-direct3d-9ex-for-windows-7"></a><span data-ttu-id="3a092-122">Verbesserte Informationen zu Direct3D 9Ex für Windows 7</span><span class="sxs-lookup"><span data-stu-id="3a092-122">What's Improved about Direct3D 9Ex for Windows 7</span></span>

<span data-ttu-id="3a092-123">Die Darstellung des Flip-Modus von Direct3D 9Ex ist ein verbesserter Modus für das darstellen von Bildern in Direct3D 9Ex, die gerenderte Bilder effizient an Windows 7 Desktopfenster-Manager (DWM) für die Komposition übergibt.</span><span class="sxs-lookup"><span data-stu-id="3a092-123">Flip Mode Presentation of Direct3D 9Ex is an improved mode of presenting images in Direct3D 9Ex that efficiently hands off rendered images to Windows 7 Desktop Window Manager (DWM) for composition.</span></span> <span data-ttu-id="3a092-124">Ab Windows Vista stellt DWM den gesamten Desktop dar.</span><span class="sxs-lookup"><span data-stu-id="3a092-124">Beginning in Windows Vista, DWM composes the entire Desktop.</span></span> <span data-ttu-id="3a092-125">Wenn DWM aktiviert ist, stellen Fenster-modusanwendungen ihren Inhalt auf dem Desktop dar, indem Sie eine Methode namens BLT-Modus für dwm (oder BLT-Modell) verwenden.</span><span class="sxs-lookup"><span data-stu-id="3a092-125">When DWM is enabled, windowed mode applications present their contents on the Desktop by using a method called Blt Mode Present to DWM (or Blt Model).</span></span> <span data-ttu-id="3a092-126">Beim BLT-Modell verwaltet DWM eine Kopie der gerenderten Direct3D 9Ex-Oberfläche für die Desktop Komposition.</span><span class="sxs-lookup"><span data-stu-id="3a092-126">With Blt Model, DWM maintains a copy of the Direct3D 9Ex rendered surface for Desktop composition.</span></span> <span data-ttu-id="3a092-127">Wenn die Anwendung aktualisiert wird, wird der neue Inhalt über ein BLT auf die DWM-Oberfläche kopiert.</span><span class="sxs-lookup"><span data-stu-id="3a092-127">When the application updates, the new content is copied to the DWM surface through a blt.</span></span> <span data-ttu-id="3a092-128">Bei Anwendungen, die Direct3D-und GDI-Inhalte enthalten, werden die GDI-Daten auch auf die DWM-Oberfläche kopiert.</span><span class="sxs-lookup"><span data-stu-id="3a092-128">For applications that contain Direct3D and GDI content, the GDI data is also copied onto the DWM surface.</span></span>

<span data-ttu-id="3a092-129">Der in Windows 7 verfügbare Flip-Modus für die DWM (oder das Flip-Modell) ist eine neue Präsentationsmethode, die im Wesentlichen das Übergeben von Handles von Anwendungs Oberflächen zwischen Anwendungen im Fenstermodus und DWM ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="3a092-129">Available in Windows 7, Flip Mode Present to DWM (or Flip Model) is a new presentation method that essentially enables passing handles of application surfaces between windowed mode applications and DWM.</span></span> <span data-ttu-id="3a092-130">Zusätzlich zum Speichern von Ressourcen unterstützt das Flip Model erweiterte vorhandene Statistiken.</span><span class="sxs-lookup"><span data-stu-id="3a092-130">In addition to saving resources, Flip Model supports enhanced present statistics.</span></span>

<span data-ttu-id="3a092-131">Aktuelle Statistiken sind Informationen zur Rahmen Zeit, die Anwendungen verwenden können, um Video-und Audiostreams zu synchronisieren und die Wiederherstellung von Videowiedergabe-Störungen durchführen.</span><span class="sxs-lookup"><span data-stu-id="3a092-131">Present statistics are frame-timing information that applications can use to synchronize video and audio streams and recover from video playback glitches.</span></span> <span data-ttu-id="3a092-132">Die Informationen zur Rahmen Zeitangabe in der aktuellen Statistik ermöglichen es Anwendungen, die Präsentations Rate ihrer Video Frames für eine reibungslosere Darstellung anzupassen.</span><span class="sxs-lookup"><span data-stu-id="3a092-132">The frame-timing information in present statistics allows applications to adjust the presentation rate of their video frames for smoother presentation.</span></span> <span data-ttu-id="3a092-133">In Windows Vista, wo DWM eine entsprechende Kopie der Frame Oberfläche für die Desktop Komposition beibehält, können Anwendungen die von DWM bereitgestellten aktuellen Statistiken verwenden.</span><span class="sxs-lookup"><span data-stu-id="3a092-133">In Windows Vista, where DWM maintains a corresponding copy of the frame surface for Desktop composition, applications can use present statistics provided by DWM.</span></span> <span data-ttu-id="3a092-134">Diese Methode zum Abrufen vorhandener Statistiken ist in Windows 7 für vorhandene Anwendungen weiterhin verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3a092-134">This method of obtaining present statistics will still be available in Windows 7 for existing applications.</span></span>

<span data-ttu-id="3a092-135">In Windows 7 sollten Direct3D 9Ex-basierte Anwendungen, die ein Flip-Modell übernehmen, D3D9Ex-APIs verwenden, um aktuelle Statistiken abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3a092-135">In Windows 7, Direct3D 9Ex-based applications that adopt Flip Model should use D3D9Ex APIs to obtain present statistics.</span></span> <span data-ttu-id="3a092-136">Wenn DWM aktiviert ist, können der Fenstermodus und der exklusive Vollbildmodus Direct3D 9Ex-Anwendungen bei Verwendung von Flip Model die gleichen aktuellen Statistik Informationen erwarten.</span><span class="sxs-lookup"><span data-stu-id="3a092-136">When DWM is enabled, windowed mode and full-screen exclusive mode Direct3D 9Ex applications can expect the same present statistics information when using Flip Model.</span></span> <span data-ttu-id="3a092-137">Direct3D 9Ex Flip Model Present Statistics ermöglicht Anwendungen, vorhandene Statistiken in Echtzeit abzufragen, statt den Frame auf dem Bildschirm anzuzeigen. die gleichen aktuellen Statistik Informationen sind für Flip-Model aktivierte Anwendungen im Fenstermodus als Vollbildanwendungen verfügbar. ein hinzugefügtes Flag in D3D9Ex-APIs ermöglicht das Kippen von Modell Anwendungen zum effektiven verwerfen späterer Frames zur Präsentationszeit.</span><span class="sxs-lookup"><span data-stu-id="3a092-137">Direct3D 9Ex Flip Model present statistics enable applications to query for present statistics in real time, rather than after the frame has been shown on screen; the same present statistics information is available for windowed-mode Flip-Model enabled applications as full-screen applications; an added flag in D3D9Ex APIs allows Flip Model applications to effectively discard late frames at presentation time.</span></span>

<span data-ttu-id="3a092-138">Das Direct3D 9Ex-Flip-Modell sollte von neuen Video-oder Frameraten basierten Präsentations Anwendungen für Windows 7 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3a092-138">Direct3D 9Ex Flip Model should be used by new video or frame rate-based presentation applications that target Windows 7.</span></span> <span data-ttu-id="3a092-139">Aufgrund der Synchronisierung zwischen DWM und der Direct3D 9Ex-Laufzeit sollten Anwendungen, die das Flip Model verwenden, zwischen 2 und 4 backbuffers angeben, um eine reibungslose Darstellung sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="3a092-139">Because of the synchronization between DWM and the Direct3D 9Ex runtime, applications that use Flip Model should specify between 2 to 4 backbuffers to ensure smooth presentation.</span></span> <span data-ttu-id="3a092-140">Die Anwendungen, die aktuelle Statistik Informationen verwenden, profitieren von der Verwendung von Flip-Modellen, die Verbesserungen der Statistik</span><span class="sxs-lookup"><span data-stu-id="3a092-140">Those applications that use present statistics information will benefit from using Flip Model enabled present statistics enhancements.</span></span>

## <a name="direct3d-9ex-flip-mode-presentation"></a><span data-ttu-id="3a092-141">Direct3D 9Ex-Flip-Modus-Präsentation</span><span class="sxs-lookup"><span data-stu-id="3a092-141">Direct3D 9EX Flip Mode Presentation</span></span>

<span data-ttu-id="3a092-142">Leistungsverbesserungen für den Direct3D 9Ex-Flip-Modus sind im System wichtig, wenn DWM eingeschaltet ist und sich die Anwendung im Fenstermodus befindet und nicht im Vollbildmodus.</span><span class="sxs-lookup"><span data-stu-id="3a092-142">Performance improvements of Direct3D 9Ex Flip Mode Present are significant on the system when DWM is on and when the application is in windowed mode, rather than in full screen exclusive mode.</span></span> <span data-ttu-id="3a092-143">In der folgenden Tabelle und Abbildung ist ein vereinfachter Vergleich der Speicher Bandbreiten-Verwendungen und der System Lese-und Schreibvorgänge von Fenster Anwendungen dargestellt, die das Modell kippen im Vergleich zum standardmäßigen BLT-Modell verwenden.</span><span class="sxs-lookup"><span data-stu-id="3a092-143">The following table and illustration show a simplified comparison of memory bandwidth usages and system reads and writes of windowed applications that choose Flip Model versus the default usage Blt Model.</span></span>



| <span data-ttu-id="3a092-144">BLT-Modus für DWM vorhanden</span><span class="sxs-lookup"><span data-stu-id="3a092-144">Blt mode present to DWM</span></span>                                                                                                 | <span data-ttu-id="3a092-145">D3D9Ex-Flip-Modus für DWM vorhanden</span><span class="sxs-lookup"><span data-stu-id="3a092-145">D3D9Ex Flip Mode Present to DWM</span></span>                                             |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="3a092-146">1. die Anwendung aktualisiert Ihren Frame (schreiben).</span><span class="sxs-lookup"><span data-stu-id="3a092-146">1. The application updates its frame (Write)</span></span><br/>                                                                 | <span data-ttu-id="3a092-147">1. die Anwendung aktualisiert Ihren Frame (schreiben).</span><span class="sxs-lookup"><span data-stu-id="3a092-147">1. The application updates its frame (Write)</span></span><br/>                     |
| <span data-ttu-id="3a092-148">2. Direct3D Runtime kopiert Oberflächen Inhalte in eine DWM-Umleitungs Oberfläche (lesen, schreiben)</span><span class="sxs-lookup"><span data-stu-id="3a092-148">2. Direct3D runtime copies surface contents to a DWM redirection surface (Read, Write)</span></span><br/>                       | <span data-ttu-id="3a092-149">2. Direct3D Runtime übergibt die Anwendungsoberfläche an DWM</span><span class="sxs-lookup"><span data-stu-id="3a092-149">2. Direct3D runtime passes the application surface to DWM</span></span><br/>        |
| <span data-ttu-id="3a092-150">3. Nachdem die freigegebene Oberflächen Kopie abgeschlossen ist, rendert DWM die Anwendungsoberfläche auf dem Bildschirm (lesen, schreiben)</span><span class="sxs-lookup"><span data-stu-id="3a092-150">3. After the shared surface copy is completed, DWM renders the application surface onto screen (Read, Write)</span></span><br/> | <span data-ttu-id="3a092-151">3. DWM rendert die Anwendungsoberfläche auf dem Bildschirm (lesen, schreiben)</span><span class="sxs-lookup"><span data-stu-id="3a092-151">3. DWM renders the application surface onto screen (Read, Write)</span></span><br/> |



 

![Abbildung eines Vergleichs zwischen dem BLT-Modell und dem Flip-Modell](images/blt-flip-mode-present.png)

<span data-ttu-id="3a092-153">Der Flip-Modus stellt die Systemspeicher Auslastung durch Verringern der Anzahl von Lese-und Schreibvorgängen durch die Direct3D-Laufzeit für die Zusammenstellung des Fensterrahmens durch DWM reduziert.</span><span class="sxs-lookup"><span data-stu-id="3a092-153">Flip Mode Present reduces system memory usage by reducing the number of reads and writes by the Direct3D runtime for the windowed frame composition by DWM.</span></span> <span data-ttu-id="3a092-154">Dadurch wird der System Energieverbrauch und die Gesamtspeicher Auslastung reduziert.</span><span class="sxs-lookup"><span data-stu-id="3a092-154">This reduces the system power consumption and overall memory usage.</span></span>

<span data-ttu-id="3a092-155">Anwendungen können den Direct3D 9Ex-Flip-Modus nutzen, wenn DWM eingeschaltet ist, und zwar unabhängig davon, ob sich die Anwendung im Fenstermodus oder im Vollbildmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="3a092-155">Applications can take advantage of Direct3D 9Ex Flip Mode present statistics enhancements when DWM is on, regardless of whether the application is in windowed mode or in full screen exclusive mode.</span></span>

## <a name="programming-model-and-apis"></a><span data-ttu-id="3a092-156">Programmiermodell und APIs</span><span class="sxs-lookup"><span data-stu-id="3a092-156">Programming Model and APIs</span></span>

<span data-ttu-id="3a092-157">Neue Video-oder Framerate: Wenn Anwendungen, die Direct3D 9Ex-APIs unter Windows 7 verwenden, genutzt werden können, kann der Arbeitsspeicher und die Energieeinsparung und die verbesserte Darstellung des Flip-Modus bei Ausführung unter Windows 7 genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="3a092-157">New video or frame rate-gauging applications that use Direct3D 9Ex APIs on Windows 7 can take advantage of the memory and power savings and of the improved presentation offered by Flip Mode Present when running on Windows 7.</span></span> <span data-ttu-id="3a092-158">(Bei Ausführung unter früheren Windows-Versionen wird die Anwendung von der Direct3D-Laufzeit standardmäßig auf den BLT-Modus festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="3a092-158">(When running on previous Windows versions, the Direct3D runtime defaults the application to Blt Mode Present.)</span></span>

<span data-ttu-id="3a092-159">Der Flip-Modus ist erforderlich, wenn die Anwendung die Echt Zeit Statistik-Feedback-und Korrekturmechanismen nutzen kann, wenn DWM eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="3a092-159">Flip Mode Present entails that the application can take advantage of real-time present statistics feedback and correction mechanisms when DWM is on.</span></span> <span data-ttu-id="3a092-160">Anwendungen, die den Flip-Modus verwenden, sollten jedoch die Einschränkungen beachten, wenn Sie das gleichzeitige GDI-API-Rendering verwenden.</span><span class="sxs-lookup"><span data-stu-id="3a092-160">However, applications that use Flip Mode Present should be aware of limitations when they use concurrent GDI API rendering.</span></span>

<span data-ttu-id="3a092-161">Sie können vorhandene Anwendungen so ändern, dass Sie den Modus "Flip-Modus" mit den gleichen Vorteilen und Einschränkungen wie die neu entwickelten Anwendungen nutzen.</span><span class="sxs-lookup"><span data-stu-id="3a092-161">You can modify existing applications to take advantage of Flip Mode Present, with the same benefits and caveats as the newly developed applications.</span></span>

### <a name="how-to-opt-into-the-direct3d-9ex-flip-model"></a><span data-ttu-id="3a092-162">So abonnieren Sie das Direct3D 9Ex-Flip-Modell</span><span class="sxs-lookup"><span data-stu-id="3a092-162">How to Opt Into the Direct3D 9Ex Flip Model</span></span>

<span data-ttu-id="3a092-163">Direct3D 9Ex-Anwendungen, die auf Windows 7 abzielen, können das Flip-Modell nutzen, indem Sie die Swapkette mit dem [**D3DSWAPEFFECT \_ flipex**](/windows/desktop/direct3d9/d3dswapeffect) -Enumerationswert erstellen.</span><span class="sxs-lookup"><span data-stu-id="3a092-163">Direct3D 9Ex applications that target Windows 7 can opt into the Flip Model by creating the swap chain with the [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) enumeration value.</span></span> <span data-ttu-id="3a092-164">Um das Flip-Modell zu abonnieren, geben Anwendungen die [**D3DPRESENT \_ Parameters**](/windows/desktop/direct3d9/d3dpresent-parameters) -Struktur an und übergeben dann einen Zeiger auf diese Struktur, wenn Sie die [**IDirect3D9Ex:: deatedeviceex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) -API aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3a092-164">To opt into the Flip Model, applications specify the [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) structure, and then pass a pointer to this structure when they call the [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) API.</span></span> <span data-ttu-id="3a092-165">In diesem Abschnitt wird beschrieben, wie Anwendungen, die auf Windows 7 abzielen, **IDirect3D9Ex:: kreatedeviceex** verwenden, um das Flip-Modell zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="3a092-165">This section describes how applications that target Windows 7 use **IDirect3D9Ex::CreateDeviceEx** to opt into the Flip Model.</span></span> <span data-ttu-id="3a092-166">Weitere Informationen zur **IDirect3D9Ex:: deatedeviceex** -API finden Sie auf der MSDN-Website unter **IDirect3D9Ex:: kreatedeviceex**.</span><span class="sxs-lookup"><span data-stu-id="3a092-166">For more information about the **IDirect3D9Ex::CreateDeviceEx** API, see **IDirect3D9Ex::CreateDeviceEx on MSDN**.</span></span>

<span data-ttu-id="3a092-167">Der Zweck wird die Syntax von [**D3DPRESENT \_ Parametern**](/windows/desktop/direct3d9/d3dpresent-parameters) und [**IDirect3D9Ex:: kreatedeviceex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) hier wiederholt.</span><span class="sxs-lookup"><span data-stu-id="3a092-167">For convenience, the syntax of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) and [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) is repeated here.</span></span>

``` syntax
HRESULT CreateDeviceEx(
  UINT Adapter,
  D3DDEVTYPE DeviceType,
  HWND hFocusWindow,
  DWORD BehaviorFlags,
  D3DPRESENT_PARAMETERS* pPresentationParameters,
  D3DDISPLAYMODEEX *pFullscreenDisplayMode,
  IDirect3DDevice9Ex **ppReturnedDeviceInterface
);
```

``` syntax
typedef struct D3DPRESENT_PARAMETERS {
    UINT BackBufferWidth, BackBufferHeight;
    D3DFORMAT BackBufferFormat;
    UINT BackBufferCount;
    D3DMULTISAMPLE_TYPE MultiSampleType;
    DWORD MultiSampleQuality;
    D3DSWAPEFFECT SwapEffect;
    HWND hDeviceWindow;
    BOOL Windowed;
    BOOL EnableAutoDepthStencil;
    D3DFORMAT AutoDepthStencilFormat;
    DWORD Flags;
    UINT FullScreen_RefreshRateInHz;
    UINT PresentationInterval;
} D3DPRESENT_PARAMETERS, *LPD3DPRESENT_PARAMETERS;
```

<span data-ttu-id="3a092-168">Wenn Sie Direct3D 9Ex-Anwendungen für Windows 7 ändern, um das Flip-Modell zu abonnieren, sollten Sie die folgenden Elemente zu den angegebenen Membern von [**D3DPRESENT- \_ Parametern**](/windows/desktop/direct3d9/d3dpresent-parameters)berücksichtigen:</span><span class="sxs-lookup"><span data-stu-id="3a092-168">When you modify Direct3D 9Ex applications for Windows 7 to opt into the Flip Model, you should consider the following items about the specified members of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters):</span></span>

<dl> <dt>

<span data-ttu-id="3a092-169">**BackBufferCount**</span><span class="sxs-lookup"><span data-stu-id="3a092-169">**BackBufferCount**</span></span>
</dt> <dd>

<span data-ttu-id="3a092-170">(Nur Windows 7)</span><span class="sxs-lookup"><span data-stu-id="3a092-170">(Windows 7 Only)</span></span>

<span data-ttu-id="3a092-171">Wenn **SwapEffect** auf den neuen D3DSWAPEFFECT flipex-SwapChain-Effekt-Typ festgelegt ist \_ , sollte die zurück Puffer Anzahl gleich oder größer als 2 sein, um eine Anwendungsleistung zu verhindern, weil darauf gewartet wird, dass der vorherige aktuelle Puffer von DWM freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3a092-171">When **SwapEffect** is set to the new D3DSWAPEFFECT\_FLIPEX swap chain effect type, the back buffer count should be equal or greater than 2, to prevent an application performance penalty as a result of waiting on the previous Present buffer to be released by DWM.</span></span>

<span data-ttu-id="3a092-172">Wenn die Anwendung auch aktuelle Statistiken verwendet, die D3DSWAPEFFECT \_ flipex zugeordnet sind, empfiehlt es sich, die zurück Puffer Anzahl auf von 2 auf 4 festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3a092-172">When the application also uses present statistics associated with D3DSWAPEFFECT\_FLIPEX, we recommend that you set the back buffer count to from 2 to 4.</span></span>

<span data-ttu-id="3a092-173">Die Verwendung \_ von D3DSWAPEFFECT flipex unter Windows Vista oder früheren Betriebssystemversionen führt zu einem Fehler von " [**devatedeviceex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)".</span><span class="sxs-lookup"><span data-stu-id="3a092-173">Using D3DSWAPEFFECT\_FLIPEX on Windows Vista or previous operating system versions will return fail from [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span>

</dd> <dt>

<span data-ttu-id="3a092-174">**SwapEffect verwenden**</span><span class="sxs-lookup"><span data-stu-id="3a092-174">**SwapEffect**</span></span>
</dt> <dd>

<span data-ttu-id="3a092-175">(Nur Windows 7)</span><span class="sxs-lookup"><span data-stu-id="3a092-175">(Windows 7 Only)</span></span>

<span data-ttu-id="3a092-176">Der neue D3DSWAPEFFECT \_ flipex-SwapChain-Effekt wird festgelegt, wenn eine Anwendung den Flip-Modus annimmt, der in DWM vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3a092-176">The new D3DSWAPEFFECT\_FLIPEX swap chain effect type designates when an application is adopting Flip Mode Present to DWM.</span></span> <span data-ttu-id="3a092-177">Dies ermöglicht es der Anwendung, den Arbeitsspeicher und die Leistung effizienter zu nutzen, und ermöglicht es der Anwendung, die voll Bild Anzeige im Fenstermodus zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="3a092-177">It allows the application more efficient usage of memory and power, and also enables the application to take advantage of full-screen present statistics in windowed mode.</span></span> <span data-ttu-id="3a092-178">Das Verhalten von Vollbildanwendungen ist nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="3a092-178">Full-screen application behavior is not affected.</span></span> <span data-ttu-id="3a092-179">Wenn "Windowed" auf " **true** " festgelegt ist und " **Swap-Effekt** " auf D3DSWAPEFFECT flipex festgelegt ist \_ , erstellt die Laufzeit einen zusätzlichen Hintergrund Puffer und rotiert, welches Handle zu dem Puffer gehört, der zur Präsentationszeit zum Vordergrund Puffer wird.</span><span class="sxs-lookup"><span data-stu-id="3a092-179">If Windowed is set to **TRUE** and **SwapEffect** is set to D3DSWAPEFFECT\_FLIPEX, the runtime creates one extra back buffer and rotates whichever handle belongs to the buffer that becomes the front buffer at presentation time.</span></span>

</dd> <dt>

<span data-ttu-id="3a092-180">**Flags**</span><span class="sxs-lookup"><span data-stu-id="3a092-180">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="3a092-181">(Nur Windows 7)</span><span class="sxs-lookup"><span data-stu-id="3a092-181">(Windows 7 Only)</span></span>

<span data-ttu-id="3a092-182">Das [D3DPRESENTFLAG \_ Lockable \_ BackBuffer](/windows/desktop/direct3d9/d3dpresentflag) -Flag kann nicht festgelegt werden, wenn SwapEffect auf den neuen [**D3DSWAPEFFECT \_ flipex**](/windows/desktop/direct3d9/d3dswapeffect) - **SwapChain** -Effekt-Typ festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3a092-182">The [D3DPRESENTFLAG\_LOCKABLE\_BACKBUFFER](/windows/desktop/direct3d9/d3dpresentflag) flag cannot be set if **SwapEffect** is set to the new [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) swap chain effect type.</span></span>

</dd> </dl>

### <a name="design-guidelines-for-direct3d-9ex-flip-model-applications"></a><span data-ttu-id="3a092-183">Entwurfs Richtlinien für Direct3D 9Ex-Flip Model-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="3a092-183">Design Guidelines for Direct3D 9Ex Flip Model Applications</span></span>

<span data-ttu-id="3a092-184">Verwenden Sie die Richtlinien in den folgenden Abschnitten, um Ihre Direct3D 9Ex-Flip-Modell Anwendungen zu entwerfen.</span><span class="sxs-lookup"><span data-stu-id="3a092-184">Use the guidelines in the following sections to design your Direct3D 9Ex Flip Model applications.</span></span>

### <a name="use-flip-mode-present-in-a-separate-hwnd-from-blt-mode-present"></a><span data-ttu-id="3a092-185">Verwenden des Flip-Modus, der in einem separaten HWND aus dem BLT-Modus vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="3a092-185">Use Flip Mode Present in a Separate HWND from Blt Mode Present</span></span>

<span data-ttu-id="3a092-186">Anwendungen sollten den Direct3D 9Ex-Flip-Modus verwenden, der in einem HWND enthalten ist, das nicht auch andere APIs als Ziel hat, einschließlich BLT-Modus Direct3D 9Ex, andere Versionen von Direct3D oder GDI.</span><span class="sxs-lookup"><span data-stu-id="3a092-186">Applications should use Direct3D 9Ex Flip Mode Present in an HWND that is not also targeted by other APIs, including Blt Mode Present Direct3D 9Ex, other versions of Direct3D, or GDI.</span></span> <span data-ttu-id="3a092-187">Der im Fenster "Kippen" vorhandene Modus kann verwendet werden, um untergeordnete Fenster anzuzeigen. Das heißt, Anwendungen können das Flip-Modell verwenden, wenn es nicht mit dem BLT-Modell im gleichen HWND gemischt wird, wie in den folgenden Abbildungen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3a092-187">Flip Mode Present can be used to present to child windows; that is, applications can use Flip Model when it is not mixed with Blt Model in the same HWND, as shown in the following illustrations.</span></span>

![Darstellung des übergeordneten Fensters Direct3D und eines untergeordneten GDI-Fensters mit jeweils eigenem HWND](images/parent-d3d.png)

![Darstellung des übergeordneten GDI-Fensters und eines untergeordneten Direct3D-Fensters mit jeweils eigenem HWND](images/parent-gdi.png)

<span data-ttu-id="3a092-190">Da das BLT-Modell eine zusätzliche Kopie der Oberfläche beibehält, können GDI und andere Direct3D-Inhalte dem gleichen HWND durch schrittweise Updates von Direct3D und GDI hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="3a092-190">Because Blt Model maintains an additional copy of the surface, GDI and other Direct3D contents can be added to the same HWND through piecemeal updates from Direct3D and GDI.</span></span> <span data-ttu-id="3a092-191">Mit dem Flip-Modell werden nur Direct3D 9Ex-Inhalte in [**D3DSWAPEFFECT \_ flipex**](/windows/desktop/direct3d9/d3dswapeffect) -Austausch Ketten, die an DWM übermittelt werden, sichtbar.</span><span class="sxs-lookup"><span data-stu-id="3a092-191">Using the Flip Model, only Direct3D 9Ex content in [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) swap chains that are passed to DWM will be visible.</span></span> <span data-ttu-id="3a092-192">Alle anderen BLT-modellDirect3D-und GDI-Inhalts Aktualisierungen werden ignoriert, wie in den folgenden Abbildungen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3a092-192">All other Blt Model Direct3D or GDI content updates will be ignored, as shown in the following illustrations.</span></span>

![Abbildung des GDI-Texts, der möglicherweise nicht angezeigt wird, wenn das Modell Kippen verwendet wird und sich Direct3D-und GDI-Inhalt im gleichen HWND befinden](images/d3d-gdi-same-hwnd.png)

![Abbildung des Direct3D-und GDI-Inhalts, in dem DWM aktiviert ist und die Anwendung im Fenstermodus ausgeführt wird](images/d3d-gdinotext-same-hwnd.png)

<span data-ttu-id="3a092-195">Daher sollte das Flip-Modell für Swapketten-Puffer Oberflächen aktiviert werden, bei denen das Direct3D 9Ex-Flip-Modell allein auf das gesamte HWND gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="3a092-195">Therefore, Flip Model should be enabled for swap chain buffers surfaces where the Direct3D 9Ex Flip Model alone renders to the entire HWND.</span></span>

### <a name="do-not-use-flip-model-with-gdis-scrollwindow-or-scrollwindowex"></a><span data-ttu-id="3a092-196">Verwenden Sie "Flip Model" nicht mit dem "scrollwindow" oder "scrollwindowex" von GDI</span><span class="sxs-lookup"><span data-stu-id="3a092-196">Do Not Use Flip Model with GDI's ScrollWindow or ScrollWindowEx</span></span>

<span data-ttu-id="3a092-197">Einige Direct3D 9Ex-Anwendungen verwenden die Funktionen scrollwindow oder scrollwindowex von GDI zum Aktualisieren von Fenster Inhalten, wenn ein Benutzer scrollereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="3a092-197">Some Direct3D 9Ex applications use GDI's ScrollWindow or ScrollWindowEx functions to update window contents when a user scroll event is triggered.</span></span> <span data-ttu-id="3a092-198">Scrollwindow und scrollwindowex führen BLTS von Fenster Inhalten auf dem Bildschirm aus, während ein Fenster einen Bildlauf ausführt.</span><span class="sxs-lookup"><span data-stu-id="3a092-198">ScrollWindow and ScrollWindowEx perform blts of window contents on screen as a window is scrolled.</span></span> <span data-ttu-id="3a092-199">Diese Funktionen erfordern auch BLT-Modell Updates für GDI und Direct3D 9Ex-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="3a092-199">These functions also require Blt Model updates for GDI and Direct3D 9Ex content.</span></span> <span data-ttu-id="3a092-200">Anwendungen, die eine der beiden Funktionen verwenden, zeigen nicht notwendigerweise sichtbare Fenster Inhalte auf dem Bildschirm an, wenn sich die Anwendung im Fenstermodus befindet und DWM aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3a092-200">Applications that use either function will not necessarily display visible window contents scrolling on screen when the application is in windowed mode and DWM is enabled.</span></span> <span data-ttu-id="3a092-201">Es wird empfohlen, die scrollwindow-und scrollwindowex-APIs von GDI nicht in Ihren Anwendungen zu verwenden und stattdessen ihren Inhalt auf dem Bildschirm neu zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="3a092-201">We recommend that you not use GDI's ScrollWindow and ScrollWindowEx APIs in your applications, and instead redraw their contents on screen in response to scrolling.</span></span>

### <a name="use-one-d3dswapeffect_flipex-swap-chain-per-hwnd"></a><span data-ttu-id="3a092-202">Verwenden Sie eine D3DSWAPEFFECT \_ flipex-Swap-Kette pro HWND.</span><span class="sxs-lookup"><span data-stu-id="3a092-202">Use One D3DSWAPEFFECT\_FLIPEX Swap Chain per HWND</span></span>

<span data-ttu-id="3a092-203">Anwendungen, die das Flip-Modell verwenden, sollten nicht mehrere Flip-Modell Austausch Ketten verwenden, die auf das gleiche HWND abzielen.</span><span class="sxs-lookup"><span data-stu-id="3a092-203">Applications that use Flip Model should not use multiple Flip Model swap chains targeting the same HWND.</span></span>

### <a name="frame-synchronization-of-direct3d-9ex-flip-model-applications"></a><span data-ttu-id="3a092-204">Frame Synchronisierung von Direct3D 9Ex-kippen-Modell Anwendungen</span><span class="sxs-lookup"><span data-stu-id="3a092-204">Frame Synchronization of Direct3D 9Ex Flip Model Applications</span></span>

<span data-ttu-id="3a092-205">Aktuelle Statistiken sind Informationen zu Frame Timeouts, die Medienanwendungen zum Synchronisieren von Video-und Audiodatenströmen und zum Wiederherstellen von Videowiedergabe-Störungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="3a092-205">Present statistics are frame timing information that media applications use to synchronize video and audio streams and recover from video playback glitches.</span></span> <span data-ttu-id="3a092-206">Um die Verfügbarkeit der aktuellen Statistik zu aktivieren, muss die Anwendung Direct3D 9Ex sicherstellen, dass der von der Anwendung an [**IDirect3D9Ex:: deatedeviceex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) übergebene Parameter " *verhaltenflags* " das geräteverhaltenflag [D3DCREATE " \_ \_ presentstats aktivieren](/windows/desktop/direct3d9/d3dcreate)" enthält.</span><span class="sxs-lookup"><span data-stu-id="3a092-206">To enable present statistics availability, the Direct3D 9Ex application must ensure that the *BehaviorFlags* parameter that the application passes to [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) contains the device behavior flag [D3DCREATE\_ENABLE\_PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate).</span></span>

<span data-ttu-id="3a092-207">Die Syntax von [**IDirect3D9Ex:: kreatedeviceex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) wird hier wiederholt.</span><span class="sxs-lookup"><span data-stu-id="3a092-207">For convenience, the syntax of [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) is repeated here.</span></span>

``` syntax
HRESULT CreateDeviceEx(
  UINT Adapter,
  D3DDEVTYPE DeviceType,
  HWND hFocusWindow,
  DWORD BehaviorFlags,
  D3DPRESENT_PARAMETERS* pPresentationParameters,
  D3DDISPLAYMODEEX *pFullscreenDisplayMode,
  IDirect3DDevice9Ex **ppReturnedDeviceInterface
);
```

<span data-ttu-id="3a092-208">Das Direct3D 9Ex-Flip-Modell fügt das [D3DPRESENT \_ forceimvermittler](/windows/desktop/direct3d9/d3dpresent) -präsentationsflag hinzu, das das D3DPRESENT Interval-Verhalten der [ \_ \_ unmittelbaren](/windows/desktop/direct3d9/d3dpresent) Darstellung/Flag erzwingt.</span><span class="sxs-lookup"><span data-stu-id="3a092-208">Direct3D 9Ex Flip Model adds the [D3DPRESENT\_FORCEIMMEDIATE](/windows/desktop/direct3d9/d3dpresent) presentation flag that enforces the [D3DPRESENT\_INTERVAL\_IMMEDIATE](/windows/desktop/direct3d9/d3dpresent) presentation-flag behavior.</span></span> <span data-ttu-id="3a092-209">Die Anwendung Direct3D 9Ex gibt diese Präsentationsflags im *dwFlags* -Parameter an, den die Anwendung an [**IDirect3DDevice9Ex::P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex)übergibt, wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="3a092-209">The Direct3D 9Ex application specifies these presentation flags in the *dwFlags* parameter that the application passes to [**IDirect3DDevice9Ex::PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex), as shown here.</span></span>

``` syntax
HRESULT PresentEx(
  CONST RECT *pSourceRect,
  CONST RECT *pDestRect,
  HWND hDestWindowOverride,
  CONST RGNDATA *pDirtyRegion,
  DWORD dwFlags
);
```

<span data-ttu-id="3a092-210">Wenn Sie Ihre Direct3D 9Ex-Anwendung für Windows 7 ändern, sollten Sie die folgenden Informationen zu den angegebenen [D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) Presentation-Flags berücksichtigen:</span><span class="sxs-lookup"><span data-stu-id="3a092-210">When you modify your Direct3D 9Ex application for Windows 7, you should consider the following information about the specified [D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) presentation flags:</span></span>

<dl> <dt>

[<span data-ttu-id="3a092-211">D3DPRESENT \_ donotflip</span><span class="sxs-lookup"><span data-stu-id="3a092-211">D3DPRESENT\_DONOTFLIP</span></span>](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

<span data-ttu-id="3a092-212">Dieses Flag ist nur im Vollbildmodus verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3a092-212">This flag is available only in full-screen mode or</span></span>

<span data-ttu-id="3a092-213">(Nur Windows 7)</span><span class="sxs-lookup"><span data-stu-id="3a092-213">(Windows 7 Only)</span></span>

<span data-ttu-id="3a092-214">Wenn die Anwendung den " **deviapeffect** "-Member von "D3DPRESENT"- [**\_ Parametern**](/windows/desktop/direct3d9/d3dpresent-parameters) in einem [**Aufrufen von "**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) [**" für " \_ "**](/windows/desktop/direct3d9/d3dswapeffect) auf "" festlegt.</span><span class="sxs-lookup"><span data-stu-id="3a092-214">when the application sets the **SwapEffect** member of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) to [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in a call to [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span>

</dd> <dt>

[<span data-ttu-id="3a092-215">D3DPRESENT \_ forceimvermittlung</span><span class="sxs-lookup"><span data-stu-id="3a092-215">D3DPRESENT\_FORCEIMMEDIATE</span></span>](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

<span data-ttu-id="3a092-216">(Nur Windows 7)</span><span class="sxs-lookup"><span data-stu-id="3a092-216">(Windows 7 Only)</span></span>

<span data-ttu-id="3a092-217">Dieses Flag kann nur angegeben werden, wenn die Anwendung den " **deviapeffect** "-Member der [**D3DPRESENT- \_ Parameter**](/windows/desktop/direct3d9/d3dpresent-parameters) auf " [**D3DSWAPEFFECT \_ flipex**](/windows/desktop/direct3d9/d3dswapeffect) " in einem Aufrufen von " [**kreatedeviceex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)" festlegt.</span><span class="sxs-lookup"><span data-stu-id="3a092-217">This flag can be specified only if the application sets the **SwapEffect** member of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) to [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in a call to [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span> <span data-ttu-id="3a092-218">Die Anwendung kann dieses Flag verwenden, um eine Oberfläche mit mehreren Frames zu einem späteren Zeitpunkt in der vorhandenen DWM-Warteschlange zu aktualisieren, wobei im Grunde zwischen Frames übersprungen werden.</span><span class="sxs-lookup"><span data-stu-id="3a092-218">The application can use this flag to immediately update a surface with several frames later in the DWM Present queue, essentially skipping intermediate frames.</span></span>

<span data-ttu-id="3a092-219">Fenster mit flipex-aktivierten Anwendungen können mit diesem Flag sofort eine Oberfläche mit einem Frame aktualisieren, der später in der DWM-Warteschlange vorhanden ist, und zwischen Frames übersprungen.</span><span class="sxs-lookup"><span data-stu-id="3a092-219">Windowed FlipEx-enabled applications can use this flag to immediately update a surface with a frame that is later in the DWM Present queue, skipping intermediate frames.</span></span> <span data-ttu-id="3a092-220">Dies ist besonders nützlich für Medienanwendungen, die Frames verwerfen möchten, die als spät erkannt wurden, und die nachfolgenden Frames zum Zeitpunkt der Komposition darstellen.</span><span class="sxs-lookup"><span data-stu-id="3a092-220">This is especially useful for media applications that want to discard frames that have been detected as late and present subsequent frames at composition time.</span></span> <span data-ttu-id="3a092-221">[**IDirect3DDevice9Ex::P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) gibt einen Fehler wegen eines ungültigen Parameters zurück, wenn dieses Flag nicht ordnungsgemäß angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="3a092-221">[**IDirect3DDevice9Ex::PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) returns invalid parameter error if this flag is improperly specified.</span></span>

</dd> </dl>

<span data-ttu-id="3a092-222">Zum Abrufen der aktuellen Statistik Informationen erhält die Anwendung die [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) -Struktur durch Aufrufen der [**IDirect3DSwapChain9Ex:: getpresentstatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) -API.</span><span class="sxs-lookup"><span data-stu-id="3a092-222">To obtain present statistics information, the application obtains the [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure by calling the [**IDirect3DSwapChain9Ex::GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) API.</span></span>

<span data-ttu-id="3a092-223">Die [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) -Struktur enthält Statistiken zu [**IDirect3DDevice9Ex::P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) -aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3a092-223">The [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure contains statistics about [**IDirect3DDevice9Ex::PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) calls.</span></span> <span data-ttu-id="3a092-224">Das Gerät muss mithilfe eines [**IDirect3D9Ex:: ":: kreatedeviceex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) "- [Aufrufes mit dem D3DCREATE \_ enable \_ presentstats](/windows/desktop/direct3d9/d3dcreate) -Flag erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="3a092-224">The device must be created by using a [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) call with the [D3DCREATE\_ENABLE\_PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) flag.</span></span> <span data-ttu-id="3a092-225">Andernfalls sind die von [**getpresentstatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) zurückgegebenen Daten nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="3a092-225">Otherwise, the data returned by [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) is undefined.</span></span> <span data-ttu-id="3a092-226">Eine mit einem Flip-Modell aktivierte Direct3D 9Ex-Swapkette stellt aktuelle Statistik Informationen sowohl im Fenstermodus als auch im Vollbildmodus bereit.</span><span class="sxs-lookup"><span data-stu-id="3a092-226">A Flip-Model-enabled Direct3D 9Ex swap chain provides present statistics information in both windowed and full-screen modes.</span></span>

<span data-ttu-id="3a092-227">Für BLT-Model-aktivierte Direct3D 9Ex-Swapketten im Fenstermodus werden alle [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) -Struktur Werte als Nullen verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a092-227">For Blt-Model-enabled Direct3D 9Ex swap chains in windowed mode, all [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure values will be zeroes.</span></span>

<span data-ttu-id="3a092-228">Für eine flipex-Statistik gibt [**getpresentstatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) \_ \_ \_ in den folgenden Situationen eine Disjunktion der D3DERR Present Statistics zurück:</span><span class="sxs-lookup"><span data-stu-id="3a092-228">For FlipEx present statistics, [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) returns D3DERR\_PRESENT\_STATISTICS\_DISJOINT in the following situations:</span></span>

-   <span data-ttu-id="3a092-229">Zuerst Aufrufen von [**getpresentstatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) , was den Anfang einer Sequenz anzeigt</span><span class="sxs-lookup"><span data-stu-id="3a092-229">First call to [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) ever, which indicates the beginning of a sequence</span></span>
-   <span data-ttu-id="3a092-230">DWM-Übergang von on zu Off</span><span class="sxs-lookup"><span data-stu-id="3a092-230">DWM transition from on to off</span></span>
-   <span data-ttu-id="3a092-231">Modusänderung: entweder der Fenstermodus zum oder vom Vollbildmodus oder vom Vollbildmodus bis zum voll Bild Übergang</span><span class="sxs-lookup"><span data-stu-id="3a092-231">Mode change: either windowed mode to or from full screen or full screen to full screen transitions</span></span>

<span data-ttu-id="3a092-232">Die Syntax von [**getpresentstatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) wird hier wiederholt.</span><span class="sxs-lookup"><span data-stu-id="3a092-232">For convenience, the syntax of [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) is repeated here.</span></span>

``` syntax
HRESULT GetPresentStatistics(
  D3DPRESENTSTATS * pPresentationStatistics
);
```

<span data-ttu-id="3a092-233">Die [**IDirect3DSwapChain9Ex:: getlastpresentcount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) -Methode gibt den letzten presentcount zurück, d. h. die aktuelle ID des letzten erfolgreichen Aufrufens, der von einem Anzeigegerät erfolgt ist, das der Swapkette zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3a092-233">The [**IDirect3DSwapChain9Ex::GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) method returns the last PresentCount, that is, the Present ID of the last successful Present call that was made by a display device that is associated with the swap chain.</span></span> <span data-ttu-id="3a092-234">Diese vorhandene ID ist der Wert des **presentcount** -Members der [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="3a092-234">This Present ID is the value of the **PresentCount** member of the [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure.</span></span> <span data-ttu-id="3a092-235">Bei BLT-Modell fähigen Direct3D 9Ex-Swapketten werden im Fenstermodus alle **D3DPRESENTSTATS** -Struktur Werte als Nullen verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a092-235">For Blt-Model-enabled Direct3D 9Ex swap chains, while in windowed mode, all **D3DPRESENTSTATS** structure values will be zeroes.</span></span>

<span data-ttu-id="3a092-236">Die Syntax von [**IDirect3DSwapChain9Ex:: getlastpresentcount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) wird hier wiederholt.</span><span class="sxs-lookup"><span data-stu-id="3a092-236">For convenience, the syntax of [**IDirect3DSwapChain9Ex::GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) is repeated here.</span></span>

``` syntax
HRESULT GetLastPresentCount(
  UINT * pLastPresentCount
);
```

<span data-ttu-id="3a092-237">Wenn Sie Ihre Direct3D 9Ex-Anwendung für Windows 7 ändern, sollten Sie die folgenden Informationen zur [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) -Struktur berücksichtigen:</span><span class="sxs-lookup"><span data-stu-id="3a092-237">When you modify your Direct3D 9Ex application for Windows 7, you should consider the following information about the [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure:</span></span>

-   <span data-ttu-id="3a092-238">Der von [**getlastpresentcount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) zurückgegebene presentcount-Wert wird nicht aktualisiert, wenn ein im dwFlags-Parameter angegebener [**presentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) -Befehl mit D3DPRESENT \_ donotwait einen Fehler zurückgibt. </span><span class="sxs-lookup"><span data-stu-id="3a092-238">The PresentCount value that [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) returns does not update when a [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) call with D3DPRESENT\_DONOTWAIT specified in the *dwFlags* parameter returns failure.</span></span>
-   <span data-ttu-id="3a092-239">Wenn [**presentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) mit D3DPRESENT \_ donotflip aufgerufen wird, wird ein [**getpresentstatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) -Aufruf erfolgreich ausgeführt, aber es wird keine aktualisierte [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) -Struktur zurückgegeben, wenn sich die Anwendung im Fenstermodus befindet.</span><span class="sxs-lookup"><span data-stu-id="3a092-239">When [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) is called with D3DPRESENT\_DONOTFLIP, a [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) call succeeds but does not return an updated [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure when the application is in windowed mode.</span></span>
-   <span data-ttu-id="3a092-240">**Presentfreshcount** im Vergleich zu **synkrefreshcount** in [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats):</span><span class="sxs-lookup"><span data-stu-id="3a092-240">**PresentRefreshCount** versus **SyncRefreshCount** in [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats):</span></span>
    -   <span data-ttu-id="3a092-241">**Presentfreshcount** ist gleich **synkrefreshcount** , wenn die Anwendung bei jeder VSYNC-Funktion dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3a092-241">**PresentRefreshCount** is equal to **SyncRefreshCount** when the application presents on every vsync.</span></span>
    -   <span data-ttu-id="3a092-242">**Synkrefreshcount** wird im VSYNC-Intervall abgerufen, wenn der vorhandene gesendet wurde. **syncqpctime** ist ungefähr die Zeit, die dem VSYNC-Intervall zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3a092-242">**SyncRefreshCount** is obtained on the vsync interval when the present was submitted, **SyncQPCTime** is approximately the time associated with the vsync interval.</span></span>

``` syntax
typedef struct _D3DPRESENTSTATS {
    UINT PresentCount;
    UINT PresentRefreshCount;
    UINT SyncRefreshCount;
    LARGE_INTEGER SyncQPCTime;
    LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```

### <a name="frame-synchronization-for-windowed-applications-when-dwm-is-off"></a><span data-ttu-id="3a092-243">Rahmen Synchronisierung für Fenster Anwendungen, wenn DWM deaktiviert ist</span><span class="sxs-lookup"><span data-stu-id="3a092-243">Frame Synchronization for Windowed Applications When DWM is Off</span></span>

<span data-ttu-id="3a092-244">Wenn DWM deaktiviert ist, werden Fenster Anwendungen direkt auf dem Bildschirm Monitor angezeigt, ohne dass eine Flip-Kette durchlaufen wird.</span><span class="sxs-lookup"><span data-stu-id="3a092-244">When DWM is off, windowed applications display directly to the monitor screen without going through a flip chain.</span></span> <span data-ttu-id="3a092-245">In Windows Vista wird die Beschaffung von Frame Statistik Informationen für Fenster Anwendungen nicht unterstützt, wenn DWM deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3a092-245">In Windows Vista, there is no support for obtaining frame statistics information for windowed applications when DWM is off.</span></span> <span data-ttu-id="3a092-246">Um eine API zu verwalten, bei der Anwendungen nicht DWM-fähig sein müssen, gibt Windows 7 Frame Statistik Informationen für Fenster Anwendungen zurück, wenn DWM deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3a092-246">To maintain an API where applications need not be DWM- aware, Windows 7 will return frame statistics information for windowed applications when DWM is off.</span></span> <span data-ttu-id="3a092-247">Die bei Deaktivierung von DWM zurückgegebene Frame Statistik sind nur Schädigungen.</span><span class="sxs-lookup"><span data-stu-id="3a092-247">The frame statistics returned when DWM is off are estimations only.</span></span>

## <a name="walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample"></a><span data-ttu-id="3a092-248">Walk-Through eines Direct3D 9Ex-Flip-Modells und präsentieren von Statistik Beispielen</span><span class="sxs-lookup"><span data-stu-id="3a092-248">Walk-Through of a Direct3D 9Ex Flip Model and Present Statistics Sample</span></span>

<span data-ttu-id="3a092-249">**So abonnieren Sie die flipex-Präsentation für Direct3D 9Ex Sample**</span><span class="sxs-lookup"><span data-stu-id="3a092-249">**To opt into FlipEx presentation for Direct3D 9Ex sample**</span></span>

1.  <span data-ttu-id="3a092-250">Stellen Sie sicher, dass die Beispielanwendung unter Windows 7 oder einer höheren Version des Betriebssystems ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a092-250">Ensure the sample application is running on Windows 7 or later operating system version.</span></span>
2.  <span data-ttu-id="3a092-251">Legen Sie in einem Aufrufen von " [**fiatedeviceex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)" den Member " **Swap** " von [**D3DPRESENT- \_ Parametern**](/windows/desktop/direct3d9/d3dpresent-parameters) auf [**D3DSWAPEFFECT \_ flipex**](/windows/desktop/direct3d9/d3dswapeffect) fest.</span><span class="sxs-lookup"><span data-stu-id="3a092-251">Set the **SwapEffect** member of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) to [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in a call to [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span>


```C++
    OSVERSIONINFO version;
    ZeroMemory(&version, sizeof(version));
    version.dwOSVersionInfoSize = sizeof(version);
    GetVersionEx(&version);
    
    // Sample would run only on Win7 or higher
    // Flip Model present and its associated present statistics behavior are only available on Windows 7 or higher operating system
    bool bIsWin7 = (version.dwMajorVersion > 6) || 
        ((version.dwMajorVersion == 6) && (version.dwMinorVersion >= 1));

    if (!bIsWin7)
    {
        MessageBox(NULL, L"This sample requires Windows 7 or higher", NULL, MB_OK);
        return 0;
    }
```



<span data-ttu-id="3a092-252">**Zum Abonnieren von flipex zugeordnete Statistik für Direct3D 9Ex Sample**</span><span class="sxs-lookup"><span data-stu-id="3a092-252">**To also opt into FlipEx associated Present Statistics for Direct3D 9Ex sample**</span></span>

-   <span data-ttu-id="3a092-253">Set [D3DCREATE \_ Aktivieren Sie \_ presentstats](/windows/desktop/direct3d9/d3dcreate) im *verhaltenflags* -Parameter von " [**kreatedeviceex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)".</span><span class="sxs-lookup"><span data-stu-id="3a092-253">Set [D3DCREATE\_ENABLE\_PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) in the *BehaviorFlags* parameter of [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span>


```C++
    // Set up the structure used to create the D3DDevice
    D3DPRESENT_PARAMETERS d3dpp;
    ZeroMemory(&d3dpp, sizeof(d3dpp));

    d3dpp.Windowed = TRUE;
    d3dpp.SwapEffect = D3DSWAPEFFECT_FLIPEX;        // Opts into Flip Model present for D3D9Ex swapchain
    d3dpp.BackBufferFormat = D3DFMT_X8R8G8B8;
    d3dpp.BackBufferWidth = 256;                
    d3dpp.BackBufferHeight = 256;
    d3dpp.BackBufferCount = QUEUE_SIZE;
    d3dpp.PresentationInterval = D3DPRESENT_INTERVAL_ONE;

    g_iWidth = d3dpp.BackBufferWidth;
    g_iHeight = d3dpp.BackBufferHeight;

    // Create the D3DDevice with present statistics enabled - set D3DCREATE_ENABLE_PRESENTSTATS for behaviorFlags parameter
    if(FAILED(g_pD3D->CreateDeviceEx(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                      D3DCREATE_HARDWARE_VERTEXPROCESSING | D3DCREATE_ENABLE_PRESENTSTATS,
                                      &d3dpp, NULL, &g_pd3dDevice)))
    {
        return E_FAIL;
    }
```



<span data-ttu-id="3a092-254">**So vermeiden Sie das erkennen und Wiederherstellen von Störungen**</span><span class="sxs-lookup"><span data-stu-id="3a092-254">**To avoid, detect and recover from glitches**</span></span>

1.  <span data-ttu-id="3a092-255">Warteschlangen Aufrufe vorhanden: die empfohlene Swapkette-Anzahl liegt zwischen 2 und 4.</span><span class="sxs-lookup"><span data-stu-id="3a092-255">Queue Present calls: recommended backbuffer count is from 2 to 4.</span></span>
2.  <span data-ttu-id="3a092-256">Direct3D 9Ex Sample fügt einen impliziten Swapkette hinzu, die tatsächliche Warteschlangen Länge ist die Swapkette-Anzahl + 1.</span><span class="sxs-lookup"><span data-stu-id="3a092-256">Direct3D 9Ex sample adds an implicit backbuffer, actual Present queue length is backbuffer count + 1.</span></span>
3.  <span data-ttu-id="3a092-257">Erstellen Sie eine Warteschlangen Struktur, um alle der aktuellen ID (presentcount) und zugeordnete, berechnete/erwartete presentaktualisierungzahl zu speichern.</span><span class="sxs-lookup"><span data-stu-id="3a092-257">Create helper Present queue structure to store all successfully submitted Present's Present ID (PresentCount) and associated, calculated/expected PresentRefreshCount.</span></span>
4.  <span data-ttu-id="3a092-258">So erkennen Sie das Auftreten eines Ereignisses:</span><span class="sxs-lookup"><span data-stu-id="3a092-258">To detect glitch occurrence:</span></span>

    -   <span data-ttu-id="3a092-259">Aufrufen von [**getpresentstatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3a092-259">Call [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)).</span></span>
    -   <span data-ttu-id="3a092-260">Dient zum Ermitteln der aktuellen ID (presentcount) und der VSYNC-Anzahl, bei der der Frame (presenterfrischendes count) des Frames angezeigt wird, dessen aktuelle Statistik abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3a092-260">Get the Present ID (PresentCount) and vsync count where the frame is shown (PresentRefreshCount) of the frame whose present statistics is obtained.</span></span>
    -   <span data-ttu-id="3a092-261">Rufen Sie die erwartete presentaktualisierungzahl (targetrefresh im Beispielcode) ab, die mit der aktuellen ID verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="3a092-261">Retrieve the expected PresentRefreshCount (TargetRefresh in sample code) associated with the Present ID.</span></span>
    -   <span data-ttu-id="3a092-262">Wenn die tatsächliche presentaktuellem Anzahl später als erwartet ist, ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="3a092-262">If actual PresentRefreshCount is later than expected, a glitch has occurred.</span></span>

5.  <span data-ttu-id="3a092-263">So stellen Sie eine Wiederherstellung nach einem Fehler:</span><span class="sxs-lookup"><span data-stu-id="3a092-263">To recover from glitch:</span></span>

    -   <span data-ttu-id="3a092-264">Berechnen Sie, wie viele Frames übersprungen werden sollen (g \_ iunmittelates Variable im Beispielcode).</span><span class="sxs-lookup"><span data-stu-id="3a092-264">Calculate how many frames to skip (g\_ iImmediates variable in sample code).</span></span>
    -   <span data-ttu-id="3a092-265">Präsentieren Sie die übersprungenen Frames mit Interval D3DPRESENT \_ forceimvermittler.</span><span class="sxs-lookup"><span data-stu-id="3a092-265">Present the skipped frames with interval D3DPRESENT\_FORCEIMMEDIATE.</span></span>

<span data-ttu-id="3a092-266">**Überlegungen zur Erkennung und Wiederherstellung von Störung**</span><span class="sxs-lookup"><span data-stu-id="3a092-266">**Considerations for glitch detection and recovery**</span></span>

1.  <span data-ttu-id="3a092-267">Die glitch-Wiederherstellung nimmt N (g \_ iqueuedelay-Variable im Beispielcode) Anzahl der aktuellen Aufrufe an, wobei n (g \_ iqueuedelay) dem Wert g \_ iunmittelates plus length der aktuellen Warteschlange entspricht, d. h.:</span><span class="sxs-lookup"><span data-stu-id="3a092-267">Glitch recovery takes N (g\_iQueueDelay variable in sample code) number of Present calls where N (g\_iQueueDelay) equals g\_iImmediates plus length of the Present queue, that is:</span></span>

    -   <span data-ttu-id="3a092-268">Überspringen von Frames mit vorhandenes Intervall D3DPRESENT \_ forceimvermittler, plus</span><span class="sxs-lookup"><span data-stu-id="3a092-268">Skipping frames with Present interval D3DPRESENT\_FORCEIMMEDIATE, plus</span></span>
    -   <span data-ttu-id="3a092-269">In der Warteschlange befindliche präsente, die verarbeitet werden müssen</span><span class="sxs-lookup"><span data-stu-id="3a092-269">Queued Presents that need to be processed</span></span>

2.  <span data-ttu-id="3a092-270">Legen Sie eine Beschränkung auf die Länge des zulässigen Werts fest (das Limit für die \_ Wiederherstellung \_ in Stichproben).</span><span class="sxs-lookup"><span data-stu-id="3a092-270">Set a limit to the glitch length (GLITCH\_RECOVERY\_LIMIT in sample).</span></span> <span data-ttu-id="3a092-271">Wenn die Beispielanwendung keine Wiederherstellung nach einem zu langen Fehler (d. h. 1 Sekunde oder 60 vsyncs auf dem 60Hz-Monitor) durchgeführt werden kann, überspringen Sie die periodische Animation, und setzen Sie die vorhandene hilfswarteschlange zurück.</span><span class="sxs-lookup"><span data-stu-id="3a092-271">If the sample application cannot recover from a glitch that is too long (that is say, 1 second, or 60 vsyncs on 60Hz monitor), jump over the intermittent animation and reset the Present helper queue.</span></span>


```C++
VOID Render()
{
    g_pd3dDevice->Clear(0, NULL, D3DCLEAR_TARGET, D3DCOLOR_XRGB(0, 0, 0), 1.0f, 0);

    g_pd3dDevice->BeginScene();

    // Compute new animation parameters for time and frame based animations

    // Time-based is a difference between base and current SyncRefreshCount
    g_aTimeBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_LastSyncRefreshCount - g_SyncRefreshCount;
    // Frame-based is incrementing frame value
    g_aFrameBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_iFrameNumber;

    RenderBlurredMesh(TRUE);    // Time-based
    RenderBlurredMesh(FALSE);   // Frame-based

    g_iBlurHistoryCounter = (g_iBlurHistoryCounter + 1) % BLUR_FRAMES;

    DrawText();

    g_pd3dDevice->EndScene();

    // Performs glitch recovery if glitch was detected
    if (g_bGlitchRecovery && (g_iImmediates > 0))
    {
        // If we have present immediates queued as a result of glitch detected, issue forceimmediate Presents for glitch recovery 
        g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_FORCEIMMEDIATE);
        g_iImmediates--;
        g_iShowingGlitchRecovery = MESSAGE_SHOW;
    }
    // Otherwise, Present normally
    else
    {
        g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, 0);
    }

    // Add to helper Present queue: PresentID + expected present refresh count of last submitted Present
    UINT PresentCount;
    g_pd3dSwapChain->GetLastPresentCount(&PresentCount);
    g_Queue.QueueFrame(PresentCount, g_TargetRefreshCount);
    
    // QueueDelay specifies # Present calls to be processed before another glitch recovery attempt
    if (g_iQueueDelay > 0)
    {
        g_iQueueDelay--;
    }

    if (g_bGlitchRecovery)
    {
        // Additional DONOTFLIP presents for frame conversions, which basically follows the same logic, but without rendering
        for (DWORD i = 0; i < g_iDoNotFlipNum; i++)
        {
            if (g_TargetRefreshCount != -1)
            {
                g_TargetRefreshCount++;
                g_iFrameNumber++;
                g_aTimeBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_LastSyncRefreshCount - g_SyncRefreshCount;
                g_aFrameBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_iFrameNumber;
                g_iBlurHistoryCounter = (g_iBlurHistoryCounter + 1) % BLUR_FRAMES;
            }
            
            if (g_iImmediates > 0)
            {
                g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_FORCEIMMEDIATE | D3DPRESENT_DONOTFLIP);
                g_iImmediates--;
            }
            else
            {
                g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_DONOTFLIP);
            }
            UINT PresentCount;
            g_pd3dSwapChain->GetLastPresentCount(&PresentCount);
            g_Queue.QueueFrame(PresentCount, g_TargetRefreshCount);

            if (g_iQueueDelay > 0)
            {
                g_iQueueDelay--;
            }
        }
    }

    // Check Present Stats info for glitch detection 
    D3DPRESENTSTATS PresentStats;

    // Obtain present statistics information for successfully displayed presents
    HRESULT hr = g_pd3dSwapChain->GetPresentStats(&PresentStats);

    if (SUCCEEDED(hr))
    {
        // Time-based update
        g_LastSyncRefreshCount = PresentStats.SyncRefreshCount;
        if ((g_SyncRefreshCount == -1) && (PresentStats.PresentCount != 0))
        {
            // First time SyncRefreshCount is reported, use it as base
            g_SyncRefreshCount = PresentStats.SyncRefreshCount;
        }

        // Fetch frame from the queue...
        UINT TargetRefresh = g_Queue.DequeueFrame(PresentStats.PresentCount);

        // If PresentStats returned a really old frame that we no longer have in the queue, just don't do any glitch detection
        if (TargetRefresh == FRAME_NOT_FOUND)
            return;

        if (g_TargetRefreshCount == -1)
        {
            // This is first time issued frame is confirmed by present stats, so fill target refresh count for all frames in the queue
            g_TargetRefreshCount = g_Queue.FillRefreshCounts(PresentStats.PresentCount, g_SyncRefreshCount);
        } 
        else
        {
            g_TargetRefreshCount++;
            g_iFrameNumber++;

            // To determine whether we're glitching, see if our estimated refresh count is confirmed
            // if the frame is displayed later than the expected vsync count
            if (TargetRefresh < PresentStats.PresentRefreshCount)
            {
                // then, glitch is detected!

                // If glitch is too big, don't bother recovering from it, just jump animation
                if ((PresentStats.PresentRefreshCount - TargetRefresh) > GLITCH_RECOVERY_LIMIT)
                {
                    g_iStartFrame += PresentStats.SyncRefreshCount - g_SyncRefreshCount;
                    ResetAnimation();
                    if (g_bGlitchRecovery)
                        g_iGlitchesInaRow++;    
                } 
                // Otherwise, compute number of immediate presents to recover from it -- if we?re not still trying to recover from another glitch
                else if (g_iQueueDelay == 0)
                {
                      // skip frames to catch up to expected refresh count
                    g_iImmediates = PresentStats.PresentRefreshCount - TargetRefresh;
                    // QueueDelay specifies # Present calls before another glitch recovery 
                    g_iQueueDelay = g_iImmediates + QUEUE_SIZE;
                    if (g_bGlitchRecovery)
                        g_iGlitchesInaRow++;
                }
            }
            else
            {
                // No glitch, reset glitch count
                g_iGlitchesInaRow = 0;
            }
        }
    }
    else if (hr == D3DERR_PRESENT_STATISTICS_DISJOINT)
    {
        // D3DERR_PRESENT_STATISTICS_DISJOINT means measurements should be started from the scratch (could be caused by mode change or DWM on/off transition)
        ResetAnimation();
    }

    // If we got too many glitches in a row, reduce framerate conversion factor (that is, render less frames)
    if (g_iGlitchesInaRow == FRAMECONVERSION_GLITCH_LIMIT)
    {
        if (g_iDoNotFlipNum < FRAMECONVERSION_LIMIT)
        {
            g_iDoNotFlipNum++;
        }
        g_iGlitchesInaRow = 0;
        g_iShowingDoNotFlipBump = MESSAGE_SHOW;
    }
}
```



<span data-ttu-id="3a092-272">**Beispielszenario**</span><span class="sxs-lookup"><span data-stu-id="3a092-272">**Sample scenario**</span></span>

-   <span data-ttu-id="3a092-273">In der folgenden Abbildung ist eine Anwendung mit einer backpufferanzahl von 4 dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3a092-273">The following illustration shows an application with backbuffer count of 4.</span></span> <span data-ttu-id="3a092-274">Die tatsächliche Warteschlangen Länge ist daher 5.</span><span class="sxs-lookup"><span data-stu-id="3a092-274">The actual Present queue length is therefore 5.</span></span>

    ![Abbildung der von einem applicas gerenderten Frames und der aktuellen Warteschlange](images/sample-scenario.png)

    <span data-ttu-id="3a092-276">Frame A ist darauf ausgerichtet, bei der Synchronisierungs Intervall Anzahl von 1 auf den Bildschirm zu wechseln, aber es wurde erkannt, dass die Synchronisierungs Intervall Anzahl von 4 angezeigt wurde.</span><span class="sxs-lookup"><span data-stu-id="3a092-276">Frame A is targeted to go on screen on sync interval count of 1 but was detected that it was shown on sync interval count of 4.</span></span> <span data-ttu-id="3a092-277">Daher ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="3a092-277">Therefore a glitch has occurred.</span></span> <span data-ttu-id="3a092-278">Nachfolgende 3 Rahmen werden mit D3DPRESENT \_ Interval \_ forceimvermittler präsentiert.</span><span class="sxs-lookup"><span data-stu-id="3a092-278">Subsequent 3 frames are presented with D3DPRESENT\_INTERVAL\_FORCEIMMEDIATE.</span></span> <span data-ttu-id="3a092-279">Der Fehler muss insgesamt acht vorhandene Aufrufe annehmen, bevor er wieder hergestellt wird. der nächste Frame wird gemäß der angegebenen Synchronisierungs Intervall Anzahl angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3a092-279">The glitch should take a total of 8 Present calls before it is recovered - the next frame will be shown as per its targeted sync interval count.</span></span>

### <a name="summary-of-programming-recommendations-for-frame-synchronization"></a><span data-ttu-id="3a092-280">Zusammenfassung der Programmier Empfehlungen für die Frame-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="3a092-280">Summary of Programming Recommendations for Frame Synchronization</span></span>

-   <span data-ttu-id="3a092-281">Erstellen Sie eine Sicherungsliste aller lastpresentcount-IDs (abgerufen über [**getlastpresentcount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount)) und der zugeordneten geschätzten presenterfrischendes-Anzahl aller übermittelten über Mitt lungs-IDs.</span><span class="sxs-lookup"><span data-stu-id="3a092-281">Create a backup list of all the LastPresentCount IDs (obtained via [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount)) and associated estimated PresentRefreshCount of all the Presents submitted.</span></span>
    > [!Note]  
    > <span data-ttu-id="3a092-282">Wenn die Anwendung einen [**presentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) mit D3DPRESENT \_ donotflip aufruft, wird der [**getpresentstatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) -Aufruf erfolgreich ausgeführt, aber es wird keine aktualisierte [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) -Struktur zurückgegeben, wenn sich die Anwendung im Fenstermodus befindet.</span><span class="sxs-lookup"><span data-stu-id="3a092-282">When the application calls [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) with D3DPRESENT\_DONOTFLIP, the [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) call succeeds but does not return an updated [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure when the application is in windowed mode.</span></span>

     

-   <span data-ttu-id="3a092-283">Rufen Sie [**getpresentstatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) auf, um die tatsächliche presentaktualzahl zu erhalten, die den einzelnen vorhandenen IDs der angezeigten Frames zugeordnet ist, um sicherzustellen, dass die Anwendung Fehler Rückgaben aus dem-Befehl behandelt.</span><span class="sxs-lookup"><span data-stu-id="3a092-283">Call [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) to obtain the actual PresentRefreshCount associated with each Present ID of frames shown, to make sure that the application handles failure returns from the call.</span></span>
-   <span data-ttu-id="3a092-284">Wenn die tatsächliche presentaktuellem Anzahl nach der geschätzten Anzahl der Present-Werte liegt, wird eine Störung erkannt.</span><span class="sxs-lookup"><span data-stu-id="3a092-284">If actual PresentRefreshCount is later than estimated PresentRefreshCount, a glitch is detected.</span></span> <span data-ttu-id="3a092-285">Kompensieren Sie durch das Übermitteln von zurückliegenden Frames mit D3DPRESENT \_ forceimvermittler.</span><span class="sxs-lookup"><span data-stu-id="3a092-285">Compensate by submitting lagging frames' Present with D3DPRESENT\_FORCEIMMEDIATE.</span></span>
-   <span data-ttu-id="3a092-286">Wenn ein Frame in der aktuellen Warteschlange spät angezeigt wird, werden alle nachfolgenden Frames in der Warteschlange später angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3a092-286">When one frame is presented late in the Present queue, all subsequent queued frames will be presented late.</span></span> <span data-ttu-id="3a092-287">D3DPRESENT \_ forceimvermittlung korrigiert nur den nächsten Frame, der nach allen in der Warteschlange befindlichen Frames angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3a092-287">D3DPRESENT\_FORCEIMMEDIATE will correct only the next frame to be presented after all the queued frames.</span></span> <span data-ttu-id="3a092-288">Daher sollte die vorhandene Warteschlange oder die backpufferanzahl nicht zu lang sein. Daher gibt es weniger Frame-gleitungen, mit denen Sie sich abfangen können.</span><span class="sxs-lookup"><span data-stu-id="3a092-288">Therefore, the Present queue or backbuffer count should not be too long -- so there are less frame glitches to catch up with.</span></span> <span data-ttu-id="3a092-289">Die optimale Puffer Anzahl ist 2 bis 4.</span><span class="sxs-lookup"><span data-stu-id="3a092-289">The optimal backbuffer count is 2 to 4.</span></span>
-   <span data-ttu-id="3a092-290">Wenn die geschätzte presentaktuellem Anzahl nach der tatsächlichen presenterfrischen-Anzahl liegt, ist möglicherweise eine DWM-Drosselung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="3a092-290">If estimated PresentRefreshCount is later than the actual PresentRefreshCount, DWM throttling might have occurred.</span></span> <span data-ttu-id="3a092-291">Folgende Lösungen sind möglich:</span><span class="sxs-lookup"><span data-stu-id="3a092-291">The following solutions are possible:</span></span>

    -   <span data-ttu-id="3a092-292">Reduzieren der aktuellen Warteschlangen Länge</span><span class="sxs-lookup"><span data-stu-id="3a092-292">reducing Present queue length</span></span>
    -   <span data-ttu-id="3a092-293">Reduzieren der GPU-Speicheranforderungen auf andere Weise, außer der Verringerung der aktuellen Warteschlangen Länge (d. h. der absteigenden Qualität, der Entfernung von Effekten usw.)</span><span class="sxs-lookup"><span data-stu-id="3a092-293">reducing GPU memory requirements with any other means besides reducing Present Queue length (that is, decreasing quality, removing effects, and so on)</span></span>
    -   <span data-ttu-id="3a092-294">Angeben von [**dwmenablemmcss**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenablemmcss) zum Verhindern der DWM-Drosselung im allgemeinen</span><span class="sxs-lookup"><span data-stu-id="3a092-294">specifying [**DwmEnableMMCSS**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenablemmcss) to prevent DWM throttling in general</span></span>

-   <span data-ttu-id="3a092-295">Überprüfen Sie die Anwendungs Anzeige Funktionalität und die Leistung von Frame Statistiken in den folgenden Szenarien:</span><span class="sxs-lookup"><span data-stu-id="3a092-295">Verify application display functionality and frame statistics performance in the following scenarios:</span></span>

    -   <span data-ttu-id="3a092-296">mit DWM ein-und ausschalten</span><span class="sxs-lookup"><span data-stu-id="3a092-296">with DWM on and off</span></span>
    -   <span data-ttu-id="3a092-297">Vollbildmodus für exklusive und Fenster</span><span class="sxs-lookup"><span data-stu-id="3a092-297">fullscreen exclusive and windowed modes</span></span>
    -   <span data-ttu-id="3a092-298">geringere Funktions Hardware</span><span class="sxs-lookup"><span data-stu-id="3a092-298">lower capability hardware</span></span>

-   <span data-ttu-id="3a092-299">Wenn Anwendungen eine große Anzahl von glitscherten Frames mit D3DPRESENT \_ forceimvermittlung nicht wiederherstellen können, können Sie möglicherweise die folgenden Vorgänge ausführen:</span><span class="sxs-lookup"><span data-stu-id="3a092-299">When applications cannot recover from large numbers of glitched frames with D3DPRESENT\_FORCEIMMEDIATE Present, they can potentially perform the following operations:</span></span>

    -   <span data-ttu-id="3a092-300">reduzieren Sie die CPU-und GPU-Nutzung durch Rendering mit weniger Arbeitsauslastung.</span><span class="sxs-lookup"><span data-stu-id="3a092-300">reduce CPU and GPU usage by rendering with less workload.</span></span>
    -   <span data-ttu-id="3a092-301">im Fall von Video Decodierung sollten Sie schneller decodieren, indem Sie Qualität und somit CPU-und GPU-Auslastung verringern.</span><span class="sxs-lookup"><span data-stu-id="3a092-301">in the case of video decode, decode faster by reducing quality and, therefore, CPU and GPU usage.</span></span>

## <a name="conclusion-about-direct3d-9ex-improvements"></a><span data-ttu-id="3a092-302">Schlussfolgerung zu Direct3D 9Ex-Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="3a092-302">Conclusion about Direct3D 9Ex Improvements</span></span>

<span data-ttu-id="3a092-303">Unter Windows 7 können Anwendungen, die während der Präsentation Video-oder Messgeräte Frameraten anzeigen, das Kippen von Modellen beschließen.</span><span class="sxs-lookup"><span data-stu-id="3a092-303">On Windows 7, applications that display video or gauge frame rate during presentation can opt into Flip Model.</span></span> <span data-ttu-id="3a092-304">Die aktuellen Verbesserungen der Statistik, die dem Flip-Modell zugeordnet sind Direct3D 9Ex können Anwendungen profitieren, die die Präsentation pro Frame-Rate synchronisieren, mit Echtzeitfeedback für die Erkennung und Wiederherstellung von Daten.</span><span class="sxs-lookup"><span data-stu-id="3a092-304">The present statistics improvements that are associated with Flip Model Direct3D 9Ex can benefit applications that synchronize presentation per frame rate, with real time feedback for glitch detection and recovery.</span></span> <span data-ttu-id="3a092-305">Entwickler, die das Direct3D 9Ex-Flip-Modell übernehmen, sollten das Ziel eines separaten HWND von GDI-Inhalten und der Frameraten Synchronisierung berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="3a092-305">Developers that adopt the Direct3D 9Ex Flip Model should take targeting a separate HWND from GDI content and frame rate synchronization into account.</span></span> <span data-ttu-id="3a092-306">Weitere Informationen finden Sie in diesem Thema und in der MSDN-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="3a092-306">Refer to details in this topic, and MSDN documentation.</span></span> <span data-ttu-id="3a092-307">Weitere Dokumentationen finden Sie unter [DirectX Developer Center auf MSDN](/previous-versions/windows/apps/hh452744(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="3a092-307">For additional documentation, see [DirectX Developer Center on MSDN](/previous-versions/windows/apps/hh452744(v=win.10)).</span></span>

## <a name="call-to-action"></a><span data-ttu-id="3a092-308">Call-to-Action</span><span class="sxs-lookup"><span data-stu-id="3a092-308">Call to Action</span></span>

<span data-ttu-id="3a092-309">Wir empfehlen Ihnen, das Direct3D 9Ex-Flip-Modell und seine aktuellen Statistiken unter Windows 7 zu verwenden, wenn Sie Anwendungen erstellen, die versuchen, die Präsentations Frame Rate zu synchronisieren oder nach Anzeige Abrufe wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="3a092-309">We encourage you to use Direct3D 9Ex Flip Model and its present statistics on Windows 7 when you create applications that attempt to synchronize presentation frame rate or recover from display glitches.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a092-310">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3a092-310">Related topics</span></span>

<span data-ttu-id="3a092-311">[DirectX Developer Center auf MSDN](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="3a092-311">[DirectX Developer Center on MSDN](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>
</dt> </dl>