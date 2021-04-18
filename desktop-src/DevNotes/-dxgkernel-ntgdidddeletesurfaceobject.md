---
description: Ntgdiddgoetesurfaceobject löscht einen zuvor erstellten kernelmodusobjekt.
ms.assetid: 95ce6c73-7e41-4ac3-b849-9b8f53aa3ac3
title: Ntgdidddelta etesurfaceobject-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDeleteSurfaceObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 03988b842aacc29915287490508eb9e9d057e907
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344344"
---
# <a name="ntgdidddeletesurfaceobject-function"></a><span data-ttu-id="90919-103">Ntgdidddelta etesurfaceobject-Funktion</span><span class="sxs-lookup"><span data-stu-id="90919-103">NtGdiDdDeleteSurfaceObject function</span></span>

<span data-ttu-id="90919-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="90919-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="90919-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="90919-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="90919-106">**Ntgdiddgoetesurfaceobject** löscht einen zuvor erstellten kernelmodusobjekt.</span><span class="sxs-lookup"><span data-stu-id="90919-106">**NtGdiDdDeleteSurfaceObject** deletes a previously created kernel-mode surface object.</span></span>

## <a name="syntax"></a><span data-ttu-id="90919-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="90919-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdDeleteSurfaceObject(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a><span data-ttu-id="90919-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="90919-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90919-109">*hsurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90919-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90919-110">Handle für das zuvor erstellte kernelmodusetobjekt.</span><span class="sxs-lookup"><span data-stu-id="90919-110">Handle to the previously created kernel-mode surface object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90919-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="90919-111">Return value</span></span>

<span data-ttu-id="90919-112">Wenn erfolgreich, gibt diese Funktion **true** zurück. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="90919-112">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="90919-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90919-113">Remarks</span></span>

<span data-ttu-id="90919-114">Anwendungen wird empfohlen, die DirectDraw-und [Direct3D](../direct3d10/d3d10-graphics-reference.md) -APIs zu verwenden, um Grafikgeräte Objekte zu erstellen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="90919-114">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="90919-115">Diese Konstrukte abstrahieren den Geräte Erstellungs Prozess auf vereinfachte und betriebssystemunabhängige Weise.</span><span class="sxs-lookup"><span data-stu-id="90919-115">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="90919-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90919-116">Requirements</span></span>



| <span data-ttu-id="90919-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90919-117">Requirement</span></span> | <span data-ttu-id="90919-118">Wert</span><span class="sxs-lookup"><span data-stu-id="90919-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="90919-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="90919-119">Minimum supported client</span></span><br/> | <span data-ttu-id="90919-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90919-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="90919-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="90919-121">Minimum supported server</span></span><br/> | <span data-ttu-id="90919-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90919-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="90919-123">Header</span><span class="sxs-lookup"><span data-stu-id="90919-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="90919-124"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="90919-124"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90919-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90919-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90919-126">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="90919-126">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="90919-127">**Dddelta etesurfaceobject**</span><span class="sxs-lookup"><span data-stu-id="90919-127">**DdDeleteSurfaceObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-dddeletesurfaceobject)
</dt> <dt>

[<span data-ttu-id="90919-128">**Ntgdiddkreatesurfaceobject**</span><span class="sxs-lookup"><span data-stu-id="90919-128">**NtGdiDdCreateSurfaceObject**</span></span>](-dxgkernel-ntgdiddcreatesurfaceobject.md)
</dt> </dl>

 

 
