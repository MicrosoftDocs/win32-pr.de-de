---
description: Fragt den Blit-Status der angegebenen Oberfläche ab.
ms.assetid: 0221bdc6-2146-4f4d-afb5-d1f701446d5e
title: Ntgdiddgetbltstatus-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetBltStatus
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 381de7f8c360f222a004786834fa36e92f1220d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345436"
---
# <a name="ntgdiddgetbltstatus-function"></a><span data-ttu-id="df310-103">Ntgdiddgetbltstatus-Funktion</span><span class="sxs-lookup"><span data-stu-id="df310-103">NtGdiDdGetBltStatus function</span></span>

<span data-ttu-id="df310-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="df310-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="df310-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="df310-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="df310-106">Fragt den Blit-Status der angegebenen Oberfläche ab.</span><span class="sxs-lookup"><span data-stu-id="df310-106">Queries the blit status of the specified surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="df310-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="df310-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetBltStatus(
  _In_    HANDLE               hSurface,
  _Inout_ PDD_GETBLTSTATUSDATA puGetBltStatusData
);
```



## <a name="parameters"></a><span data-ttu-id="df310-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="df310-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df310-109">*hsurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df310-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df310-110">Handle für eine [ \_ \_ lokale DD-Oberfläche](https://msdn.microsoft.com/library/ms793861.aspx) , die die Oberfläche darstellt, deren Blit-Status abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="df310-110">Handle to a [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure representing the surface whose blit status is being queried.</span></span>

</dd> <dt>

<span data-ttu-id="df310-111">*pugetbltstatus-Daten* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="df310-111">*puGetBltStatusData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="df310-112">Zeiger auf eine [DD \_ getbltstatusdata](https://msdn.microsoft.com/library/ms794243.aspx) -Struktur, die die zum Ausführen der Blit-Statusabfrage erforderlichen Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="df310-112">Pointer to a [DD\_GETBLTSTATUSDATA](https://msdn.microsoft.com/library/ms794243.aspx) structure that contains the information required to perform the blit status query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df310-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="df310-113">Return value</span></span>

<span data-ttu-id="df310-114">**Ntgdiddgetbltstatus** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="df310-114">**NtGdiDdGetBltStatus** returns one of the following callback codes.</span></span>



| <span data-ttu-id="df310-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="df310-115">Return code</span></span>                                                                                              | <span data-ttu-id="df310-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="df310-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="df310-117"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="df310-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="df310-118">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="df310-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="df310-119">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="df310-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="df310-120">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="df310-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="df310-121"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="df310-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="df310-122">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="df310-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="df310-123">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="df310-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="df310-124">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="df310-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="df310-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df310-125">Requirements</span></span>



| <span data-ttu-id="df310-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df310-126">Requirement</span></span> | <span data-ttu-id="df310-127">Wert</span><span class="sxs-lookup"><span data-stu-id="df310-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="df310-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="df310-128">Minimum supported client</span></span><br/> | <span data-ttu-id="df310-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df310-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="df310-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="df310-130">Minimum supported server</span></span><br/> | <span data-ttu-id="df310-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df310-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="df310-132">Header</span><span class="sxs-lookup"><span data-stu-id="df310-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="df310-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="df310-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df310-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df310-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df310-135">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="df310-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




