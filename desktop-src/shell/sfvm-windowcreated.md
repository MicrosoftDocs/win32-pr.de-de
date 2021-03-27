---
description: 'Benachrichtigt das Rückruf Objekt, dass das Fenster der Ordneransicht erstellt wird. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
title: SFVM_WINDOWCREATED Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b57eb1d8-a897-4358-a855-89e152035eff
api_name:
- SFVM_WINDOWCREATED
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9d545feadecdaadbf776f94e653df8b71150ac05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980865"
---
# <a name="sfvm_windowcreated-message"></a><span data-ttu-id="abc84-104">Sfvm- \_ WindowCreated-Nachricht</span><span class="sxs-lookup"><span data-stu-id="abc84-104">SFVM\_WINDOWCREATED message</span></span>

<span data-ttu-id="abc84-105">Benachrichtigt das Rückruf Objekt, dass das Fenster der Ordneransicht erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="abc84-105">Notifies the callback object that the folder view window is being created.</span></span> <span data-ttu-id="abc84-106">Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.</span><span class="sxs-lookup"><span data-stu-id="abc84-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_WINDOWCREATED 

    wParam = (WPARAM)(HWND) hwndView;

            
```



## <a name="parameters"></a><span data-ttu-id="abc84-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="abc84-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abc84-108">*hwndview* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="abc84-108">*hwndView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abc84-109">Das Fenster Handle der Ordneransicht.</span><span class="sxs-lookup"><span data-stu-id="abc84-109">The folder view's window handle.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="abc84-110">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="abc84-110">Requirements</span></span>



| <span data-ttu-id="abc84-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="abc84-111">Requirement</span></span> | <span data-ttu-id="abc84-112">Wert</span><span class="sxs-lookup"><span data-stu-id="abc84-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="abc84-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="abc84-113">Minimum supported client</span></span><br/> | <span data-ttu-id="abc84-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abc84-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="abc84-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="abc84-115">Minimum supported server</span></span><br/> | <span data-ttu-id="abc84-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abc84-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="abc84-117">Header</span><span class="sxs-lookup"><span data-stu-id="abc84-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="abc84-118"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="abc84-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
