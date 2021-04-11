---
title: Benachrichtigungs Code für NM_RDBLCLK (Strukturansicht) (kommctrl. h)
description: Benachrichtigt das übergeordnete Element eines Strukturansicht-Steuer Elements, dass der Benutzer die Rechte Maustaste im Steuerelement doppelt geklickt hat. Diese Benachrichtigung wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: eb1ae167-32cb-45d6-92e6-7bf5f7e46c2a
keywords:
- NM_RDBLCLK (Strukturansicht) Windows-Steuerelemente für Benachrichtigungs Code
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ef5b4f1dbaf1031c995028028cc0b44e544f5f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105284"
---
# <a name="nm_rdblclk-tree-view-notification-code"></a><span data-ttu-id="c02ef-105">NM \_ rdblclk (Strukturansicht) Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="c02ef-105">NM\_RDBLCLK (tree view) notification code</span></span>

<span data-ttu-id="c02ef-106">Benachrichtigt das übergeordnete Element eines Strukturansicht-Steuer Elements, dass der Benutzer die Rechte Maustaste im Steuerelement doppelt geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="c02ef-106">Notifies the parent of a tree-view control that the user has double-clicked the right mouse button within the control.</span></span> <span data-ttu-id="c02ef-107">Diese Benachrichtigung wird in Form einer WM-Benachrichtigungs Meldung gesendet. [**\_**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="c02ef-107">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RDBLCLK

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="c02ef-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c02ef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c02ef-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c02ef-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c02ef-110">Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="c02ef-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c02ef-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c02ef-111">Return value</span></span>

<span data-ttu-id="c02ef-112">Gibt einen Wert ungleich 0 (null) zurück, um die Standard Verarbeitung zu verhindern, oder NULL, um die Standard Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="c02ef-112">Return nonzero to prevent the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="c02ef-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c02ef-113">Requirements</span></span>



| <span data-ttu-id="c02ef-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c02ef-114">Requirement</span></span> | <span data-ttu-id="c02ef-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c02ef-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c02ef-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c02ef-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c02ef-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c02ef-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c02ef-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c02ef-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c02ef-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c02ef-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c02ef-120">Header</span><span class="sxs-lookup"><span data-stu-id="c02ef-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c02ef-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c02ef-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





