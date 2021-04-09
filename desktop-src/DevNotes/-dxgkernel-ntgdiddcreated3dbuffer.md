---
description: Wird verwendet, um einen Befehl auf Treiber Ebene oder einen Vertex-Puffer der angegebenen Beschreibung zu erstellen.
ms.assetid: c65403a1-5686-4c7d-80a4-6e49417c11eb
title: NtGdiDdCreateD3DBuffer-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 2d402a70822fba094d22c82b8767ee3298b86374
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958189"
---
# <a name="ntgdiddcreated3dbuffer-function"></a><span data-ttu-id="926f9-103">NtGdiDdCreateD3DBuffer-Funktion</span><span class="sxs-lookup"><span data-stu-id="926f9-103">NtGdiDdCreateD3DBuffer function</span></span>

<span data-ttu-id="926f9-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="926f9-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="926f9-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="926f9-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="926f9-106">Wird verwendet, um einen Befehl auf Treiber Ebene oder einen Vertex-Puffer der angegebenen Beschreibung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="926f9-106">Used to create a driver-level command or vertex buffer of the specified description.</span></span>

## <a name="syntax"></a><span data-ttu-id="926f9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="926f9-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCreateD3DBuffer(
  _In_    HANDLE               hDirectDraw,
  _Inout_ HANDLE               *hSurface,
  _Inout_ DDSURFACEDESC        *puSurfaceDescription,
  _Inout_ DD_SURFACE_GLOBAL    *puSurfaceGlobalData,
  _Inout_ DD_SURFACE_LOCAL     *puSurfaceLocalData,
  _Inout_ DD_SURFACE_MORE      *puSurfaceMoreData,
  _Inout_ DD_CREATESURFACEDATA *puCreateSurfaceData,
  _Inout_ HANDLE               *puhSurface
);
```



## <a name="parameters"></a><span data-ttu-id="926f9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="926f9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="926f9-109">*hdirectdraw* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="926f9-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="926f9-110">Handle zur [**globalen DD \_ DirectDraw \_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) -Struktur, die den Treiber darstellt.</span><span class="sxs-lookup"><span data-stu-id="926f9-110">Handle to the [**DD\_DIRECTDRAW\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) structure representing the driver.</span></span>

</dd> <dt>

<span data-ttu-id="926f9-111">*hsurface* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="926f9-111">*hSurface* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="926f9-112">Zeiger auf ein Array von Oberflächen Handles.</span><span class="sxs-lookup"><span data-stu-id="926f9-112">Pointer to an array of surface handles.</span></span> <span data-ttu-id="926f9-113">Der Aufrufer kann diese Handles auf die vorherigen handle-Werte festlegen, wenn die Oberflächen nach einem Modusschalter neu erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="926f9-113">The caller can set these handles to the previous handle values if the surfaces are being re-created after a mode switch.</span></span> <span data-ttu-id="926f9-114">Dieser Vorgang wird in der DirectDraw-Dokumentation als "Wiederherstellen" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="926f9-114">This process is called "restoring" in the DirectDraw documentation.</span></span>

</dd> <dt>

<span data-ttu-id="926f9-115">*pusurfacedescription* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="926f9-115">*puSurfaceDescription* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="926f9-116">Ein Zeiger auf eine [**ddsurfacedebug**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) -Struktur, die die vom Treiber zu erstellende Oberfläche oder den Puffer beschreibt.</span><span class="sxs-lookup"><span data-stu-id="926f9-116">Pointer to a [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) structure describing the surface or buffer that the driver should create.</span></span>

</dd> <dt>

<span data-ttu-id="926f9-117">*pusurfakeglobaldata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="926f9-117">*puSurfaceGlobalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="926f9-118">Zeiger auf eine [**\_ \_ globale**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) TT-Oberflächenstruktur, die Oberflächendaten enthält, die Global mit mehreren Oberflächen gemeinsam genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="926f9-118">Pointer to a [**DD\_SURFACE\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) structure containing surface data that is shared globally with multiple surfaces.</span></span>

</dd> <dt>

<span data-ttu-id="926f9-119">*pusurfakelocaldata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="926f9-119">*puSurfaceLocalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="926f9-120">Zeiger auf eine Liste von [**\_ \_ lokalen**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) TT-Oberflächenstrukturen, die die vom Treiber erstellten Oberflächen Objekte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="926f9-120">Pointer to a list of [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structures describing the surface objects created by the driver.</span></span> <span data-ttu-id="926f9-121">Es gibt in der Regel nur einen Eintrag in diesem Array.</span><span class="sxs-lookup"><span data-stu-id="926f9-121">There is usually only one entry in this array.</span></span>

</dd> <dt>

<span data-ttu-id="926f9-122">*pusurfakemoredata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="926f9-122">*puSurfaceMoreData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="926f9-123">Zeiger auf eine [**DD- \_ Oberfläche \_ mehr**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) Struktur, die zusätzliche lokale Oberflächendaten enthält.</span><span class="sxs-lookup"><span data-stu-id="926f9-123">Pointer to a [**DD\_SURFACE\_MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) structure that contains additional local surface data.</span></span>

</dd> <dt>

<span data-ttu-id="926f9-124">*pukreatesurfacedata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="926f9-124">*puCreateSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="926f9-125">Ein Zeiger auf eine DD-Struktur von " [**\_ kreatesurfacedata**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) ", die die zum Erstellen des Puffers erforderlichen Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="926f9-125">Pointer to a [**DD\_CREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) structure that contains the information required to create the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="926f9-126">*puhsurface* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="926f9-126">*puhSurface* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="926f9-127">Wird von der DirectDraw-API verwendet und sollte nicht vom Treiber ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="926f9-127">Is used by the DirectDraw  API and should not be filled in by the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="926f9-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="926f9-128">Return value</span></span>

<span data-ttu-id="926f9-129">**NtGdiDdCreateD3DBuffer** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="926f9-129">**NtGdiDdCreateD3DBuffer** returns one of the following callback codes.</span></span>



| <span data-ttu-id="926f9-130">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="926f9-130">Return code</span></span>                                                                                              | <span data-ttu-id="926f9-131">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="926f9-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="926f9-132"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="926f9-132"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="926f9-133">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="926f9-133">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="926f9-134">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="926f9-134">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="926f9-135">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="926f9-135">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="926f9-136"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="926f9-136"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="926f9-137">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="926f9-137">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="926f9-138">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="926f9-138">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="926f9-139">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="926f9-139">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="926f9-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="926f9-140">Requirements</span></span>



| <span data-ttu-id="926f9-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="926f9-141">Requirement</span></span> | <span data-ttu-id="926f9-142">Wert</span><span class="sxs-lookup"><span data-stu-id="926f9-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="926f9-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="926f9-143">Minimum supported client</span></span><br/> | <span data-ttu-id="926f9-144">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="926f9-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="926f9-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="926f9-145">Minimum supported server</span></span><br/> | <span data-ttu-id="926f9-146">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="926f9-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="926f9-147">Header</span><span class="sxs-lookup"><span data-stu-id="926f9-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="926f9-148"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="926f9-148"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="926f9-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="926f9-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="926f9-150">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="926f9-150">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
