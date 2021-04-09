---
title: TBN_ENDDRAG Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster der Symbolleiste, dass der Benutzer das Ziehen einer Schaltfläche auf einer Symbolleiste beendet hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 846ba42e-6e0d-45bb-88ce-7b4d2cb17e13
keywords:
- Windows-Steuerelemente für TBN_ENDDRAG Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd493ac338e11716ea381e83102b200334a1eec4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105032"
---
# <a name="tbn_enddrag-notification-code"></a><span data-ttu-id="6cbe5-105">TBN- \_ EndDrag-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="6cbe5-105">TBN\_ENDDRAG notification code</span></span>

<span data-ttu-id="6cbe5-106">Benachrichtigt das übergeordnete Fenster der Symbolleiste, dass der Benutzer das Ziehen einer Schaltfläche auf einer Symbolleiste beendet hat.</span><span class="sxs-lookup"><span data-stu-id="6cbe5-106">Notifies the toolbar's parent window that the user has stopped dragging a button in a toolbar.</span></span> <span data-ttu-id="6cbe5-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="6cbe5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_ENDDRAG 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="6cbe5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6cbe5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cbe5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6cbe5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6cbe5-110">Zeiger auf eine [**nmtoolbar**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="6cbe5-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="6cbe5-111">Der **iItem** -Member enthält den Befehls Bezeichner der gezogenen Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="6cbe5-111">The **iItem** member contains the command identifier of the button being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cbe5-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6cbe5-112">Return value</span></span>

<span data-ttu-id="6cbe5-113">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="6cbe5-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cbe5-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6cbe5-114">Requirements</span></span>



| <span data-ttu-id="6cbe5-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6cbe5-115">Requirement</span></span> | <span data-ttu-id="6cbe5-116">Wert</span><span class="sxs-lookup"><span data-stu-id="6cbe5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6cbe5-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6cbe5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6cbe5-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6cbe5-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6cbe5-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6cbe5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6cbe5-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6cbe5-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6cbe5-121">Header</span><span class="sxs-lookup"><span data-stu-id="6cbe5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cbe5-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cbe5-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





