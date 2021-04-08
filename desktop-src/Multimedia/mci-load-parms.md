---
title: MCI_LOAD_PARMS-Struktur (MMSYSTEM. h)
description: Die Struktur des MCI- \_ Lade- \_ Parametern enthält den Dateinamen, der für den Befehl MCI Load geladen werden soll \_ .
ms.assetid: 371d11cc-44db-496b-b51a-66d7b919b794
keywords:
- MCI_LOAD_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_LOAD_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04697a52eb9f8bb33db6063eb47e791be674f1d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742945"
---
# <a name="mci_load_parms-structure"></a><span data-ttu-id="3456b-104">Struktur von MCI- \_ Lade- \_ Parametern</span><span class="sxs-lookup"><span data-stu-id="3456b-104">MCI\_LOAD\_PARMS structure</span></span>

<span data-ttu-id="3456b-105">Die Struktur des **MCI- \_ Lade- \_ Parametern** enthält den Dateinamen, der für den Befehl [**MCI \_**](mci-load.md) Load geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="3456b-105">The **MCI\_LOAD\_PARMS** structure contains the filename to load for the [**MCI\_LOAD**](mci-load.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="3456b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3456b-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
} MCI_LOAD_PARMS;
```



## <a name="members"></a><span data-ttu-id="3456b-107">Member</span><span class="sxs-lookup"><span data-stu-id="3456b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3456b-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="3456b-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="3456b-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="3456b-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="3456b-110">**lpFileName**</span><span class="sxs-lookup"><span data-stu-id="3456b-110">**lpfilename**</span></span>
</dt> <dd>

<span data-ttu-id="3456b-111">Der Name der zu ladenden Datei.</span><span class="sxs-lookup"><span data-stu-id="3456b-111">Name of file to load.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3456b-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3456b-112">Remarks</span></span>

<span data-ttu-id="3456b-113">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3456b-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="3456b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3456b-114">Requirements</span></span>



| <span data-ttu-id="3456b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3456b-115">Requirement</span></span> | <span data-ttu-id="3456b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="3456b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3456b-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3456b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3456b-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3456b-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="3456b-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3456b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3456b-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3456b-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3456b-121">Header</span><span class="sxs-lookup"><span data-stu-id="3456b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3456b-122"><dt>MMSYSTEM. h</dt></span><span class="sxs-lookup"><span data-stu-id="3456b-122"><dt>Mmsystem.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3456b-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3456b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3456b-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="3456b-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3456b-125">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="3456b-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="3456b-126">**MCI- \_ Auslastung**</span><span class="sxs-lookup"><span data-stu-id="3456b-126">**MCI\_LOAD**</span></span>](mci-load.md)
</dt> <dt>

<span data-ttu-id="3456b-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3456b-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

