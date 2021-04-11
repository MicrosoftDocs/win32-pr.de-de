---
description: Benachrichtigt den Treiber, dass ein Software Decoder mit der Verwendung der Motion-Kompensierung mit der angegebenen GUID beginnt.
ms.assetid: c9a55428-7fe6-45dd-987a-d9ab8ae8a1cb
title: Ntgdiddkreatemocomp-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateMoComp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: f1705b5bf7ac5eddd1ac39e14f3b91b7fd3728cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126632"
---
# <a name="ntgdiddcreatemocomp-function"></a><span data-ttu-id="b6bc3-103">Ntgdiddkreatemocomp-Funktion</span><span class="sxs-lookup"><span data-stu-id="b6bc3-103">NtGdiDdCreateMoComp function</span></span>

<span data-ttu-id="b6bc3-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="b6bc3-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="b6bc3-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="b6bc3-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="b6bc3-106">Benachrichtigt den Treiber, dass ein Software Decoder mit der Verwendung der Motion-Kompensierung mit der angegebenen GUID beginnt.</span><span class="sxs-lookup"><span data-stu-id="b6bc3-106">Notifies the driver that a software decoder will start using motion compensation with the specified GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6bc3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6bc3-107">Syntax</span></span>


```C++
HANDLE APIENTRY NtGdiDdCreateMoComp(
  _In_    HANDLE               hDirectDraw,
  _Inout_ PDD_CREATEMOCOMPDATA puCreateMoCompData
);
```



## <a name="parameters"></a><span data-ttu-id="b6bc3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6bc3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6bc3-109">*hdirectdraw* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6bc3-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6bc3-110">Handle für ein zuvor erstelltes DirectDraw-kernelmodusobjekt für das Gerät, für das die Motion-Kompensierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b6bc3-110">Handle to a previously created DirectDraw kernel-mode object for the device on which motion compensation is to be used.</span></span>

</dd> <dt>

<span data-ttu-id="b6bc3-111">*pukreatemocompdata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b6bc3-111">*puCreateMoCompData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6bc3-112">Ein Zeiger auf eine DD-Struktur [**\_ emocompdata**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createmocompdata) , die die Informationen enthält, die für die Verwendung der Motion-Kompensierung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="b6bc3-112">Pointer to a [**DD\_CREATEMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createmocompdata) structure that contains the information required to begin using motion compensation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6bc3-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b6bc3-113">Return value</span></span>

<span data-ttu-id="b6bc3-114">**Ntgdiddkreatemocomp** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="b6bc3-114">**NtGdiDdCreateMoComp** returns one of the following callback codes.</span></span>



| <span data-ttu-id="b6bc3-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b6bc3-115">Return code</span></span>                                                                                              | <span data-ttu-id="b6bc3-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b6bc3-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b6bc3-117"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="b6bc3-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="b6bc3-118">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b6bc3-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="b6bc3-119">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="b6bc3-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="b6bc3-120">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="b6bc3-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="b6bc3-121"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="b6bc3-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="b6bc3-122">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="b6bc3-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="b6bc3-123">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="b6bc3-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="b6bc3-124">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="b6bc3-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b6bc3-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6bc3-125">Remarks</span></span>

<span data-ttu-id="b6bc3-126">Weitere Informationen finden Sie im Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="b6bc3-126">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6bc3-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6bc3-127">Requirements</span></span>



| <span data-ttu-id="b6bc3-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6bc3-128">Requirement</span></span> | <span data-ttu-id="b6bc3-129">Wert</span><span class="sxs-lookup"><span data-stu-id="b6bc3-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b6bc3-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b6bc3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b6bc3-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6bc3-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="b6bc3-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b6bc3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b6bc3-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6bc3-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b6bc3-134">Header</span><span class="sxs-lookup"><span data-stu-id="b6bc3-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6bc3-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6bc3-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6bc3-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6bc3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6bc3-137">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="b6bc3-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
