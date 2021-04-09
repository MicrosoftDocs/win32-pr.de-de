---
title: MCI_VCR_SETAUDIO_PARMS Struktur (VCR. h)
description: Die Struktur der MCI- \_ VCR \_ - \_ setaudioparameter enthält Parameter für den MCI \_ setaudiobefehl für Video-Kassetten-Recorder.
ms.assetid: 328d8e63-7ddd-4c9b-85d6-2e56fd802dbc
keywords:
- MCI_VCR_SETAUDIO_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_SETAUDIO_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 143345f494f381054335d2dfec3b0c10222adca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858708"
---
# <a name="mci_vcr_setaudio_parms-structure"></a><span data-ttu-id="11767-104">MCI \_ VCR \_ -setaudioparamemstruktur \_</span><span class="sxs-lookup"><span data-stu-id="11767-104">MCI\_VCR\_SETAUDIO\_PARMS structure</span></span>

<span data-ttu-id="11767-105">Die Struktur der **MCI- \_ VCR \_ -setaudioparameter \_** enthält Parameter für den [**MCI \_ setaudiobefehl**](mci-setaudio.md) für Video-Kassetten-Recorder.</span><span class="sxs-lookup"><span data-stu-id="11767-105">The **MCI\_VCR\_SETAUDIO\_PARMS** structure contains parameters for the [**MCI\_SETAUDIO**](mci-setaudio.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="11767-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="11767-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SETAUDIO_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTrack;
  DWORD     dwTo;
  DWORD     dwNumber;
} MCI_VCR_SETAUDIO_PARMS;
```



## <a name="members"></a><span data-ttu-id="11767-107">Member</span><span class="sxs-lookup"><span data-stu-id="11767-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="11767-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="11767-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="11767-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="11767-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="11767-110">**dwtrack**</span><span class="sxs-lookup"><span data-stu-id="11767-110">**dwTrack**</span></span>
</dt> <dd>

<span data-ttu-id="11767-111">Audiospur.</span><span class="sxs-lookup"><span data-stu-id="11767-111">Audio track.</span></span>

</dd> <dt>

<span data-ttu-id="11767-112">**dwto**</span><span class="sxs-lookup"><span data-stu-id="11767-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="11767-113">Typ der Eingabe-oder überwachten Eingabe.</span><span class="sxs-lookup"><span data-stu-id="11767-113">Type of input or monitored input.</span></span>

</dd> <dt>

<span data-ttu-id="11767-114">**dwnumber**</span><span class="sxs-lookup"><span data-stu-id="11767-114">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="11767-115">Audioeingabe (des Typs, der im **dwto** -Member angegeben ist), der verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="11767-115">Audio input (of the type specified in the **dwTo** member) to use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="11767-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11767-116">Remarks</span></span>

<span data-ttu-id="11767-117">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="11767-117">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="11767-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11767-118">Requirements</span></span>



| <span data-ttu-id="11767-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11767-119">Requirement</span></span> | <span data-ttu-id="11767-120">Wert</span><span class="sxs-lookup"><span data-stu-id="11767-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="11767-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11767-121">Minimum supported client</span></span><br/> | <span data-ttu-id="11767-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11767-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="11767-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11767-123">Minimum supported server</span></span><br/> | <span data-ttu-id="11767-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11767-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="11767-125">Header</span><span class="sxs-lookup"><span data-stu-id="11767-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="11767-126"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="11767-126"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11767-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11767-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11767-128">**MCI**</span><span class="sxs-lookup"><span data-stu-id="11767-128">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="11767-129">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="11767-129">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="11767-130">**MCI \_ -setaudiodatei**</span><span class="sxs-lookup"><span data-stu-id="11767-130">**MCI\_SETAUDIO**</span></span>](mci-setaudio.md)
</dt> <dt>

<span data-ttu-id="11767-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="11767-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

