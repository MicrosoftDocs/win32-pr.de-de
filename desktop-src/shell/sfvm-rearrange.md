---
description: Benachrichtigt die ishellview, ihre Elemente neu anzuordnen. Wird von der shshellfolderview- \_ Nachricht verwendet.
title: SFVM_REARRANGE Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d745bafc-f2f5-40a1-b7e8-e16e4cf0153d
api_name:
- SFVM_REARRANGE
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 524b507ed5af08fbf70b51d9252e7bcb12af1f27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050536"
---
# <a name="sfvm_rearrange-message"></a><span data-ttu-id="c24d2-104">Sfvm- \_ Nachricht neu anordnen</span><span class="sxs-lookup"><span data-stu-id="c24d2-104">SFVM\_REARRANGE message</span></span>

<span data-ttu-id="c24d2-105">Benachrichtigt die [**ishellview**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) , ihre Elemente neu anzuordnen.</span><span class="sxs-lookup"><span data-stu-id="c24d2-105">Notifies the [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) to rearrange its items.</span></span> <span data-ttu-id="c24d2-106">Wird von der [**shshellfolderview- \_ Nachricht**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)verwendet.</span><span class="sxs-lookup"><span data-stu-id="c24d2-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_REARRANGE 

    lParam = (LPARAM) lparam;

            
```



## <a name="parameters"></a><span data-ttu-id="c24d2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c24d2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c24d2-108">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c24d2-108">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c24d2-109">An [**IShellFolder:: compareids**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids)übermittelt.</span><span class="sxs-lookup"><span data-stu-id="c24d2-109">Passed to [**IShellFolder::CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids).</span></span> <span data-ttu-id="c24d2-110">Weitere Informationen zu diesem Parameter finden Sie unter [**IShellFolder:: compareids**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) .</span><span class="sxs-lookup"><span data-stu-id="c24d2-110">See [**IShellFolder::CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) for more information on this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c24d2-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c24d2-111">Return value</span></span>

<span data-ttu-id="c24d2-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="c24d2-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c24d2-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c24d2-113">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c24d2-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c24d2-114">Requirements</span></span>



| <span data-ttu-id="c24d2-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c24d2-115">Requirement</span></span> | <span data-ttu-id="c24d2-116">Wert</span><span class="sxs-lookup"><span data-stu-id="c24d2-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c24d2-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c24d2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c24d2-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c24d2-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c24d2-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c24d2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c24d2-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c24d2-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c24d2-121">Header</span><span class="sxs-lookup"><span data-stu-id="c24d2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c24d2-122"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="c24d2-122"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




