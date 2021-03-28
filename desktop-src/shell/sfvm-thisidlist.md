---
description: Die sfvm- \_ thisidlist kann geändert werden oder ist nicht verfügbar.
ms.assetid: 488f696d-aa71-4727-bbd2-c99e7d245d85
title: SFVM_THISIDLIST Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86e24199e5adbb895c8d1d5fc36bfff0c109bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760195"
---
# <a name="sfvm_thisidlist-message"></a><span data-ttu-id="00af0-103">Sfvm- \_ thisidlist-Meldung</span><span class="sxs-lookup"><span data-stu-id="00af0-103">SFVM\_THISIDLIST message</span></span>

<span data-ttu-id="00af0-104">\[**Sfvm \_ Thisidlist** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="00af0-104">\[**SFVM\_THISIDLIST** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="00af0-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="00af0-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="00af0-106">Ermöglicht dem Rückruf Objekt, den Zeiger der Ansicht auf eine Element Bezeichner-Liste (PIDL) anzugeben.</span><span class="sxs-lookup"><span data-stu-id="00af0-106">Allows the callback object to specify the view's pointer to an item identifier list (PIDL).</span></span> <span data-ttu-id="00af0-107">Dies wird nur verwendet, wenn " [**ipersistidlist:: abtidlist**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistidlist-setidlist) " und " [**IPersistFolder2:: getcurrfolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder2-getcurfolder) " fehlgeschlagen sind.</span><span class="sxs-lookup"><span data-stu-id="00af0-107">This is used only when [**IPersistIDList::SetIDList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistidlist-setidlist) and [**IPersistFolder2::GetCurFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder2-getcurfolder) have failed.</span></span> <span data-ttu-id="00af0-108">Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.</span><span class="sxs-lookup"><span data-stu-id="00af0-108">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_THISIDLIST
    lParam = (LPARAM)(LPITEMIDLIST*) pidl;
            
```



## <a name="parameters"></a><span data-ttu-id="00af0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="00af0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00af0-110">*PIDL* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="00af0-110">*pidl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00af0-111">Die Adresse der PIDL der Ansicht.</span><span class="sxs-lookup"><span data-stu-id="00af0-111">The address of the view's PIDL.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="00af0-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="00af0-112">Requirements</span></span>



| <span data-ttu-id="00af0-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00af0-113">Requirement</span></span> | <span data-ttu-id="00af0-114">Wert</span><span class="sxs-lookup"><span data-stu-id="00af0-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="00af0-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="00af0-115">Minimum supported client</span></span><br/> | <span data-ttu-id="00af0-116">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00af0-116">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="00af0-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="00af0-117">Minimum supported server</span></span><br/> | <span data-ttu-id="00af0-118">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00af0-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="00af0-119">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="00af0-119">End of client support</span></span><br/>    | <span data-ttu-id="00af0-120">Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="00af0-120">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="00af0-121">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="00af0-121">End of server support</span></span><br/>    | <span data-ttu-id="00af0-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="00af0-122">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="00af0-123">Header</span><span class="sxs-lookup"><span data-stu-id="00af0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="00af0-124"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="00af0-124"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
