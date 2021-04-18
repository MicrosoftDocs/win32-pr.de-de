---
title: MCI_SYSINFO_PARMS-Struktur (mciapi. h)
description: Die MCI- \_ sysinfo- \_ Struktur enthält Informationen für den MCI- \_ Befehl "sysinfo".
ms.assetid: 433649ed-7c00-440d-84f3-164949e01cc4
keywords:
- MCI_SYSINFO_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SYSINFO_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf143bb0d895dc03df38bbb0a657467d506eac77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337705"
---
# <a name="mci_sysinfo_parms-structure"></a><span data-ttu-id="39713-104">Struktur von MCI- \_ sysinfo- \_ Parametern</span><span class="sxs-lookup"><span data-stu-id="39713-104">MCI\_SYSINFO\_PARMS structure</span></span>

<span data-ttu-id="39713-105">Die **MCI- \_ sysinfo \_** -Struktur enthält Informationen für den [**MCI-Befehl " \_ sysinfo**](mci-sysinfo.md) ".</span><span class="sxs-lookup"><span data-stu-id="39713-105">The **MCI\_SYSINFO\_PARMS** structure contains information for the [**MCI\_SYSINFO**](mci-sysinfo.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="39713-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="39713-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPTSTR    lpstrReturn;
  DWORD     dwRetSize;
  DWORD     dwNumber;
  UINT      wDeviceType;
} MCI_SYSINFO_PARMS;
```



## <a name="members"></a><span data-ttu-id="39713-107">Member</span><span class="sxs-lookup"><span data-stu-id="39713-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="39713-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="39713-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="39713-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="39713-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="39713-110">**lpstraureturn**</span><span class="sxs-lookup"><span data-stu-id="39713-110">**lpstrReturn**</span></span>
</dt> <dd>

<span data-ttu-id="39713-111">Zeiger auf einen vom Benutzer bereitgestellten Puffer für die Rückgabe Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="39713-111">Pointer to a user-supplied buffer for the return string.</span></span> <span data-ttu-id="39713-112">Sie wird auch verwendet, um einen **DWORD** -Wert zurückzugeben, wenn das MCI-Flag für die \_ sysinfo- \_ Menge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="39713-112">It is also used to return a **DWORD** value when the MCI\_SYSINFO\_QUANTITY flag is used.</span></span>

</dd> <dt>

<span data-ttu-id="39713-113">**dwretsize**</span><span class="sxs-lookup"><span data-stu-id="39713-113">**dwRetSize**</span></span>
</dt> <dd>

<span data-ttu-id="39713-114">Größe (in Bytes) des Rückgabe Puffers.</span><span class="sxs-lookup"><span data-stu-id="39713-114">Size, in bytes, of return buffer.</span></span>

</dd> <dt>

<span data-ttu-id="39713-115">**dwnumber**</span><span class="sxs-lookup"><span data-stu-id="39713-115">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="39713-116">Zahl, die die Geräte Position in der MCI-Gerätetabelle oder in der Liste der geöffneten Geräte angibt, wenn das MCI- \_ sysinfo- \_ Flag zum Öffnen festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="39713-116">Number indicating the device position in the MCI device table or in the list of open devices if the MCI\_SYSINFO\_OPEN flag is set.</span></span>

</dd> <dt>

<span data-ttu-id="39713-117">**WDE vicetype**</span><span class="sxs-lookup"><span data-stu-id="39713-117">**wDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="39713-118">Typ des Geräts.</span><span class="sxs-lookup"><span data-stu-id="39713-118">Type of device.</span></span> <span data-ttu-id="39713-119">Dieser Member kann einer der Werte sein, die in den [MCI-Gerätetypen](mci-device-types.md)aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="39713-119">This member can be one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39713-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39713-120">Remarks</span></span>

<span data-ttu-id="39713-121">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="39713-121">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="39713-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39713-122">Requirements</span></span>



| <span data-ttu-id="39713-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39713-123">Requirement</span></span> | <span data-ttu-id="39713-124">Wert</span><span class="sxs-lookup"><span data-stu-id="39713-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="39713-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39713-125">Minimum supported client</span></span><br/> | <span data-ttu-id="39713-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39713-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="39713-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39713-127">Minimum supported server</span></span><br/> | <span data-ttu-id="39713-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39713-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="39713-129">Header</span><span class="sxs-lookup"><span data-stu-id="39713-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="39713-130"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="39713-130"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39713-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39713-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39713-132">**MCI**</span><span class="sxs-lookup"><span data-stu-id="39713-132">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="39713-133">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="39713-133">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="39713-134">**MCI- \_ sysinfo**</span><span class="sxs-lookup"><span data-stu-id="39713-134">**MCI\_SYSINFO**</span></span>](mci-sysinfo.md)
</dt> <dt>

<span data-ttu-id="39713-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="39713-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

