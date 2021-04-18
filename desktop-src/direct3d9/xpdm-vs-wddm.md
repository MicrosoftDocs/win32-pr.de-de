---
description: Die Direct3D 9-API funktioniert abhängig vom installierten Betriebssystem entweder mit dem Windows XP-Anzeigetreiber Modell (XPDM) oder dem Windows Vista-Anzeigetreiber Modell (WDDM).
ms.assetid: b552c822-aa01-4f1d-a0a6-1411ab006e7b
title: XPDM im Vergleich zu WDDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccdf4bba28b53959d8e86d8928c786db3b1d0c7f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343932"
---
# <a name="xpdm-vs-wddm"></a><span data-ttu-id="8042e-103">XPDM im Vergleich zu WDDM</span><span class="sxs-lookup"><span data-stu-id="8042e-103">XPDM vs. WDDM</span></span>

<span data-ttu-id="8042e-104">Die Direct3D 9-API funktioniert abhängig vom installierten Betriebssystem entweder mit dem Windows XP-Anzeigetreiber Modell (XPDM) oder dem Windows Vista-Anzeigetreiber Modell (WDDM).</span><span class="sxs-lookup"><span data-stu-id="8042e-104">The Direct3D 9 API operates on either the Windows XP display driver model (XPDM) or the Windows Vista display driver model (WDDM), depending on the operating system installed.</span></span> <span data-ttu-id="8042e-105">Es gibt einige Unterschiede in der Art und Weise, wie sich die Direct3D-API auf die beiden Treiber Modelle verhält.</span><span class="sxs-lookup"><span data-stu-id="8042e-105">There are some differences in the way the Direct3D API behaves on the two driver models.</span></span>

-   [<span data-ttu-id="8042e-106">Sicherer Desktop</span><span class="sxs-lookup"><span data-stu-id="8042e-106">Secure Desktop</span></span>](#secure-desktop)
-   [<span data-ttu-id="8042e-107">Remotedesktop</span><span class="sxs-lookup"><span data-stu-id="8042e-107">Remote Desktop</span></span>](#remote-desktop)
-   [<span data-ttu-id="8042e-108">Windows-Dienst</span><span class="sxs-lookup"><span data-stu-id="8042e-108">Windows Service</span></span>](#windows-service)
-   [<span data-ttu-id="8042e-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8042e-109">Related topics</span></span>](#related-topics)

## <a name="secure-desktop"></a><span data-ttu-id="8042e-110">Sicherer Desktop</span><span class="sxs-lookup"><span data-stu-id="8042e-110">Secure Desktop</span></span>

<span data-ttu-id="8042e-111">Der sichere Desktop ist aktiv, wenn eine der folgenden Aktionen auftritt: der Benutzer sperrt den Desktop (Windows + L), der Bildschirmschoner wird aktiviert (wenn kein Benutzer angemeldet ist) oder standardmäßig, wenn die Benutzerkontensteuerung eine Eingabeaufforderung anzeigt.</span><span class="sxs-lookup"><span data-stu-id="8042e-111">The secure desktop is active whenever any of the following occur: the user locks their desktop (Windows+L), the screen saver activates (when no user is logged in), or by default when User Account Control presents a prompt.</span></span> <span data-ttu-id="8042e-112">Wenn der sichere Desktop aktiv ist, kann nicht auf das HAL-Gerät zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="8042e-112">When the secure desktop is active, the HAL device is not accessible.</span></span>



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8042e-113">Unterschiede zwischen XPDM und WDDM:</span><span class="sxs-lookup"><span data-stu-id="8042e-113">Differences between XPDM and WDDM:</span></span><br/> <span data-ttu-id="8042e-114">Beim Versuch, ein von Direct3D9 HAL-Gerät zu erstellen, tritt ein Fehler auf (mit **D3DERR \_ nicht \_ verfügbar**), und jedes vorhandene Direct3D 9-Gerät weist auf einen verlorenen Geräte Rückgabecode hin.</span><span class="sxs-lookup"><span data-stu-id="8042e-114">Attempting to create a Direct3D9 HAL device will fail (with **D3DERR\_NOT\_AVAILABLE**), and any existing Direct3D 9 device will indicate a lost device return code on Present.</span></span><br/> <span data-ttu-id="8042e-115">Die APIs Direct3D9Ex und Direct3D 10 können ein Gerät erfolgreich erstellen, während der sichere Desktop aktiv ist, und alle Aufrufe an Present ([**IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) oder DXGI) geben einen Statuscode zurück, der anzeigt, dass der Desktop zurzeit nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="8042e-115">Direct3D9Ex and Direct3D 10 APIs can successfully create a device while the secure desktop is active, and any calls to Present ([**IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) or DXGI) will return a status code indicating the desktop is currently unavailable.</span></span><br/> |



 

## <a name="remote-desktop"></a><span data-ttu-id="8042e-116">Remotedesktop</span><span class="sxs-lookup"><span data-stu-id="8042e-116">Remote Desktop</span></span>

<span data-ttu-id="8042e-117">Wenn ein Remote Desktop aktiv ist, wird die Anzeige vom Computer mit dem hostingcomputer behandelt, der Informationen über das Netzwerk sendet.</span><span class="sxs-lookup"><span data-stu-id="8042e-117">When a remote desktop is active, the display is handled by the viewing machine with the hosting machine sending information via the network.</span></span>



|                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8042e-118">Unterschiede zwischen XPDM und WDDM:</span><span class="sxs-lookup"><span data-stu-id="8042e-118">Differences between XPDM and WDDM:</span></span><br/> <span data-ttu-id="8042e-119">Bei XPDM tritt bei allen versuchen, ein Direct3D 9-Gerät auf einem Remote Desktop zu erstellen, ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="8042e-119">On XPDM, all attempts to create a Direct3D 9 device on a remote desktop will fail.</span></span><br/> <span data-ttu-id="8042e-120">Auf WDDM unterstützt Remote Desktop das Erstellen eines HAL-Geräts über eine Remote Desktop Sitzung.</span><span class="sxs-lookup"><span data-stu-id="8042e-120">On WDDM, remote desktop does support creating a HAL device over a remote desktop session.</span></span><br/> |



 

## <a name="windows-service"></a><span data-ttu-id="8042e-121">Windows-Dienst</span><span class="sxs-lookup"><span data-stu-id="8042e-121">Windows Service</span></span>

<span data-ttu-id="8042e-122">Ein Windows-Dienst ist ein Prozess, der im Hintergrund ausgeführt wird, der vom Dienststeuerungs-Manager (Service Control Manager, SCM) gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="8042e-122">A Windows service is a process that runs in the background, controlled by the service-control manager (SCM).</span></span> <span data-ttu-id="8042e-123">Ein Dienst wird unabhängig vom aktiven Desktop ausgeführt und verfügt daher über eingeschränkte Möglichkeiten zur Interaktion mit Benutzern.</span><span class="sxs-lookup"><span data-stu-id="8042e-123">A service runs independent of the active desktop and therefore has limited ability to interact with users.</span></span>



|                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8042e-124">Unterschiede zwischen XPDM und WDDM:</span><span class="sxs-lookup"><span data-stu-id="8042e-124">Differences between XPDM and WDDM:</span></span><br/> <span data-ttu-id="8042e-125">Bei WDDM stellt die Isolation der Sitzung 0 sicher, dass ein Dienst nicht als Sicherheitsmaßnahme auf einen Benutzer Desktop zugreifen kann. aus diesem Grund ist ein Direct3D 9 HAL-Gerät nie über einen Windows-Dienst verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8042e-125">On WDDM, Session 0 Isolation ensures that a service does not have access to any user desktop as a security measure, therefore, a Direct3D 9 HAL device is never available from a Windows service.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="8042e-126">Sie können Direct3D 9 nicht in einem Windows-Dienst verwenden.</span><span class="sxs-lookup"><span data-stu-id="8042e-126">You cannot use Direct3D 9 in a Windows service.</span></span> <span data-ttu-id="8042e-127">Weitere Informationen finden Sie im [Microsoft Support-Artikel 978635](https://support.microsoft.com/kb/978635).</span><span class="sxs-lookup"><span data-stu-id="8042e-127">For more information, see [Microsoft support article 978635](https://support.microsoft.com/kb/978635).</span></span>

 


<span data-ttu-id="8042e-128">In der folgenden Tabelle werden die hier aufgeführten Unterschiede zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="8042e-128">The following table summarizes the differences listed here.</span></span>



|                 | <span data-ttu-id="8042e-129">XPDM</span><span class="sxs-lookup"><span data-stu-id="8042e-129">XPDM</span></span> | <span data-ttu-id="8042e-130">WDDM (von Direct3D9)</span><span class="sxs-lookup"><span data-stu-id="8042e-130">WDDM (Direct3D9)</span></span> | <span data-ttu-id="8042e-131">WDDM (Direct3D9Ex/Direct3D10)</span><span class="sxs-lookup"><span data-stu-id="8042e-131">WDDM(Direct3D9Ex/Direct3D10)</span></span> |
|-----------------|------|------------------|------------------------------|
| <span data-ttu-id="8042e-132">Sicherer Desktop</span><span class="sxs-lookup"><span data-stu-id="8042e-132">Secure Desktop</span></span>  |      |                  |                              |
| <span data-ttu-id="8042e-133">NullRef</span><span class="sxs-lookup"><span data-stu-id="8042e-133">NULLREF</span></span>         | <span data-ttu-id="8042e-134">Ja</span><span class="sxs-lookup"><span data-stu-id="8042e-134">Yes</span></span>  | <span data-ttu-id="8042e-135">Ja</span><span class="sxs-lookup"><span data-stu-id="8042e-135">Yes</span></span>              | <span data-ttu-id="8042e-136">Ja</span><span class="sxs-lookup"><span data-stu-id="8042e-136">Yes</span></span>                          |
| <span data-ttu-id="8042e-137">Hale</span><span class="sxs-lookup"><span data-stu-id="8042e-137">HAL</span></span>             | <span data-ttu-id="8042e-138">Nein</span><span class="sxs-lookup"><span data-stu-id="8042e-138">No</span></span>   | <span data-ttu-id="8042e-139">Nein</span><span class="sxs-lookup"><span data-stu-id="8042e-139">No</span></span>               | <span data-ttu-id="8042e-140">Ja</span><span class="sxs-lookup"><span data-stu-id="8042e-140">Yes</span></span>                          |
| <span data-ttu-id="8042e-141">REF</span><span class="sxs-lookup"><span data-stu-id="8042e-141">REF</span></span>             | <span data-ttu-id="8042e-142">Ja</span><span class="sxs-lookup"><span data-stu-id="8042e-142">Yes</span></span>  | <span data-ttu-id="8042e-143">Ja</span><span class="sxs-lookup"><span data-stu-id="8042e-143">Yes</span></span>              | <span data-ttu-id="8042e-144">Ja</span><span class="sxs-lookup"><span data-stu-id="8042e-144">Yes</span></span>                          |
| <span data-ttu-id="8042e-145">Remotedesktop</span><span class="sxs-lookup"><span data-stu-id="8042e-145">Remote Desktop</span></span>  |      |                  |                              |
| <span data-ttu-id="8042e-146">NullRef</span><span class="sxs-lookup"><span data-stu-id="8042e-146">NULLREF</span></span>         | <span data-ttu-id="8042e-147">Nein</span><span class="sxs-lookup"><span data-stu-id="8042e-147">No</span></span>   | <span data-ttu-id="8042e-148">Ja</span><span class="sxs-lookup"><span data-stu-id="8042e-148">Yes</span></span>              | <span data-ttu-id="8042e-149">Ja</span><span class="sxs-lookup"><span data-stu-id="8042e-149">Yes</span></span>                          |
| <span data-ttu-id="8042e-150">Hale</span><span class="sxs-lookup"><span data-stu-id="8042e-150">HAL</span></span>             | <span data-ttu-id="8042e-151">Nein</span><span class="sxs-lookup"><span data-stu-id="8042e-151">No</span></span>   | <span data-ttu-id="8042e-152">Ja</span><span class="sxs-lookup"><span data-stu-id="8042e-152">Yes</span></span>              | <span data-ttu-id="8042e-153">Ja</span><span class="sxs-lookup"><span data-stu-id="8042e-153">Yes</span></span>                          |
| <span data-ttu-id="8042e-154">REF</span><span class="sxs-lookup"><span data-stu-id="8042e-154">REF</span></span>             | <span data-ttu-id="8042e-155">Ja</span><span class="sxs-lookup"><span data-stu-id="8042e-155">Yes</span></span>  | <span data-ttu-id="8042e-156">Ja</span><span class="sxs-lookup"><span data-stu-id="8042e-156">Yes</span></span>              | <span data-ttu-id="8042e-157">Ja</span><span class="sxs-lookup"><span data-stu-id="8042e-157">Yes</span></span>                          |
| <span data-ttu-id="8042e-158">Windows-Dienst</span><span class="sxs-lookup"><span data-stu-id="8042e-158">Windows Service</span></span> |      |                  |                              |
| <span data-ttu-id="8042e-159">NullRef</span><span class="sxs-lookup"><span data-stu-id="8042e-159">NULLREF</span></span>         | <span data-ttu-id="8042e-160">Nein</span><span class="sxs-lookup"><span data-stu-id="8042e-160">No</span></span>   | <span data-ttu-id="8042e-161">Nein</span><span class="sxs-lookup"><span data-stu-id="8042e-161">No</span></span>               | <span data-ttu-id="8042e-162">Nein</span><span class="sxs-lookup"><span data-stu-id="8042e-162">No</span></span>                           |
| <span data-ttu-id="8042e-163">Hale</span><span class="sxs-lookup"><span data-stu-id="8042e-163">HAL</span></span>             | <span data-ttu-id="8042e-164">Nein</span><span class="sxs-lookup"><span data-stu-id="8042e-164">No</span></span>   | <span data-ttu-id="8042e-165">Nein</span><span class="sxs-lookup"><span data-stu-id="8042e-165">No</span></span>               | <span data-ttu-id="8042e-166">Nein</span><span class="sxs-lookup"><span data-stu-id="8042e-166">No</span></span>                           |
| <span data-ttu-id="8042e-167">REF</span><span class="sxs-lookup"><span data-stu-id="8042e-167">REF</span></span>             | <span data-ttu-id="8042e-168">Nein</span><span class="sxs-lookup"><span data-stu-id="8042e-168">No</span></span>   | <span data-ttu-id="8042e-169">Nein</span><span class="sxs-lookup"><span data-stu-id="8042e-169">No</span></span>               | <span data-ttu-id="8042e-170">Nein</span><span class="sxs-lookup"><span data-stu-id="8042e-170">No</span></span>                           |
| <span data-ttu-id="8042e-171">WARP10</span><span class="sxs-lookup"><span data-stu-id="8042e-171">WARP10</span></span>          | <span data-ttu-id="8042e-172">–</span><span class="sxs-lookup"><span data-stu-id="8042e-172">N/A</span></span>  | <span data-ttu-id="8042e-173">–</span><span class="sxs-lookup"><span data-stu-id="8042e-173">N/A</span></span>              | <span data-ttu-id="8042e-174">Ja</span><span class="sxs-lookup"><span data-stu-id="8042e-174">Yes</span></span>                          |



 

<span data-ttu-id="8042e-175">Weitere Informationen zu XPDM, WDDM, Direct3D9Ex und Direct3D 10 finden Sie unter [Grafik-APIs in Windows](../direct3darticles/graphics-apis-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="8042e-175">For more information about XPDM, WDDM, Direct3D9Ex, and Direct3D 10, see [Graphics APIs in Windows](../direct3darticles/graphics-apis-in-windows-vista.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8042e-176">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8042e-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8042e-177">Direct3D-Geräte</span><span class="sxs-lookup"><span data-stu-id="8042e-177">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
