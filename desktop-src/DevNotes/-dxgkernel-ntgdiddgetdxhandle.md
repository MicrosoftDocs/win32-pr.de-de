---
description: Gibt den Kernel Modus-Microsoft DirectX-API-Handle zurück, der bei nachfolgenden Aufrufen der kernelmoduseinstiegs Punkte verwendet werden soll, die den DirectX-API-Mechanismus steuern.
ms.assetid: c95cb188-305f-4b60-be55-0511b57f0597
title: Ntgdiddgetdxhandle-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDxHandle
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: f1b304216c518765be73d9f3a3e63d39ec4b37fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342765"
---
# <a name="ntgdiddgetdxhandle-function"></a><span data-ttu-id="dc0c2-103">Ntgdiddgetdxhandle-Funktion</span><span class="sxs-lookup"><span data-stu-id="dc0c2-103">NtGdiDdGetDxHandle function</span></span>

<span data-ttu-id="dc0c2-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="dc0c2-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="dc0c2-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="dc0c2-106">Gibt den Kernel Modus-Microsoft DirectX-API-Handle zurück, der bei nachfolgenden Aufrufen der kernelmoduseinstiegs Punkte verwendet werden soll, die den DirectX-API-Mechanismus steuern.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-106">Returns the kernel-mode Microsoft DirectX  API handle to use in subsequent calls to the kernel-mode entry points that control the DirectX  API mechanism.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc0c2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc0c2-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetDxHandle(
  _In_ HANDLE hDirectDraw,
  _In_ HANDLE hSurface,
  _In_ BOOL   bRelease
);
```



## <a name="parameters"></a><span data-ttu-id="dc0c2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc0c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc0c2-109">*hdirectdraw* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc0c2-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc0c2-110">Handle für das DirectDraw-Objekt, das die Oberfläche besitzt.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-110">Handle to DirectDraw object owning the surface.</span></span> <span data-ttu-id="dc0c2-111">Dieser Parameter ist optional und kann auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-111">This parameter is optional and may be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dc0c2-112">*hsurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc0c2-112">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc0c2-113">Handle für die Oberfläche, für die ein DirectX-API-Handle im Kernel Modus zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-113">Handle to surface for which to return a kernel-mode DirectX API handle.</span></span> <span data-ttu-id="dc0c2-114">Dieser Parameter ist optional und kann auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-114">This parameter is optional and may be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dc0c2-115">*brelease* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc0c2-115">*bRelease* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc0c2-116">Legen Sie diese Einstellung auf " **true** " fest, wenn die DirectX API-kernelmodusschnittstelle</span><span class="sxs-lookup"><span data-stu-id="dc0c2-116">Set to **TRUE** if the DirectX API kernel mode interface should be released.</span></span> <span data-ttu-id="dc0c2-117">Andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-117">Otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc0c2-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dc0c2-118">Return value</span></span>

<span data-ttu-id="dc0c2-119">Ein DirectX-API-handle, das in nachfolgenden DirectX-API-orientierten Kernel Einstiegspunkten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-119">A DirectX API handle used in subsequent DirectX API-oriented kernel entry points.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc0c2-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc0c2-120">Remarks</span></span>

<span data-ttu-id="dc0c2-121">Wenn sowohl *hdirectdraw* als auch *hsurface* angegeben werden, wird *hsurface* ignoriert.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-121">If both *hDirectDraw* and *hSurface* are specified, *hSurface* is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc0c2-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc0c2-122">Requirements</span></span>



| <span data-ttu-id="dc0c2-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc0c2-123">Requirement</span></span> | <span data-ttu-id="dc0c2-124">Wert</span><span class="sxs-lookup"><span data-stu-id="dc0c2-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dc0c2-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dc0c2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="dc0c2-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dc0c2-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="dc0c2-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dc0c2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="dc0c2-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dc0c2-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dc0c2-129">Header</span><span class="sxs-lookup"><span data-stu-id="dc0c2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc0c2-130"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc0c2-130"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc0c2-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc0c2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc0c2-132">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="dc0c2-132">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




