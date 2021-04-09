---
description: Gibt den zuvor erstellten Gerätekontext (DC) für den angezeigten Kernel Modus-Microsoft DirectDraw Surface-Objekt frei.
ms.assetid: 98def2a1-878d-4776-a519-32cb70107338
title: Ntgdiddreleasedc-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdReleaseDC
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: a7319b423f12d7e4415d78d995bfb1d7cd0341a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860624"
---
# <a name="ntgdiddreleasedc-function"></a><span data-ttu-id="b4010-103">Ntgdiddreleasedc-Funktion</span><span class="sxs-lookup"><span data-stu-id="b4010-103">NtGdiDdReleaseDC function</span></span>

<span data-ttu-id="b4010-104">\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden.</span><span class="sxs-lookup"><span data-stu-id="b4010-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="b4010-105">Verwenden Sie stattdessen DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]</span><span class="sxs-lookup"><span data-stu-id="b4010-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="b4010-106">Gibt den zuvor erstellten Gerätekontext (DC) für den angezeigten Kernel Modus-Microsoft DirectDraw Surface-Objekt frei.</span><span class="sxs-lookup"><span data-stu-id="b4010-106">Releases the previously created device context (DC) for the indicated kernel-mode Microsoft DirectDraw surface object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4010-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4010-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdReleaseDC(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a><span data-ttu-id="b4010-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4010-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4010-109">*hsurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b4010-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4010-110">Handle für das zuvor erstellte Kernel Modus-DirectDraw-Oberflächen Objekt.</span><span class="sxs-lookup"><span data-stu-id="b4010-110">Handle to the previously created kernel-mode DirectDraw surface object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4010-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b4010-111">Return value</span></span>

<span data-ttu-id="b4010-112">Wenn erfolgreich, gibt diese Funktion **true** zurück. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b4010-112">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4010-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4010-113">Remarks</span></span>

<span data-ttu-id="b4010-114">Anwendungen, die einen Domänen Controller für eine DirectDraw-Oberfläche benötigen, können [IDirectDrawSurface7:: GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc)verwenden, die diese Funktionalität auf eine Weise unabhängig vom Betriebssystem verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="b4010-114">Applications that need to obtain a DC for a DirectDraw surface may use [IDirectDrawSurface7::GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc), which exposes this functionality in a manner independent of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4010-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4010-115">Requirements</span></span>



| <span data-ttu-id="b4010-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4010-116">Requirement</span></span> | <span data-ttu-id="b4010-117">Wert</span><span class="sxs-lookup"><span data-stu-id="b4010-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b4010-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b4010-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b4010-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b4010-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="b4010-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b4010-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b4010-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b4010-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b4010-122">Header</span><span class="sxs-lookup"><span data-stu-id="b4010-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4010-123"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4010-123"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4010-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4010-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4010-125">Unterstützung der untergeordneten Grafik Ebene</span><span class="sxs-lookup"><span data-stu-id="b4010-125">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="b4010-126">**Ddreleasedc**</span><span class="sxs-lookup"><span data-stu-id="b4010-126">**DdReleaseDC**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreleasedc)
</dt> </dl>

 

 
