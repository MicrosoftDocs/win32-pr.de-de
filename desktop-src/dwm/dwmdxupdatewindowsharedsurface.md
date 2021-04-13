---
description: Benachrichtigt den DWM-Code über ein eingehender Update für eine freigegebene Fenster Oberfläche.
ms.assetid: 8357D977-E501-47D7-85BC-7C8954C6D166
title: Dwmdxupdatewindowsharedsurface-Funktion
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
- DwmDxUpdateWindowSharedSurface
ms.openlocfilehash: 7649e96fb3a16458b518d0fc2c6dd09725a4b0ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528130"
---
# <a name="dwmdxupdatewindowsharedsurface-function"></a><span data-ttu-id="65840-103">Dwmdxupdatewindowsharedsurface-Funktion</span><span class="sxs-lookup"><span data-stu-id="65840-103">DwmDxUpdateWindowSharedSurface function</span></span>

<span data-ttu-id="65840-104">Benachrichtigt den DWM-Code über ein eingehender Update für eine freigegebene Fenster Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="65840-104">Notifies the DWM of an incoming update to a window shared surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="65840-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="65840-105">Syntax</span></span>

```C++
HRESULT WINAPI DwmDxUpdateWindowSharedSurface(
  _In_     HWND     hwnd,
  _In_     UINT64   uiUpdateId,
  _In_     DWORD    dwFlags,
  _In_opt_ HMONITOR hmonitorAssociation,
  _In_     RECT     *prc
);
```

## <a name="parameters"></a><span data-ttu-id="65840-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="65840-106">Parameters</span></span>

`hwnd`

<span data-ttu-id="65840-107">Ein [**HWND**](/windows/desktop/winprog/windows-data-types) , das das zu Aktualisier Ende Fenster angibt.</span><span class="sxs-lookup"><span data-stu-id="65840-107">An [**HWND**](/windows/desktop/winprog/windows-data-types) specifying the window being updated.</span></span>

`uiUpdateId`

<span data-ttu-id="65840-108">Die Update-ID, die von [**dwmdxgetwindowsharedsurface**](dwmdxgetwindowsharedsurface.md)abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="65840-108">The update ID retrieved from [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md).</span></span>

`dwFlags`

<span data-ttu-id="65840-109">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="65840-109">Reserved.</span></span>

`hmonitorAssociation`

<span data-ttu-id="65840-110">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="65840-110">Reserved.</span></span>

`prc`

<span data-ttu-id="65840-111">Der Rect des zu aktualisierenden Fensters im Fenster Koordinaten Bereich.</span><span class="sxs-lookup"><span data-stu-id="65840-111">The rect of the window being updated, in window coordinate space.</span></span> <span data-ttu-id="65840-112">Ein NULL-Rechteck gibt an, dass keine Region aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="65840-112">A NULL rectangle indicates that no region was updated.</span></span>

## <a name="return-value"></a><span data-ttu-id="65840-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="65840-113">Return value</span></span>

<span data-ttu-id="65840-114">**S \_ OK** , wenn erfolgreich, andernfalls ein **HRESULT** mit Fehlern.</span><span class="sxs-lookup"><span data-stu-id="65840-114">**S\_OK** if successful, otherwise a FAILED **HRESULT.**</span></span>

## <a name="remarks"></a><span data-ttu-id="65840-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="65840-115">Remarks</span></span>

<span data-ttu-id="65840-116">Diese API ist für die Implementierung eines Grafik Treibers oder einer Laufzeit vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="65840-116">This API is intended for implementing a graphics driver or runtime.</span></span> <span data-ttu-id="65840-117">Eine Anwendung ruft diese Methode möglicherweise nicht auf.</span><span class="sxs-lookup"><span data-stu-id="65840-117">An application may not call this method.</span></span> <span data-ttu-id="65840-118">Diese Dokumentation ist nur für Windows 7 gültig, und diese API ist nicht garantiert vorhanden und verhält sich in anderen Versionen von Windows nicht auf ähnliche Weise.</span><span class="sxs-lookup"><span data-stu-id="65840-118">This documentation is only valid for Windows 7, and this API is not guaranteed to exist nor behave in a similar manner on other versions of Windows.</span></span> <span data-ttu-id="65840-119">Diese Funktion ist in keiner Header-oder statischen Link Bibliothek vorhanden und befindet sich in dwmapi.dll in der Ordnungszahl 101.</span><span class="sxs-lookup"><span data-stu-id="65840-119">This function is not present in any header or static-link library, and it is located at ordinal 101 in dwmapi.dll.</span></span>

<span data-ttu-id="65840-120">Diese Methode sollte nur aufgerufen werden, nachdem " [**dwmdxgetwindowsharedsurface**](dwmdxgetwindowsharedsurface.md) " den Wert " **\_ OK**" zurückgegeben hat und in diesem Szenario aufgerufen werden muss, unabhängig davon, ob die Oberfläche aktualisiert wurde oder nicht.</span><span class="sxs-lookup"><span data-stu-id="65840-120">This method should only ever be called after [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md) returns **S\_OK**, and must be called in that scenario, regardless of whether the surface is updated or not.</span></span>

## <a name="requirements"></a><span data-ttu-id="65840-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65840-121">Requirements</span></span>

| <span data-ttu-id="65840-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65840-122">Requirement</span></span> | <span data-ttu-id="65840-123">Wert</span><span class="sxs-lookup"><span data-stu-id="65840-123">Value</span></span> |
|-|-|
| <span data-ttu-id="65840-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="65840-124">Minimum supported client</span></span> | <span data-ttu-id="65840-125">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="65840-125">Windows 7 \[desktop apps only\]</span></span> |
| <span data-ttu-id="65840-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="65840-126">Minimum supported server</span></span> | <span data-ttu-id="65840-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="65840-127">None supported</span></span> |
| <span data-ttu-id="65840-128">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="65840-128">End of client support</span></span> | <span data-ttu-id="65840-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="65840-129">Windows 7</span></span> |
| <span data-ttu-id="65840-130">Header</span><span class="sxs-lookup"><span data-stu-id="65840-130">Header</span></span> | <span data-ttu-id="65840-131">N/V</span><span class="sxs-lookup"><span data-stu-id="65840-131">N/A</span></span> |
| <span data-ttu-id="65840-132">DLL</span><span class="sxs-lookup"><span data-stu-id="65840-132">DLL</span></span> | <span data-ttu-id="65840-133">Dwmapi.dll</span><span class="sxs-lookup"><span data-stu-id="65840-133">Dwmapi.dll</span></span> |
