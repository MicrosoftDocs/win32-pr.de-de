---
description: Fügt eine Oberfläche an eine andere Oberfläche an.
ms.assetid: c4ef9e96-c498-4175-a2cd-22e0f88fd86e
title: Ntgdiddaddattachedsurface-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdAddAttachedSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: d6e87d3a077c1381eeaa306e594daec0f5b855d1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860811"
---
# <a name="ntgdiddaddattachedsurface-function"></a><span data-ttu-id="d5bcc-103">Ntgdiddaddattachedsurface-Funktion</span><span class="sxs-lookup"><span data-stu-id="d5bcc-103">NtGdiDdAddAttachedSurface function</span></span>

<span data-ttu-id="d5bcc-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d5bcc-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="d5bcc-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="d5bcc-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="d5bcc-106">Fügt eine Oberfläche an eine andere Oberfläche an.</span><span class="sxs-lookup"><span data-stu-id="d5bcc-106">Attaches a surface to another surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5bcc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5bcc-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdAddAttachedSurface(
  _In_    HANDLE                     hSurface,
  _In_    HANDLE                     hSurfaceAttached,
  _Inout_ PDD_ADDATTACHEDSURFACEDATA puAddAttachedSurfaceData
);
```



## <a name="parameters"></a><span data-ttu-id="d5bcc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5bcc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5bcc-109">*hsurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5bcc-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5bcc-110">Handle für eine [**\_ \_ lokale DD-Oberflächen**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) Struktur, die die Oberfläche darstellt, an die eine andere Oberfläche angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="d5bcc-110">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the surface to which another surface is being attached.</span></span>

</dd> <dt>

<span data-ttu-id="d5bcc-111">*hsurfaceattached* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5bcc-111">*hSurfaceAttached* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5bcc-112">Handle für eine [**\_ \_ lokale DD-Oberflächen**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) Struktur, die die anzufügende Oberfläche darstellt.</span><span class="sxs-lookup"><span data-stu-id="d5bcc-112">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the surface to be attached.</span></span>

</dd> <dt>

<span data-ttu-id="d5bcc-113">*puaddattachedsurfacedata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d5bcc-113">*puAddAttachedSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5bcc-114">Ein Zeiger auf eine [**DD \_ addattachedsurfacedata**](/windows/win32/api/ddrawint/ns-ddrawint-dd_addattachedsurfacedata) -Struktur, die Informationen enthält, die der Treiber zum Durchführen der Anlage benötigt.</span><span class="sxs-lookup"><span data-stu-id="d5bcc-114">Pointer to a [**DD\_ADDATTACHEDSURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_addattachedsurfacedata) structure that contains information required for the driver to perform the attachment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5bcc-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d5bcc-115">Return value</span></span>

<span data-ttu-id="d5bcc-116">**Ntgdiddaddattachedsurface** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="d5bcc-116">**NtGdiDdAddAttachedSurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="d5bcc-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d5bcc-117">Return code</span></span>                                                                                              | <span data-ttu-id="d5bcc-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5bcc-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d5bcc-119"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="d5bcc-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="d5bcc-120">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d5bcc-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="d5bcc-121">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="d5bcc-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="d5bcc-122">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="d5bcc-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="d5bcc-123"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="d5bcc-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="d5bcc-124">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d5bcc-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="d5bcc-125">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="d5bcc-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="d5bcc-126">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d5bcc-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d5bcc-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5bcc-127">Requirements</span></span>



| <span data-ttu-id="d5bcc-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5bcc-128">Requirement</span></span> | <span data-ttu-id="d5bcc-129">Wert</span><span class="sxs-lookup"><span data-stu-id="d5bcc-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d5bcc-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d5bcc-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d5bcc-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5bcc-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="d5bcc-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d5bcc-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d5bcc-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5bcc-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d5bcc-134">Header</span><span class="sxs-lookup"><span data-stu-id="d5bcc-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5bcc-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5bcc-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5bcc-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5bcc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5bcc-137">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="d5bcc-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
