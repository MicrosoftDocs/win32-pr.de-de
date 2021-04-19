---
title: MCI_ESCAPE Befehl (MMSYSTEM. h)
description: Der MCI- \_ Befehl "Escape" sendet eine Zeichenfolge direkt an das Gerät. Videodisk-Geräte erkennen diesen Befehl.
ms.assetid: 56ebc717-f0f7-4612-8e51-57b13ff9d42b
keywords:
- MCI_ESCAPE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_ESCAPE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab4bcd55590cb1b2cab5482eeb921118531002c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339986"
---
# <a name="mci_escape-command"></a><span data-ttu-id="9fabb-105">MCI- \_ escapebefehl</span><span class="sxs-lookup"><span data-stu-id="9fabb-105">MCI\_ESCAPE command</span></span>

<span data-ttu-id="9fabb-106">Der MCI- \_ Befehl "Escape" sendet eine Zeichenfolge direkt an das Gerät.</span><span class="sxs-lookup"><span data-stu-id="9fabb-106">The MCI\_ESCAPE command sends a string directly to the device.</span></span> <span data-ttu-id="9fabb-107">Videodisk-Geräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="9fabb-107">Videodisc devices recognize this command.</span></span>

<span data-ttu-id="9fabb-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="9fabb-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_ESCAPE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_VD_ESCAPE_PARMS) lpEscape
);
```



## <a name="parameters"></a><span data-ttu-id="9fabb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9fabb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fabb-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="9fabb-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="9fabb-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="9fabb-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="9fabb-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="9fabb-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="9fabb-113">MCI- \_ Benachrichtigung oder MCI- \_ Wartezeit.</span><span class="sxs-lookup"><span data-stu-id="9fabb-113">MCI\_NOTIFY or MCI\_WAIT.</span></span> <span data-ttu-id="9fabb-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="9fabb-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="9fabb-115"><span id="lpEscape"></span><span id="lpescape"></span><span id="LPESCAPE"></span>*lpescape*</span><span class="sxs-lookup"><span data-stu-id="9fabb-115"><span id="lpEscape"></span><span id="lpescape"></span><span id="LPESCAPE"></span>*lpEscape*</span></span>
</dt> <dd>

<span data-ttu-id="9fabb-116">Zeiger auf eine [**MCI- \_ VD \_ \_**](mci-vd-escape-parms.md) -escapeparameterstruktur.</span><span class="sxs-lookup"><span data-stu-id="9fabb-116">Pointer to an [**MCI\_VD\_ESCAPE\_PARMS**](mci-vd-escape-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fabb-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9fabb-117">Return Value</span></span>

<span data-ttu-id="9fabb-118">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="9fabb-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fabb-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9fabb-119">Remarks</span></span>

<span data-ttu-id="9fabb-120">Die mit der MCI-Escapesequenz gesendeten Daten \_ sind Geräte abhängig und werden normalerweise direkt an die dem Gerät zugeordnete Hardware übermittelt.</span><span class="sxs-lookup"><span data-stu-id="9fabb-120">The data sent with MCI\_ESCAPE is device-dependent and is usually passed directly to the hardware associated with the device.</span></span>

<span data-ttu-id="9fabb-121">Das folgende zusätzliche Flag gilt für Videodisk-Geräte:</span><span class="sxs-lookup"><span data-stu-id="9fabb-121">The following additional flag applies to videodisc devices:</span></span>

<dl> <dt>

<span data-ttu-id="9fabb-122"><span id="MCI_VD_ESCAPE_STRING"></span><span id="mci_vd_escape_string"></span>MCI VD-Escapesequenz \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="9fabb-122"><span id="MCI_VD_ESCAPE_STRING"></span><span id="mci_vd_escape_string"></span>MCI\_VD\_ESCAPE\_STRING</span></span>
</dt> <dd>

<span data-ttu-id="9fabb-123">Eine Befehls Zeichenfolge wird im **lpstrecommand** -Member der von *lpescape* identifizierten Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="9fabb-123">A command string is specified in the **lpstrCommand** member of the structure identified by *lpEscape*.</span></span> <span data-ttu-id="9fabb-124">Dieses Flag ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9fabb-124">This flag is required.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9fabb-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9fabb-125">Requirements</span></span>



| <span data-ttu-id="9fabb-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9fabb-126">Requirement</span></span> | <span data-ttu-id="9fabb-127">Wert</span><span class="sxs-lookup"><span data-stu-id="9fabb-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fabb-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9fabb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9fabb-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9fabb-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9fabb-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9fabb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9fabb-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9fabb-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9fabb-132">Header</span><span class="sxs-lookup"><span data-stu-id="9fabb-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fabb-133"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9fabb-133"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fabb-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fabb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fabb-135">MCI</span><span class="sxs-lookup"><span data-stu-id="9fabb-135">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="9fabb-136">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="9fabb-136">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

