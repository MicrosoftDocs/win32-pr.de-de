---
title: MCI_WINDOW Befehl (MMSYSTEM. h)
description: Der MCI \_ -Fenster Befehl gibt das Fenster und die Fenster Eigenschaften für Grafikgeräte an. Dieser Befehl wird von Digital Video-und Video Überlagerungs Geräten erkannt.
ms.assetid: 8b6c4d9a-ee72-4c64-aebe-6c8153167496
keywords:
- MCI_WINDOW Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_WINDOW
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41b4d630dbc9dbc7403e93cd0bda3de2eef1e5cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956614"
---
# <a name="mci_window-command"></a><span data-ttu-id="8206b-105">Befehl "MCI- \_ Fenster"</span><span class="sxs-lookup"><span data-stu-id="8206b-105">MCI\_WINDOW command</span></span>

<span data-ttu-id="8206b-106">Der MCI \_ -Fenster Befehl gibt das Fenster und die Fenster Eigenschaften für Grafikgeräte an.</span><span class="sxs-lookup"><span data-stu-id="8206b-106">The MCI\_WINDOW command specifies the window and the window characteristics for graphic devices.</span></span> <span data-ttu-id="8206b-107">Dieser Befehl wird von Digital Video-und Video Überlagerungs Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="8206b-107">Digital-video, and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="8206b-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="8206b-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_WINDOW, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpWindow
);
```



## <a name="parameters"></a><span data-ttu-id="8206b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8206b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8206b-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="8206b-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="8206b-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="8206b-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="8206b-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="8206b-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="8206b-113">MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder, für Digital Video-Geräte, MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="8206b-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="8206b-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="8206b-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="8206b-115"><span id="lpWindow"></span><span id="lpwindow"></span><span id="LPWINDOW"></span>*lpwindow*</span><span class="sxs-lookup"><span data-stu-id="8206b-115"><span id="lpWindow"></span><span id="lpwindow"></span><span id="LPWINDOW"></span>*lpWindow*</span></span>
</dt> <dd>

<span data-ttu-id="8206b-116">Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="8206b-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="8206b-117">(Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="8206b-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8206b-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8206b-118">Return Value</span></span>

<span data-ttu-id="8206b-119">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="8206b-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8206b-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8206b-120">Remarks</span></span>

<span data-ttu-id="8206b-121">Grafikgeräte sollten ein Standardfenster erstellen, wenn ein Gerät geöffnet wird, das jedoch erst angezeigt werden soll, wenn der Befehl " [MCI \_ Play](mci-play.md) " empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="8206b-121">Graphic devices should create a default window when a device is opened but should not display it until they receive the [MCI\_PLAY](mci-play.md) command.</span></span> <span data-ttu-id="8206b-122">Der MCI \_ -Fenster Befehl wird verwendet, um ein von der Anwendung erstelltes Fenster für das Gerät bereitzustellen und die Anzeigeeigenschaften eines Anwendungs definierten oder standardmäßigen Anzeige Fensters zu ändern.</span><span class="sxs-lookup"><span data-stu-id="8206b-122">The MCI\_WINDOW command is used to supply an application-created window to the device and to change the display characteristics of an application-defined or default display window.</span></span> <span data-ttu-id="8206b-123">Wenn die Anwendung das Anzeige Fenster bereitstellt, sollte Sie darauf vorbereitet sein, ein ungültiges Rechteck im Fenster zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="8206b-123">If the application supplies the display window, it should be prepared to update an invalid rectangle on the window.</span></span>

<span data-ttu-id="8206b-124">Die folgenden zusätzlichen Flags werden mit dem **Digitalvideo** -Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="8206b-124">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="8206b-125"><span id="MCI_DGV_WINDOW_HWND"></span><span id="mci_dgv_window_hwnd"></span>MCI- \_ DGV- \_ Fenster ( \_ HWND)</span><span class="sxs-lookup"><span data-stu-id="8206b-125"><span id="MCI_DGV_WINDOW_HWND"></span><span id="mci_dgv_window_hwnd"></span>MCI\_DGV\_WINDOW\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="8206b-126">Das Handle des Fensters, das für die Verwendung als Ziel benötigt wird, ist im **HWND** -Member der durch *lpwindow* identifizierten Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="8206b-126">The handle of the window needed for use as the destination is included in the **hWnd** member of the structure identified by *lpWindow*.</span></span>

</dd> <dt>

<span data-ttu-id="8206b-127"><span id="MCI_DGV_WINDOW_STATE"></span><span id="mci_dgv_window_state"></span>Status des MCI- \_ DGV- \_ Fensters \_</span><span class="sxs-lookup"><span data-stu-id="8206b-127"><span id="MCI_DGV_WINDOW_STATE"></span><span id="mci_dgv_window_state"></span>MCI\_DGV\_WINDOW\_STATE</span></span>
</dt> <dd>

<span data-ttu-id="8206b-128">Der **nCmdShow** -Member der Struktur, die von *lpwindow* identifiziert wird, enthält Parameter zum Festlegen des Fenster Zustands.</span><span class="sxs-lookup"><span data-stu-id="8206b-128">The **nCmdShow** member of the structure identified by *lpWindow* contains parameters for setting the window state.</span></span>

</dd> <dt>

<span data-ttu-id="8206b-129"><span id="MCI_DGV_WINDOW_TEXT"></span><span id="mci_dgv_window_text"></span>MCI- \_ DGV- \_ Fenster \_ Text</span><span class="sxs-lookup"><span data-stu-id="8206b-129"><span id="MCI_DGV_WINDOW_TEXT"></span><span id="mci_dgv_window_text"></span>MCI\_DGV\_WINDOW\_TEXT</span></span>
</dt> <dd>

<span data-ttu-id="8206b-130">Der **lpstrautext** -Member der durch *lpwindow* identifizierten Struktur enthält die Adresse eines Puffers, der die in der Fenstertitelleiste verwendete Beschriftung enthält.</span><span class="sxs-lookup"><span data-stu-id="8206b-130">The **lpstrText** member of the structure identified by *lpWindow* contains an address of a buffer containing the caption used in the window title bar.</span></span>

</dd> </dl>

<span data-ttu-id="8206b-131">Für Digital Video-Geräte verweist der *lpwindow* -Parameter auf eine [**MCI- \_ DGV- \_ Fenster \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_window_parmsa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="8206b-131">For digital-video devices, the *lpWindow* parameter points to an [**MCI\_DGV\_WINDOW\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_window_parmsa) structure.</span></span>

<span data-ttu-id="8206b-132">Die folgenden zusätzlichen Flags werden mit dem **Überlagerungs** Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="8206b-132">The following additional flags are used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="8206b-133"><span id="MCI_OVLY_WINDOW_DISABLE_STRETCH"></span><span id="mci_ovly_window_disable_stretch"></span>MCI- \_ OVLY- \_ Fenster zum Deaktivieren der \_ \_ Streckung</span><span class="sxs-lookup"><span data-stu-id="8206b-133"><span id="MCI_OVLY_WINDOW_DISABLE_STRETCH"></span><span id="mci_ovly_window_disable_stretch"></span>MCI\_OVLY\_WINDOW\_DISABLE\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="8206b-134">Deaktiviert die Streckung des Bilds.</span><span class="sxs-lookup"><span data-stu-id="8206b-134">Disables stretching of the image.</span></span>

</dd> <dt>

<span data-ttu-id="8206b-135"><span id="MCI_OVLY_WINDOW_ENABLE_STRETCH"></span><span id="mci_ovly_window_enable_stretch"></span>MCI- \_ OVLY- \_ Fenster zum Aktivieren der \_ \_ Streckung</span><span class="sxs-lookup"><span data-stu-id="8206b-135"><span id="MCI_OVLY_WINDOW_ENABLE_STRETCH"></span><span id="mci_ovly_window_enable_stretch"></span>MCI\_OVLY\_WINDOW\_ENABLE\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="8206b-136">Ermöglicht das Stretching des Bilds.</span><span class="sxs-lookup"><span data-stu-id="8206b-136">Enables stretching of the image.</span></span>

</dd> <dt>

<span data-ttu-id="8206b-137"><span id="MCI_OVLY_WINDOW_HWND"></span><span id="mci_ovly_window_hwnd"></span>MCI \_ OVLY \_ Window \_ HWND</span><span class="sxs-lookup"><span data-stu-id="8206b-137"><span id="MCI_OVLY_WINDOW_HWND"></span><span id="mci_ovly_window_hwnd"></span>MCI\_OVLY\_WINDOW\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="8206b-138">Das Handle des Fensters, das für das Ziel verwendet wird, ist in das **HWND** -Element der von *lpwindow* identifizierten Struktur eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="8206b-138">The handle of the window used for the destination is included in the **hWnd** member of the structure identified by *lpWindow*.</span></span> <span data-ttu-id="8206b-139">Legen Sie dieses Flag auf MCI \_ OVLY \_ Window \_ default fest, um zum Standardfenster zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="8206b-139">Set this flag to MCI\_OVLY\_WINDOW\_DEFAULT to return to the default window.</span></span>

</dd> <dt>

<span data-ttu-id="8206b-140"><span id="MCI_OVLY_WINDOW_STATE"></span><span id="mci_ovly_window_state"></span>Status des MCI- \_ OVLY- \_ Fensters \_</span><span class="sxs-lookup"><span data-stu-id="8206b-140"><span id="MCI_OVLY_WINDOW_STATE"></span><span id="mci_ovly_window_state"></span>MCI\_OVLY\_WINDOW\_STATE</span></span>
</dt> <dd>

<span data-ttu-id="8206b-141">Der **nCmdShow** -Member der *lpwindow* -Struktur enthält Parameter zum Festlegen des Fenster Zustands.</span><span class="sxs-lookup"><span data-stu-id="8206b-141">The **nCmdShow** member of the *lpWindow* structure contains parameters for setting the window state.</span></span> <span data-ttu-id="8206b-142">Dieses Flag entspricht dem Aufrufen von [ShowWindow](/windows/win32/api/winuser/nf-winuser-showwindow) mit dem *State* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="8206b-142">This flag is equivalent to calling [ShowWindow](/windows/win32/api/winuser/nf-winuser-showwindow) with the *state* parameter.</span></span> <span data-ttu-id="8206b-143">Die Konstanten sind identisch mit den in Windows definierten Konstanten. H (z. b \_ . SW Hide, SW \_ minimieren oder SW \_ shownormal).</span><span class="sxs-lookup"><span data-stu-id="8206b-143">The constants are the same as those defined in WINDOWS.H (such as SW\_HIDE, SW\_MINIMIZE, or SW\_SHOWNORMAL).</span></span>

</dd> <dt>

<span data-ttu-id="8206b-144"><span id="MCI_OVLY_WINDOW_TEXT"></span><span id="mci_ovly_window_text"></span>Text des MCI- \_ OVLY- \_ Fensters \_</span><span class="sxs-lookup"><span data-stu-id="8206b-144"><span id="MCI_OVLY_WINDOW_TEXT"></span><span id="mci_ovly_window_text"></span>MCI\_OVLY\_WINDOW\_TEXT</span></span>
</dt> <dd>

<span data-ttu-id="8206b-145">Der **lpstrautext** -Member der durch *lpwindow* identifizierten Struktur enthält eine Adresse eines Puffers, der die für das Fenster verwendete Beschriftung enthält.</span><span class="sxs-lookup"><span data-stu-id="8206b-145">The **lpstrText** member of the structure identified by *lpWindow* contains an address of a buffer containing the caption used for the window.</span></span>

</dd> </dl>

<span data-ttu-id="8206b-146">Bei Video Überlagerungs Geräten zeigt der *lpwindow* -Parameter auf eine Struktur des [**MCI- \_ OVLY- \_ Fensters \_**](mci-ovly-window-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="8206b-146">For video-overlay devices, the *lpWindow* parameter points to an [**MCI\_OVLY\_WINDOW\_PARMS**](mci-ovly-window-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="8206b-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8206b-147">Requirements</span></span>



| <span data-ttu-id="8206b-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8206b-148">Requirement</span></span> | <span data-ttu-id="8206b-149">Wert</span><span class="sxs-lookup"><span data-stu-id="8206b-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8206b-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8206b-150">Minimum supported client</span></span><br/> | <span data-ttu-id="8206b-151">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8206b-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8206b-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8206b-152">Minimum supported server</span></span><br/> | <span data-ttu-id="8206b-153">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8206b-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8206b-154">Header</span><span class="sxs-lookup"><span data-stu-id="8206b-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="8206b-155"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8206b-155"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8206b-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8206b-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8206b-157">MCI</span><span class="sxs-lookup"><span data-stu-id="8206b-157">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8206b-158">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="8206b-158">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

