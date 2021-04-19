---
title: sysinfo-Befehl
description: Der sysinfo-Befehl ruft MCI-Systeminformationen ab. Der sysinfo-Befehl ist ein MCI-Systembefehl. Sie wird direkt von MCI interpretiert.
ms.assetid: 494e8976-aac3-4d9f-b14b-3d3fd1917b45
keywords:
- sysinfo-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- sysinfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4751a5633462afe1ca8e8cd9abee1afeb16ac242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342479"
---
# <a name="sysinfo-command"></a><span data-ttu-id="becbe-105">sysinfo-Befehl</span><span class="sxs-lookup"><span data-stu-id="becbe-105">sysinfo command</span></span>

<span data-ttu-id="becbe-106">Der sysinfo-Befehl ruft MCI-Systeminformationen ab.</span><span class="sxs-lookup"><span data-stu-id="becbe-106">The sysinfo command retrieves MCI system information.</span></span> <span data-ttu-id="becbe-107">Der sysinfo-Befehl ist ein MCI-Systembefehl. Sie wird direkt von MCI interpretiert.</span><span class="sxs-lookup"><span data-stu-id="becbe-107">The sysinfo command is an MCI system command; it is interpreted directly by MCI.</span></span>

<span data-ttu-id="becbe-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="becbe-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("sysinfo %s %s %s"), 
  lpszDeviceID, 
  lpszRequest, 
  lpszFlags
);
```

## <a name="parameters"></a><span data-ttu-id="becbe-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="becbe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="becbe-110">*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="becbe-110">*lpszDeviceID*</span></span> 
</dt> <dd>

<span data-ttu-id="becbe-111">Der Bezeichner eines MCI-Geräts oder-Gerätetyps.</span><span class="sxs-lookup"><span data-stu-id="becbe-111">Identifier of an MCI device or device type.</span></span> <span data-ttu-id="becbe-112">Wenn ein Gerätetyp angegeben wird, muss es sich um einen standardmäßigen MCI-Gerätetyp Namen handeln, wie im Referenzmaterial für [**den Funktions**](capability.md) Befehl aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="becbe-112">If a device type is specified, it must be a standard MCI device-type name, as listed in the reference material for the [**capability**](capability.md) command.</span></span> <span data-ttu-id="becbe-113">Sie können "All" angeben, wenn das in *lpszrequest* angegebene Flag diese Möglichkeit zulässt.</span><span class="sxs-lookup"><span data-stu-id="becbe-113">You can specify "all" when the flag specified in *lpszRequest* allows that possibility.</span></span>

</dd> <dt>

<span data-ttu-id="becbe-114">*lpszrequest*</span><span class="sxs-lookup"><span data-stu-id="becbe-114">*lpszRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="becbe-115">Eines der folgenden Flags.</span><span class="sxs-lookup"><span data-stu-id="becbe-115">One of the following flags.</span></span>



| <span data-ttu-id="becbe-116">Wert</span><span class="sxs-lookup"><span data-stu-id="becbe-116">Value</span></span>                                                                                                                                                                | <span data-ttu-id="becbe-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="becbe-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="installname"></span><span id="INSTALLNAME"></span><dl> <span data-ttu-id="becbe-118"><dt>**installname**</dt></span><span class="sxs-lookup"><span data-stu-id="becbe-118"><dt>**installname**</dt></span></span> </dl>               | <span data-ttu-id="becbe-119">Gibt den Namen zurück, der in der Registrierung aufgeführt ist, oder die SYSTEM.INI Datei, die zum Installieren des geöffneten Geräts mit der angegebenen Gerätekennung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="becbe-119">Returns the name listed in the registry or the SYSTEM.INI file used to install the open device with the specified device identifier.</span></span><br/>                                                                                                                                                                                                            |
| <span id="quantity"></span><span id="QUANTITY"></span><dl> <span data-ttu-id="becbe-120"><dt>**Mess**</dt></span><span class="sxs-lookup"><span data-stu-id="becbe-120"><dt>**quantity**</dt></span></span> </dl>                        | <span data-ttu-id="becbe-121">Gibt die Anzahl der in der Registrierung aufgelisteten MCI-Geräte oder die SYSTEM.INI Datei des im *lpszdeviceid* -Parameter angegebenen Typs zurück.</span><span class="sxs-lookup"><span data-stu-id="becbe-121">Returns the number of MCI devices listed in the registry or the SYSTEM.INI file of the type specified in the *lpszDeviceID* parameter.</span></span> <span data-ttu-id="becbe-122">Bei dieser Gerätekennung muss es sich um einen standardmäßigen MCI-Gerätetyp Namen handeln.</span><span class="sxs-lookup"><span data-stu-id="becbe-122">This device identifier must be a standard MCI device-type name.</span></span> <span data-ttu-id="becbe-123">Alle Ziffern nach dem Gerätetyp werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="becbe-123">Any digits after the device type are ignored.</span></span> <span data-ttu-id="becbe-124">Bei Angabe von "All" für *lpszde viceid* wird die Gesamtzahl der MCI-Geräte im System zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="becbe-124">Specifying "all" for *lpszDeviceID* returns the total number of MCI devices in the system.</span></span><br/> |
| <span id="quantity_open"></span><span id="QUANTITY_OPEN"></span><dl> <span data-ttu-id="becbe-125"><dt>**Menge geöffnet**</dt></span><span class="sxs-lookup"><span data-stu-id="becbe-125"><dt>**quantity open**</dt></span></span> </dl>         | <span data-ttu-id="becbe-126">Gibt die Anzahl der geöffneten MCI-Geräte des in " *lpszdeviceid*" angegebenen Typs zurück.</span><span class="sxs-lookup"><span data-stu-id="becbe-126">Returns the number of open MCI devices of the type specified in *lpszDeviceID*.</span></span> <span data-ttu-id="becbe-127">Bei dieser Gerätekennung muss es sich um einen standardmäßigen MCI-Gerätetyp Namen handeln.</span><span class="sxs-lookup"><span data-stu-id="becbe-127">This device identifier must be a standard MCI device-type name.</span></span> <span data-ttu-id="becbe-128">Bei Angabe von "All" für *lpsztoviceid* wird die Gesamtzahl der geöffneten MCI-Geräte im System zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="becbe-128">Specifying "all" for *lpszDeviceID* returns the total number of open MCI devices in the system.</span></span><br/>                                                                                                 |
| <span id="name_index"></span><span id="NAME_INDEX"></span><dl> <span data-ttu-id="becbe-129"><dt>\* \* Name \* Index \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="becbe-129"><dt>\*\*name \*index\*\*\*</dt></span></span> </dl>                | <span data-ttu-id="becbe-130">Gibt den Namen eines MCI-Geräts zurück.</span><span class="sxs-lookup"><span data-stu-id="becbe-130">Returns the name of an MCI device.</span></span> <span data-ttu-id="becbe-131">Der Geräte Bezeichner muss ein standardmäßiger MCI-Gerätetyp Name sein.</span><span class="sxs-lookup"><span data-stu-id="becbe-131">The device identifier must be a standard MCI device-type name.</span></span> <span data-ttu-id="becbe-132">Der *Index* liegt zwischen 1 und der Anzahl der Geräte dieses Typs.</span><span class="sxs-lookup"><span data-stu-id="becbe-132">The *index* ranges from 1 to the number of devices of that type.</span></span> <span data-ttu-id="becbe-133">Wenn "All" für *lpszde viceid* angegeben ist, liegt der *Index* zwischen 1 und der Gesamtzahl der Geräte im System.</span><span class="sxs-lookup"><span data-stu-id="becbe-133">If "all" is specified for *lpszDeviceID*, *index* ranges from 1 to the total number of devices in the system.</span></span><br/>                                                                |
| <span id="name_index_open"></span><span id="NAME_INDEX_OPEN"></span><dl> <span data-ttu-id="becbe-134"><dt>**namens *Index* geöffnet**</dt></span><span class="sxs-lookup"><span data-stu-id="becbe-134"><dt>**name *index* open**</dt></span></span> </dl> | <span data-ttu-id="becbe-135">Gibt den Namen eines geöffneten MCI-Geräts zurück.</span><span class="sxs-lookup"><span data-stu-id="becbe-135">Returns the name of an open MCI device.</span></span> <span data-ttu-id="becbe-136">Der Geräte Bezeichner muss ein standardmäßiger MCI-Gerätetyp Name sein.</span><span class="sxs-lookup"><span data-stu-id="becbe-136">The device identifier must be a standard MCI device-type name.</span></span> <span data-ttu-id="becbe-137">Der *Index* liegt zwischen 1 und der Anzahl der geöffneten Geräte dieses Gerätetyps.</span><span class="sxs-lookup"><span data-stu-id="becbe-137">The *index* ranges from 1 to the number of open devices of that device type.</span></span> <span data-ttu-id="becbe-138">Wenn "All" für *lpszde viceid* angegeben ist, liegt der *Index* zwischen 1 und der Gesamtzahl der geöffneten Geräte im System.</span><span class="sxs-lookup"><span data-stu-id="becbe-138">If "all" is specified for *lpszDeviceID*, *index* ranges from 1 to the total number of open devices in the system.</span></span><br/>                                          |



 

</dd> <dt>

<span data-ttu-id="becbe-139">*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="becbe-139">*lpszFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="becbe-140">Kann "wait", "notify" oder beides sein.</span><span class="sxs-lookup"><span data-stu-id="becbe-140">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="becbe-141">Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="becbe-141">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="becbe-142">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="becbe-142">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="becbe-143">Beispiele</span><span class="sxs-lookup"><span data-stu-id="becbe-143">Examples</span></span>

<span data-ttu-id="becbe-144">Mit dem folgenden Befehl wird die Anzahl der geöffneten Wellenform-Audiogeräte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="becbe-144">The following command returns the number of open waveform-audio devices.</span></span>

``` syntax
sysinfo waveaudio quantity open
```

<span data-ttu-id="becbe-145">Der folgende Befehl gibt den Namen (Gerätealias) des ersten geöffneten Waveform-Audiogeräts zurück.</span><span class="sxs-lookup"><span data-stu-id="becbe-145">The following command returns the name (device alias) of the first open waveform-audio device.</span></span>

``` syntax
sysinfo waveaudio name 1 open
```

## <a name="requirements"></a><span data-ttu-id="becbe-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="becbe-146">Requirements</span></span>



| <span data-ttu-id="becbe-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="becbe-147">Requirement</span></span> | <span data-ttu-id="becbe-148">Wert</span><span class="sxs-lookup"><span data-stu-id="becbe-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="becbe-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="becbe-149">Minimum supported client</span></span><br/> | <span data-ttu-id="becbe-150">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="becbe-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="becbe-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="becbe-151">Minimum supported server</span></span><br/> | <span data-ttu-id="becbe-152">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="becbe-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="becbe-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="becbe-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="becbe-154">MCI</span><span class="sxs-lookup"><span data-stu-id="becbe-154">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="becbe-155">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="becbe-155">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="becbe-156">**Re**</span><span class="sxs-lookup"><span data-stu-id="becbe-156">**capability**</span></span>](capability.md)
</dt> </dl>

 

