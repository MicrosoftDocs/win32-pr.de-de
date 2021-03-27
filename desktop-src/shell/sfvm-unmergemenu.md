---
description: 'Benachrichtigt das Rückruf Objekt, dass ein Menü entfernt wird. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
title: SFVM_UNMERGEMENU Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0255a41d-e8b4-48d2-931a-aa76ad83c18c
api_name:
- SFVM_UNMERGEMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6c83df7ca42d66f320339901a176dc9d4d38ff37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980816"
---
# <a name="sfvm_unmergemenu-message"></a><span data-ttu-id="57940-104">Sfvm \_ unmergemenu-Meldung</span><span class="sxs-lookup"><span data-stu-id="57940-104">SFVM\_UNMERGEMENU message</span></span>

<span data-ttu-id="57940-105">Benachrichtigt das Rückruf Objekt, dass ein Menü entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="57940-105">Notifies the callback object that a menu is being removed.</span></span> <span data-ttu-id="57940-106">Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.</span><span class="sxs-lookup"><span data-stu-id="57940-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_UNMERGEMENU 

    lParam = (LPARAM)(HMENU) hmenuCurrent;

            
```



## <a name="parameters"></a><span data-ttu-id="57940-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="57940-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57940-108">*hmenucurrent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57940-108">*hmenuCurrent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57940-109">Das Handle des Menüs, das entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="57940-109">The handle of the menu that is being removed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="57940-110">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="57940-110">Requirements</span></span>



| <span data-ttu-id="57940-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57940-111">Requirement</span></span> | <span data-ttu-id="57940-112">Wert</span><span class="sxs-lookup"><span data-stu-id="57940-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="57940-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="57940-113">Minimum supported client</span></span><br/> | <span data-ttu-id="57940-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57940-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="57940-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="57940-115">Minimum supported server</span></span><br/> | <span data-ttu-id="57940-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57940-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="57940-117">Header</span><span class="sxs-lookup"><span data-stu-id="57940-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="57940-118"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="57940-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
