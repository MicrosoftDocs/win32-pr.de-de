---
description: Erstellt einen Kontext.
ms.assetid: f972ab40-c9e9-4d2a-88f6-4c7817d5533f
title: NtGdiD3DContextCreate-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DContextCreate
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: f59a80d3efd5e077bc1eadea66255ff5e6ea7523
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125965"
---
# <a name="ntgdid3dcontextcreate-function"></a><span data-ttu-id="af152-103">NtGdiD3DContextCreate-Funktion</span><span class="sxs-lookup"><span data-stu-id="af152-103">NtGdiD3DContextCreate function</span></span>

<span data-ttu-id="af152-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="af152-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="af152-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="af152-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="af152-106">Erstellt einen Kontext.</span><span class="sxs-lookup"><span data-stu-id="af152-106">Creates a context.</span></span>

## <a name="syntax"></a><span data-ttu-id="af152-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="af152-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiD3DContextCreate(
  _In_    HANDLE                  hDirectDrawLocal,
  _In_    HANDLE                  hSurfColor,
  _In_    HANDLE                  hSurfZ,
  _Inout_ D3DNTHAL_CONTEXTCREATEI *pdcci
);
```



## <a name="parameters"></a><span data-ttu-id="af152-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="af152-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af152-109">*hdirectdrawlocal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af152-109">*hDirectDrawLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af152-110">Handle für ein DirectDraw-Objekt im Kernelmodus, das zuvor mit [**ntgdiddkreatedirectdrawobject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md)erstellt wurde und das Gerät darstellt, auf dem der Direct3D-Kontext erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="af152-110">Handle to a kernel-mode DirectDraw object, previously created with [**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md), representing the device on which the Direct3D context is to be created.</span></span>

</dd> <dt>

<span data-ttu-id="af152-111">*hsurfcolor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af152-111">*hSurfColor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af152-112">Handle für eine [**\_ \_ lokale DD-Oberflächen**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) Struktur, die die DirectDraw-Oberfläche beschreibt, die als Renderziel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="af152-112">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the DirectDraw surface to be used as the rendering target.</span></span>

</dd> <dt>

<span data-ttu-id="af152-113">*hsurfz* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af152-113">*hSurfZ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af152-114">Handle für eine [**\_ \_ lokale DD-Oberflächen**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) Struktur, die die DirectDraw-Oberfläche beschreibt, die als tiefen Puffer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="af152-114">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the DirectDraw surface to be used as a depth buffer.</span></span> <span data-ttu-id="af152-115">Wenn dieser Member **null** ist, muss keine tiefen Pufferung durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="af152-115">If this member is **NULL**, no depth buffering is to be performed.</span></span>

</dd> <dt>

<span data-ttu-id="af152-116">*pdcci* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="af152-116">*pdcci* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="af152-117">Zeiger auf eine [**D3DNTHAL \_ contextkreatedata**](/windows-hardware/drivers/ddi/) -Struktur, die die zum Erstellen eines Kontexts erforderlichen Informationen und die Daten enthält, die vom Treiber im neuen Kontext gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="af152-117">Pointer to a [**D3DNTHAL\_CONTEXTCREATEDATA**](/windows-hardware/drivers/ddi/) structure that contains the information required to create a context and the data that the driver should store in the new context.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af152-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="af152-118">Return value</span></span>

<span data-ttu-id="af152-119">**NtGdiD3DContextCreate** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="af152-119">**NtGdiD3DContextCreate** returns one of the following callback codes.</span></span>



| <span data-ttu-id="af152-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="af152-120">Return code</span></span>                                                                                              | <span data-ttu-id="af152-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="af152-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="af152-122"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="af152-122"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="af152-123">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="af152-123">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="af152-124">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="af152-124">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="af152-125">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="af152-125">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="af152-126"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="af152-126"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="af152-127">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="af152-127">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="af152-128">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="af152-128">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="af152-129">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="af152-129">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="af152-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af152-130">Requirements</span></span>



| <span data-ttu-id="af152-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af152-131">Requirement</span></span> | <span data-ttu-id="af152-132">Wert</span><span class="sxs-lookup"><span data-stu-id="af152-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="af152-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="af152-133">Minimum supported client</span></span><br/> | <span data-ttu-id="af152-134">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="af152-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="af152-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="af152-135">Minimum supported server</span></span><br/> | <span data-ttu-id="af152-136">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="af152-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="af152-137">Header</span><span class="sxs-lookup"><span data-stu-id="af152-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="af152-138"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="af152-138"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af152-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af152-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af152-140">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="af152-140">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
