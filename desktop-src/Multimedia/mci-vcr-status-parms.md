---
title: MCI_VCR_STATUS_PARMS Struktur (VCR. h)
description: Die Struktur der MCI- \_ VCR- \_ Status \_ Parameter enthält Parameter für den MCI- \_ Status Befehl für Video-Kassetten-Recorder.
ms.assetid: 5d7cbb64-a81d-4bdd-8f07-8c20dd7b9ef5
keywords:
- MCI_VCR_STATUS_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_STATUS_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0b197acfa0e170a9ab199cd6d6c51a64e14c320
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949485"
---
# <a name="mci_vcr_status_parms-structure"></a><span data-ttu-id="245b1-104">Struktur des MCI \_ VCR- \_ Status \_ Parametern</span><span class="sxs-lookup"><span data-stu-id="245b1-104">MCI\_VCR\_STATUS\_PARMS structure</span></span>

<span data-ttu-id="245b1-105">Die Struktur der **MCI- \_ VCR- \_ Status \_** Parameter enthält Parameter für den [**MCI- \_ Status**](mci-status.md) Befehl für Video-Kassetten-Recorder.</span><span class="sxs-lookup"><span data-stu-id="245b1-105">The **MCI\_VCR\_STATUS\_PARMS** structure contains parameters for the [**MCI\_STATUS**](mci-status.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="245b1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="245b1-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_STATUS_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwItem;
  DWORD     dwTrack;
  DWORD     dwNumber;
} MCI_VCR_STATUS_PARMS;
```



## <a name="members"></a><span data-ttu-id="245b1-107">Member</span><span class="sxs-lookup"><span data-stu-id="245b1-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="245b1-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="245b1-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="245b1-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="245b1-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="245b1-110">**dwreturn**</span><span class="sxs-lookup"><span data-stu-id="245b1-110">**dwReturn**</span></span>
</dt> <dd>

<span data-ttu-id="245b1-111">Wert, der vom [**MCI- \_ Status**](mci-status.md) Befehl zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="245b1-111">Value returned by the [**MCI\_STATUS**](mci-status.md) command.</span></span> <span data-ttu-id="245b1-112">Der Rückgabewert variiert je nach Abfrage des Befehls.</span><span class="sxs-lookup"><span data-stu-id="245b1-112">The return value varies according to the inquiry of the command.</span></span> <span data-ttu-id="245b1-113">Weitere Informationen finden Sie in der Beschreibung des Befehls " [**MCI- \_ Status**](mci-status-parms.md) ".</span><span class="sxs-lookup"><span data-stu-id="245b1-113">For more information, see the description of the [**MCI\_STATUS**](mci-status-parms.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="245b1-114">**dwitem**</span><span class="sxs-lookup"><span data-stu-id="245b1-114">**dwItem**</span></span>
</dt> <dd>

<span data-ttu-id="245b1-115">Der Typ der angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="245b1-115">Type of information requested.</span></span>

</dd> <dt>

<span data-ttu-id="245b1-116">**dwtrack**</span><span class="sxs-lookup"><span data-stu-id="245b1-116">**dwTrack**</span></span>
</dt> <dd>

<span data-ttu-id="245b1-117">Audiobild oder Videotitel, das Informationen während der nächsten Aufzeichnung speichert.</span><span class="sxs-lookup"><span data-stu-id="245b1-117">Audio or video track that will store information during the next recording.</span></span> <span data-ttu-id="245b1-118">Dieser Member wird verwendet, um Informationen zurückzugeben, wenn der [**MCI- \_ Status**](mci-status-parms.md) Befehl den Video-oder audioaufzeichnungs Status fragt.</span><span class="sxs-lookup"><span data-stu-id="245b1-118">This member is used to return information when the [**MCI\_STATUS**](mci-status-parms.md) command inquires about the video or audio recording status.</span></span>

</dd> <dt>

<span data-ttu-id="245b1-119">**dwnumber**</span><span class="sxs-lookup"><span data-stu-id="245b1-119">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="245b1-120">Logischer Tuner, dem der aktuelle Channel zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="245b1-120">Logical tuner that the current channel is associated with.</span></span> <span data-ttu-id="245b1-121">Dieser Member wird verwendet, um Informationen zurückzugeben, wenn der [**MCI- \_ Status**](mci-status.md) Befehl die aktuelle Channelnummer fragt.</span><span class="sxs-lookup"><span data-stu-id="245b1-121">This member is used to return information when the [**MCI\_STATUS**](mci-status.md) command inquires about the current channel number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="245b1-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="245b1-122">Remarks</span></span>

<span data-ttu-id="245b1-123">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="245b1-123">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="245b1-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="245b1-124">Requirements</span></span>



| <span data-ttu-id="245b1-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="245b1-125">Requirement</span></span> | <span data-ttu-id="245b1-126">Wert</span><span class="sxs-lookup"><span data-stu-id="245b1-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="245b1-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="245b1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="245b1-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="245b1-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="245b1-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="245b1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="245b1-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="245b1-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="245b1-131">Header</span><span class="sxs-lookup"><span data-stu-id="245b1-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="245b1-132"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="245b1-132"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="245b1-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="245b1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="245b1-134">**MCI**</span><span class="sxs-lookup"><span data-stu-id="245b1-134">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="245b1-135">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="245b1-135">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="245b1-136">**MCI- \_ Status**</span><span class="sxs-lookup"><span data-stu-id="245b1-136">**MCI\_STATUS**</span></span>](mci-status.md)
</dt> <dt>

<span data-ttu-id="245b1-137">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="245b1-137">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

