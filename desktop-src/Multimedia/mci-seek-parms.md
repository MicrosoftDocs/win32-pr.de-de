---
title: MCI_SEEK_PARMS-Struktur (mciapi. h)
description: Die MCI \_ - \_ suchparametenstruktur enthält Positionsinformationen für den MCI \_ Seek-Befehl.
ms.assetid: 2c199855-2134-4709-9313-5b8d66ce4f03
keywords:
- MCI_SEEK_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SEEK_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c31f419b2458dedc19c6533e8f0f7fade97026e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740488"
---
# <a name="mci_seek_parms-structure"></a><span data-ttu-id="0da9e-104">Struktur der MCI- \_ Such \_ Teilwerte</span><span class="sxs-lookup"><span data-stu-id="0da9e-104">MCI\_SEEK\_PARMS structure</span></span>

<span data-ttu-id="0da9e-105">Die **MCI \_ - \_ suchparametenstruktur** enthält Positionsinformationen für den [**MCI \_ Seek**](mci-seek.md) -Befehl.</span><span class="sxs-lookup"><span data-stu-id="0da9e-105">The **MCI\_SEEK\_PARMS** structure contains positioning information for the [**MCI\_SEEK**](mci-seek.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="0da9e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0da9e-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTo;
} MCI_SEEK_PARMS;
```



## <a name="members"></a><span data-ttu-id="0da9e-107">Member</span><span class="sxs-lookup"><span data-stu-id="0da9e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0da9e-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="0da9e-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="0da9e-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="0da9e-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="0da9e-110">**dwto**</span><span class="sxs-lookup"><span data-stu-id="0da9e-110">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="0da9e-111">Position, an der gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="0da9e-111">Position to seek to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0da9e-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0da9e-112">Remarks</span></span>

<span data-ttu-id="0da9e-113">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="0da9e-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="0da9e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0da9e-114">Requirements</span></span>



| <span data-ttu-id="0da9e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0da9e-115">Requirement</span></span> | <span data-ttu-id="0da9e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0da9e-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0da9e-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0da9e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0da9e-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0da9e-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0da9e-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0da9e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0da9e-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0da9e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0da9e-121">Header</span><span class="sxs-lookup"><span data-stu-id="0da9e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0da9e-122"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0da9e-122"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0da9e-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0da9e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0da9e-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="0da9e-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="0da9e-125">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="0da9e-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="0da9e-126">**MCI- \_ Suche**</span><span class="sxs-lookup"><span data-stu-id="0da9e-126">**MCI\_SEEK**</span></span>](mci-seek.md)
</dt> <dt>

<span data-ttu-id="0da9e-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0da9e-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

