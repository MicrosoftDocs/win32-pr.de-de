---
title: IPN_FIELDCHANGED Benachrichtigungs Code (kommctrl. h)
description: Wird gesendet, wenn der Benutzer ein Feld im Steuerelement ändert oder von einem Feld zu einem anderen verschoben wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: f9ca6435-1715-458e-8d0e-475920ed75bd
keywords:
- Windows-Steuerelemente für IPN_FIELDCHANGED Benachrichtigungs
topic_type:
- apiref
api_name:
- IPN_FIELDCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e283d42d0aba3c237db51fe492a34ec93e8eb73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040855"
---
# <a name="ipn_fieldchanged-notification-code"></a><span data-ttu-id="5c095-105">IPN \_ FieldChanged-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="5c095-105">IPN\_FIELDCHANGED notification code</span></span>

<span data-ttu-id="5c095-106">Wird gesendet, wenn der Benutzer ein Feld im Steuerelement ändert oder von einem Feld zu einem anderen verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="5c095-106">Sent when the user changes a field in the control or moves from one field to another.</span></span> <span data-ttu-id="5c095-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="5c095-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
IPN_FIELDCHANGED

    lpnmipa = (LPNMIPADDRESS) lParam;
```



## <a name="parameters"></a><span data-ttu-id="5c095-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c095-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c095-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5c095-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c095-110">Ein Zeiger auf eine [**nmipaddress**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) -Struktur, die Informationen über die geänderte Adresse enthält.</span><span class="sxs-lookup"><span data-stu-id="5c095-110">A pointer to an [**NMIPADDRESS**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) structure that contains information about the changed address.</span></span> <span data-ttu-id="5c095-111">Der **iValue** -Member dieser Struktur enthält den eingegebenen Wert, auch wenn er außerhalb des Bereichs des Felds liegt.</span><span class="sxs-lookup"><span data-stu-id="5c095-111">The **iValue** member of this structure will contain the entered value, even if it is out of the range of the field.</span></span> <span data-ttu-id="5c095-112">Sie können dieses Element in einen beliebigen Wert ändern, der als Reaktion auf diesen Benachrichtigungs Code innerhalb des Bereichs für das Feld liegt.</span><span class="sxs-lookup"><span data-stu-id="5c095-112">You can modify this member to any value that is within the range for the field in response to this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c095-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c095-113">Return value</span></span>

<span data-ttu-id="5c095-114">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5c095-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c095-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c095-115">Remarks</span></span>

<span data-ttu-id="5c095-116">Dieser Benachrichtigungs Code wird nicht als Antwort auf eine [**IPM- \_ setAddress**](ipm-setaddress.md) -Nachricht gesendet.</span><span class="sxs-lookup"><span data-stu-id="5c095-116">This notification code is not sent in response to a [**IPM\_SETADDRESS**](ipm-setaddress.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c095-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c095-117">Requirements</span></span>



| <span data-ttu-id="5c095-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c095-118">Requirement</span></span> | <span data-ttu-id="5c095-119">Wert</span><span class="sxs-lookup"><span data-stu-id="5c095-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5c095-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5c095-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5c095-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c095-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5c095-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5c095-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5c095-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c095-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5c095-124">Header</span><span class="sxs-lookup"><span data-stu-id="5c095-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c095-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c095-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





