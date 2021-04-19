---
description: Die setrenderrange-Methode legt den Zeitbereich auf der Zeitachse fest, der gerendert werden soll. Objekte, die sich außerhalb des angegebenen Bereichs befinden, werden nicht gerendert, und Ressourcen werden nicht zugeordnet.
ms.assetid: 2dcdca6b-2bae-4a27-bfbc-19a9b2ea633a
title: "\"Unenderengine:: *\"-Methode (\"qedit. h\")"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetRenderRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e715c2c0077a890948cfd5f5026afe98633325ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369176"
---
# <a name="irenderenginesetrenderrange-method"></a><span data-ttu-id="17451-104">"Unenderengine:: \*"-Methode</span><span class="sxs-lookup"><span data-stu-id="17451-104">IRenderEngine::SetRenderRange method</span></span>

> [!Note]  
> <span data-ttu-id="17451-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="17451-105">\[Deprecated.</span></span> <span data-ttu-id="17451-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="17451-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="17451-107">Die- `SetRenderRange` Methode legt den Zeitbereich auf der Zeitachse fest, der gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="17451-107">The `SetRenderRange` method sets the range of time on the timeline to be rendered.</span></span> <span data-ttu-id="17451-108">Objekte, die sich außerhalb des angegebenen Bereichs befinden, werden nicht gerendert, und Ressourcen werden nicht zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="17451-108">Objects that lie outside the specified range are not rendered, and resources are not allocated for them.</span></span>

## <a name="syntax"></a><span data-ttu-id="17451-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="17451-109">Syntax</span></span>


```C++
HRESULT SetRenderRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="17451-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="17451-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17451-111">*Starten*</span><span class="sxs-lookup"><span data-stu-id="17451-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="17451-112">Startzeit in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="17451-112">Start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="17451-113">*Beenden*</span><span class="sxs-lookup"><span data-stu-id="17451-113">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="17451-114">Endzeit in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="17451-114">Stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17451-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="17451-115">Return value</span></span>

<span data-ttu-id="17451-116">Gibt einen der folgenden **HRESULT** -Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="17451-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="17451-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="17451-117">Return code</span></span>                                                                                            | <span data-ttu-id="17451-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17451-118">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="17451-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="17451-119"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="17451-120">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="17451-120">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="17451-121"><dt>**E \_ muss \_ Init \_ Renderer**</dt></span><span class="sxs-lookup"><span data-stu-id="17451-121"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="17451-122">Fehler beim Initialisieren der Rendering-Engine.</span><span class="sxs-lookup"><span data-stu-id="17451-122">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="17451-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17451-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="17451-124">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="17451-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="17451-125">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="17451-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="17451-126">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="17451-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="17451-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17451-127">Requirements</span></span>



| <span data-ttu-id="17451-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17451-128">Requirement</span></span> | <span data-ttu-id="17451-129">Wert</span><span class="sxs-lookup"><span data-stu-id="17451-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17451-130">Header</span><span class="sxs-lookup"><span data-stu-id="17451-130">Header</span></span><br/>  | <dl> <span data-ttu-id="17451-131"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="17451-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="17451-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="17451-132">Library</span></span><br/> | <dl> <span data-ttu-id="17451-133"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="17451-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17451-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17451-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17451-135">**Schnittstelle ""**</span><span class="sxs-lookup"><span data-stu-id="17451-135">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="17451-136">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="17451-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




