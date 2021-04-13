---
title: MCI_WAVE_DELETE_PARMS-Struktur (mciapi. h)
description: Die Struktur des MCI \_ \_ -Wave DELETE \_ -Parametern enthält Positionsinformationen für den MCI \_ Delete-Befehl für Waveform-Audiogeräte.
ms.assetid: 5c0bf0ca-773b-4b96-8b55-9ef7b5a306d9
keywords:
- MCI_WAVE_DELETE_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_WAVE_DELETE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 286c6443a229da266dae4992687c0e9ead5640bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475684"
---
# <a name="mci_wave_delete_parms-structure"></a><span data-ttu-id="46081-104">MCI \_ Wave \_ Delete- \_ paramemstruktur</span><span class="sxs-lookup"><span data-stu-id="46081-104">MCI\_WAVE\_DELETE\_PARMS structure</span></span>

<span data-ttu-id="46081-105">Die Struktur des **MCI- \_ Wave \_ Delete- \_ Parametern** enthält Positionsinformationen für den [**MCI \_ Delete**](mci-delete.md) -Befehl für Waveform-Audiogeräte.</span><span class="sxs-lookup"><span data-stu-id="46081-105">The **MCI\_WAVE\_DELETE\_PARMS** structure contains position information for the [**MCI\_DELETE**](mci-delete.md) command for waveform-audio devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="46081-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="46081-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_WAVE_DELETE_PARMS;
```



## <a name="members"></a><span data-ttu-id="46081-107">Member</span><span class="sxs-lookup"><span data-stu-id="46081-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="46081-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="46081-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="46081-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="46081-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="46081-110">**dwfrom**</span><span class="sxs-lookup"><span data-stu-id="46081-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="46081-111">Die zu löschende Position.</span><span class="sxs-lookup"><span data-stu-id="46081-111">Position to delete from.</span></span>

</dd> <dt>

<span data-ttu-id="46081-112">**dwto**</span><span class="sxs-lookup"><span data-stu-id="46081-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="46081-113">Position, an der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="46081-113">Position to delete to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46081-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46081-114">Remarks</span></span>

<span data-ttu-id="46081-115">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="46081-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="46081-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46081-116">Requirements</span></span>



| <span data-ttu-id="46081-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46081-117">Requirement</span></span> | <span data-ttu-id="46081-118">Wert</span><span class="sxs-lookup"><span data-stu-id="46081-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="46081-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="46081-119">Minimum supported client</span></span><br/> | <span data-ttu-id="46081-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46081-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="46081-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="46081-121">Minimum supported server</span></span><br/> | <span data-ttu-id="46081-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46081-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="46081-123">Header</span><span class="sxs-lookup"><span data-stu-id="46081-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="46081-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="46081-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46081-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46081-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46081-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="46081-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="46081-127">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="46081-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="46081-128">**MCI \_ Löschen**</span><span class="sxs-lookup"><span data-stu-id="46081-128">**MCI\_DELETE**</span></span>](mci-delete.md)
</dt> <dt>

<span data-ttu-id="46081-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="46081-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

