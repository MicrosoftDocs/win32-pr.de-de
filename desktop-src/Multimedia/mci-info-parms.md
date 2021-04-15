---
title: MCI_INFO_PARMS-Struktur (mciapi. h)
description: Die Struktur der MCI-info-Parameter \_ \_ enthält Informationen zum MCI- \_ Befehl "Info".
ms.assetid: c64cff7d-a6d5-44b7-8cfb-9593f6328832
keywords:
- MCI_INFO_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_INFO_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d23221d140aaf093525691d7127c8466f392b95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479143"
---
# <a name="mci_info_parms-structure"></a><span data-ttu-id="3451a-104">MCI-info-Parameter \_ \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="3451a-104">MCI\_INFO\_PARMS structure</span></span>

<span data-ttu-id="3451a-105">Die Struktur der **MCI- \_ Info \_** -Parameter enthält Informationen zum MCI-Befehl " [**\_ Info**](mci-info.md) ".</span><span class="sxs-lookup"><span data-stu-id="3451a-105">The **MCI\_INFO\_PARMS** structure contains information for the [**MCI\_INFO**](mci-info.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="3451a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3451a-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPTSTR    lpstrReturn;
  DWORD     dwRetSize;
} MCI_INFO_PARMS;
```



## <a name="members"></a><span data-ttu-id="3451a-107">Member</span><span class="sxs-lookup"><span data-stu-id="3451a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3451a-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="3451a-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="3451a-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="3451a-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="3451a-110">**lpstraureturn**</span><span class="sxs-lookup"><span data-stu-id="3451a-110">**lpstrReturn**</span></span>
</dt> <dd>

<span data-ttu-id="3451a-111">Puffer für die Rückgabe Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="3451a-111">Buffer for return string.</span></span>

</dd> <dt>

<span data-ttu-id="3451a-112">**dwretsize**</span><span class="sxs-lookup"><span data-stu-id="3451a-112">**dwRetSize**</span></span>
</dt> <dd>

<span data-ttu-id="3451a-113">Die Größe der Rückgabe Zeichenfolge in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="3451a-113">Size, in characters, of return string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3451a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3451a-114">Remarks</span></span>

<span data-ttu-id="3451a-115">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3451a-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="3451a-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3451a-116">Requirements</span></span>



| <span data-ttu-id="3451a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3451a-117">Requirement</span></span> | <span data-ttu-id="3451a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="3451a-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3451a-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3451a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3451a-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3451a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3451a-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3451a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3451a-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3451a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3451a-123">Header</span><span class="sxs-lookup"><span data-stu-id="3451a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3451a-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3451a-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3451a-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3451a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3451a-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="3451a-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3451a-127">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="3451a-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="3451a-128">**MCI- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="3451a-128">**MCI\_INFO**</span></span>](mci-info.md)
</dt> <dt>

<span data-ttu-id="3451a-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3451a-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

