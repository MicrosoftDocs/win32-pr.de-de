---
title: Allgemeine Steuerelement Versionen
description: In diesem Thema werden die verfügbaren Versionen der allgemeinen Steuerelement Bibliothek (ComCtl32.dll) aufgelistet. es wird beschrieben, wie Sie die Version identifizieren, die von der Anwendung verwendet wird, und es wird erläutert, wie Sie Ihre Anwendung für eine bestimmte Version ausrichten.
ms.assetid: 1B524A91-B433-4968-9546-8A6AFB67E89C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc51fe027e6169ab1c28904c3145be2f5042d9a0
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104474703"
---
# <a name="common-control-versions"></a><span data-ttu-id="92671-103">Allgemeine Steuerelement Versionen</span><span class="sxs-lookup"><span data-stu-id="92671-103">Common Control Versions</span></span>

<span data-ttu-id="92671-104">In diesem Thema werden die verfügbaren Versionen der allgemeinen Steuerelement Bibliothek (ComCtl32.dll) aufgelistet. es wird beschrieben, wie Sie die Version identifizieren, die von der Anwendung verwendet wird, und es wird erläutert, wie Sie Ihre Anwendung für eine bestimmte Version ausrichten.</span><span class="sxs-lookup"><span data-stu-id="92671-104">This topic lists the available versions of the Common Control library (ComCtl32.dll), describes how to identify the version that your application is using, and explains how to target your application for a specific version.</span></span>

<span data-ttu-id="92671-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="92671-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="92671-106">Versions Nummern für allgemeine Steuerelement-dll</span><span class="sxs-lookup"><span data-stu-id="92671-106">Common Control DLL Versions Numbers</span></span>](#common-control-dll-versions-numbers)
-   [<span data-ttu-id="92671-107">Struktur Größen für verschiedene allgemeine Steuerelement Versionen</span><span class="sxs-lookup"><span data-stu-id="92671-107">Structure Sizes for Different Common Control Versions</span></span>](#structure-sizes-for-different-common-control-versions)
-   [<span data-ttu-id="92671-108">Verwenden von dllgetversion zum Ermitteln der Versionsnummer</span><span class="sxs-lookup"><span data-stu-id="92671-108">Using DllGetVersion to Determine the Version Number</span></span>](#using-dllgetversion-to-determine-the-version-number)
-   [<span data-ttu-id="92671-109">Projekt Versionen</span><span class="sxs-lookup"><span data-stu-id="92671-109">Project Versions</span></span>](#project-versions)
-   [<span data-ttu-id="92671-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="92671-110">Related topics</span></span>](#related-topics)

## <a name="common-control-dll-versions-numbers"></a><span data-ttu-id="92671-111">Versions Nummern für allgemeine Steuerelement-dll</span><span class="sxs-lookup"><span data-stu-id="92671-111">Common Control DLL Versions Numbers</span></span>

<span data-ttu-id="92671-112">Die Unterstützung für allgemeine Steuerelemente wird von ComCtl32.dll bereitgestellt, die alle 32-Bit-und 64-Bit-Versionen von Windows enthalten.</span><span class="sxs-lookup"><span data-stu-id="92671-112">Support for common controls is provided by ComCtl32.dll, which all 32-bit and 64-bit versions of Windows include.</span></span> <span data-ttu-id="92671-113">Jede aufeinander folgende Version der DLL unterstützt die Features und API früherer Versionen und fügt neue Funktionen hinzu.</span><span class="sxs-lookup"><span data-stu-id="92671-113">Each successive version of the DLL supports the features and API of earlier versions and adds new features.</span></span>

<span data-ttu-id="92671-114">Da verschiedene Versionen von ComCtl32.dll mit Internet Explorer verteilt wurden, unterscheidet sich die aktive Version manchmal von der Version, die mit dem Betriebssystem ausgeliefert wurde.</span><span class="sxs-lookup"><span data-stu-id="92671-114">Because various versions of ComCtl32.dll were distributed with Internet Explorer, the version that is active is sometimes different from the version that was shipped with the operating system.</span></span> <span data-ttu-id="92671-115">Daher muss Ihre Anwendung direkt ermitteln, welche Version von ComCtl32.dll vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="92671-115">Therefore, your application must directly determine which version of ComCtl32.dll is present.</span></span>

<span data-ttu-id="92671-116">In der Referenz Dokumentation zu allgemeinen Steuerelementen geben viele Programmier Elemente eine unterstützte dll-Versionsnummer an.</span><span class="sxs-lookup"><span data-stu-id="92671-116">In the common controls reference documentation, many programming elements specify a minimum supported DLL version number.</span></span> <span data-ttu-id="92671-117">Diese Versionsnummer gibt an, dass das Programmier Element in dieser Version und in nachfolgenden Versionen der dll implementiert ist, sofern nicht anders angegeben.</span><span class="sxs-lookup"><span data-stu-id="92671-117">This version number indicates that the programming element is implemented in that version and subsequent versions of the DLL unless otherwise specified.</span></span> <span data-ttu-id="92671-118">Wenn keine Versionsnummer angegeben ist, wird das Programmier Element in allen vorhandenen Versionen der dll implementiert.</span><span class="sxs-lookup"><span data-stu-id="92671-118">If no version number is specified, the programming element is implemented in all existing versions of the DLL.</span></span>

<span data-ttu-id="92671-119">In der folgenden Tabelle werden die verschiedenen dll-Versionen und deren Verteilung auf unterstützte Betriebssysteme beschrieben.</span><span class="sxs-lookup"><span data-stu-id="92671-119">The following table outlines the different DLL versions and how they were distributed on supported OSes.</span></span>



<span data-ttu-id="92671-120">ComCtl32.dll</span><span class="sxs-lookup"><span data-stu-id="92671-120">ComCtl32.dll</span></span>

<span data-ttu-id="92671-121">Version</span><span class="sxs-lookup"><span data-stu-id="92671-121">Version</span></span>

<span data-ttu-id="92671-122">Verteilungs Plattform</span><span class="sxs-lookup"><span data-stu-id="92671-122">Distribution Platform</span></span>

<span data-ttu-id="92671-123">5,81</span><span class="sxs-lookup"><span data-stu-id="92671-123">5.81</span></span>

<span data-ttu-id="92671-124">Microsoft Internet Explorer 5,01, Microsoft Internet Explorer 5,5 und Microsoft Internet Explorer 6</span><span class="sxs-lookup"><span data-stu-id="92671-124">Microsoft Internet Explorer 5.01, Microsoft Internet Explorer 5.5, and Microsoft Internet Explorer 6</span></span>

<span data-ttu-id="92671-125">5,82</span><span class="sxs-lookup"><span data-stu-id="92671-125">5.82</span></span>

<span data-ttu-id="92671-126">Windows Server 2003, Windows Vista, Windows Server 2008 und Windows 7</span><span class="sxs-lookup"><span data-stu-id="92671-126">Windows Server 2003, Windows Vista, Windows Server 2008, and Windows 7</span></span>

<span data-ttu-id="92671-127">6.0</span><span class="sxs-lookup"><span data-stu-id="92671-127">6.0</span></span>

<span data-ttu-id="92671-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="92671-128">Windows Server 2003</span></span>

<span data-ttu-id="92671-129">6.10</span><span class="sxs-lookup"><span data-stu-id="92671-129">6.10</span></span>

<span data-ttu-id="92671-130">Windows Vista, Windows Server 2008 und Windows 7</span><span class="sxs-lookup"><span data-stu-id="92671-130">Windows Vista, Windows Server 2008, and Windows 7</span></span>



 

## <a name="structure-sizes-for-different-common-control-versions"></a><span data-ttu-id="92671-131">Struktur Größen für verschiedene allgemeine Steuerelement Versionen</span><span class="sxs-lookup"><span data-stu-id="92671-131">Structure Sizes for Different Common Control Versions</span></span>

<span data-ttu-id="92671-132">Fortlaufende Verbesserungen an allgemeinen Steuerelementen haben dazu geführt, dass viele der Strukturen erweitert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="92671-132">Ongoing enhancements to common controls have resulted in the need to extend many of the structures.</span></span> <span data-ttu-id="92671-133">Aus diesem Grund hat sich die Größe der Strukturen zwischen den verschiedenen Versionen von "kommctrl. h" geändert.</span><span class="sxs-lookup"><span data-stu-id="92671-133">For this reason, the size of the structures has changed between different versions of Commctrl.h.</span></span> <span data-ttu-id="92671-134">Da die meisten der allgemeinen Steuerelement Strukturen eine Struktur Größe als einen der Parameter annehmen, kann eine Nachricht oder Funktion fehlschlagen, wenn die Größe nicht erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="92671-134">Because most of the common control structures take a structure size as one of the parameters, a message or function can fail if the size is not recognized.</span></span> <span data-ttu-id="92671-135">Um dieses Problem zu beheben, wurden strukturgrößenkonstanten definiert, um das Ziel einer anderen Version von ComCtl32.dll zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="92671-135">To remedy this, structure size constants have been defined to aid in targeting different version of ComCtl32.dll.</span></span> <span data-ttu-id="92671-136">In der folgenden Liste sind die Konstanten für die Struktur Größe definiert.</span><span class="sxs-lookup"><span data-stu-id="92671-136">The following list defines the structure size constants.</span></span>



|                               |                                                                                              |
|-------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="92671-137">HDITEM \_ v1- \_ Größe</span><span class="sxs-lookup"><span data-stu-id="92671-137">HDITEM\_V1\_SIZE</span></span>              | <span data-ttu-id="92671-138">Die Größe der [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) -Struktur in Version 4,0.</span><span class="sxs-lookup"><span data-stu-id="92671-138">The size of the [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure in version 4.0.</span></span>                           |
| <span data-ttu-id="92671-139">Imagelistdrawparameams \_ V3- \_ Größe</span><span class="sxs-lookup"><span data-stu-id="92671-139">IMAGELISTDRAWPARAMS\_V3\_SIZE</span></span> | <span data-ttu-id="92671-140">Die Größe der [**imagelistdrawparameams**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) -Struktur in Version 5,9.</span><span class="sxs-lookup"><span data-stu-id="92671-140">The size of the [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) structure in version 5.9.</span></span> |
| <span data-ttu-id="92671-141">Größe von Pipeline Column \_ v1 \_</span><span class="sxs-lookup"><span data-stu-id="92671-141">LVCOLUMN\_V1\_SIZE</span></span>            | <span data-ttu-id="92671-142">Die Größe der [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) -Struktur in Version 4,0.</span><span class="sxs-lookup"><span data-stu-id="92671-142">The size of the [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure in version 4.0.</span></span>                       |
| <span data-ttu-id="92671-143">Größe der \_ \_ Größe der Größe der Größe</span><span class="sxs-lookup"><span data-stu-id="92671-143">LVGROUP\_V5\_SIZE</span></span>             | <span data-ttu-id="92671-144">Die Größe der Struktur von " [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) " in Version 6,0.</span><span class="sxs-lookup"><span data-stu-id="92671-144">The size of the [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure in version 6.0.</span></span>                         |
| <span data-ttu-id="92671-145">Größe von "lvhittestinfo \_ v1" \_</span><span class="sxs-lookup"><span data-stu-id="92671-145">LVHITTESTINFO\_V1\_SIZE</span></span>       | <span data-ttu-id="92671-146">Die Größe der " [**lvhittestinfo**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) "-Struktur in Version 4,0.</span><span class="sxs-lookup"><span data-stu-id="92671-146">The size of the [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure in version 4.0.</span></span>             |
| <span data-ttu-id="92671-147">Lvitem \_ v1- \_ Größe</span><span class="sxs-lookup"><span data-stu-id="92671-147">LVITEM\_V1\_SIZE</span></span>              | <span data-ttu-id="92671-148">Die Größe der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur in Version 4,0.</span><span class="sxs-lookup"><span data-stu-id="92671-148">The size of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure in version 4.0.</span></span>                           |
| <span data-ttu-id="92671-149">Lvitem \_ V5- \_ Größe</span><span class="sxs-lookup"><span data-stu-id="92671-149">LVITEM\_V5\_SIZE</span></span>              | <span data-ttu-id="92671-150">Die Größe der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur in Version 6,0.</span><span class="sxs-lookup"><span data-stu-id="92671-150">The size of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure in version 6.0.</span></span>                           |
| <span data-ttu-id="92671-151">Größe von "lvtileinfo \_ V5" \_</span><span class="sxs-lookup"><span data-stu-id="92671-151">LVTILEINFO\_V5\_SIZE</span></span>          | <span data-ttu-id="92671-152">Die Größe der " [**lvtileinfo**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) "-Struktur in Version 6,0.</span><span class="sxs-lookup"><span data-stu-id="92671-152">The size of the [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) structure in version 6.0.</span></span>                   |
| <span data-ttu-id="92671-153">MCHITTESTINFO \_ v1- \_ Größe</span><span class="sxs-lookup"><span data-stu-id="92671-153">MCHITTESTINFO\_V1\_SIZE</span></span>       | <span data-ttu-id="92671-154">Die Größe der [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) -Struktur in Version 4,0.</span><span class="sxs-lookup"><span data-stu-id="92671-154">The size of the [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) structure in version 4.0.</span></span>             |
| <span data-ttu-id="92671-155">Nmlvcustomdraw \_ V3- \_ Größe</span><span class="sxs-lookup"><span data-stu-id="92671-155">NMLVCUSTOMDRAW\_V3\_SIZE</span></span>      | <span data-ttu-id="92671-156">Die Größe der [**nmlvcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) -Struktur in Version 4,7.</span><span class="sxs-lookup"><span data-stu-id="92671-156">The size of the [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) structure in version 4.7.</span></span>           |
| <span data-ttu-id="92671-157">Nmttdispinfo \_ v1- \_ Größe</span><span class="sxs-lookup"><span data-stu-id="92671-157">NMTTDISPINFO\_V1\_SIZE</span></span>        | <span data-ttu-id="92671-158">Die Größe der [**nmttdispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) -Struktur in Version 4,0.</span><span class="sxs-lookup"><span data-stu-id="92671-158">The size of the [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure in version 4.0.</span></span>               |
| <span data-ttu-id="92671-159">Nmtvcustomdraw \_ V3- \_ Größe</span><span class="sxs-lookup"><span data-stu-id="92671-159">NMTVCUSTOMDRAW\_V3\_SIZE</span></span>      | <span data-ttu-id="92671-160">Die Größe der [**nmtvcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) -Struktur in Version 4,7.</span><span class="sxs-lookup"><span data-stu-id="92671-160">The size of the [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) structure in version 4.7.</span></span>           |
| <span data-ttu-id="92671-161">Propsheeteader \_ v1- \_ Größe</span><span class="sxs-lookup"><span data-stu-id="92671-161">PROPSHEETHEADER\_V1\_SIZE</span></span>     | <span data-ttu-id="92671-162">Die Größe der [**propsheeteader**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) -Struktur in Version 4,0.</span><span class="sxs-lookup"><span data-stu-id="92671-162">The size of the [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) structure in version 4.0.</span></span>         |
| <span data-ttu-id="92671-163">PROPSHEETPAGE \_ v1- \_ Größe</span><span class="sxs-lookup"><span data-stu-id="92671-163">PROPSHEETPAGE\_V1\_SIZE</span></span>       | <span data-ttu-id="92671-164">Die Größe der [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) -Struktur in Version 4,0.</span><span class="sxs-lookup"><span data-stu-id="92671-164">The size of the [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) structure in version 4.0.</span></span>             |
| <span data-ttu-id="92671-165">REBARBANDINFO \_ V3- \_ Größe</span><span class="sxs-lookup"><span data-stu-id="92671-165">REBARBANDINFO\_V3\_SIZE</span></span>       | <span data-ttu-id="92671-166">Die Größe der [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) -Struktur in Version 4,7.</span><span class="sxs-lookup"><span data-stu-id="92671-166">The size of the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure in version 4.7.</span></span>             |
| <span data-ttu-id="92671-167">REBARBANDINFO \_ V6- \_ Größe</span><span class="sxs-lookup"><span data-stu-id="92671-167">REBARBANDINFO\_V6\_SIZE</span></span>       | <span data-ttu-id="92671-168">Die Größe der [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) -Struktur in Version 6,0.</span><span class="sxs-lookup"><span data-stu-id="92671-168">The size of the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure in version 6.0.</span></span>             |
| <span data-ttu-id="92671-169">Tttoolinfo \_ v1- \_ Größe</span><span class="sxs-lookup"><span data-stu-id="92671-169">TTTOOLINFO\_V1\_SIZE</span></span>          | <span data-ttu-id="92671-170">Die Größe der [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur in Version 4,0.</span><span class="sxs-lookup"><span data-stu-id="92671-170">The size of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure in version 4.0.</span></span>                       |
| <span data-ttu-id="92671-171">Tttoolinfo \_ v2- \_ Größe</span><span class="sxs-lookup"><span data-stu-id="92671-171">TTTOOLINFO\_V2\_SIZE</span></span>          | <span data-ttu-id="92671-172">Die Größe der [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur in Version 4,7.</span><span class="sxs-lookup"><span data-stu-id="92671-172">The size of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure in version 4.7.</span></span>                       |
| <span data-ttu-id="92671-173">Tttoolinfo \_ V3- \_ Größe</span><span class="sxs-lookup"><span data-stu-id="92671-173">TTTOOLINFO\_V3\_SIZE</span></span>          | <span data-ttu-id="92671-174">Die Größe der [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur in Version 6,0.</span><span class="sxs-lookup"><span data-stu-id="92671-174">The size of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure in version 6.0.</span></span>                       |
| <span data-ttu-id="92671-175">TVINSERTSTRUCT \_ v1- \_ Größe</span><span class="sxs-lookup"><span data-stu-id="92671-175">TVINSERTSTRUCT\_V1\_SIZE</span></span>      | <span data-ttu-id="92671-176">Die Größe der [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) -Struktur in Version 4,0.</span><span class="sxs-lookup"><span data-stu-id="92671-176">The size of the [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) structure in version 4.0.</span></span>           |



 

## <a name="using-dllgetversion-to-determine-the-version-number"></a><span data-ttu-id="92671-177">Verwenden von dllgetversion zum Ermitteln der Versionsnummer</span><span class="sxs-lookup"><span data-stu-id="92671-177">Using DllGetVersion to Determine the Version Number</span></span>

<span data-ttu-id="92671-178">Die [**dllgetversion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) -Funktion kann von einer Anwendung aufgerufen werden, um zu bestimmen, welche DLL-Version auf dem System vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="92671-178">The [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) function can be called by an application to determine which DLL version is present on the system.</span></span>

<span data-ttu-id="92671-179">[**Dllgetversion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) gibt eine [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) -Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="92671-179">[**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) returns a [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="92671-180">Zusätzlich zu den Informationen, die über [**dllversioninfo**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo)bereitgestellt werden, stellt **DLLVERSIONINFO2** auch die Hotfixnummer bereit, mit der die neuesten installierten Service Pack identifiziert werden, die eine stabilere Möglichkeit zum Vergleichen von Versionsnummern bietet.</span><span class="sxs-lookup"><span data-stu-id="92671-180">In addition to the information provided through [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo), **DLLVERSIONINFO2** also provides the hotfix number that identifies the latest installed service pack, which provides a more robust way to compare version numbers.</span></span> <span data-ttu-id="92671-181">Da der erste Member von **DLLVERSIONINFO2** eine **dllversioninfo** -Struktur ist, ist die spätere Struktur abwärts kompatibel.</span><span class="sxs-lookup"><span data-stu-id="92671-181">Because the first member of **DLLVERSIONINFO2** is a **DLLVERSIONINFO** structure, the later structure is backward-compatible.</span></span>


<span data-ttu-id="92671-182">Die folgende Beispiel Funktion `GetVersion` lädt eine angegebene DLL und versucht, Ihre [**dllgetversion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) -Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="92671-182">The following sample function `GetVersion` loads a specified DLL and attempts to call its [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) function.</span></span> <span data-ttu-id="92671-183">Wenn erfolgreich, wird ein Makro verwendet, um die Haupt-und neben Versionsnummern aus der [**dllversioninfo**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo) -Struktur in ein **DWORD** zu packen, das an die aufrufenden Anwendung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="92671-183">If successful, it uses a macro to pack the major and minor version numbers from the [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo) structure into a **DWORD** that is returned to the calling application.</span></span> <span data-ttu-id="92671-184">Wenn die DLL **dllgetversion** nicht exportiert, gibt die Funktion 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="92671-184">If the DLL does not export **DllGetVersion**, the function returns zero.</span></span> <span data-ttu-id="92671-185">Sie können die-Funktion ändern, um die Möglichkeit zu behandeln, dass **dllgetversion** eine [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) -Struktur zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="92671-185">You can modify the function to handle the possibility that **DllGetVersion** returns a [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="92671-186">Wenn dies der Fall ist, verwenden Sie die Informationen im **ullversion** -Member der **DLLVERSIONINFO2** -Struktur, um Versionen, Buildnummern und Service Pack Releases zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="92671-186">If so, use the information in that **DLLVERSIONINFO2** structure's **ullVersion** member to compare versions, build numbers, and service pack releases.</span></span> <span data-ttu-id="92671-187">Das [**makedllverull**](/windows/desktop/api/shlwapi/nf-shlwapi-makedllverull) -Makro vereinfacht die Aufgabe, diese Werte mit den Werten in **ullversion** zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="92671-187">The [**MAKEDLLVERULL**](/windows/desktop/api/shlwapi/nf-shlwapi-makedllverull) macro simplifies the task of comparing these values to those in **ullVersion**.</span></span>

> [!Note]  
> <span data-ttu-id="92671-188">Das nicht ordnungsgemäße Verwenden von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann Sicherheitsrisiken darstellen.</span><span class="sxs-lookup"><span data-stu-id="92671-188">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can pose security risks.</span></span> <span data-ttu-id="92671-189">Informationen zum ordnungsgemäßen Laden von DLLs mit unterschiedlichen Versionen von Windows finden Sie in der Dokumentation zu **LoadLibrary** .</span><span class="sxs-lookup"><span data-stu-id="92671-189">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>

 


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



<span data-ttu-id="92671-190">Im folgenden Codebeispiel wird veranschaulicht, wie Sie `GetVersion` mit überprüfen können, ob ComCtl32.dll die Version 6,0 oder höher ist.</span><span class="sxs-lookup"><span data-stu-id="92671-190">The following code example shows how you can use `GetVersion` to test whether ComCtl32.dll is version 6.0 or later.</span></span>


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



## <a name="project-versions"></a><span data-ttu-id="92671-191">Projekt Versionen</span><span class="sxs-lookup"><span data-stu-id="92671-191">Project Versions</span></span>

<span data-ttu-id="92671-192">Um sicherzustellen, dass Ihre Anwendung mit unterschiedlichen Ziel Versionen einer DLL-Datei kompatibel ist, sind Versions Makros in den Header Dateien vorhanden.</span><span class="sxs-lookup"><span data-stu-id="92671-192">To ensure that your application is compatible with different targeted versions of a .dll file, version macros are present in the header files.</span></span> <span data-ttu-id="92671-193">Diese Makros werden verwendet, um bestimmte Definitionen für verschiedene Versionen der dll zu definieren, auszuschließen oder neu zu definieren.</span><span class="sxs-lookup"><span data-stu-id="92671-193">These macros are used to define, exclude, or redefine certain definitions for different versions of the DLL.</span></span> <span data-ttu-id="92671-194">Eine ausführliche Beschreibung dieser Makros finden [Sie unter Verwenden der Windows-Header](/windows/desktop/WinProg/using-the-windows-headers) .</span><span class="sxs-lookup"><span data-stu-id="92671-194">See [Using the Windows Headers](/windows/desktop/WinProg/using-the-windows-headers) for an in-depth description of these macros.</span></span>

<span data-ttu-id="92671-195">Beispielsweise befindet sich der Makro Name **\_ Win32 \_ IE** häufig in älteren Headern.</span><span class="sxs-lookup"><span data-stu-id="92671-195">For example, the macro name **\_WIN32\_IE** is commonly found in older headers.</span></span> <span data-ttu-id="92671-196">Sie sind dafür verantwortlich, das Makro als hexadezimale Zahl zu definieren.</span><span class="sxs-lookup"><span data-stu-id="92671-196">You are responsible for defining the macro as a hexadecimal number.</span></span> <span data-ttu-id="92671-197">Diese Versionsnummer definiert die Zielversion der Anwendung, die die dll verwendet.</span><span class="sxs-lookup"><span data-stu-id="92671-197">This version number defines the target version of the application that is using the DLL.</span></span> <span data-ttu-id="92671-198">In der folgenden Tabelle sind die verfügbaren Versionsnummern und die Auswirkungen der einzelnen Anwendungen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="92671-198">The following table shows the available version numbers and the effect each has on your application.</span></span>



| <span data-ttu-id="92671-199">Version</span><span class="sxs-lookup"><span data-stu-id="92671-199">Version</span></span> | <span data-ttu-id="92671-200">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="92671-200">Description</span></span>                                                                                                                                           |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92671-201">0x0300</span><span class="sxs-lookup"><span data-stu-id="92671-201">0x0300</span></span>  | <span data-ttu-id="92671-202">Die Anwendung ist kompatibel mit ComCtl32.dll Version 4,70 und höher.</span><span class="sxs-lookup"><span data-stu-id="92671-202">The application is compatible with ComCtl32.dll version 4.70 and later.</span></span> <span data-ttu-id="92671-203">Die Anwendung kann keine Features implementieren, die nach Version 4,70 hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="92671-203">The application cannot implement features that were added after version 4.70.</span></span> |
| <span data-ttu-id="92671-204">0x0400</span><span class="sxs-lookup"><span data-stu-id="92671-204">0x0400</span></span>  | <span data-ttu-id="92671-205">Die Anwendung ist kompatibel mit ComCtl32.dll Version 4,71 und höher.</span><span class="sxs-lookup"><span data-stu-id="92671-205">The application is compatible with ComCtl32.dll version 4.71 and later.</span></span> <span data-ttu-id="92671-206">Die Anwendung kann keine Features implementieren, die nach Version 4,71 hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="92671-206">The application cannot implement features that were added after version 4.71.</span></span> |
| <span data-ttu-id="92671-207">0x0401</span><span class="sxs-lookup"><span data-stu-id="92671-207">0x0401</span></span>  | <span data-ttu-id="92671-208">Die Anwendung ist kompatibel mit ComCtl32.dll Version 4,72 und höher.</span><span class="sxs-lookup"><span data-stu-id="92671-208">The application is compatible with ComCtl32.dll version 4.72 and later.</span></span> <span data-ttu-id="92671-209">Die Anwendung kann keine Features implementieren, die nach Version 4,72 hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="92671-209">The application cannot implement features that were added after version 4.72.</span></span> |
| <span data-ttu-id="92671-210">0x0500 sein</span><span class="sxs-lookup"><span data-stu-id="92671-210">0x0500</span></span>  | <span data-ttu-id="92671-211">Die Anwendung ist kompatibel mit ComCtl32.dll Version 5,80 und höher.</span><span class="sxs-lookup"><span data-stu-id="92671-211">The application is compatible with ComCtl32.dll version 5.80 and later.</span></span> <span data-ttu-id="92671-212">Die Anwendung kann keine Features implementieren, die nach Version 5,80 hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="92671-212">The application cannot implement features that were added after version 5.80.</span></span> |
| <span data-ttu-id="92671-213">0x0501</span><span class="sxs-lookup"><span data-stu-id="92671-213">0x0501</span></span>  | <span data-ttu-id="92671-214">Die Anwendung ist kompatibel mit ComCtl32.dll Version 5,81 und höher.</span><span class="sxs-lookup"><span data-stu-id="92671-214">The application is compatible with ComCtl32.dll version 5.81 and later.</span></span> <span data-ttu-id="92671-215">Die Anwendung kann keine Features implementieren, die nach Version 5,81 hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="92671-215">The application cannot implement features that were added after version 5.81.</span></span> |
| <span data-ttu-id="92671-216">0x0600 sein</span><span class="sxs-lookup"><span data-stu-id="92671-216">0x0600</span></span>  | <span data-ttu-id="92671-217">Die Anwendung ist kompatibel mit ComCtl32.dll Version 6,0 und höher.</span><span class="sxs-lookup"><span data-stu-id="92671-217">The application is compatible with ComCtl32.dll version 6.0 and later.</span></span> <span data-ttu-id="92671-218">Die Anwendung kann keine Features implementieren, die nach Version 6,0 hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="92671-218">The application cannot implement features that were added after version 6.0.</span></span>   |



 

<span data-ttu-id="92671-219">Wenn Sie das **\_ Win32- \_ IE** -Makro nicht in Ihrem Projekt definieren, wird es automatisch als 0x0500 definiert.</span><span class="sxs-lookup"><span data-stu-id="92671-219">If you do not define the **\_WIN32\_IE** macro in your project, it is automatically defined as 0x0500.</span></span> <span data-ttu-id="92671-220">Wenn Sie einen anderen Wert definieren möchten, können Sie den Compilerdirektiven in ihrer Make-Datei Folgendes hinzufügen: Ersetzen Sie die gewünschte Versionsnummer für 0x0400.</span><span class="sxs-lookup"><span data-stu-id="92671-220">To define a different value, you can add the following to the compiler directives in your make file; substitute the desired version number for 0x0400.</span></span>


```C++
/D _WIN32_IE=0x0400
```



<span data-ttu-id="92671-221">Eine andere Methode ist das Hinzufügen einer Zeile ähnlich der folgenden in Ihrem Quellcode, bevor Sie die shellheaderdateien einschließen.</span><span class="sxs-lookup"><span data-stu-id="92671-221">Another method is to add a line similar to the following in your source code before you include the Shell header files.</span></span> <span data-ttu-id="92671-222">Ersetzen Sie die gewünschte Versionsnummer für 0x0400.</span><span class="sxs-lookup"><span data-stu-id="92671-222">Substitute the desired version number for 0x0400.</span></span>


```C++
#define _WIN32_IE 0x0400
#include <commctrl.h>
```



## <a name="related-topics"></a><span data-ttu-id="92671-223">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="92671-223">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92671-224">Informationen zu allgemeinen Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="92671-224">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 