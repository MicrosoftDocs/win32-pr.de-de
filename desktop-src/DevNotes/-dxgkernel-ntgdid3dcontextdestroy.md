---
description: Löscht den angegebenen Kontext.
ms.assetid: ac113178-bdb6-4601-940d-6b00b339904d
title: NtGdiD3DContextDestroy-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DContextDestroy
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: 19799c3895072011dd104deec18664d1ffc52b9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523635"
---
# <a name="ntgdid3dcontextdestroy-function"></a><span data-ttu-id="3817b-103">NtGdiD3DContextDestroy-Funktion</span><span class="sxs-lookup"><span data-stu-id="3817b-103">NtGdiD3DContextDestroy function</span></span>

<span data-ttu-id="3817b-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3817b-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="3817b-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="3817b-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="3817b-106">Löscht den angegebenen Kontext.</span><span class="sxs-lookup"><span data-stu-id="3817b-106">Deletes the specified context.</span></span>

## <a name="syntax"></a><span data-ttu-id="3817b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3817b-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DContextDestroy(
  _In_ LPD3DNTHAL_CONTEXTDESTROYDATA pContextDestroyData
);
```



## <a name="parameters"></a><span data-ttu-id="3817b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3817b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3817b-109">*pcontextdestroydata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3817b-109">*pContextDestroyData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3817b-110">Zeiger auf eine [**D3DNTHAL \_ contextdestroydata**](/windows-hardware/drivers/ddi/) -Struktur, die die Informationen enthält, die der Treiber zum Zerstören des Kontexts benötigt.</span><span class="sxs-lookup"><span data-stu-id="3817b-110">Pointer to a [**D3DNTHAL\_CONTEXTDESTROYDATA**](/windows-hardware/drivers/ddi/) structure that contains the information required for the driver to destroy the context.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3817b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3817b-111">Return value</span></span>

<span data-ttu-id="3817b-112">**NtGdiD3DContextDestroy** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="3817b-112">**NtGdiD3DContextDestroy** returns one of the following callback codes.</span></span>



| <span data-ttu-id="3817b-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3817b-113">Return code</span></span>                                                                                              | <span data-ttu-id="3817b-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3817b-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3817b-115"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="3817b-115"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="3817b-116">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3817b-116">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="3817b-117">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="3817b-117">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="3817b-118">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="3817b-118">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="3817b-119"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="3817b-119"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="3817b-120">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="3817b-120">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="3817b-121">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="3817b-121">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="3817b-122">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="3817b-122">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3817b-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3817b-123">Requirements</span></span>



| <span data-ttu-id="3817b-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3817b-124">Requirement</span></span> | <span data-ttu-id="3817b-125">Wert</span><span class="sxs-lookup"><span data-stu-id="3817b-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3817b-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3817b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3817b-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3817b-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="3817b-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3817b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3817b-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3817b-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3817b-130">Header</span><span class="sxs-lookup"><span data-stu-id="3817b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3817b-131"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3817b-131"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3817b-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3817b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3817b-133">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="3817b-133">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
