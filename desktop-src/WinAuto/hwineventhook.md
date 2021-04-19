---
title: Hwineventhook (WINDEF. h)
description: Wird verwendet, um eine Windows Event Hook-Funktion zu deklarieren.
ms.assetid: fa193e8e-46a8-46d4-83e1-e6274276b218
keywords:
- Hwineventhook
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf526846916dfdd701f4f5ee98778dbbe9e66d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341610"
---
# <a name="hwineventhook"></a><span data-ttu-id="d8eff-104">Hwineventhook</span><span class="sxs-lookup"><span data-stu-id="d8eff-104">HWINEVENTHOOK</span></span>

<span data-ttu-id="d8eff-105">Wird verwendet, um eine Windows Event Hook-Funktion zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="d8eff-105">Used to declare a window event hook function.</span></span>


```C++
typedef HANDLE HWINEVENTHOOK;
```



## <a name="remarks"></a><span data-ttu-id="d8eff-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d8eff-106">Remarks</span></span>

<span data-ttu-id="d8eff-107">Dieser Datentyp wird mit der [*wineventproc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) -Rückruffunktion und den Funktionen [**setwineventhook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) und [**unhookwinevent**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) verwendet.</span><span class="sxs-lookup"><span data-stu-id="d8eff-107">This data type is used with the [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) callback function and the [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) and [**UnhookWinEvent**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8eff-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8eff-108">Requirements</span></span>



| <span data-ttu-id="d8eff-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8eff-109">Requirement</span></span> | <span data-ttu-id="d8eff-110">Wert</span><span class="sxs-lookup"><span data-stu-id="d8eff-110">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8eff-111">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d8eff-111">Minimum supported client</span></span><br/> | <span data-ttu-id="d8eff-112">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d8eff-112">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="d8eff-113">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d8eff-113">Minimum supported server</span></span><br/> | <span data-ttu-id="d8eff-114">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d8eff-114">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                          |
| <span data-ttu-id="d8eff-115">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="d8eff-115">Redistributable</span></span><br/>          | <span data-ttu-id="d8eff-116">Active Accessibility 1,3 RDK unter Windows NT 4,0 mit SP6 und höher und Windows 95</span><span class="sxs-lookup"><span data-stu-id="d8eff-116">Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95</span></span><br/>                                   |
| <span data-ttu-id="d8eff-117">Header</span><span class="sxs-lookup"><span data-stu-id="d8eff-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8eff-118"><dt>WINDEF. h (winver >= 0x0500) (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8eff-118"><dt>Windef.h (WINVER >= 0x0500) (include Windows.h)</dt></span></span> </dl> |



 

 





