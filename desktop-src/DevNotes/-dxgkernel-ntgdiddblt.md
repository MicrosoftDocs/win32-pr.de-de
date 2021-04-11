---
description: Führt eine Bitblock Übertragung aus.
ms.assetid: 90cc02af-96af-4913-ae7d-62f39cd6ddd7
title: Ntgdiddblt-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdBlt
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 86249a8ff1069bc0875aad3fcca576ef78b9db68
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126763"
---
# <a name="ntgdiddblt-function"></a><span data-ttu-id="8291f-103">Ntgdiddblt-Funktion</span><span class="sxs-lookup"><span data-stu-id="8291f-103">NtGdiDdBlt function</span></span>

<span data-ttu-id="8291f-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="8291f-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="8291f-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="8291f-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="8291f-106">Führt eine Bitblock Übertragung aus.</span><span class="sxs-lookup"><span data-stu-id="8291f-106">Performs a bit-block transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="8291f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8291f-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdBlt(
  _In_    HANDLE      hSurfaceDest,
  _In_    HANDLE      hSurfaceSrc,
  _Inout_ PDD_BLTDATA puBltData
);
```



## <a name="parameters"></a><span data-ttu-id="8291f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8291f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8291f-109">*hsurfacedest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8291f-109">*hSurfaceDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8291f-110">Handle für eine [**\_ \_ lokale DD-Oberflächen**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) Struktur, die die Oberfläche beschreibt, auf der Blit werden soll.</span><span class="sxs-lookup"><span data-stu-id="8291f-110">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the surface on which to blit.</span></span>

</dd> <dt>

<span data-ttu-id="8291f-111">*hsurfakesrc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8291f-111">*hSurfaceSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8291f-112">Handle für eine [**\_ \_ lokale DD-Oberflächen**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) Struktur, die die Quell Oberfläche beschreibt.</span><span class="sxs-lookup"><span data-stu-id="8291f-112">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the source surface.</span></span>

</dd> <dt>

<span data-ttu-id="8291f-113">*publtdata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8291f-113">*puBltData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8291f-114">Zeiger auf eine [**DD \_ bltdata**](/windows/win32/api/ddrawint/ns-ddrawint-dd_bltdata) -Struktur, die die Informationen enthält, die der Treiber zum Durchführen des Blit benötigt.</span><span class="sxs-lookup"><span data-stu-id="8291f-114">Pointer to a [**DD\_BLTDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_bltdata) structure that contains the information required for the driver to perform the blit.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8291f-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8291f-115">Return value</span></span>

<span data-ttu-id="8291f-116">**Ntgdiddblt** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="8291f-116">**NtGdiDdBlt** returns one of the following callback codes.</span></span>



| <span data-ttu-id="8291f-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="8291f-117">Return code</span></span>                                                                                              | <span data-ttu-id="8291f-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8291f-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8291f-119"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="8291f-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="8291f-120">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8291f-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="8291f-121">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="8291f-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="8291f-122">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="8291f-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="8291f-123"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="8291f-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="8291f-124">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="8291f-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="8291f-125">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="8291f-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="8291f-126">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8291f-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8291f-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8291f-127">Requirements</span></span>



| <span data-ttu-id="8291f-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8291f-128">Requirement</span></span> | <span data-ttu-id="8291f-129">Wert</span><span class="sxs-lookup"><span data-stu-id="8291f-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8291f-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8291f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8291f-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8291f-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="8291f-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8291f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8291f-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8291f-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8291f-134">Header</span><span class="sxs-lookup"><span data-stu-id="8291f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8291f-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8291f-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8291f-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8291f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8291f-137">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="8291f-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
