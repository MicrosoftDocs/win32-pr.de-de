---
title: MCI_VCR_SETTUNER_PARMS Struktur (VCR. h)
description: Die Struktur des MCI \_ VCR \_ settuner- \_ Parameters enthält Parameter für den MCI \_ settuner-Befehl für Video-Kassetten-Recorder.
ms.assetid: 8254b4c0-80bb-44e4-9f51-1d7434d3b08f
keywords:
- MCI_VCR_SETTUNER_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_SETTUNER_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 891ddf3b4b3dcb9532a2431901b0b2b9d84b0e52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741801"
---
# <a name="mci_vcr_settuner_parms-structure"></a><span data-ttu-id="d0598-104">Struktur von MCI \_ VCR \_ settuner- \_ Parametern</span><span class="sxs-lookup"><span data-stu-id="d0598-104">MCI\_VCR\_SETTUNER\_PARMS structure</span></span>

<span data-ttu-id="d0598-105">Die Struktur des **MCI \_ VCR \_ settuner- \_ para** meters enthält Parameter für den [**MCI \_ settuner**](mci-settuner.md) -Befehl für Video-Kassetten-Recorder.</span><span class="sxs-lookup"><span data-stu-id="d0598-105">The **MCI\_VCR\_SETTUNER\_PARMS** structure contains parameters for the [**MCI\_SETTUNER**](mci-settuner.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0598-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0598-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SETTUNER_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwChannel;
  DWORD     dwNumber;
} MCI_VCR_SETTUNER_PARMS;
```



## <a name="members"></a><span data-ttu-id="d0598-107">Member</span><span class="sxs-lookup"><span data-stu-id="d0598-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d0598-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="d0598-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="d0598-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="d0598-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="d0598-110">**dwchannel**</span><span class="sxs-lookup"><span data-stu-id="d0598-110">**dwChannel**</span></span>
</dt> <dd>

<span data-ttu-id="d0598-111">Neue Channelnummer.</span><span class="sxs-lookup"><span data-stu-id="d0598-111">New channel number.</span></span>

</dd> <dt>

<span data-ttu-id="d0598-112">**dwnumber**</span><span class="sxs-lookup"><span data-stu-id="d0598-112">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="d0598-113">Logischer Tuner, auf den der [**MCI- \_ settuner**](mci-settuner.md) -Befehl wirkt.</span><span class="sxs-lookup"><span data-stu-id="d0598-113">Logical tuner that the [**MCI\_SETTUNER**](mci-settuner.md) command affects.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0598-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0598-114">Remarks</span></span>

<span data-ttu-id="d0598-115">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d0598-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0598-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0598-116">Requirements</span></span>



| <span data-ttu-id="d0598-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d0598-117">Requirement</span></span> | <span data-ttu-id="d0598-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d0598-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d0598-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d0598-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d0598-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d0598-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d0598-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d0598-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d0598-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d0598-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d0598-123">Header</span><span class="sxs-lookup"><span data-stu-id="d0598-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0598-124"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0598-124"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0598-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0598-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0598-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="d0598-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d0598-127">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="d0598-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="d0598-128">**MCI- \_ settuner**</span><span class="sxs-lookup"><span data-stu-id="d0598-128">**MCI\_SETTUNER**</span></span>](mci-settuner.md)
</dt> <dt>

<span data-ttu-id="d0598-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d0598-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

