---
description: Die iswindowredirectedforprint-Funktion bestimmt, ob das angegebene Fenster zurzeit zum Drucken umgeleitet wird.
ms.assetid: 49FD0D63-0F7F-48C6-81B6-25715294E7B7
title: Iswindowredirectedforprint-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsWindowRedirectedForPrint
api_type:
- DllExport
api_location:
- user32.dll
ms.openlocfilehash: b6648e5638ec6f05a2677ce279b0c3d7b160b49b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362965"
---
# <a name="iswindowredirectedforprint-function"></a><span data-ttu-id="eba8f-103">Iswindowredirectedforprint-Funktion</span><span class="sxs-lookup"><span data-stu-id="eba8f-103">IsWindowRedirectedForPrint function</span></span>

<span data-ttu-id="eba8f-104">Die **iswindowredirectedforprint** -Funktion bestimmt, ob das angegebene Fenster zurzeit zum Drucken umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="eba8f-104">The **IsWindowRedirectedForPrint** function determines whether the specified window is currently redirected for printing.</span></span>

## <a name="syntax"></a><span data-ttu-id="eba8f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eba8f-105">Syntax</span></span>


```C++
BOOL WINAPI IsWindowRedirectedForPrint(
  _In_   HWND hWnd
);
```



## <a name="parameters"></a><span data-ttu-id="eba8f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eba8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eba8f-107">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eba8f-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eba8f-108">Das Handle des Fensters.</span><span class="sxs-lookup"><span data-stu-id="eba8f-108">The handle of the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eba8f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eba8f-109">Return value</span></span>

<span data-ttu-id="eba8f-110">Wenn das Fenster zurzeit zum Drucken umgeleitet wird, gibt die Funktion einen Wert ungleich 0 (null) zurück. Andernfalls wird 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="eba8f-110">If the window is currently redirected for printing, the function returns a nonzero value; otherwise, it returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="eba8f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eba8f-111">Remarks</span></span>

<span data-ttu-id="eba8f-112">Ein Fenster wird zum Drucken umgeleitet, wenn ein Aufrufen von [**PrintWindow**](/windows/desktop/api/Winuser/nf-winuser-printwindow)verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="eba8f-112">A window is redirected for printing when it processes a call to [**PrintWindow**](/windows/desktop/api/Winuser/nf-winuser-printwindow).</span></span> <span data-ttu-id="eba8f-113">In einem Aufrufen von **PrintWindow** rendert ein Fenster seinen Inhalt auf einem Offscreen-Gerätekontext.</span><span class="sxs-lookup"><span data-stu-id="eba8f-113">In a call to **PrintWindow**, a window renders its content to an off-screen device context.</span></span>

<span data-ttu-id="eba8f-114">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="eba8f-114">This function has no associated import library or header file; you must call it by using the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="eba8f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eba8f-115">Requirements</span></span>



| <span data-ttu-id="eba8f-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eba8f-116">Requirement</span></span> | <span data-ttu-id="eba8f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="eba8f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eba8f-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eba8f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="eba8f-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eba8f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eba8f-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eba8f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="eba8f-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eba8f-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eba8f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="eba8f-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eba8f-123"><dt>User32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eba8f-123"><dt>User32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eba8f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eba8f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eba8f-125">**PrintWindow**</span><span class="sxs-lookup"><span data-stu-id="eba8f-125">**PrintWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-printwindow)
</dt> <dt>

[<span data-ttu-id="eba8f-126">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="eba8f-126">**GetProcAddress**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="eba8f-127">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="eba8f-127">**LoadLibrary**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[<span data-ttu-id="eba8f-128">**WM- \_ Druck**</span><span class="sxs-lookup"><span data-stu-id="eba8f-128">**WM\_PRINT**</span></span>](/windows/desktop/gdi/wm-print)
</dt> <dt>

[<span data-ttu-id="eba8f-129">**WM- \_ printclient**</span><span class="sxs-lookup"><span data-stu-id="eba8f-129">**WM\_PRINTCLIENT**</span></span>](/windows/desktop/gdi/wm-printclient)
</dt> </dl>

 

