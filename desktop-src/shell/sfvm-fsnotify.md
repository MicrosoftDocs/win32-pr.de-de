---
description: 'Benachrichtigt das Rückruf Objekt, dass ein Ereignis aufgetreten ist, das sich auf eines seiner Elemente auswirkt. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
title: SFVM_FSNOTIFY Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: ff159c35-afdf-4147-8dd6-7febd9519b18
api_name:
- SFVM_FSNOTIFY
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 74c17f9d4b8c8c1979fa7da2d6f0ff63dff74a9b
ms.sourcegitcommit: cd9672511263d04c0e4bc41758dd1d9e89ea92b4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2021
ms.locfileid: "104995222"
---
# <a name="sfvm_fsnotify-message"></a><span data-ttu-id="a2fb2-104">Sfvm \_ fsnotify-Nachricht</span><span class="sxs-lookup"><span data-stu-id="a2fb2-104">SFVM\_FSNOTIFY message</span></span>

<span data-ttu-id="a2fb2-105">Benachrichtigt das Rückruf Objekt, dass ein Ereignis aufgetreten ist, das sich auf eines seiner Elemente auswirkt.</span><span class="sxs-lookup"><span data-stu-id="a2fb2-105">Notifies the callback object that an event has taken place that affects one of its items.</span></span> <span data-ttu-id="a2fb2-106">Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.</span><span class="sxs-lookup"><span data-stu-id="a2fb2-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_FSNOTIFY 

    wParam = (WPARAM)(LPCITEMIDLIST*) ppidl;

    lParam = (LPARAM)(DWORD) lEvent;

            
```



## <a name="parameters"></a><span data-ttu-id="a2fb2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2fb2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2fb2-108">*ppidl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2fb2-108">*ppidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2fb2-109">Der Zeiger der PIDL des betroffenen Elements.</span><span class="sxs-lookup"><span data-stu-id="a2fb2-109">The pointer of PIDL of the affected item.</span></span>

</dd> <dt>

<span data-ttu-id="a2fb2-110">*Levent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2fb2-110">*lEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2fb2-111">Ein shcne-Wert, der angibt, welches Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="a2fb2-111">A SHCNE value that indicates which event occurred.</span></span> <span data-ttu-id="a2fb2-112">Eine Liste möglicher Werte finden Sie unter [**shchangenotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify).</span><span class="sxs-lookup"><span data-stu-id="a2fb2-112">For a list of possible values, see [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a2fb2-113">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a2fb2-113">Requirements</span></span>



| <span data-ttu-id="a2fb2-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2fb2-114">Requirement</span></span> | <span data-ttu-id="a2fb2-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a2fb2-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a2fb2-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2fb2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a2fb2-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2fb2-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a2fb2-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2fb2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a2fb2-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2fb2-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a2fb2-120">Header</span><span class="sxs-lookup"><span data-stu-id="a2fb2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2fb2-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2fb2-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
