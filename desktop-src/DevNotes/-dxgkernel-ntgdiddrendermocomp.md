---
description: Teilt dem Treiber mit, welche Makroblöcke gerendert werden sollen, indem er die Oberflächen mit den Macroblocks, die Offsets auf jeder Oberfläche, auf der die Makroblöcke vorhanden sind, und die Größe der zu rendernden Makroblock-Daten angibt.
ms.assetid: c49d9dfa-a3db-4572-a474-72c7d4e80940
title: Ntgdiddrendermucomp-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdRenderMoComp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 6e1dd0942a6996264e02531f7e21b2a99f059143
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860623"
---
# <a name="ntgdiddrendermocomp-function"></a><span data-ttu-id="182f4-103">Ntgdiddrendermucomp-Funktion</span><span class="sxs-lookup"><span data-stu-id="182f4-103">NtGdiDdRenderMoComp function</span></span>

<span data-ttu-id="182f4-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="182f4-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="182f4-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="182f4-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="182f4-106">Teilt dem Treiber mit, welche Makroblöcke gerendert werden sollen, indem er die Oberflächen mit den Macroblocks, die Offsets auf jeder Oberfläche, auf der die Makroblöcke vorhanden sind, und die Größe der zu rendernden Makroblock-Daten angibt.</span><span class="sxs-lookup"><span data-stu-id="182f4-106">Tells the driver what macroblocks to render by specifying the surfaces containing the macroblocks, the offsets in each surface where the macroblocks exist, and the size of the macroblock data to be rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="182f4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="182f4-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdRenderMoComp(
  _In_    HANDLE               hMoComp,
  _Inout_ PDD_RENDERMOCOMPDATA puRenderMoCompData
);
```



## <a name="parameters"></a><span data-ttu-id="182f4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="182f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="182f4-109">*hmucomp* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="182f4-109">*hMoComp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="182f4-110">Handle für eine [**\_ \_ lokale DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) -Struktur, die eine Beschreibung der angeforderten Bewegungskompensation enthält.</span><span class="sxs-lookup"><span data-stu-id="182f4-110">Handle to a [**DD\_MOTIONCOMP\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) structure that contains a description of the motion compensation being requested.</span></span>

</dd> <dt>

<span data-ttu-id="182f4-111">*purendermucompdata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="182f4-111">*puRenderMoCompData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="182f4-112">Ein Zeiger auf eine [**DD \_ rendermocompdata**](/windows/win32/api/ddrawint/ns-ddrawint-dd_rendermocompdata) -Struktur, die die zum renderingframe erforderlichen Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="182f4-112">Pointer to a [**DD\_RENDERMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_rendermocompdata) structure that contains the information needed to render a frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="182f4-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="182f4-113">Return value</span></span>

<span data-ttu-id="182f4-114">**Ntgdiddrendermucomp** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="182f4-114">**NtGdiDdRenderMoComp** returns one of the following callback codes.</span></span>



| <span data-ttu-id="182f4-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="182f4-115">Return code</span></span>                                                                                              | <span data-ttu-id="182f4-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="182f4-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="182f4-117"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="182f4-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="182f4-118">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="182f4-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="182f4-119">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="182f4-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="182f4-120">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="182f4-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="182f4-121"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="182f4-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="182f4-122">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="182f4-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="182f4-123">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="182f4-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="182f4-124">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="182f4-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="182f4-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="182f4-125">Remarks</span></span>

<span data-ttu-id="182f4-126">Weitere Informationen finden Sie im Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="182f4-126">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="182f4-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="182f4-127">Requirements</span></span>



| <span data-ttu-id="182f4-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="182f4-128">Requirement</span></span> | <span data-ttu-id="182f4-129">Wert</span><span class="sxs-lookup"><span data-stu-id="182f4-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="182f4-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="182f4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="182f4-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="182f4-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="182f4-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="182f4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="182f4-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="182f4-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="182f4-134">Header</span><span class="sxs-lookup"><span data-stu-id="182f4-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="182f4-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="182f4-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="182f4-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="182f4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="182f4-137">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="182f4-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
