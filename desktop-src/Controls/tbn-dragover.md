---
title: TBN_DRAGOVER Benachrichtigungs Code (kommctrl. h)
description: Gibt an, ob eine TB- \_ markbutton-Nachricht für eine Schaltfläche gesendet werden soll, die gezogen wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 2bb5c52e-0c90-4662-8ffd-045ecc7ed7e5
keywords:
- Windows-Steuerelemente für TBN_DRAGOVER Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_DRAGOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa02aa8fabf89ea27fce628d3d63165255bbd66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475903"
---
# <a name="tbn_dragover-notification-code"></a><span data-ttu-id="98be4-105">TBN- \_ DragOver-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="98be4-105">TBN\_DRAGOVER notification code</span></span>

<span data-ttu-id="98be4-106">Gibt an, ob eine [**TB- \_ markbutton**](tb-markbutton.md) -Nachricht für eine Schaltfläche gesendet werden soll, die gezogen wird.</span><span class="sxs-lookup"><span data-stu-id="98be4-106">Ascertains whether a [**TB\_MARKBUTTON**](tb-markbutton.md) message should be sent for a button that is being dragged over.</span></span> <span data-ttu-id="98be4-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="98be4-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_DRAGOVER

    lpnmtb = (NMTBHOTITEM*) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="98be4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="98be4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98be4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="98be4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98be4-110">Ein Zeiger auf eine [**nmtbhutitem**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) -Struktur, die angibt, auf welches Element gezogen wird.</span><span class="sxs-lookup"><span data-stu-id="98be4-110">A pointer to an [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) structure that specifies which item is being dragged over.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98be4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="98be4-111">Return value</span></span>

<span data-ttu-id="98be4-112">**False** , wenn die Symbolleiste eine TB- \_ markbutton-Nachricht senden soll; andernfalls **true**.</span><span class="sxs-lookup"><span data-stu-id="98be4-112">**FALSE** if the toolbar should send a TB\_MARKBUTTON message; otherwise **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="98be4-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98be4-113">Requirements</span></span>



| <span data-ttu-id="98be4-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98be4-114">Requirement</span></span> | <span data-ttu-id="98be4-115">Wert</span><span class="sxs-lookup"><span data-stu-id="98be4-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="98be4-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="98be4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="98be4-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98be4-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="98be4-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="98be4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="98be4-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98be4-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="98be4-120">Header</span><span class="sxs-lookup"><span data-stu-id="98be4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="98be4-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="98be4-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





