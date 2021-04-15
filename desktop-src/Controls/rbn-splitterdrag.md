---
title: RBN_SPLITTERDRAG Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Grund leisten-Steuerelement gesendet, wenn der Benutzer einen Splitter zieht. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 7827c971-6a92-452f-b961-1abe6ae66d2a
keywords:
- Windows-Steuerelemente für RBN_SPLITTERDRAG Benachrichtigungs
topic_type:
- apiref
api_name:
- RBN_SPLITTERDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0b2d3fc00433be9cd3011f2f2b24d515b8cbd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518269"
---
# <a name="rbn_splitterdrag-notification-code"></a><span data-ttu-id="7728a-105">RBN- \_ splitterdrag-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="7728a-105">RBN\_SPLITTERDRAG notification code</span></span>

<span data-ttu-id="7728a-106">Wird von einem Grund leisten-Steuerelement gesendet, wenn der Benutzer einen Splitter zieht.</span><span class="sxs-lookup"><span data-stu-id="7728a-106">Sent by a rebar control when the user drags a splitter.</span></span> <span data-ttu-id="7728a-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="7728a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_SPLITTERDRAG

    lpnmrbspltr = (LPNMREBARSPLITTER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7728a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7728a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7728a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7728a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7728a-110">Zeiger auf eine [**nmrebarsplitter**](/windows/win32/api/commctrl/ns-commctrl-nmrebarsplitter) -Struktur, die Informationen über den Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="7728a-110">Pointer to an [**NMREBARSPLITTER**](/windows/win32/api/commctrl/ns-commctrl-nmrebarsplitter) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7728a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7728a-111">Return value</span></span>

<span data-ttu-id="7728a-112">Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="7728a-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="7728a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7728a-113">Requirements</span></span>



| <span data-ttu-id="7728a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7728a-114">Requirement</span></span> | <span data-ttu-id="7728a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7728a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7728a-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7728a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7728a-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7728a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7728a-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7728a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7728a-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7728a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7728a-120">Header</span><span class="sxs-lookup"><span data-stu-id="7728a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7728a-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="7728a-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





