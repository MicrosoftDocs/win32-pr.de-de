---
title: MCI_WAVE_OPEN_PARMS-Struktur (mciapi. h)
description: Die \_ Struktur von MCI Wave \_ Open \_ -Parametern enthält Informationen für den MCI \_ -Befehl Open für Waveform-Audiogeräte.
ms.assetid: 2fc9383e-4610-4751-acad-b545dc6d8992
keywords:
- MCI_WAVE_OPEN_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_WAVE_OPEN_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5a4107c6283edab1ffeaf18297e2898a8b17761
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344690"
---
# <a name="mci_wave_open_parms-structure"></a><span data-ttu-id="3b226-104">MCI \_ Wave \_ Open- \_ paramemstruktur</span><span class="sxs-lookup"><span data-stu-id="3b226-104">MCI\_WAVE\_OPEN\_PARMS structure</span></span>

<span data-ttu-id="3b226-105">Die Struktur von **MCI \_ Wave \_ Open- \_ Parametern** enthält Informationen für den [**MCI-Befehl \_ Open**](mci-open.md) für Waveform-Audiogeräte.</span><span class="sxs-lookup"><span data-stu-id="3b226-105">The **MCI\_WAVE\_OPEN\_PARMS** structure contains information for [**MCI\_OPEN**](mci-open.md) command for waveform-audio devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b226-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b226-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
  DWORD       dwBufferSeconds;
} MCI_WAVE_OPEN_PARMS;
```



## <a name="members"></a><span data-ttu-id="3b226-107">Member</span><span class="sxs-lookup"><span data-stu-id="3b226-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3b226-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="3b226-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="3b226-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="3b226-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="3b226-110">**WDE viceid**</span><span class="sxs-lookup"><span data-stu-id="3b226-110">**wDeviceID**</span></span>
</dt> <dd>

<span data-ttu-id="3b226-111">Der INDENTIFIER wurde an die Anwendung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3b226-111">Indentifier returned to application.</span></span>

</dd> <dt>

<span data-ttu-id="3b226-112">**lpstraude vicetype**</span><span class="sxs-lookup"><span data-stu-id="3b226-112">**lpstrDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="3b226-113">Der Name oder Konstantenbezeichner des Gerätetyps.</span><span class="sxs-lookup"><span data-stu-id="3b226-113">Name or constant identifier of the device type.</span></span> <span data-ttu-id="3b226-114">(Der Name des Geräts wird in der Regel aus der Registrierung oder SYSTEM.INI Datei abgerufen.) Dieser Member kann einer der Werte sein, die in den [MCI-Gerätetypen](mci-device-types.md)aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="3b226-114">(The name of the device is typically obtained from the registry or SYSTEM.INI file.) This member can be one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b226-115">**lpstrelementname**</span><span class="sxs-lookup"><span data-stu-id="3b226-115">**lpstrElementName**</span></span>
</dt> <dd>

<span data-ttu-id="3b226-116">Der Name des Geräte Elements (in der Regel ein Pfad).</span><span class="sxs-lookup"><span data-stu-id="3b226-116">Device element name (usually a path).</span></span>

</dd> <dt>

<span data-ttu-id="3b226-117">**lpstraualias**</span><span class="sxs-lookup"><span data-stu-id="3b226-117">**lpstrAlias**</span></span>
</dt> <dd>

<span data-ttu-id="3b226-118">Optionaler Gerätealias.</span><span class="sxs-lookup"><span data-stu-id="3b226-118">Optional device alias.</span></span>

</dd> <dt>

<span data-ttu-id="3b226-119">**dwbufferseconds**</span><span class="sxs-lookup"><span data-stu-id="3b226-119">**dwBufferSeconds**</span></span>
</dt> <dd>

<span data-ttu-id="3b226-120">Pufferlänge in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="3b226-120">Buffer length, in seconds.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b226-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b226-121">Remarks</span></span>

<span data-ttu-id="3b226-122">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3b226-122">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

<span data-ttu-id="3b226-123">Wenn Sie die erweiterten Datenmember nicht verwenden, können Sie die [**MCI-Struktur \_ Open- \_ Parser**](mci-open-parms.md) anstelle von **MCI \_ Wave Open- \_ \_ para** Metern verwenden.</span><span class="sxs-lookup"><span data-stu-id="3b226-123">You can use the [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure instead of **MCI\_WAVE\_OPEN\_PARMS** if you are not using the extended data members.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b226-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3b226-124">Requirements</span></span>



| <span data-ttu-id="3b226-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3b226-125">Requirement</span></span> | <span data-ttu-id="3b226-126">Wert</span><span class="sxs-lookup"><span data-stu-id="3b226-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3b226-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3b226-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3b226-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3b226-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3b226-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3b226-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3b226-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3b226-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3b226-131">Header</span><span class="sxs-lookup"><span data-stu-id="3b226-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b226-132"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b226-132"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b226-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b226-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b226-134">**MCI**</span><span class="sxs-lookup"><span data-stu-id="3b226-134">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3b226-135">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="3b226-135">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="3b226-136">**MCI \_ geöffnet**</span><span class="sxs-lookup"><span data-stu-id="3b226-136">**MCI\_OPEN**</span></span>](mci-open.md)
</dt> <dt>

<span data-ttu-id="3b226-137">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3b226-137">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3b226-138">**geöffnete MCI- \_ \_ Parser**</span><span class="sxs-lookup"><span data-stu-id="3b226-138">**MCI\_OPEN\_PARMS**</span></span>](mci-open-parms.md)
</dt> </dl>

 

