---
description: Wird von Microsoft DirectDraw-und Microsoft Direct3D-Laufzeiten verwendet, um Informationen vom Treiber zum aktuellen Status abzurufen.
ms.assetid: a7697e0c-9485-4a9c-b211-67ce07dc3604
title: NtGdiD3DGetDriverState-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DGetDriverState
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: c88f2fde4d848aac5ecae3c60aef77d4c6b783cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345607"
---
# <a name="ntgdid3dgetdriverstate-function"></a><span data-ttu-id="28b50-103">NtGdiD3DGetDriverState-Funktion</span><span class="sxs-lookup"><span data-stu-id="28b50-103">NtGdiD3DGetDriverState function</span></span>

<span data-ttu-id="28b50-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="28b50-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="28b50-105">Verwenden Sie stattdessen DirectDraw und Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="28b50-105">Instead, use the DirectDraw and Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="28b50-106">Wird von Microsoft DirectDraw-und Microsoft Direct3D-Laufzeiten verwendet, um Informationen vom Treiber zum aktuellen Status abzurufen.</span><span class="sxs-lookup"><span data-stu-id="28b50-106">Used by both the Microsoft DirectDraw and Microsoft Direct3D runtimes to obtain information from the driver about its current state.</span></span>

## <a name="syntax"></a><span data-ttu-id="28b50-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="28b50-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DGetDriverState(
  _Inout_ PDD_GETDRIVERSTATEDATA pdata
);
```



## <a name="parameters"></a><span data-ttu-id="28b50-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="28b50-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28b50-109">*pData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="28b50-109">*pdata* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="28b50-110">Zeiger auf eine [**DD \_ getdriverstatedata**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getdriverstatedata) -Struktur, die den Status des Treibers beschreibt.</span><span class="sxs-lookup"><span data-stu-id="28b50-110">Pointer to a [**DD\_GETDRIVERSTATEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getdriverstatedata) structure that describes the state of the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28b50-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="28b50-111">Return value</span></span>

<span data-ttu-id="28b50-112">**NtGdiD3DGetDriverState** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="28b50-112">**NtGdiD3DGetDriverState** returns one of the following callback codes.</span></span>



| <span data-ttu-id="28b50-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="28b50-113">Return code</span></span>                                                                                              | <span data-ttu-id="28b50-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28b50-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="28b50-115"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="28b50-115"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="28b50-116">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="28b50-116">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="28b50-117">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="28b50-117">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="28b50-118">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="28b50-118">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="28b50-119"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="28b50-119"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="28b50-120">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="28b50-120">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="28b50-121">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="28b50-121">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="28b50-122">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="28b50-122">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="28b50-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28b50-123">Requirements</span></span>



| <span data-ttu-id="28b50-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28b50-124">Requirement</span></span> | <span data-ttu-id="28b50-125">Wert</span><span class="sxs-lookup"><span data-stu-id="28b50-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="28b50-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="28b50-126">Minimum supported client</span></span><br/> | <span data-ttu-id="28b50-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="28b50-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="28b50-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="28b50-128">Minimum supported server</span></span><br/> | <span data-ttu-id="28b50-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="28b50-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="28b50-130">Header</span><span class="sxs-lookup"><span data-stu-id="28b50-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="28b50-131"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="28b50-131"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28b50-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28b50-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28b50-133">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="28b50-133">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
