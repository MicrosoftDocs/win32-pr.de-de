---
description: Gibt an, ob der Treiber eine Oberfläche der angegebenen Oberflächen Beschreibung erstellen kann.
ms.assetid: 4626163b-3070-4246-9a04-0b3438fc7057
title: Ntgdiddcankreatesurface-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCanCreateSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: c45f3e93bff409f68e5ba7fbe441a398e80b0e7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482878"
---
# <a name="ntgdiddcancreatesurface-function"></a><span data-ttu-id="7079a-103">Ntgdiddcankreatesurface-Funktion</span><span class="sxs-lookup"><span data-stu-id="7079a-103">NtGdiDdCanCreateSurface function</span></span>

<span data-ttu-id="7079a-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="7079a-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="7079a-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="7079a-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="7079a-106">Gibt an, ob der Treiber eine Oberfläche der angegebenen Oberflächen Beschreibung erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="7079a-106">Indicates whether the driver can create a surface of the specified surface description.</span></span>

## <a name="syntax"></a><span data-ttu-id="7079a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7079a-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCanCreateSurface(
  _In_    HANDLE                   hDirectDraw,
  _Inout_ PDD_CANCREATESURFACEDATA puCanCreateSurfaceData
);
```



## <a name="parameters"></a><span data-ttu-id="7079a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7079a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7079a-109">*hdirectdraw* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7079a-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7079a-110">Handle zur [**globalen DD \_ DirectDraw \_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) -Struktur, die das DirectDraw-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="7079a-110">Handle to the [**DD\_DIRECTDRAW\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) structure representing the DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="7079a-111">*pucankreatesurfacedata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7079a-111">*puCanCreateSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7079a-112">Zeiger auf eine [**DD \_ canfoatesurfacedata**](/windows/win32/api/ddrawint/ns-ddrawint-dd_cancreatesurfacedata) -Struktur, die die Informationen enthält, die für den Treiber erforderlich sind, um zu bestimmen, ob eine Oberfläche erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7079a-112">Pointer to a [**DD\_CANCREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_cancreatesurfacedata) structure containing the information required for the driver to determine whether a surface can be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7079a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7079a-113">Return value</span></span>

<span data-ttu-id="7079a-114">**Ntgdiddcankreatesurface** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="7079a-114">**NtGdiDdCanCreateSurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="7079a-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7079a-115">Return code</span></span>                                                                                              | <span data-ttu-id="7079a-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7079a-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7079a-117"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="7079a-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="7079a-118">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7079a-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="7079a-119">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="7079a-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="7079a-120">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="7079a-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="7079a-121"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="7079a-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="7079a-122">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="7079a-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="7079a-123">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="7079a-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="7079a-124">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7079a-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7079a-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7079a-125">Requirements</span></span>



| <span data-ttu-id="7079a-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7079a-126">Requirement</span></span> | <span data-ttu-id="7079a-127">Wert</span><span class="sxs-lookup"><span data-stu-id="7079a-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7079a-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7079a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7079a-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7079a-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="7079a-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7079a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7079a-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7079a-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7079a-132">Header</span><span class="sxs-lookup"><span data-stu-id="7079a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7079a-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7079a-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7079a-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7079a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7079a-135">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="7079a-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
