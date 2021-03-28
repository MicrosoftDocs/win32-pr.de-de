---
description: 'Benachrichtigt das Rückruf Objekt der Container Site. Dieser Wert wird nur verwendet, wenn "IObjectWithSite:: SetSite" nicht unterstützt wird und "shkreateshellfolderviewex" verwendet wird. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
ms.assetid: a4aa40f8-1d98-4686-86e2-87280e470aac
title: SFVM_SETISFV Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83021f1d6d52286f08e8ec7bd51bbaa806c17c7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980880"
---
# <a name="sfvm_setisfv-message"></a><span data-ttu-id="2772e-105">Sfvm- \_ Nachricht "abtisfv"</span><span class="sxs-lookup"><span data-stu-id="2772e-105">SFVM\_SETISFV message</span></span>

<span data-ttu-id="2772e-106">\[Diese Benachrichtigung wird durch Windows XP Service Pack 2 (SP2) und Windows Server 2003 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2772e-106">\[This notification is supported through Windows XP Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="2772e-107">Sie wird möglicherweise in nachfolgenden Versionen von Windows nicht unterstützt.\]</span><span class="sxs-lookup"><span data-stu-id="2772e-107">It might be unsupported in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="2772e-108">Benachrichtigt das Rückruf Objekt der Container Site.</span><span class="sxs-lookup"><span data-stu-id="2772e-108">Notifies the callback object of the container site.</span></span> <span data-ttu-id="2772e-109">Dieser Wert wird nur verwendet, wenn " [**IObjectWithSite:: SetSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768221(v=vs.85)) " nicht unterstützt wird und " [**shkreateshellfolderviewex**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex) " verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2772e-109">This is used only when [**IObjectWithSite::SetSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768221(v=vs.85)) is not supported and [**SHCreateShellFolderViewEx**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex) is used.</span></span> <span data-ttu-id="2772e-110">Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.</span><span class="sxs-lookup"><span data-stu-id="2772e-110">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_SETISFV
    lParam = (LPARAM)(IUnknown*) site;
            
```



## <a name="parameters"></a><span data-ttu-id="2772e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2772e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2772e-112">*Website* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2772e-112">*site* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2772e-113">Ein Zeiger auf die [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle der Container Site.</span><span class="sxs-lookup"><span data-stu-id="2772e-113">A pointer to the container site's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2772e-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="2772e-114">Requirements</span></span>



| <span data-ttu-id="2772e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2772e-115">Requirement</span></span> | <span data-ttu-id="2772e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="2772e-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2772e-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2772e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2772e-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2772e-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2772e-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2772e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2772e-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2772e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2772e-121">Header</span><span class="sxs-lookup"><span data-stu-id="2772e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2772e-122"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="2772e-122"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
