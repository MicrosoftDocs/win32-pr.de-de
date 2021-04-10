---
description: Erstellt ein Surface-Objekt im Kernelmodus, das das Benutzermodus-Surface-Objekt darstellt, auf das von pusurfacelocal verwiesen wird.
ms.assetid: 1b2886a8-279b-4bec-9fb8-b88a68ded25b
title: Ntgdiddkreatesurfaceobject-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurfaceObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 5aef9a70897f5a8a46f9c966242d8842c54f9946
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041351"
---
# <a name="ntgdiddcreatesurfaceobject-function"></a><span data-ttu-id="52d61-103">Ntgdiddkreatesurfaceobject-Funktion</span><span class="sxs-lookup"><span data-stu-id="52d61-103">NtGdiDdCreateSurfaceObject function</span></span>

<span data-ttu-id="52d61-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="52d61-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="52d61-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="52d61-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="52d61-106">Erstellt ein Surface-Objekt im Kernelmodus, das das Benutzermodus-Surface-Objekt darstellt, auf das von *pusurfacelocal* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="52d61-106">Creates a kernel-mode surface object that represents the user-mode surface object referenced by *puSurfaceLocal*.</span></span>

## <a name="syntax"></a><span data-ttu-id="52d61-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="52d61-107">Syntax</span></span>


```C++
HANDLE APIENTRY NtGdiDdCreateSurfaceObject(
  _In_ HANDLE             hDirectDrawLocal,
  _In_ HANDLE             hSurface,
  _In_ PDD_SURFACE_LOCAL  puSurfaceLocal,
  _In_ PDD_SURFACE_MORE   puSurfaceMore,
  _In_ PDD_SURFACE_GLOBAL puSurfaceGlobal,
  _In_ BOOL               bComplete
);
```



## <a name="parameters"></a><span data-ttu-id="52d61-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="52d61-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52d61-109">*hdirectdrawlocal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52d61-109">*hDirectDrawLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52d61-110">Handle für den kernelmodusdirectdraw-Objekt.</span><span class="sxs-lookup"><span data-stu-id="52d61-110">Handle to the kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="52d61-111">*hsurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52d61-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52d61-112">Vorheriges Handle für dieselbe Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="52d61-112">Previous handle to the same surface.</span></span> <span data-ttu-id="52d61-113">Wird verwendet, wenn die Oberfläche nach einem Modusschalter neu erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="52d61-113">Used if the surface is being re-created after a mode switch.</span></span>

</dd> <dt>

<span data-ttu-id="52d61-114">*pusurfakelocal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52d61-114">*puSurfaceLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52d61-115">Ein Zeiger auf [**die \_ \_ lokale DD-Oberflächen**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) Struktur, die das DirectDraw-Benutzermodus-Surface-Objekt darstellt, dem der zugeordnete Arbeitsspeicher zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="52d61-115">Pointer to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the DirectDraw user-mode surface object with which to associate the allocated memory.</span></span> <span data-ttu-id="52d61-116">Weitere Informationen finden Sie in der DDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="52d61-116">See the DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="52d61-117">*pusurfakemore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52d61-117">*puSurfaceMore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52d61-118">Zeiger auf die [**DD- \_ Oberfläche \_ mehr**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) Struktur, die zusätzliche lokale Daten für jedes einzelne Surface-Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="52d61-118">Pointer to the [**DD\_SURFACE\_MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) structure that contains additional local data for each individual surface object.</span></span> <span data-ttu-id="52d61-119">Weitere Informationen finden Sie in der DDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="52d61-119">See the DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="52d61-120">*pusurfakeglobal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52d61-120">*puSurfaceGlobal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52d61-121">Zeiger zur [**\_ \_ globalen**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) TT-Oberflächenstruktur, die Oberflächendaten enthält, die Global mit mehreren Oberflächen gemeinsam genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="52d61-121">Pointer to the [**DD\_SURFACE\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) structure that contains surface data shared globally with multiple surfaces.</span></span> <span data-ttu-id="52d61-122">Weitere Informationen finden Sie in der DDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="52d61-122">See the DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="52d61-123">*bcomplete* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52d61-123">*bComplete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52d61-124">Kernel Modus-objektvervollständigungs Kennzeichen.</span><span class="sxs-lookup"><span data-stu-id="52d61-124">Kernel-mode object completion flag.</span></span> <span data-ttu-id="52d61-125">Kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="52d61-125">Can be one of the following values.</span></span>

<dt>



 <span data-ttu-id="52d61-126">Fall</span><span class="sxs-lookup"><span data-stu-id="52d61-126">(TRUE)</span></span>


</dt> <dd>

<span data-ttu-id="52d61-127">Vervollständigen Sie die gesamte Verarbeitung in Bezug auf die Kernel Modus-Darstellung.</span><span class="sxs-lookup"><span data-stu-id="52d61-127">Complete all processing concerning the kernel-mode representation.</span></span>

</dd> <dt>



 <span data-ttu-id="52d61-128">Alarm</span><span class="sxs-lookup"><span data-stu-id="52d61-128">(FALSE)</span></span>


</dt> <dd>

<span data-ttu-id="52d61-129">Erstellen Sie das-Objekt, aber richten Sie keine internen Daten ein, z. b. den Speicher Zeiger.</span><span class="sxs-lookup"><span data-stu-id="52d61-129">Create the object, but do not set up internal data such as the memory pointer.</span></span> <span data-ttu-id="52d61-130">Mit **false** erstellte Objekte können mithilfe von [**ntgdiddattachsurface**](-dxgkernel-ntgdiddattachsurface.md) angefügt und durch einen-Befehl von [**ntgdiddkreatesurface**](-dxgkernel-ntgdiddcreatesurface.md)abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="52d61-130">Objects created using **FALSE** can be attached using [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) and are completed by a call to [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md).</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52d61-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="52d61-131">Return value</span></span>

<span data-ttu-id="52d61-132">Bei erfolgreicher Ausführung gibt diese Funktion ein Handle für die Darstellung des kernelmodusausdrucks zurück. Andernfalls wird **null** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="52d61-132">If successful, this function returns a handle to the kernel-mode surface representation; otherwise it returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="52d61-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52d61-133">Remarks</span></span>

<span data-ttu-id="52d61-134">Anwendungen wird empfohlen, die DirectDraw-und [Direct3D](../direct3d10/d3d10-graphics-reference.md) -APIs zu verwenden, um Grafikgeräte Objekte zu erstellen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="52d61-134">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="52d61-135">Diese Konstrukte abstrahieren den Geräte Erstellungs Prozess auf vereinfachte und betriebssystemunabhängige Weise.</span><span class="sxs-lookup"><span data-stu-id="52d61-135">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="52d61-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52d61-136">Requirements</span></span>



| <span data-ttu-id="52d61-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52d61-137">Requirement</span></span> | <span data-ttu-id="52d61-138">Wert</span><span class="sxs-lookup"><span data-stu-id="52d61-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="52d61-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="52d61-139">Minimum supported client</span></span><br/> | <span data-ttu-id="52d61-140">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52d61-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="52d61-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="52d61-141">Minimum supported server</span></span><br/> | <span data-ttu-id="52d61-142">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52d61-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="52d61-143">Header</span><span class="sxs-lookup"><span data-stu-id="52d61-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="52d61-144"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="52d61-144"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52d61-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52d61-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52d61-146">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="52d61-146">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="52d61-147">**Ddkreatesurfaceobject**</span><span class="sxs-lookup"><span data-stu-id="52d61-147">**DdCreateSurfaceObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatesurfaceobject)
</dt> <dt>

[<span data-ttu-id="52d61-148">**Ntgdidddelta etesurfaceobject**</span><span class="sxs-lookup"><span data-stu-id="52d61-148">**NtGdiDdDeleteSurfaceObject**</span></span>](-dxgkernel-ntgdidddeletesurfaceobject.md)
</dt> <dt>

[<span data-ttu-id="52d61-149">**Ntgdiddattachsurface**</span><span class="sxs-lookup"><span data-stu-id="52d61-149">**NtGdiDdAttachSurface**</span></span>](-dxgkernel-ntgdiddattachsurface.md)
</dt> <dt>

[<span data-ttu-id="52d61-150">**Ntgdiddkreatesurface**</span><span class="sxs-lookup"><span data-stu-id="52d61-150">**NtGdiDdCreateSurface**</span></span>](-dxgkernel-ntgdiddcreatesurface.md)
</dt> </dl>

 

 
