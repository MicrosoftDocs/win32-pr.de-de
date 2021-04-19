---
title: TBN_WRAPACCELERATOR Benachrichtigungs Code (kommctrl. h)
description: Fordert den Index der Schaltfläche in einem oder mehreren Symbolleisten an, der dem angegebenen Zugriffstasten Zeichen entspricht. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: fc2443fd-e1b3-4085-b65d-96c08f544944
keywords:
- Windows-Steuerelemente für TBN_WRAPACCELERATOR Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_WRAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ed5e6063f8ac32b317b8f7ce37682b151c56a4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340983"
---
# <a name="tbn_wrapaccelerator-notification-code"></a><span data-ttu-id="a0f4c-105">TBN- \_ wrapaccelerator-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="a0f4c-105">TBN\_WRAPACCELERATOR notification code</span></span>

<span data-ttu-id="a0f4c-106">Fordert den Index der Schaltfläche in einem oder mehreren Symbolleisten an, der dem angegebenen Zugriffstasten Zeichen entspricht.</span><span class="sxs-lookup"><span data-stu-id="a0f4c-106">Requests the index of the button in one or more toolbars corresponding to the specified accelerator character.</span></span> <span data-ttu-id="a0f4c-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="a0f4c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_WRAPACCELERATOR

    lpnmtb = (NMTBWRAPACCELERATOR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a0f4c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0f4c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0f4c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a0f4c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0f4c-110">Ein Zeiger auf eine-Struktur, die das Tastenkombination-Zeichen enthält und den Index der entsprechenden Schaltfläche empfängt.</span><span class="sxs-lookup"><span data-stu-id="a0f4c-110">A pointer to a structure that contains the accelerator key character, and that receives the index of the corresponding button.</span></span> <span data-ttu-id="a0f4c-111">Der Index ist-1, wenn die Zugriffstaste keinem Befehl entspricht.</span><span class="sxs-lookup"><span data-stu-id="a0f4c-111">The index is -1 if the accelerator does not correspond to a command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0f4c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a0f4c-112">Return value</span></span>

<span data-ttu-id="a0f4c-113">**True** , wenn ein Index zurückgegeben wird, andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="a0f4c-113">**TRUE** if an index is returned, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0f4c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0f4c-114">Remarks</span></span>

<span data-ttu-id="a0f4c-115">Anwendungen mit einem oder mehreren Symbolleisten können diesen Benachrichtigungs Code erhalten.</span><span class="sxs-lookup"><span data-stu-id="a0f4c-115">Applications with one or more toolbars may receive this notification code.</span></span>

<span data-ttu-id="a0f4c-116">Die **nmtbwrapaccelerator** -Struktur muss von der Anwendung wie folgt definiert werden:</span><span class="sxs-lookup"><span data-stu-id="a0f4c-116">The **NMTBWRAPACCELERATOR** structure must be defined by the application as follows:</span></span>

``` syntax
typedef struct tagNMTBWRAPACCELERATOR {
    NMHDR hdr;
    UINT ch;
    int iButton;
} NMTBWRAPACCELERATOR, *LPNMTBWRAPACCELERATOR;
```

## <a name="requirements"></a><span data-ttu-id="a0f4c-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0f4c-117">Requirements</span></span>



| <span data-ttu-id="a0f4c-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0f4c-118">Requirement</span></span> | <span data-ttu-id="a0f4c-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a0f4c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0f4c-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a0f4c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a0f4c-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a0f4c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a0f4c-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a0f4c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a0f4c-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a0f4c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a0f4c-124">Header</span><span class="sxs-lookup"><span data-stu-id="a0f4c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0f4c-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0f4c-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





