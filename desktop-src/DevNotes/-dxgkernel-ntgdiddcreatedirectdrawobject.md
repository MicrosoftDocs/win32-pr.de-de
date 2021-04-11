---
description: Erstellt eine Kernel seitige Darstellung des Microsoft DirectDraw-Objekts.
ms.assetid: e380f948-35a0-4cf0-9b69-ab2bd4f9a161
title: Ntgdiddkreatedirectdrawobject-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 16dd140c7b205c92b34cb9bd397a4b8d2d3e1a60
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125942"
---
# <a name="ntgdiddcreatedirectdrawobject-function"></a><span data-ttu-id="c2a61-103">Ntgdiddkreatedirectdrawobject-Funktion</span><span class="sxs-lookup"><span data-stu-id="c2a61-103">NtGdiDdCreateDirectDrawObject function</span></span>

<span data-ttu-id="c2a61-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c2a61-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="c2a61-105">Verwenden Sie stattdessen DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="c2a61-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="c2a61-106">Erstellt eine Kernel seitige Darstellung des Microsoft DirectDraw-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c2a61-106">Creates a kernel-side representation of the Microsoft DirectDraw object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2a61-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2a61-107">Syntax</span></span>


```C++
HANDLE APIENTRY NtGdiDdCreateDirectDrawObject(
  _In_ HDC hdc
);
```



## <a name="parameters"></a><span data-ttu-id="c2a61-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2a61-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2a61-109">*hdc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2a61-109">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2a61-110">Alle DC-Anzeigegeräte, für die das DirectDraw-Objekt erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2a61-110">Any DC display device for which the DirectDraw object should be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2a61-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c2a61-111">Return value</span></span>

<span data-ttu-id="c2a61-112">Bei erfolgreicher Ausführung gibt diese Funktion ein Handle für die Objektdarstellung im Kernelmodus zurück. Andernfalls wird **null** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c2a61-112">If successful, this function returns a handle to the kernel-mode object representation; otherwise it returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2a61-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2a61-113">Remarks</span></span>

<span data-ttu-id="c2a61-114">Anwendungen wird empfohlen, die DirectDraw-und [Direct3D](../direct3d10/d3d10-graphics-reference.md) -APIs zu verwenden, um Grafikgeräte Objekte zu erstellen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="c2a61-114">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="c2a61-115">Diese Konstrukte abstrahieren den Geräte Erstellungs Prozess auf vereinfachte und betriebssystemunabhängige Weise.</span><span class="sxs-lookup"><span data-stu-id="c2a61-115">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2a61-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2a61-116">Requirements</span></span>



| <span data-ttu-id="c2a61-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2a61-117">Requirement</span></span> | <span data-ttu-id="c2a61-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c2a61-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c2a61-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2a61-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c2a61-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2a61-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="c2a61-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2a61-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c2a61-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2a61-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c2a61-123">Header</span><span class="sxs-lookup"><span data-stu-id="c2a61-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2a61-124"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2a61-124"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2a61-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2a61-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2a61-126">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="c2a61-126">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="c2a61-127">**Ddkreatedirectdrawobject**</span><span class="sxs-lookup"><span data-stu-id="c2a61-127">**DdCreateDirectDrawObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatedirectdrawobject)
</dt> </dl>

 

 
