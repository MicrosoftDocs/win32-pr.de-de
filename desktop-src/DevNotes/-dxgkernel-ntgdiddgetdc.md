---
description: Erstellt einen Gerätekontext (DC) für die angegebene Oberfläche.
ms.assetid: c2eaaed6-db19-4dab-ac12-6b4e7eeb58e4
title: Ntgdiddgetdc-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDC
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 4f930334f0712107d5651a22b35d6917c7977011
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126752"
---
# <a name="ntgdiddgetdc-function"></a><span data-ttu-id="3515b-103">Ntgdiddgetdc-Funktion</span><span class="sxs-lookup"><span data-stu-id="3515b-103">NtGdiDdGetDC function</span></span>

<span data-ttu-id="3515b-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3515b-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="3515b-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="3515b-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="3515b-106">Erstellt einen Gerätekontext (DC) für die angegebene Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="3515b-106">Creates a device context (DC) for the specified surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="3515b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3515b-107">Syntax</span></span>


```C++
HDC APIENTRY NtGdiDdGetDC(
  _In_ HANDLE       hSurface,
  _In_ PALETTEENTRY *puColorTable
);
```



## <a name="parameters"></a><span data-ttu-id="3515b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3515b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3515b-109">*hsurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3515b-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3515b-110">Handle für eine DirectDraw-Oberfläche im Kernelmodus, die zuvor von [**ntgdiddkreatesurface**](-dxgkernel-ntgdiddcreatesurface.md) oder [**ntgdiddkreatesurfaceobject**](-dxgkernel-ntgdiddcreatesurfaceobject.md)zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="3515b-110">Handle to a kernel-mode DirectDraw surface previously returned by [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md) or [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="3515b-111">*pucolortable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3515b-111">*puColorTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3515b-112">Zeiger auf eine Überschreibungs Farbtabelle für den zurückgegebenen DC.</span><span class="sxs-lookup"><span data-stu-id="3515b-112">Pointer to an override color table for the returned DC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3515b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3515b-113">Return value</span></span>

<span data-ttu-id="3515b-114">Bei erfolgreicher Ausführung gibt diese Funktion einen gültigen **hdc** zurück. Andernfalls wird **null** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3515b-114">If successful, this function returns a valid **HDC**; otherwise it returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3515b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3515b-115">Remarks</span></span>

<span data-ttu-id="3515b-116">Pro Oberfläche ist jeweils nur ein DC zulässig.</span><span class="sxs-lookup"><span data-stu-id="3515b-116">Only one DC is allowed per surface at any given time.</span></span> <span data-ttu-id="3515b-117">Bei nachfolgenden Aufrufen von **ntgdiddgetdc** tritt ein Fehler auf, bis der vorherige DC freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="3515b-117">Subsequent calls to **NtGdiDdGetDC** will fail until the previous DC is released.</span></span>

<span data-ttu-id="3515b-118">Anwendungen wird empfohlen, stattdessen [IDirectDrawSurface7:: GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc) aufzurufen, wodurch die gleiche Funktionalität auf eine Weise unabhängig vom Betriebssystem bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3515b-118">Applications are advised to call [IDirectDrawSurface7::GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc) instead, which provides the same functionality in a manner independent of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="3515b-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3515b-119">Requirements</span></span>



| <span data-ttu-id="3515b-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3515b-120">Requirement</span></span> | <span data-ttu-id="3515b-121">Wert</span><span class="sxs-lookup"><span data-stu-id="3515b-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3515b-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3515b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3515b-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3515b-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="3515b-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3515b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3515b-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3515b-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3515b-126">Header</span><span class="sxs-lookup"><span data-stu-id="3515b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3515b-127"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3515b-127"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3515b-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3515b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3515b-129">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="3515b-129">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="3515b-130">**Ddgetdc**</span><span class="sxs-lookup"><span data-stu-id="3515b-130">**DdGetDC**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddgetdc)
</dt> </dl>

 

 
