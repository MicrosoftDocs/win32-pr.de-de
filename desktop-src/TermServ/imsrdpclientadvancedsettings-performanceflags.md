---
title: Imsrdpclientadvancedsettings Performance Flags-Eigenschaft
description: Gibt eine Gruppe von Funktionen an, die auf dem Server festgelegt werden können, um die Leistung zu verbessern.
ms.assetid: dbbc7c13-ad8a-461d-9d2e-c454bf4b9dea
ms.tgt_platform: multiple
keywords:
- Performanceflags-Eigenschaft Remotedesktopdienste
- Performanceflags-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, performanceflags-Eigenschaft
- Performanceflags-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, performanceflags (Eigenschaft)
- Performanceflags-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, performanceflags (Eigenschaft)
- Performanceflags-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, performanceflags (Eigenschaft)
- Performanceflags-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, performanceflags (Eigenschaft)
- Performanceflags-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, performanceflags (Eigenschaft)
- Performanceflags-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, performanceflags (Eigenschaft)
- Performanceflags-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, performanceflags (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.PerformanceFlags
- IMsRdpClientAdvancedSettings.get_PerformanceFlags
- IMsRdpClientAdvancedSettings.put_PerformanceFlags
- IMsRdpClientAdvancedSettings2.PerformanceFlags
- IMsRdpClientAdvancedSettings2.get_PerformanceFlags
- IMsRdpClientAdvancedSettings2.put_PerformanceFlags
- IMsRdpClientAdvancedSettings3.PerformanceFlags
- IMsRdpClientAdvancedSettings3.get_PerformanceFlags
- IMsRdpClientAdvancedSettings3.put_PerformanceFlags
- IMsRdpClientAdvancedSettings4.PerformanceFlags
- IMsRdpClientAdvancedSettings4.get_PerformanceFlags
- IMsRdpClientAdvancedSettings4.put_PerformanceFlags
- IMsRdpClientAdvancedSettings5.PerformanceFlags
- IMsRdpClientAdvancedSettings5.get_PerformanceFlags
- IMsRdpClientAdvancedSettings5.put_PerformanceFlags
- IMsRdpClientAdvancedSettings6.PerformanceFlags
- IMsRdpClientAdvancedSettings6.get_PerformanceFlags
- IMsRdpClientAdvancedSettings6.put_PerformanceFlags
- IMsRdpClientAdvancedSettings7.PerformanceFlags
- IMsRdpClientAdvancedSettings7.get_PerformanceFlags
- IMsRdpClientAdvancedSettings7.put_PerformanceFlags
- IMsRdpClientAdvancedSettings8.PerformanceFlags
- IMsRdpClientAdvancedSettings8.get_PerformanceFlags
- IMsRdpClientAdvancedSettings8.put_PerformanceFlags
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1731afc6d58cede5da055da8cacaf11c8712d3c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391733"
---
# <a name="imsrdpclientadvancedsettingsperformanceflags-property"></a><span data-ttu-id="fa165-120">Imsrdpclientadvancedsettings::P erformanceflags-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fa165-120">IMsRdpClientAdvancedSettings::PerformanceFlags property</span></span>

<span data-ttu-id="fa165-121">Gibt eine Gruppe von Funktionen an, die auf dem Server festgelegt werden können, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="fa165-121">Specifies a set of features that can be set at the server to improve performance.</span></span>

<span data-ttu-id="fa165-122">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="fa165-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa165-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa165-123">Syntax</span></span>


```C++
HRESULT put_PerformanceFlags(
  [in]  LONG DisableList = TS_PERF_DISABLE_NOTHING
);

HRESULT get_PerformanceFlags(
  [out] LONG *pDisableList
);
```



## <a name="property-value"></a><span data-ttu-id="fa165-124">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="fa165-124">Property value</span></span>

<span data-ttu-id="fa165-125">Die neuen Flags.</span><span class="sxs-lookup"><span data-stu-id="fa165-125">The new flags.</span></span> <span data-ttu-id="fa165-126">Der Standardwert ist 0 (**TS \_ perf \_ deaktiviert \_ nichts**.)</span><span class="sxs-lookup"><span data-stu-id="fa165-126">The default is 0 (**TS\_PERF\_DISABLE\_NOTHING**.)</span></span>

<dt>

<span id="TS_PERF_DISABLE_NOTHING"></span><span id="ts_perf_disable_nothing"></span>

<span data-ttu-id="fa165-127"><span id="TS_PERF_DISABLE_NOTHING"></span><span id="ts_perf_disable_nothing"></span>**TS \_ Perf \_ deaktiviert \_ nichts** (0x00000000)</span><span class="sxs-lookup"><span data-stu-id="fa165-127"><span id="TS_PERF_DISABLE_NOTHING"></span><span id="ts_perf_disable_nothing"></span>**TS\_PERF\_DISABLE\_NOTHING** (0x00000000)</span></span>


</dt> <dd>

<span data-ttu-id="fa165-128">Keine Funktionen sind deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="fa165-128">No features are disabled.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_WALLPAPER"></span><span id="ts_perf_disable_wallpaper"></span>

<span data-ttu-id="fa165-129"><span id="TS_PERF_DISABLE_WALLPAPER"></span><span id="ts_perf_disable_wallpaper"></span>**TS \_ Perf \_ - \_ Hintergrundbild deaktivieren** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="fa165-129"><span id="TS_PERF_DISABLE_WALLPAPER"></span><span id="ts_perf_disable_wallpaper"></span>**TS\_PERF\_DISABLE\_WALLPAPER** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="fa165-130">Das Hintergrundbild wird auf dem Desktop nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fa165-130">Wallpaper on the desktop is not displayed.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_FULLWINDOWDRAG"></span><span id="ts_perf_disable_fullwindowdrag"></span>

<span data-ttu-id="fa165-131"><span id="TS_PERF_DISABLE_FULLWINDOWDRAG"></span><span id="ts_perf_disable_fullwindowdrag"></span>**TS \_ Perf \_ Deaktivieren von \_ fullwindowdrag** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="fa165-131"><span id="TS_PERF_DISABLE_FULLWINDOWDRAG"></span><span id="ts_perf_disable_fullwindowdrag"></span>**TS\_PERF\_DISABLE\_FULLWINDOWDRAG** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="fa165-132">Drag & amp; Drop ist deaktiviert. Wenn das Fenster verschoben wird, wird nur die Fenster Gliederung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fa165-132">Full-window drag is disabled; only the window outline is displayed when the window is moved.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_MENUANIMATIONS"></span><span id="ts_perf_disable_menuanimations"></span>

<span data-ttu-id="fa165-133"><span id="TS_PERF_DISABLE_MENUANIMATIONS"></span><span id="ts_perf_disable_menuanimations"></span>**TS \_ Perf \_ Deaktivieren von \_ menuanimationen** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="fa165-133"><span id="TS_PERF_DISABLE_MENUANIMATIONS"></span><span id="ts_perf_disable_menuanimations"></span>**TS\_PERF\_DISABLE\_MENUANIMATIONS** (0x00000004)</span></span>


</dt> <dd>

<span data-ttu-id="fa165-134">Menü Animationen sind deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="fa165-134">Menu animations are disabled.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_THEMING"></span><span id="ts_perf_disable_theming"></span>

<span data-ttu-id="fa165-135"><span id="TS_PERF_DISABLE_THEMING"></span><span id="ts_perf_disable_theming"></span>**TS \_ Leistungs Auswahl \_ Deaktivieren \_** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="fa165-135"><span id="TS_PERF_DISABLE_THEMING"></span><span id="ts_perf_disable_theming"></span>**TS\_PERF\_DISABLE\_THEMING** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="fa165-136">Designs sind deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="fa165-136">Themes are disabled.</span></span>

</dd> <dt>

<span id="TS_PERF_ENABLE_ENHANCED_GRAPHICS"></span><span id="ts_perf_enable_enhanced_graphics"></span>

<span data-ttu-id="fa165-137"><span id="TS_PERF_ENABLE_ENHANCED_GRAPHICS"></span><span id="ts_perf_enable_enhanced_graphics"></span>**TS \_ Perf \_ \_ Erweiterte Grafiken aktivieren** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="fa165-137"><span id="TS_PERF_ENABLE_ENHANCED_GRAPHICS"></span><span id="ts_perf_enable_enhanced_graphics"></span>**TS\_PERF\_ENABLE\_ENHANCED GRAPHICS** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="fa165-138">Aktivieren Sie Erweiterte Grafiken.</span><span class="sxs-lookup"><span data-stu-id="fa165-138">Enable enhanced graphics.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_CURSOR_SHADOW"></span><span id="ts_perf_disable_cursor_shadow"></span>

<span data-ttu-id="fa165-139"><span id="TS_PERF_DISABLE_CURSOR_SHADOW"></span><span id="ts_perf_disable_cursor_shadow"></span>**TS \_ Perf \_ deaktiviert \_ Cursor \_ Schatten** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="fa165-139"><span id="TS_PERF_DISABLE_CURSOR_SHADOW"></span><span id="ts_perf_disable_cursor_shadow"></span>**TS\_PERF\_DISABLE\_CURSOR\_SHADOW** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="fa165-140">Für den Cursor wird kein Schatten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fa165-140">No shadow is displayed for the cursor.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_CURSORSETTINGS"></span><span id="ts_perf_disable_cursorsettings"></span>

<span data-ttu-id="fa165-141"><span id="TS_PERF_DISABLE_CURSORSETTINGS"></span><span id="ts_perf_disable_cursorsettings"></span>**TS \_ Perf \_ Deaktivieren von \_ Cursor Settings** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="fa165-141"><span id="TS_PERF_DISABLE_CURSORSETTINGS"></span><span id="ts_perf_disable_cursorsettings"></span>**TS\_PERF\_DISABLE\_CURSORSETTINGS** (0x00000040)</span></span>


</dt> <dd>

<span data-ttu-id="fa165-142">Cursor blinkt ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="fa165-142">Cursor blinking is disabled.</span></span>

</dd> <dt>

<span id="TS_PERF_ENABLE_FONT_SMOOTHING"></span><span id="ts_perf_enable_font_smoothing"></span>

<span data-ttu-id="fa165-143"><span id="TS_PERF_ENABLE_FONT_SMOOTHING"></span><span id="ts_perf_enable_font_smoothing"></span>**TS \_ Perf \_ Aktivieren der \_ Schriftart \_ Glättung** (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="fa165-143"><span id="TS_PERF_ENABLE_FONT_SMOOTHING"></span><span id="ts_perf_enable_font_smoothing"></span>**TS\_PERF\_ENABLE\_FONT\_SMOOTHING** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="fa165-144">Aktivieren Sie die Schriftart Glättung.</span><span class="sxs-lookup"><span data-stu-id="fa165-144">Enable font smoothing.</span></span>

</dd> <dt>

<span id="TS_PERF_ENABLE_DESKTOP_COMPOSITION"></span><span id="ts_perf_enable_desktop_composition"></span>

<span data-ttu-id="fa165-145"><span id="TS_PERF_ENABLE_DESKTOP_COMPOSITION"></span><span id="ts_perf_enable_desktop_composition"></span>**TS \_ Perf \_ Aktivieren der \_ Desktop \_ Komposition** (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="fa165-145"><span id="TS_PERF_ENABLE_DESKTOP_COMPOSITION"></span><span id="ts_perf_enable_desktop_composition"></span>**TS\_PERF\_ENABLE\_DESKTOP\_COMPOSITION** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="fa165-146">Aktivieren Sie die Desktop Komposition.</span><span class="sxs-lookup"><span data-stu-id="fa165-146">Enable desktop composition.</span></span>

</dd> <dt>

<span id="TS_PERF_DEFAULT_NONPERFCLIENT_SETTING"></span><span id="ts_perf_default_nonperfclient_setting"></span>

<span data-ttu-id="fa165-147"><span id="TS_PERF_DEFAULT_NONPERFCLIENT_SETTING"></span><span id="ts_perf_default_nonperfclient_setting"></span>**TS \_ Perf- \_ Standard \_ \_ Einstellung für nicht perfclient** (0x40000000)</span><span class="sxs-lookup"><span data-stu-id="fa165-147"><span id="TS_PERF_DEFAULT_NONPERFCLIENT_SETTING"></span><span id="ts_perf_default_nonperfclient_setting"></span>**TS\_PERF\_DEFAULT\_NONPERFCLIENT\_SETTING** (0x40000000)</span></span>


</dt> <dd>

<span data-ttu-id="fa165-148">Wird intern für Clients festgelegt, die diese Einstellung nicht kennen.</span><span class="sxs-lookup"><span data-stu-id="fa165-148">Set internally for clients not aware of this setting.</span></span>

</dd> <dt>

<span id="TS_PERF_RESERVED1"></span><span id="ts_perf_reserved1"></span>

<span data-ttu-id="fa165-149"><span id="TS_PERF_RESERVED1"></span><span id="ts_perf_reserved1"></span>**TS \_ Perf \_ "reserved1"** (0x80000000)</span><span class="sxs-lookup"><span data-stu-id="fa165-149"><span id="TS_PERF_RESERVED1"></span><span id="ts_perf_reserved1"></span>**TS\_PERF\_RESERVED1** (0x80000000)</span></span>


</dt> <dd>

<span data-ttu-id="fa165-150">Reserviert und intern vom Client verwendet.</span><span class="sxs-lookup"><span data-stu-id="fa165-150">Reserved and used internally by the client.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="fa165-151">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="fa165-151">Error codes</span></span>

<span data-ttu-id="fa165-152">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="fa165-152">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa165-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fa165-153">Remarks</span></span>

<span data-ttu-id="fa165-154">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="fa165-154">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fa165-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa165-155">Requirements</span></span>



| <span data-ttu-id="fa165-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa165-156">Requirement</span></span> | <span data-ttu-id="fa165-157">Wert</span><span class="sxs-lookup"><span data-stu-id="fa165-157">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa165-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fa165-158">Minimum supported client</span></span><br/> | <span data-ttu-id="fa165-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa165-159">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="fa165-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fa165-160">Minimum supported server</span></span><br/> | <span data-ttu-id="fa165-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa165-161">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="fa165-162">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="fa165-162">Type library</span></span><br/>             | <dl> <span data-ttu-id="fa165-163"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa165-163"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="fa165-164">DLL</span><span class="sxs-lookup"><span data-stu-id="fa165-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa165-165"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa165-165"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="fa165-166">IID</span><span class="sxs-lookup"><span data-stu-id="fa165-166">IID</span></span><br/>                      | <span data-ttu-id="fa165-167">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="fa165-167">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fa165-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa165-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa165-169">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="fa165-169">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="fa165-170">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="fa165-170">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="fa165-171">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="fa165-171">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="fa165-172">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="fa165-172">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="fa165-173">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="fa165-173">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="fa165-174">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="fa165-174">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="fa165-175">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="fa165-175">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="fa165-176">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="fa165-176">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





