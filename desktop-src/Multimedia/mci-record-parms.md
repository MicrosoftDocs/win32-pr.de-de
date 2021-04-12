---
title: MCI_RECORD_PARMS-Struktur (mciapi. h)
description: Die Struktur der MCI- \_ Daten Satz- \_ Parser enthält Positionsinformationen für den MCI- \_ Datensatz-Befehl.
ms.assetid: 5d502cf8-3963-49d6-b515-d26e19195322
keywords:
- MCI_RECORD_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_RECORD_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b633ce192d0f4b2467cb744d614ea38056eafb60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475087"
---
# <a name="mci_record_parms-structure"></a><span data-ttu-id="3e70d-104">Struktur von MCI- \_ Daten Satz- \_ Parametern</span><span class="sxs-lookup"><span data-stu-id="3e70d-104">MCI\_RECORD\_PARMS structure</span></span>

<span data-ttu-id="3e70d-105">Die Struktur der **MCI- \_ Daten Satz- \_ Parser** enthält Positionsinformationen für den [**MCI- \_ Datensatz**](mci-record.md) -Befehl.</span><span class="sxs-lookup"><span data-stu-id="3e70d-105">The **MCI\_RECORD\_PARMS** structure contains positioning information for the [**MCI\_RECORD**](mci-record.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e70d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e70d-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_RECORD_PARMS;
```



## <a name="members"></a><span data-ttu-id="3e70d-107">Member</span><span class="sxs-lookup"><span data-stu-id="3e70d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3e70d-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="3e70d-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="3e70d-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="3e70d-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="3e70d-110">**dwfrom**</span><span class="sxs-lookup"><span data-stu-id="3e70d-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="3e70d-111">Wiedergabe Position</span><span class="sxs-lookup"><span data-stu-id="3e70d-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="3e70d-112">**dwto**</span><span class="sxs-lookup"><span data-stu-id="3e70d-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="3e70d-113">Position der Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="3e70d-113">Position to play to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e70d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e70d-114">Remarks</span></span>

<span data-ttu-id="3e70d-115">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3e70d-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e70d-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e70d-116">Requirements</span></span>



| <span data-ttu-id="3e70d-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e70d-117">Requirement</span></span> | <span data-ttu-id="3e70d-118">Wert</span><span class="sxs-lookup"><span data-stu-id="3e70d-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3e70d-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3e70d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3e70d-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e70d-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3e70d-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3e70d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3e70d-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e70d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3e70d-123">Header</span><span class="sxs-lookup"><span data-stu-id="3e70d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e70d-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e70d-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e70d-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e70d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e70d-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="3e70d-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3e70d-127">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="3e70d-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="3e70d-128">**MCI- \_ Datensatz**</span><span class="sxs-lookup"><span data-stu-id="3e70d-128">**MCI\_RECORD**</span></span>](mci-record.md)
</dt> <dt>

<span data-ttu-id="3e70d-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3e70d-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

