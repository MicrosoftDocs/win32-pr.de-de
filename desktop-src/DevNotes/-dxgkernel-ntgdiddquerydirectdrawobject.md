---
description: Fragt eine zuvor erstellte Kernel Modus-Darstellung eines Microsoft DirectDraw-Objekts für seine Funktionen ab.
ms.assetid: ec07c7ef-4c57-4ed9-849b-f30692cc3181
title: Ntgdiddquerydirectdrawobject-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdQueryDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 557854f70f4f1a55022b16d1bfe045efbc017a13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861475"
---
# <a name="ntgdiddquerydirectdrawobject-function"></a><span data-ttu-id="b9f19-103">Ntgdiddquerydirectdrawobject-Funktion</span><span class="sxs-lookup"><span data-stu-id="b9f19-103">NtGdiDdQueryDirectDrawObject function</span></span>

<span data-ttu-id="b9f19-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="b9f19-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="b9f19-105">Verwenden Sie stattdessen DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="b9f19-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="b9f19-106">Fragt eine zuvor erstellte Kernel Modus-Darstellung eines Microsoft DirectDraw-Objekts für seine Funktionen ab.</span><span class="sxs-lookup"><span data-stu-id="b9f19-106">Queries a previously created kernel-mode representation of a Microsoft DirectDraw object for its capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9f19-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9f19-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdQueryDirectDrawObject(
  _In_  HANDLE                      hDirectDrawLocal,
  _Out_ DD_HALINFO                  *pHalInfo,
        DWORD                       *pCallBackFlags,
  _Out_ LPD3DNTHAL_CALLBACKS        puD3dCallbacks,
  _Out_ LPD3DNTHAL_GLOBALDRIVERDATA puD3dDriverData,
  _Out_ PDD_D3DBUFCALLBACKS         puD3dBufferCallbacks,
  _Out_ LPDDSURFACEDESC             puD3dTextureFormats,
  _Out_ DWORD                       *puNumHeaps,
  _Out_ VIDEOMEMORY                 *puvmList,
  _Out_ DWORD                       *puNumFourCC,
  _Out_ DWORD                       *puFourCC
);
```



## <a name="parameters"></a><span data-ttu-id="b9f19-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9f19-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9f19-109">*hdirectdrawlocal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9f19-109">*hDirectDrawLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9f19-110">Handle für den zuvor erstellten Kernel Modus-DirectDraw-Gerät.</span><span class="sxs-lookup"><span data-stu-id="b9f19-110">Handle to the previously-created kernel-mode DirectDraw device.</span></span>

</dd> <dt>

<span data-ttu-id="b9f19-111">*phalinfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b9f19-111">*pHalInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9f19-112">Zeiger auf eine [**DD \_ halinfo**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo) -Struktur, die mit den Funktionen des Geräts gefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="b9f19-112">Pointer to a [**DD\_HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo) structure that will be filled with the device's capabilities.</span></span> <span data-ttu-id="b9f19-113">Weitere Informationen finden Sie in der DDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="b9f19-113">See DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="b9f19-114">*pcallbackflags*</span><span class="sxs-lookup"><span data-stu-id="b9f19-114">*pCallBackFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="b9f19-115">Zeiger auf einen vom Aufrufer bereitgestellten Puffer, der die vom Treiber gemeldeten Rückruf Flags speichert.</span><span class="sxs-lookup"><span data-stu-id="b9f19-115">Pointer to a caller-provided buffer that stores driver-reported callback flags.</span></span> <span data-ttu-id="b9f19-116">Der Puffer sollte die Größe 3 \* sizeof (DWORD) aufweisen und Rückruf Flags in der folgenden Reihenfolge speichern: pcallbackflags \[ 0 für Flags in TT-Rückrufen \] , pcallbackflags [**\_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_callbacks) \[ 1 \] für Flags in [**DD \_ surfakecallbacks**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surfacecallbacks)und pcallbackflags \[ 2 \] für Flags in [**DD \_ palettecallbacks**](/windows/win32/api/ddrawint/ns-ddrawint-dd_palettecallbacks).</span><span class="sxs-lookup"><span data-stu-id="b9f19-116">The buffer should be of size 3\*sizeof(DWORD) and stores callback flags in the following order: pCallBackFlags\[0\] for flags in [**DD\_CALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_callbacks), pCallBackFlags\[1\] for flags in [**DD\_SURFACECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surfacecallbacks), and pCallBackFlags\[2\] for flags in [**DD\_PALETTECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_palettecallbacks).</span></span> <span data-ttu-id="b9f19-117">Weitere Informationen finden Sie in der DDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="b9f19-117">See DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="b9f19-118">*puD3dCallbacks* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b9f19-118">*puD3dCallbacks* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9f19-119">Zeiger auf eine Tabelle mit Direct3D-Rückruf Zeigern.</span><span class="sxs-lookup"><span data-stu-id="b9f19-119">Pointer to a table of Direct3D callback pointers.</span></span> <span data-ttu-id="b9f19-120">Die Tabelle wird mit Zeigern auf Funktionen in Gdi32.dll gefüllt, die einen Direct3D-Anzeigetreiber imitieren.</span><span class="sxs-lookup"><span data-stu-id="b9f19-120">The table is filled with pointers to functions within Gdi32.dll that imitate a Direct3D display driver.</span></span> <span data-ttu-id="b9f19-121">Diese Rückruf Tabelle ist identisch mit der D3DHAL \_ D3DCALLBACKS-Struktur, die in der DDK-Dokumentation erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="b9f19-121">This callback table is identical to the D3DHAL\_D3DCALLBACKS structure discussed in the DDK documentation.</span></span>

</dd> <dt>

<span data-ttu-id="b9f19-122">*puD3dDriverData* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b9f19-122">*puD3dDriverData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9f19-123">Zeiger auf [**D3DHAL \_ globaldriverdata**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata) -Daten, wie in der DDK-Dokumentation beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b9f19-123">Pointer to [**D3DHAL\_GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata) data, as described in the DDK documentation.</span></span>

</dd> <dt>

<span data-ttu-id="b9f19-124">*puD3dBufferCallbacks* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b9f19-124">*puD3dBufferCallbacks* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9f19-125">Zeiger auf eine Tabelle mit Rückruf Zeigern.</span><span class="sxs-lookup"><span data-stu-id="b9f19-125">Pointer to a table of callback pointers.</span></span> <span data-ttu-id="b9f19-126">Die Tabelle wird mit Zeigern auf Funktionen in Gdi32.dll gefüllt, die einen Direct3D-Anzeigetreiber imitieren.</span><span class="sxs-lookup"><span data-stu-id="b9f19-126">The table is filled with pointers to functions within Gdi32.dll that imitate a Direct3D display driver.</span></span> <span data-ttu-id="b9f19-127">Diese Rückruf Tabelle ist identisch mit der ddhal \_ dbxebufcallbacks-Struktur, die der in der DDK-Dokumentation erörterten [**DD \_ D3DBUFCALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_d3dbufcallbacks) -Struktur zugeordnet ist, mit dem Unterschied, dass Member XxxD3DBuffer in **DD \_ D3DBUFCALLBACKS** durch xxxexecutebuffer in ddhal \_ DDE xebufcallbacks ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="b9f19-127">This callback table is identical to the DDHAL\_DDEXEBUFCALLBACKS structure, which maps to the [**DD\_D3DBUFCALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_d3dbufcallbacks) structure discussed in the DDK documentation, except that members XxxD3DBuffer in **DD\_D3DBUFCALLBACKS** are replaced with XxxExecuteBuffer in DDHAL\_DDEXEBUFCALLBACKS.</span></span>

</dd> <dt>

<span data-ttu-id="b9f19-128">*puD3dTextureFormats* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b9f19-128">*puD3dTextureFormats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9f19-129">Zeiger auf ein Array von [**ddsurfacede SC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) -Strukturen, die den Satz zulässiger Textur Formate definieren.</span><span class="sxs-lookup"><span data-stu-id="b9f19-129">Pointer to an array of [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) structures that define the set of permissible texture formats.</span></span>

</dd> <dt>

<span data-ttu-id="b9f19-130">*punüberheaps* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b9f19-130">*puNumHeaps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9f19-131">Zeiger auf den **dwnumheaps** -Member von [**DD \_ halinfo**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**vmidata**.</span><span class="sxs-lookup"><span data-stu-id="b9f19-131">Pointer to the **dwNumHeaps** member of [**DD\_HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**vmiData**.</span></span> <span data-ttu-id="b9f19-132">Der **dwnumheaps** -Member gibt die Anzahl der Arbeitsspeicher Heaps in *puvmlist* an.</span><span class="sxs-lookup"><span data-stu-id="b9f19-132">The **dwNumHeaps** member specifies the number of memory heaps in *puvmList*.</span></span> <span data-ttu-id="b9f19-133">Weitere Informationen finden Sie in der DDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="b9f19-133">See DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="b9f19-134">*puvmlist* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b9f19-134">*puvmList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9f19-135">Zeiger auf eine Liste von Videospeicher-Heap Deskriptoren.</span><span class="sxs-lookup"><span data-stu-id="b9f19-135">Pointer to a list of video memory heap descriptors.</span></span> <span data-ttu-id="b9f19-136">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="b9f19-136">Can be **NULL**.</span></span> <span data-ttu-id="b9f19-137">Dieser Parameter wird nicht verwendet, da die Videospeicher Verwaltung vollständig im Kernel Modus erfolgt.</span><span class="sxs-lookup"><span data-stu-id="b9f19-137">This parameter is not used because video memory management is handled entirely within kernel mode.</span></span>

</dd> <dt>

<span data-ttu-id="b9f19-138">*punumschlag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b9f19-138">*puNumFourCC* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9f19-139">Zeiger auf den **punumfourcccodes** -Member von [**DD \_ halinfo**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddcaps**.</span><span class="sxs-lookup"><span data-stu-id="b9f19-139">Pointer to the **puNumFourCCCodes** member of [**DD\_HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**.</span></span> <span data-ttu-id="b9f19-140">Der **punenumfourcccodes** -Member gibt die Anzahl von [vier Zeichen Codes](../directshow/fourcc-codes.md) an, die vom Treiber unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b9f19-140">The **puNumFourCCCodes** member specifies the number of [Four-Character Codes (FOURCC)](../directshow/fourcc-codes.md) codes that the driver supports.</span></span> <span data-ttu-id="b9f19-141">Weitere Informationen finden Sie in der DDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="b9f19-141">See DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="b9f19-142">*pufourcc* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b9f19-142">*puFourCC* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9f19-143">Zeiger auf eine Liste der unterstützten [viercc-Oberflächen Formate (vier Zeichen Codes)](../directshow/fourcc-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="b9f19-143">Pointer to a list of supported [Four-Character Codes (FOURCC)](../directshow/fourcc-codes.md) surface formats.</span></span> <span data-ttu-id="b9f19-144">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="b9f19-144">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9f19-145">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b9f19-145">Return value</span></span>

<span data-ttu-id="b9f19-146">Wenn erfolgreich, gibt diese Funktion **true** zurück. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b9f19-146">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9f19-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9f19-147">Remarks</span></span>

<span data-ttu-id="b9f19-148">Ein-Vorgang wurde in einem zweistufigen Prozess durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="b9f19-148">A call to this function is designed to be made in a two-step process.</span></span> <span data-ttu-id="b9f19-149">Im ersten Schritt sollten *pufourcc*, *puvmlist* und *puD3dTextureFormats* **null** sein, und [**ddquerydirectdrawobject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject) wird [**DD \_ halinfo**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo)ausfüllen.**ddcaps**. **dwnumfourcccodes**, **DD \_ halinfo**.**vmidata**. **dwnumheaps** und [**D3DHAL \_ globaldriverdata**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata).**dwnumtextureformats** mit der Anzahl der Einträge, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b9f19-149">In the first step, *puFourCC*, *puvmList* and *puD3dTextureFormats* should be **NULL**, and [**DdQueryDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject) will fill in [**DD\_HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**.**dwNumFourCCCodes**, **DD\_HALINFO**.**vmiData**.**dwNumHeaps**, and [**D3DHAL\_GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata).**dwNumTextureFormats** with the number of entries that are to be returned.</span></span> <span data-ttu-id="b9f19-150">Im zweiten Aufruf sollte der Aufrufer Arrays der angegebener Größe zuordnen und diese Zeiger anstelle von **null** -Werten in den Parametern " *pufourcc*", " *puvmlist* " und " *puD3dTextureFormats* " übergeben.</span><span class="sxs-lookup"><span data-stu-id="b9f19-150">In the second call, the caller should allocate arrays of the indicated size and pass those pointers instead of **NULL** values in the *puFourCC*, *puvmList* and *puD3dTextureFormats* parameters.</span></span> <span data-ttu-id="b9f19-151">Die Arrays werden dann mit den entsprechenden Daten aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="b9f19-151">The arrays will then be populated with appropriate data.</span></span>

<span data-ttu-id="b9f19-152">Anwendungen wird empfohlen, die DirectDraw-und [Direct3D](../direct3d10/d3d10-graphics-reference.md) -APIs zu verwenden, um Grafikgeräte Objekte zu erstellen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="b9f19-152">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="b9f19-153">Diese Konstrukte abstrahieren den Geräte Erstellungs Prozess auf vereinfachte und betriebssystemunabhängige Weise.</span><span class="sxs-lookup"><span data-stu-id="b9f19-153">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9f19-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9f19-154">Requirements</span></span>



| <span data-ttu-id="b9f19-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9f19-155">Requirement</span></span> | <span data-ttu-id="b9f19-156">Wert</span><span class="sxs-lookup"><span data-stu-id="b9f19-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b9f19-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b9f19-157">Minimum supported client</span></span><br/> | <span data-ttu-id="b9f19-158">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9f19-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="b9f19-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b9f19-159">Minimum supported server</span></span><br/> | <span data-ttu-id="b9f19-160">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9f19-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b9f19-161">Header</span><span class="sxs-lookup"><span data-stu-id="b9f19-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9f19-162"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9f19-162"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9f19-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9f19-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9f19-164">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="b9f19-164">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="b9f19-165">**Ddquerydirectdrawobject**</span><span class="sxs-lookup"><span data-stu-id="b9f19-165">**DdQueryDirectDrawObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject)
</dt> <dt>

[<span data-ttu-id="b9f19-166">**Ntgdiddkreatedirectdrawobject**</span><span class="sxs-lookup"><span data-stu-id="b9f19-166">**NtGdiDdCreateDirectDrawObject**</span></span>](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> </dl>

 

 
