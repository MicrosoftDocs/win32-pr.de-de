---
title: MCI_SYSINFO Befehl (MMSYSTEM. h)
description: Der MCI- \_ Befehl sysinfo Ruft Informationen zu MCI-Geräten ab.
ms.assetid: 605efd25-8849-42aa-99fd-b36b6fd2c7b7
keywords:
- MCI_SYSINFO Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_SYSINFO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e722625449893771726a83738c3b0d7bc8bc523c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956577"
---
# <a name="mci_sysinfo-command"></a><span data-ttu-id="cfbaa-104">MCI- \_ sysinfo-Befehl</span><span class="sxs-lookup"><span data-stu-id="cfbaa-104">MCI\_SYSINFO command</span></span>

<span data-ttu-id="cfbaa-105">Der MCI- \_ Befehl sysinfo Ruft Informationen zu MCI-Geräten ab.</span><span class="sxs-lookup"><span data-stu-id="cfbaa-105">The MCI\_SYSINFO command retrieves information about MCI devices.</span></span> <span data-ttu-id="cfbaa-106">MCI unterstützt diesen Befehl direkt, anstatt ihn an das Gerät zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="cfbaa-106">MCI supports this command directly rather than passing it to the device.</span></span> <span data-ttu-id="cfbaa-107">Alle MCI-Anwendungen können diesen Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="cfbaa-107">Any MCI application can use this command.</span></span> <span data-ttu-id="cfbaa-108">Zeichen folgen Informationen werden im von der Anwendung bereitgestellten Puffer zurückgegeben, auf den der **lpstraureturn** -Member der Struktur verweist, die von *lpsysinfo* identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="cfbaa-108">String information is returned in the application-supplied buffer pointed to by the **lpstrReturn** member of the structure identified by *lpSysInfo*.</span></span> <span data-ttu-id="cfbaa-109">Numerische Informationen werden als **DWORD** -Wert zurückgegeben, der in den von der Anwendung bereitgestellten Puffer eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="cfbaa-109">Numeric information is returned as a **DWORD** value placed in the application-supplied buffer.</span></span> <span data-ttu-id="cfbaa-110">Der **dwretsize** -Member gibt die Länge des Puffers an.</span><span class="sxs-lookup"><span data-stu-id="cfbaa-110">The **dwRetSize** member specifies the buffer length.</span></span>

<span data-ttu-id="cfbaa-111">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="cfbaa-111">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SYSINFO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SYSINFO_PARMS) lpSysInfo
);
```



## <a name="parameters"></a><span data-ttu-id="cfbaa-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="cfbaa-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfbaa-113"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="cfbaa-113"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="cfbaa-114">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="cfbaa-114">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="cfbaa-115"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="cfbaa-115"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="cfbaa-116">Eines oder mehrere der folgenden Standard-und Befehls spezifischen Flags:</span><span class="sxs-lookup"><span data-stu-id="cfbaa-116">One or more of the following standard and command-specific flags:</span></span>

</dd> <dt>

<span data-ttu-id="cfbaa-117"><span id="MCI_SYSINFO_INSTALLNAME"></span><span id="mci_sysinfo_installname"></span>MCI- \_ sysinfo- \_ installname</span><span class="sxs-lookup"><span data-stu-id="cfbaa-117"><span id="MCI_SYSINFO_INSTALLNAME"></span><span id="mci_sysinfo_installname"></span>MCI\_SYSINFO\_INSTALLNAME</span></span>
</dt> <dd>

<span data-ttu-id="cfbaa-118">Ruft den Namen (aufgelistet in der Registrierung oder der SYSTEM.INI Datei) ab, der zur Installation des Geräts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cfbaa-118">Obtains the name (listed in the registry or the SYSTEM.INI file) used to install the device.</span></span>

</dd> <dt>

<span data-ttu-id="cfbaa-119"><span id="MCI_SYSINFO_NAME"></span><span id="mci_sysinfo_name"></span>MCI- \_ sysinfo- \_ Name</span><span class="sxs-lookup"><span data-stu-id="cfbaa-119"><span id="MCI_SYSINFO_NAME"></span><span id="mci_sysinfo_name"></span>MCI\_SYSINFO\_NAME</span></span>
</dt> <dd>

<span data-ttu-id="cfbaa-120">Erhält einen Gerätenamen, der der Gerätenummer entspricht, die im **dwnumber** -Member der von **lpsysinfo** identifizierten Struktur angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="cfbaa-120">Obtains a device name corresponding to the device number specified in the **dwNumber** member of the structure identified by **lpSysInfo**.</span></span> <span data-ttu-id="cfbaa-121">Wenn das MCI- \_ Flag zum \_ Öffnen von sysinfo festgelegt ist, gibt MCI die Namen offener Geräte zurück.</span><span class="sxs-lookup"><span data-stu-id="cfbaa-121">If the MCI\_SYSINFO\_OPEN flag is set, MCI returns the names of open devices.</span></span>

</dd> <dt>

<span data-ttu-id="cfbaa-122"><span id="MCI_SYSINFO_OPEN"></span><span id="mci_sysinfo_open"></span>MCI- \_ sysinfo \_ geöffnet</span><span class="sxs-lookup"><span data-stu-id="cfbaa-122"><span id="MCI_SYSINFO_OPEN"></span><span id="mci_sysinfo_open"></span>MCI\_SYSINFO\_OPEN</span></span>
</dt> <dd>

<span data-ttu-id="cfbaa-123">Ruft die Menge oder den Namen offener Geräte ab.</span><span class="sxs-lookup"><span data-stu-id="cfbaa-123">Obtains the quantity or name of open devices.</span></span>

</dd> <dt>

<span data-ttu-id="cfbaa-124"><span id="MCI_SYSINFO_QUANTITY"></span><span id="mci_sysinfo_quantity"></span>MCI- \_ sysinfo- \_ Menge</span><span class="sxs-lookup"><span data-stu-id="cfbaa-124"><span id="MCI_SYSINFO_QUANTITY"></span><span id="mci_sysinfo_quantity"></span>MCI\_SYSINFO\_QUANTITY</span></span>
</dt> <dd>

<span data-ttu-id="cfbaa-125">Ruft die Anzahl der Geräte des angegebenen Typs ab, die in der Registrierung oder im \[ MCI- \] Abschnitt der SYSTEM.INI Datei aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="cfbaa-125">Obtains the number of devices of the specified type that are listed in the registry or the \[mci\] section of the SYSTEM.INI file.</span></span> <span data-ttu-id="cfbaa-126">Wenn das \_ geöffnende MCI-sysinfo- \_ Flag festgelegt ist, wird die Anzahl der geöffneten Geräte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cfbaa-126">If the MCI\_SYSINFO\_OPEN flag is set, the number of open devices is returned.</span></span>

</dd> <dt>

<span data-ttu-id="cfbaa-127"><span id="lpSysInfo"></span><span id="lpsysinfo"></span><span id="LPSYSINFO"></span>*lpsysinfo*</span><span class="sxs-lookup"><span data-stu-id="cfbaa-127"><span id="lpSysInfo"></span><span id="lpsysinfo"></span><span id="LPSYSINFO"></span>*lpSysInfo*</span></span>
</dt> <dd>

<span data-ttu-id="cfbaa-128">Zeiger auf eine [**MCI- \_ sysinfo \_**](mci-sysinfo-parms.md) -Elementstruktur.</span><span class="sxs-lookup"><span data-stu-id="cfbaa-128">Pointer to an [**MCI\_SYSINFO\_PARMS**](mci-sysinfo-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfbaa-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cfbaa-129">Return Value</span></span>

<span data-ttu-id="cfbaa-130">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="cfbaa-130">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfbaa-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cfbaa-131">Remarks</span></span>

<span data-ttu-id="cfbaa-132">Der **wdevicetype** -Member der durch *lpsysinfo* identifizierten Struktur wird verwendet, um den Gerätetyp der Abfrage anzugeben.</span><span class="sxs-lookup"><span data-stu-id="cfbaa-132">The **wDeviceType** member of the structure identified by *lpSysInfo* is used to indicate the device type of the query.</span></span> <span data-ttu-id="cfbaa-133">Wenn der *WDE viceid* -Parameter auf MCI \_ all Device ID festgelegt ist, wird \_ \_ der Wert von **wdebug Type** überschrieben.</span><span class="sxs-lookup"><span data-stu-id="cfbaa-133">If the *wDeviceID* parameter is set to MCI\_ALL\_DEVICE\_ID, it overrides the value of **wDeviceType**.</span></span> <span data-ttu-id="cfbaa-134">Eine Liste der Gerätetypen finden Sie unter [MCI-Gerätetypen](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="cfbaa-134">For a list of device types, see [MCI Device Types](mci-device-types.md).</span></span>

<span data-ttu-id="cfbaa-135">Ganzzahlige Rückgabewerte sind im Puffer zurückgegebene **DWORD** -Werte, auf die durch den **lpstraureturn** -Member der durch *lpsysinfo* identifizierten Struktur verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="cfbaa-135">Integer return values are **DWORD** values returned in the buffer pointed to by the **lpstrReturn** member of the structure identified by *lpSysInfo*.</span></span>

<span data-ttu-id="cfbaa-136">Zeichen folgen Rückgabewerte sind im Puffer zurückgegebene NULL-terminierte Zeichen folgen, auf die durch den **lpstrreturn** -Member der durch *lpsysinfo* identifizierten Struktur verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="cfbaa-136">String return values are null-terminated strings returned in the buffer pointed to by the **lpstrReturn** member of the structure identified by *lpSysInfo*.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfbaa-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfbaa-137">Requirements</span></span>



| <span data-ttu-id="cfbaa-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cfbaa-138">Requirement</span></span> | <span data-ttu-id="cfbaa-139">Wert</span><span class="sxs-lookup"><span data-stu-id="cfbaa-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfbaa-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cfbaa-140">Minimum supported client</span></span><br/> | <span data-ttu-id="cfbaa-141">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cfbaa-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cfbaa-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cfbaa-142">Minimum supported server</span></span><br/> | <span data-ttu-id="cfbaa-143">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cfbaa-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cfbaa-144">Header</span><span class="sxs-lookup"><span data-stu-id="cfbaa-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfbaa-145"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cfbaa-145"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfbaa-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfbaa-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfbaa-147">MCI</span><span class="sxs-lookup"><span data-stu-id="cfbaa-147">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="cfbaa-148">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="cfbaa-148">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

