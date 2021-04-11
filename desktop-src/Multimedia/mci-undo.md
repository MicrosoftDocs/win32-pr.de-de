---
title: MCI_UNDO Befehl (MMSYSTEM. h)
description: Der Befehl MCI \_ Undo kehrt mit dem letzten erfolgreichen MCI-Befehl, dem MCI- \_ Kopiervorgang, dem \_ MCI DELETE-Befehl oder dem \_ MCI-Befehl " \_ Einfügen" zurück. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: 1593457a-e680-4732-a89e-00f4eff7605a
keywords:
- MCI_UNDO Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_UNDO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d099d95159afee8d91acb77eb64e8e80bee5425d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040221"
---
# <a name="mci_undo-command"></a><span data-ttu-id="8c54a-105">Befehl "MCI \_ Rückgängig"</span><span class="sxs-lookup"><span data-stu-id="8c54a-105">MCI\_UNDO command</span></span>

<span data-ttu-id="8c54a-106">Der Befehl MCI \_ Undo kehrt mit dem letzten erfolgreichen [MCI- \_ ](mci-cut.md)Befehl, dem MCI- [ \_ Kopier](mci-copy.md)Vorgang, dem [MCI \_ Delete](mci-delete.md)-Befehl oder dem MCI-Befehl " [ \_ Einfügen](mci-paste.md) " zurück.</span><span class="sxs-lookup"><span data-stu-id="8c54a-106">The MCI\_UNDO command reverses the most recent successful [MCI\_CUT](mci-cut.md), [MCI\_COPY](mci-copy.md), [MCI\_DELETE](mci-delete.md), or [MCI\_PASTE](mci-paste.md) command.</span></span> <span data-ttu-id="8c54a-107">Dieser Befehl wird von Digital-Video-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="8c54a-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="8c54a-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="8c54a-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UNDO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpUndo
);
```



## <a name="parameters"></a><span data-ttu-id="8c54a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c54a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c54a-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="8c54a-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="8c54a-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="8c54a-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="8c54a-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="8c54a-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="8c54a-113">MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="8c54a-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="8c54a-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="8c54a-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c54a-115"><span id="lpUndo"></span><span id="lpundo"></span><span id="LPUNDO"></span>*lpundo*</span><span class="sxs-lookup"><span data-stu-id="8c54a-115"><span id="lpUndo"></span><span id="lpundo"></span><span id="LPUNDO"></span>*lpUndo*</span></span>
</dt> <dd>

<span data-ttu-id="8c54a-116">Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="8c54a-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="8c54a-117">(Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="8c54a-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c54a-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c54a-118">Return Value</span></span>

<span data-ttu-id="8c54a-119">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="8c54a-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c54a-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c54a-120">Requirements</span></span>



| <span data-ttu-id="8c54a-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c54a-121">Requirement</span></span> | <span data-ttu-id="8c54a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="8c54a-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c54a-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8c54a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8c54a-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c54a-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8c54a-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8c54a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8c54a-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c54a-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8c54a-127">Header</span><span class="sxs-lookup"><span data-stu-id="8c54a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c54a-128"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c54a-128"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c54a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c54a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c54a-130">MCI</span><span class="sxs-lookup"><span data-stu-id="8c54a-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8c54a-131">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="8c54a-131">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

