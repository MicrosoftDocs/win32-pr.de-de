---
description: Erstellt eine Microsoft Direct3D-Oberfläche aus einer Microsoft DirectDraw-Oberfläche und ordnet ihr einen angeforderten handle-Wert zu.
ms.assetid: 7b1ce714-a56e-4508-8160-af8c1748c5f7
title: Ntgdiddkreatesurfaceex-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurfaceEx
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 8aad613762773e466fb83eadf689b7703a8c4198
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125941"
---
# <a name="ntgdiddcreatesurfaceex-function"></a><span data-ttu-id="17684-103">Ntgdiddkreatesurfaceex-Funktion</span><span class="sxs-lookup"><span data-stu-id="17684-103">NtGdiDdCreateSurfaceEx function</span></span>

<span data-ttu-id="17684-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="17684-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="17684-105">Verwenden Sie stattdessen DirectDraw und Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="17684-105">Instead, use the DirectDraw and Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="17684-106">Erstellt eine Microsoft Direct3D-Oberfläche aus einer Microsoft DirectDraw-Oberfläche und ordnet ihr einen angeforderten handle-Wert zu.</span><span class="sxs-lookup"><span data-stu-id="17684-106">Creates a Microsoft Direct3D surface from a Microsoft DirectDraw surface and associates a requested handle value to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="17684-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="17684-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCreateSurfaceEx(
  _In_ HANDLE hDirectDraw,
  _In_ HANDLE hSurface,
  _In_ DWORD  dwSurfaceHandle
);
```



## <a name="parameters"></a><span data-ttu-id="17684-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="17684-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17684-109">*hdirectdraw* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="17684-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17684-110">Handle für das von der Anwendung erstellte DirectDraw-Objekt.</span><span class="sxs-lookup"><span data-stu-id="17684-110">Handle to the DirectDraw object created by the application.</span></span>

</dd> <dt>

<span data-ttu-id="17684-111">*hsurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="17684-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17684-112">Handle für die DirectDraw-Oberfläche, die für Direct3D erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="17684-112">Handle to the DirectDraw surface to be created for Direct3D.</span></span> <span data-ttu-id="17684-113">Diese Handles sind innerhalb jeder anderen [**DD \_ DirectDraw- \_ lokalen**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_local) Struktur eindeutig.</span><span class="sxs-lookup"><span data-stu-id="17684-113">These handles are unique within each different [**DD\_DIRECTDRAW\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_local) structure.</span></span>

</dd> <dt>

<span data-ttu-id="17684-114">*dwsurfakehandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="17684-114">*dwSurfaceHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17684-115">Handle für eine DD-Struktur von " [**\_ foatesurfaceexdata**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfaceexdata) ", die die Informationen enthält, die der Treiber zum Erstellen der Oberfläche benötigt.</span><span class="sxs-lookup"><span data-stu-id="17684-115">Handle to a [**DD\_CREATESURFACEEXDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfaceexdata) structure that contains the information required for the driver to create the surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17684-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="17684-116">Return value</span></span>

<span data-ttu-id="17684-117">**Ntgdiddkreatesurfaceex** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="17684-117">**NtGdiDdCreateSurfaceEx** returns one of the following callback codes.</span></span>



| <span data-ttu-id="17684-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="17684-118">Return code</span></span>                                                                                              | <span data-ttu-id="17684-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17684-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="17684-120"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="17684-120"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="17684-121">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="17684-121">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="17684-122">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="17684-122">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="17684-123">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="17684-123">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="17684-124"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="17684-124"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="17684-125">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="17684-125">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="17684-126">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="17684-126">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="17684-127">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="17684-127">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="17684-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17684-128">Requirements</span></span>



| <span data-ttu-id="17684-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17684-129">Requirement</span></span> | <span data-ttu-id="17684-130">Wert</span><span class="sxs-lookup"><span data-stu-id="17684-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="17684-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="17684-131">Minimum supported client</span></span><br/> | <span data-ttu-id="17684-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17684-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="17684-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="17684-133">Minimum supported server</span></span><br/> | <span data-ttu-id="17684-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17684-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="17684-135">Header</span><span class="sxs-lookup"><span data-stu-id="17684-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="17684-136"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="17684-136"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17684-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17684-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17684-138">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="17684-138">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
