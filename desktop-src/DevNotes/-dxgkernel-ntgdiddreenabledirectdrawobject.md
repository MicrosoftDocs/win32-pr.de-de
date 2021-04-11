---
description: Aktiviert ein Microsoft DirectDraw-kernelmodusobjekt nach einem Modusschalter erneut.
ms.assetid: 26451881-cebf-4db1-aeed-365f0dae6704
title: Ntgdiddreenabledirectdrawobject-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdReenableDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: afd736317ecdf802cb418e81063b622db43f0651
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127284"
---
# <a name="ntgdiddreenabledirectdrawobject-function"></a><span data-ttu-id="f9e32-103">Ntgdiddreenabledirectdrawobject-Funktion</span><span class="sxs-lookup"><span data-stu-id="f9e32-103">NtGdiDdReenableDirectDrawObject function</span></span>

<span data-ttu-id="f9e32-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="f9e32-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="f9e32-105">Verwenden Sie stattdessen DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="f9e32-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="f9e32-106">Aktiviert ein Microsoft DirectDraw-kernelmodusobjekt nach einem Modusschalter erneut.</span><span class="sxs-lookup"><span data-stu-id="f9e32-106">Re-enables a Microsoft DirectDraw kernel-mode device object after a mode switch.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9e32-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9e32-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdReenableDirectDrawObject(
  _In_    HANDLE hDirectDrawLocal,
  _Inout_ BOOL   *pubNewMode
);
```



## <a name="parameters"></a><span data-ttu-id="f9e32-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9e32-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9e32-109">*hdirectdrawlocal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f9e32-109">*hDirectDrawLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9e32-110">Das DirectDraw-Objekt, das erneut aktiviert werden muss.</span><span class="sxs-lookup"><span data-stu-id="f9e32-110">DirectDraw object that needs to be re-enabled.</span></span>

</dd> <dt>

<span data-ttu-id="f9e32-111">*pubnewmode* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f9e32-111">*pubNewMode* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9e32-112">Ein Zeiger auf einen booleschen Wert, der mit einem Wert aufgefüllt wird, der angibt, ob sich der Anzeigemodus geändert hat.</span><span class="sxs-lookup"><span data-stu-id="f9e32-112">Pointer to a BOOL that will be filled with a value that represents whether the display mode changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9e32-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9e32-113">Return value</span></span>

<span data-ttu-id="f9e32-114">Bei erfolgreicher Ausführung (das Gerät kann erneut aktiviert werden) gibt diese Funktion " **true**" zurück.</span><span class="sxs-lookup"><span data-stu-id="f9e32-114">If successful (the device can be re-enabled), this function returns **TRUE**.</span></span> <span data-ttu-id="f9e32-115">Andernfalls (z. b. wurde der Anzeigetreiber geändert), wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f9e32-115">Otherwise (for example, the display driver was changed), it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9e32-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9e32-116">Remarks</span></span>

<span data-ttu-id="f9e32-117">Nachdem das Objekt erneut aktiviert wurde, können die Funktionen für das Gerät über einen [**ntgdiddquerydirectdrawobject**](-dxgkernel-ntgdiddquerydirectdrawobject.md)-Befehl erneut abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="f9e32-117">Once the object has been re-enabled, the capabilities for the device can be re-queried via a call to [**NtGdiDdQueryDirectDrawObject**](-dxgkernel-ntgdiddquerydirectdrawobject.md).</span></span>

<span data-ttu-id="f9e32-118">Anwendungen wird empfohlen, die DirectDraw-oder [Direct3D](../direct3d10/d3d10-graphics-reference.md) -APIs zu verwenden, die diesen Prozess unabhängig vom Betriebssystem automatisieren und abstrahieren.</span><span class="sxs-lookup"><span data-stu-id="f9e32-118">Applications are advised to use the DirectDraw or [Direct3D](../direct3d10/d3d10-graphics-reference.md) version 8 APIs, which automate and abstract this process in a manner independent of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9e32-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9e32-119">Requirements</span></span>



| <span data-ttu-id="f9e32-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9e32-120">Requirement</span></span> | <span data-ttu-id="f9e32-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f9e32-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f9e32-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9e32-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f9e32-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9e32-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="f9e32-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9e32-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f9e32-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9e32-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f9e32-126">Header</span><span class="sxs-lookup"><span data-stu-id="f9e32-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9e32-127"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9e32-127"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9e32-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9e32-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9e32-129">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="f9e32-129">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="f9e32-130">**Ddreenabledirectdrawobject**</span><span class="sxs-lookup"><span data-stu-id="f9e32-130">**DdReenableDirectDrawObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreenabledirectdrawobject)
</dt> </dl>

 

 
