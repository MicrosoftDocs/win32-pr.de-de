---
title: PGN_CALCSIZE Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Pager-Steuerelement gesendet, um die scrollbaren Dimensionen des enthaltenen Fensters abzurufen.
ms.assetid: a15f4191-2f26-4139-bdaf-bab219449b78
keywords:
- Windows-Steuerelemente für PGN_CALCSIZE Benachrichtigungs
topic_type:
- apiref
api_name:
- PGN_CALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ee6de1c45402f8bdc154f9f10be00140d7c766c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741217"
---
# <a name="pgn_calcsize-notification-code"></a><span data-ttu-id="055cf-104">PGN \_ calcsize-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="055cf-104">PGN\_CALCSIZE notification code</span></span>

<span data-ttu-id="055cf-105">Wird von einem Pager-Steuerelement gesendet, um die scrollbaren Dimensionen des enthaltenen Fensters abzurufen.</span><span class="sxs-lookup"><span data-stu-id="055cf-105">Sent by a pager control to obtain the scrollable dimensions of the contained window.</span></span> <span data-ttu-id="055cf-106">Diese Dimensionen werden vom Pager-Steuerelement zum Bestimmen der scrollbaren Größe des enthaltenen Fensters verwendet.</span><span class="sxs-lookup"><span data-stu-id="055cf-106">These dimensions are used by the pager control to determine the scrollable size of the contained window.</span></span> <span data-ttu-id="055cf-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="055cf-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PGN_CALCSIZE

    lpnmcs = (LPNMPGCALCSIZE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="055cf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="055cf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="055cf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="055cf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="055cf-110">Ein Zeiger auf eine [**nmpgcalcsize**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) -Struktur, die Informationen über den Benachrichtigungs Code enthält und empfängt.</span><span class="sxs-lookup"><span data-stu-id="055cf-110">Pointer to an [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) structure that contains and receives information about the notification code.</span></span> <span data-ttu-id="055cf-111">Der **dwFlag** -Member dieser Struktur gibt an, welche Dimension berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="055cf-111">The **dwFlag** member of this structure indicates which dimension is being calculated.</span></span> <span data-ttu-id="055cf-112">Abhängig vom Wert von **dwFlag** sollten Sie die gewünschte Dimension im **iWidth** -oder **iHeight** -Member dieser Struktur platzieren.</span><span class="sxs-lookup"><span data-stu-id="055cf-112">Depending on the value of **dwFlag**, you should place the desired dimension in the **iWidth** or **iHeight** member of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="055cf-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="055cf-113">Return value</span></span>

<span data-ttu-id="055cf-114">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="055cf-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="055cf-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="055cf-115">Requirements</span></span>



| <span data-ttu-id="055cf-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="055cf-116">Requirement</span></span> | <span data-ttu-id="055cf-117">Wert</span><span class="sxs-lookup"><span data-stu-id="055cf-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="055cf-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="055cf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="055cf-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="055cf-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="055cf-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="055cf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="055cf-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="055cf-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="055cf-122">Header</span><span class="sxs-lookup"><span data-stu-id="055cf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="055cf-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="055cf-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





