---
title: MCI_VD_ESCAPE_PARMS-Struktur (mciapi. h)
description: Die MCI-VD-escapeparameterstruktur \_ \_ \_ enthält den Befehl, der für den Befehl "MCI-Escapezeichen" an ein Gerät gesendet wird \_ .
ms.assetid: 7c735943-b67a-4be5-82b5-6a058349623e
keywords:
- MCI_VD_ESCAPE_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VD_ESCAPE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a80712cd693e2c7ebe290be6b9827c1e051dd86a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339959"
---
# <a name="mci_vd_escape_parms-structure"></a><span data-ttu-id="257a7-104">MCI-VD-escapeparameterstruktur \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="257a7-104">MCI\_VD\_ESCAPE\_PARMS structure</span></span>

<span data-ttu-id="257a7-105">Die **MCI- \_ VD \_ \_** -escapeparameterstruktur enthält den Befehl, der für den Befehl " [**MCI \_**](mci-escape.md) -Escapezeichen" an ein Gerät gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="257a7-105">The **MCI\_VD\_ESCAPE\_PARMS** structure contains the command sent to a device for the [**MCI\_ESCAPE**](mci-escape.md) command for videodisc devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="257a7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="257a7-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpstrCommand;
} MCI_VD_ESCAPE_PARMS;
```



## <a name="members"></a><span data-ttu-id="257a7-107">Member</span><span class="sxs-lookup"><span data-stu-id="257a7-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="257a7-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="257a7-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="257a7-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="257a7-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="257a7-110">**lpstraucommand**</span><span class="sxs-lookup"><span data-stu-id="257a7-110">**lpstrCommand**</span></span>
</dt> <dd>

<span data-ttu-id="257a7-111">Befehl, der an das Gerät gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="257a7-111">Command to send to device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="257a7-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="257a7-112">Remarks</span></span>

<span data-ttu-id="257a7-113">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="257a7-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="257a7-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="257a7-114">Requirements</span></span>



| <span data-ttu-id="257a7-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="257a7-115">Requirement</span></span> | <span data-ttu-id="257a7-116">Wert</span><span class="sxs-lookup"><span data-stu-id="257a7-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="257a7-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="257a7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="257a7-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="257a7-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="257a7-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="257a7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="257a7-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="257a7-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="257a7-121">Header</span><span class="sxs-lookup"><span data-stu-id="257a7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="257a7-122"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="257a7-122"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="257a7-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="257a7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="257a7-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="257a7-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="257a7-125">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="257a7-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="257a7-126">**MCI- \_ Escape**</span><span class="sxs-lookup"><span data-stu-id="257a7-126">**MCI\_ESCAPE**</span></span>](mci-escape.md)
</dt> <dt>

<span data-ttu-id="257a7-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="257a7-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

