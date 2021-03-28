---
description: 'Ermöglicht dem Rückruf Objekt das Angeben eines standardmäßigen Sortier Parameters. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
title: SFVM_GETSORTDEFAULTS Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: edd428f2-50d9-4819-ba77-df51262e33ff
api_name:
- SFVM_GETSORTDEFAULTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: db6477cc9660f8084e2bf8298e028ed7a445f26c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980881"
---
# <a name="sfvm_getsortdefaults-message"></a><span data-ttu-id="a640c-104">Sfvm \_ getsortdefaults-Meldung</span><span class="sxs-lookup"><span data-stu-id="a640c-104">SFVM\_GETSORTDEFAULTS message</span></span>

<span data-ttu-id="a640c-105">Ermöglicht dem Rückruf Objekt das Angeben eines standardmäßigen Sortier Parameters.</span><span class="sxs-lookup"><span data-stu-id="a640c-105">Allows the callback object to specify a default sorting parameter.</span></span> <span data-ttu-id="a640c-106">Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.</span><span class="sxs-lookup"><span data-stu-id="a640c-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETSORTDEFAULTS 

    wParam = (WPARAM)(int*) iDirection;

    lParam = (LPARAM)(int*) iColumn;

            
```



## <a name="parameters"></a><span data-ttu-id="a640c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a640c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a640c-108">*idirection* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a640c-108">*iDirection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a640c-109">Die Standard Sortierrichtung.</span><span class="sxs-lookup"><span data-stu-id="a640c-109">The default sorting direction.</span></span> <span data-ttu-id="a640c-110">Legen Sie diesen Parameter auf einen positiven Wert fest, um in aufsteigender Reihenfolge zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="a640c-110">Set this parameter to a positive value to sort in ascending order.</span></span> <span data-ttu-id="a640c-111">Legen Sie diesen Parameter auf NULL oder einen negativen Wert fest, um in absteigender Reihenfolge sortiert zu werden.</span><span class="sxs-lookup"><span data-stu-id="a640c-111">Set this parameter to zero or a negative value to sort in descending order.</span></span>

</dd> <dt>

<span data-ttu-id="a640c-112">*icolumn* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a640c-112">*iColumn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a640c-113">Die Spalte, die für die Sortierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a640c-113">The column used for the sort.</span></span> <span data-ttu-id="a640c-114">Diese wird an die [**IShellFolder:: compareids**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) in den unteren 16 Bits des *LPARAM* -Werts übermittelt.</span><span class="sxs-lookup"><span data-stu-id="a640c-114">This will be passed to the [**IShellFolder::CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) in the lower 16 bits of its *lParam* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a640c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a640c-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a640c-116">: **Sfvm \_ getsortdefaults** wird vom Systemordner View-Objekt nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="a640c-116">: **SFVM\_GETSORTDEFAULTS** is not recognized by the system folder view object.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a640c-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a640c-117">Requirements</span></span>



| <span data-ttu-id="a640c-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a640c-118">Requirement</span></span> | <span data-ttu-id="a640c-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a640c-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a640c-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a640c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a640c-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a640c-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a640c-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a640c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a640c-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a640c-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a640c-124">Header</span><span class="sxs-lookup"><span data-stu-id="a640c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a640c-125"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="a640c-125"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
