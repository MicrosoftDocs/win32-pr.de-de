---
description: 'Ermöglicht dem Rückruf Objekt, die Anzahl der Elemente in der Ordneransicht anzugeben. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
title: SFVM_DEFITEMCOUNT Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 62306eaa-e52e-432b-9233-d990519d5739
api_name:
- SFVM_DEFITEMCOUNT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4e3f746e422428ab9f925cf4ff3f460ccd578367
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959995"
---
# <a name="sfvm_defitemcount-message"></a><span data-ttu-id="ede2d-104">Sfvm- \_ defitemcount-Nachricht</span><span class="sxs-lookup"><span data-stu-id="ede2d-104">SFVM\_DEFITEMCOUNT message</span></span>

<span data-ttu-id="ede2d-105">Ermöglicht dem Rückruf Objekt, die Anzahl der Elemente in der Ordneransicht anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ede2d-105">Allows the callback object to specify the number of items in the folder view.</span></span> <span data-ttu-id="ede2d-106">Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.</span><span class="sxs-lookup"><span data-stu-id="ede2d-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_DEFITEMCOUNT 

    lParam = (LPARAM)(UINT*) cItems;

            
```



## <a name="parameters"></a><span data-ttu-id="ede2d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ede2d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ede2d-108">*cItems* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ede2d-108">*cItems* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ede2d-109">Die Anzahl der Elemente in der Ordneransicht.</span><span class="sxs-lookup"><span data-stu-id="ede2d-109">The number of items in the folder view.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ede2d-110">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ede2d-110">Requirements</span></span>



| <span data-ttu-id="ede2d-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ede2d-111">Requirement</span></span> | <span data-ttu-id="ede2d-112">Wert</span><span class="sxs-lookup"><span data-stu-id="ede2d-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ede2d-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ede2d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="ede2d-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ede2d-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ede2d-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ede2d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="ede2d-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ede2d-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ede2d-117">Header</span><span class="sxs-lookup"><span data-stu-id="ede2d-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="ede2d-118"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="ede2d-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
