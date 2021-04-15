---
title: MCI_BREAK Befehl (MMSYSTEM. h)
description: Der MCI- \_ break-Befehl legt einen Break Key für ein MCI-Gerät fest. MCI unterstützt diesen Befehl direkt, anstatt ihn an das Gerät zu übergeben. Alle MCI-Anwendungen können diesen Befehl verwenden.
ms.assetid: 127b5179-2838-4bde-8d0c-37a4cc87fa4d
keywords:
- MCI_BREAK Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_BREAK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33b17e3796192344ef974fed1af7229d41746aaf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476239"
---
# <a name="mci_break-command"></a><span data-ttu-id="c1383-106">MCI- \_ break-Befehl</span><span class="sxs-lookup"><span data-stu-id="c1383-106">MCI\_BREAK command</span></span>

<span data-ttu-id="c1383-107">Der MCI- \_ break-Befehl legt einen Break Key für ein MCI-Gerät fest.</span><span class="sxs-lookup"><span data-stu-id="c1383-107">The MCI\_BREAK command sets a break key for an MCI device.</span></span> <span data-ttu-id="c1383-108">MCI unterstützt diesen Befehl direkt, anstatt ihn an das Gerät zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="c1383-108">MCI supports this command directly rather than passing it to the device.</span></span> <span data-ttu-id="c1383-109">Alle MCI-Anwendungen können diesen Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="c1383-109">Any MCI application can use this command.</span></span>

<span data-ttu-id="c1383-110">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="c1383-110">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_BREAK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_BREAK_PARMS) lpBreak
);
```



## <a name="parameters"></a><span data-ttu-id="c1383-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1383-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1383-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="c1383-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c1383-113">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="c1383-113">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="c1383-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="c1383-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c1383-115">MCI \_ -Benachrichtigung, MCI \_ -Wartezeit oder, für Digital Video-und Video-Kassettenrecorder-Geräte (VCR), MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="c1383-115">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and video-cassette recorder (VCR) devices, MCI\_TEST.</span></span> <span data-ttu-id="c1383-116">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c1383-116">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1383-117"><span id="lpBreak"></span><span id="lpbreak"></span><span id="LPBREAK"></span>*lpbreak*</span><span class="sxs-lookup"><span data-stu-id="c1383-117"><span id="lpBreak"></span><span id="lpbreak"></span><span id="LPBREAK"></span>*lpBreak*</span></span>
</dt> <dd>

<span data-ttu-id="c1383-118">Zeiger auf eine [**MCI-unter \_ Brechung \_**](mci-break-parms.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c1383-118">Pointer to an [**MCI\_ BREAK\_PARMS**](mci-break-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1383-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1383-119">Return Value</span></span>

<span data-ttu-id="c1383-120">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="c1383-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1383-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1383-121">Remarks</span></span>

<span data-ttu-id="c1383-122">Sie müssen möglicherweise mehrmals die Unterbrechungs Taste drücken, um einen Warte Vorgang zu unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="c1383-122">You might have to press the break key multiple times to interrupt a wait operation.</span></span> <span data-ttu-id="c1383-123">Das Drücken der Pause-Taste, nachdem ein Geräte Wartezeit abgebrochen wurde, kann die Unterbrechung an eine Anwendung senden.</span><span class="sxs-lookup"><span data-stu-id="c1383-123">Pressing the break key after a device wait is canceled can send the break to an application.</span></span> <span data-ttu-id="c1383-124">Wenn für eine Anwendung eine Aktion definiert ist, die für den Code des virtuellen Schlüssels definiert ist, kann Sie versehentlich auf die Unterbrechung reagieren.</span><span class="sxs-lookup"><span data-stu-id="c1383-124">If an application has an action defined for the virtual-key code, then it can inadvertently respond to the break.</span></span> <span data-ttu-id="c1383-125">Beispielsweise kann eine Anwendung, \_ die den VK-Abbruch für eine Zugriffstaste verwendet, auf die Standard Taste Strg + Pause reagieren, wenn Sie nach dem Abbrechen eines warte Vorgangs gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="c1383-125">For example, an application using VK\_CANCEL for an accelerator key can respond to the default CTRL+BREAK key if it is pressed after a wait is canceled.</span></span>

<span data-ttu-id="c1383-126">Die folgenden zusätzlichen Flags gelten für alle Geräte:</span><span class="sxs-lookup"><span data-stu-id="c1383-126">The following additional flags apply to all devices:</span></span>

<dl> <dt>

<span data-ttu-id="c1383-127"><span id="MCI_BREAK_HWND"></span><span id="mci_break_hwnd"></span>MCI- \_ break- \_ HWND</span><span class="sxs-lookup"><span data-stu-id="c1383-127"><span id="MCI_BREAK_HWND"></span><span id="mci_break_hwnd"></span>MCI\_BREAK\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="c1383-128">Der **hwndbreak** -Member der durch *lpbreak* identifizierten Struktur enthält ein Fenster Handle, das das aktuelle Fenster sein muss, um die Unterbrechung für dieses MCI-Gerät zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c1383-128">The **hwndBreak** member of the structure identified by *lpBreak* contains a window handle that must be the current window in order to enable break detection for that MCI device.</span></span> <span data-ttu-id="c1383-129">Dies ist normalerweise das Hauptfenster der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c1383-129">This is usually the application's main window.</span></span> <span data-ttu-id="c1383-130">Wenn dieser nicht ausgelassen wird, überprüft MCI nicht das Fenster Handle des aktuellen Fensters.</span><span class="sxs-lookup"><span data-stu-id="c1383-130">If omitted, MCI does not check the window handle of the current window.</span></span>

</dd> <dt>

<span data-ttu-id="c1383-131"><span id="MCI_BREAK_KEY"></span><span id="mci_break_key"></span>MCI- \_ break- \_ Taste</span><span class="sxs-lookup"><span data-stu-id="c1383-131"><span id="MCI_BREAK_KEY"></span><span id="mci_break_key"></span>MCI\_BREAK\_KEY</span></span>
</dt> <dd>

<span data-ttu-id="c1383-132">Der **nvirtkey** -Member der durch *lpbreak* identifizierten Struktur gibt den Code für den virtuellen Schlüssel an, der für die Pause-Taste verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c1383-132">The **nVirtKey** member of the structure identified by *lpBreak* specifies the virtual-key code used for the break key.</span></span> <span data-ttu-id="c1383-133">Standardmäßig weist MCI STRG + Unterbrechung als Break Key zu.</span><span class="sxs-lookup"><span data-stu-id="c1383-133">By default, MCI assigns CTRL+BREAK as the break key.</span></span> <span data-ttu-id="c1383-134">Dieses Flag ist erforderlich, wenn die MCI-unter \_ Brechung \_ nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c1383-134">This flag is required if MCI\_BREAK\_OFF is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="c1383-135"><span id="MCI_BREAK_OFF"></span><span id="mci_break_off"></span>MCI-unter \_ Brechung \_</span><span class="sxs-lookup"><span data-stu-id="c1383-135"><span id="MCI_BREAK_OFF"></span><span id="mci_break_off"></span>MCI\_BREAK\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="c1383-136">Deaktiviert alle vorhandenen Break-Schlüssel für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="c1383-136">Disables any existing break key for the indicated device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c1383-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1383-137">Requirements</span></span>



| <span data-ttu-id="c1383-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1383-138">Requirement</span></span> | <span data-ttu-id="c1383-139">Wert</span><span class="sxs-lookup"><span data-stu-id="c1383-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1383-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c1383-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c1383-141">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1383-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c1383-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c1383-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c1383-143">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1383-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c1383-144">Header</span><span class="sxs-lookup"><span data-stu-id="c1383-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1383-145"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1383-145"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1383-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1383-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1383-147">MCI</span><span class="sxs-lookup"><span data-stu-id="c1383-147">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c1383-148">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="c1383-148">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

