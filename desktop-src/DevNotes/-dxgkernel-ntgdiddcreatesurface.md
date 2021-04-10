---
description: Fügt eine Oberfläche an eine andere Oberfläche an.
ms.assetid: 4fd757c7-9e32-4737-b666-3226f6cf29fa
title: Ntgdiddkreatesurface-Funktion (ntgdi. h)
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
ms.openlocfilehash: 663d29be32dc544d44a47061e1a6ff7f81e60862
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125947"
---
# <a name="ntgdiddcreatesurface-function"></a><span data-ttu-id="7cfeb-103">Ntgdiddkreatesurface-Funktion</span><span class="sxs-lookup"><span data-stu-id="7cfeb-103">NtGdiDdCreateSurface function</span></span>

<span data-ttu-id="7cfeb-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="7cfeb-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="7cfeb-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="7cfeb-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="7cfeb-106">Fügt eine Oberfläche an eine andere Oberfläche an.</span><span class="sxs-lookup"><span data-stu-id="7cfeb-106">Attaches a surface to another surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cfeb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7cfeb-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="7cfeb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7cfeb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cfeb-109">*hdirectdraw* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7cfeb-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cfeb-110">Handle zur [**globalen DD \_ DirectDraw \_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) -Struktur, die den Treiber darstellt.</span><span class="sxs-lookup"><span data-stu-id="7cfeb-110">Handle to the [**DD\_DIRECTDRAW\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) structure representing the driver.</span></span>

</dd> <dt>

<span data-ttu-id="7cfeb-111">*hsurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7cfeb-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cfeb-112">Vorheriges Handle für dieselbe Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="7cfeb-112">Previous handle to the same surface.</span></span> <span data-ttu-id="7cfeb-113">Wird verwendet, wenn die Oberfläche nach einem Modusschalter neu erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7cfeb-113">Used if the surface is being re-created after a mode switch.</span></span>

</dd> <dt>

<span data-ttu-id="7cfeb-114">*pusurfacedescription* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7cfeb-114">*puSurfaceDescription* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cfeb-115">Ein Zeiger auf die [**ddsurfacedebug**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) -Struktur, die die vom Treiber zu erstellende Oberfläche oder den Puffer beschreibt.</span><span class="sxs-lookup"><span data-stu-id="7cfeb-115">Pointer to the [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) structure describing the surface or buffer that the driver should create.</span></span>

</dd> <dt>

<span data-ttu-id="7cfeb-116">*pusurfakeglobaldata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7cfeb-116">*puSurfaceGlobalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cfeb-117">Ein Zeiger auf [**die \_ \_ globale DD-Oberflächen**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) Struktur, die Oberflächendaten enthält, die Global mit mehreren Oberflächen gemeinsam genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="7cfeb-117">Pointer to the [**DD\_SURFACE\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) structure containing surface data that is shared globally with multiple surfaces.</span></span>

</dd> <dt>

<span data-ttu-id="7cfeb-118">*pusurfakelocaldata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7cfeb-118">*puSurfaceLocalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cfeb-119">Zeiger auf eine Liste von [**\_ \_ lokalen**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) TT-Oberflächenstrukturen, die die vom Treiber erstellten Oberflächen Objekte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="7cfeb-119">Pointer to a list of [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structures describing the surface objects created by the driver.</span></span>

</dd> <dt>

<span data-ttu-id="7cfeb-120">*pusurfakemoredata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7cfeb-120">*puSurfaceMoreData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cfeb-121">Zeiger auf eine [**DD- \_ Oberfläche \_ mehr**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) Struktur, die zusätzliche lokale Oberflächendaten enthält.</span><span class="sxs-lookup"><span data-stu-id="7cfeb-121">Pointer to a [**DD\_SURFACE\_MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) structure that contains additional local surface data.</span></span>

</dd> <dt>

<span data-ttu-id="7cfeb-122">*pukreatesurfacedata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7cfeb-122">*puCreateSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cfeb-123">Zeiger auf eine DD-Struktur von " [**\_ foatesurfacedata**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) ", die die zum Erstellen einer Oberfläche erforderlichen Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="7cfeb-123">Pointer to a [**DD\_CREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) structure that contains the information required to create a surface.</span></span>

</dd> <dt>

<span data-ttu-id="7cfeb-124">*puhsurface* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7cfeb-124">*puhSurface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cfeb-125">Wird von der DirectDraw-API verwendet und sollte nicht vom Treiber ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="7cfeb-125">Is used by the DirectDraw  API and should not be filled in by the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cfeb-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7cfeb-126">Return value</span></span>

<span data-ttu-id="7cfeb-127">**Ntgdiddkreatesurface** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="7cfeb-127">**NtGdiDdCreateSurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="7cfeb-128">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7cfeb-128">Return code</span></span>                                                                                              | <span data-ttu-id="7cfeb-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7cfeb-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7cfeb-130"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="7cfeb-130"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="7cfeb-131">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7cfeb-131">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="7cfeb-132">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="7cfeb-132">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="7cfeb-133">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="7cfeb-133">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="7cfeb-134"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="7cfeb-134"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="7cfeb-135">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="7cfeb-135">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="7cfeb-136">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="7cfeb-136">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="7cfeb-137">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7cfeb-137">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7cfeb-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7cfeb-138">Remarks</span></span>

<span data-ttu-id="7cfeb-139">Es wird empfohlen, dass Ihre Anwendung [IDirectDraw7:: | atesurface](/windows/win32/api/ddraw/nf-ddraw-idirectdraw7-createsurface) aufruft, anstatt diese Funktion zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7cfeb-139">It is recommended that your application call [IDirectDraw7::CreateSurface](/windows/win32/api/ddraw/nf-ddraw-idirectdraw7-createsurface) instead of using this function.</span></span>

<span data-ttu-id="7cfeb-140">Beim Erstellen einer Kette angefügter Oberflächen, z. b. einer Swapkette oder einer Kette oder von Mipmaps, sollte [**ntgdiddkreatesurfaceobject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) zuerst für jede Oberfläche aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7cfeb-140">When creating a chain of attached surfaces, such as a swap chain or chain or mipmaps, [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) should be called for each surface first.</span></span> <span data-ttu-id="7cfeb-141">Anschließend wird [**ntgdiddattachsurface**](-dxgkernel-ntgdiddattachsurface.md) aufgerufen, um sie anzufügen.</span><span class="sxs-lookup"><span data-stu-id="7cfeb-141">Then call [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) to attach them.</span></span> <span data-ttu-id="7cfeb-142">Nennen Sie schließlich **ntgdiddkreatesurface** nur für die erste Oberfläche in der Kette.</span><span class="sxs-lookup"><span data-stu-id="7cfeb-142">Finally, call **NtGdiDdCreateSurface** for the first surface in the chain only.</span></span> <span data-ttu-id="7cfeb-143">In diesem Fall wäre *hsurface* das Handle, das von **ntgdiddkreatesurfaceobject** für die erste Oberfläche in der Kette zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7cfeb-143">In this case, *hSurface* would be the handle returned by **NtGdiDdCreateSurfaceObject** for the first surface in the chain.</span></span>

<span data-ttu-id="7cfeb-144">**Ntgdiddkreatesurface** sollte nur aufgerufen werden, um Oberflächen in lokalem und nicht lokalem Videospeicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7cfeb-144">**NtGdiDdCreateSurface** should only be called to create surfaces in local and non-local video memory.</span></span> <span data-ttu-id="7cfeb-145">Es sollte nie aufgerufen werden, um Systemspeicher Oberflächen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7cfeb-145">It should never be called to create system memory surfaces.</span></span> <span data-ttu-id="7cfeb-146">Verwenden Sie stattdessen [**ntgdiddkreatesurfaceobject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) , um Systemspeicher Oberflächen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7cfeb-146">To create system memory surfaces, use [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cfeb-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7cfeb-147">Requirements</span></span>



| <span data-ttu-id="7cfeb-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7cfeb-148">Requirement</span></span> | <span data-ttu-id="7cfeb-149">Wert</span><span class="sxs-lookup"><span data-stu-id="7cfeb-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7cfeb-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7cfeb-150">Minimum supported client</span></span><br/> | <span data-ttu-id="7cfeb-151">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7cfeb-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="7cfeb-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7cfeb-152">Minimum supported server</span></span><br/> | <span data-ttu-id="7cfeb-153">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7cfeb-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7cfeb-154">Header</span><span class="sxs-lookup"><span data-stu-id="7cfeb-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cfeb-155"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cfeb-155"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cfeb-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7cfeb-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cfeb-157">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="7cfeb-157">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
