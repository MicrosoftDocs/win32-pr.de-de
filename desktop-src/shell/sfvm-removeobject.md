---
description: Entfernt ein Objekt aus der shellansicht. Wird von der shshellfolderview- \_ Nachricht verwendet.
title: SFVM_REMOVEOBJECT Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5b493cea-dfbd-4aee-8126-b118c058bb4c
api_name:
- SFVM_REMOVEOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 99eaf6b1e8ca49403e0003d6cd60a6769778233a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980888"
---
# <a name="sfvm_removeobject-message"></a><span data-ttu-id="9dac4-104">Sfvm- \_ removeobject-Nachricht</span><span class="sxs-lookup"><span data-stu-id="9dac4-104">SFVM\_REMOVEOBJECT message</span></span>

<span data-ttu-id="9dac4-105">Entfernt ein Objekt aus der shellansicht.</span><span class="sxs-lookup"><span data-stu-id="9dac4-105">Removes an object from the shell view.</span></span> <span data-ttu-id="9dac4-106">Wird von der [**shshellfolderview- \_ Nachricht**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)verwendet.</span><span class="sxs-lookup"><span data-stu-id="9dac4-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_REMOVEOBJECT 
    lParam = (LPARAM) pidl;
            
```



## <a name="parameters"></a><span data-ttu-id="9dac4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9dac4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dac4-108">*PIDL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9dac4-108">*pidl* \[in\]</span></span>
</dt> <dd><span data-ttu-id="9dac4-109">PIDL des zu entfernenden-Objekts.</span><span class="sxs-lookup"><span data-stu-id="9dac4-109">PIDL of the object to remove.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dac4-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9dac4-110">Return value</span></span>

<span data-ttu-id="9dac4-111">Gibt den Index des Elements zurück, das entfernt wurde, wenn ein Element gefunden wurde, das mit der angegebenen PIDL übereinstimmt. Andernfalls wird-1 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9dac4-111">Returns the index of the item that was removed if an item matching the specified PIDL was found; otherwise, returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dac4-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9dac4-112">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9dac4-113">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9dac4-113">Requirements</span></span>



| <span data-ttu-id="9dac4-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9dac4-114">Requirement</span></span> | <span data-ttu-id="9dac4-115">Wert</span><span class="sxs-lookup"><span data-stu-id="9dac4-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9dac4-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9dac4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9dac4-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9dac4-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9dac4-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9dac4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9dac4-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9dac4-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9dac4-120">Header</span><span class="sxs-lookup"><span data-stu-id="9dac4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9dac4-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dac4-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




