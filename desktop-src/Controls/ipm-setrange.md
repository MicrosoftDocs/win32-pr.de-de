---
title: IPM_SETRANGE Meldung (kommstrg. h)
description: Legt den gültigen Bereich für das angegebene Feld im IP-Adress Steuerelement fest.
ms.assetid: 03068c5d-822f-459d-8f79-e7f0430a27bf
keywords:
- Windows-Steuerelemente für IPM_SETRANGE Meldung
topic_type:
- apiref
api_name:
- IPM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e70df7b2b8f76f514d9a0cc6101aba2ee7cf4ec6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040856"
---
# <a name="ipm_setrange-message"></a><span data-ttu-id="8cefc-104">IPM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="8cefc-104">IPM\_SETRANGE message</span></span>

<span data-ttu-id="8cefc-105">Legt den gültigen Bereich für das angegebene Feld im IP-Adress Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="8cefc-105">Sets the valid range for the specified field in the IP address control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8cefc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cefc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cefc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8cefc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8cefc-108">Ein NULL basierter Feld Index, auf den der Bereich angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8cefc-108">A zero-based field index to which the range will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="8cefc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8cefc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8cefc-110">Ein **Word** -Wert, der die untere Grenze des Bereichs in dem nieder wertigen Byte und die Obergrenze im höherwertigen Byte enthält.</span><span class="sxs-lookup"><span data-stu-id="8cefc-110">A **WORD** value that contains the lower limit of the range in the low-order byte and the upper limit in the high-order byte.</span></span> <span data-ttu-id="8cefc-111">Beide Werte sind inklusiv.</span><span class="sxs-lookup"><span data-stu-id="8cefc-111">Both of these values are inclusive.</span></span> <span data-ttu-id="8cefc-112">Das [**makeiprange**](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange) -Makro kann auch verwendet werden, um den Bereich zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8cefc-112">The [**MAKEIPRANGE**](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange) macro can also be used to create the range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cefc-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8cefc-113">Return value</span></span>

<span data-ttu-id="8cefc-114">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="8cefc-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cefc-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8cefc-115">Remarks</span></span>

<span data-ttu-id="8cefc-116">Wenn der Benutzer einen Wert in das Feld eingibt, der außerhalb dieses Bereichs liegt, sendet das Steuerelement die [IPN \_ FieldChanged](ipn-fieldchanged.md) -Benachrichtigung mit dem eingegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="8cefc-116">If the user enters a value in the field that is outside of this range, the control will send the [IPN\_FIELDCHANGED](ipn-fieldchanged.md) notification with the entered value.</span></span> <span data-ttu-id="8cefc-117">Wenn der Wert nach dem Senden der Benachrichtigung noch außerhalb des Bereichs liegt, versucht das Steuerelement, den eingegebenen Wert in den nächstgelegenen Bereichs Grenzwert zu ändern.</span><span class="sxs-lookup"><span data-stu-id="8cefc-117">If the value is still outside of the range after sending the notification, the control will attempt to change the entered value to the closest range limit.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cefc-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8cefc-118">Requirements</span></span>



| <span data-ttu-id="8cefc-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8cefc-119">Requirement</span></span> | <span data-ttu-id="8cefc-120">Wert</span><span class="sxs-lookup"><span data-stu-id="8cefc-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8cefc-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8cefc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8cefc-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8cefc-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8cefc-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8cefc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8cefc-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8cefc-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8cefc-125">Header</span><span class="sxs-lookup"><span data-stu-id="8cefc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cefc-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cefc-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





