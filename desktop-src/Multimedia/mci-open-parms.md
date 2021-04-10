---
title: MCI_OPEN_PARMS-Struktur (mciapi. h)
description: Die geöffnete MCI- \_ \_ Struktur enthält Informationen für den MCI- \_ Befehl "Öffnen".
ms.assetid: d22cefeb-3d49-47cf-a946-f73c77ae43fd
keywords:
- MCI_OPEN_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_OPEN_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 658f97a9b2677347c9818265c1f05c2115c95fdd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103442"
---
# <a name="mci_open_parms-structure"></a><span data-ttu-id="d0f8c-104">MCI \_ - \_ Struktur mit offenen Parametern</span><span class="sxs-lookup"><span data-stu-id="d0f8c-104">MCI\_OPEN\_PARMS structure</span></span>

<span data-ttu-id="d0f8c-105">Die **\_ geöffnete \_ MCI** -Struktur enthält Informationen für den MCI-Befehl " [**\_ Öffnen**](mci-open.md) ".</span><span class="sxs-lookup"><span data-stu-id="d0f8c-105">The **MCI\_OPEN\_PARMS** structure contains information for the [**MCI\_OPEN**](mci-open.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0f8c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0f8c-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
} MCI_OPEN_PARMS;
```



## <a name="members"></a><span data-ttu-id="d0f8c-107">Member</span><span class="sxs-lookup"><span data-stu-id="d0f8c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d0f8c-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="d0f8c-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="d0f8c-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="d0f8c-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="d0f8c-110">**WDE viceid**</span><span class="sxs-lookup"><span data-stu-id="d0f8c-110">**wDeviceID**</span></span>
</dt> <dd>

<span data-ttu-id="d0f8c-111">An die Anwendung zurückgegebener Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="d0f8c-111">Identifier returned to application.</span></span>

</dd> <dt>

<span data-ttu-id="d0f8c-112">**lpstraude vicetype**</span><span class="sxs-lookup"><span data-stu-id="d0f8c-112">**lpstrDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="d0f8c-113">Der Name oder Konstantenbezeichner des Gerätetyps.</span><span class="sxs-lookup"><span data-stu-id="d0f8c-113">Name or constant identifier of the device type.</span></span> <span data-ttu-id="d0f8c-114">(Der Name des Geräts wird in der Regel aus der Registrierung oder SYSTEM.INI Datei abgerufen.) Wenn dieser Member eine Konstante ist, kann er einer der Werte sein, die in den [MCI-Gerätetypen](mci-device-types.md)aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="d0f8c-114">(The name of the device is typically obtained from the registry or SYSTEM.INI file.) If this member is a constant, it can be one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0f8c-115">**lpstrelementname**</span><span class="sxs-lookup"><span data-stu-id="d0f8c-115">**lpstrElementName**</span></span>
</dt> <dd>

<span data-ttu-id="d0f8c-116">Device-Element (häufig ein Pfad).</span><span class="sxs-lookup"><span data-stu-id="d0f8c-116">Device element (often a path).</span></span>

</dd> <dt>

<span data-ttu-id="d0f8c-117">**lpstraualias**</span><span class="sxs-lookup"><span data-stu-id="d0f8c-117">**lpstrAlias**</span></span>
</dt> <dd>

<span data-ttu-id="d0f8c-118">Optionaler Gerätealias.</span><span class="sxs-lookup"><span data-stu-id="d0f8c-118">Optional device alias.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0f8c-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0f8c-119">Remarks</span></span>

<span data-ttu-id="d0f8c-120">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d0f8c-120">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0f8c-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0f8c-121">Requirements</span></span>



| <span data-ttu-id="d0f8c-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d0f8c-122">Requirement</span></span> | <span data-ttu-id="d0f8c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="d0f8c-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d0f8c-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d0f8c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d0f8c-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d0f8c-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d0f8c-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d0f8c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d0f8c-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d0f8c-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d0f8c-128">Header</span><span class="sxs-lookup"><span data-stu-id="d0f8c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0f8c-129"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0f8c-129"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0f8c-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0f8c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0f8c-131">**MCI**</span><span class="sxs-lookup"><span data-stu-id="d0f8c-131">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d0f8c-132">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="d0f8c-132">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="d0f8c-133">**MCI \_ geöffnet**</span><span class="sxs-lookup"><span data-stu-id="d0f8c-133">**MCI\_OPEN**</span></span>](mci-open.md)
</dt> <dt>

<span data-ttu-id="d0f8c-134">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d0f8c-134">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

