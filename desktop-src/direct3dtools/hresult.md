---
description: Benutzerdefinierte HRESULT-Werte für die Schnittstelle zur Grafik Diagnose Erfassung.
MS-HAID: vspixengine.Hresult
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: HRESULT-Enumeration
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 246FA53F-FF5B-44E1-BABB-F45AE0212687
api_name:
- Hresult
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3d5419feb0acb5967132fbb804a9bbc11bfa4248
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521568"
---
# <a name="span-idvspixenginehresultspanhresult-enumeration"></a><span data-ttu-id="cad1d-103"><span id="vspixengine.hresult"></span>HRESULT-Enumeration</span><span class="sxs-lookup"><span data-stu-id="cad1d-103"><span id="vspixengine.hresult"></span>Hresult enumeration</span></span>

<span data-ttu-id="cad1d-104">Benutzerdefinierte HRESULT-Werte für die Schnittstelle zur Grafik Diagnose Erfassung.</span><span class="sxs-lookup"><span data-stu-id="cad1d-104">Custom HRESULT values for the graphics diagnostics capture interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="cad1d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cad1d-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="cad1d-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="cad1d-106">Constants</span></span>

<span data-ttu-id="cad1d-107"><span id="PIX_S_OK"></span><span id="pix_s_ok"></span>**Pix \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="cad1d-107"><span id="PIX_S_OK"></span><span id="pix_s_ok"></span>**PIX\_S\_OK**</span></span>  
<span data-ttu-id="cad1d-108">Ein gängiges HRESULT, das angibt, dass der Vorgang erwartungsgemäß erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="cad1d-108">A common HRESULT which indicates that the operation succeeded as expected.</span></span>

<span data-ttu-id="cad1d-109"><span id="PIX_S_FALSE"></span><span id="pix_s_false"></span>**Pix \_ S \_ false**</span><span class="sxs-lookup"><span data-stu-id="cad1d-109"><span id="PIX_S_FALSE"></span><span id="pix_s_false"></span>**PIX\_S\_FALSE**</span></span>  
<span data-ttu-id="cad1d-110">Ein gängiges HRESULT, das angibt, dass der Vorgang erfolgreich war, jedoch anders als erwartet.</span><span class="sxs-lookup"><span data-stu-id="cad1d-110">A common HRESULT which indicates that the operation succeeded, but in a different way than was expected.</span></span>

<span data-ttu-id="cad1d-111"><span id="PIX_ERROR_FILE_NOT_FOUND"></span><span id="pix_error_file_not_found"></span>**Pix- \_ Fehler \_ Datei \_ nicht \_ gefunden**</span><span class="sxs-lookup"><span data-stu-id="cad1d-111"><span id="PIX_ERROR_FILE_NOT_FOUND"></span><span id="pix_error_file_not_found"></span>**PIX\_ERROR\_FILE\_NOT\_FOUND**</span></span>  
<span data-ttu-id="cad1d-112">Ein benutzerdefiniertes HRESULT, dass die Fehler \_ Datei " \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cad1d-112">A custom HRESULT that echos ERROR\_FILE\_NOT\_FOUND.</span></span>

<span data-ttu-id="cad1d-113"><span id="PIX_ERROR_BAD_ENVIRONMENT"></span><span id="pix_error_bad_environment"></span>**Pix- \_ fehlerhafte \_ \_ Umgebung**</span><span class="sxs-lookup"><span data-stu-id="cad1d-113"><span id="PIX_ERROR_BAD_ENVIRONMENT"></span><span id="pix_error_bad_environment"></span>**PIX\_ERROR\_BAD\_ENVIRONMENT**</span></span>  
<span data-ttu-id="cad1d-114">Ein benutzerdefiniertes HRESULT, das auf eine ungültige Umgebung für Fehler \_ \_</span><span class="sxs-lookup"><span data-stu-id="cad1d-114">A custom HRESULT that echos ERROR\_BAD\_ENVIRONMENT.</span></span>

<span data-ttu-id="cad1d-115"><span id="PIX_ERROR_BAD_FORMAT"></span><span id="pix_error_bad_format"></span>**Pix \_ - \_ Fehler \_ Format**</span><span class="sxs-lookup"><span data-stu-id="cad1d-115"><span id="PIX_ERROR_BAD_FORMAT"></span><span id="pix_error_bad_format"></span>**PIX\_ERROR\_BAD\_FORMAT**</span></span>  
<span data-ttu-id="cad1d-116">Ein benutzerdefiniertes HRESULT, das ein ungültiges Format für den Fehler \_ \_</span><span class="sxs-lookup"><span data-stu-id="cad1d-116">A custom HRESULT that echos ERROR\_BAD\_FORMAT.</span></span>

<span data-ttu-id="cad1d-117"><span id="PIX_ERROR_SHARING_VIOLATION"></span><span id="pix_error_sharing_violation"></span>**Pix- \_ Fehler \_ Freigabe \_ Verletzung**</span><span class="sxs-lookup"><span data-stu-id="cad1d-117"><span id="PIX_ERROR_SHARING_VIOLATION"></span><span id="pix_error_sharing_violation"></span>**PIX\_ERROR\_SHARING\_VIOLATION**</span></span>  
<span data-ttu-id="cad1d-118">Ein benutzerdefiniertes HRESULT, bei dem die Verletzung der Fehler \_ Freigabe " \_</span><span class="sxs-lookup"><span data-stu-id="cad1d-118">A custom HRESULT that echos ERROR\_SHARING\_VIOLATION.</span></span>

<span data-ttu-id="cad1d-119"><span id="PIX_ERROR_DISK_FULL"></span><span id="pix_error_disk_full"></span>**Pix-Fehler Datenträger \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cad1d-119"><span id="PIX_ERROR_DISK_FULL"></span><span id="pix_error_disk_full"></span>**PIX\_ERROR\_DISK\_FULL**</span></span>  
<span data-ttu-id="cad1d-120">Ein benutzerdefiniertes HRESULT, das den Fehler Datenträger \_ \_ voll ist.</span><span class="sxs-lookup"><span data-stu-id="cad1d-120">A custom HRESULT that echos ERROR\_DISK\_FULL.</span></span>

<span data-ttu-id="cad1d-121"><span id="PIX_ERROR_MORE_DATA"></span><span id="pix_error_more_data"></span>**Pix- \_ Fehler \_ Weitere \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="cad1d-121"><span id="PIX_ERROR_MORE_DATA"></span><span id="pix_error_more_data"></span>**PIX\_ERROR\_MORE\_DATA**</span></span>  
<span data-ttu-id="cad1d-122">Ein benutzerdefiniertes HRESULT, bei dem \_ ein Fehler mit einem Fehler bei \_</span><span class="sxs-lookup"><span data-stu-id="cad1d-122">A custom HRESULT that echos ERROR\_MORE\_DATA.</span></span>

<span data-ttu-id="cad1d-123"><span id="PIX_E_MISSING_DEBUG_KITS_POLICY"></span><span id="pix_e_missing_debug_kits_policy"></span>**Pix \_ E \_ fehlende \_ Debug- \_ Kits- \_ Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="cad1d-123"><span id="PIX_E_MISSING_DEBUG_KITS_POLICY"></span><span id="pix_e_missing_debug_kits_policy"></span>**PIX\_E\_MISSING\_DEBUG\_KITS\_POLICY**</span></span>  
<span data-ttu-id="cad1d-124">Ein benutzerdefiniertes HRESULT, das angibt, dass die Debug Kits-Richtlinie fehlt.</span><span class="sxs-lookup"><span data-stu-id="cad1d-124">A custom HRESULT which indicates that the Debug Kits policy is missing.</span></span>

<span data-ttu-id="cad1d-125"><span id="PIX_E_INVALID_VERSION"></span><span id="pix_e_invalid_version"></span>**Pix \_ E \_ ungültige \_ Version.**</span><span class="sxs-lookup"><span data-stu-id="cad1d-125"><span id="PIX_E_INVALID_VERSION"></span><span id="pix_e_invalid_version"></span>**PIX\_E\_INVALID\_VERSION**</span></span>  
<span data-ttu-id="cad1d-126">Ein benutzerdefiniertes HRESULT, das angibt, dass eine ungültige Version verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cad1d-126">A custom HRESULT which indicates that an invalid version is being used.</span></span>

<span data-ttu-id="cad1d-127"><span id="PIX_E_USING_DCOMP"></span><span id="pix_e_using_dcomp"></span>**Pix \_ E \_ mit \_ Dcomp**</span><span class="sxs-lookup"><span data-stu-id="cad1d-127"><span id="PIX_E_USING_DCOMP"></span><span id="pix_e_using_dcomp"></span>**PIX\_E\_USING\_DCOMP**</span></span>  
<span data-ttu-id="cad1d-128">Ein benutzerdefiniertes HRESULT, das angibt, dass directcomposition verwendet wird (die Erfassung von directcomposition wird nicht unterstützt.)</span><span class="sxs-lookup"><span data-stu-id="cad1d-128">A custom HRESULT which indicates that DirectComposition is in use (capture of DirectComposition is not supported.)</span></span>

<span data-ttu-id="cad1d-129"><span id="PIX_E_USING_DIRECTWRITE"></span><span id="pix_e_using_directwrite"></span>**Pix \_ E \_ mithilfe von \_ DirectWrite**</span><span class="sxs-lookup"><span data-stu-id="cad1d-129"><span id="PIX_E_USING_DIRECTWRITE"></span><span id="pix_e_using_directwrite"></span>**PIX\_E\_USING\_DIRECTWRITE**</span></span>  
<span data-ttu-id="cad1d-130">Ein benutzerdefiniertes HRESULT, das angibt, dass DirectWrite verwendet wird (die Erfassung von DirectWrite wird nicht unterstützt.)</span><span class="sxs-lookup"><span data-stu-id="cad1d-130">A custom HRESULT which indicates that DirectWrite is in use (capture of DirectWrite is not supported.)</span></span>

<span data-ttu-id="cad1d-131"><span id="PIX_E_USING_D3D9"></span><span id="pix_e_using_d3d9"></span>**Pix \_ E \_ mithilfe von \_ d3d9**</span><span class="sxs-lookup"><span data-stu-id="cad1d-131"><span id="PIX_E_USING_D3D9"></span><span id="pix_e_using_d3d9"></span>**PIX\_E\_USING\_D3D9**</span></span>  
<span data-ttu-id="cad1d-132">Ein benutzerdefiniertes HRESULT, das angibt, dass von Direct3D9 verwendet wird (die Erfassung von von Direct3D9 wird in Windows 10 nicht unterstützt.)</span><span class="sxs-lookup"><span data-stu-id="cad1d-132">A custom HRESULT which indicates that Direct3D9 is in use (capture of Direct3D9 is not supported in Windows 10.)</span></span>

<span data-ttu-id="cad1d-133"><span id="PIX_E_CANT_CREATE_SHADER"></span><span id="pix_e_cant_create_shader"></span>**Pix \_ E nicht zum \_ Erstellen eines \_ \_ Shaders**</span><span class="sxs-lookup"><span data-stu-id="cad1d-133"><span id="PIX_E_CANT_CREATE_SHADER"></span><span id="pix_e_cant_create_shader"></span>**PIX\_E\_CANT\_CREATE\_SHADER**</span></span>  
<span data-ttu-id="cad1d-134">Ein benutzerdefiniertes HRESULT, das angibt, dass ein angegebener Shader nicht erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cad1d-134">A custom HRESULT which indicates that a specified shader can't be created.</span></span>

<span data-ttu-id="cad1d-135"><span id="PIX_E_USING_D2D"></span><span id="pix_e_using_d2d"></span>**Pix \_ E \_ mithilfe von \_ D2D**</span><span class="sxs-lookup"><span data-stu-id="cad1d-135"><span id="PIX_E_USING_D2D"></span><span id="pix_e_using_d2d"></span>**PIX\_E\_USING\_D2D**</span></span>  
<span data-ttu-id="cad1d-136">Ein benutzerdefiniertes HRESULT, das angibt, dass Direct2D verwendet wird (die Erfassung von Direct2D wird nicht unterstützt.)</span><span class="sxs-lookup"><span data-stu-id="cad1d-136">A custom HRESULT which indicates that Direct2D is in use (capture of Direct2D is not supported.)</span></span>

<span data-ttu-id="cad1d-137"><span id="PIX_E_NO_FRAMES"></span><span id="pix_e_no_frames"></span>**Pix \_ E \_ keine \_ Frames**</span><span class="sxs-lookup"><span data-stu-id="cad1d-137"><span id="PIX_E_NO_FRAMES"></span><span id="pix_e_no_frames"></span>**PIX\_E\_NO\_FRAMES**</span></span>  
<span data-ttu-id="cad1d-138">Ein benutzerdefiniertes HRESULT, das angibt, dass keine Frames aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="cad1d-138">A custom HRESULT which indicates that no frames have been captured.</span></span>

<span data-ttu-id="cad1d-139"><span id="PIX_E_DISABLE_SPY"></span><span id="pix_e_disable_spy"></span>**Pix \_ E \_ Deaktivieren von \_ Spy**</span><span class="sxs-lookup"><span data-stu-id="cad1d-139"><span id="PIX_E_DISABLE_SPY"></span><span id="pix_e_disable_spy"></span>**PIX\_E\_DISABLE\_SPY**</span></span>  

<span data-ttu-id="cad1d-140"><span id="PIX_E_WIN8LOG_ON_WIN7"></span><span id="pix_e_win8log_on_win7"></span>**Pix \_ E \_ WIN8LOG \_ auf \_ Win7**</span><span class="sxs-lookup"><span data-stu-id="cad1d-140"><span id="PIX_E_WIN8LOG_ON_WIN7"></span><span id="pix_e_win8log_on_win7"></span>**PIX\_E\_WIN8LOG\_ON\_WIN7**</span></span>  
<span data-ttu-id="cad1d-141">Ein benutzerdefiniertes HRESULT, das angibt, dass ein Windows 8 vsglog auf Windows 7 nicht wiedergegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="cad1d-141">A custom HRESULT which indicates that a Windows 8 vsglog cannot be played back on Windows 7.</span></span>

<span data-ttu-id="cad1d-142"><span id="PIX_E_BUILD_SHADER_TRACE"></span><span id="pix_e_build_shader_trace"></span>**Pix \_ E \_ Build- \_ Shader-Ablauf \_ Verfolgung**</span><span class="sxs-lookup"><span data-stu-id="cad1d-142"><span id="PIX_E_BUILD_SHADER_TRACE"></span><span id="pix_e_build_shader_trace"></span>**PIX\_E\_BUILD\_SHADER\_TRACE**</span></span>  
<span data-ttu-id="cad1d-143">Ein benutzerdefiniertes HRESULT, das angibt, dass beim Aufbau der shaderablaufverfolgung ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="cad1d-143">A custom HRESULT which indicates that there was an error building the shader trace.</span></span>

<span data-ttu-id="cad1d-144"><span id="PIX_E_NO_CS_DATA_VISUALIZATION"></span><span id="pix_e_no_cs_data_visualization"></span>**Pix \_ E \_ keine \_ CS- \_ Daten \_ Visualisierung**</span><span class="sxs-lookup"><span data-stu-id="cad1d-144"><span id="PIX_E_NO_CS_DATA_VISUALIZATION"></span><span id="pix_e_no_cs_data_visualization"></span>**PIX\_E\_NO\_CS\_DATA\_VISUALIZATION**</span></span>  
<span data-ttu-id="cad1d-145">Ein benutzerdefiniertes HRESULT, das angibt, dass keine Datenvisualisierung für Compute-Shader vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="cad1d-145">A custom HRESULT which indicates that there is no compute shader data visualization.</span></span>

<span data-ttu-id="cad1d-146"><span id="PIX_E_MISMATCH_SDK"></span><span id="pix_e_mismatch_sdk"></span>**Pix \_ E \_ Mismatch \_ SDK**</span><span class="sxs-lookup"><span data-stu-id="cad1d-146"><span id="PIX_E_MISMATCH_SDK"></span><span id="pix_e_mismatch_sdk"></span>**PIX\_E\_MISMATCH\_SDK**</span></span>  
<span data-ttu-id="cad1d-147">Ein benutzerdefiniertes HRESULT, das angibt, dass das aktuelle SDK nicht übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="cad1d-147">A custom HRESULT which indicates that there is a mismatch with the current SDK.</span></span>

<span data-ttu-id="cad1d-148"><span id="PIX_E_POSSIBLE_MISMATCH_SDK"></span><span id="pix_e_possible_mismatch_sdk"></span>**Pix \_ E möglicherweise nicht übereinstimmende \_ \_ \_ SDK**</span><span class="sxs-lookup"><span data-stu-id="cad1d-148"><span id="PIX_E_POSSIBLE_MISMATCH_SDK"></span><span id="pix_e_possible_mismatch_sdk"></span>**PIX\_E\_POSSIBLE\_MISMATCH\_SDK**</span></span>  
<span data-ttu-id="cad1d-149">Ein benutzerdefiniertes HRESULT, das angibt, dass eine mögliche Übereinstimmung mit dem aktuellen SDK vorliegt.</span><span class="sxs-lookup"><span data-stu-id="cad1d-149">A custom HRESULT which indicates that there is a possible mismatch with the current SDK.</span></span>

<span data-ttu-id="cad1d-150"><span id="PIX_E_UNDETECTABLE_PIXEL"></span><span id="pix_e_undetectable_pixel"></span>**Pix \_ E \_ nicht erkennbares \_ Pixel**</span><span class="sxs-lookup"><span data-stu-id="cad1d-150"><span id="PIX_E_UNDETECTABLE_PIXEL"></span><span id="pix_e_undetectable_pixel"></span>**PIX\_E\_UNDETECTABLE\_PIXEL**</span></span>  
<span data-ttu-id="cad1d-151">Ein benutzerdefiniertes HRESULT, das angibt, dass ein nicht erkennbares Pixel vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="cad1d-151">A custom HRESULT which indicates that there is an undetectable pixel.</span></span>

<span data-ttu-id="cad1d-152"><span id="PIX_E_CANT_DEBUG_SHADER_USING_SYSTEM_VALUE_SEMANTICS"></span><span id="pix_e_cant_debug_shader_using_system_value_semantics"></span>**Pix \_ E \_ cant \_ Debuggen von \_ Shader \_ mithilfe von \_ System \_ Wert \_ Semantik**</span><span class="sxs-lookup"><span data-stu-id="cad1d-152"><span id="PIX_E_CANT_DEBUG_SHADER_USING_SYSTEM_VALUE_SEMANTICS"></span><span id="pix_e_cant_debug_shader_using_system_value_semantics"></span>**PIX\_E\_CANT\_DEBUG\_SHADER\_USING\_SYSTEM\_VALUE\_SEMANTICS**</span></span>  
<span data-ttu-id="cad1d-153">Ein benutzerdefiniertes HRESULT, das angibt, dass der sahder nicht mithilfe der System Wert Semantik debuggten werden kann.</span><span class="sxs-lookup"><span data-stu-id="cad1d-153">A custom HRESULT which indicates that the sahder can't be debugged using system value semantics.</span></span>

<span data-ttu-id="cad1d-154"><span id="PIX_S_UPDATEAVAILABLE"></span><span id="pix_s_updateavailable"></span>**Pix \_ S \_ UpdateAvailable**</span><span class="sxs-lookup"><span data-stu-id="cad1d-154"><span id="PIX_S_UPDATEAVAILABLE"></span><span id="pix_s_updateavailable"></span>**PIX\_S\_UPDATEAVAILABLE**</span></span>  
<span data-ttu-id="cad1d-155">Ein benutzerdefiniertes HRESULT, das angibt, dass ein Update verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="cad1d-155">A custom HRESULT which indicates that there is an update available.</span></span>

<span data-ttu-id="cad1d-156"><span id="PIX_DXGI_STATUS_NO_REDIRECTION"></span><span id="pix_dxgi_status_no_redirection"></span>**Pix \_ DXGI- \_ Status \_ keine \_ Umleitung**</span><span class="sxs-lookup"><span data-stu-id="cad1d-156"><span id="PIX_DXGI_STATUS_NO_REDIRECTION"></span><span id="pix_dxgi_status_no_redirection"></span>**PIX\_DXGI\_STATUS\_NO\_REDIRECTION**</span></span>  
<span data-ttu-id="cad1d-157">Ein benutzerdefiniertes HRESULT, für das der DXGI- \_ Status \_ keine \_ Umleitung hat.</span><span class="sxs-lookup"><span data-stu-id="cad1d-157">A custom HRESULT that echos DXGI\_STATUS\_NO\_REDIRECTION.</span></span>

<span data-ttu-id="cad1d-158"><span id="PIX_DXGI_STATUS_NO_DESKTOP_ACCESS"></span><span id="pix_dxgi_status_no_desktop_access"></span>**Pix \_ DXGI \_ \_ -Status ohne \_ Desktop \_ Zugriff**</span><span class="sxs-lookup"><span data-stu-id="cad1d-158"><span id="PIX_DXGI_STATUS_NO_DESKTOP_ACCESS"></span><span id="pix_dxgi_status_no_desktop_access"></span>**PIX\_DXGI\_STATUS\_NO\_DESKTOP\_ACCESS**</span></span>  
<span data-ttu-id="cad1d-159">Ein benutzerdefiniertes HRESULT, das für den DXGI \_ \_ -Status keinen \_ Desktop \_ Zugriff hat.</span><span class="sxs-lookup"><span data-stu-id="cad1d-159">A custom HRESULT that echos DXGI\_STATUS\_NO\_DESKTOP\_ACCESS.</span></span>

<span data-ttu-id="cad1d-160"><span id="PIX_DXGI_STATUS_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_status_graphics_vidpn_source_in_use"></span>**Pix- \_ DXGI- \_ Status \_ Grafik \_ VidPN- \_ Quelle wird \_ \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="cad1d-160"><span id="PIX_DXGI_STATUS_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_status_graphics_vidpn_source_in_use"></span>**PIX\_DXGI\_STATUS\_GRAPHICS\_VIDPN\_SOURCE\_IN\_USE**</span></span>  
<span data-ttu-id="cad1d-161">Ein benutzerdefiniertes HRESULT, das von der in Verwendung von Echos DXGI- \_ Status \_ Grafik \_ VidPN \_ \_ \_ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="cad1d-161">A custom HRESULT that echos DXGI\_STATUS\_GRAPHICS\_VIDPN\_SOURCE\_IN\_USE.</span></span>

<span data-ttu-id="cad1d-162"><span id="PIX_DXGI_STATUS_MODE_CHANGED"></span><span id="pix_dxgi_status_mode_changed"></span>**Pix \_ DXGI- \_ Status \_ Modus \_ geändert**</span><span class="sxs-lookup"><span data-stu-id="cad1d-162"><span id="PIX_DXGI_STATUS_MODE_CHANGED"></span><span id="pix_dxgi_status_mode_changed"></span>**PIX\_DXGI\_STATUS\_MODE\_CHANGED**</span></span>  
<span data-ttu-id="cad1d-163">Ein benutzerdefiniertes HRESULT, für das der \_ Status Modus von " \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cad1d-163">A custom HRESULT that echos DXGI\_STATUS\_MODE\_CHANGED.</span></span>

<span data-ttu-id="cad1d-164"><span id="PIX_DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_status_mode_change_in_progress"></span>**\_ \_ Status \_ Modus \_ \_ für \_ pix DXGI-Status wird geändert**</span><span class="sxs-lookup"><span data-stu-id="cad1d-164"><span id="PIX_DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_status_mode_change_in_progress"></span>**PIX\_DXGI\_STATUS\_MODE\_CHANGE\_IN\_PROGRESS**</span></span>  
<span data-ttu-id="cad1d-165">Ein benutzerdefiniertes HRESULT, in dem der Status Modus für den DXGI- \_ Status \_ geändert wird \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cad1d-165">A custom HRESULT that echos DXGI\_STATUS\_MODE\_CHANGE\_IN\_PROGRESS.</span></span>

<span data-ttu-id="cad1d-166"><span id="PIX_DXGI_STATUS_UNOCCLUDED"></span><span id="pix_dxgi_status_unoccluded"></span>**Pix \_ DXGI- \_ Status wurde \_ aufgehoben**</span><span class="sxs-lookup"><span data-stu-id="cad1d-166"><span id="PIX_DXGI_STATUS_UNOCCLUDED"></span><span id="pix_dxgi_status_unoccluded"></span>**PIX\_DXGI\_STATUS\_UNOCCLUDED**</span></span>  
<span data-ttu-id="cad1d-167">Ein benutzerdefiniertes HRESULT, das den DXGI- \_ Status " \_ aufgehoben" hat.</span><span class="sxs-lookup"><span data-stu-id="cad1d-167">A custom HRESULT that echos DXGI\_STATUS\_UNOCCLUDED.</span></span>

<span data-ttu-id="cad1d-168"><span id="PIX_DXGI_STATUS_DDA_WAS_STILL_DRAWING"></span><span id="pix_dxgi_status_dda_was_still_drawing"></span>**Pix \_ DXGI- \_ Status- \_ DDA \_ wurde \_ immer noch \_ gezeichnet.**</span><span class="sxs-lookup"><span data-stu-id="cad1d-168"><span id="PIX_DXGI_STATUS_DDA_WAS_STILL_DRAWING"></span><span id="pix_dxgi_status_dda_was_still_drawing"></span>**PIX\_DXGI\_STATUS\_DDA\_WAS\_STILL\_DRAWING**</span></span>  
<span data-ttu-id="cad1d-169">Ein benutzerdefiniertes HRESULT, das der DXGI- \_ Status- \_ DDA \_ \_ nach wie vor \_ zeichnet.</span><span class="sxs-lookup"><span data-stu-id="cad1d-169">A custom HRESULT that echos DXGI\_STATUS\_DDA\_WAS\_STILL\_DRAWING.</span></span>

<span data-ttu-id="cad1d-170"><span id="PIX_E_NOTIMPL"></span><span id="pix_e_notimpl"></span>**Pix \_ E \_ notimpl**</span><span class="sxs-lookup"><span data-stu-id="cad1d-170"><span id="PIX_E_NOTIMPL"></span><span id="pix_e_notimpl"></span>**PIX\_E\_NOTIMPL**</span></span>  
<span data-ttu-id="cad1d-171">Ein benutzerdefiniertes HRESULT, das von der Meldung E benachrichtigt wird \_ .</span><span class="sxs-lookup"><span data-stu-id="cad1d-171">A custom HRESULT that echos E\_NOTIMPL.</span></span>

<span data-ttu-id="cad1d-172"><span id="PIX_E_NOINTERFACE"></span><span id="pix_e_nointerface"></span>**Pix \_ E \_ nointerface**</span><span class="sxs-lookup"><span data-stu-id="cad1d-172"><span id="PIX_E_NOINTERFACE"></span><span id="pix_e_nointerface"></span>**PIX\_E\_NOINTERFACE**</span></span>  
<span data-ttu-id="cad1d-173">Ein benutzerdefiniertes HRESULT, das auf " \_ nointerface" fest.</span><span class="sxs-lookup"><span data-stu-id="cad1d-173">A custom HRESULT that echos E\_NOINTERFACE.</span></span>

<span data-ttu-id="cad1d-174"><span id="PIX_E_POINTER"></span><span id="pix_e_pointer"></span>**Pix \_ E- \_ Zeiger**</span><span class="sxs-lookup"><span data-stu-id="cad1d-174"><span id="PIX_E_POINTER"></span><span id="pix_e_pointer"></span>**PIX\_E\_POINTER**</span></span>  
<span data-ttu-id="cad1d-175">Ein benutzerdefiniertes HRESULT, das einen Zeiger auf einen \_ Zeiger hat</span><span class="sxs-lookup"><span data-stu-id="cad1d-175">A custom HRESULT that echos E\_POINTER.</span></span>

<span data-ttu-id="cad1d-176"><span id="PIX_E_ABORT"></span><span id="pix_e_abort"></span>**Pix \_ E \_ Abbrechen**</span><span class="sxs-lookup"><span data-stu-id="cad1d-176"><span id="PIX_E_ABORT"></span><span id="pix_e_abort"></span>**PIX\_E\_ABORT**</span></span>  
<span data-ttu-id="cad1d-177">Ein benutzerdefiniertes HRESULT, das den \_ Abbruch abbricht.</span><span class="sxs-lookup"><span data-stu-id="cad1d-177">A custom HRESULT that echos E\_ABORT.</span></span>

<span data-ttu-id="cad1d-178"><span id="PIX_E_FAIL"></span><span id="pix_e_fail"></span>**Pix \_ E \_ schlägt fehl**</span><span class="sxs-lookup"><span data-stu-id="cad1d-178"><span id="PIX_E_FAIL"></span><span id="pix_e_fail"></span>**PIX\_E\_FAIL**</span></span>  
<span data-ttu-id="cad1d-179">Ein benutzerdefiniertes HRESULT, bei dem ein Fehler auftritt \_ .</span><span class="sxs-lookup"><span data-stu-id="cad1d-179">A custom HRESULT that echos E\_FAIL.</span></span>

<span data-ttu-id="cad1d-180"><span id="PIX_E_UNEXPECTED"></span><span id="pix_e_unexpected"></span>**Pix \_ E \_ unerwartet**</span><span class="sxs-lookup"><span data-stu-id="cad1d-180"><span id="PIX_E_UNEXPECTED"></span><span id="pix_e_unexpected"></span>**PIX\_E\_UNEXPECTED**</span></span>  
<span data-ttu-id="cad1d-181">Ein benutzerdefiniertes HRESULT, das von Echos E \_ unerwartet ist.</span><span class="sxs-lookup"><span data-stu-id="cad1d-181">A custom HRESULT that echos E\_UNEXPECTED.</span></span>

<span data-ttu-id="cad1d-182"><span id="PIX_E_ACCESSDENIED"></span><span id="pix_e_accessdenied"></span>**Pix \_ E \_ AccessDenied**</span><span class="sxs-lookup"><span data-stu-id="cad1d-182"><span id="PIX_E_ACCESSDENIED"></span><span id="pix_e_accessdenied"></span>**PIX\_E\_ACCESSDENIED**</span></span>  
<span data-ttu-id="cad1d-183">Ein benutzerdefiniertes HRESULT, auf das der Zugriff \_ verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="cad1d-183">A custom HRESULT that echos E\_ACCESSDENIED.</span></span>

<span data-ttu-id="cad1d-184"><span id="PIX_E_HANDLE"></span><span id="pix_e_handle"></span>**Pix- \_ E- \_ handle**</span><span class="sxs-lookup"><span data-stu-id="cad1d-184"><span id="PIX_E_HANDLE"></span><span id="pix_e_handle"></span>**PIX\_E\_HANDLE**</span></span>  
<span data-ttu-id="cad1d-185">Ein benutzerdefiniertes HRESULT, das mit dem-Wert von " \_</span><span class="sxs-lookup"><span data-stu-id="cad1d-185">A custom HRESULT that echos E\_HANDLE.</span></span>

<span data-ttu-id="cad1d-186"><span id="PIX_E_OUTOFMEMORY"></span><span id="pix_e_outofmemory"></span>**Pix \_ E \_ outo-Memory**</span><span class="sxs-lookup"><span data-stu-id="cad1d-186"><span id="PIX_E_OUTOFMEMORY"></span><span id="pix_e_outofmemory"></span>**PIX\_E\_OUTOFMEMORY**</span></span>  
<span data-ttu-id="cad1d-187">Ein benutzerdefiniertes HRESULT, das auf den Wert von \_ outo-Memory zurückgeht</span><span class="sxs-lookup"><span data-stu-id="cad1d-187">A custom HRESULT that echos E\_OUTOFMEMORY.</span></span>

<span data-ttu-id="cad1d-188"><span id="PIX_E_INVALIDARG"></span><span id="pix_e_invalidarg"></span>**Pix \_ E \_ invalidArg**</span><span class="sxs-lookup"><span data-stu-id="cad1d-188"><span id="PIX_E_INVALIDARG"></span><span id="pix_e_invalidarg"></span>**PIX\_E\_INVALIDARG**</span></span>  
<span data-ttu-id="cad1d-189">Ein benutzerdefiniertes HRESULT, das auf \_ invalidArg steht.</span><span class="sxs-lookup"><span data-stu-id="cad1d-189">A custom HRESULT that echos E\_INVALIDARG.</span></span>

<span data-ttu-id="cad1d-190"><span id="PIX_XBOX_ERROR_DISK_FULL"></span><span id="pix_xbox_error_disk_full"></span>**Pix Xbox Fehler Datenträger \_ \_ \_ \_ voll**</span><span class="sxs-lookup"><span data-stu-id="cad1d-190"><span id="PIX_XBOX_ERROR_DISK_FULL"></span><span id="pix_xbox_error_disk_full"></span>**PIX\_XBOX\_ERROR\_DISK\_FULL**</span></span>  
<span data-ttu-id="cad1d-191">Ein benutzerdefiniertes HRESULT, das angibt, dass der Datenträger voll ist.</span><span class="sxs-lookup"><span data-stu-id="cad1d-191">A custom HRESULT which indicates that the disk is full.</span></span>

<span data-ttu-id="cad1d-192"><span id="PIX_WS_E_ADDRESS_IN_USE"></span><span id="pix_ws_e_address_in_use"></span>**Pix \_ WS \_ E \_ Adresse \_ in \_ Verwendung**</span><span class="sxs-lookup"><span data-stu-id="cad1d-192"><span id="PIX_WS_E_ADDRESS_IN_USE"></span><span id="pix_ws_e_address_in_use"></span>**PIX\_WS\_E\_ADDRESS\_IN\_USE**</span></span>  
<span data-ttu-id="cad1d-193">Ein benutzerdefiniertes HRESULT, das angibt, dass die Adresse bereits verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cad1d-193">A custom HRESULT which indicates that the address is already in use.</span></span>

<span data-ttu-id="cad1d-194"><span id="PIX_WS_E_MISSING_KITS_POLICY"></span><span id="pix_ws_e_missing_kits_policy"></span>**Pix \_ WS \_ E \_ - \_ Richtlinie für fehlende Kits \_**</span><span class="sxs-lookup"><span data-stu-id="cad1d-194"><span id="PIX_WS_E_MISSING_KITS_POLICY"></span><span id="pix_ws_e_missing_kits_policy"></span>**PIX\_WS\_E\_MISSING\_KITS\_POLICY**</span></span>  
<span data-ttu-id="cad1d-195">Ein benutzerdefiniertes HRESULT, das angibt, dass die Adresse nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="cad1d-195">A custom HRESULT which indicates that the address is not available.</span></span>

<span data-ttu-id="cad1d-196"><span id="PIX_TE_FAILEDTOLOADSOFTWAREMODULE"></span><span id="pix_te_failedtoloadsoftwaremodule"></span>**Pix \_ te \_ failedtoloadsoftwaremodule**</span><span class="sxs-lookup"><span data-stu-id="cad1d-196"><span id="PIX_TE_FAILEDTOLOADSOFTWAREMODULE"></span><span id="pix_te_failedtoloadsoftwaremodule"></span>**PIX\_TE\_FAILEDTOLOADSOFTWAREMODULE**</span></span>  
<span data-ttu-id="cad1d-197">Ein benutzerdefiniertes HRESULT, das angibt, dass ein erforderlicher Softwaremodul nicht geladen werden konnte.</span><span class="sxs-lookup"><span data-stu-id="cad1d-197">A custom HRESULT which indicates that a necessary software module failed to load.</span></span>

<span data-ttu-id="cad1d-198"><span id="PIX_TE_USEDSOFTWAREMODULETHATWASNTWARPORREF"></span><span id="pix_te_usedsoftwaremodulethatwasntwarporref"></span>**Pix \_ te \_ usedsoftwaremodulethatwasntwarporref**</span><span class="sxs-lookup"><span data-stu-id="cad1d-198"><span id="PIX_TE_USEDSOFTWAREMODULETHATWASNTWARPORREF"></span><span id="pix_te_usedsoftwaremodulethatwasntwarporref"></span>**PIX\_TE\_USEDSOFTWAREMODULETHATWASNTWARPORREF**</span></span>  
<span data-ttu-id="cad1d-199">Ein benutzerdefiniertes HRESULT, das angibt, dass das verwendete Softwaremodul nicht der Warp-oder ref-Treiber war.</span><span class="sxs-lookup"><span data-stu-id="cad1d-199">A custom HRESULT which indicates that the used software module was not the WARP or REF driver.</span></span>

<span data-ttu-id="cad1d-200"><span id="PIX_TE_CORRUPTEDFILE"></span><span id="pix_te_corruptedfile"></span>**Pix \_ te beschädigte \_ Datei**</span><span class="sxs-lookup"><span data-stu-id="cad1d-200"><span id="PIX_TE_CORRUPTEDFILE"></span><span id="pix_te_corruptedfile"></span>**PIX\_TE\_CORRUPTEDFILE**</span></span>  
<span data-ttu-id="cad1d-201">Ein benutzerdefiniertes HRESULT, das angibt, dass die Datei beschädigt ist.</span><span class="sxs-lookup"><span data-stu-id="cad1d-201">A custom HRESULT which indicates that the file is corrupted.</span></span>

<span data-ttu-id="cad1d-202"><span id="PIX_TE_FAILEDTOOPENFILE"></span><span id="pix_te_failedtoopenfile"></span>**Pix \_ te \_ faileddeopenfile**</span><span class="sxs-lookup"><span data-stu-id="cad1d-202"><span id="PIX_TE_FAILEDTOOPENFILE"></span><span id="pix_te_failedtoopenfile"></span>**PIX\_TE\_FAILEDTOOPENFILE**</span></span>  
<span data-ttu-id="cad1d-203">Ein benutzerdefiniertes HRESULT, das angibt, dass die Datei nicht geöffnet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="cad1d-203">A custom HRESULT which indicates that the file failed to open.</span></span>

<span data-ttu-id="cad1d-204"><span id="PIX_TE_CALLFAILEDONPLAYBACK"></span><span id="pix_te_callfailedonplayback"></span>**Pix \_ te \_ callfailedonplayback**</span><span class="sxs-lookup"><span data-stu-id="cad1d-204"><span id="PIX_TE_CALLFAILEDONPLAYBACK"></span><span id="pix_te_callfailedonplayback"></span>**PIX\_TE\_CALLFAILEDONPLAYBACK**</span></span>  
<span data-ttu-id="cad1d-205">Ein benutzerdefiniertes HRESULT, das angibt, dass ein Fehler während der Wiedergabe aufgetreten ist</span><span class="sxs-lookup"><span data-stu-id="cad1d-205">A custom HRESULT which indicates that a call failed during playback.</span></span>

<span data-ttu-id="cad1d-206"><span id="PIX_TE_UNKNOWNUUID"></span><span id="pix_te_unknownuuid"></span>**Pix \_ te \_ unknownuuid**</span><span class="sxs-lookup"><span data-stu-id="cad1d-206"><span id="PIX_TE_UNKNOWNUUID"></span><span id="pix_te_unknownuuid"></span>**PIX\_TE\_UNKNOWNUUID**</span></span>  
<span data-ttu-id="cad1d-207">Ein benutzerdefiniertes HRESULT, das angibt, dass eine unbekannte UUID gefunden wurde. Dies sollte nie vorkommen.</span><span class="sxs-lookup"><span data-stu-id="cad1d-207">A custom HRESULT which indicates that an unknown UUID was encountered; this should never occur.</span></span>

<span data-ttu-id="cad1d-208"><span id="PIX_TE_NOTCAPTUREFILEORCORRUPTED"></span><span id="pix_te_notcapturefileorcorrupted"></span>**Pix \_ te \_ notcapturefileorbeschädigte**</span><span class="sxs-lookup"><span data-stu-id="cad1d-208"><span id="PIX_TE_NOTCAPTUREFILEORCORRUPTED"></span><span id="pix_te_notcapturefileorcorrupted"></span>**PIX\_TE\_NOTCAPTUREFILEORCORRUPTED**</span></span>  
<span data-ttu-id="cad1d-209">Ein benutzerdefiniertes HRESULT, das angibt, dass die Datei keine Erfassungs Datei ist oder beschädigt ist.</span><span class="sxs-lookup"><span data-stu-id="cad1d-209">A custom HRESULT which indicates that the file is not a capture file or is corrupted.</span></span>

<span data-ttu-id="cad1d-210"><span id="PIX_TE_NEWERFILE"></span><span id="pix_te_newerfile"></span>**Pix \_ te- \_ netzwerdatei**</span><span class="sxs-lookup"><span data-stu-id="cad1d-210"><span id="PIX_TE_NEWERFILE"></span><span id="pix_te_newerfile"></span>**PIX\_TE\_NEWERFILE**</span></span>  

<span data-ttu-id="cad1d-211"><span id="PIX_TE_OLDERFILE"></span><span id="pix_te_olderfile"></span>**Pix \_ te \_ OlderFile**</span><span class="sxs-lookup"><span data-stu-id="cad1d-211"><span id="PIX_TE_OLDERFILE"></span><span id="pix_te_olderfile"></span>**PIX\_TE\_OLDERFILE**</span></span>  

<span data-ttu-id="cad1d-212"><span id="PIX_TE_INVALIDMOMENT"></span><span id="pix_te_invalidmoment"></span>**Pix \_ te \_ invalidmoment**</span><span class="sxs-lookup"><span data-stu-id="cad1d-212"><span id="PIX_TE_INVALIDMOMENT"></span><span id="pix_te_invalidmoment"></span>**PIX\_TE\_INVALIDMOMENT**</span></span>  

<span data-ttu-id="cad1d-213"><span id="PIX_TE_BAD_DRIVER"></span><span id="pix_te_bad_driver"></span>**Pix \_ - \_ Treiber "schlecht" \_**</span><span class="sxs-lookup"><span data-stu-id="cad1d-213"><span id="PIX_TE_BAD_DRIVER"></span><span id="pix_te_bad_driver"></span>**PIX\_TE\_BAD\_DRIVER**</span></span>  
<span data-ttu-id="cad1d-214">Ein benutzerdefiniertes HRESULT, das angibt, dass der Treiber schlecht ist.</span><span class="sxs-lookup"><span data-stu-id="cad1d-214">A custom HRESULT which indicates that the driver is bad.</span></span>

<span data-ttu-id="cad1d-215"><span id="PIX_ERROR_CANT_ACCESS_DEPTHSTENCIL_IN_CPU"></span><span id="pix_error_cant_access_depthstencil_in_cpu"></span>**Pix \_ - \_ Fehler \_ \_ beim Zugriff auf depthstencil \_ in der \_ CPU.**</span><span class="sxs-lookup"><span data-stu-id="cad1d-215"><span id="PIX_ERROR_CANT_ACCESS_DEPTHSTENCIL_IN_CPU"></span><span id="pix_error_cant_access_depthstencil_in_cpu"></span>**PIX\_ERROR\_CANT\_ACCESS\_DEPTHSTENCIL\_IN\_CPU**</span></span>  
<span data-ttu-id="cad1d-216">Ein benutzerdefiniertes HRESULT, das angibt, dass die CPU versucht hat, auf den tiefen Schablonen Puffer zuzugreifen, was zu einem Fehler führt.</span><span class="sxs-lookup"><span data-stu-id="cad1d-216">A custom HRESULT which indicates that the CPU attempted to access the depth-stencil buffer, resulting in an error.</span></span>

<span data-ttu-id="cad1d-217"><span id="PIX_ERROR_CANT_RESOLVE_MULTISAMPLED_TEXTURE"></span><span id="pix_error_cant_resolve_multisampled_texture"></span>**Pix- \_ Fehler beim \_ Auflösen von \_ \_ Multisampling- \_ Textur.**</span><span class="sxs-lookup"><span data-stu-id="cad1d-217"><span id="PIX_ERROR_CANT_RESOLVE_MULTISAMPLED_TEXTURE"></span><span id="pix_error_cant_resolve_multisampled_texture"></span>**PIX\_ERROR\_CANT\_RESOLVE\_MULTISAMPLED\_TEXTURE**</span></span>  
<span data-ttu-id="cad1d-218">Ein benutzerdefiniertes HRESULT, das angibt, dass versucht wurde, eine Multisampling-Textur aufzulösen, was zu einem Fehler führt.</span><span class="sxs-lookup"><span data-stu-id="cad1d-218">A custom HRESULT which indicates that there was an attempt to resolve a multi-sampled texture, resulting in an error.</span></span>

<span data-ttu-id="cad1d-219"><span id="PIX_DXGI_ERROR_INVALID_CALL"></span><span id="pix_dxgi_error_invalid_call"></span>**Pix \_ DXGI- \_ Fehler \_ ungültiger \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="cad1d-219"><span id="PIX_DXGI_ERROR_INVALID_CALL"></span><span id="pix_dxgi_error_invalid_call"></span>**PIX\_DXGI\_ERROR\_INVALID\_CALL**</span></span>  
<span data-ttu-id="cad1d-220">Ein benutzerdefiniertes HRESULT, für das der Befehl "Echos DXGI" \_ \_ ungültig ist \_</span><span class="sxs-lookup"><span data-stu-id="cad1d-220">A custom HRESULT that echos DXGI\_ERROR\_INVALID\_CALL.</span></span>

<span data-ttu-id="cad1d-221"><span id="PIX_DXGI_ERROR_NOT_FOUND"></span><span id="pix_dxgi_error_not_found"></span>**Pix \_ DXGI- \_ Fehler \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="cad1d-221"><span id="PIX_DXGI_ERROR_NOT_FOUND"></span><span id="pix_dxgi_error_not_found"></span>**PIX\_DXGI\_ERROR\_NOT\_FOUND**</span></span>  
<span data-ttu-id="cad1d-222">Ein benutzerdefiniertes HRESULT, das der DXGI- \_ Fehler \_ nicht \_ gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="cad1d-222">A custom HRESULT that echos DXGI\_ERROR\_NOT\_FOUND.</span></span>

<span data-ttu-id="cad1d-223"><span id="PIX_DXGI_ERROR_MORE_DATA"></span><span id="pix_dxgi_error_more_data"></span>**Pix \_ DXGI- \_ Fehler \_ Weitere \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="cad1d-223"><span id="PIX_DXGI_ERROR_MORE_DATA"></span><span id="pix_dxgi_error_more_data"></span>**PIX\_DXGI\_ERROR\_MORE\_DATA**</span></span>  
<span data-ttu-id="cad1d-224">Ein benutzerdefiniertes HRESULT, das für DXGI einen \_ Fehler \_ mehr \_ Daten verursacht.</span><span class="sxs-lookup"><span data-stu-id="cad1d-224">A custom HRESULT that echos DXGI\_ERROR\_MORE\_DATA.</span></span>

<span data-ttu-id="cad1d-225"><span id="PIX_DXGI_ERROR_UNSUPPORTED"></span><span id="pix_dxgi_error_unsupported"></span>**Pix \_ DXGI- \_ Fehler \_ nicht unterstützt**</span><span class="sxs-lookup"><span data-stu-id="cad1d-225"><span id="PIX_DXGI_ERROR_UNSUPPORTED"></span><span id="pix_dxgi_error_unsupported"></span>**PIX\_DXGI\_ERROR\_UNSUPPORTED**</span></span>  
<span data-ttu-id="cad1d-226">Ein benutzerdefiniertes HRESULT, das den DXGI-Fehler "" \_ \_ nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cad1d-226">A custom HRESULT that echos DXGI\_ERROR\_UNSUPPORTED.</span></span>

<span data-ttu-id="cad1d-227"><span id="PIX_DXGI_ERROR_DEVICE_REMOVED"></span><span id="pix_dxgi_error_device_removed"></span>**Pix- \_ DXGI- \_ Fehler \_ Gerät \_ entfernt**</span><span class="sxs-lookup"><span data-stu-id="cad1d-227"><span id="PIX_DXGI_ERROR_DEVICE_REMOVED"></span><span id="pix_dxgi_error_device_removed"></span>**PIX\_DXGI\_ERROR\_DEVICE\_REMOVED**</span></span>  
<span data-ttu-id="cad1d-228">Ein benutzerdefiniertes HRESULT, das von der Meldung DXGI \_ Error \_ \_ entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="cad1d-228">A custom HRESULT that echos DXGI\_ERROR\_DEVICE\_REMOVED.</span></span>

<span data-ttu-id="cad1d-229"><span id="PIX_DXGI_ERROR_DEVICE_HUNG"></span><span id="pix_dxgi_error_device_hung"></span>**Pix \_ DXGI- \_ Fehler \_ Gerät \_ nicht reagiert**</span><span class="sxs-lookup"><span data-stu-id="cad1d-229"><span id="PIX_DXGI_ERROR_DEVICE_HUNG"></span><span id="pix_dxgi_error_device_hung"></span>**PIX\_DXGI\_ERROR\_DEVICE\_HUNG**</span></span>  
<span data-ttu-id="cad1d-230">Ein benutzerdefiniertes HRESULT, das auf das-DXGI- \_ Fehler \_ Gerät reagiert \_ .</span><span class="sxs-lookup"><span data-stu-id="cad1d-230">A custom HRESULT that echos DXGI\_ERROR\_DEVICE\_HUNG.</span></span>

<span data-ttu-id="cad1d-231"><span id="PIX_DXGI_ERROR_DEVICE_RESET"></span><span id="pix_dxgi_error_device_reset"></span>**Pix \_ DXGI- \_ Fehler beim \_ \_ Zurücksetzen des Geräts**</span><span class="sxs-lookup"><span data-stu-id="cad1d-231"><span id="PIX_DXGI_ERROR_DEVICE_RESET"></span><span id="pix_dxgi_error_device_reset"></span>**PIX\_DXGI\_ERROR\_DEVICE\_RESET**</span></span>  
<span data-ttu-id="cad1d-232">Ein benutzerdefiniertes HRESULT, das beim \_ \_ \_ Zurücksetzen von "DXGI"-Fehlern</span><span class="sxs-lookup"><span data-stu-id="cad1d-232">A custom HRESULT that echos DXGI\_ERROR\_DEVICE\_RESET.</span></span>

<span data-ttu-id="cad1d-233"><span id="PIX_DXGI_ERROR_WAS_STILL_DRAWING"></span><span id="pix_dxgi_error_was_still_drawing"></span>**Pix \_ DXGI- \_ Fehler \_ war \_ immer noch \_ gezeichnet.**</span><span class="sxs-lookup"><span data-stu-id="cad1d-233"><span id="PIX_DXGI_ERROR_WAS_STILL_DRAWING"></span><span id="pix_dxgi_error_was_still_drawing"></span>**PIX\_DXGI\_ERROR\_WAS\_STILL\_DRAWING**</span></span>  
<span data-ttu-id="cad1d-234">Ein benutzerdefiniertes HRESULT, das den Fehler "Echos DXGI" \_ \_ \_ immer noch \_ zeichnet.</span><span class="sxs-lookup"><span data-stu-id="cad1d-234">A custom HRESULT that echos DXGI\_ERROR\_WAS\_STILL\_DRAWING.</span></span>

<span data-ttu-id="cad1d-235"><span id="PIX_DXGI_ERROR_FRAME_STATISTICS_DISJOINT"></span><span id="pix_dxgi_error_frame_statistics_disjoint"></span>**Pix \_ DXGI- \_ Fehler \_ Rahmen \_ Statistik \_ getrennt**</span><span class="sxs-lookup"><span data-stu-id="cad1d-235"><span id="PIX_DXGI_ERROR_FRAME_STATISTICS_DISJOINT"></span><span id="pix_dxgi_error_frame_statistics_disjoint"></span>**PIX\_DXGI\_ERROR\_FRAME\_STATISTICS\_DISJOINT**</span></span>  
<span data-ttu-id="cad1d-236">Ein benutzerdefiniertes HRESULT, bei dem die Fehler in der DXGI- \_ Fehler \_ Frame \_ Statistik \_ getrennt werden</span><span class="sxs-lookup"><span data-stu-id="cad1d-236">A custom HRESULT that echos DXGI\_ERROR\_FRAME\_STATISTICS\_DISJOINT.</span></span>

<span data-ttu-id="cad1d-237"><span id="PIX_DXGI_ERROR_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_error_graphics_vidpn_source_in_use"></span>**Pix \_ DXGI- \_ Fehler \_ Grafik \_ VidPN-Quelle wird \_ \_ \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="cad1d-237"><span id="PIX_DXGI_ERROR_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_error_graphics_vidpn_source_in_use"></span>**PIX\_DXGI\_ERROR\_GRAPHICS\_VIDPN\_SOURCE\_IN\_USE**</span></span>  
<span data-ttu-id="cad1d-238">Ein benutzerdefiniertes HRESULT, das bei der Verwendung von Echos DXGI \_ Error \_ Graphics \_ VidPN \_ Source \_ verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="cad1d-238">A custom HRESULT that echos DXGI\_ERROR\_GRAPHICS\_VIDPN\_SOURCE\_IN\_USE.</span></span>

<span data-ttu-id="cad1d-239"><span id="PIX_DXGI_ERROR_DRIVER_INTERNAL_ERROR"></span><span id="pix_dxgi_error_driver_internal_error"></span>**\_Interner Fehler des pix DXGI- \_ Fehler \_ Treibers. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cad1d-239"><span id="PIX_DXGI_ERROR_DRIVER_INTERNAL_ERROR"></span><span id="pix_dxgi_error_driver_internal_error"></span>**PIX\_DXGI\_ERROR\_DRIVER\_INTERNAL\_ERROR**</span></span>  
<span data-ttu-id="cad1d-240">Ein benutzerdefiniertes HRESULT, das einen internen Fehler des DXGI- \_ Fehler \_ Treibers verursacht \_ \_</span><span class="sxs-lookup"><span data-stu-id="cad1d-240">A custom HRESULT that echos DXGI\_ERROR\_DRIVER\_INTERNAL\_ERROR.</span></span>

<span data-ttu-id="cad1d-241"><span id="PIX_DXGI_ERROR_NONEXCLUSIVE"></span><span id="pix_dxgi_error_nonexclusive"></span>**Pix \_ DXGI- \_ Fehler \_ nicht exklusiv**</span><span class="sxs-lookup"><span data-stu-id="cad1d-241"><span id="PIX_DXGI_ERROR_NONEXCLUSIVE"></span><span id="pix_dxgi_error_nonexclusive"></span>**PIX\_DXGI\_ERROR\_NONEXCLUSIVE**</span></span>  
<span data-ttu-id="cad1d-242">Ein benutzerdefiniertes HRESULT, das für den DXGI- \_ Fehler \_ nicht exklusiv ist.</span><span class="sxs-lookup"><span data-stu-id="cad1d-242">A custom HRESULT that echos DXGI\_ERROR\_NONEXCLUSIVE.</span></span>

<span data-ttu-id="cad1d-243"><span id="PIX_DXGI_ERROR_NOT_CURRENTLY_AVAILABLE"></span><span id="pix_dxgi_error_not_currently_available"></span>**Pix \_ DXGI- \_ Fehler ist \_ \_ zurzeit nicht \_ verfügbar.**</span><span class="sxs-lookup"><span data-stu-id="cad1d-243"><span id="PIX_DXGI_ERROR_NOT_CURRENTLY_AVAILABLE"></span><span id="pix_dxgi_error_not_currently_available"></span>**PIX\_DXGI\_ERROR\_NOT\_CURRENTLY\_AVAILABLE**</span></span>  
<span data-ttu-id="cad1d-244">Ein benutzerdefiniertes HRESULT, das für den Fehler "Echos DXGI" \_ \_ nicht \_ \_ verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="cad1d-244">A custom HRESULT that echos DXGI\_ERROR\_NOT\_CURRENTLY\_AVAILABLE.</span></span>

<span data-ttu-id="cad1d-245"><span id="PIX_DXGI_ERROR_REMOTE_CLIENT_DISCONNECTED"></span><span id="pix_dxgi_error_remote_client_disconnected"></span>**Pix \_ DXGI- \_ Fehler " \_ Remote \_ Client \_ getrennt"**</span><span class="sxs-lookup"><span data-stu-id="cad1d-245"><span id="PIX_DXGI_ERROR_REMOTE_CLIENT_DISCONNECTED"></span><span id="pix_dxgi_error_remote_client_disconnected"></span>**PIX\_DXGI\_ERROR\_REMOTE\_CLIENT\_DISCONNECTED**</span></span>  
<span data-ttu-id="cad1d-246">Ein benutzerdefiniertes HRESULT, für das der DXGI-Fehler für den \_ \_ Remote \_ Client \_ nicht</span><span class="sxs-lookup"><span data-stu-id="cad1d-246">A custom HRESULT that echos DXGI\_ERROR\_REMOTE\_CLIENT\_DISCONNECTED.</span></span>

<span data-ttu-id="cad1d-247"><span id="PIX_DXGI_ERROR_REMOTE_OUTOFMEMORY"></span><span id="pix_dxgi_error_remote_outofmemory"></span>**Pix \_ DXGI \_ - \_ Remote- \_ oudef-Fehler**</span><span class="sxs-lookup"><span data-stu-id="cad1d-247"><span id="PIX_DXGI_ERROR_REMOTE_OUTOFMEMORY"></span><span id="pix_dxgi_error_remote_outofmemory"></span>**PIX\_DXGI\_ERROR\_REMOTE\_OUTOFMEMORY**</span></span>  
<span data-ttu-id="cad1d-248">Ein benutzerdefiniertes HRESULT, das auf einen remoten DXGI-Fehler zurückgeht \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cad1d-248">A custom HRESULT that echos DXGI\_ERROR\_REMOTE\_OUTOFMEMORY.</span></span>

<span data-ttu-id="cad1d-249"><span id="PIX_DXGI_ERROR_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_error_mode_change_in_progress"></span>**Pix- \_ DXGI- \_ fehlermodusänderung \_ \_ \_ in \_ Bearbeitung**</span><span class="sxs-lookup"><span data-stu-id="cad1d-249"><span id="PIX_DXGI_ERROR_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_error_mode_change_in_progress"></span>**PIX\_DXGI\_ERROR\_MODE\_CHANGE\_IN\_PROGRESS**</span></span>  
<span data-ttu-id="cad1d-250">Ein benutzerdefiniertes HRESULT, bei dem der Status der Echos DXGI- \_ Fehlermeldung \_ \_ geändert wird \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cad1d-250">A custom HRESULT that echos DXGI\_ERROR\_MODE\_CHANGE\_IN\_PROGRESS.</span></span>

<span data-ttu-id="cad1d-251"><span id="PIX_DXGI_ERROR_ACCESS_LOST"></span><span id="pix_dxgi_error_access_lost"></span>**Pix \_ DXGI- \_ Fehler beim \_ Zugriff \_ verloren**</span><span class="sxs-lookup"><span data-stu-id="cad1d-251"><span id="PIX_DXGI_ERROR_ACCESS_LOST"></span><span id="pix_dxgi_error_access_lost"></span>**PIX\_DXGI\_ERROR\_ACCESS\_LOST**</span></span>  
<span data-ttu-id="cad1d-252">Ein benutzerdefiniertes HRESULT, das für den Zugriff auf den DXGI- \_ Fehler in \_ \_</span><span class="sxs-lookup"><span data-stu-id="cad1d-252">A custom HRESULT that echos DXGI\_ERROR\_ACCESS\_LOST.</span></span>

<span data-ttu-id="cad1d-253"><span id="PIX_DXGI_ERROR_WAIT_TIMEOUT"></span><span id="pix_dxgi_error_wait_timeout"></span>**Pix \_ DXGI- \_ Fehler \_ Wartezeit- \_ Timeout**</span><span class="sxs-lookup"><span data-stu-id="cad1d-253"><span id="PIX_DXGI_ERROR_WAIT_TIMEOUT"></span><span id="pix_dxgi_error_wait_timeout"></span>**PIX\_DXGI\_ERROR\_WAIT\_TIMEOUT**</span></span>  
<span data-ttu-id="cad1d-254">Ein benutzerdefiniertes HRESULT, das den Timeout Wert für DXGI- \_ Fehler \_ Wartezeiten \_</span><span class="sxs-lookup"><span data-stu-id="cad1d-254">A custom HRESULT that echos DXGI\_ERROR\_WAIT\_TIMEOUT.</span></span>

<span data-ttu-id="cad1d-255"><span id="PIX_DXGI_ERROR_SESSION_DISCONNECTED"></span><span id="pix_dxgi_error_session_disconnected"></span>**Pix \_ DXGI- \_ Fehler \_ Sitzung \_ getrennt**</span><span class="sxs-lookup"><span data-stu-id="cad1d-255"><span id="PIX_DXGI_ERROR_SESSION_DISCONNECTED"></span><span id="pix_dxgi_error_session_disconnected"></span>**PIX\_DXGI\_ERROR\_SESSION\_DISCONNECTED**</span></span>  
<span data-ttu-id="cad1d-256">Ein benutzerdefiniertes HRESULT, für das die DXGI- \_ Fehler Sitzung von " \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cad1d-256">A custom HRESULT that echos DXGI\_ERROR\_SESSION\_DISCONNECTED.</span></span>

<span data-ttu-id="cad1d-257"><span id="PIX_DXGI_ERROR_RESTRICT_TO_OUTPUT_STALE"></span><span id="pix_dxgi_error_restrict_to_output_stale"></span>**Pix \_ DXGI \_ - \_ Fehler \_ auf \_ Ausgabe \_ veraltet beschränken**</span><span class="sxs-lookup"><span data-stu-id="cad1d-257"><span id="PIX_DXGI_ERROR_RESTRICT_TO_OUTPUT_STALE"></span><span id="pix_dxgi_error_restrict_to_output_stale"></span>**PIX\_DXGI\_ERROR\_RESTRICT\_TO\_OUTPUT\_STALE**</span></span>  
<span data-ttu-id="cad1d-258">Ein benutzerdefiniertes HRESULT, das von "Echos DXGI \_ Error" \_ \_ auf \_ Ausgabe veraltet beschränkt wird \_ .</span><span class="sxs-lookup"><span data-stu-id="cad1d-258">A custom HRESULT that echos DXGI\_ERROR\_RESTRICT\_TO\_OUTPUT\_STALE.</span></span>

<span data-ttu-id="cad1d-259"><span id="PIX_DXGI_ERROR_CANNOT_PROTECT_CONTENT"></span><span id="pix_dxgi_error_cannot_protect_content"></span>**Pix \_ DXGI \_ - \_ Fehler \_ kann \_ Inhalte nicht schützen.**</span><span class="sxs-lookup"><span data-stu-id="cad1d-259"><span id="PIX_DXGI_ERROR_CANNOT_PROTECT_CONTENT"></span><span id="pix_dxgi_error_cannot_protect_content"></span>**PIX\_DXGI\_ERROR\_CANNOT\_PROTECT\_CONTENT**</span></span>  
<span data-ttu-id="cad1d-260">Ein benutzerdefiniertes HRESULT, das der DXGI-Fehler "Echos" \_ \_ nicht \_ schützen kann \_</span><span class="sxs-lookup"><span data-stu-id="cad1d-260">A custom HRESULT that echos DXGI\_ERROR\_CANNOT\_PROTECT\_CONTENT.</span></span>

<span data-ttu-id="cad1d-261"><span id="PIX_DXGI_ERROR_ACCESS_DENIED"></span><span id="pix_dxgi_error_access_denied"></span>**Pix \_ DXGI- \_ Fehler \_ Zugriff \_ verweigert**</span><span class="sxs-lookup"><span data-stu-id="cad1d-261"><span id="PIX_DXGI_ERROR_ACCESS_DENIED"></span><span id="pix_dxgi_error_access_denied"></span>**PIX\_DXGI\_ERROR\_ACCESS\_DENIED**</span></span>  
<span data-ttu-id="cad1d-262">Ein benutzerdefiniertes HRESULT, auf das der DXGI- \_ Fehler \_ Zugriff \_ verweigert wurde.</span><span class="sxs-lookup"><span data-stu-id="cad1d-262">A custom HRESULT that echos DXGI\_ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="cad1d-263"><span id="PIX_DXGI_ERROR_NAME_ALREADY_EXISTS"></span><span id="pix_dxgi_error_name_already_exists"></span>**Pix \_ DXGI- \_ Fehler \_ Name ist \_ bereits \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="cad1d-263"><span id="PIX_DXGI_ERROR_NAME_ALREADY_EXISTS"></span><span id="pix_dxgi_error_name_already_exists"></span>**PIX\_DXGI\_ERROR\_NAME\_ALREADY\_EXISTS**</span></span>  
<span data-ttu-id="cad1d-264">Ein benutzerdefiniertes HRESULT, das den Namen "Echos DXGI \_ Error" \_ bereits enthält \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cad1d-264">A custom HRESULT that echos DXGI\_ERROR\_NAME\_ALREADY\_EXISTS.</span></span>

<span data-ttu-id="cad1d-265"><span id="PIX_DXGI_ERROR_SDK_COMPONENT_MISSING"></span><span id="pix_dxgi_error_sdk_component_missing"></span>**Pix- \_ DXGI- \_ Fehler-SDK- \_ \_ Komponente \_ fehlt**</span><span class="sxs-lookup"><span data-stu-id="cad1d-265"><span id="PIX_DXGI_ERROR_SDK_COMPONENT_MISSING"></span><span id="pix_dxgi_error_sdk_component_missing"></span>**PIX\_DXGI\_ERROR\_SDK\_COMPONENT\_MISSING**</span></span>  
<span data-ttu-id="cad1d-266">Ein benutzerdefiniertes HRESULT, das für die "DXGI \_ Error \_ SDK \_ Component" \_ fehlt.</span><span class="sxs-lookup"><span data-stu-id="cad1d-266">A custom HRESULT that echos DXGI\_ERROR\_SDK\_COMPONENT\_MISSING.</span></span>

<span data-ttu-id="cad1d-267"><span id="PIX_DXGI_DDI_ERR_WASSTILLDRAWING"></span><span id="pix_dxgi_ddi_err_wasstilldrawing"></span>**Pix \_ DXGI \_ DDI \_ Err \_ wasstilldrawing**</span><span class="sxs-lookup"><span data-stu-id="cad1d-267"><span id="PIX_DXGI_DDI_ERR_WASSTILLDRAWING"></span><span id="pix_dxgi_ddi_err_wasstilldrawing"></span>**PIX\_DXGI\_DDI\_ERR\_WASSTILLDRAWING**</span></span>  
<span data-ttu-id="cad1d-268">Ein benutzerdefiniertes HRESULT, das auf DXGI \_ DDI \_ Err \_ wasstilldrawing festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cad1d-268">A custom HRESULT that echos DXGI\_DDI\_ERR\_WASSTILLDRAWING.</span></span>

<span data-ttu-id="cad1d-269"><span id="PIX_DXGI_DDI_ERR_UNSUPPORTED"></span><span id="pix_dxgi_ddi_err_unsupported"></span>**Pix \_ DXGI \_ DDI \_ Err \_ wird nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="cad1d-269"><span id="PIX_DXGI_DDI_ERR_UNSUPPORTED"></span><span id="pix_dxgi_ddi_err_unsupported"></span>**PIX\_DXGI\_DDI\_ERR\_UNSUPPORTED**</span></span>  
<span data-ttu-id="cad1d-270">Ein benutzerdefiniertes HRESULT, das von Echos DXGI \_ DDI \_ Err \_ nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="cad1d-270">A custom HRESULT that echos DXGI\_DDI\_ERR\_UNSUPPORTED.</span></span>

<span data-ttu-id="cad1d-271"><span id="PIX_DXGI_DDI_ERR_NONEXCLUSIVE"></span><span id="pix_dxgi_ddi_err_nonexclusive"></span>**Pix \_ DXGI \_ DDI \_ Err \_ nicht exklusiv**</span><span class="sxs-lookup"><span data-stu-id="cad1d-271"><span id="PIX_DXGI_DDI_ERR_NONEXCLUSIVE"></span><span id="pix_dxgi_ddi_err_nonexclusive"></span>**PIX\_DXGI\_DDI\_ERR\_NONEXCLUSIVE**</span></span>  
<span data-ttu-id="cad1d-272">Ein benutzerdefiniertes HRESULT, das auf "DXGI \_ DDI \_ Err nicht exklusiv" fest liegt \_ .</span><span class="sxs-lookup"><span data-stu-id="cad1d-272">A custom HRESULT that echos DXGI\_DDI\_ERR\_NONEXCLUSIVE.</span></span>

<span data-ttu-id="cad1d-273"><span id="PIX_D3D10_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d10_error_too_many_unique_state_objects"></span>**Pix \_ d3d10 \_ Fehler \_ zu \_ viele \_ eindeutige \_ Zustands \_ Objekte**</span><span class="sxs-lookup"><span data-stu-id="cad1d-273"><span id="PIX_D3D10_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d10_error_too_many_unique_state_objects"></span>**PIX\_D3D10\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS**</span></span>  
<span data-ttu-id="cad1d-274">Ein benutzerdefiniertes HRESULT, das den \_ Fehler d3d10 \_ zu \_ viele \_ eindeutige \_ Zustands \_ Objekte verursacht.</span><span class="sxs-lookup"><span data-stu-id="cad1d-274">A custom HRESULT that echos D3D10\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS.</span></span>

<span data-ttu-id="cad1d-275"><span id="PIX_D3D10_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d10_error_file_not_found"></span>**Pix \_ d3d10 \_ Fehler \_ Datei \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="cad1d-275"><span id="PIX_D3D10_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d10_error_file_not_found"></span>**PIX\_D3D10\_ERROR\_FILE\_NOT\_FOUND**</span></span>  
<span data-ttu-id="cad1d-276">Ein benutzerdefiniertes HRESULT, das die Fehler Datei "d3d10" \_ \_ \_ nicht \_ gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="cad1d-276">A custom HRESULT that echos D3D10\_ERROR\_FILE\_NOT\_FOUND.</span></span>

<span data-ttu-id="cad1d-277"><span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_state_objects"></span>**Pix \_ D3D11 \_ Fehler \_ zu \_ viele \_ eindeutige \_ Zustands \_ Objekte**</span><span class="sxs-lookup"><span data-stu-id="cad1d-277"><span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_state_objects"></span>**PIX\_D3D11\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS**</span></span>  
<span data-ttu-id="cad1d-278">Ein benutzerdefiniertes HRESULT, das den \_ Fehler D3D11 \_ zu \_ viele \_ eindeutige \_ Zustands \_ Objekte verursacht.</span><span class="sxs-lookup"><span data-stu-id="cad1d-278">A custom HRESULT that echos D3D11\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS.</span></span>

<span data-ttu-id="cad1d-279"><span id="PIX_D3D11_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d11_error_file_not_found"></span>**Pix \_ D3D11 \_ Fehler \_ Datei \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="cad1d-279"><span id="PIX_D3D11_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d11_error_file_not_found"></span>**PIX\_D3D11\_ERROR\_FILE\_NOT\_FOUND**</span></span>  
<span data-ttu-id="cad1d-280">Ein benutzerdefiniertes HRESULT, das die Fehler Datei "D3D11" \_ \_ \_ nicht \_ gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="cad1d-280">A custom HRESULT that echos D3D11\_ERROR\_FILE\_NOT\_FOUND.</span></span>

<span data-ttu-id="cad1d-281"><span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_view_objects"></span>**Pix \_ D3D11 \_ Fehler \_ zu \_ viele \_ eindeutige \_ Ansichts \_ Objekte**</span><span class="sxs-lookup"><span data-stu-id="cad1d-281"><span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_view_objects"></span>**PIX\_D3D11\_ERROR\_TOO\_MANY\_UNIQUE\_VIEW\_OBJECTS**</span></span>  
<span data-ttu-id="cad1d-282">Ein benutzerdefiniertes HRESULT, das den Fehler "D3D11" \_ \_ zu \_ viele \_ eindeutige \_ Ansichts \_ Objekte verursacht</span><span class="sxs-lookup"><span data-stu-id="cad1d-282">A custom HRESULT that echos D3D11\_ERROR\_TOO\_MANY\_UNIQUE\_VIEW\_OBJECTS.</span></span>

<span data-ttu-id="cad1d-283"><span id="PIX_D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD"></span><span id="pix_d3d11_error_deferred_context_map_without_initial_discard"></span>**Pix \_ D3D11 \_ Fehler bei \_ verzögerter \_ Kontext Zuordnung \_ \_ ohne \_ anfängliche \_ verwerfen**</span><span class="sxs-lookup"><span data-stu-id="cad1d-283"><span id="PIX_D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD"></span><span id="pix_d3d11_error_deferred_context_map_without_initial_discard"></span>**PIX\_D3D11\_ERROR\_DEFERRED\_CONTEXT\_MAP\_WITHOUT\_INITIAL\_DISCARD**</span></span>  
<span data-ttu-id="cad1d-284">Ein benutzerdefiniertes HRESULT, das eine \_ Fehlermeldung zurückgibt \_ \_ \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="cad1d-284">A custom HRESULT that echos D3D11\_ERROR\_DEFERRED\_CONTEXT\_MAP\_WITHOUT\_INITIAL\_DISCARD.</span></span>

<span data-ttu-id="cad1d-285"><span id="PIX_ERROR_OCCLUDED_DRAW_CALL"></span><span id="pix_error_occluded_draw_call"></span>**Pix- \_ Fehler beim \_ \_ Zeichnen \_ -Befehl.**</span><span class="sxs-lookup"><span data-stu-id="cad1d-285"><span id="PIX_ERROR_OCCLUDED_DRAW_CALL"></span><span id="pix_error_occluded_draw_call"></span>**PIX\_ERROR\_OCCLUDED\_DRAW\_CALL**</span></span>  
<span data-ttu-id="cad1d-286">Ein benutzerdefiniertes HRESULT, das angibt, dass ein Draw-Befehl vollständig geokelt wurde, was zu einem Fehler führt.</span><span class="sxs-lookup"><span data-stu-id="cad1d-286">A custom HRESULT which indicates that a draw call was entirely occluded, resulting in an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="cad1d-287">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cad1d-287">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="cad1d-288">Header</span><span class="sxs-lookup"><span data-stu-id="cad1d-288">Header</span></span></p></td><td><span data-ttu-id="cad1d-289">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="cad1d-289">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



