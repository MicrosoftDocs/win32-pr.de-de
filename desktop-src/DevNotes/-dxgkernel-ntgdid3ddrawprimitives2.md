---
description: Rendert primitive und gibt den aktualisierten renderzustand zurück.
ms.assetid: ef28ee62-a7ad-406c-a892-ffee14123d16
title: NtGdiD3DDrawPrimitives2-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DDrawPrimitives2
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: ebde2fd5adf3b0892606d0ebbc1c7d5f6b55d9cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041371"
---
# <a name="ntgdid3ddrawprimitives2-function"></a><span data-ttu-id="6fb2a-103">NtGdiD3DDrawPrimitives2-Funktion</span><span class="sxs-lookup"><span data-stu-id="6fb2a-103">NtGdiD3DDrawPrimitives2 function</span></span>

<span data-ttu-id="6fb2a-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6fb2a-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="6fb2a-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="6fb2a-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="6fb2a-106">Rendert primitive und gibt den aktualisierten renderzustand zurück.</span><span class="sxs-lookup"><span data-stu-id="6fb2a-106">Renders primitives and returns the updated render state.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fb2a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fb2a-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DDrawPrimitives2(
  _In_    HANDLE                         hCmdBuf,
  _In_    HANDLE                         hVBuf,
  _Inout_ LPD3DNTHAL_DRAWPRIMITIVES2DATA pded,
  _Inout_ FLATPTR                        *pfpVidMemCmd,
  _Inout_ DWORD                          *pdwSizeCmd,
  _Inout_ FLATPTR                        *pfpVidMemVtx,
  _Inout_ DWORD                          *pdwSizeVtx
);
```



## <a name="parameters"></a><span data-ttu-id="6fb2a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6fb2a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fb2a-109">*hcmdbuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6fb2a-109">*hCmdBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fb2a-110">Handle für die [**\_ \_ lokale DD-Oberflächen**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) Struktur, die die DirectDraw-Oberfläche mit den Befehlsdaten identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6fb2a-110">Handle to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that identifies the DirectDraw surface containing the command data.</span></span>

</dd> <dt>

<span data-ttu-id="6fb2a-111">*hvbuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6fb2a-111">*hVBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fb2a-112">Handle für die [**\_ \_ lokale DD-Oberflächen**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) Struktur, die die DirectDraw-Oberfläche identifiziert, die die Scheitelpunkt Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="6fb2a-112">Handle to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that identifies the DirectDraw surface containing the vertex data.</span></span>

</dd> <dt>

<span data-ttu-id="6fb2a-113">*pded* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6fb2a-113">*pded* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6fb2a-114">Ein Zeiger auf eine [**D3DNTHAL \_ DRAWPRIMITIVES2DATA**](/windows-hardware/drivers/ddi/) -Struktur, die die Informationen enthält, die der Treiber zum Rendering von mindestens einem primitiv benötigt.</span><span class="sxs-lookup"><span data-stu-id="6fb2a-114">Pointer to a [**D3DNTHAL\_DRAWPRIMITIVES2DATA**](/windows-hardware/drivers/ddi/) structure that contains the information required for the driver to render one or more primitives.</span></span>

</dd> <dt>

<span data-ttu-id="6fb2a-115">*pfpvidmemcmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6fb2a-115">*pfpVidMemCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6fb2a-116">Neuer Zeiger auf den Videospeicher, wenn der Treiber den Befehls Puffer ausgetauscht hat.</span><span class="sxs-lookup"><span data-stu-id="6fb2a-116">New pointer to video memory if the driver swapped the command buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6fb2a-117">*pdwsizecmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6fb2a-117">*pdwSizeCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6fb2a-118">Gibt die Mindestanzahl von Bytes an, um die der Treiber den Austausch Befehls Puffer erhöhen muss.</span><span class="sxs-lookup"><span data-stu-id="6fb2a-118">Specifies the minimum number of bytes that the driver must increase the swap command buffer by.</span></span>

</dd> <dt>

<span data-ttu-id="6fb2a-119">*pfpvidmemvtx* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6fb2a-119">*pfpVidMemVtx* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6fb2a-120">Neuer Zeiger auf den Videospeicher, wenn der Treiber den Vertex-Puffer ausgetauscht hat.</span><span class="sxs-lookup"><span data-stu-id="6fb2a-120">New pointer to video memory if the driver swapped the vertex buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6fb2a-121">*pdwsizevtx* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6fb2a-121">*pdwSizeVtx* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6fb2a-122">Gibt die Mindestanzahl von Bytes an, die der Treiber für den Vertex-Austausch Puffer zuordnen muss.</span><span class="sxs-lookup"><span data-stu-id="6fb2a-122">Specifies the minimum number of bytes that the driver must allocate for the swap vertex buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fb2a-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6fb2a-123">Return value</span></span>

<span data-ttu-id="6fb2a-124">**NtGdiD3DDrawPrimitives2** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="6fb2a-124">**NtGdiD3DDrawPrimitives2** returns one of the following callback codes.</span></span>



| <span data-ttu-id="6fb2a-125">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6fb2a-125">Return code</span></span>                                                                                              | <span data-ttu-id="6fb2a-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6fb2a-126">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6fb2a-127"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="6fb2a-127"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="6fb2a-128">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6fb2a-128">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="6fb2a-129">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="6fb2a-129">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="6fb2a-130">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="6fb2a-130">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="6fb2a-131"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="6fb2a-131"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="6fb2a-132">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="6fb2a-132">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="6fb2a-133">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="6fb2a-133">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="6fb2a-134">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="6fb2a-134">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6fb2a-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6fb2a-135">Requirements</span></span>



| <span data-ttu-id="6fb2a-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6fb2a-136">Requirement</span></span> | <span data-ttu-id="6fb2a-137">Wert</span><span class="sxs-lookup"><span data-stu-id="6fb2a-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6fb2a-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6fb2a-138">Minimum supported client</span></span><br/> | <span data-ttu-id="6fb2a-139">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6fb2a-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="6fb2a-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6fb2a-140">Minimum supported server</span></span><br/> | <span data-ttu-id="6fb2a-141">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6fb2a-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6fb2a-142">Header</span><span class="sxs-lookup"><span data-stu-id="6fb2a-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fb2a-143"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fb2a-143"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fb2a-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6fb2a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fb2a-145">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="6fb2a-145">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
