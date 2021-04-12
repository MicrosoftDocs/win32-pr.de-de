---
description: Startet die Decodierung eines neuen Frames.
ms.assetid: da2c231d-89a9-4fd9-99b5-f7c1309c26e0
title: Ntgdiddbeginmucompframe-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdBeginMoCompFrame
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 45c359092d1a161aae7671c437fdb9683a2a8eb9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523187"
---
# <a name="ntgdiddbeginmocompframe-function"></a><span data-ttu-id="2b25a-103">Ntgdiddbeginmucompframe-Funktion</span><span class="sxs-lookup"><span data-stu-id="2b25a-103">NtGdiDdBeginMoCompFrame function</span></span>

<span data-ttu-id="2b25a-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="2b25a-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="2b25a-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="2b25a-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="2b25a-106">Startet die Decodierung eines neuen Frames.</span><span class="sxs-lookup"><span data-stu-id="2b25a-106">Starts decoding a new frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b25a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b25a-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdBeginMoCompFrame(
  _In_    HANDLE                   hMoComp,
  _Inout_ PDD_BEGINMOCOMPFRAMEDATA puBeginFrameData
);
```



## <a name="parameters"></a><span data-ttu-id="2b25a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b25a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b25a-109">*hmucomp* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b25a-109">*hMoComp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b25a-110">Handle für eine [**\_ \_ lokale DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) -Struktur, die eine Beschreibung der angeforderten Bewegungskompensation enthält.</span><span class="sxs-lookup"><span data-stu-id="2b25a-110">Handle to a [**DD\_MOTIONCOMP\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) structure that contains a description of the motion compensation being requested.</span></span>

</dd> <dt>

<span data-ttu-id="2b25a-111">*pubeginframedata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2b25a-111">*puBeginFrameData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b25a-112">Zeiger auf eine [**DD \_ beginmucompframedata**](/windows/win32/api/ddrawint/ns-ddrawint-dd_beginmocompframedata) -Struktur, die die Informationen enthält, die zum Starten der Decodierung eines neuen Frames benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="2b25a-112">Pointer to a [**DD\_BEGINMOCOMPFRAMEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_beginmocompframedata) structure that contains the information needed to start decoding a new frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b25a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2b25a-113">Return value</span></span>

<span data-ttu-id="2b25a-114">**Ntgdiddbeginmucompframe** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="2b25a-114">**NtGdiDdBeginMoCompFrame** returns one of the following callback codes.</span></span>



| <span data-ttu-id="2b25a-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2b25a-115">Return code</span></span>                                                                                              | <span data-ttu-id="2b25a-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b25a-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2b25a-117"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="2b25a-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="2b25a-118">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2b25a-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="2b25a-119">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="2b25a-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="2b25a-120">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="2b25a-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="2b25a-121"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="2b25a-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="2b25a-122">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="2b25a-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="2b25a-123">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="2b25a-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="2b25a-124">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2b25a-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2b25a-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b25a-125">Remarks</span></span>

<span data-ttu-id="2b25a-126">Weitere Informationen finden Sie im Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="2b25a-126">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b25a-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b25a-127">Requirements</span></span>



| <span data-ttu-id="2b25a-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b25a-128">Requirement</span></span> | <span data-ttu-id="2b25a-129">Wert</span><span class="sxs-lookup"><span data-stu-id="2b25a-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2b25a-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2b25a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2b25a-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b25a-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="2b25a-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2b25a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2b25a-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b25a-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2b25a-134">Header</span><span class="sxs-lookup"><span data-stu-id="2b25a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b25a-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b25a-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b25a-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b25a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b25a-137">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="2b25a-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
