---
description: Bewirkt, dass der mit dem Ziel und den aktuellen Oberflächen verknüpfte Oberflächen Speicher geändert wird.
ms.assetid: 2c557393-079e-48e5-b3a6-1157265d88e3
title: Ntgdiddflip-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdFlip
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 1fd2d6f84f602fd07cc29a0efeae28209cb970a5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861096"
---
# <a name="ntgdiddflip-function"></a><span data-ttu-id="76464-103">Ntgdiddflip-Funktion</span><span class="sxs-lookup"><span data-stu-id="76464-103">NtGdiDdFlip function</span></span>

<span data-ttu-id="76464-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="76464-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="76464-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="76464-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="76464-106">Bewirkt, dass der mit dem Ziel und den aktuellen Oberflächen verknüpfte Oberflächen Speicher geändert wird.</span><span class="sxs-lookup"><span data-stu-id="76464-106">Causes the surface memory associated with the target and current surfaces to be interchanged.</span></span>

## <a name="syntax"></a><span data-ttu-id="76464-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="76464-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdFlip(
  _In_    HANDLE       hSurfaceCurrent,
  _In_    HANDLE       hSurfaceTarget,
  _In_    HANDLE       hSurfaceCurrentLeft,
  _In_    HANDLE       hSurfaceTargetLeft,
  _Inout_ PDD_FLIPDATA puFlipData
);
```



## <a name="parameters"></a><span data-ttu-id="76464-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="76464-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76464-109">*hsurfakecurrent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76464-109">*hSurfaceCurrent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76464-110">Handle für die [ \_ \_ lokale DD-Oberflächen](https://msdn.microsoft.com/library/ms793861.aspx) Struktur, die die aktuelle Oberfläche beschreibt.</span><span class="sxs-lookup"><span data-stu-id="76464-110">Handle to the [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure describing the current surface.</span></span>

</dd> <dt>

<span data-ttu-id="76464-111">*hsurfaketarget* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76464-111">*hSurfaceTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76464-112">Handle für die [ \_ \_ lokale DD-Oberflächen](https://msdn.microsoft.com/library/ms793861.aspx) Struktur, die die Ziel Oberfläche beschreibt, d. h. die Oberfläche, auf die der Treiber kippen soll.</span><span class="sxs-lookup"><span data-stu-id="76464-112">Handle to the [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure describing the target surface; that is, the surface to which the driver should flip.</span></span>

</dd> <dt>

<span data-ttu-id="76464-113">*hsurfakecurrentleft* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76464-113">*hSurfaceCurrentLeft* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76464-114">Handle für die [ \_ \_ lokale DD-Oberflächen](https://msdn.microsoft.com/library/ms793861.aspx) Struktur, die die aktuelle linke Oberfläche beschreibt.</span><span class="sxs-lookup"><span data-stu-id="76464-114">Handle to the [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure describing the current left surface.</span></span>

</dd> <dt>

<span data-ttu-id="76464-115">*hsurfaketargetleft* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76464-115">*hSurfaceTargetLeft* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76464-116">Handle für die [ \_ \_ lokale DD-Oberflächen](https://msdn.microsoft.com/library/ms793861.aspx) Struktur, die die linke Ziel Oberfläche beschreibt, zu der gewechselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="76464-116">Handle to the [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure describing the left target surface to flip to.</span></span>

</dd> <dt>

<span data-ttu-id="76464-117">*puflipdata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="76464-117">*puFlipData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="76464-118">Zeiger auf eine [DD- \_ flipdata](https://msdn.microsoft.com/library/ms794213.aspx) -Struktur, die die zum Ausführen des kippen erforderlichen Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="76464-118">Pointer to a [DD\_FLIPDATA](https://msdn.microsoft.com/library/ms794213.aspx) structure that contains the information required to perform the flip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76464-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76464-119">Return value</span></span>

<span data-ttu-id="76464-120">**Ntgdiddflip** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="76464-120">**NtGdiDdFlip** returns one of the following callback codes.</span></span>



| <span data-ttu-id="76464-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="76464-121">Return code</span></span>                                                                                              | <span data-ttu-id="76464-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76464-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="76464-123"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="76464-123"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="76464-124">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="76464-124">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="76464-125">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="76464-125">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="76464-126">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="76464-126">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="76464-127"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="76464-127"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="76464-128">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="76464-128">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="76464-129">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="76464-129">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="76464-130">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="76464-130">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="76464-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76464-131">Requirements</span></span>



| <span data-ttu-id="76464-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76464-132">Requirement</span></span> | <span data-ttu-id="76464-133">Wert</span><span class="sxs-lookup"><span data-stu-id="76464-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="76464-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76464-134">Minimum supported client</span></span><br/> | <span data-ttu-id="76464-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76464-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="76464-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76464-136">Minimum supported server</span></span><br/> | <span data-ttu-id="76464-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76464-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="76464-138">Header</span><span class="sxs-lookup"><span data-stu-id="76464-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="76464-139"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="76464-139"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76464-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76464-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76464-141">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="76464-141">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




