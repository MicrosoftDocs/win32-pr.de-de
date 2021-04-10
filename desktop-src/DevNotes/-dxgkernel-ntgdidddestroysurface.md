---
description: Zerstört ein zuvor zugewiesenes Microsoft DirectDraw Surface-Objekt im Kernel Modus.
ms.assetid: 65419fce-9e82-4621-9906-832144888a3b
title: Ntgdidddestroysurface-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroySurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 54799aa90007370439b2be8c8cf8c1f584360a5d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041427"
---
# <a name="ntgdidddestroysurface-function"></a><span data-ttu-id="ad6f7-103">Ntgdidddestroysurface-Funktion</span><span class="sxs-lookup"><span data-stu-id="ad6f7-103">NtGdiDdDestroySurface function</span></span>

<span data-ttu-id="ad6f7-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="ad6f7-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="ad6f7-105">Verwenden Sie stattdessen DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="ad6f7-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="ad6f7-106">Zerstört ein zuvor zugewiesenes Microsoft DirectDraw Surface-Objekt im Kernel Modus.</span><span class="sxs-lookup"><span data-stu-id="ad6f7-106">Destroys a previously allocated kernel-mode Microsoft DirectDraw surface object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad6f7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad6f7-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdDestroySurface(
  _In_ HANDLE hSurface,
  _In_ BOOL   bRealDestroy
);
```



## <a name="parameters"></a><span data-ttu-id="ad6f7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad6f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad6f7-109">*hsurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad6f7-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad6f7-110">Handle für das zuvor zugewiesene kernelmodusetobjekt.</span><span class="sxs-lookup"><span data-stu-id="ad6f7-110">Handle to previously allocated kernel-mode surface object.</span></span>

</dd> <dt>

<span data-ttu-id="ad6f7-111">*brealdestroy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad6f7-111">*bRealDestroy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad6f7-112">Gibt an, wie die-Oberfläche zerstört werden soll.</span><span class="sxs-lookup"><span data-stu-id="ad6f7-112">Specifies how to destroy the surface.</span></span> <span data-ttu-id="ad6f7-113">Kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ad6f7-113">Can be one of the following values.</span></span>

<dt>



 <span data-ttu-id="ad6f7-114">Fall</span><span class="sxs-lookup"><span data-stu-id="ad6f7-114">(TRUE)</span></span>


</dt> <dd>

<span data-ttu-id="ad6f7-115">Zerstören der Oberfläche und kostenlosen Video Arbeitsspeichers.</span><span class="sxs-lookup"><span data-stu-id="ad6f7-115">Destroy the surface and free video memory.</span></span>

</dd> <dt>



 <span data-ttu-id="ad6f7-116">Alarm</span><span class="sxs-lookup"><span data-stu-id="ad6f7-116">(FALSE)</span></span>


</dt> <dd>

<span data-ttu-id="ad6f7-117">Geben Sie den Videospeicher frei, aber lassen Sie die Oberfläche in einem nicht initialisierten Zustand.</span><span class="sxs-lookup"><span data-stu-id="ad6f7-117">Free the video memory but leave the surface in an uninitialized state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad6f7-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad6f7-118">Return value</span></span>

<span data-ttu-id="ad6f7-119">**Ntgdidddestroysurface** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="ad6f7-119">**NtGdiDdDestroySurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="ad6f7-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ad6f7-120">Return code</span></span>                                                                                              | <span data-ttu-id="ad6f7-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad6f7-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ad6f7-122"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="ad6f7-122"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="ad6f7-123">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ad6f7-123">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="ad6f7-124">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="ad6f7-124">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="ad6f7-125">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="ad6f7-125">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="ad6f7-126"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="ad6f7-126"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="ad6f7-127">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="ad6f7-127">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="ad6f7-128">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="ad6f7-128">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="ad6f7-129">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ad6f7-129">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ad6f7-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad6f7-130">Remarks</span></span>

<span data-ttu-id="ad6f7-131">Es wird empfohlen, dass Anwendungen die DirectDraw-und Direct3D-APIs verwenden, um Oberflächen anstelle dieser Funktion zu erstellen und zu zerstören.</span><span class="sxs-lookup"><span data-stu-id="ad6f7-131">It is recommended that applications use the DirectDraw and Direct3D APIs to create and destroy surfaces instead of this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad6f7-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad6f7-132">Requirements</span></span>



| <span data-ttu-id="ad6f7-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad6f7-133">Requirement</span></span> | <span data-ttu-id="ad6f7-134">Wert</span><span class="sxs-lookup"><span data-stu-id="ad6f7-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ad6f7-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ad6f7-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ad6f7-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad6f7-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="ad6f7-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ad6f7-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ad6f7-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad6f7-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ad6f7-139">Header</span><span class="sxs-lookup"><span data-stu-id="ad6f7-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad6f7-140"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad6f7-140"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad6f7-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad6f7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad6f7-142">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="ad6f7-142">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




