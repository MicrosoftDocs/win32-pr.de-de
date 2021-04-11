---
title: TBN_DUPACCELERATOR Benachrichtigungs Code (kommctrl. h)
description: Gibt an, ob eine Zugriffstaste auf zwei oder mehr aktiven Symbolleisten verwendet werden kann. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 98068d1a-1460-4be3-8575-9294b82ce903
keywords:
- Windows-Steuerelemente für TBN_DUPACCELERATOR Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_DUPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e530fa2101f8145148b7ede7d74f53a1828fa58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040837"
---
# <a name="tbn_dupaccelerator-notification-code"></a><span data-ttu-id="f5e67-105">TBN- \_ dupaccelerators-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="f5e67-105">TBN\_DUPACCELERATOR notification code</span></span>

<span data-ttu-id="f5e67-106">Gibt an, ob eine Zugriffstaste auf zwei oder mehr aktiven Symbolleisten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f5e67-106">Ascertains whether an accelerator key can be used on two or more active toolbars.</span></span> <span data-ttu-id="f5e67-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="f5e67-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_DUPACCELERATOR

    lpnmtb = (NMTBDUPACCELERATOR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f5e67-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5e67-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5e67-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f5e67-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5e67-110">Ein Zeiger auf eine-Struktur, die eine Zugriffstaste bietet und einen Wert empfängt, der angibt, ob mehrere Symbolleisten auf dasselbe Zeichen reagieren.</span><span class="sxs-lookup"><span data-stu-id="f5e67-110">A pointer to a structure that provides an accelerator and that receives a value specifying whether multiple toolbars respond to the same character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5e67-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f5e67-111">Return value</span></span>

<span data-ttu-id="f5e67-112">Gibt **true** zurück, wenn erfolgreich, andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="f5e67-112">Returns **TRUE** if successful, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5e67-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5e67-113">Remarks</span></span>

<span data-ttu-id="f5e67-114">Die Anwendung muss die **nmtbdupaccelerator** -Struktur wie folgt deklarieren:</span><span class="sxs-lookup"><span data-stu-id="f5e67-114">The application must declare the **NMTBDUPACCELERATOR** structure as follows:</span></span>

``` syntax
typedef struct tagNMTBDUPACCELERATOR
{
    NMHDR hdr;
    UINT ch;   // The accelerator.
    BOOL fDup; // TRUE if multiple toolbars respond to the accelerator.
} NMTBDUPACCELERATOR, *LPNMTBDUPACCELERATOR;
```

## <a name="requirements"></a><span data-ttu-id="f5e67-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5e67-115">Requirements</span></span>



| <span data-ttu-id="f5e67-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5e67-116">Requirement</span></span> | <span data-ttu-id="f5e67-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f5e67-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f5e67-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f5e67-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f5e67-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5e67-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f5e67-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f5e67-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f5e67-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5e67-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f5e67-122">Header</span><span class="sxs-lookup"><span data-stu-id="f5e67-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5e67-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5e67-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





