---
description: Fügt zwei Oberflächen Darstellungen im Kernel Modus an.
ms.assetid: f1b1859f-8b62-4385-9e8a-296086446fe7
title: Ntgdiddattachsurface-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdAttachSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: a3d099e7b3a3106e0e1e4285b37d2ea205baf3d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346626"
---
# <a name="ntgdiddattachsurface-function"></a><span data-ttu-id="8f112-103">Ntgdiddattachsurface-Funktion</span><span class="sxs-lookup"><span data-stu-id="8f112-103">NtGdiDdAttachSurface function</span></span>

<span data-ttu-id="8f112-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="8f112-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="8f112-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="8f112-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="8f112-106">Fügt zwei Oberflächen Darstellungen im Kernel Modus an.</span><span class="sxs-lookup"><span data-stu-id="8f112-106">Attaches two kernel-mode surface representations.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f112-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f112-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdAttachSurface(
  _In_ HANDLE hSurfaceFrom,
  _In_ HANDLE hSurfaceTo
);
```



## <a name="parameters"></a><span data-ttu-id="8f112-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f112-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f112-109">*hsurfacefrom* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8f112-109">*hSurfaceFrom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f112-110">Handle für das kernelmodusobjekt, das als Ausgangspunkt der neuen Anlage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8f112-110">Handle to kernel-mode surface object that will be the start point of the new attachment.</span></span>

</dd> <dt>

<span data-ttu-id="8f112-111">*hsurfaceto* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8f112-111">*hSurfaceTo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f112-112">Handle für das kernelmodusobjekt, das der Endpunkt der neuen Anlage ist.</span><span class="sxs-lookup"><span data-stu-id="8f112-112">Handle to kernel-mode surface object that will be the end point of the new attachment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f112-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8f112-113">Return value</span></span>

<span data-ttu-id="8f112-114">**Ntgdiddattachsurface** gibt eine der folgenden Elemente zurück:</span><span class="sxs-lookup"><span data-stu-id="8f112-114">**NtGdiDdAttachSurface** returns one of the following:</span></span>



| <span data-ttu-id="8f112-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="8f112-115">Return code</span></span>                                                                          | <span data-ttu-id="8f112-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8f112-116">Description</span></span>                             |
|--------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="8f112-117"><dt>**Fall**</dt></span><span class="sxs-lookup"><span data-stu-id="8f112-117"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="8f112-118">Der Funktions Aufrufvorgang war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8f112-118">The function call succeeded.</span></span><br/> |
| <dl> <span data-ttu-id="8f112-119"><dt>**Alarm**</dt></span><span class="sxs-lookup"><span data-stu-id="8f112-119"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="8f112-120">Fehler beim Funktions Aufruf.</span><span class="sxs-lookup"><span data-stu-id="8f112-120">The function call failed.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="8f112-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8f112-121">Remarks</span></span>

<span data-ttu-id="8f112-122">Eine vollständige Beschreibung der oberflächenanlagen finden Sie unter DirectDraw Software Development Kit (SDK) und Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="8f112-122">See the DirectDraw  software development kit (SDK) and Driver Development Kit (DDK) for a full description of surface attachments.</span></span>

> [!Note]  
> <span data-ttu-id="8f112-123">Wie bei anderen oberflächenanlagen ist die resultierende Anlage unidirektional.</span><span class="sxs-lookup"><span data-stu-id="8f112-123">As with other surface attachments, the resulting attachment is one-way.</span></span> <span data-ttu-id="8f112-124">Nachdem diese Funktion aufgerufen wurde, wird *hsurfaceto* nicht an *hsurfacefrom* angefügt.</span><span class="sxs-lookup"><span data-stu-id="8f112-124">After this function is called, *hSurfaceTo* will not be attached to *hSurfaceFrom*.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8f112-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f112-125">Requirements</span></span>



| <span data-ttu-id="8f112-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8f112-126">Requirement</span></span> | <span data-ttu-id="8f112-127">Wert</span><span class="sxs-lookup"><span data-stu-id="8f112-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8f112-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8f112-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8f112-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8f112-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="8f112-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8f112-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8f112-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8f112-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8f112-132">Header</span><span class="sxs-lookup"><span data-stu-id="8f112-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f112-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f112-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f112-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f112-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f112-135">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="8f112-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




