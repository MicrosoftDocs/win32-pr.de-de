---
description: 'Ermöglicht dem Rückruf Objekt, den Ansichtsmodus anzugeben. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
title: SFVM_DEFVIEWMODE Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5118fc81-490f-4d76-9361-0d6af0c4b4c0
api_name:
- SFVM_DEFVIEWMODE
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8d57bb61b2b938947d0290345215e3735d9d8763
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995110"
---
# <a name="sfvm_defviewmode-message"></a><span data-ttu-id="afc6e-104">Sfvm \_ defviewmode-Meldung</span><span class="sxs-lookup"><span data-stu-id="afc6e-104">SFVM\_DEFVIEWMODE message</span></span>

<span data-ttu-id="afc6e-105">Ermöglicht dem Rückruf Objekt, den Ansichtsmodus anzugeben.</span><span class="sxs-lookup"><span data-stu-id="afc6e-105">Allows the callback object to specify the view mode.</span></span> <span data-ttu-id="afc6e-106">Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.</span><span class="sxs-lookup"><span data-stu-id="afc6e-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_DEFVIEWMODE 

    lParam = (LPARAM)(FOLDERVIEWMODE*) pViewMode;

            
```



## <a name="parameters"></a><span data-ttu-id="afc6e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="afc6e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afc6e-108">*pviewmode* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="afc6e-108">*pViewMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="afc6e-109">Einer der Werte aus dem [**folderviewmode**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode) -Enumerationstyp.</span><span class="sxs-lookup"><span data-stu-id="afc6e-109">One of the values from the [**FOLDERVIEWMODE**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode) enumerated type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="afc6e-110">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="afc6e-110">Requirements</span></span>



| <span data-ttu-id="afc6e-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="afc6e-111">Requirement</span></span> | <span data-ttu-id="afc6e-112">Wert</span><span class="sxs-lookup"><span data-stu-id="afc6e-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="afc6e-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="afc6e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="afc6e-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="afc6e-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="afc6e-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="afc6e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="afc6e-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="afc6e-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="afc6e-117">Header</span><span class="sxs-lookup"><span data-stu-id="afc6e-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="afc6e-118"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="afc6e-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
