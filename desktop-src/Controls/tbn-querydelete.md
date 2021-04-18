---
title: TBN_QUERYDELETE Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster der Symbolleiste, ob eine Schaltfläche aus einer Symbolleiste gelöscht werden kann, während der Benutzer die Symbolleiste anpasst. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: fa6a8fe4-a9a3-4c59-9237-d28bd34d664c
keywords:
- Windows-Steuerelemente für TBN_QUERYDELETE Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_QUERYDELETE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a416545ecf7ad8562c1327160d683a109eccb3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517360"
---
# <a name="tbn_querydelete-notification-code"></a><span data-ttu-id="81e6f-105">TBN- \_ querydelete-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="81e6f-105">TBN\_QUERYDELETE notification code</span></span>

<span data-ttu-id="81e6f-106">Benachrichtigt das übergeordnete Fenster der Symbolleiste, ob eine Schaltfläche aus einer Symbolleiste gelöscht werden kann, während der Benutzer die Symbolleiste anpasst.</span><span class="sxs-lookup"><span data-stu-id="81e6f-106">Notifies the toolbar's parent window whether a button may be deleted from a toolbar while the user is customizing the toolbar.</span></span> <span data-ttu-id="81e6f-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="81e6f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_QUERYDELETE 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="81e6f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="81e6f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81e6f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="81e6f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81e6f-110">Zeiger auf eine [**nmtoolbar**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="81e6f-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="81e6f-111">Das **iItem** -Member enthält den nullbasierten Index der zu löschenden Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="81e6f-111">The **iItem** member contains the zero-based index of the button to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81e6f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81e6f-112">Return value</span></span>

<span data-ttu-id="81e6f-113">Gibt **true** zurück, um das Löschen der Schaltfläche zuzulassen, oder **false** , um zu verhindern, dass die Schaltfläche gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="81e6f-113">Returns **TRUE** to allow the button to be deleted, or **FALSE** to prevent the button from being deleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="81e6f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81e6f-114">Requirements</span></span>



| <span data-ttu-id="81e6f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81e6f-115">Requirement</span></span> | <span data-ttu-id="81e6f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="81e6f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81e6f-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="81e6f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="81e6f-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81e6f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="81e6f-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="81e6f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="81e6f-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81e6f-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="81e6f-121">Header</span><span class="sxs-lookup"><span data-stu-id="81e6f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="81e6f-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="81e6f-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





