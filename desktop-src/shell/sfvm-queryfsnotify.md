---
description: Sfvm \_ queryfsnotify kann geändert oder nicht verfügbar sein.
ms.assetid: 5d777115-bae3-47c4-9edc-c99c40a4f926
title: SFVM_QUERYFSNOTIFY Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4416bda249e3ec0f2a0c0f2d45ac353961e180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218586"
---
# <a name="sfvm_queryfsnotify-message"></a><span data-ttu-id="11f91-103">Sfvm \_ queryfsnotify-Meldung</span><span class="sxs-lookup"><span data-stu-id="11f91-103">SFVM\_QUERYFSNOTIFY message</span></span>

<span data-ttu-id="11f91-104">\[**Sfvm \_ Queryfsnotify** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="11f91-104">\[**SFVM\_QUERYFSNOTIFY** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="11f91-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="11f91-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="11f91-106">Ermöglicht dem Rückruf Objekt das Registrieren eines Ordners, damit Änderungen an der Ansicht dieses Ordners Benachrichtigungen generieren.</span><span class="sxs-lookup"><span data-stu-id="11f91-106">Allows the callback object to register a folder so that changes to that folder's view will generate notifications.</span></span> <span data-ttu-id="11f91-107">Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.</span><span class="sxs-lookup"><span data-stu-id="11f91-107">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_QUERYFSNOTIFY 
    lParam = (LPARAM)(SHChangeNotifyEntry*) shcne;
            
```



## <a name="parameters"></a><span data-ttu-id="11f91-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="11f91-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11f91-109">*shcne* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="11f91-109">*shcne* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="11f91-110">Eine-Struktur, die die PIDL des Elements enthält, das auf Ereignisse überwacht werden soll, und ein Hinweis darauf, ob die Unterordner dieses Elements ebenfalls überwacht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="11f91-110">A structure to hold the PIDL of the item to watch for events and an indication whether subfolders of that item should also be watched.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11f91-111">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="11f91-111">Requirements</span></span>



| <span data-ttu-id="11f91-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11f91-112">Requirement</span></span> | <span data-ttu-id="11f91-113">Wert</span><span class="sxs-lookup"><span data-stu-id="11f91-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="11f91-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11f91-114">Minimum supported client</span></span><br/> | <span data-ttu-id="11f91-115">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11f91-115">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="11f91-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11f91-116">Minimum supported server</span></span><br/> | <span data-ttu-id="11f91-117">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11f91-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="11f91-118">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="11f91-118">End of client support</span></span><br/>    | <span data-ttu-id="11f91-119">Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="11f91-119">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="11f91-120">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="11f91-120">End of server support</span></span><br/>    | <span data-ttu-id="11f91-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="11f91-121">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="11f91-122">Header</span><span class="sxs-lookup"><span data-stu-id="11f91-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="11f91-123"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="11f91-123"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
