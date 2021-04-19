---
description: Benachrichtigt den Treiber, wenn eine Microsoft DirectDraw-Anwendung zum oder aus dem exklusiven Modus wechselt.
ms.assetid: f2b63d90-7ede-479f-a2fd-ae9870c4d7b9
title: Ntgdiddabtexclusivemode-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetExclusiveMode
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 1d2420f4ae093b4bfc3f68871daefd5c20da308e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346007"
---
# <a name="ntgdiddsetexclusivemode-function"></a><span data-ttu-id="e43c1-103">Ntgdiddabtexclusivemode-Funktion</span><span class="sxs-lookup"><span data-stu-id="e43c1-103">NtGdiDdSetExclusiveMode function</span></span>

<span data-ttu-id="e43c1-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="e43c1-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="e43c1-105">Verwenden Sie stattdessen DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="e43c1-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="e43c1-106">Benachrichtigt den Treiber, wenn eine Microsoft DirectDraw-Anwendung zum oder aus dem exklusiven Modus wechselt.</span><span class="sxs-lookup"><span data-stu-id="e43c1-106">Notifies the driver when a Microsoft DirectDraw application is switching to or from exclusive mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="e43c1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e43c1-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdSetExclusiveMode(
  _In_    HANDLE                   hDirectDraw,
  _Inout_ PDD_SETEXCLUSIVEMODEDATA puSetExclusiveModeData
);
```



## <a name="parameters"></a><span data-ttu-id="e43c1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e43c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e43c1-109">*hdirectdraw* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e43c1-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e43c1-110">Handle für das zuvor erstellte Kernel Modus-DirectDraw-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e43c1-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="e43c1-111">*puabtexclusivemodedata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e43c1-111">*puSetExclusiveModeData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e43c1-112">Zeiger auf eine [**DD- \_ texclusivemodedata**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setexclusivemodedata) -Struktur, die die Benachrichtigungs Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="e43c1-112">Pointer to a [**DD\_SETEXCLUSIVEMODEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setexclusivemodedata) structure that contains the notification information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e43c1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e43c1-113">Return value</span></span>

<span data-ttu-id="e43c1-114">**Ntgdiddabtexclusivemode** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="e43c1-114">**NtGdiDdSetExclusiveMode** returns one of the following callback codes.</span></span>



| <span data-ttu-id="e43c1-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e43c1-115">Return code</span></span>                                                                                              | <span data-ttu-id="e43c1-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e43c1-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e43c1-117"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="e43c1-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="e43c1-118">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e43c1-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="e43c1-119">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="e43c1-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="e43c1-120">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="e43c1-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="e43c1-121"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="e43c1-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="e43c1-122">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="e43c1-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="e43c1-123">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="e43c1-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="e43c1-124">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e43c1-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e43c1-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e43c1-125">Requirements</span></span>



| <span data-ttu-id="e43c1-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e43c1-126">Requirement</span></span> | <span data-ttu-id="e43c1-127">Wert</span><span class="sxs-lookup"><span data-stu-id="e43c1-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e43c1-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e43c1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e43c1-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e43c1-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e43c1-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e43c1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e43c1-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e43c1-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e43c1-132">Header</span><span class="sxs-lookup"><span data-stu-id="e43c1-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e43c1-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e43c1-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e43c1-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e43c1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e43c1-135">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="e43c1-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
