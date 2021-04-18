---
description: Wird verwendet, um einen angegebenen Bereich des Pufferspeichers zu sperren und einen gültigen Zeiger auf einen Speicherblock bereitzustellen, der dem Puffer zugeordnet ist.
ms.assetid: 6f2ecefa-376c-4f6c-a031-666dd992f96a
title: NtGdiDdLockD3D-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdLockD3D
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: c049d37e3507f5bf4429b6ffd5d8ec03327640e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343990"
---
# <a name="ntgdiddlockd3d-function"></a><span data-ttu-id="c7c6a-103">NtGdiDdLockD3D-Funktion</span><span class="sxs-lookup"><span data-stu-id="c7c6a-103">NtGdiDdLockD3D function</span></span>

<span data-ttu-id="c7c6a-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c7c6a-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="c7c6a-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="c7c6a-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="c7c6a-106">Wird verwendet, um einen angegebenen Bereich des Pufferspeichers zu sperren und einen gültigen Zeiger auf einen Speicherblock bereitzustellen, der dem Puffer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c7c6a-106">Used to lock a specified area of buffer memory and to provide a valid pointer to a block of memory associated with the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7c6a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7c6a-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdLockD3D(
  _In_    HANDLE       hSurface,
  _Inout_ PDD_LOCKDATA puLockData
);
```



## <a name="parameters"></a><span data-ttu-id="c7c6a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7c6a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7c6a-109">*hsurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7c6a-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7c6a-110">Ein Zeiger auf eine TT- [**\_ Oberflächen \_ lokale**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) Struktur, die die Oberfläche beschreibt, die der zu sperrenden Speicher Region zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c7c6a-110">Pointer to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the surface associated with the memory region to be locked down.</span></span>

</dd> <dt>

<span data-ttu-id="c7c6a-111">*pulockdata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c7c6a-111">*puLockData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7c6a-112">Ein Zeiger auf eine TT- [**\_ Sperr Daten**](/windows/win32/api/ddrawint/ns-ddrawint-dd_lockdata) Struktur, die die zum Ausführen der Sperre erforderlichen Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="c7c6a-112">Pointer to a [**DD\_LOCKDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_lockdata) structure that contains the information required to perform the lock down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7c6a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7c6a-113">Return value</span></span>

<span data-ttu-id="c7c6a-114">**NtGdiDdLockD3D** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="c7c6a-114">**NtGdiDdLockD3D** returns one of the following callback codes.</span></span>



| <span data-ttu-id="c7c6a-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c7c6a-115">Return code</span></span>                                                                                              | <span data-ttu-id="c7c6a-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7c6a-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c7c6a-117"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="c7c6a-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="c7c6a-118">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c7c6a-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="c7c6a-119">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="c7c6a-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="c7c6a-120">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="c7c6a-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="c7c6a-121"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="c7c6a-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="c7c6a-122">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="c7c6a-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="c7c6a-123">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="c7c6a-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="c7c6a-124">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c7c6a-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c7c6a-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7c6a-125">Requirements</span></span>



| <span data-ttu-id="c7c6a-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7c6a-126">Requirement</span></span> | <span data-ttu-id="c7c6a-127">Wert</span><span class="sxs-lookup"><span data-stu-id="c7c6a-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c7c6a-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c7c6a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c7c6a-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7c6a-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="c7c6a-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c7c6a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c7c6a-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7c6a-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c7c6a-132">Header</span><span class="sxs-lookup"><span data-stu-id="c7c6a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7c6a-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7c6a-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7c6a-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7c6a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7c6a-135">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="c7c6a-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
