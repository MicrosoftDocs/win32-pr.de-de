---
title: Allgemeine Steuerelementversionen
description: In diesem Thema werden die verfügbaren Versionen der Common Control-Bibliothek (ComCtl32.dll) aufgeführt. Es wird beschrieben, wie Sie die Version identifizieren, die ihre Anwendung verwendet, und wie Sie ihre Anwendung auf eine bestimmte Version ausdrungen.
ms.assetid: 1B524A91-B433-4968-9546-8A6AFB67E89C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1131466bd4d3afcaae3a241a6f7854fd5a49450
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423960"
---
# <a name="common-control-versions"></a><span data-ttu-id="c83d6-103">Allgemeine Steuerelementversionen</span><span class="sxs-lookup"><span data-stu-id="c83d6-103">Common Control Versions</span></span>

<span data-ttu-id="c83d6-104">In diesem Thema werden die verfügbaren Versionen der Common Control-Bibliothek (ComCtl32.dll) aufgeführt. Es wird beschrieben, wie Sie die Version identifizieren, die ihre Anwendung verwendet, und wie Sie ihre Anwendung auf eine bestimmte Version ausdrungen.</span><span class="sxs-lookup"><span data-stu-id="c83d6-104">This topic lists the available versions of the Common Control library (ComCtl32.dll), describes how to identify the version that your application is using, and explains how to target your application for a specific version.</span></span>

<span data-ttu-id="c83d6-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="c83d6-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c83d6-106">Allgemeine Versionsnummern der Steuerelement-DLL</span><span class="sxs-lookup"><span data-stu-id="c83d6-106">Common Control DLL Versions Numbers</span></span>](#common-control-dll-versions-numbers)
-   [<span data-ttu-id="c83d6-107">Strukturgrößen für verschiedene allgemeine Steuerelementversionen</span><span class="sxs-lookup"><span data-stu-id="c83d6-107">Structure Sizes for Different Common Control Versions</span></span>](#structure-sizes-for-different-common-control-versions)
-   [<span data-ttu-id="c83d6-108">Verwenden von DllGetVersion zum Bestimmen der Versionsnummer</span><span class="sxs-lookup"><span data-stu-id="c83d6-108">Using DllGetVersion to Determine the Version Number</span></span>](#using-dllgetversion-to-determine-the-version-number)
-   [<span data-ttu-id="c83d6-109">Projektversionen</span><span class="sxs-lookup"><span data-stu-id="c83d6-109">Project Versions</span></span>](#project-versions)
-   [<span data-ttu-id="c83d6-110">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c83d6-110">Related topics</span></span>](#related-topics)

## <a name="common-control-dll-versions-numbers"></a><span data-ttu-id="c83d6-111">Allgemeine Versionsnummern der Steuerelement-DLL</span><span class="sxs-lookup"><span data-stu-id="c83d6-111">Common Control DLL Versions Numbers</span></span>

<span data-ttu-id="c83d6-112">Unterstützung für allgemeine Steuerelemente wird von ComCtl32.dll bereitgestellt, die alle 32-Bit- und 64-Bit-Versionen von Windows enthalten.</span><span class="sxs-lookup"><span data-stu-id="c83d6-112">Support for common controls is provided by ComCtl32.dll, which all 32-bit and 64-bit versions of Windows include.</span></span> <span data-ttu-id="c83d6-113">Jede aufeinander folgende Version der DLL unterstützt die Features und die API früherer Versionen und fügt neue Features hinzu.</span><span class="sxs-lookup"><span data-stu-id="c83d6-113">Each successive version of the DLL supports the features and API of earlier versions and adds new features.</span></span>

<span data-ttu-id="c83d6-114">Da verschiedene Versionen von ComCtl32.dll mit Internet Explorer verteilt wurden, ist die aktive Version manchmal anders als die im Lieferumfang des Betriebssystems enthaltene Version.</span><span class="sxs-lookup"><span data-stu-id="c83d6-114">Because various versions of ComCtl32.dll were distributed with Internet Explorer, the version that is active is sometimes different from the version that was shipped with the operating system.</span></span> <span data-ttu-id="c83d6-115">Aus diesem Grund muss Ihre Anwendung direkt bestimmen, welche Version ComCtl32.dll vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c83d6-115">Therefore, your application must directly determine which version of ComCtl32.dll is present.</span></span>

<span data-ttu-id="c83d6-116">In der Referenzdokumentation zu allgemeinen Steuerelementen geben viele Programmierelemente eine unterstützte DLL-Mindestversionsnummer an.</span><span class="sxs-lookup"><span data-stu-id="c83d6-116">In the common controls reference documentation, many programming elements specify a minimum supported DLL version number.</span></span> <span data-ttu-id="c83d6-117">Diese Versionsnummer gibt an, dass das Programmierelement in dieser Version und in nachfolgenden Versionen der DLL implementiert ist, sofern nichts anderes angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c83d6-117">This version number indicates that the programming element is implemented in that version and subsequent versions of the DLL unless otherwise specified.</span></span> <span data-ttu-id="c83d6-118">Wenn keine Versionsnummer angegeben wird, wird das Programmierelement in allen vorhandenen Versionen der DLL implementiert.</span><span class="sxs-lookup"><span data-stu-id="c83d6-118">If no version number is specified, the programming element is implemented in all existing versions of the DLL.</span></span>

<span data-ttu-id="c83d6-119">In der folgenden Tabelle werden die verschiedenen DLL-Versionen und deren Verteilung auf unterstützte Betriebssystemen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c83d6-119">The following table outlines the different DLL versions and how they were distributed on supported OSes.</span></span>



<span data-ttu-id="c83d6-120">ComCtl32.dll</span><span class="sxs-lookup"><span data-stu-id="c83d6-120">ComCtl32.dll</span></span>

<span data-ttu-id="c83d6-121">Version</span><span class="sxs-lookup"><span data-stu-id="c83d6-121">Version</span></span>

<span data-ttu-id="c83d6-122">Verteilungsplattform</span><span class="sxs-lookup"><span data-stu-id="c83d6-122">Distribution Platform</span></span>

<span data-ttu-id="c83d6-123">5.81</span><span class="sxs-lookup"><span data-stu-id="c83d6-123">5.81</span></span>

<span data-ttu-id="c83d6-124">Microsoft Internet Explorer 5.01, Microsoft Internet Explorer 5.5 und Microsoft Internet Explorer 6</span><span class="sxs-lookup"><span data-stu-id="c83d6-124">Microsoft Internet Explorer 5.01, Microsoft Internet Explorer 5.5, and Microsoft Internet Explorer 6</span></span>

<span data-ttu-id="c83d6-125">5.82</span><span class="sxs-lookup"><span data-stu-id="c83d6-125">5.82</span></span>

<span data-ttu-id="c83d6-126">Windows Server 2003, Windows Vista, Windows Server 2008 und Windows 7</span><span class="sxs-lookup"><span data-stu-id="c83d6-126">Windows Server 2003, Windows Vista, Windows Server 2008, and Windows 7</span></span>

<span data-ttu-id="c83d6-127">6.0</span><span class="sxs-lookup"><span data-stu-id="c83d6-127">6.0</span></span>

<span data-ttu-id="c83d6-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c83d6-128">Windows Server 2003</span></span>

<span data-ttu-id="c83d6-129">6.10</span><span class="sxs-lookup"><span data-stu-id="c83d6-129">6.10</span></span>

<span data-ttu-id="c83d6-130">Windows Vista, Windows Server 2008 und Windows 7</span><span class="sxs-lookup"><span data-stu-id="c83d6-130">Windows Vista, Windows Server 2008, and Windows 7</span></span>



 

## <a name="structure-sizes-for-different-common-control-versions"></a><span data-ttu-id="c83d6-131">Strukturgrößen für verschiedene allgemeine Steuerelementversionen</span><span class="sxs-lookup"><span data-stu-id="c83d6-131">Structure Sizes for Different Common Control Versions</span></span>

<span data-ttu-id="c83d6-132">Fortlaufende Verbesserungen an allgemeinen Steuerelementen haben dazu geführt, dass viele der Strukturen erweitert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c83d6-132">Ongoing enhancements to common controls have resulted in the need to extend many of the structures.</span></span> <span data-ttu-id="c83d6-133">Aus diesem Grund hat sich die Größe der Strukturen zwischen verschiedenen Versionen von Commctrl.h geändert.</span><span class="sxs-lookup"><span data-stu-id="c83d6-133">For this reason, the size of the structures has changed between different versions of Commctrl.h.</span></span> <span data-ttu-id="c83d6-134">Da die meisten allgemeinen Steuerelementstrukturen eine Strukturgröße als einen der Parameter annehmen, kann eine Nachricht oder Funktion fehlschlagen, wenn die Größe nicht erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="c83d6-134">Because most of the common control structures take a structure size as one of the parameters, a message or function can fail if the size is not recognized.</span></span> <span data-ttu-id="c83d6-135">Um dies zu beheben, wurden Strukturgrößenkonstanten definiert, um die Ausrichtung auf verschiedene Versionen von ComCtl32.dll zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c83d6-135">To remedy this, structure size constants have been defined to aid in targeting different version of ComCtl32.dll.</span></span> <span data-ttu-id="c83d6-136">In der folgenden Liste werden die Strukturgrößenkonstanten definiert.</span><span class="sxs-lookup"><span data-stu-id="c83d6-136">The following list defines the structure size constants.</span></span>



|    <span data-ttu-id="c83d6-137">Strukturgrößenkonstante</span><span class="sxs-lookup"><span data-stu-id="c83d6-137">Structure Size Constant</span></span>                           |     <span data-ttu-id="c83d6-138">Definition</span><span class="sxs-lookup"><span data-stu-id="c83d6-138">Definition</span></span>                                                                                         |
|-------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c83d6-139">HDITEM \_ \_ V1-GRÖßE</span><span class="sxs-lookup"><span data-stu-id="c83d6-139">HDITEM\_V1\_SIZE</span></span>              | <span data-ttu-id="c83d6-140">Die Größe der [**HDITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-hditema) in Version 4.0.</span><span class="sxs-lookup"><span data-stu-id="c83d6-140">The size of the [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure in version 4.0.</span></span>                           |
| <span data-ttu-id="c83d6-141">IMAGELISTDRAWPARAMS \_ \_ V3-GRÖßE</span><span class="sxs-lookup"><span data-stu-id="c83d6-141">IMAGELISTDRAWPARAMS\_V3\_SIZE</span></span> | <span data-ttu-id="c83d6-142">Die Größe der [**IMAGELISTDRAWPARAMS-Struktur**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) in Version 5.9.</span><span class="sxs-lookup"><span data-stu-id="c83d6-142">The size of the [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) structure in version 5.9.</span></span> |
| <span data-ttu-id="c83d6-143">LVCOLUMN \_ \_ V1-GRÖßE</span><span class="sxs-lookup"><span data-stu-id="c83d6-143">LVCOLUMN\_V1\_SIZE</span></span>            | <span data-ttu-id="c83d6-144">Die Größe der [**LVCOLUMN-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) in Version 4.0.</span><span class="sxs-lookup"><span data-stu-id="c83d6-144">The size of the [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure in version 4.0.</span></span>                       |
| <span data-ttu-id="c83d6-145">LVGROUP \_ \_ V5-GRÖßE</span><span class="sxs-lookup"><span data-stu-id="c83d6-145">LVGROUP\_V5\_SIZE</span></span>             | <span data-ttu-id="c83d6-146">Die Größe der [**LVGROUP-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) in Version 6.0.</span><span class="sxs-lookup"><span data-stu-id="c83d6-146">The size of the [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure in version 6.0.</span></span>                         |
| <span data-ttu-id="c83d6-147">LVHITTESTINFO \_ V1 \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="c83d6-147">LVHITTESTINFO\_V1\_SIZE</span></span>       | <span data-ttu-id="c83d6-148">Die Größe der [**LVHITTESTINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) in Version 4.0.</span><span class="sxs-lookup"><span data-stu-id="c83d6-148">The size of the [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure in version 4.0.</span></span>             |
| <span data-ttu-id="c83d6-149">LVITEM \_ \_ V1-GRÖßE</span><span class="sxs-lookup"><span data-stu-id="c83d6-149">LVITEM\_V1\_SIZE</span></span>              | <span data-ttu-id="c83d6-150">Die Größe der [**LVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitema) in Version 4.0.</span><span class="sxs-lookup"><span data-stu-id="c83d6-150">The size of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure in version 4.0.</span></span>                           |
| <span data-ttu-id="c83d6-151">LVITEM \_ V5 \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="c83d6-151">LVITEM\_V5\_SIZE</span></span>              | <span data-ttu-id="c83d6-152">Die Größe der [**LVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitema) in Version 6.0.</span><span class="sxs-lookup"><span data-stu-id="c83d6-152">The size of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure in version 6.0.</span></span>                           |
| <span data-ttu-id="c83d6-153">LVTILEINFO \_ V5 \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="c83d6-153">LVTILEINFO\_V5\_SIZE</span></span>          | <span data-ttu-id="c83d6-154">Die Größe der [**LVTILEINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) in Version 6.0.</span><span class="sxs-lookup"><span data-stu-id="c83d6-154">The size of the [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) structure in version 6.0.</span></span>                   |
| <span data-ttu-id="c83d6-155">MCHITTESTINFO \_ \_ V1-GRÖßE</span><span class="sxs-lookup"><span data-stu-id="c83d6-155">MCHITTESTINFO\_V1\_SIZE</span></span>       | <span data-ttu-id="c83d6-156">Die Größe der [**MCHITTESTINFO-Struktur**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) in Version 4.0.</span><span class="sxs-lookup"><span data-stu-id="c83d6-156">The size of the [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) structure in version 4.0.</span></span>             |
| <span data-ttu-id="c83d6-157">NMLVCUSTOMDRAW \_ V3 \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="c83d6-157">NMLVCUSTOMDRAW\_V3\_SIZE</span></span>      | <span data-ttu-id="c83d6-158">Die Größe der [**NMLVCUSTOMDRAW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) in Version 4.7.</span><span class="sxs-lookup"><span data-stu-id="c83d6-158">The size of the [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) structure in version 4.7.</span></span>           |
| <span data-ttu-id="c83d6-159">NMTTDISPINFO \_ V1 \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="c83d6-159">NMTTDISPINFO\_V1\_SIZE</span></span>        | <span data-ttu-id="c83d6-160">Die Größe der [**NMTTDISPINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) in Version 4.0.</span><span class="sxs-lookup"><span data-stu-id="c83d6-160">The size of the [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure in version 4.0.</span></span>               |
| <span data-ttu-id="c83d6-161">NMTVCUSTOMDRAW \_ V3 \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="c83d6-161">NMTVCUSTOMDRAW\_V3\_SIZE</span></span>      | <span data-ttu-id="c83d6-162">Die Größe der [**NMTVCUSTOMDRAW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) in Version 4.7.</span><span class="sxs-lookup"><span data-stu-id="c83d6-162">The size of the [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) structure in version 4.7.</span></span>           |
| <span data-ttu-id="c83d6-163">PROPSHEETHEADER \_ V1 \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="c83d6-163">PROPSHEETHEADER\_V1\_SIZE</span></span>     | <span data-ttu-id="c83d6-164">Die Größe der [**PROPSHEETHEADER-Struktur**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) in Version 4.0.</span><span class="sxs-lookup"><span data-stu-id="c83d6-164">The size of the [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) structure in version 4.0.</span></span>         |
| <span data-ttu-id="c83d6-165">PROPSHEETPAGE \_ V1 \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="c83d6-165">PROPSHEETPAGE\_V1\_SIZE</span></span>       | <span data-ttu-id="c83d6-166">Die Größe der [**PROPSHEETPAGE-Struktur**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) in Version 4.0.</span><span class="sxs-lookup"><span data-stu-id="c83d6-166">The size of the [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) structure in version 4.0.</span></span>             |
| <span data-ttu-id="c83d6-167">REBARBANDINFO \_ \_ V3-GRÖßE</span><span class="sxs-lookup"><span data-stu-id="c83d6-167">REBARBANDINFO\_V3\_SIZE</span></span>       | <span data-ttu-id="c83d6-168">Die Größe der [**REBARBANDINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) in Version 4.7.</span><span class="sxs-lookup"><span data-stu-id="c83d6-168">The size of the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure in version 4.7.</span></span>             |
| <span data-ttu-id="c83d6-169">REBARBANDINFO \_ \_ V6-GRÖßE</span><span class="sxs-lookup"><span data-stu-id="c83d6-169">REBARBANDINFO\_V6\_SIZE</span></span>       | <span data-ttu-id="c83d6-170">Die Größe der [**REBARBANDINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) in Version 6.0.</span><span class="sxs-lookup"><span data-stu-id="c83d6-170">The size of the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure in version 6.0.</span></span>             |
| <span data-ttu-id="c83d6-171">TTTOOLINFO \_ V1 \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="c83d6-171">TTTOOLINFO\_V1\_SIZE</span></span>          | <span data-ttu-id="c83d6-172">Die Größe der [**TOOLINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) in Version 4.0.</span><span class="sxs-lookup"><span data-stu-id="c83d6-172">The size of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure in version 4.0.</span></span>                       |
| <span data-ttu-id="c83d6-173">TTTOOLINFO \_ V2 \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="c83d6-173">TTTOOLINFO\_V2\_SIZE</span></span>          | <span data-ttu-id="c83d6-174">Die Größe der [**TOOLINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) in Version 4.7.</span><span class="sxs-lookup"><span data-stu-id="c83d6-174">The size of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure in version 4.7.</span></span>                       |
| <span data-ttu-id="c83d6-175">TTTOOLINFO \_ V3 \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="c83d6-175">TTTOOLINFO\_V3\_SIZE</span></span>          | <span data-ttu-id="c83d6-176">Die Größe der [**TOOLINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) in Version 6.0.</span><span class="sxs-lookup"><span data-stu-id="c83d6-176">The size of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure in version 6.0.</span></span>                       |
| <span data-ttu-id="c83d6-177">TVINSERTSTRUCT \_ V1 \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="c83d6-177">TVINSERTSTRUCT\_V1\_SIZE</span></span>      | <span data-ttu-id="c83d6-178">Die Größe der [**TVINSERTSTRUCT-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) in Version 4.0.</span><span class="sxs-lookup"><span data-stu-id="c83d6-178">The size of the [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) structure in version 4.0.</span></span>           |



 

## <a name="using-dllgetversion-to-determine-the-version-number"></a><span data-ttu-id="c83d6-179">Ermitteln der Versionsnummer mithilfe von DllGetVersion</span><span class="sxs-lookup"><span data-stu-id="c83d6-179">Using DllGetVersion to Determine the Version Number</span></span>

<span data-ttu-id="c83d6-180">Die [**DllGetVersion-Funktion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) kann von einer Anwendung aufgerufen werden, um zu bestimmen, welche DLL-Version auf dem System vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c83d6-180">The [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) function can be called by an application to determine which DLL version is present on the system.</span></span>

<span data-ttu-id="c83d6-181">[**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) gibt eine [**DLLVERSIONINFO2-Struktur**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) zurück.</span><span class="sxs-lookup"><span data-stu-id="c83d6-181">[**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) returns a [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="c83d6-182">Zusätzlich zu den Informationen, die über [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo)bereitgestellt werden, stellt **DLLVERSIONINFO2** auch die Hotfixnummer bereit, mit der das neueste installierte Service Pack identifiziert wird. Dies bietet eine stabilere Möglichkeit zum Vergleichen von Versionsnummern.</span><span class="sxs-lookup"><span data-stu-id="c83d6-182">In addition to the information provided through [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo), **DLLVERSIONINFO2** also provides the hotfix number that identifies the latest installed service pack, which provides a more robust way to compare version numbers.</span></span> <span data-ttu-id="c83d6-183">Da der erste Member von **DLLVERSIONINFO2** eine **DLLVERSIONINFO-Struktur** ist, ist die spätere -Struktur abwärtskompatibel.</span><span class="sxs-lookup"><span data-stu-id="c83d6-183">Because the first member of **DLLVERSIONINFO2** is a **DLLVERSIONINFO** structure, the later structure is backward-compatible.</span></span>


<span data-ttu-id="c83d6-184">Die folgende Beispielfunktion `GetVersion` lädt eine angegebene DLL und versucht, ihre [**DllGetVersion-Funktion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c83d6-184">The following sample function `GetVersion` loads a specified DLL and attempts to call its [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) function.</span></span> <span data-ttu-id="c83d6-185">Bei Erfolg wird ein Makro verwendet, um die Haupt- und Nebenversionsnummern aus der [**DLLVERSIONINFO-Struktur**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo) in ein **DWORD** zu packen, das an die aufrufende Anwendung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c83d6-185">If successful, it uses a macro to pack the major and minor version numbers from the [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo) structure into a **DWORD** that is returned to the calling application.</span></span> <span data-ttu-id="c83d6-186">Wenn die DLL **dllGetVersion** nicht exportiert, gibt die Funktion 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="c83d6-186">If the DLL does not export **DllGetVersion**, the function returns zero.</span></span> <span data-ttu-id="c83d6-187">Sie können die Funktion ändern, um die Möglichkeit zu behandeln, **dass DllGetVersion** eine [**DLLVERSIONINFO2-Struktur zurückgibt.**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2)</span><span class="sxs-lookup"><span data-stu-id="c83d6-187">You can modify the function to handle the possibility that **DllGetVersion** returns a [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="c83d6-188">Falls ja, verwenden Sie die Informationen im **ullVersion-Member** dieser **DLLVERSIONINFO2-Struktur,** um Versionen, Buildnummern und Service Pack-Releases zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="c83d6-188">If so, use the information in that **DLLVERSIONINFO2** structure's **ullVersion** member to compare versions, build numbers, and service pack releases.</span></span> <span data-ttu-id="c83d6-189">Das [**MAKEDLLVERULL-Makro**](/windows/desktop/api/shlwapi/nf-shlwapi-makedllverull) vereinfacht die Aufgabe, diese Werte mit denen in **ullVersion zu vergleichen.**</span><span class="sxs-lookup"><span data-stu-id="c83d6-189">The [**MAKEDLLVERULL**](/windows/desktop/api/shlwapi/nf-shlwapi-makedllverull) macro simplifies the task of comparing these values to those in **ullVersion**.</span></span>

> [!Note]  
> <span data-ttu-id="c83d6-190">Die [**falsche Verwendung von LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann Sicherheitsrisiken darstellen.</span><span class="sxs-lookup"><span data-stu-id="c83d6-190">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can pose security risks.</span></span> <span data-ttu-id="c83d6-191">Informationen zum ordnungsgemäßen Laden von DLLs mit verschiedenen Versionen von Windows finden Sie in der **LoadLibrary-Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="c83d6-191">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>

 


```C++
#include "stdafx.h"
#include "windows.h"
#include "windef.h"
#include "winbase.h"
#include "shlwapi.h"

#define PACKVERSION(major,minor) MAKELONG(minor,major)

DWORD GetVersion(LPCTSTR lpszDllName)
{
    HINSTANCE hinstDll;
    DWORD dwVersion = 0;

    // For security purposes, LoadLibrary should be provided with a fully qualified 
    // path to the DLL. The lpszDllName variable should be tested to ensure that it 
    // is a fully qualified path before it is used. 
    hinstDll = LoadLibrary(lpszDllName);
    
    if(hinstDll)
    {
        DLLGETVERSIONPROC pDllGetVersion;
        pDllGetVersion = (DLLGETVERSIONPROC)GetProcAddress(hinstDll, "DllGetVersion");

        // Because some DLLs might not implement this function, you must test for 
        // it explicitly. Depending on the particular DLL, the lack of a DllGetVersion 
        // function can be a useful indicator of the version. 

        if(pDllGetVersion)
        {
            DLLVERSIONINFO dvi;
            HRESULT hr;

            ZeroMemory(&dvi, sizeof(dvi));
            dvi.info1.cbSize = sizeof(dvi);

            hr = (*pDllGetVersion)(&dvi);

            if(SUCCEEDED(hr))
            {
               dwVersion = PACKVERSION(dvi.info1.dwMajorVersion, dvi.info1.dwMinorVersion);
            }
        }
        FreeLibrary(hinstDll);
    }
    return dwVersion;
}
```



<span data-ttu-id="c83d6-192">Das folgende Codebeispiel zeigt, wie Sie mit testen können, ob ComCtl32.dll Version `GetVersion` 6.0 oder höher ist.</span><span class="sxs-lookup"><span data-stu-id="c83d6-192">The following code example shows how you can use `GetVersion` to test whether ComCtl32.dll is version 6.0 or later.</span></span>


```C++
LPCTSTR lpszDllName = L"C:\\Windows\\System32\\ComCtl32.dll";
DWORD dwVer = GetVersion(lpszDllName);
DWORD dwTarget = PACKVERSION(6,0);

if(dwVer >= dwTarget)
{
    // This version of ComCtl32.dll is version 6.0 or later.
}
else
{
    // Proceed knowing that version 6.0 or later additions are not available.
    // Use an alternate approach for older the DLL version.
}
```



## <a name="project-versions"></a><span data-ttu-id="c83d6-193">Projektversionen</span><span class="sxs-lookup"><span data-stu-id="c83d6-193">Project Versions</span></span>

<span data-ttu-id="c83d6-194">Um sicherzustellen, dass Ihre Anwendung mit verschiedenen Zielversionen einer DLL-Datei kompatibel ist, sind Versionsmakros in den Headerdateien vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c83d6-194">To ensure that your application is compatible with different targeted versions of a .dll file, version macros are present in the header files.</span></span> <span data-ttu-id="c83d6-195">Diese Makros werden verwendet, um bestimmte Definitionen für verschiedene Versionen der DLL zu definieren, auszuschließen oder neu zu definieren.</span><span class="sxs-lookup"><span data-stu-id="c83d6-195">These macros are used to define, exclude, or redefine certain definitions for different versions of the DLL.</span></span> <span data-ttu-id="c83d6-196">Eine [ausführliche Beschreibung dieser Makros](/windows/desktop/WinProg/using-the-windows-headers) finden Sie unter Verwenden der Windows-Header.</span><span class="sxs-lookup"><span data-stu-id="c83d6-196">See [Using the Windows Headers](/windows/desktop/WinProg/using-the-windows-headers) for an in-depth description of these macros.</span></span>

<span data-ttu-id="c83d6-197">Der Makroname **\_ WIN32 \_ IE** befindet sich beispielsweise häufig in älteren Headern.</span><span class="sxs-lookup"><span data-stu-id="c83d6-197">For example, the macro name **\_WIN32\_IE** is commonly found in older headers.</span></span> <span data-ttu-id="c83d6-198">Sie sind dafür verantwortlich, das Makro als Hexadezimalzahl zu definieren.</span><span class="sxs-lookup"><span data-stu-id="c83d6-198">You are responsible for defining the macro as a hexadecimal number.</span></span> <span data-ttu-id="c83d6-199">Diese Versionsnummer definiert die Zielversion der Anwendung, die die DLL verwendet.</span><span class="sxs-lookup"><span data-stu-id="c83d6-199">This version number defines the target version of the application that is using the DLL.</span></span> <span data-ttu-id="c83d6-200">Die folgende Tabelle zeigt die verfügbaren Versionsnummern und die Auswirkungen auf Ihre Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c83d6-200">The following table shows the available version numbers and the effect each has on your application.</span></span>



| <span data-ttu-id="c83d6-201">Version</span><span class="sxs-lookup"><span data-stu-id="c83d6-201">Version</span></span> | <span data-ttu-id="c83d6-202">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c83d6-202">Description</span></span>                                                                                                                                           |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c83d6-203">0x0300</span><span class="sxs-lookup"><span data-stu-id="c83d6-203">0x0300</span></span>  | <span data-ttu-id="c83d6-204">Die Anwendung ist mit ComCtl32.dll 4.70 und höher kompatibel.</span><span class="sxs-lookup"><span data-stu-id="c83d6-204">The application is compatible with ComCtl32.dll version 4.70 and later.</span></span> <span data-ttu-id="c83d6-205">Die Anwendung kann keine Features implementieren, die nach Version 4.70 hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="c83d6-205">The application cannot implement features that were added after version 4.70.</span></span> |
| <span data-ttu-id="c83d6-206">0x0400</span><span class="sxs-lookup"><span data-stu-id="c83d6-206">0x0400</span></span>  | <span data-ttu-id="c83d6-207">Die Anwendung ist mit ComCtl32.dll Version 4.71 und höher kompatibel.</span><span class="sxs-lookup"><span data-stu-id="c83d6-207">The application is compatible with ComCtl32.dll version 4.71 and later.</span></span> <span data-ttu-id="c83d6-208">Die Anwendung kann keine Features implementieren, die nach Version 4.71 hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="c83d6-208">The application cannot implement features that were added after version 4.71.</span></span> |
| <span data-ttu-id="c83d6-209">0x0401</span><span class="sxs-lookup"><span data-stu-id="c83d6-209">0x0401</span></span>  | <span data-ttu-id="c83d6-210">Die Anwendung ist mit ComCtl32.dll 4.72 und höher kompatibel.</span><span class="sxs-lookup"><span data-stu-id="c83d6-210">The application is compatible with ComCtl32.dll version 4.72 and later.</span></span> <span data-ttu-id="c83d6-211">Die Anwendung kann keine Features implementieren, die nach Version 4.72 hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="c83d6-211">The application cannot implement features that were added after version 4.72.</span></span> |
| <span data-ttu-id="c83d6-212">0x0500</span><span class="sxs-lookup"><span data-stu-id="c83d6-212">0x0500</span></span>  | <span data-ttu-id="c83d6-213">Die Anwendung ist mit ComCtl32.dll Version 5.80 und höher kompatibel.</span><span class="sxs-lookup"><span data-stu-id="c83d6-213">The application is compatible with ComCtl32.dll version 5.80 and later.</span></span> <span data-ttu-id="c83d6-214">Die Anwendung kann keine Features implementieren, die nach Version 5.80 hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="c83d6-214">The application cannot implement features that were added after version 5.80.</span></span> |
| <span data-ttu-id="c83d6-215">0x0501</span><span class="sxs-lookup"><span data-stu-id="c83d6-215">0x0501</span></span>  | <span data-ttu-id="c83d6-216">Die Anwendung ist mit ComCtl32.dll Version 5.81 und höher kompatibel.</span><span class="sxs-lookup"><span data-stu-id="c83d6-216">The application is compatible with ComCtl32.dll version 5.81 and later.</span></span> <span data-ttu-id="c83d6-217">Die Anwendung kann keine Features implementieren, die nach Version 5.81 hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="c83d6-217">The application cannot implement features that were added after version 5.81.</span></span> |
| <span data-ttu-id="c83d6-218">0x0600</span><span class="sxs-lookup"><span data-stu-id="c83d6-218">0x0600</span></span>  | <span data-ttu-id="c83d6-219">Die Anwendung ist mit ComCtl32.dll Version 6.0 und höher kompatibel.</span><span class="sxs-lookup"><span data-stu-id="c83d6-219">The application is compatible with ComCtl32.dll version 6.0 and later.</span></span> <span data-ttu-id="c83d6-220">Die Anwendung kann keine Features implementieren, die nach Version 6.0 hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="c83d6-220">The application cannot implement features that were added after version 6.0.</span></span>   |



 

<span data-ttu-id="c83d6-221">Wenn Sie das **\_ \_ WIN32-IE-Makro** in Ihrem Projekt nicht definieren, wird es automatisch als 0x0500 definiert.</span><span class="sxs-lookup"><span data-stu-id="c83d6-221">If you do not define the **\_WIN32\_IE** macro in your project, it is automatically defined as 0x0500.</span></span> <span data-ttu-id="c83d6-222">Um einen anderen Wert zu definieren, können Sie den Compilerdirektiven in Ihrer Make-Datei Folgendes hinzufügen: ersetzen Sie die gewünschte Versionsnummer für 0x0400.</span><span class="sxs-lookup"><span data-stu-id="c83d6-222">To define a different value, you can add the following to the compiler directives in your make file; substitute the desired version number for 0x0400.</span></span>


```C++
/D _WIN32_IE=0x0400
```



<span data-ttu-id="c83d6-223">Eine weitere Methode besteht darin, eine Zeile ähnlich der folgenden in Ihrem Quellcode hinzuzufügen, bevor Sie die Shell-Headerdateien einschließen.</span><span class="sxs-lookup"><span data-stu-id="c83d6-223">Another method is to add a line similar to the following in your source code before you include the Shell header files.</span></span> <span data-ttu-id="c83d6-224">Ersetzen Sie 0x0400 durch die gewünschte Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="c83d6-224">Substitute the desired version number for 0x0400.</span></span>


```C++
#define _WIN32_IE 0x0400
#include <commctrl.h>
```



## <a name="related-topics"></a><span data-ttu-id="c83d6-225">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c83d6-225">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c83d6-226">Informationen zu allgemeinen Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="c83d6-226">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 