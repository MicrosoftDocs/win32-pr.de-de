---
description: Bestimmt, ob das zuletzt angeforderte kippen auf einer-Oberfläche aufgetreten ist.
ms.assetid: 4489e259-b22d-4e72-807a-5290401f0331
title: Ntgdiddgetflipstatus-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetFlipStatus
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 49ef59fd110c315b3111252084a3c60ddf4cd598
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861088"
---
# <a name="ntgdiddgetflipstatus-function"></a><span data-ttu-id="d9907-103">Ntgdiddgetflipstatus-Funktion</span><span class="sxs-lookup"><span data-stu-id="d9907-103">NtGdiDdGetFlipStatus function</span></span>

<span data-ttu-id="d9907-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d9907-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="d9907-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="d9907-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="d9907-106">Bestimmt, ob das zuletzt angeforderte kippen auf einer-Oberfläche aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="d9907-106">Determines whether the most recently requested flip on a surface has occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9907-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9907-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetFlipStatus(
  _In_    HANDLE                hSurface,
  _Inout_ PDD_GETFLIPSTATUSDATA puGetFlipStatusData
);
```



## <a name="parameters"></a><span data-ttu-id="d9907-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9907-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9907-109">*hsurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9907-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9907-110">Handle für eine [ \_ \_ lokale DD-Oberflächen](https://msdn.microsoft.com/library/ms793861.aspx) Struktur, die die-Oberfläche beschreibt, deren Flip-Status abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="d9907-110">Handle to a [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure that describes the surface whose flip status is being queried.</span></span>

</dd> <dt>

<span data-ttu-id="d9907-111">*pugetflipstatus Data* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d9907-111">*puGetFlipStatusData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9907-112">Zeiger auf eine [DD \_ getflipstatusdata](https://msdn.microsoft.com/library/ms793859.aspx) -Struktur, die die zum Ausführen der Flip Status-Abfrage erforderlichen Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="d9907-112">Pointer to a [DD\_GETFLIPSTATUSDATA](https://msdn.microsoft.com/library/ms793859.aspx) structure that contains the information required to perform the flip status query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9907-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9907-113">Return value</span></span>

<span data-ttu-id="d9907-114">**Ntgdiddgetflipstatus** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="d9907-114">**NtGdiDdGetFlipStatus** returns one of the following callback codes.</span></span>



| <span data-ttu-id="d9907-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d9907-115">Return code</span></span>                                                                                              | <span data-ttu-id="d9907-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9907-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d9907-117"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="d9907-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="d9907-118">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d9907-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="d9907-119">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="d9907-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="d9907-120">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="d9907-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="d9907-121"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="d9907-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="d9907-122">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d9907-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="d9907-123">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="d9907-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="d9907-124">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d9907-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d9907-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9907-125">Requirements</span></span>



| <span data-ttu-id="d9907-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9907-126">Requirement</span></span> | <span data-ttu-id="d9907-127">Wert</span><span class="sxs-lookup"><span data-stu-id="d9907-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d9907-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d9907-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d9907-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9907-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="d9907-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d9907-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d9907-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9907-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d9907-132">Header</span><span class="sxs-lookup"><span data-stu-id="d9907-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9907-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9907-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9907-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9907-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9907-135">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="d9907-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




