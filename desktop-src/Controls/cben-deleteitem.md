---
title: CBEN_DELETEITEM Benachrichtigungs Code (kommctrl. h)
description: Wird gesendet, wenn ein Element gelöscht wurde. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 8b0d03ff-57fa-44dc-ab3e-05089b876e3c
keywords:
- Windows-Steuerelemente für CBEN_DELETEITEM Benachrichtigungs
topic_type:
- apiref
api_name:
- CBEN_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4c7ca7329898c9dd0c6bba76cba9d3524b017e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859206"
---
# <a name="cben_deleteitem-notification-code"></a><span data-ttu-id="f42f7-105">Cben \_ DeleteItem-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="f42f7-105">CBEN\_DELETEITEM notification code</span></span>

<span data-ttu-id="f42f7-106">Wird gesendet, wenn ein Element gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="f42f7-106">Sent when an item has been deleted.</span></span> <span data-ttu-id="f42f7-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="f42f7-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_DELETEITEM

    pCBEx = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a><span data-ttu-id="f42f7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f42f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f42f7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f42f7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f42f7-110">Ein Zeiger auf eine [**nmcomboboxex**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) -Struktur, die Informationen über den Benachrichtigungs Code und das gelöschte Element enthält.</span><span class="sxs-lookup"><span data-stu-id="f42f7-110">A pointer to an [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) structure that contains information about the notification code and the deleted item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f42f7-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f42f7-111">Return value</span></span>

<span data-ttu-id="f42f7-112">Die Anwendung, die diesen Benachrichtigungs Code verarbeitet, muss NULL zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f42f7-112">The application processing this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="f42f7-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f42f7-113">Requirements</span></span>



| <span data-ttu-id="f42f7-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f42f7-114">Requirement</span></span> | <span data-ttu-id="f42f7-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f42f7-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f42f7-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f42f7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f42f7-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f42f7-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f42f7-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f42f7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f42f7-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f42f7-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f42f7-120">Header</span><span class="sxs-lookup"><span data-stu-id="f42f7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f42f7-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f42f7-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





