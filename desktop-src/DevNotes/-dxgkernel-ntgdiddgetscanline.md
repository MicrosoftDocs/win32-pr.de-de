---
description: Gibt die Nummer der aktuellen physischen Scan Zeile zurück.
ms.assetid: 159d5ea0-25b8-4c2d-9cd4-cf4ee0ca0561
title: Ntgdiddgetscanline-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetScanLine
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 814063208e8115c5ba2a7fe427e21223ac478f57
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342759"
---
# <a name="ntgdiddgetscanline-function"></a><span data-ttu-id="c226d-103">Ntgdiddgetscanline-Funktion</span><span class="sxs-lookup"><span data-stu-id="c226d-103">NtGdiDdGetScanLine function</span></span>

<span data-ttu-id="c226d-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c226d-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="c226d-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="c226d-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="c226d-106">Gibt die Nummer der aktuellen physischen Scan Zeile zurück.</span><span class="sxs-lookup"><span data-stu-id="c226d-106">Returns the number of the current physical scan line.</span></span>

## <a name="syntax"></a><span data-ttu-id="c226d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c226d-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetScanLine(
  _In_    HANDLE              hDirectDraw,
  _Inout_ PDD_GETSCANLINEDATA puGetScanLineData
);
```



## <a name="parameters"></a><span data-ttu-id="c226d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c226d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c226d-109">*hdirectdraw* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c226d-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c226d-110">Handle für eine [**\_ \_ globale DD DirectDraw**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) -Struktur, die den Treiber darstellt.</span><span class="sxs-lookup"><span data-stu-id="c226d-110">Handle to a [**DD\_DIRECTDRAW\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) structure that represents the driver.</span></span>

</dd> <dt>

<span data-ttu-id="c226d-111">*pugetscanlinedata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c226d-111">*puGetScanLineData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c226d-112">Zeiger auf eine [**DD \_ getscanlinedata**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getscanlinedata) -Struktur, in der der Treiber die Nummer der aktuellen Scan Zeile zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="c226d-112">Pointer to a [**DD\_GETSCANLINEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getscanlinedata) structure in which the driver returns the number of the current scan line.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c226d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c226d-113">Return value</span></span>

<span data-ttu-id="c226d-114">**Ntgdiddgetscanline** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="c226d-114">**NtGdiDdGetScanLine** returns one of the following callback codes.</span></span>



| <span data-ttu-id="c226d-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c226d-115">Return code</span></span>                                                                                              | <span data-ttu-id="c226d-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c226d-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c226d-117"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="c226d-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="c226d-118">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c226d-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="c226d-119">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="c226d-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="c226d-120">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="c226d-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="c226d-121"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="c226d-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="c226d-122">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="c226d-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="c226d-123">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="c226d-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="c226d-124">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c226d-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c226d-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c226d-125">Requirements</span></span>



| <span data-ttu-id="c226d-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c226d-126">Requirement</span></span> | <span data-ttu-id="c226d-127">Wert</span><span class="sxs-lookup"><span data-stu-id="c226d-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c226d-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c226d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c226d-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c226d-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="c226d-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c226d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c226d-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c226d-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c226d-132">Header</span><span class="sxs-lookup"><span data-stu-id="c226d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c226d-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c226d-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c226d-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c226d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c226d-135">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="c226d-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
