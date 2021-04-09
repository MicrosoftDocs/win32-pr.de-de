---
description: Wird verwendet, um den Benutzermodus zu aktivieren, um ein gültiges Verständnis des Clippingbereichs für Windows auf dem Desktop zu erhalten. Dieses Clipping kann sich asynchron aus der Sicht der benutzermodusthreads ändern.
ms.assetid: 286f1c06-c27b-42bd-aecc-3a6923e3df29
title: Ntgdiddresetvisrgn-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdResetVisrgn
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: dd83bcfd6c1f3dec31fb80cf78750bfdfef5e7a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860622"
---
# <a name="ntgdiddresetvisrgn-function"></a><span data-ttu-id="774cd-104">Ntgdiddresetvisrgn-Funktion</span><span class="sxs-lookup"><span data-stu-id="774cd-104">NtGdiDdResetVisrgn function</span></span>

<span data-ttu-id="774cd-105">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="774cd-105">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="774cd-106">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="774cd-106">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="774cd-107">Wird verwendet, um den Benutzermodus zu aktivieren, um ein gültiges Verständnis des Clippingbereichs für Windows auf dem Desktop zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="774cd-107">Used to enable the user mode to gain a valid understanding of the clipping region for windows on the desktop.</span></span> <span data-ttu-id="774cd-108">Dieses Clipping kann sich asynchron aus der Sicht der benutzermodusthreads ändern.</span><span class="sxs-lookup"><span data-stu-id="774cd-108">This clipping can change asynchronously from the point of view of user-mode threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="774cd-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="774cd-109">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdResetVisrgn(
  _In_ HANDLE hSurface,
  _In_ HWND   hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="774cd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="774cd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="774cd-111">*hsurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="774cd-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="774cd-112">Zeiger auf das benutzermodusobjekt einer beliebigen Oberfläche, die zu dem DirectDraw-Gerät gehört, für das Clipping zurückgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="774cd-112">Pointer to the user-mode object of any surface belonging to the DirectDraw device for which clipping is to be reset.</span></span> <span data-ttu-id="774cd-113">Weitere Informationen finden Sie in der DDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="774cd-113">For details, see the DDK documentation.</span></span>

</dd> <dt>

<span data-ttu-id="774cd-114">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="774cd-114">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="774cd-115">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="774cd-115">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="774cd-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="774cd-116">Return value</span></span>

<span data-ttu-id="774cd-117">Wenn erfolgreich, gibt diese Funktion **true** zurück. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="774cd-117">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="774cd-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="774cd-118">Remarks</span></span>

<span data-ttu-id="774cd-119">Das Clipping kann sich asynchron von der Sicht der benutzermodusthreads aus ändern.</span><span class="sxs-lookup"><span data-stu-id="774cd-119">Clipping can change asynchronously from the point of view of user-mode threads.</span></span> <span data-ttu-id="774cd-120">Die kernelmodusteile von DirectDraw und Windows Graphics Device Interface (GDI) behalten einen-Wert bei, der immer dann erhöht wird, wenn sich die clippingliste für den gesamten Desktop ändert.</span><span class="sxs-lookup"><span data-stu-id="774cd-120">The kernel-mode parts of DirectDraw and Windows Graphics Device Interface (GDI) maintain a counter that is incremented whenever the clipping list for the entire desktop changes.</span></span> <span data-ttu-id="774cd-121">Durch einen Aufrufen dieser Funktion wird dieser Counter mit jeder vorhandenen primären DirectDraw-Oberfläche auf dem System aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="774cd-121">A call to this function records this counter with every existing DirectDraw primary surface on the system.</span></span>

<span data-ttu-id="774cd-122">Wenn eine dieser primären Oberflächen zu einem späteren Zeitpunkt durch einen [IDirectDrawSurface7:: BLT](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-blt) -oder [IDirectDrawSurface7:: Lock](/previous-versions/ms858221(v=msdn.10)) -Vorgang geändert wird (siehe DDK-Dokumentation), wird der mit der-Oberfläche aufgezeichnete-Wert mit dem globalen-Wert verglichen.</span><span class="sxs-lookup"><span data-stu-id="774cd-122">At any later time when one of these primary surfaces is modified by a [IDirectDrawSurface7::Blt](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-blt) or [IDirectDrawSurface7::Lock](/previous-versions/ms858221(v=msdn.10)) operation (see DDK documentation), then the counter recorded with the surface is compared with the global counter.</span></span> <span data-ttu-id="774cd-123">Wenn diese Werte unterschiedlich sind, wird ein Fehlercode dderr \_ visrgnchanged an den Benutzermoduscode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="774cd-123">If these values are different, an error code DDERR\_VISRGNCHANGED is returned to the user-mode code.</span></span> <span data-ttu-id="774cd-124">Der Benutzermoduscode fragt dann das aktuelle Clipping für den Desktop erneut ab, ruft **ntgdiddresetvisrgn** auf und wiederholt den auf die primäre Oberfläche angewendeten IDirectDrawSurface7:: BLT, wobei das neue Clipping respektiert wird.</span><span class="sxs-lookup"><span data-stu-id="774cd-124">The user-mode code will then re-query the current clipping for the desktop, call **NtGdiDdResetVisrgn**, and re-try the IDirectDrawSurface7::Blt applied to the primary surface, respecting the new clipping.</span></span> <span data-ttu-id="774cd-125">Schließlich ist das Clipping, das durch den Benutzermoduscode entnommen wurde, mit dem aktuellen Clipping im Besitz des Kernel Modus identisch, und IDirectDrawSurface7:: BLT kann fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="774cd-125">Eventually, the clipping that was sampled by the user-mode code will be the same as the current clipping owned by kernel mode, and the IDirectDrawSurface7::Blt will be allowed to continue.</span></span>

<span data-ttu-id="774cd-126">Anwendungen wird empfohlen, die [idirectdrawclipperschnittstelle](/previous-versions/aa919448(v=msdn.10)) oder die [IDirect3DDevice8::P Resent](/previous-versions/ms889707(v=msdn.10)) -Methode zu verwenden, um asynchrone clippingänderungen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="774cd-126">Applications are advised to use the [IDirectDrawClipper](/previous-versions/aa919448(v=msdn.10)) interface or [IDirect3DDevice8::Present](/previous-versions/ms889707(v=msdn.10)) method to handle asynchronous clipping changes.</span></span> <span data-ttu-id="774cd-127">Diese Konstrukte implementieren ein asynchrones Clipping in automatisierter und Betriebssystem unabhängiger Weise.</span><span class="sxs-lookup"><span data-stu-id="774cd-127">These constructs implement asynchronous clipping in an automated and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="774cd-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="774cd-128">Requirements</span></span>



| <span data-ttu-id="774cd-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="774cd-129">Requirement</span></span> | <span data-ttu-id="774cd-130">Wert</span><span class="sxs-lookup"><span data-stu-id="774cd-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="774cd-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="774cd-131">Minimum supported client</span></span><br/> | <span data-ttu-id="774cd-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="774cd-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="774cd-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="774cd-133">Minimum supported server</span></span><br/> | <span data-ttu-id="774cd-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="774cd-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="774cd-135">Header</span><span class="sxs-lookup"><span data-stu-id="774cd-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="774cd-136"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="774cd-136"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="774cd-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="774cd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="774cd-138">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="774cd-138">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="774cd-139">**Ddresetvisrgn**</span><span class="sxs-lookup"><span data-stu-id="774cd-139">**DdResetVisrgn**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddresetvisrgn)
</dt> </dl>

 

 
