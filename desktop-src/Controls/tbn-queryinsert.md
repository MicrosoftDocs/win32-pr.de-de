---
title: TBN_QUERYINSERT Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster der Symbolleiste, ob links neben der angegebenen Schaltfläche eine Schaltfläche eingefügt werden kann, während der Benutzer eine Symbolleiste anpasst. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: d389fabb-16f6-43aa-a4b6-abb80723345b
keywords:
- Windows-Steuerelemente für TBN_QUERYINSERT Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_QUERYINSERT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1a21e9ade8f54ffe27ebffdfc2a8b535b4b3630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957101"
---
# <a name="tbn_queryinsert-notification-code"></a><span data-ttu-id="508c8-105">TBN \_ queryinsert-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="508c8-105">TBN\_QUERYINSERT notification code</span></span>

<span data-ttu-id="508c8-106">Benachrichtigt das übergeordnete Fenster der Symbolleiste, ob links neben der angegebenen Schaltfläche eine Schaltfläche eingefügt werden kann, während der Benutzer eine Symbolleiste anpasst.</span><span class="sxs-lookup"><span data-stu-id="508c8-106">Notifies the toolbar's parent window whether a button may be inserted to the left of the specified button while the user is customizing a toolbar.</span></span> <span data-ttu-id="508c8-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="508c8-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_QUERYINSERT 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="508c8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="508c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="508c8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="508c8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="508c8-110">Zeiger auf eine [**nmtoolbar**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="508c8-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="508c8-111">Das **iItem** -Member enthält den nullbasierten Index der einzufügenden Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="508c8-111">The **iItem** member contains the zero-based index of the button to be inserted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="508c8-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="508c8-112">Return value</span></span>

<span data-ttu-id="508c8-113">Gibt **true** zurück, um zuzulassen, dass eine Schaltfläche vor der angegebenen Schaltfläche eingefügt wird, oder **false** , um zu verhindern, dass die Schaltfläche eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="508c8-113">Return **TRUE** to allow a button to be inserted in front of the given button, or **FALSE** to prevent the button from being inserted.</span></span>

## <a name="requirements"></a><span data-ttu-id="508c8-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="508c8-114">Requirements</span></span>



| <span data-ttu-id="508c8-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="508c8-115">Requirement</span></span> | <span data-ttu-id="508c8-116">Wert</span><span class="sxs-lookup"><span data-stu-id="508c8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="508c8-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="508c8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="508c8-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="508c8-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="508c8-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="508c8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="508c8-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="508c8-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="508c8-121">Header</span><span class="sxs-lookup"><span data-stu-id="508c8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="508c8-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="508c8-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





