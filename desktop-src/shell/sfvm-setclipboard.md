---
description: Benachrichtigt ishellview, wenn eines der Objekte als Ergebnis eines Menübefehls in der Zwischenablage platziert wird. Wird von der shshellfolderview- \_ Nachricht verwendet.
title: SFVM_SETCLIPBOARD Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6a4cf0c5-2349-4e1e-b6c5-ee9b5430456e
api_name:
- SFVM_SETCLIPBOARD
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c9c30848de77ef7de101eaa9d724f2f26f9d384c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995158"
---
# <a name="sfvm_setclipboard-message"></a><span data-ttu-id="12c00-104">Sfvm- \_ setClipboard-Nachricht</span><span class="sxs-lookup"><span data-stu-id="12c00-104">SFVM\_SETCLIPBOARD message</span></span>

<span data-ttu-id="12c00-105">Benachrichtigt [**ishellview**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) , wenn eines der Objekte als Ergebnis eines Menübefehls in der Zwischenablage platziert wird.</span><span class="sxs-lookup"><span data-stu-id="12c00-105">Notifies the [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) when one of its objects is placed on the Clipboard as a result of a menu command.</span></span> <span data-ttu-id="12c00-106">Wird von der [**shshellfolderview- \_ Nachricht**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)verwendet.</span><span class="sxs-lookup"><span data-stu-id="12c00-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_SETCLIPBOARD 

    lParam = (DWORD) dwEffect;

            
```



## <a name="parameters"></a><span data-ttu-id="12c00-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="12c00-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12c00-108">*dweffect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12c00-108">*dwEffect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12c00-109">Verwenden Sie (wParam)-2, wenn das Element in die Zwischenablage ausgeschnitten wird, oder (wParam)-3, wenn das Element in die Zwischenablage kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="12c00-109">Use (WPARAM)-2 if the item is being cut to the Clipboard or (WPARAM)-3 if the item is being copied to the Clipboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12c00-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="12c00-110">Return value</span></span>

<span data-ttu-id="12c00-111">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="12c00-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="12c00-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="12c00-112">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="12c00-113">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="12c00-113">Requirements</span></span>



| <span data-ttu-id="12c00-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12c00-114">Requirement</span></span> | <span data-ttu-id="12c00-115">Wert</span><span class="sxs-lookup"><span data-stu-id="12c00-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="12c00-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="12c00-116">Minimum supported client</span></span><br/> | <span data-ttu-id="12c00-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12c00-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="12c00-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="12c00-118">Minimum supported server</span></span><br/> | <span data-ttu-id="12c00-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12c00-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="12c00-120">Header</span><span class="sxs-lookup"><span data-stu-id="12c00-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="12c00-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="12c00-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




