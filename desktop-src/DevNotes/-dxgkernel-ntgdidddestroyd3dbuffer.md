---
description: Zerstört ein zuvor zugewiesenes Microsoft DirectDraw Surface-Objekt im Kernel Modus, das mit dem dwcaps-Member der DDSCAPS-Struktur erstellt wurde, die auf DDSCAPS \_ executebuffer festgelegt ist.
ms.assetid: c737b706-25be-49b8-8d8c-35f48aea2889
title: NtGdiDdDestroyD3DBuffer-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroyD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: e88394e8cc3d13e1d117a1e53eab1190b1290ca4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747720"
---
# <a name="ntgdidddestroyd3dbuffer-function"></a><span data-ttu-id="1b092-103">NtGdiDdDestroyD3DBuffer-Funktion</span><span class="sxs-lookup"><span data-stu-id="1b092-103">NtGdiDdDestroyD3DBuffer function</span></span>

<span data-ttu-id="1b092-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="1b092-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="1b092-105">Verwenden Sie stattdessen DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="1b092-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="1b092-106">Zerstört ein zuvor zugewiesenes Microsoft DirectDraw Surface-Objekt im Kernel Modus, das mit dem **dwcaps** -Member der [**DDSCAPS**](/previous-versions/windows/hardware/drivers/ff550286(v=vs.85)) -Struktur erstellt wurde, die auf DDSCAPS \_ executebuffer festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1b092-106">Destroys a previously allocated kernel-mode Microsoft DirectDraw surface object that was created with the **dwCaps** member of the [**DDSCAPS**](/previous-versions/windows/hardware/drivers/ff550286(v=vs.85)) structure set to DDSCAPS\_EXECUTEBUFFER.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b092-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b092-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdDestroyD3DBuffer(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a><span data-ttu-id="1b092-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b092-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b092-109">*hsurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b092-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b092-110">Handle für eine [**DD \_ destroysurfacedata**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroysurfacedata) -Struktur, die die Informationen enthält, die zum Zerstören eines Direct3D-Befehls oder Scheitelpunkt Puffers erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="1b092-110">Handle to a [**DD\_DESTROYSURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroysurfacedata) structure that contains the information needed to destroy a Direct3D command or vertex buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b092-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b092-111">Return value</span></span>

<span data-ttu-id="1b092-112">**NtGdiDdDestroyD3DBuffer** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="1b092-112">**NtGdiDdDestroyD3DBuffer** returns one of the following callback codes.</span></span>



| <span data-ttu-id="1b092-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1b092-113">Return code</span></span>                                                                                              | <span data-ttu-id="1b092-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1b092-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1b092-115"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="1b092-115"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="1b092-116">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1b092-116">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="1b092-117">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="1b092-117">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="1b092-118">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="1b092-118">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="1b092-119"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="1b092-119"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="1b092-120">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="1b092-120">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="1b092-121">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="1b092-121">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="1b092-122">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1b092-122">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1b092-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b092-123">Requirements</span></span>



| <span data-ttu-id="1b092-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b092-124">Requirement</span></span> | <span data-ttu-id="1b092-125">Wert</span><span class="sxs-lookup"><span data-stu-id="1b092-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1b092-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b092-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1b092-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b092-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="1b092-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b092-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1b092-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b092-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1b092-130">Header</span><span class="sxs-lookup"><span data-stu-id="1b092-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b092-131"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b092-131"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b092-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b092-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b092-133">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="1b092-133">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
