---
description: Legt die Gamma-Rampe für das Gerät fest.
ms.assetid: 92ea0247-6eec-4c5f-9ea7-65f6b97dde1e
title: Ntgdiddsetgammaramp-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetGammaRamp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 0c5efba67eedbd6e70f1e0682f42c1855948cecd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125930"
---
# <a name="ntgdiddsetgammaramp-function"></a><span data-ttu-id="0f048-103">Ntgdiddsetgammaramp-Funktion</span><span class="sxs-lookup"><span data-stu-id="0f048-103">NtGdiDdSetGammaRamp function</span></span>

<span data-ttu-id="0f048-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="0f048-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="0f048-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="0f048-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="0f048-106">Legt die Gamma-Rampe für das Gerät fest.</span><span class="sxs-lookup"><span data-stu-id="0f048-106">Sets the gamma ramp for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f048-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f048-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdSetGammaRamp(
  _In_ HANDLE hDirectDraw,
  _In_ HDC    hdc,
  _In_ LPVOID lpGammaRamp
);
```



## <a name="parameters"></a><span data-ttu-id="0f048-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f048-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f048-109">*hdirectdraw* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f048-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f048-110">Handle für das Kernel Modus-Treiber Objekt, für das die Rampe festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0f048-110">Handle to the kernel-mode driver object for which the ramp is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="0f048-111">*hdc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f048-111">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f048-112">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="0f048-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0f048-113">*lpgammaramp* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f048-113">*lpGammaRamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f048-114">Zeiger auf ein Array von **ddgammaramp** -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="0f048-114">Pointer to an array of **DDGAMMARAMP** structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f048-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0f048-115">Return value</span></span>

<span data-ttu-id="0f048-116">Der Rückgabewert ist " **true** ", wenn die Funktion erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="0f048-116">The return value is **TRUE** if the function is successful.</span></span> <span data-ttu-id="0f048-117">Andernfalls ist der Wert **null**.</span><span class="sxs-lookup"><span data-stu-id="0f048-117">Otherwise, it is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f048-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f048-118">Remarks</span></span>

<span data-ttu-id="0f048-119">Es wird empfohlen, dass Anwendungen stattdessen die **idirectdrawgammacontrol:: setgammaramp** -oder [**IDirect3DDevice9:: setgammaramp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) -Methoden verwenden, da diese Methoden unabhängig vom Betriebssystem die gleiche Funktionalität bieten.</span><span class="sxs-lookup"><span data-stu-id="0f048-119">It is recommended that applications use the **IDirectDrawGammaControl::SetGammaRamp** or [**IDirect3DDevice9::SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) methods instead because these methods offer the same functionality independent of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f048-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f048-120">Requirements</span></span>



| <span data-ttu-id="0f048-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f048-121">Requirement</span></span> | <span data-ttu-id="0f048-122">Wert</span><span class="sxs-lookup"><span data-stu-id="0f048-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0f048-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0f048-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0f048-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f048-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="0f048-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0f048-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0f048-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f048-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0f048-127">Header</span><span class="sxs-lookup"><span data-stu-id="0f048-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f048-128"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f048-128"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f048-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f048-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f048-130">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="0f048-130">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
