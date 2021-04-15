---
title: TBN_WRAPHOTITEM Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt eine Anwendung mit zwei oder mehr Symbolleisten, dass das heiße Element gerade geändert wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 169309ec-68dd-4cbb-8963-f842cf75b4fc
keywords:
- Windows-Steuerelemente für TBN_WRAPHOTITEM Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_WRAPHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58eb513780da464ead40f8a4fb1264f6268d4370
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476299"
---
# <a name="tbn_wraphotitem-notification-code"></a><span data-ttu-id="bf24e-105">TBN- \_ wraphotitem-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="bf24e-105">TBN\_WRAPHOTITEM notification code</span></span>

<span data-ttu-id="bf24e-106">Benachrichtigt eine Anwendung mit zwei oder mehr Symbolleisten, dass das heiße Element gerade geändert wird.</span><span class="sxs-lookup"><span data-stu-id="bf24e-106">Notifies an application with two or more toolbars that the hot item is about to change.</span></span> <span data-ttu-id="bf24e-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="bf24e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_WRAPHOTITEM

    lpnmtb = (NMTBWRAPHOTITEM) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="bf24e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf24e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf24e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bf24e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf24e-110">Ein Zeiger auf eine-Struktur, die das alte Hot-Element (**iStart**) enthält, und ob das neue heiße Element vor dem Element (**Idir** =-1) oder danach (**Idir** = 1) ist. Außerdem wird ein Grund dafür angezeigt, warum das heiße Element geändert wird.</span><span class="sxs-lookup"><span data-stu-id="bf24e-110">A pointer to a structure that contains the old hot item (**iStart**) and whether the new hot item is before it (**iDir** = -1) or after it (**iDir** = 1), as well as a reason why the hot item is changing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf24e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bf24e-111">Return value</span></span>

<span data-ttu-id="bf24e-112">**True** , wenn die Anwendung die Änderung des aktiven Elements selbst verarbeitet. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="bf24e-112">**TRUE** if the application is handling the hot item change itself; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf24e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf24e-113">Remarks</span></span>

<span data-ttu-id="bf24e-114">Die **nmtbwraphotitem** -Struktur muss von der Anwendung wie folgt definiert werden:</span><span class="sxs-lookup"><span data-stu-id="bf24e-114">The **NMTBWRAPHOTITEM** structure must be defined by the application as follows:</span></span>

``` syntax
typedef struct tagNMTBWRAPHOTITEM {
    NMHDR hdr;
    int iStart;
    int iDir;
    UINT nReason;       // HICF_* flags
} NMTBWRAPHOTITEM, *LPNMTBWRAPHOTITEM;
```

## <a name="requirements"></a><span data-ttu-id="bf24e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bf24e-115">Requirements</span></span>



| <span data-ttu-id="bf24e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bf24e-116">Requirement</span></span> | <span data-ttu-id="bf24e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="bf24e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf24e-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bf24e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bf24e-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bf24e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bf24e-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bf24e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bf24e-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bf24e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bf24e-122">Header</span><span class="sxs-lookup"><span data-stu-id="bf24e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf24e-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf24e-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





