---
description: Ändert die visuellen Attribute einer Überlagerungs Oberfläche neu oder ändert Sie.
ms.assetid: 6d39166c-0efc-450d-adf4-9f4dfdf7c57f
title: Ntgdiddupdateoverlay-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdUpdateOverlay
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: bbe610c27d83061bda0996ce9acc082efa95e3a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958185"
---
# <a name="ntgdiddupdateoverlay-function"></a><span data-ttu-id="89204-103">Ntgdiddupdateoverlay-Funktion</span><span class="sxs-lookup"><span data-stu-id="89204-103">NtGdiDdUpdateOverlay function</span></span>

<span data-ttu-id="89204-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="89204-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="89204-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="89204-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="89204-106">Ändert die visuellen Attribute einer Überlagerungs Oberfläche neu oder ändert Sie.</span><span class="sxs-lookup"><span data-stu-id="89204-106">Repositions or modifies the visual attributes of an overlay surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="89204-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="89204-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdUpdateOverlay(
  _In_    HANDLE                hSurfaceDestination,
  _In_    HANDLE                hSurfaceSource,
  _Inout_ PDD_UPDATEOVERLAYDATA puUpdateOverlayData
);
```



## <a name="parameters"></a><span data-ttu-id="89204-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="89204-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89204-109">*hsurfacedestination* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89204-109">*hSurfaceDestination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89204-110">Handle für das zuvor erstellte Kernel Modus-DirectDraw-Objekt.</span><span class="sxs-lookup"><span data-stu-id="89204-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="89204-111">*hsurfakesource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89204-111">*hSurfaceSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89204-112">Handle für eine [**\_ \_ lokale DD-Oberflächen**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) Struktur, die die Überlagerungs Oberfläche beschreibt.</span><span class="sxs-lookup"><span data-stu-id="89204-112">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the overlay surface.</span></span>

</dd> <dt>

<span data-ttu-id="89204-113">*puupdateoverlaydata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="89204-113">*puUpdateOverlayData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="89204-114">Ein Zeiger auf eine [**DD \_ updateoverlaydata**](/windows/win32/api/ddrawint/ns-ddrawint-dd_updateoverlaydata) -Struktur, die die zum Aktualisieren der Überlagerung erforderlichen Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="89204-114">Pointer to a [**DD\_UPDATEOVERLAYDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_updateoverlaydata) structure that contains the information required to update the overlay.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89204-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="89204-115">Return value</span></span>

<span data-ttu-id="89204-116">**Ntgdiddupdateoverlay** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="89204-116">**NtGdiDdUpdateOverlay** returns one of the following callback codes.</span></span>



| <span data-ttu-id="89204-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="89204-117">Return code</span></span>                                                                                              | <span data-ttu-id="89204-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89204-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="89204-119"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="89204-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="89204-120">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="89204-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="89204-121">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="89204-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="89204-122">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="89204-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="89204-123"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="89204-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="89204-124">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="89204-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="89204-125">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="89204-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="89204-126">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="89204-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="89204-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89204-127">Requirements</span></span>



| <span data-ttu-id="89204-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89204-128">Requirement</span></span> | <span data-ttu-id="89204-129">Wert</span><span class="sxs-lookup"><span data-stu-id="89204-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="89204-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="89204-130">Minimum supported client</span></span><br/> | <span data-ttu-id="89204-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="89204-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="89204-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="89204-132">Minimum supported server</span></span><br/> | <span data-ttu-id="89204-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="89204-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="89204-134">Header</span><span class="sxs-lookup"><span data-stu-id="89204-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="89204-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="89204-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89204-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89204-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89204-137">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="89204-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
