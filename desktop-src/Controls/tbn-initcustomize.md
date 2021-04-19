---
title: TBN_INITCUSTOMIZE Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass die Anpassung gestartet wurde. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: f4b9a1b0-94f7-4b2b-81b3-772da09134d2
keywords:
- Windows-Steuerelemente für TBN_INITCUSTOMIZE Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_INITCUSTOMIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d5e855374699a100bf78019f1ca3d89857bc7c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338319"
---
# <a name="tbn_initcustomize-notification-code"></a><span data-ttu-id="9c875-105">TBN \_ initcustomize-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="9c875-105">TBN\_INITCUSTOMIZE notification code</span></span>

<span data-ttu-id="9c875-106">Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass die Anpassung gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="9c875-106">Notifies a toolbar's parent window that customizing has started.</span></span> <span data-ttu-id="9c875-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="9c875-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_INITCUSTOMIZE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="9c875-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c875-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c875-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c875-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c875-110">Zeiger auf die [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur der Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="9c875-110">Pointer to the toolbar's [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c875-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9c875-111">Return value</span></span>

<span data-ttu-id="9c875-112">Gibt tbnrf \_ hidehelp zurück, um die Schaltfläche Hilfe zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="9c875-112">Returns TBNRF\_HIDEHELP to suppress the Help button.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c875-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c875-113">Requirements</span></span>



| <span data-ttu-id="9c875-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9c875-114">Requirement</span></span> | <span data-ttu-id="9c875-115">Wert</span><span class="sxs-lookup"><span data-stu-id="9c875-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9c875-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9c875-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9c875-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c875-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9c875-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9c875-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9c875-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c875-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9c875-120">Header</span><span class="sxs-lookup"><span data-stu-id="9c875-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c875-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c875-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





