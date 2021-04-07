---
description: Schließt einen decodierten Frame ab.
ms.assetid: 476f8bcc-2a93-430e-bda5-33102e36a35a
title: Ntgdiddendmucompframe-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdEndMoCompFrame
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 50f56faa724f88e16ef10b46342d8dd53afaf497
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748329"
---
# <a name="ntgdiddendmocompframe-function"></a><span data-ttu-id="2f153-103">Ntgdiddendmucompframe-Funktion</span><span class="sxs-lookup"><span data-stu-id="2f153-103">NtGdiDdEndMoCompFrame function</span></span>

<span data-ttu-id="2f153-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="2f153-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="2f153-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="2f153-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="2f153-106">Schließt einen decodierten Frame ab.</span><span class="sxs-lookup"><span data-stu-id="2f153-106">Completes a decoded frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f153-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f153-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdEndMoCompFrame(
  _In_    HANDLE                 hMoComp,
  _Inout_ PDD_ENDMOCOMPFRAMEDATA puEndFrameData
);
```



## <a name="parameters"></a><span data-ttu-id="2f153-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f153-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f153-109">*hmucomp* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f153-109">*hMoComp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f153-110">Handle für eine [ \_ \_ lokale DD](https://msdn.microsoft.com/library/ms794211.aspx) -Struktur, die eine Beschreibung der angeforderten Bewegungskompensation enthält.</span><span class="sxs-lookup"><span data-stu-id="2f153-110">Handle to a [DD\_MOTIONCOMP\_LOCAL](https://msdn.microsoft.com/library/ms794211.aspx) structure that contains a description of the motion compensation being requested.</span></span>

</dd> <dt>

<span data-ttu-id="2f153-111">*puendframedata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2f153-111">*puEndFrameData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f153-112">Ein Zeiger auf eine [DD \_ endmucompframedata](https://msdn.microsoft.com/library/ms793897.aspx) -Struktur, die die Informationen enthält, die erforderlich sind, um den decodierten Frame abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="2f153-112">Pointer to a [DD\_ENDMOCOMPFRAMEDATA](https://msdn.microsoft.com/library/ms793897.aspx) structure that contains the information needed to complete the decoded frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f153-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f153-113">Return value</span></span>

<span data-ttu-id="2f153-114">**Ntgdiddendmucompframe** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="2f153-114">**NtGdiDdEndMoCompFrame** returns one of the following callback codes.</span></span>



| <span data-ttu-id="2f153-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2f153-115">Return code</span></span>                                                                                              | <span data-ttu-id="2f153-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f153-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2f153-117"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="2f153-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="2f153-118">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2f153-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="2f153-119">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="2f153-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="2f153-120">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="2f153-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="2f153-121"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="2f153-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="2f153-122">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="2f153-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="2f153-123">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="2f153-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="2f153-124">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2f153-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2f153-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f153-125">Remarks</span></span>

<span data-ttu-id="2f153-126">Weitere Informationen finden Sie im Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="2f153-126">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f153-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f153-127">Requirements</span></span>



| <span data-ttu-id="2f153-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f153-128">Requirement</span></span> | <span data-ttu-id="2f153-129">Wert</span><span class="sxs-lookup"><span data-stu-id="2f153-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2f153-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f153-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2f153-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f153-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="2f153-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f153-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2f153-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f153-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2f153-134">Header</span><span class="sxs-lookup"><span data-stu-id="2f153-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f153-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f153-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f153-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f153-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f153-137">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="2f153-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




