---
title: TBN_TOOLBARCHANGE Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster der Symbolleiste, dass der Benutzer eine Symbolleiste angepasst hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 6c5127e6-391f-4592-8547-4cc3d3ed6cf0
keywords:
- Windows-Steuerelemente für TBN_TOOLBARCHANGE Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_TOOLBARCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af9c533a7a26dd1ed0f1938e6c5138bbae13c31f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956872"
---
# <a name="tbn_toolbarchange-notification-code"></a><span data-ttu-id="54601-105">TBN- \_ toolbarchange-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="54601-105">TBN\_TOOLBARCHANGE notification code</span></span>

<span data-ttu-id="54601-106">Benachrichtigt das übergeordnete Fenster der Symbolleiste, dass der Benutzer eine Symbolleiste angepasst hat.</span><span class="sxs-lookup"><span data-stu-id="54601-106">Notifies the toolbar's parent window that the user has customized a toolbar.</span></span> <span data-ttu-id="54601-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="54601-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_TOOLBARCHANGE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="54601-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="54601-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54601-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54601-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54601-110">Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die Informationen über den Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="54601-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54601-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54601-111">Return value</span></span>

<span data-ttu-id="54601-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="54601-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="54601-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54601-113">Requirements</span></span>



| <span data-ttu-id="54601-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54601-114">Requirement</span></span> | <span data-ttu-id="54601-115">Wert</span><span class="sxs-lookup"><span data-stu-id="54601-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54601-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54601-116">Minimum supported client</span></span><br/> | <span data-ttu-id="54601-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54601-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="54601-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54601-118">Minimum supported server</span></span><br/> | <span data-ttu-id="54601-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54601-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="54601-120">Header</span><span class="sxs-lookup"><span data-stu-id="54601-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="54601-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="54601-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





