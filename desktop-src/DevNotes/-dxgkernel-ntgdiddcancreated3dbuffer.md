---
description: Bestimmt, ob der Treiber einen Befehl auf Treiber Ebene oder einen Vertex-Puffer der angegebenen Beschreibung erstellen kann.
ms.assetid: c67492d9-c4ba-4206-8beb-3d67235192f9
title: NtGdiDdCanCreateD3DBuffer-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCanCreateD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 849eb2ba9c1349c54c20703217989b0b92ee78e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346427"
---
# <a name="ntgdiddcancreated3dbuffer-function"></a><span data-ttu-id="37f1b-103">NtGdiDdCanCreateD3DBuffer-Funktion</span><span class="sxs-lookup"><span data-stu-id="37f1b-103">NtGdiDdCanCreateD3DBuffer function</span></span>

<span data-ttu-id="37f1b-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="37f1b-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="37f1b-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="37f1b-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="37f1b-106">Bestimmt, ob der Treiber einen Befehl auf Treiber Ebene oder einen Vertex-Puffer der angegebenen Beschreibung erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="37f1b-106">Determines whether the driver can create a driver-level command or vertex buffer of the specified description.</span></span>

## <a name="syntax"></a><span data-ttu-id="37f1b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="37f1b-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCanCreateD3DBuffer(
  _In_    HANDLE                   hDirectDraw,
  _Inout_ PDD_CANCREATESURFACEDATA puCanCreateSurfaceData
);
```



## <a name="parameters"></a><span data-ttu-id="37f1b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="37f1b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37f1b-109">*hdirectdraw* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="37f1b-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37f1b-110">Handle zur [**globalen DD \_ DirectDraw \_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) -Struktur, die das DirectDraw-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="37f1b-110">Handle to the [**DD\_DIRECTDRAW\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) structure representing the DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="37f1b-111">*pucankreatesurfacedata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="37f1b-111">*puCanCreateSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="37f1b-112">Zeiger auf eine [**DD \_ cankreatesurfacedata**](/windows/win32/api/ddrawint/ns-ddrawint-dd_cancreatesurfacedata) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="37f1b-112">Pointer to a [**DD\_CANCREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_cancreatesurfacedata) structure.</span></span> <span data-ttu-id="37f1b-113">Diese Struktur enthält die Informationen, die für den Treiber erforderlich sind, um zu bestimmen, ob ein Befehl oder ein Vertex-Puffer erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="37f1b-113">This structure contains the information required for the driver to determine whether a command or vertex buffer can be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37f1b-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="37f1b-114">Return value</span></span>

<span data-ttu-id="37f1b-115">**NtGdiDdCanCreateD3DBuffer** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="37f1b-115">**NtGdiDdCanCreateD3DBuffer** returns one of the following callback codes.</span></span>



| <span data-ttu-id="37f1b-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="37f1b-116">Return code</span></span>                                                                                              | <span data-ttu-id="37f1b-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37f1b-117">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="37f1b-118"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="37f1b-118"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="37f1b-119">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="37f1b-119">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="37f1b-120">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="37f1b-120">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="37f1b-121">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="37f1b-121">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="37f1b-122"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="37f1b-122"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="37f1b-123">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="37f1b-123">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="37f1b-124">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="37f1b-124">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="37f1b-125">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="37f1b-125">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="37f1b-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37f1b-126">Requirements</span></span>



| <span data-ttu-id="37f1b-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37f1b-127">Requirement</span></span> | <span data-ttu-id="37f1b-128">Wert</span><span class="sxs-lookup"><span data-stu-id="37f1b-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="37f1b-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37f1b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="37f1b-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37f1b-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="37f1b-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37f1b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="37f1b-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37f1b-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="37f1b-133">Header</span><span class="sxs-lookup"><span data-stu-id="37f1b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="37f1b-134"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="37f1b-134"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37f1b-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37f1b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37f1b-136">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="37f1b-136">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
