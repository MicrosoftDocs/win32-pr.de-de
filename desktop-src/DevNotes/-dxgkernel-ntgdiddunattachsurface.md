---
description: Entfernt eine Anlage, die mit ntgdiddattachsurface erstellt wurde, zwischen zwei Kernel Modus-Oberflächen Objekten.
ms.assetid: 28037b42-a00c-4063-93ee-5d71761a95d8
title: Ntgdiddunattachsurface-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdUnattachSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 4513020a40c9b704e0b84e1a8b1c582be95db78f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958186"
---
# <a name="ntgdiddunattachsurface-function"></a><span data-ttu-id="d2afe-103">Ntgdiddunattachsurface-Funktion</span><span class="sxs-lookup"><span data-stu-id="d2afe-103">NtGdiDdUnattachSurface function</span></span>

<span data-ttu-id="d2afe-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d2afe-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="d2afe-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="d2afe-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="d2afe-106">Entfernt eine Anlage, die mit [**ntgdiddattachsurface**](-dxgkernel-ntgdiddattachsurface.md)erstellt wurde, zwischen zwei Kernel Modus-Oberflächen Objekten.</span><span class="sxs-lookup"><span data-stu-id="d2afe-106">Removes an attachment, created with [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md), between two kernel-mode surface objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2afe-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2afe-107">Syntax</span></span>


```C++
VOID APIENTRY NtGdiDdUnattachSurface(
  _In_ HANDLE hSurface,
  _In_ HANDLE hSurfaceAttached
);
```



## <a name="parameters"></a><span data-ttu-id="d2afe-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2afe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2afe-109">*hsurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2afe-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2afe-110">Das kernelmodusobjekt, das als hsurfacefrom-Parameter an [**ntgdiddattachsurface**](-dxgkernel-ntgdiddattachsurface.md)übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="d2afe-110">The kernel-mode surface object that was passed as the hSurfaceFrom parameter to [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2afe-111">*hsurfaceattached* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2afe-111">*hSurfaceAttached* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2afe-112">Das für den hsurfaceto-Parameter an [ **ntgdiddattachsurface** übergebenen kernelmodusobjekt.](-dxgkernel-ntgdiddattachsurface.md)</span><span class="sxs-lookup"><span data-stu-id="d2afe-112">The kernel-mode surface object that was passed as the hSurfaceTo parameter to [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2afe-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d2afe-113">Return value</span></span>

<span data-ttu-id="d2afe-114">**Ntgdiddunattachsurface** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="d2afe-114">**NtGdiDdUnattachSurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="d2afe-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d2afe-115">Return code</span></span>                                                                                              | <span data-ttu-id="d2afe-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2afe-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d2afe-117"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="d2afe-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="d2afe-118">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d2afe-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="d2afe-119">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="d2afe-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="d2afe-120">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="d2afe-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="d2afe-121"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="d2afe-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="d2afe-122">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d2afe-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="d2afe-123">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="d2afe-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="d2afe-124">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d2afe-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d2afe-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2afe-125">Remarks</span></span>

<span data-ttu-id="d2afe-126">Es wird empfohlen, dass Anwendungen die DirectDraw-API verwenden, die oberflächenanlagen auf höherer Ebene verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d2afe-126">It is recommended that applications use the DirectDraw  API, which handles surface attachments in a higher-level manner.</span></span>

<span data-ttu-id="d2afe-127">Es ist nicht erforderlich, diese Funktion aufzurufen, da der Kernel alle Anlagen automatisch zerstört, wenn [**ntgdidddestroysurface**](-dxgkernel-ntgdidddestroysurface.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d2afe-127">It is not necessary to call this function because the kernel will automatically destroy all attachments when [**NtGdiDdDestroySurface**](-dxgkernel-ntgdidddestroysurface.md) is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2afe-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2afe-128">Requirements</span></span>



| <span data-ttu-id="d2afe-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2afe-129">Requirement</span></span> | <span data-ttu-id="d2afe-130">Wert</span><span class="sxs-lookup"><span data-stu-id="d2afe-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d2afe-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d2afe-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d2afe-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2afe-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="d2afe-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d2afe-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d2afe-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2afe-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d2afe-135">Header</span><span class="sxs-lookup"><span data-stu-id="d2afe-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2afe-136"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2afe-136"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2afe-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2afe-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2afe-138">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="d2afe-138">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




