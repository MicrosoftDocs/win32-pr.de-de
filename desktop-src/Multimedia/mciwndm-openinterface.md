---
title: MCIWNDM_OPENINTERFACE Meldung (VFW. h)
description: Die mciwndm- \_ openinterface-Nachricht fügt den Datenstrom oder die Datei, die der angegebenen Schnittstelle zugeordnet ist, einem mciwnd-Fenster an. Sie können diese Nachricht explizit oder mithilfe des mciwndopeninterface-Makros senden.
ms.assetid: 73cbd637-d315-4b39-a978-2b72aed1f303
keywords:
- MCIWNDM_OPENINTERFACE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_OPENINTERFACE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c40453f4d587429508a5aae19bc432fc46088ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391507"
---
# <a name="mciwndm_openinterface-message"></a><span data-ttu-id="bc2dc-105">Mciwndm- \_ openinterface-Meldung</span><span class="sxs-lookup"><span data-stu-id="bc2dc-105">MCIWNDM\_OPENINTERFACE message</span></span>

<span data-ttu-id="bc2dc-106">Die **mciwndm- \_ openinterface** -Nachricht fügt den Datenstrom oder die Datei, die der angegebenen Schnittstelle zugeordnet ist, einem mciwnd-Fenster an.</span><span class="sxs-lookup"><span data-stu-id="bc2dc-106">The **MCIWNDM\_OPENINTERFACE** message attaches the data stream or file associated with the specified interface to an MCIWnd window.</span></span> <span data-ttu-id="bc2dc-107">Sie können diese Nachricht explizit oder mithilfe des [**mciwndopeninterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="bc2dc-107">You can send this message explicitly or by using the [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) macro.</span></span>


```C++
MCIWNDM_OPENINTERFACE 
wParam = 0; 
lParam = (LPARAM) (LPUNKNOWN) pUnk; 
```



## <a name="parameters"></a><span data-ttu-id="bc2dc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc2dc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc2dc-109"><span id="pUnk"></span><span id="punk"></span><span id="PUNK"></span>*Kro*</span><span class="sxs-lookup"><span data-stu-id="bc2dc-109"><span id="pUnk"></span><span id="punk"></span><span id="PUNK"></span>*pUnk*</span></span>
</dt> <dd>

<span data-ttu-id="bc2dc-110">Zeiger auf eine IAVI-Schnittstelle, die auf eine Datei oder einen Datenstrom in einer Datei zeigt.</span><span class="sxs-lookup"><span data-stu-id="bc2dc-110">Pointer to an IAVI interface that points to a file or a data stream in a file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc2dc-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc2dc-111">Return Value</span></span>

<span data-ttu-id="bc2dc-112">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="bc2dc-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc2dc-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc2dc-113">Requirements</span></span>



| <span data-ttu-id="bc2dc-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc2dc-114">Requirement</span></span> | <span data-ttu-id="bc2dc-115">Wert</span><span class="sxs-lookup"><span data-stu-id="bc2dc-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bc2dc-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc2dc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bc2dc-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc2dc-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="bc2dc-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc2dc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bc2dc-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc2dc-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bc2dc-120">Header</span><span class="sxs-lookup"><span data-stu-id="bc2dc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc2dc-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc2dc-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc2dc-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc2dc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc2dc-123">**Mciwndopeninterface**</span><span class="sxs-lookup"><span data-stu-id="bc2dc-123">**MCIWndOpenInterface**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface)
</dt> </dl>

 

 





