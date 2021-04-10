---
description: Wird verwendet, um eine Sperre freizugeben, die in einem angegebenen Bereich des Pufferspeichers aufbewahrt wird.
ms.assetid: ec06829b-2b3a-45db-9ecd-d4c7cf67b8ae
title: NtGdiDdUnlockD3D-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdUnlockD3D
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 207f647cadc81a797d71a607fdfd6f73ea38f475
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125918"
---
# <a name="ntgdiddunlockd3d-function"></a><span data-ttu-id="fb000-103">NtGdiDdUnlockD3D-Funktion</span><span class="sxs-lookup"><span data-stu-id="fb000-103">NtGdiDdUnlockD3D function</span></span>

<span data-ttu-id="fb000-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="fb000-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="fb000-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="fb000-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="fb000-106">Wird verwendet, um eine Sperre freizugeben, die in einem angegebenen Bereich des Pufferspeichers aufbewahrt wird.</span><span class="sxs-lookup"><span data-stu-id="fb000-106">Used to release a lock held on a specified area of buffer memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb000-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb000-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdUnlockD3D(
  _In_    HANDLE         hSurface,
  _Inout_ PDD_UNLOCKDATA puUnlockData
);
```



## <a name="parameters"></a><span data-ttu-id="fb000-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb000-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb000-109">*hsurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb000-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb000-110">Ein Zeiger auf eine TT- [**\_ Oberflächen \_ lokale**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) Struktur, die die zu entsperrende Fläche beschreibt.</span><span class="sxs-lookup"><span data-stu-id="fb000-110">Pointer to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the surface to be unlocked.</span></span>

</dd> <dt>

<span data-ttu-id="fb000-111">*puunlockdata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fb000-111">*puUnlockData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb000-112">Zeiger auf eine TT- [**\_ unlockdata**](/windows/win32/api/ddrawint/ns-ddrawint-dd_unlockdata) -Struktur, die die Informationen enthält, die zum Ausführen der Sperr Freigabe erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="fb000-112">Pointer to a [**DD\_UNLOCKDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_unlockdata) structure that contains the information required to perform the lock release.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb000-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb000-113">Return value</span></span>

<span data-ttu-id="fb000-114">**NtGdiDdUnlockD3D** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="fb000-114">**NtGdiDdUnlockD3D** returns one of the following callback codes.</span></span>



| <span data-ttu-id="fb000-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="fb000-115">Return code</span></span>                                                                                              | <span data-ttu-id="fb000-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb000-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fb000-117"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="fb000-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="fb000-118">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fb000-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="fb000-119">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="fb000-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="fb000-120">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="fb000-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="fb000-121"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="fb000-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="fb000-122">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="fb000-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="fb000-123">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="fb000-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="fb000-124">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="fb000-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fb000-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb000-125">Requirements</span></span>



| <span data-ttu-id="fb000-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb000-126">Requirement</span></span> | <span data-ttu-id="fb000-127">Wert</span><span class="sxs-lookup"><span data-stu-id="fb000-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fb000-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fb000-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fb000-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb000-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="fb000-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fb000-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fb000-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb000-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fb000-132">Header</span><span class="sxs-lookup"><span data-stu-id="fb000-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb000-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb000-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb000-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb000-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb000-135">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="fb000-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
