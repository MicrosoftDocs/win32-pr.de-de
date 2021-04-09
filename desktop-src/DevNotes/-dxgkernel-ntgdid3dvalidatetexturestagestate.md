---
description: Gibt die Anzahl von Durchläufen zurück, bei denen die Hardware die im aktuellen Zustand angegebenen Mischungs Vorgänge ausführen kann.
ms.assetid: 355dae78-cd65-4fc9-8f08-8e5ae123064b
title: NtGdiD3DValidateTextureStageState-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DValidateTextureStageState
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: 37c852343c70c5d3325926c9108dcab2948fdc95
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860815"
---
# <a name="ntgdid3dvalidatetexturestagestate-function"></a><span data-ttu-id="bb3f3-103">NtGdiD3DValidateTextureStageState-Funktion</span><span class="sxs-lookup"><span data-stu-id="bb3f3-103">NtGdiD3DValidateTextureStageState function</span></span>

<span data-ttu-id="bb3f3-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="bb3f3-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="bb3f3-105">Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="bb3f3-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="bb3f3-106">Gibt die Anzahl von Durchläufen zurück, bei denen die Hardware die im aktuellen Zustand angegebenen Mischungs Vorgänge ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="bb3f3-106">Returns the number of passes where the hardware can perform the blending operations specified in the current state.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb3f3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb3f3-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DValidateTextureStageState(
  _Inout_ LPD3DNTHAL_VALIDATETEXTURESTAGESTATEDATA pData
);
```



## <a name="parameters"></a><span data-ttu-id="bb3f3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb3f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb3f3-109">*pData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bb3f3-109">*pData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb3f3-110">Ein Zeiger auf eine [**D3DNTHAL \_ validatetexturestagestatedata**](/windows-hardware/drivers/ddi/) -Struktur, die die Informationen enthält, die der Treiber zum Ermitteln und Zurückgeben der Anzahl der zum Durchführen der Mischungs Vorgänge erforderlichen Durchläufen benötigt.</span><span class="sxs-lookup"><span data-stu-id="bb3f3-110">Pointer to a [**D3DNTHAL\_VALIDATETEXTURESTAGESTATEDATA**](/windows-hardware/drivers/ddi/) structure that contains the information required for the driver to determine and return the number of passes required to perform the blending operations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb3f3-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb3f3-111">Return value</span></span>

<span data-ttu-id="bb3f3-112">**NtGdiD3DValidateTextureStageState** gibt einen der folgenden Rückruf Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="bb3f3-112">**NtGdiD3DValidateTextureStageState** returns one of the following callback codes.</span></span>



| <span data-ttu-id="bb3f3-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="bb3f3-113">Return code</span></span>                                                                                              | <span data-ttu-id="bb3f3-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb3f3-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bb3f3-115"><dt>**ddhal- \_ Treiber \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="bb3f3-115"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="bb3f3-116">Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bb3f3-116">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="bb3f3-117">Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort.</span><span class="sxs-lookup"><span data-stu-id="bb3f3-117">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="bb3f3-118">Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="bb3f3-118">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="bb3f3-119"><dt>**ddhal- \_ Treiber \_ nothandled**</dt></span><span class="sxs-lookup"><span data-stu-id="bb3f3-119"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="bb3f3-120">Der Treiber hat keinen Kommentar zum angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="bb3f3-120">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="bb3f3-121">Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="bb3f3-121">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="bb3f3-122">Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="bb3f3-122">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bb3f3-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb3f3-123">Requirements</span></span>



| <span data-ttu-id="bb3f3-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb3f3-124">Requirement</span></span> | <span data-ttu-id="bb3f3-125">Wert</span><span class="sxs-lookup"><span data-stu-id="bb3f3-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bb3f3-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb3f3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bb3f3-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb3f3-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="bb3f3-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb3f3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bb3f3-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb3f3-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bb3f3-130">Header</span><span class="sxs-lookup"><span data-stu-id="bb3f3-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb3f3-131"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb3f3-131"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb3f3-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb3f3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb3f3-133">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="bb3f3-133">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
