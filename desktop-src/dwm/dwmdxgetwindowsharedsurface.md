---
description: Ruft die freigegebene DirectX-Oberfläche ab, die ein bestimmtes Fenster sichert. Diese Oberfläche kann geschrieben werden, um den Inhalt des Fensters zu aktualisieren.
ms.assetid: 500CF5B4-0D56-4201-91F4-7333E45DACEE
title: Dwmdxgetwindowsharedsurface-Funktion
ms.topic: reference
ms.date: 11/27/2018
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Dwmapi.dll
api_name:
- DwmDxGetWindowSharedSurface
ms.openlocfilehash: 15e7829383ce23e5bc06bb61ab9c0c224ab18182
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350542"
---
# <a name="dwmdxgetwindowsharedsurface-function"></a><span data-ttu-id="f4fc5-104">Dwmdxgetwindowsharedsurface-Funktion</span><span class="sxs-lookup"><span data-stu-id="f4fc5-104">DwmDxGetWindowSharedSurface function</span></span>

<span data-ttu-id="f4fc5-105">Ruft die freigegebene DirectX-Oberfläche ab, die ein bestimmtes Fenster sichert.</span><span class="sxs-lookup"><span data-stu-id="f4fc5-105">Retrieves the DirectX shared surface backing a given window.</span></span> <span data-ttu-id="f4fc5-106">Diese Oberfläche kann geschrieben werden, um den Inhalt des Fensters zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f4fc5-106">This surface can be written to in order to update the contents of the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4fc5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4fc5-107">Syntax</span></span>

```C++
HRESULT WINAPI DwmDxGetWindowSharedSurface(
  _In_     HWND        hwnd,
  _In_     LUID        luidAdapter,
  _In_opt_ HMONITOR    hmonitorAssociation,
  _In_     DWORD       dwFlags,
  _Inout_  DXGI_FORMAT *pfmtWindow,
  _Out_    HANDLE      *phDxSurface,
  _Out_    UINT64      *puiUpdateId
);
```

## <a name="parameters"></a><span data-ttu-id="f4fc5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4fc5-108">Parameters</span></span>

`hwnd`

<span data-ttu-id="f4fc5-109">Ein [**HWND**](/windows/desktop/winprog/windows-data-types) , das das zu Aktualisier Ende Fenster angibt.</span><span class="sxs-lookup"><span data-stu-id="f4fc5-109">An [**HWND**](/windows/desktop/winprog/windows-data-types) specifying the window to be updated.</span></span>

`luidAdapter`

<span data-ttu-id="f4fc5-110">Die [**LUID**](/previous-versions/bb401655(v%3dmsdn.10)) des Adapters, auf dem sich die Oberfläche befinden soll.</span><span class="sxs-lookup"><span data-stu-id="f4fc5-110">The [**LUID**](/previous-versions/bb401655(v%3dmsdn.10)) of the adapter where the surface should be located.</span></span>

`hmonitorAssociation`

<span data-ttu-id="f4fc5-111">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="f4fc5-111">Reserved.</span></span>

`dwFlags`

<span data-ttu-id="f4fc5-112">Bei diesem Parameter kann es sich um einen der folgenden Werte oder eine bitweise OR-Kombination mehrerer Werte handeln.</span><span class="sxs-lookup"><span data-stu-id="f4fc5-112">This parameter can be one of the following values, or a bitwise OR combination of multiple values where appropriate.</span></span>

| <span data-ttu-id="f4fc5-113">Wert</span><span class="sxs-lookup"><span data-stu-id="f4fc5-113">Value</span></span> | <span data-ttu-id="f4fc5-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f4fc5-114">Meaning</span></span> |
|-|-|
| <span id="DWM_REDIRECTION_FLAG_WAIT"></span><span id="dwm_redirection_flag_wait"></span><dl> <span data-ttu-id="f4fc5-115"><dt>**DWM \_ Umleitungs Kennzeichen, \_ \_ Wartezeit**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f4fc5-115"><dt>**DWM\_REDIRECTION\_FLAG\_WAIT**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="f4fc5-116">Bewirkt, dass die-Funktion blockiert wird, bis eine vertikale Synchronisierung (VSYNC) seit dem letzten Aufruf der Funktion erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="f4fc5-116">Causes the function to block until a vertical synchronization (VSync) has passed since the last time the function was called successfully.</span></span> |
| <span id="DWM_REDIRECTION_FLAG_SUPPORT_PRESENT_TO_GDI_SURFACE"></span><span id="dwm_redirection_flag_support_present_to_gdi_surface"></span><dl> <span data-ttu-id="f4fc5-117"><dt>**DWM \_ \_ \_ Unterstützung für Umleitungs Kennzeichen \_ \_ für \_ GDI- \_ Oberfläche**</dt> <dt>0x10</dt> vorhanden</span><span class="sxs-lookup"><span data-stu-id="f4fc5-117"><dt>**DWM\_REDIRECTION\_FLAG\_SUPPORT\_PRESENT\_TO\_GDI\_SURFACE**</dt> <dt>0x10</dt></span></span> </dl> | <span data-ttu-id="f4fc5-118">Gibt an, dass die aufrufenden Anwendung eine freigegebene GDI-Oberfläche darstellen kann.</span><span class="sxs-lookup"><span data-stu-id="f4fc5-118">Indicates that the calling application is capable of presenting to a GDI shared surface.</span></span> |

`pfmtWindow`

<span data-ttu-id="f4fc5-119">Bei Eingabe das gewünschte Format der-Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="f4fc5-119">On input, the desired format of the surface.</span></span> <span data-ttu-id="f4fc5-120">Bei Ausgabe das tatsächliche Format der zurückgegebenen Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="f4fc5-120">On output, the actual format of the returned surface.</span></span>

`phDxSurface`

<span data-ttu-id="f4fc5-121">Bei der Ausgabe das freigegebene Handle für die-Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="f4fc5-121">On output, the shared handle to the surface.</span></span>

`puiUpdateId`

<span data-ttu-id="f4fc5-122">Bei Ausgabe die ID des Updates.</span><span class="sxs-lookup"><span data-stu-id="f4fc5-122">On output, the ID of the update.</span></span>

## <a name="return-value"></a><span data-ttu-id="f4fc5-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f4fc5-123">Return value</span></span>

<span data-ttu-id="f4fc5-124">Diese Funktion kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f4fc5-124">This function can return one of these values.</span></span>

| <span data-ttu-id="f4fc5-125">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f4fc5-125">Return code</span></span> | <span data-ttu-id="f4fc5-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4fc5-126">Description</span></span> |
|-|-|
| <span data-ttu-id="f4fc5-127">**S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="f4fc5-127">**S\_OK**</span></span> | <span data-ttu-id="f4fc5-128">Der Aufruf war erfolgreich, und Sie sollten die Oberfläche aktualisieren und dabei sicherstellen, dass die Update-ID an [D3DKMTRender](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtrender) übergeben wird (im Element " **presenthistorytoken** " der **D3DKMT- \_ Renderstruktur** , wenn das Update übermittelt wird, und " [**dwmdxupdatewindowsharedsurface**](dwmdxupdatewindowsharedsurface.md) " sollte mit derselben Update-ID aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f4fc5-128">The call succeeded, and you should update the surface, being sure to pass the update ID to [D3DKMTRender](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtrender) (in the **PresentHistoryToken** member of the **D3DKMT\_RENDER** structure when the update is submitted, and then [**DwmDxUpdateWindowSharedSurface**](dwmdxupdatewindowsharedsurface.md) should be called with the same update ID.</span></span> <span data-ttu-id="f4fc5-129">Beachten Sie, dass **dwmdxupdatewindowsharedsurface** unabhängig davon aufgerufen werden sollte, ob die Oberfläche tatsächlich aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f4fc5-129">Note that **DwmDxUpdateWindowSharedSurface** should be called regardless of whether the surface was actually updated or not.</span></span> |
| <span data-ttu-id="f4fc5-130">**DWM \_ S- \_ GDI- \_ Umleitungs \_ Oberfläche**</span><span class="sxs-lookup"><span data-stu-id="f4fc5-130">**DWM\_S\_GDI\_REDIRECTION\_SURFACE**</span></span> | <span data-ttu-id="f4fc5-131">Der Aufruf war erfolgreich, und Sie sollten die Oberfläche durch Aufrufen von [D3DKMTPresent](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtpresent)aktualisieren und das **Modell** des **presenthistorytoken** -Members auf **D3DKMT \_ PM \_ umgeleitete \_ blt** festlegen und die Update-ID im **blt** -Member der Union angeben.</span><span class="sxs-lookup"><span data-stu-id="f4fc5-131">The call succeeded, and you should update the surface by calling [D3DKMTPresent](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtpresent), and setting **PresentHistoryToken** member's **Model** to **D3DKMT\_PM\_REDIRECTED\_BLT**, and providing the update ID in the **Blt** member of the union.</span></span> <span data-ttu-id="f4fc5-132">Dieser Wert wird nur zurückgegeben **, wenn \_ die Unterstützung von DWM-Umleitungs Kennzeichen \_ \_ \_ \_ für \_ GDI- \_ Oberfläche** in *dwFlags* angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="f4fc5-132">This value is only returned if **DWM\_REDIRECTION\_FLAG\_SUPPORT\_PRESENT\_TO\_GDI\_SURFACE** was specified in *dwFlags*.</span></span> |
| <span data-ttu-id="f4fc5-133">**der DWM \_ E- \_ Adapter wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="f4fc5-133">**DWM\_E\_ADAPTER\_NOT\_FOUND**</span></span> | <span data-ttu-id="f4fc5-134">Der Wert von *luidadapter* ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f4fc5-134">The value of *luidAdapter* is not valid.</span></span> |
| <span data-ttu-id="f4fc5-135">**DWM \_ E \_ compositiondeaktiviert**</span><span class="sxs-lookup"><span data-stu-id="f4fc5-135">**DWM\_E\_COMPOSITIONDISABLED**</span></span> | <span data-ttu-id="f4fc5-136">DWM ist zurzeit nicht aktiviert, und die Anwendung muss eine andere Möglichkeit darstellen.</span><span class="sxs-lookup"><span data-stu-id="f4fc5-136">DWM is not currently enabled, and the application will need to present another way.</span></span> |

## <a name="remarks"></a><span data-ttu-id="f4fc5-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4fc5-137">Remarks</span></span>

<span data-ttu-id="f4fc5-138">Diese API ist für die Implementierung eines Grafik Treibers oder einer Laufzeit vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="f4fc5-138">This API is intended for implementing a graphics driver or runtime.</span></span> <span data-ttu-id="f4fc5-139">Eine Anwendung ruft diese Methode möglicherweise nicht auf.</span><span class="sxs-lookup"><span data-stu-id="f4fc5-139">An application may not call this method.</span></span> <span data-ttu-id="f4fc5-140">Diese Dokumentation ist nur für Windows 7 gültig, und diese API ist nicht garantiert vorhanden und verhält sich in anderen Versionen von Windows nicht auf ähnliche Weise.</span><span class="sxs-lookup"><span data-stu-id="f4fc5-140">This documentation is only valid for Windows 7, and this API is not guaranteed to exist nor behave in a similar manner on other versions of Windows.</span></span> <span data-ttu-id="f4fc5-141">Diese Funktion ist in keiner Header-oder statischen Link Bibliothek vorhanden und befindet sich in dwmapi.dll in der Ordnungszahl 100.</span><span class="sxs-lookup"><span data-stu-id="f4fc5-141">This function is not present in any header or static-link library, and it is located at ordinal 100 in dwmapi.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4fc5-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4fc5-142">Requirements</span></span>

| <span data-ttu-id="f4fc5-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4fc5-143">Requirement</span></span> | <span data-ttu-id="f4fc5-144">Wert</span><span class="sxs-lookup"><span data-stu-id="f4fc5-144">Value</span></span> |
|-|-|
| <span data-ttu-id="f4fc5-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f4fc5-145">Minimum supported client</span></span> | <span data-ttu-id="f4fc5-146">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4fc5-146">Windows 7 \[desktop apps only\]</span></span> |
| <span data-ttu-id="f4fc5-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f4fc5-147">Minimum supported server</span></span> | <span data-ttu-id="f4fc5-148">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f4fc5-148">None supported</span></span> |
| <span data-ttu-id="f4fc5-149">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f4fc5-149">End of client support</span></span> | <span data-ttu-id="f4fc5-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f4fc5-150">Windows 7</span></span> |
| <span data-ttu-id="f4fc5-151">Header</span><span class="sxs-lookup"><span data-stu-id="f4fc5-151">Header</span></span> | <span data-ttu-id="f4fc5-152">N/V</span><span class="sxs-lookup"><span data-stu-id="f4fc5-152">N/A</span></span> |
| <span data-ttu-id="f4fc5-153">DLL</span><span class="sxs-lookup"><span data-stu-id="f4fc5-153">DLL</span></span> | <span data-ttu-id="f4fc5-154">Dwmapi.dll</span><span class="sxs-lookup"><span data-stu-id="f4fc5-154">Dwmapi.dll</span></span> |
