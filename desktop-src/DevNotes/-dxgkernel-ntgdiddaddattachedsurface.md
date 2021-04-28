---
description: 'NtGdiDdAddAttachedSurface-Funktion: Fügt eine Oberfläche an eine andere Oberfläche an.'
ms.assetid: c4ef9e96-c498-4175-a2cd-22e0f88fd86e
title: NtGdiDdAddAttachedSurface-Funktion (Ntgdi.h)
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
ms.openlocfilehash: dacaa07a586a88c808d8da07b8233002e8ae5055
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085788"
---
# <a name="ntgdiddaddattachedsurface-function"></a><span data-ttu-id="61515-103">NtGdiDdAddAttachedSurface-Funktion</span><span class="sxs-lookup"><span data-stu-id="61515-103">NtGdiDdAddAttachedSurface function</span></span>

<span data-ttu-id="61515-104">\[Diese Funktion kann bei jeder Betriebssystemrevision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="61515-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="61515-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs. diese APIs isolieren Anwendungen vor solchen Betriebssystemänderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeigetreibern.\]</span><span class="sxs-lookup"><span data-stu-id="61515-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="61515-106">Fügt eine Oberfläche an eine andere Oberfläche an.</span><span class="sxs-lookup"><span data-stu-id="61515-106">Attaches a surface to another surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="61515-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="61515-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdAddAttachedSurface(
  _In_    HANDLE                     hSurface,
  _In_    HANDLE                     hSurfaceAttached,
  _Inout_ PDD_ADDATTACHEDSURFACEDATA puAddAttachedSurfaceData
);
```



## <a name="parameters"></a><span data-ttu-id="61515-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="61515-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61515-109">*hSurface* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="61515-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61515-110">Handle für eine [**DD \_ SURFACE \_ LOCAL-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) die die Oberfläche darstellt, an die eine andere Oberfläche angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="61515-110">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the surface to which another surface is being attached.</span></span>

</dd> <dt>

<span data-ttu-id="61515-111">*hSurfaceAttached* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="61515-111">*hSurfaceAttached* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61515-112">Handle für eine [**DD \_ SURFACE \_ LOCAL-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) die die anzufügende Oberfläche darstellt.</span><span class="sxs-lookup"><span data-stu-id="61515-112">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the surface to be attached.</span></span>

</dd> <dt>

<span data-ttu-id="61515-113">*puAddAttachedSurfaceData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="61515-113">*puAddAttachedSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="61515-114">Zeiger auf eine [**\_ DD-ADDATTACHEDSURFACEDATA-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_addattachedsurfacedata) die Informationen enthält, die der Treiber zum Ausführen der Anlage benötigt.</span><span class="sxs-lookup"><span data-stu-id="61515-114">Pointer to a [**DD\_ADDATTACHEDSURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_addattachedsurfacedata) structure that contains information required for the driver to perform the attachment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61515-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="61515-115">Return value</span></span>

<span data-ttu-id="61515-116">**NtGdiDdAddAttachedSurface** gibt einen der folgenden Rückrufcodes zurück.</span><span class="sxs-lookup"><span data-stu-id="61515-116">**NtGdiDdAddAttachedSurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="61515-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="61515-117">Return code</span></span>                                                                                              | <span data-ttu-id="61515-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61515-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="61515-119"><dt>**BEHANDELTER \_ DDHAL-TREIBER \_**</dt></span><span class="sxs-lookup"><span data-stu-id="61515-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="61515-120">Der Treiber hat den Vorgang ausgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="61515-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="61515-121">Wenn dieser Code DD \_ OK lautet, wird DirectDraw oder Direct3D mit der -Funktion fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="61515-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="61515-122">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="61515-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="61515-123"><dt>**\_DDHAL-TREIBER \_ NICHT BEHANDELT**</dt></span><span class="sxs-lookup"><span data-stu-id="61515-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="61515-124">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="61515-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="61515-125">Wenn der Treiber einen bestimmten Rückruf implementiert haben muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="61515-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="61515-126">Andernfalls verarbeitet DirectDraw oder Direct3D den Vorgang so, als ob der Treiberrückruf nicht durch Ausführen der geräteunabhängigen DirectDraw- oder Direct3D-Implementierung definiert worden wäre.</span><span class="sxs-lookup"><span data-stu-id="61515-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="61515-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61515-127">Requirements</span></span>



| <span data-ttu-id="61515-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61515-128">Requirement</span></span> | <span data-ttu-id="61515-129">Wert</span><span class="sxs-lookup"><span data-stu-id="61515-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="61515-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="61515-130">Minimum supported client</span></span><br/> | <span data-ttu-id="61515-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61515-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="61515-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="61515-132">Minimum supported server</span></span><br/> | <span data-ttu-id="61515-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61515-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="61515-134">Header</span><span class="sxs-lookup"><span data-stu-id="61515-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="61515-135"><dt>Ntgdi.h</dt></span><span class="sxs-lookup"><span data-stu-id="61515-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61515-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="61515-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61515-137">Clientunterstützung auf niedriger Grafikebene</span><span class="sxs-lookup"><span data-stu-id="61515-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
