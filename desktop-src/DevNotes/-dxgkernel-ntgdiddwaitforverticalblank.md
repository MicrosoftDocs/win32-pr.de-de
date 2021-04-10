---
description: Gibt den vertikalen leeren Status des Geräts zurück.
ms.assetid: d09b684b-3482-424d-8a60-d123a65f9053
title: Ntgdiddwaitforverticalblank-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdWaitForVerticalBlank
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: d138480e4a45a2b2cb67ece44ab8ceb67efae72d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125917"
---
# <a name="ntgdiddwaitforverticalblank-function"></a><span data-ttu-id="fe5c7-103">Ntgdiddwaitforverticalblank-Funktion</span><span class="sxs-lookup"><span data-stu-id="fe5c7-103">NtGdiDdWaitForVerticalBlank function</span></span>

<span data-ttu-id="fe5c7-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="fe5c7-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="fe5c7-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="fe5c7-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="fe5c7-106">Gibt den vertikalen leeren Status des Geräts zurück.</span><span class="sxs-lookup"><span data-stu-id="fe5c7-106">Returns the vertical blank status of the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe5c7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe5c7-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdWaitForVerticalBlank(
  _In_    HANDLE                       hDirectDraw,
  _Inout_ PDD_WAITFORVERTICALBLANKDATA puWaitForVerticalBlankData
);
```



## <a name="parameters"></a><span data-ttu-id="fe5c7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe5c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe5c7-109">*hdirectdraw* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe5c7-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe5c7-110">Handle für das zuvor erstellte Kernel Modus-DirectDraw-Objekt.</span><span class="sxs-lookup"><span data-stu-id="fe5c7-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="fe5c7-111">*puwaitforverticalblankdata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fe5c7-111">*puWaitForVerticalBlankData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe5c7-112">Zeiger auf eine [**DD \_ waitforverticalblankdata**](/windows/win32/api/ddrawi/ns-ddrawi-ddhal_waitforverticalblankdata) -Struktur, die die Informationen enthält, die erforderlich sind, um den vertikalen leeren Status zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fe5c7-112">Pointer to a [**DD\_WAITFORVERTICALBLANKDATA**](/windows/win32/api/ddrawi/ns-ddrawi-ddhal_waitforverticalblankdata) structure that contains the information required to obtain the vertical blank status.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe5c7-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe5c7-113">Return value</span></span>

<span data-ttu-id="fe5c7-114">**Ntgdiddwaitforverticalblank** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="fe5c7-114">**NtGdiDdWaitForVerticalBlank** returns one of the following callback codes.</span></span>



| <span data-ttu-id="fe5c7-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="fe5c7-115">Return code</span></span>                                                                                              | <span data-ttu-id="fe5c7-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fe5c7-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fe5c7-117"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="fe5c7-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="fe5c7-118">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fe5c7-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="fe5c7-119">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="fe5c7-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="fe5c7-120">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="fe5c7-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="fe5c7-121"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="fe5c7-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="fe5c7-122">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="fe5c7-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="fe5c7-123">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="fe5c7-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="fe5c7-124">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="fe5c7-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fe5c7-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe5c7-125">Requirements</span></span>



| <span data-ttu-id="fe5c7-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe5c7-126">Requirement</span></span> | <span data-ttu-id="fe5c7-127">Wert</span><span class="sxs-lookup"><span data-stu-id="fe5c7-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fe5c7-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe5c7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fe5c7-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe5c7-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="fe5c7-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe5c7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fe5c7-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe5c7-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fe5c7-132">Header</span><span class="sxs-lookup"><span data-stu-id="fe5c7-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe5c7-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe5c7-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe5c7-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe5c7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe5c7-135">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="fe5c7-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
