---
title: MCI_VCR_LIST_PARMS Struktur (VCR. h)
description: Die Struktur der MCI- \_ VCR- \_ Listen \_ Parameter enthält Parameter für den MCI- \_ Listen Befehl für Video-Kassetten-Recorder.
ms.assetid: 88725599-8057-4787-96e6-49b4a651c894
keywords:
- MCI_VCR_LIST_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_LIST_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d3e7a2eae67ebc7148b7ff424361f16554a435c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341157"
---
# <a name="mci_vcr_list_parms-structure"></a><span data-ttu-id="6fc48-104">Struktur von MCI- \_ VCR- \_ Listen- \_ Parametern</span><span class="sxs-lookup"><span data-stu-id="6fc48-104">MCI\_VCR\_LIST\_PARMS structure</span></span>

<span data-ttu-id="6fc48-105">Die Struktur der **MCI- \_ VCR- \_ Listen \_** Parameter enthält Parameter für den [**MCI- \_ Listen**](mci-list.md) Befehl für Video-Kassetten-Recorder.</span><span class="sxs-lookup"><span data-stu-id="6fc48-105">The **MCI\_VCR\_LIST\_PARMS** structure contains parameters for the [**MCI\_LIST**](mci-list.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fc48-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fc48-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_LIST_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwNumber;
} MCI_VCR_LIST_PARMS;
```



## <a name="members"></a><span data-ttu-id="6fc48-107">Member</span><span class="sxs-lookup"><span data-stu-id="6fc48-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6fc48-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="6fc48-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="6fc48-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="6fc48-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="6fc48-110">**dwreturn**</span><span class="sxs-lookup"><span data-stu-id="6fc48-110">**dwReturn**</span></span>
</dt> <dd>

<span data-ttu-id="6fc48-111">Der Puffer für die zurückgegebenen Informationen.</span><span class="sxs-lookup"><span data-stu-id="6fc48-111">Buffer for returned information.</span></span>

</dd> <dt>

<span data-ttu-id="6fc48-112">**dwnumber**</span><span class="sxs-lookup"><span data-stu-id="6fc48-112">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="6fc48-113">Die Anzahl der Video-oder Audioeingaben von VCR.</span><span class="sxs-lookup"><span data-stu-id="6fc48-113">Number of VCR's video or audio inputs.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6fc48-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6fc48-114">Remarks</span></span>

<span data-ttu-id="6fc48-115">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="6fc48-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fc48-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6fc48-116">Requirements</span></span>



| <span data-ttu-id="6fc48-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6fc48-117">Requirement</span></span> | <span data-ttu-id="6fc48-118">Wert</span><span class="sxs-lookup"><span data-stu-id="6fc48-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6fc48-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6fc48-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6fc48-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6fc48-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6fc48-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6fc48-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6fc48-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6fc48-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6fc48-123">Header</span><span class="sxs-lookup"><span data-stu-id="6fc48-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fc48-124"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fc48-124"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fc48-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6fc48-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fc48-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="6fc48-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6fc48-127">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="6fc48-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="6fc48-128">**MCI- \_ Liste**</span><span class="sxs-lookup"><span data-stu-id="6fc48-128">**MCI\_LIST**</span></span>](mci-list.md)
</dt> <dt>

<span data-ttu-id="6fc48-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6fc48-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

