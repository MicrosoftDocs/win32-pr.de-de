---
title: LVN_ODSTATECHANGED Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Listenansicht-Steuerelement gesendet, wenn sich der Zustand eines Elements oder eines Bereichs von Elementen geändert hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: a3aafda5-a3ec-4f84-8153-8d34097e04f1
keywords:
- Windows-Steuerelemente für LVN_ODSTATECHANGED Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_ODSTATECHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86de2f5e01e15d0a97c49f451914aac5b74b27e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742552"
---
# <a name="lvn_odstatechanged-notification-code"></a><span data-ttu-id="93feb-105">LVN \_ odstatechanged-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="93feb-105">LVN\_ODSTATECHANGED notification code</span></span>

<span data-ttu-id="93feb-106">Wird von einem Listenansicht-Steuerelement gesendet, wenn sich der Zustand eines Elements oder eines Bereichs von Elementen geändert hat.</span><span class="sxs-lookup"><span data-stu-id="93feb-106">Sent by a list-view control when the state of an item or range of items has changed.</span></span> <span data-ttu-id="93feb-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="93feb-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ODSTATECHANGED

    lpStateChange = (LPNMLVODSTATECHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="93feb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="93feb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93feb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="93feb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93feb-110">Ein Zeiger auf eine [**nmlvodstatechange**](/windows/win32/api/commctrl/ns-commctrl-nmlvodstatechange) -Struktur, die Informationen über die geänderten Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="93feb-110">Pointer to an [**NMLVODSTATECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmlvodstatechange) structure that contains information about the item or items that have changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93feb-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="93feb-111">Return value</span></span>

<span data-ttu-id="93feb-112">Die Anwendung, die diesen Benachrichtigungs Code empfängt, muss NULL zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="93feb-112">The application receiving this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="93feb-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93feb-113">Requirements</span></span>



| <span data-ttu-id="93feb-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93feb-114">Requirement</span></span> | <span data-ttu-id="93feb-115">Wert</span><span class="sxs-lookup"><span data-stu-id="93feb-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="93feb-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="93feb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="93feb-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="93feb-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="93feb-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="93feb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="93feb-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="93feb-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="93feb-120">Header</span><span class="sxs-lookup"><span data-stu-id="93feb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="93feb-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="93feb-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





