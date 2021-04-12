---
description: Legt den Farbschlüssel Wert für die angegebene Oberfläche fest.
ms.assetid: 052dba97-c047-4ef7-a908-2a66ade3af10
title: Ntgdiddsetcolorkey-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetColorKey
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 7d6186df13ee88ca3de4f123381c012548b1cd85
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523003"
---
# <a name="ntgdiddsetcolorkey-function"></a><span data-ttu-id="c9300-103">Ntgdiddsetcolorkey-Funktion</span><span class="sxs-lookup"><span data-stu-id="c9300-103">NtGdiDdSetColorKey function</span></span>

<span data-ttu-id="c9300-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c9300-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="c9300-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="c9300-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="c9300-106">Legt den Farbschlüssel Wert für die angegebene Oberfläche fest.</span><span class="sxs-lookup"><span data-stu-id="c9300-106">Sets the color key value for the specified surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9300-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9300-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdSetColorKey(
  _In_    HANDLE              hSurface,
  _Inout_ PDD_SETCOLORKEYDATA puSetColorKeyData
);
```



## <a name="parameters"></a><span data-ttu-id="c9300-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9300-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9300-109">*hsurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9300-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9300-110">Ein Zeiger auf [**die \_ \_ lokale DD-Oberflächen**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) Struktur, die die Oberfläche beschreibt, der der Farbschlüssel zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c9300-110">Pointer to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the surface with which the color key is to be associated.</span></span>

</dd> <dt>

<span data-ttu-id="c9300-111">*pusetcolorkeydata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c9300-111">*puSetColorKeyData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9300-112">Ein Zeiger auf eine [**DD \_ setcolorkeydata**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setcolorkeydata) -Struktur, die die Informationen enthält, die erforderlich sind, um den Farbschlüssel für die angegebene Oberfläche festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c9300-112">Pointer to a [**DD\_SETCOLORKEYDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setcolorkeydata) structure that contains the information required to set the color key for the specified surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9300-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c9300-113">Return value</span></span>

<span data-ttu-id="c9300-114">**Ntgdiddsetcolorkey** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="c9300-114">**NtGdiDdSetColorKey** returns one of the following callback codes.</span></span>



| <span data-ttu-id="c9300-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c9300-115">Return code</span></span>                                                                                              | <span data-ttu-id="c9300-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9300-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c9300-117"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="c9300-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="c9300-118">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c9300-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="c9300-119">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="c9300-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="c9300-120">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="c9300-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="c9300-121"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="c9300-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="c9300-122">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="c9300-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="c9300-123">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="c9300-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="c9300-124">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c9300-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c9300-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9300-125">Requirements</span></span>



| <span data-ttu-id="c9300-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9300-126">Requirement</span></span> | <span data-ttu-id="c9300-127">Wert</span><span class="sxs-lookup"><span data-stu-id="c9300-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c9300-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c9300-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c9300-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9300-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="c9300-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c9300-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c9300-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9300-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c9300-132">Header</span><span class="sxs-lookup"><span data-stu-id="c9300-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9300-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9300-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9300-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9300-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9300-135">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="c9300-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
