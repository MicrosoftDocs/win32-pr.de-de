---
title: MCI_CONFIGURE Befehl (MMSYSTEM. h)
description: Mit dem Befehl MCI \_ configure wird ein Dialogfeld zum Festlegen der Betriebs Optionen angezeigt. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: 92683579-e6af-42a7-8a0f-6b88b04441f2
keywords:
- MCI_CONFIGURE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_CONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f752f17ac0d0a5c04edf628edfb6c04a339783f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391574"
---
# <a name="mci_configure-command"></a><span data-ttu-id="c9c1c-105">MCI- \_ Befehl "configure"</span><span class="sxs-lookup"><span data-stu-id="c9c1c-105">MCI\_CONFIGURE command</span></span>

<span data-ttu-id="c9c1c-106">Mit dem Befehl MCI \_ configure wird ein Dialogfeld zum Festlegen der Betriebs Optionen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c9c1c-106">The MCI\_CONFIGURE command displays a dialog box for setting the operating options.</span></span> <span data-ttu-id="c9c1c-107">Dieser Befehl wird von Digital-Video-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="c9c1c-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="c9c1c-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="c9c1c-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CONFIGURE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpConfigure
);
```



## <a name="parameters"></a><span data-ttu-id="c9c1c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9c1c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9c1c-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="c9c1c-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c9c1c-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="c9c1c-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="c9c1c-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="c9c1c-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c9c1c-113">MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="c9c1c-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="c9c1c-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c9c1c-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9c1c-115"><span id="lpConfigure"></span><span id="lpconfigure"></span><span id="LPCONFIGURE"></span>*lpconfigure*</span><span class="sxs-lookup"><span data-stu-id="c9c1c-115"><span id="lpConfigure"></span><span id="lpconfigure"></span><span id="LPCONFIGURE"></span>*lpConfigure*</span></span>
</dt> <dd>

<span data-ttu-id="c9c1c-116">Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="c9c1c-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="c9c1c-117">(Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="c9c1c-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9c1c-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c9c1c-118">Return Value</span></span>

<span data-ttu-id="c9c1c-119">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="c9c1c-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9c1c-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9c1c-120">Requirements</span></span>



| <span data-ttu-id="c9c1c-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9c1c-121">Requirement</span></span> | <span data-ttu-id="c9c1c-122">Wert</span><span class="sxs-lookup"><span data-stu-id="c9c1c-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9c1c-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c9c1c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c9c1c-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9c1c-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c9c1c-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c9c1c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c9c1c-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9c1c-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c9c1c-127">Header</span><span class="sxs-lookup"><span data-stu-id="c9c1c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9c1c-128"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9c1c-128"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9c1c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9c1c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9c1c-130">MCI</span><span class="sxs-lookup"><span data-stu-id="c9c1c-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c9c1c-131">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="c9c1c-131">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

