---
title: MCI_OVLY_WINDOW_PARMS-Struktur (mciapi. h)
description: Die Struktur der Fenster "MCI \_ OVLY \_ Window" \_ enthält Fenster Anzeigeinformationen für den MCI- \_ Fenster Befehl für Video Überlagerungs Geräte.
ms.assetid: 1189f31e-6e54-4279-a23d-b4e21c6cd276
keywords:
- MCI_OVLY_WINDOW_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_OVLY_WINDOW_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a554c9ed4e4869eab333b93736a0400ef93053cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949400"
---
# <a name="mci_ovly_window_parms-structure"></a><span data-ttu-id="39caf-104">Struktur des MCI- \_ OVLY- \_ Fenster \_ Parametern</span><span class="sxs-lookup"><span data-stu-id="39caf-104">MCI\_OVLY\_WINDOW\_PARMS structure</span></span>

<span data-ttu-id="39caf-105">Die Struktur der Fenster " **MCI \_ OVLY \_ Window \_** " enthält Fenster Anzeigeinformationen für den [**MCI- \_ Fenster**](mci-window.md) Befehl für Video Überlagerungs Geräte.</span><span class="sxs-lookup"><span data-stu-id="39caf-105">The **MCI\_OVLY\_WINDOW\_PARMS** structure contains window-display information for the [**MCI\_WINDOW**](mci-window.md) command for video-overlay devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="39caf-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="39caf-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  HWND      hWnd;
  UINT      nCmdShow;
  LPCTSTR   lpstrText;
} MCI_OVLY_WINDOW_PARMS;
```



## <a name="members"></a><span data-ttu-id="39caf-107">Member</span><span class="sxs-lookup"><span data-stu-id="39caf-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="39caf-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="39caf-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="39caf-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="39caf-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="39caf-110">**hWnd**</span><span class="sxs-lookup"><span data-stu-id="39caf-110">**hWnd**</span></span>
</dt> <dd>

<span data-ttu-id="39caf-111">Handle für Anzeige Fenster.</span><span class="sxs-lookup"><span data-stu-id="39caf-111">Handle to display window.</span></span>

</dd> <dt>

<span data-ttu-id="39caf-112">**nCmdShow**</span><span class="sxs-lookup"><span data-stu-id="39caf-112">**nCmdShow**</span></span>
</dt> <dd>

<span data-ttu-id="39caf-113">Fenster Anzeige Befehl.</span><span class="sxs-lookup"><span data-stu-id="39caf-113">Window-display command.</span></span>

</dd> <dt>

<span data-ttu-id="39caf-114">**lpstrautext**</span><span class="sxs-lookup"><span data-stu-id="39caf-114">**lpstrText**</span></span>
</dt> <dd>

<span data-ttu-id="39caf-115">Fenster Beschriftung.</span><span class="sxs-lookup"><span data-stu-id="39caf-115">Window caption.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39caf-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39caf-116">Remarks</span></span>

<span data-ttu-id="39caf-117">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="39caf-117">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="39caf-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39caf-118">Requirements</span></span>



| <span data-ttu-id="39caf-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39caf-119">Requirement</span></span> | <span data-ttu-id="39caf-120">Wert</span><span class="sxs-lookup"><span data-stu-id="39caf-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="39caf-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39caf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="39caf-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39caf-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="39caf-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39caf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="39caf-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39caf-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="39caf-125">Header</span><span class="sxs-lookup"><span data-stu-id="39caf-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="39caf-126"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="39caf-126"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39caf-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39caf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39caf-128">**MCI**</span><span class="sxs-lookup"><span data-stu-id="39caf-128">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="39caf-129">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="39caf-129">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="39caf-130">**MCI- \_ Fenster**</span><span class="sxs-lookup"><span data-stu-id="39caf-130">**MCI\_WINDOW**</span></span>](mci-window.md)
</dt> <dt>

<span data-ttu-id="39caf-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="39caf-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

