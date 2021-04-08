---
title: SBM_GETSCROLLBARINFO Meldung (Winuser. h)
description: Wird von einer Anwendung gesendet, um Informationen über die angegebene Scrollleiste abzurufen.
ms.assetid: db6f704f-99ee-448c-ae7a-dd5a23399fb6
keywords:
- Windows-Steuerelemente für SBM_GETSCROLLBARINFO Meldung
topic_type:
- apiref
api_name:
- SBM_GETSCROLLBARINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8bdd78eb665bd069d854538bb2bdfae1a946765
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741376"
---
# <a name="sbm_getscrollbarinfo-message"></a><span data-ttu-id="c8deb-104">SBM \_ getscrollbarinfo-Meldung</span><span class="sxs-lookup"><span data-stu-id="c8deb-104">SBM\_GETSCROLLBARINFO message</span></span>

<span data-ttu-id="c8deb-105">Wird von einer Anwendung gesendet, um Informationen über die angegebene Scrollleiste abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c8deb-105">Sent by an application to retrieve information about the specified scroll bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="c8deb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8deb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8deb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c8deb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8deb-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="c8deb-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c8deb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8deb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8deb-110">Zeiger auf eine [**scrollbarinfo**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) -Struktur, die die Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="c8deb-110">Pointer to a [**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) structure that receives the information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8deb-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c8deb-111">Return value</span></span>

<span data-ttu-id="c8deb-112">Gibt einen Wert ungleich 0 (null) zurück, wenn erfolgreich, andernfalls</span><span class="sxs-lookup"><span data-stu-id="c8deb-112">Returns nonzero if successful or zero otherwise.</span></span>

<span data-ttu-id="c8deb-113">Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.</span><span class="sxs-lookup"><span data-stu-id="c8deb-113">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="c8deb-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8deb-114">Requirements</span></span>



| <span data-ttu-id="c8deb-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8deb-115">Requirement</span></span> | <span data-ttu-id="c8deb-116">Wert</span><span class="sxs-lookup"><span data-stu-id="c8deb-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8deb-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c8deb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c8deb-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8deb-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c8deb-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c8deb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c8deb-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8deb-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c8deb-121">Header</span><span class="sxs-lookup"><span data-stu-id="c8deb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8deb-122"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="c8deb-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8deb-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8deb-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="c8deb-124">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="c8deb-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c8deb-125">**GetScrollBarInfo**</span><span class="sxs-lookup"><span data-stu-id="c8deb-125">**GetScrollBarInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollbarinfo)
</dt> <dt>

[<span data-ttu-id="c8deb-126">**Scrollbarinfo**</span><span class="sxs-lookup"><span data-stu-id="c8deb-126">**SCROLLBARINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-scrollbarinfo)
</dt> </dl>

 

