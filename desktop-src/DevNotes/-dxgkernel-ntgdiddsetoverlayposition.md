---
description: Legt die Position für eine Überlagerung fest.
ms.assetid: dd495118-9ceb-4100-a7ec-794659bb4461
title: Ntgdiddtaronreverlayposition-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetOverlayPosition
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 73882e20fd7065d208835c2005d102b1312e8ce1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041349"
---
# <a name="ntgdiddsetoverlayposition-function"></a><span data-ttu-id="92bb3-103">Ntgdiddtartarslayposition-Funktion</span><span class="sxs-lookup"><span data-stu-id="92bb3-103">NtGdiDdSetOverlayPosition function</span></span>

<span data-ttu-id="92bb3-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="92bb3-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="92bb3-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="92bb3-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="92bb3-106">Legt die Position für eine Überlagerung fest.</span><span class="sxs-lookup"><span data-stu-id="92bb3-106">Sets the position for an overlay.</span></span>

## <a name="syntax"></a><span data-ttu-id="92bb3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="92bb3-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdSetOverlayPosition(
  _In_    HANDLE                     hSurfaceSource,
  _In_    HANDLE                     hSurfaceDestination,
  _Inout_ PDD_SETOVERLAYPOSITIONDATA puSetOverlayPositionData
);
```



## <a name="parameters"></a><span data-ttu-id="92bb3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="92bb3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92bb3-109">*hsurfakesource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="92bb3-109">*hSurfaceSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92bb3-110">Handle für eine [**\_ \_ lokale DD-Oberflächen**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) Struktur, die die DirectDraw-über Lagerungs Oberfläche darstellt.</span><span class="sxs-lookup"><span data-stu-id="92bb3-110">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the DirectDraw overlay surface.</span></span>

</dd> <dt>

<span data-ttu-id="92bb3-111">*hsurfacedestination* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="92bb3-111">*hSurfaceDestination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92bb3-112">Ein Zeiger auf eine TT- [**\_ Oberflächen \_ lokale**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) Struktur, die die Oberfläche darstellt, die überlagert wird.</span><span class="sxs-lookup"><span data-stu-id="92bb3-112">Pointer to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure representing the surface that is being overlaid.</span></span>

</dd> <dt>

<span data-ttu-id="92bb3-113">*putartarverlaypositiondata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="92bb3-113">*puSetOverlayPositionData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="92bb3-114">Ein Zeiger auf eine [**DD \_ sedeverlaypositiondata**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setoverlaypositiondata) -Struktur, die die zum Festlegen der Überlagerungs Position erforderlichen Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="92bb3-114">Pointer to a [**DD\_SETOVERLAYPOSITIONDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setoverlaypositiondata) structure that contains the information required to set the overlay position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92bb3-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="92bb3-115">Return value</span></span>

<span data-ttu-id="92bb3-116">**Ntgdiddtaresverlayposition** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="92bb3-116">**NtGdiDdSetOverlayPosition** returns one of the following callback codes.</span></span>



| <span data-ttu-id="92bb3-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="92bb3-117">Return code</span></span>                                                                                              | <span data-ttu-id="92bb3-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92bb3-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="92bb3-119"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="92bb3-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="92bb3-120">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="92bb3-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="92bb3-121">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="92bb3-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="92bb3-122">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="92bb3-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="92bb3-123"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="92bb3-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="92bb3-124">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="92bb3-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="92bb3-125">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="92bb3-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="92bb3-126">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="92bb3-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="92bb3-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="92bb3-127">Requirements</span></span>



| <span data-ttu-id="92bb3-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="92bb3-128">Requirement</span></span> | <span data-ttu-id="92bb3-129">Wert</span><span class="sxs-lookup"><span data-stu-id="92bb3-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="92bb3-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="92bb3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="92bb3-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="92bb3-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="92bb3-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="92bb3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="92bb3-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="92bb3-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="92bb3-134">Header</span><span class="sxs-lookup"><span data-stu-id="92bb3-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="92bb3-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="92bb3-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92bb3-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92bb3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92bb3-137">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="92bb3-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
