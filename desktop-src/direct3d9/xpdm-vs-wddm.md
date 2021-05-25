---
description: Die Direct3D 9-API funktioniert abhängig vom installierten Betriebssystem entweder mit dem Windows XP-Anzeigetreibermodell (XPDM) oder dem Windows Vista-Anzeigetreibermodell (Windows Vista Display Driver Model, WDDM).
ms.assetid: b552c822-aa01-4f1d-a0a6-1411ab006e7b
title: XPDM im Vergleich zu WDDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12c7d811850c953eb53c346b628363a2642dda9
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343535"
---
# <a name="xpdm-vs-wddm"></a><span data-ttu-id="408c7-103">XPDM im Vergleich zu WDDM</span><span class="sxs-lookup"><span data-stu-id="408c7-103">XPDM vs. WDDM</span></span>

<span data-ttu-id="408c7-104">Die Direct3D 9-API funktioniert abhängig vom installierten Betriebssystem entweder mit dem Windows XP-Anzeigetreibermodell (XPDM) oder dem Windows Vista-Anzeigetreibermodell (Windows Vista Display Driver Model, WDDM).</span><span class="sxs-lookup"><span data-stu-id="408c7-104">The Direct3D 9 API operates on either the Windows XP display driver model (XPDM) or the Windows Vista display driver model (WDDM), depending on the operating system installed.</span></span> <span data-ttu-id="408c7-105">Es gibt einige Unterschiede im Verhalten der Direct3D-API bei den beiden Treibermodellen.</span><span class="sxs-lookup"><span data-stu-id="408c7-105">There are some differences in the way the Direct3D API behaves on the two driver models.</span></span>

-   [<span data-ttu-id="408c7-106">Sicherer Desktop</span><span class="sxs-lookup"><span data-stu-id="408c7-106">Secure Desktop</span></span>](#secure-desktop)
-   [<span data-ttu-id="408c7-107">Remotedesktop</span><span class="sxs-lookup"><span data-stu-id="408c7-107">Remote Desktop</span></span>](#remote-desktop)
-   [<span data-ttu-id="408c7-108">Windows-Dienst</span><span class="sxs-lookup"><span data-stu-id="408c7-108">Windows Service</span></span>](#windows-service)
-   [<span data-ttu-id="408c7-109">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="408c7-109">Related topics</span></span>](#related-topics)

## <a name="secure-desktop"></a><span data-ttu-id="408c7-110">Sicherer Desktop</span><span class="sxs-lookup"><span data-stu-id="408c7-110">Secure Desktop</span></span>

<span data-ttu-id="408c7-111">Der sichere Desktop ist immer dann aktiv, wenn einer der folgenden Ereignisse auftritt: Der Benutzer sperrt seinen Desktop (Windows+L), der Bildschirmschoner wird aktiviert (wenn kein Benutzer angemeldet ist) oder standardmäßig, wenn die Benutzerkontensteuerung eine Eingabeaufforderung einleiten.</span><span class="sxs-lookup"><span data-stu-id="408c7-111">The secure desktop is active whenever any of the following occur: the user locks their desktop (Windows+L), the screen saver activates (when no user is logged in), or by default when User Account Control presents a prompt.</span></span> <span data-ttu-id="408c7-112">Wenn der sichere Desktop aktiv ist, ist der Zugriff auf das HALOGEN-Gerät nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="408c7-112">When the secure desktop is active, the HAL device is not accessible.</span></span>

<span data-ttu-id="408c7-113">Unterschiede zwischen XPDM und WDDM:</span><span class="sxs-lookup"><span data-stu-id="408c7-113">Differences between XPDM and WDDM:</span></span>

- <span data-ttu-id="408c7-114">Beim Versuch, ein Direct3D9-GERÄT zu erstellen, ist ein Fehler **(D3DERR \_ \_ NICHT** VERFÜGBAR) möglich, und alle vorhandenen Direct3D 9-Geräte weisen auf einen verloren gegangenen Geräte-Rückgabecode auf Present hin.</span><span class="sxs-lookup"><span data-stu-id="408c7-114">Attempting to create a Direct3D9 HAL device will fail (with **D3DERR\_NOT\_AVAILABLE**), and any existing Direct3D 9 device will indicate a lost device return code on Present.</span></span>

- <span data-ttu-id="408c7-115">Direct3D9Ex- und Direct3D 10-APIs können erfolgreich ein Gerät erstellen, während der sichere Desktop aktiv ist, und alle Aufrufe von Present ([**IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) oder DXGI) geben einen Statuscode zurück, der angibt, dass der Desktop derzeit nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="408c7-115">Direct3D9Ex and Direct3D 10 APIs can successfully create a device while the secure desktop is active, and any calls to Present ([**IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) or DXGI) will return a status code indicating the desktop is currently unavailable.</span></span>



 

## <a name="remote-desktop"></a><span data-ttu-id="408c7-116">Remotedesktop</span><span class="sxs-lookup"><span data-stu-id="408c7-116">Remote Desktop</span></span>

<span data-ttu-id="408c7-117">Wenn ein Remotedesktop aktiv ist, wird die Anzeige vom Anzeigecomputer verarbeitet, während der Hostcomputer Informationen über das Netzwerk sendet.</span><span class="sxs-lookup"><span data-stu-id="408c7-117">When a remote desktop is active, the display is handled by the viewing machine with the hosting machine sending information via the network.</span></span>

<span data-ttu-id="408c7-118">Unterschiede zwischen XPDM und WDDM:</span><span class="sxs-lookup"><span data-stu-id="408c7-118">Differences between XPDM and WDDM:</span></span>

- <span data-ttu-id="408c7-119">Unter XPDM sind alle Versuche, ein Direct3D 9-Gerät auf einem Remotedesktop zu erstellen, fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="408c7-119">On XPDM, all attempts to create a Direct3D 9 device on a remote desktop will fail.</span></span>

- <span data-ttu-id="408c7-120">Auf WDDM unterstützt Remotedesktop das Erstellen eines HALOGEN-Geräts über eine Remotedesktopsitzung.</span><span class="sxs-lookup"><span data-stu-id="408c7-120">On WDDM, remote desktop does support creating a HAL device over a remote desktop session.</span></span>



 

## <a name="windows-service"></a><span data-ttu-id="408c7-121">Windows-Dienst</span><span class="sxs-lookup"><span data-stu-id="408c7-121">Windows Service</span></span>

<span data-ttu-id="408c7-122">Ein Windows-Dienst ist ein Prozess, der im Hintergrund ausgeführt wird und vom Dienststeuerungs-Manager (Service Control Manager, SCM) gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="408c7-122">A Windows service is a process that runs in the background, controlled by the service-control manager (SCM).</span></span> <span data-ttu-id="408c7-123">Ein Dienst wird unabhängig vom aktiven Desktop ausgeführt und verfügt daher nur über eingeschränkte Möglichkeiten zur Interaktion mit Benutzern.</span><span class="sxs-lookup"><span data-stu-id="408c7-123">A service runs independent of the active desktop and therefore has limited ability to interact with users.</span></span>

<span data-ttu-id="408c7-124">Unterschiede zwischen XPDM und WDDM:</span><span class="sxs-lookup"><span data-stu-id="408c7-124">Differences between XPDM and WDDM:</span></span>

- <span data-ttu-id="408c7-125">Unter WDDM stellt die Sitzungs-0-Isolation sicher, dass ein Dienst keinen Zugriff auf Benutzerdesktops als Sicherheitsmaßnahme hat. Daher ist ein Direct3D 9-MSI-Gerät nie über einen Windows-Dienst verfügbar.</span><span class="sxs-lookup"><span data-stu-id="408c7-125">On WDDM, Session 0 Isolation ensures that a service does not have access to any user desktop as a security measure, therefore, a Direct3D 9 HAL device is never available from a Windows service.</span></span>



 

> [!Note]  
> <span data-ttu-id="408c7-126">Direct3D 9 kann nicht in einem Windows-Dienst verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="408c7-126">You cannot use Direct3D 9 in a Windows service.</span></span> <span data-ttu-id="408c7-127">Weitere Informationen finden Sie im [Microsoft-Supportartikel 978635.](https://support.microsoft.com/kb/978635)</span><span class="sxs-lookup"><span data-stu-id="408c7-127">For more information, see [Microsoft support article 978635](https://support.microsoft.com/kb/978635).</span></span>

 


<span data-ttu-id="408c7-128">In der folgenden Tabelle sind die hier aufgeführten Unterschiede zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="408c7-128">The following table summarizes the differences listed here.</span></span>



| <span data-ttu-id="408c7-129">Sicherer Desktop</span><span class="sxs-lookup"><span data-stu-id="408c7-129">Secure Desktop</span></span> | <span data-ttu-id="408c7-130">Xpdm</span><span class="sxs-lookup"><span data-stu-id="408c7-130">XPDM</span></span> | <span data-ttu-id="408c7-131">WDDM (Direct3D9)</span><span class="sxs-lookup"><span data-stu-id="408c7-131">WDDM (Direct3D9)</span></span> | <span data-ttu-id="408c7-132">WDDM(Direct3D9Ex/Direct3D10)</span><span class="sxs-lookup"><span data-stu-id="408c7-132">WDDM(Direct3D9Ex/Direct3D10)</span></span> |
|-----------------|------|------------------|------------------------------|
| <span data-ttu-id="408c7-133">NULLREF</span><span class="sxs-lookup"><span data-stu-id="408c7-133">NULLREF</span></span>         | <span data-ttu-id="408c7-134">Ja</span><span class="sxs-lookup"><span data-stu-id="408c7-134">Yes</span></span>  | <span data-ttu-id="408c7-135">Ja</span><span class="sxs-lookup"><span data-stu-id="408c7-135">Yes</span></span>              | <span data-ttu-id="408c7-136">Ja</span><span class="sxs-lookup"><span data-stu-id="408c7-136">Yes</span></span>                          |
| <span data-ttu-id="408c7-137">Hal</span><span class="sxs-lookup"><span data-stu-id="408c7-137">HAL</span></span>             | <span data-ttu-id="408c7-138">Nein</span><span class="sxs-lookup"><span data-stu-id="408c7-138">No</span></span>   | <span data-ttu-id="408c7-139">Nein</span><span class="sxs-lookup"><span data-stu-id="408c7-139">No</span></span>               | <span data-ttu-id="408c7-140">Ja</span><span class="sxs-lookup"><span data-stu-id="408c7-140">Yes</span></span>                          |
| <span data-ttu-id="408c7-141">REF</span><span class="sxs-lookup"><span data-stu-id="408c7-141">REF</span></span>             | <span data-ttu-id="408c7-142">Ja</span><span class="sxs-lookup"><span data-stu-id="408c7-142">Yes</span></span>  | <span data-ttu-id="408c7-143">Ja</span><span class="sxs-lookup"><span data-stu-id="408c7-143">Yes</span></span>              | <span data-ttu-id="408c7-144">Ja</span><span class="sxs-lookup"><span data-stu-id="408c7-144">Yes</span></span>                          |
| <span data-ttu-id="408c7-145">Remotedesktop</span><span class="sxs-lookup"><span data-stu-id="408c7-145">Remote Desktop</span></span>  |      |                  |                              |
| <span data-ttu-id="408c7-146">NULLREF</span><span class="sxs-lookup"><span data-stu-id="408c7-146">NULLREF</span></span>         | <span data-ttu-id="408c7-147">Nein</span><span class="sxs-lookup"><span data-stu-id="408c7-147">No</span></span>   | <span data-ttu-id="408c7-148">Ja</span><span class="sxs-lookup"><span data-stu-id="408c7-148">Yes</span></span>              | <span data-ttu-id="408c7-149">Ja</span><span class="sxs-lookup"><span data-stu-id="408c7-149">Yes</span></span>                          |
| <span data-ttu-id="408c7-150">Hal</span><span class="sxs-lookup"><span data-stu-id="408c7-150">HAL</span></span>             | <span data-ttu-id="408c7-151">Nein</span><span class="sxs-lookup"><span data-stu-id="408c7-151">No</span></span>   | <span data-ttu-id="408c7-152">Ja</span><span class="sxs-lookup"><span data-stu-id="408c7-152">Yes</span></span>              | <span data-ttu-id="408c7-153">Ja</span><span class="sxs-lookup"><span data-stu-id="408c7-153">Yes</span></span>                          |
| <span data-ttu-id="408c7-154">REF</span><span class="sxs-lookup"><span data-stu-id="408c7-154">REF</span></span>             | <span data-ttu-id="408c7-155">Ja</span><span class="sxs-lookup"><span data-stu-id="408c7-155">Yes</span></span>  | <span data-ttu-id="408c7-156">Ja</span><span class="sxs-lookup"><span data-stu-id="408c7-156">Yes</span></span>              | <span data-ttu-id="408c7-157">Ja</span><span class="sxs-lookup"><span data-stu-id="408c7-157">Yes</span></span>                          |
| <span data-ttu-id="408c7-158">Windows-Dienst</span><span class="sxs-lookup"><span data-stu-id="408c7-158">Windows Service</span></span> |      |                  |                              |
| <span data-ttu-id="408c7-159">NULLREF</span><span class="sxs-lookup"><span data-stu-id="408c7-159">NULLREF</span></span>         | <span data-ttu-id="408c7-160">Nein</span><span class="sxs-lookup"><span data-stu-id="408c7-160">No</span></span>   | <span data-ttu-id="408c7-161">Nein</span><span class="sxs-lookup"><span data-stu-id="408c7-161">No</span></span>               | <span data-ttu-id="408c7-162">Nein</span><span class="sxs-lookup"><span data-stu-id="408c7-162">No</span></span>                           |
| <span data-ttu-id="408c7-163">Hal</span><span class="sxs-lookup"><span data-stu-id="408c7-163">HAL</span></span>             | <span data-ttu-id="408c7-164">Nein</span><span class="sxs-lookup"><span data-stu-id="408c7-164">No</span></span>   | <span data-ttu-id="408c7-165">Nein</span><span class="sxs-lookup"><span data-stu-id="408c7-165">No</span></span>               | <span data-ttu-id="408c7-166">Nein</span><span class="sxs-lookup"><span data-stu-id="408c7-166">No</span></span>                           |
| <span data-ttu-id="408c7-167">REF</span><span class="sxs-lookup"><span data-stu-id="408c7-167">REF</span></span>             | <span data-ttu-id="408c7-168">Nein</span><span class="sxs-lookup"><span data-stu-id="408c7-168">No</span></span>   | <span data-ttu-id="408c7-169">Nein</span><span class="sxs-lookup"><span data-stu-id="408c7-169">No</span></span>               | <span data-ttu-id="408c7-170">Nein</span><span class="sxs-lookup"><span data-stu-id="408c7-170">No</span></span>                           |
| <span data-ttu-id="408c7-171">WARP10</span><span class="sxs-lookup"><span data-stu-id="408c7-171">WARP10</span></span>          | <span data-ttu-id="408c7-172">–</span><span class="sxs-lookup"><span data-stu-id="408c7-172">N/A</span></span>  | <span data-ttu-id="408c7-173">–</span><span class="sxs-lookup"><span data-stu-id="408c7-173">N/A</span></span>              | <span data-ttu-id="408c7-174">Ja</span><span class="sxs-lookup"><span data-stu-id="408c7-174">Yes</span></span>                          |



 

<span data-ttu-id="408c7-175">Weitere Informationen zu XPDM, WDDM, Direct3D9Ex und Direct3D 10 finden Sie unter [Grafik-APIs in Windows.](../direct3darticles/graphics-apis-in-windows-vista.md)</span><span class="sxs-lookup"><span data-stu-id="408c7-175">For more information about XPDM, WDDM, Direct3D9Ex, and Direct3D 10, see [Graphics APIs in Windows](../direct3darticles/graphics-apis-in-windows-vista.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="408c7-176">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="408c7-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="408c7-177">Direct3D-Geräte</span><span class="sxs-lookup"><span data-stu-id="408c7-177">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
