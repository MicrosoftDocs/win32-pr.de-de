---
description: Fragt den freien Speicherplatz im vom Treiber verwalteten Speicher Heap ab.
ms.assetid: d7f8792b-a515-4e70-9474-6a3474b6612b
title: NtGdiD3DContextDestroyAll-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DContextDestroyAll
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: 8bb42c902555568ebe7a26656cd188e9c8e40213
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860916"
---
# <a name="ntgdid3dcontextdestroyall-function"></a><span data-ttu-id="53fc0-103">NtGdiD3DContextDestroyAll-Funktion</span><span class="sxs-lookup"><span data-stu-id="53fc0-103">NtGdiD3DContextDestroyAll function</span></span>

<span data-ttu-id="53fc0-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="53fc0-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="53fc0-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="53fc0-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="53fc0-106">Fragt den freien Speicherplatz im vom Treiber verwalteten Speicher Heap ab.</span><span class="sxs-lookup"><span data-stu-id="53fc0-106">Queries the amount of free memory in the driver-managed memory heap.</span></span>

## <a name="syntax"></a><span data-ttu-id="53fc0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="53fc0-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DContextDestroyAll(void);
```



## <a name="parameters"></a><span data-ttu-id="53fc0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="53fc0-108">Parameters</span></span>

<span data-ttu-id="53fc0-109">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="53fc0-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="53fc0-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53fc0-110">Return value</span></span>

<span data-ttu-id="53fc0-111">**NtGdiD3DContextDestroyAll** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="53fc0-111">**NtGdiD3DContextDestroyAll** returns one of the following callback codes.</span></span>



| <span data-ttu-id="53fc0-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="53fc0-112">Return code</span></span>                                                                                              | <span data-ttu-id="53fc0-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="53fc0-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="53fc0-114"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="53fc0-114"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="53fc0-115">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="53fc0-115">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="53fc0-116">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="53fc0-116">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="53fc0-117">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="53fc0-117">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="53fc0-118"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="53fc0-118"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="53fc0-119">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="53fc0-119">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="53fc0-120">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="53fc0-120">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="53fc0-121">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="53fc0-121">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="53fc0-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53fc0-122">Requirements</span></span>



| <span data-ttu-id="53fc0-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53fc0-123">Requirement</span></span> | <span data-ttu-id="53fc0-124">Wert</span><span class="sxs-lookup"><span data-stu-id="53fc0-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="53fc0-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="53fc0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="53fc0-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53fc0-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="53fc0-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="53fc0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="53fc0-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53fc0-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="53fc0-129">Header</span><span class="sxs-lookup"><span data-stu-id="53fc0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="53fc0-130"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="53fc0-130"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53fc0-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53fc0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53fc0-132">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="53fc0-132">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




