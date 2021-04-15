---
title: MCI_BREAK_PARMS-Struktur (mciapi. h)
description: Die Struktur der MCI \_ \_ -break-Parser enthält Code-und Fenster Informationen des virtuellen Schlüssels für den MCI- \_ break-Befehl.
ms.assetid: c8df8c55-cc6b-4dd7-b275-784d3eb9dce1
keywords:
- MCI_BREAK_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_BREAK_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e66b52992827b447b6d4b5585ca3f98564142680
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517630"
---
# <a name="mci_break_parms-structure"></a><span data-ttu-id="0f44d-104">Struktur der MCI- \_ break- \_ Parametern</span><span class="sxs-lookup"><span data-stu-id="0f44d-104">MCI\_BREAK\_PARMS structure</span></span>

<span data-ttu-id="0f44d-105">Die Struktur der **MCI- \_ break- \_ Parser** enthält Code-und Fenster Informationen des virtuellen Schlüssels für den [**MCI- \_ break**](mci-break.md) -Befehl.</span><span class="sxs-lookup"><span data-stu-id="0f44d-105">The **MCI\_BREAK\_PARMS** structure contains virtual-key code and window information for the [**MCI\_BREAK**](mci-break.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f44d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f44d-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  int       nVirtKey;
  HWND      hwndBreak;
} MCI_BREAK_PARMS;
```



## <a name="members"></a><span data-ttu-id="0f44d-107">Member</span><span class="sxs-lookup"><span data-stu-id="0f44d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0f44d-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="0f44d-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="0f44d-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="0f44d-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="0f44d-110">**nvirtkey**</span><span class="sxs-lookup"><span data-stu-id="0f44d-110">**nVirtKey**</span></span>
</dt> <dd>

<span data-ttu-id="0f44d-111">Code des virtuellen Schlüssels für die Pause-Taste.</span><span class="sxs-lookup"><span data-stu-id="0f44d-111">Virtual-key code for break key.</span></span>

</dd> <dt>

<span data-ttu-id="0f44d-112">**hwndbreak**</span><span class="sxs-lookup"><span data-stu-id="0f44d-112">**hwndBreak**</span></span>
</dt> <dd>

<span data-ttu-id="0f44d-113">Handle für das Fenster, das das aktuelle Fenster für die unterschieterkennung sein muss.</span><span class="sxs-lookup"><span data-stu-id="0f44d-113">Handle to the window that must be the current window for break detection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f44d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f44d-114">Remarks</span></span>

<span data-ttu-id="0f44d-115">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="0f44d-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span> <span data-ttu-id="0f44d-116">Die folgenden Flags sind definiert:</span><span class="sxs-lookup"><span data-stu-id="0f44d-116">The following flags are defined:</span></span>

<span data-ttu-id="0f44d-117">MCI- \_ break- \_ HWND</span><span class="sxs-lookup"><span data-stu-id="0f44d-117">MCI\_BREAK\_HWND</span></span>

<span data-ttu-id="0f44d-118">Überprüft das **hwndbreak** -Element und gibt das Fenster an, das den Fokus haben muss, um die Unterbrechung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="0f44d-118">Validates the **hwndBreak** member specifying the window that must have focus to enable break detection.</span></span>

<span data-ttu-id="0f44d-119">MCI- \_ break- \_ Taste</span><span class="sxs-lookup"><span data-stu-id="0f44d-119">MCI\_BREAK\_KEY</span></span>

<span data-ttu-id="0f44d-120">Überprüft den **nvirtkey** -Member, der den Code für den virtuellen Schlüssel angibt, der für die Break Key-Taste verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0f44d-120">Validates the **nVirtKey** member specifying the virtual-key code to be used for the break key.</span></span>

<span data-ttu-id="0f44d-121">MCI-unter \_ Brechung \_</span><span class="sxs-lookup"><span data-stu-id="0f44d-121">MCI\_BREAK\_OFF</span></span>

<span data-ttu-id="0f44d-122">Deaktiviert alle vorhandenen Break-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="0f44d-122">Disables any existing break key.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f44d-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f44d-123">Requirements</span></span>



| <span data-ttu-id="0f44d-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f44d-124">Requirement</span></span> | <span data-ttu-id="0f44d-125">Wert</span><span class="sxs-lookup"><span data-stu-id="0f44d-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0f44d-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0f44d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0f44d-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f44d-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0f44d-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0f44d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0f44d-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f44d-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0f44d-130">Header</span><span class="sxs-lookup"><span data-stu-id="0f44d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f44d-131"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f44d-131"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f44d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f44d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f44d-133">**MCI**</span><span class="sxs-lookup"><span data-stu-id="0f44d-133">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="0f44d-134">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="0f44d-134">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="0f44d-135">**MCI-unter \_ Brechung**</span><span class="sxs-lookup"><span data-stu-id="0f44d-135">**MCI\_BREAK**</span></span>](mci-break.md)
</dt> <dt>

<span data-ttu-id="0f44d-136">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0f44d-136">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

