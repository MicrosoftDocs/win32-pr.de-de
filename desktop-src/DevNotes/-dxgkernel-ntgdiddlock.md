---
description: Sperrt einen angegebenen Bereich des Oberflächen Speichers und stellt einen gültigen Zeiger auf einen Speicherblock bereit, der einer Oberfläche zugeordnet ist.
ms.assetid: 02810576-73d8-431d-ab41-3244dcff311f
title: Ntgdiddlock-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdLock
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 3ddf40ae992b6b463886396ba026ec08293bb027
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482907"
---
# <a name="ntgdiddlock-function"></a><span data-ttu-id="7746a-103">Ntgdiddlock-Funktion</span><span class="sxs-lookup"><span data-stu-id="7746a-103">NtGdiDdLock function</span></span>

<span data-ttu-id="7746a-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="7746a-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="7746a-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="7746a-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="7746a-106">Sperrt einen angegebenen Bereich des Oberflächen Speichers und stellt einen gültigen Zeiger auf einen Speicherblock bereit, der einer Oberfläche zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7746a-106">Locks a specified area of surface memory and provides a valid pointer to a block of memory associated with a surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="7746a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7746a-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdLock(
  _In_    HANDLE       hSurface,
  _Inout_ PDD_LOCKDATA puLockData,
  _In_    HDC          hdcClip
);
```



## <a name="parameters"></a><span data-ttu-id="7746a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7746a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7746a-109">*hsurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7746a-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7746a-110">Handle für eine [**\_ \_ lokale DD-Oberflächen**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) Struktur, die die Oberfläche beschreibt, die der zu Sperr enden Speicher Region zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7746a-110">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the surface associated with the memory region to be locked down.</span></span>

</dd> <dt>

<span data-ttu-id="7746a-111">*pulockdata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7746a-111">*puLockData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7746a-112">Zeiger auf eine TT- [**\_ Sperr Daten**](/windows/win32/api/ddrawint/ns-ddrawint-dd_lockdata) Struktur, die die zum Ausführen der Sperrung erforderlichen Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="7746a-112">Pointer to a [**DD\_LOCKDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_lockdata) structure that contains the information required to perform the lockdown.</span></span>

</dd> <dt>

<span data-ttu-id="7746a-113">*hdcclip* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7746a-113">*hdcClip* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7746a-114">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="7746a-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7746a-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7746a-115">Return value</span></span>

<span data-ttu-id="7746a-116">**Ntgdiddlock** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="7746a-116">**NtGdiDdLock** returns one of the following callback codes.</span></span>



| <span data-ttu-id="7746a-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7746a-117">Return code</span></span>                                                                                              | <span data-ttu-id="7746a-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7746a-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7746a-119"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="7746a-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="7746a-120">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7746a-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="7746a-121">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="7746a-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="7746a-122">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="7746a-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="7746a-123"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="7746a-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="7746a-124">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="7746a-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="7746a-125">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="7746a-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="7746a-126">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7746a-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7746a-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7746a-127">Requirements</span></span>



| <span data-ttu-id="7746a-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7746a-128">Requirement</span></span> | <span data-ttu-id="7746a-129">Wert</span><span class="sxs-lookup"><span data-stu-id="7746a-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7746a-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7746a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7746a-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7746a-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="7746a-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7746a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7746a-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7746a-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7746a-134">Header</span><span class="sxs-lookup"><span data-stu-id="7746a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="7746a-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7746a-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7746a-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7746a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7746a-137">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="7746a-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
