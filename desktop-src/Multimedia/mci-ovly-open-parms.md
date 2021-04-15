---
title: MCI_OVLY_OPEN_PARMS-Struktur (MMSYSTEM. h)
description: Die MCI- \_ Struktur mit OVLY- \_ Open-Parametern \_ enthält Informationen zum MCI- \_ Befehl "Öffnen" für Video Überlagerungs Geräte.
ms.assetid: 1559ae40-4aa5-4dfc-b337-7b056c706b67
keywords:
- MCI_OVLY_OPEN_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_OVLY_OPEN_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e64b864b4b0366421828960504aff3f5a83836b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475096"
---
# <a name="mci_ovly_open_parms-structure"></a><span data-ttu-id="b060c-104">MCI \_ OVLY- \_ Struktur zum Öffnen von \_ Parametern</span><span class="sxs-lookup"><span data-stu-id="b060c-104">MCI\_OVLY\_OPEN\_PARMS structure</span></span>

<span data-ttu-id="b060c-105">Die **MCI-Struktur mit \_ OVLY- \_ Open- \_ Parametern** enthält Informationen zum MCI-Befehl " [**\_ Öffnen**](mci-open.md) " für Video Überlagerungs Geräte.</span><span class="sxs-lookup"><span data-stu-id="b060c-105">The **MCI\_OVLY\_OPEN\_PARMS** structure contains information for the [**MCI\_OPEN**](mci-open.md) command for video-overlay devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="b060c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b060c-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
  DWORD       dwStyle;
  DWORD       hWndParent;
} MCI_OVLY_OPEN_PARMS;
```



## <a name="members"></a><span data-ttu-id="b060c-107">Member</span><span class="sxs-lookup"><span data-stu-id="b060c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b060c-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="b060c-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="b060c-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="b060c-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="b060c-110">**WDE viceid**</span><span class="sxs-lookup"><span data-stu-id="b060c-110">**wDeviceID**</span></span>
</dt> <dd>

<span data-ttu-id="b060c-111">An die Anwendung zurückgegebener Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="b060c-111">Identifier returned to application.</span></span>

</dd> <dt>

<span data-ttu-id="b060c-112">**lpstraude vicetype**</span><span class="sxs-lookup"><span data-stu-id="b060c-112">**lpstrDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="b060c-113">Der Name oder Konstantenbezeichner des Gerätetyps.</span><span class="sxs-lookup"><span data-stu-id="b060c-113">Name or constant identifier of the device type.</span></span> <span data-ttu-id="b060c-114">(Der Name des Geräts wird in der Regel aus der Registrierung oder SYSTEM.INI Datei abgerufen.) Wenn dieser Member eine Konstante ist, kann er einer der Werte sein, die in den [MCI-Gerätetypen](mci-device-types.md)aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b060c-114">(The name of the device is typically obtained from the registry or SYSTEM.INI file.) If this member is a constant, it can be one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="b060c-115">**lpstrelementname**</span><span class="sxs-lookup"><span data-stu-id="b060c-115">**lpstrElementName**</span></span>
</dt> <dd>

<span data-ttu-id="b060c-116">Der Name des Geräte Elements (in der Regel ein Pfad).</span><span class="sxs-lookup"><span data-stu-id="b060c-116">Device element name (usually a path).</span></span>

</dd> <dt>

<span data-ttu-id="b060c-117">**lpstraualias**</span><span class="sxs-lookup"><span data-stu-id="b060c-117">**lpstrAlias**</span></span>
</dt> <dd>

<span data-ttu-id="b060c-118">Optionaler Gerätealias.</span><span class="sxs-lookup"><span data-stu-id="b060c-118">Optional device alias.</span></span>

</dd> <dt>

<span data-ttu-id="b060c-119">**dwstyle**</span><span class="sxs-lookup"><span data-stu-id="b060c-119">**dwStyle**</span></span>
</dt> <dd>

<span data-ttu-id="b060c-120">Fenster Stil.</span><span class="sxs-lookup"><span data-stu-id="b060c-120">Window style.</span></span>

</dd> <dt>

<span data-ttu-id="b060c-121">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="b060c-121">**hWndParent**</span></span>
</dt> <dd>

<span data-ttu-id="b060c-122">Handle für das übergeordnete Fenster.</span><span class="sxs-lookup"><span data-stu-id="b060c-122">Handle to parent window.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b060c-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b060c-123">Remarks</span></span>

<span data-ttu-id="b060c-124">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b060c-124">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

<span data-ttu-id="b060c-125">Wenn Sie die erweiterten Datenmember nicht verwenden, können Sie die [**MCI-Struktur \_ Open- \_ Parser**](mci-open-parms.md) anstelle von **MCI \_ OVLY \_ Open- \_ Parametern** verwenden.</span><span class="sxs-lookup"><span data-stu-id="b060c-125">You can use the [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure in place of **MCI\_OVLY\_OPEN\_PARMS** if you are not using the extended data members.</span></span>

## <a name="requirements"></a><span data-ttu-id="b060c-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b060c-126">Requirements</span></span>



| <span data-ttu-id="b060c-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b060c-127">Requirement</span></span> | <span data-ttu-id="b060c-128">Wert</span><span class="sxs-lookup"><span data-stu-id="b060c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b060c-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b060c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b060c-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b060c-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b060c-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b060c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b060c-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b060c-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b060c-133">Header</span><span class="sxs-lookup"><span data-stu-id="b060c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b060c-134"><dt>MMSYSTEM. h</dt></span><span class="sxs-lookup"><span data-stu-id="b060c-134"><dt>Mmsystem.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b060c-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b060c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b060c-136">**MCI**</span><span class="sxs-lookup"><span data-stu-id="b060c-136">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b060c-137">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="b060c-137">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="b060c-138">**MCI \_ geöffnet**</span><span class="sxs-lookup"><span data-stu-id="b060c-138">**MCI\_OPEN**</span></span>](mci-open.md)
</dt> <dt>

[<span data-ttu-id="b060c-139">**geöffnete MCI- \_ \_ Parser**</span><span class="sxs-lookup"><span data-stu-id="b060c-139">**MCI\_OPEN\_PARMS**</span></span>](mci-open-parms.md)
</dt> <dt>

<span data-ttu-id="b060c-140">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b060c-140">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

