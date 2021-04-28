---
description: 'NtGdiDdCreateSurface-Funktion: Fügt eine Oberfläche an eine andere Oberfläche an.'
ms.assetid: 4fd757c7-9e32-4737-b666-3226f6cf29fa
title: NtGdiDdCreateSurface-Funktion (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: bf8e13cff80ddea4e102c045c174565e7e835274
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085778"
---
# <a name="ntgdiddcreatesurface-function"></a><span data-ttu-id="315cb-103">NtGdiDdCreateSurface-Funktion</span><span class="sxs-lookup"><span data-stu-id="315cb-103">NtGdiDdCreateSurface function</span></span>

<span data-ttu-id="315cb-104">\[Diese Funktion kann bei jeder Betriebssystemrevision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="315cb-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="315cb-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs. diese APIs isolieren Anwendungen vor solchen Betriebssystemänderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeigetreibern.\]</span><span class="sxs-lookup"><span data-stu-id="315cb-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="315cb-106">Fügt eine Oberfläche an eine andere Oberfläche an.</span><span class="sxs-lookup"><span data-stu-id="315cb-106">Attaches a surface to another surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="315cb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="315cb-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCreateSurface(
  _In_    HANDLE               hDirectDraw,
  _In_    HANDLE               *hSurface,
  _Inout_ DDSURFACEDESC        *puSurfaceDescription,
  _Inout_ DD_SURFACE_GLOBAL    *puSurfaceGlobalData,
  _Inout_ DD_SURFACE_LOCAL     *puSurfaceLocalData,
  _Inout_ DD_SURFACE_MORE      *puSurfaceMoreData,
  _Inout_ DD_CREATESURFACEDATA *puCreateSurfaceData,
  _Out_   HANDLE               *puhSurface
);
```



## <a name="parameters"></a><span data-ttu-id="315cb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="315cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="315cb-109">*hDirectDraw* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="315cb-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="315cb-110">Handle für die [**DD \_ DIRECTDRAW \_ GLOBAL-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) die den Treiber darstellt.</span><span class="sxs-lookup"><span data-stu-id="315cb-110">Handle to the [**DD\_DIRECTDRAW\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) structure representing the driver.</span></span>

</dd> <dt>

<span data-ttu-id="315cb-111">*hSurface* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="315cb-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="315cb-112">Vorheriges Handle für dieselbe Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="315cb-112">Previous handle to the same surface.</span></span> <span data-ttu-id="315cb-113">Wird verwendet, wenn die Oberfläche nach einem Moduswechsel neu erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="315cb-113">Used if the surface is being re-created after a mode switch.</span></span>

</dd> <dt>

<span data-ttu-id="315cb-114">*puSurfaceDescription* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="315cb-114">*puSurfaceDescription* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="315cb-115">Zeiger auf die [**DDSURFACEDESC-Struktur,**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) die die Oberfläche oder den Puffer beschreibt, die der Treiber erstellen soll.</span><span class="sxs-lookup"><span data-stu-id="315cb-115">Pointer to the [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) structure describing the surface or buffer that the driver should create.</span></span>

</dd> <dt>

<span data-ttu-id="315cb-116">*puSurfaceGlobalData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="315cb-116">*puSurfaceGlobalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="315cb-117">Zeiger auf die [**GLOBALE DD \_ \_ SURFACE-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) die Oberflächendaten enthält, die global mit mehreren Oberflächen gemeinsam genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="315cb-117">Pointer to the [**DD\_SURFACE\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) structure containing surface data that is shared globally with multiple surfaces.</span></span>

</dd> <dt>

<span data-ttu-id="315cb-118">*puSurfaceLocalData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="315cb-118">*puSurfaceLocalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="315cb-119">Zeiger auf eine Liste von [**DD \_ SURFACE \_ LOCAL-Strukturen,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) die die vom Treiber erstellten Oberflächenobjekte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="315cb-119">Pointer to a list of [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structures describing the surface objects created by the driver.</span></span>

</dd> <dt>

<span data-ttu-id="315cb-120">*puSurfaceMoreData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="315cb-120">*puSurfaceMoreData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="315cb-121">Zeiger auf eine [**DD \_ SURFACE \_ MORE-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) die zusätzliche lokale Oberflächendaten enthält.</span><span class="sxs-lookup"><span data-stu-id="315cb-121">Pointer to a [**DD\_SURFACE\_MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) structure that contains additional local surface data.</span></span>

</dd> <dt>

<span data-ttu-id="315cb-122">*puCreateSurfaceData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="315cb-122">*puCreateSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="315cb-123">Zeiger auf eine [**DD \_ CREATESURFACEDATA-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) die die zum Erstellen einer Oberfläche erforderlichen Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="315cb-123">Pointer to a [**DD\_CREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) structure that contains the information required to create a surface.</span></span>

</dd> <dt>

<span data-ttu-id="315cb-124">*puhSurface* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="315cb-124">*puhSurface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="315cb-125">Wird von der DirectDraw-API verwendet und darf nicht vom Treiber ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="315cb-125">Is used by the DirectDraw  API and should not be filled in by the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="315cb-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="315cb-126">Return value</span></span>

<span data-ttu-id="315cb-127">**NtGdiDdCreateSurface** gibt einen der folgenden Rückrufcodes zurück.</span><span class="sxs-lookup"><span data-stu-id="315cb-127">**NtGdiDdCreateSurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="315cb-128">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="315cb-128">Return code</span></span>                                                                                              | <span data-ttu-id="315cb-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="315cb-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="315cb-130"><dt>**BEHANDELTER \_ DDHAL-TREIBER \_**</dt></span><span class="sxs-lookup"><span data-stu-id="315cb-130"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="315cb-131">Der Treiber hat den Vorgang ausgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="315cb-131">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="315cb-132">Wenn dieser Code DD \_ OK lautet, wird DirectDraw oder Direct3D mit der -Funktion fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="315cb-132">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="315cb-133">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="315cb-133">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="315cb-134"><dt>**\_DDHAL-TREIBER \_ NICHT BEHANDELT**</dt></span><span class="sxs-lookup"><span data-stu-id="315cb-134"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="315cb-135">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="315cb-135">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="315cb-136">Wenn der Treiber einen bestimmten Rückruf implementiert haben muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="315cb-136">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="315cb-137">Andernfalls verarbeitet DirectDraw oder Direct3D den Vorgang so, als ob der Treiberrückruf nicht durch Ausführen der geräteunabhängigen DirectDraw- oder Direct3D-Implementierung definiert worden wäre.</span><span class="sxs-lookup"><span data-stu-id="315cb-137">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="315cb-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="315cb-138">Remarks</span></span>

<span data-ttu-id="315cb-139">Es wird empfohlen, dass Ihre Anwendung [IDirectDraw7::CreateSurface](/windows/win32/api/ddraw/nf-ddraw-idirectdraw7-createsurface) aufruft, anstatt diese Funktion zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="315cb-139">It is recommended that your application call [IDirectDraw7::CreateSurface](/windows/win32/api/ddraw/nf-ddraw-idirectdraw7-createsurface) instead of using this function.</span></span>

<span data-ttu-id="315cb-140">Beim Erstellen einer Kette von angefügten Oberflächen, z. B. einer Verkettung oder Kette oder Mipmaps, sollte [**ntGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) zuerst für jede Oberfläche aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="315cb-140">When creating a chain of attached surfaces, such as a swap chain or chain or mipmaps, [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) should be called for each surface first.</span></span> <span data-ttu-id="315cb-141">Rufen Sie dann [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) auf, um sie anzufügen.</span><span class="sxs-lookup"><span data-stu-id="315cb-141">Then call [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) to attach them.</span></span> <span data-ttu-id="315cb-142">Rufen Sie schließlich **NtGdiDdCreateSurface** nur für die erste Oberfläche in der Kette auf.</span><span class="sxs-lookup"><span data-stu-id="315cb-142">Finally, call **NtGdiDdCreateSurface** for the first surface in the chain only.</span></span> <span data-ttu-id="315cb-143">In diesem Fall ist *hSurface* das Handle, das von **NtGdiDdCreateSurfaceObject** für die erste Oberfläche in der Kette zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="315cb-143">In this case, *hSurface* would be the handle returned by **NtGdiDdCreateSurfaceObject** for the first surface in the chain.</span></span>

<span data-ttu-id="315cb-144">**NtGdiDdCreateSurface** sollte nur aufgerufen werden, um Oberflächen im lokalen und nicht lokalen Videospeicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="315cb-144">**NtGdiDdCreateSurface** should only be called to create surfaces in local and non-local video memory.</span></span> <span data-ttu-id="315cb-145">Es sollte nie aufgerufen werden, um Systemspeicheroberflächen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="315cb-145">It should never be called to create system memory surfaces.</span></span> <span data-ttu-id="315cb-146">Verwenden Sie stattdessen [**NtGdiDdCreateSurfaceObject,**](-dxgkernel-ntgdiddcreatesurfaceobject.md) um Systemspeicheroberflächen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="315cb-146">To create system memory surfaces, use [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="315cb-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="315cb-147">Requirements</span></span>



| <span data-ttu-id="315cb-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="315cb-148">Requirement</span></span> | <span data-ttu-id="315cb-149">Wert</span><span class="sxs-lookup"><span data-stu-id="315cb-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="315cb-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="315cb-150">Minimum supported client</span></span><br/> | <span data-ttu-id="315cb-151">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="315cb-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="315cb-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="315cb-152">Minimum supported server</span></span><br/> | <span data-ttu-id="315cb-153">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="315cb-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="315cb-154">Header</span><span class="sxs-lookup"><span data-stu-id="315cb-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="315cb-155"><dt>Ntgdi.h</dt></span><span class="sxs-lookup"><span data-stu-id="315cb-155"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="315cb-156">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="315cb-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="315cb-157">Clientunterstützung auf niedriger Grafikebene</span><span class="sxs-lookup"><span data-stu-id="315cb-157">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
