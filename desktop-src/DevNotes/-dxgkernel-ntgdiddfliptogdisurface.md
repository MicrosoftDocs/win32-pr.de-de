---
description: Benachrichtigt den Treiber, wenn Microsoft DirectDraw in eine oder aus einer Windows Graphics Device Interface (GDI)-Oberfläche gekippt wird.
ms.assetid: e79be33a-24bc-477b-bc67-395fff74309c
title: Ntgdiddflipumgdisurface-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdFlipToGDISurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 7e233bddf72c79507eab1fcefbf3de66460d228e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126757"
---
# <a name="ntgdiddfliptogdisurface-function"></a><span data-ttu-id="f5372-103">Ntgdiddflipumgdisurface-Funktion</span><span class="sxs-lookup"><span data-stu-id="f5372-103">NtGdiDdFlipToGDISurface function</span></span>

<span data-ttu-id="f5372-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="f5372-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="f5372-105">Verwenden Sie stattdessen DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="f5372-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="f5372-106">Benachrichtigt den Treiber, wenn Microsoft DirectDraw in eine oder aus einer Windows Graphics Device Interface (GDI)-Oberfläche gekippt wird.</span><span class="sxs-lookup"><span data-stu-id="f5372-106">Notifies the driver when Microsoft DirectDraw is flipping to or from a Windows Graphics Device Interface (GDI) surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5372-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5372-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdFlipToGDISurface(
  _In_    HANDLE                   hDirectDraw,
  _Inout_ PDD_FLIPTOGDISURFACEDATA puFlipToGDISurfaceData
);
```



## <a name="parameters"></a><span data-ttu-id="f5372-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5372-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5372-109">*hdirectdraw* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5372-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5372-110">Handle für das zuvor erstellte Kernel Modus-DirectDraw-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f5372-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="f5372-111">*puflipabgdisurfacedata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f5372-111">*puFlipToGDISurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5372-112">Zeiger auf eine [DD \_ flipdegdisurfacedata](https://msdn.microsoft.com/library/ms793922.aspx) -Struktur, die die Benachrichtigungs Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="f5372-112">Pointer to a [DD\_FLIPTOGDISURFACEDATA](https://msdn.microsoft.com/library/ms793922.aspx) structure that contains the notification information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5372-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f5372-113">Return value</span></span>

<span data-ttu-id="f5372-114">**Ntgdiddflipfligdisurface** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="f5372-114">**NtGdiDdFlipToGDISurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="f5372-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f5372-115">Return code</span></span>                                                                                              | <span data-ttu-id="f5372-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5372-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f5372-117"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="f5372-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="f5372-118">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f5372-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="f5372-119">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="f5372-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="f5372-120">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="f5372-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="f5372-121"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="f5372-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="f5372-122">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="f5372-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="f5372-123">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="f5372-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="f5372-124">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f5372-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f5372-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5372-125">Requirements</span></span>



| <span data-ttu-id="f5372-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5372-126">Requirement</span></span> | <span data-ttu-id="f5372-127">Wert</span><span class="sxs-lookup"><span data-stu-id="f5372-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f5372-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f5372-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f5372-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5372-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="f5372-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f5372-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f5372-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5372-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f5372-132">Header</span><span class="sxs-lookup"><span data-stu-id="f5372-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5372-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5372-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5372-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5372-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5372-135">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="f5372-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




