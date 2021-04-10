---
description: Zerstört ein zuvor erstelltes Microsoft DirectDraw-Geräte Objekt im Kernel Modus.
ms.assetid: 0b2e1bae-8291-4fe4-9528-980680906e0a
title: Ntgdidddeletedirectdrawobject-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDeleteDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 9ac10798f83fe7e1a07a0803dd29cfa9cd8b1c98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125936"
---
# <a name="ntgdidddeletedirectdrawobject-function"></a><span data-ttu-id="423d4-103">Ntgdidddeletedirectdrawobject-Funktion</span><span class="sxs-lookup"><span data-stu-id="423d4-103">NtGdiDdDeleteDirectDrawObject function</span></span>

<span data-ttu-id="423d4-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="423d4-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="423d4-105">Verwenden Sie stattdessen DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="423d4-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="423d4-106">Zerstört ein zuvor erstelltes Microsoft DirectDraw-Geräte Objekt im Kernel Modus.</span><span class="sxs-lookup"><span data-stu-id="423d4-106">Destroys a previously created kernel-mode Microsoft DirectDraw device object.</span></span>

## <a name="syntax"></a><span data-ttu-id="423d4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="423d4-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdDeleteDirectDrawObject(
   HANDLE hDirectDrawLocal
);
```



## <a name="parameters"></a><span data-ttu-id="423d4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="423d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="423d4-109">*hdirectdrawlocal*</span><span class="sxs-lookup"><span data-stu-id="423d4-109">*hDirectDrawLocal*</span></span> 
</dt> <dd>

<span data-ttu-id="423d4-110">Handle für das DirectDraw-Geräte Objekt im Kernel Modus.</span><span class="sxs-lookup"><span data-stu-id="423d4-110">Handle to the kernel-mode DirectDraw device object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="423d4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="423d4-111">Return value</span></span>

<span data-ttu-id="423d4-112">Wenn erfolgreich, gibt diese Funktion **true** zurück. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="423d4-112">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="423d4-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="423d4-113">Remarks</span></span>

<span data-ttu-id="423d4-114">Anwendungen wird empfohlen, die DirectDraw-und [Direct3D](../direct3d10/d3d10-graphics-reference.md) -APIs zu verwenden, um Grafikgeräte Objekte zu erstellen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="423d4-114">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="423d4-115">Diese Konstrukte abstrahieren den Geräte Erstellungs Prozess auf vereinfachte und betriebssystemunabhängige Weise.</span><span class="sxs-lookup"><span data-stu-id="423d4-115">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="423d4-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="423d4-116">Requirements</span></span>



| <span data-ttu-id="423d4-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="423d4-117">Requirement</span></span> | <span data-ttu-id="423d4-118">Wert</span><span class="sxs-lookup"><span data-stu-id="423d4-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="423d4-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="423d4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="423d4-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="423d4-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="423d4-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="423d4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="423d4-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="423d4-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="423d4-123">Header</span><span class="sxs-lookup"><span data-stu-id="423d4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="423d4-124"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="423d4-124"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="423d4-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="423d4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="423d4-126">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="423d4-126">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="423d4-127">**Ntgdiddkreatedirectdrawobject**</span><span class="sxs-lookup"><span data-stu-id="423d4-127">**NtGdiDdCreateDirectDrawObject**</span></span>](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> <dt>

[<span data-ttu-id="423d4-128">**Dddeletedirectdrawobject**</span><span class="sxs-lookup"><span data-stu-id="423d4-128">**DdDeleteDirectDrawObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-dddeletedirectdrawobject)
</dt> </dl>

 

 
