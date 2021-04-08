---
title: MCI_SEQ_SET_PARMS-Struktur (mciapi. h)
description: Die Struktur des MCI \_ Seq- \_ Set-Parametern \_ enthält Informationen zum MCI- \_ Befehl Set für die Komponenten von MIDI Sequencer.
ms.assetid: 71638a92-c1d6-474b-bc97-ea63ca586aaa
keywords:
- MCI_SEQ_SET_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SEQ_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 879dd575918a33676e3ba73bd2a8f6212e3dc412
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949534"
---
# <a name="mci_seq_set_parms-structure"></a><span data-ttu-id="16ce5-104">Struktur von MCI \_ Seq- \_ Set- \_ Parametern</span><span class="sxs-lookup"><span data-stu-id="16ce5-104">MCI\_SEQ\_SET\_PARMS structure</span></span>

<span data-ttu-id="16ce5-105">Die Struktur des **MCI \_ Seq- \_ Set- \_ Parametern** enthält Informationen zum [**MCI-Befehl \_ Set**](mci-set.md) für die Komponenten von MIDI Sequencer.</span><span class="sxs-lookup"><span data-stu-id="16ce5-105">The **MCI\_SEQ\_SET\_PARMS** structure contains information for the [**MCI\_SET**](mci-set.md) command for MIDI sequencer devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="16ce5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="16ce5-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  DWORD     dwTempo;
  DWORD     dwPort;
  DWORD     dwSlave;
  DWORD     dwMaster;
  DWORD     dwOffset;
} MCI_SEQ_SET_PARMS;
```



## <a name="members"></a><span data-ttu-id="16ce5-107">Member</span><span class="sxs-lookup"><span data-stu-id="16ce5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="16ce5-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="16ce5-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="16ce5-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="16ce5-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="16ce5-110">**dwtimeformat**</span><span class="sxs-lookup"><span data-stu-id="16ce5-110">**dwTimeFormat**</span></span>
</dt> <dd>

<span data-ttu-id="16ce5-111">Das Zeitformat von Sequencer.</span><span class="sxs-lookup"><span data-stu-id="16ce5-111">Sequencer's time format.</span></span>

</dd> <dt>

<span data-ttu-id="16ce5-112">**dwaudiodatei**</span><span class="sxs-lookup"><span data-stu-id="16ce5-112">**dwAudio**</span></span>
</dt> <dd>

<span data-ttu-id="16ce5-113">Audioausgabechannel.</span><span class="sxs-lookup"><span data-stu-id="16ce5-113">Audio output channel.</span></span>

</dd> <dt>

<span data-ttu-id="16ce5-114">**dwtempo**</span><span class="sxs-lookup"><span data-stu-id="16ce5-114">**dwTempo**</span></span>
</dt> <dd>

<span data-ttu-id="16ce5-115">Lern.</span><span class="sxs-lookup"><span data-stu-id="16ce5-115">Tempo.</span></span>

</dd> <dt>

<span data-ttu-id="16ce5-116">**dwport**</span><span class="sxs-lookup"><span data-stu-id="16ce5-116">**dwPort**</span></span>
</dt> <dd>

<span data-ttu-id="16ce5-117">Port.</span><span class="sxs-lookup"><span data-stu-id="16ce5-117">Port.</span></span>

</dd> <dt>

<span data-ttu-id="16ce5-118">**dwslave**</span><span class="sxs-lookup"><span data-stu-id="16ce5-118">**dwSlave**</span></span>
</dt> <dd>

<span data-ttu-id="16ce5-119">Der Synchronisierungstyp, der vom Sequencer für den untergeordneten Vorgang verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="16ce5-119">Type of synchronization used by the sequencer for subordinate operation.</span></span>

</dd> <dt>

<span data-ttu-id="16ce5-120">**dwmaster**</span><span class="sxs-lookup"><span data-stu-id="16ce5-120">**dwMaster**</span></span>
</dt> <dd>

<span data-ttu-id="16ce5-121">Der Synchronisierungstyp, der vom Sequencer für den Master Vorgang verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="16ce5-121">Type of synchronization used by the sequencer for master operation.</span></span>

</dd> <dt>

<span data-ttu-id="16ce5-122">**dwOffset**</span><span class="sxs-lookup"><span data-stu-id="16ce5-122">**dwOffset**</span></span>
</dt> <dd>

<span data-ttu-id="16ce5-123">Daten Offset.</span><span class="sxs-lookup"><span data-stu-id="16ce5-123">Data offset.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="16ce5-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16ce5-124">Remarks</span></span>

<span data-ttu-id="16ce5-125">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="16ce5-125">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="16ce5-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16ce5-126">Requirements</span></span>



| <span data-ttu-id="16ce5-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16ce5-127">Requirement</span></span> | <span data-ttu-id="16ce5-128">Wert</span><span class="sxs-lookup"><span data-stu-id="16ce5-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="16ce5-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="16ce5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="16ce5-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16ce5-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="16ce5-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="16ce5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="16ce5-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16ce5-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="16ce5-133">Header</span><span class="sxs-lookup"><span data-stu-id="16ce5-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="16ce5-134"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="16ce5-134"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16ce5-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16ce5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16ce5-136">**MCI**</span><span class="sxs-lookup"><span data-stu-id="16ce5-136">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="16ce5-137">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="16ce5-137">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="16ce5-138">**MCI- \_ Gruppe**</span><span class="sxs-lookup"><span data-stu-id="16ce5-138">**MCI\_SET**</span></span>](mci-set.md)
</dt> <dt>

<span data-ttu-id="16ce5-139">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="16ce5-139">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

