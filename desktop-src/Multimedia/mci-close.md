---
title: MCI_CLOSE Befehl (MMSYSTEM. h)
description: Der Befehl zum \_ Schließen von MCI gibt den Zugriff auf ein Gerät oder eine Datei frei. Alle Geräte erkennen diesen Befehl.
ms.assetid: 62dadd90-e8fc-4bdd-9f8c-f9ea9ff5550f
keywords:
- MCI_CLOSE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 417129595405aeb6c9a2345eb9c3f03f1e2731e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103443"
---
# <a name="mci_close-command"></a><span data-ttu-id="60e96-105">Befehl zum Schließen von MCI \_</span><span class="sxs-lookup"><span data-stu-id="60e96-105">MCI\_CLOSE command</span></span>

<span data-ttu-id="60e96-106">Der Befehl zum \_ Schließen von MCI gibt den Zugriff auf ein Gerät oder eine Datei frei.</span><span class="sxs-lookup"><span data-stu-id="60e96-106">The MCI\_CLOSE command releases access to a device or file.</span></span> <span data-ttu-id="60e96-107">Alle Geräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="60e96-107">All devices recognize this command.</span></span>

<span data-ttu-id="60e96-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="60e96-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CLOSE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpClose
);
```



## <a name="parameters"></a><span data-ttu-id="60e96-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="60e96-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60e96-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="60e96-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="60e96-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="60e96-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="60e96-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="60e96-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="60e96-113">MCI- \_ Benachrichtigung oder MCI- \_ Wartezeit.</span><span class="sxs-lookup"><span data-stu-id="60e96-113">MCI\_NOTIFY or MCI\_WAIT.</span></span> <span data-ttu-id="60e96-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="60e96-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="60e96-115"><span id="lpClose"></span><span id="lpclose"></span><span id="LPCLOSE"></span>*lpclose*</span><span class="sxs-lookup"><span data-stu-id="60e96-115"><span id="lpClose"></span><span id="lpclose"></span><span id="LPCLOSE"></span>*lpClose*</span></span>
</dt> <dd>

<span data-ttu-id="60e96-116">Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="60e96-116">Pointer to an [**MCI\_ GENERIC\_ PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="60e96-117">(Sie können auch eine MCI-Struktur zum **\_ Schließen von \_ Parametern** verwenden.</span><span class="sxs-lookup"><span data-stu-id="60e96-117">(You can also use an **MCI\_CLOSE\_PARMS** structure.</span></span> <span data-ttu-id="60e96-118">Weitere Informationen finden Sie in den Kommentaren zu **generischen MCI- \_ \_ Parametern**.)</span><span class="sxs-lookup"><span data-stu-id="60e96-118">For more information, see the comments for **MCI\_GENERIC\_PARMS**.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60e96-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="60e96-119">Return Value</span></span>

<span data-ttu-id="60e96-120">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="60e96-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="60e96-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60e96-121">Remarks</span></span>

<span data-ttu-id="60e96-122">Wenn Sie eine Anwendung beenden, ohne die geöffneten MCI-Geräte zu schließen, kann das Gerät nicht mehr zugänglich sein.</span><span class="sxs-lookup"><span data-stu-id="60e96-122">Exiting an application without closing any MCI devices it has opened can leave the device inaccessible.</span></span> <span data-ttu-id="60e96-123">Die Anwendung sollte jedes Gerät oder jede Datei explizit schließen, wenn Sie damit fertig ist.</span><span class="sxs-lookup"><span data-stu-id="60e96-123">Your application should explicitly close each device or file when it is finished with it.</span></span> <span data-ttu-id="60e96-124">MCI entlädt das Gerät, wenn alle Instanzen des Geräts oder alle zugehörigen Dateien geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="60e96-124">MCI unloads the device when all instances of the device or all associated files are closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="60e96-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60e96-125">Requirements</span></span>



| <span data-ttu-id="60e96-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60e96-126">Requirement</span></span> | <span data-ttu-id="60e96-127">Wert</span><span class="sxs-lookup"><span data-stu-id="60e96-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60e96-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60e96-128">Minimum supported client</span></span><br/> | <span data-ttu-id="60e96-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60e96-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="60e96-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="60e96-130">Minimum supported server</span></span><br/> | <span data-ttu-id="60e96-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60e96-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="60e96-132">Header</span><span class="sxs-lookup"><span data-stu-id="60e96-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="60e96-133"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="60e96-133"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60e96-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60e96-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60e96-135">MCI</span><span class="sxs-lookup"><span data-stu-id="60e96-135">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="60e96-136">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="60e96-136">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

