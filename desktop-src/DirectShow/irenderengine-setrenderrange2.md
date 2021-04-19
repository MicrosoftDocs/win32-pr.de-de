---
description: Die SetRenderRange2-Methode legt den Zeitbereich auf der Zeitachse fest, der gerendert werden soll. Diese Methode entspricht dem Wert von "tyenderengine::-Trend Modul Range", aber nimmt Werte vom Typ "Double" an.
ms.assetid: 07df97a8-aa83-405d-91a0-45cd99185588
title: 'Unenderengine:: SetRenderRange2-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetRenderRange2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 555533b11c96073763af0d2b52823af44e3797be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358669"
---
# <a name="irenderenginesetrenderrange2-method"></a><span data-ttu-id="21a2b-104">Unenderengine:: SetRenderRange2-Methode</span><span class="sxs-lookup"><span data-stu-id="21a2b-104">IRenderEngine::SetRenderRange2 method</span></span>

> [!Note]  
> <span data-ttu-id="21a2b-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="21a2b-105">\[Deprecated.</span></span> <span data-ttu-id="21a2b-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="21a2b-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="21a2b-107">Die- `SetRenderRange2` Methode legt den Zeitbereich auf der Zeitachse fest, der gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="21a2b-107">The `SetRenderRange2` method sets the range of time on the timeline to be rendered.</span></span> <span data-ttu-id="21a2b-108">Diese Methode entspricht dem Wert von " [**tyenderengine::-Trend Modul Range**](irenderengine-setrenderrange.md)", aber nimmt Werte vom Typ " **Double**" an.</span><span class="sxs-lookup"><span data-stu-id="21a2b-108">This method is equivalent to [**IRenderEngine::SetRenderRange**](irenderengine-setrenderrange.md), but takes values of type **double**.</span></span>

## <a name="syntax"></a><span data-ttu-id="21a2b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="21a2b-109">Syntax</span></span>


```C++
HRESULT SetRenderRange2(
   double Start,
   double Stop
);
```



## <a name="parameters"></a><span data-ttu-id="21a2b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="21a2b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21a2b-111">*Starten*</span><span class="sxs-lookup"><span data-stu-id="21a2b-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="21a2b-112">Startzeit in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="21a2b-112">Start time, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="21a2b-113">*Beenden*</span><span class="sxs-lookup"><span data-stu-id="21a2b-113">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="21a2b-114">Endzeit in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="21a2b-114">Stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21a2b-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="21a2b-115">Return value</span></span>

<span data-ttu-id="21a2b-116">Gibt einen der folgenden **HRESULT** -Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="21a2b-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="21a2b-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="21a2b-117">Return code</span></span>                                                                                            | <span data-ttu-id="21a2b-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="21a2b-118">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="21a2b-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="21a2b-119"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="21a2b-120">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="21a2b-120">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="21a2b-121"><dt>**E \_ muss \_ Init \_ Renderer**</dt></span><span class="sxs-lookup"><span data-stu-id="21a2b-121"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="21a2b-122">Fehler beim Initialisieren der Rendering-Engine.</span><span class="sxs-lookup"><span data-stu-id="21a2b-122">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="21a2b-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21a2b-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="21a2b-124">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="21a2b-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="21a2b-125">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="21a2b-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="21a2b-126">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="21a2b-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="21a2b-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21a2b-127">Requirements</span></span>



| <span data-ttu-id="21a2b-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21a2b-128">Requirement</span></span> | <span data-ttu-id="21a2b-129">Wert</span><span class="sxs-lookup"><span data-stu-id="21a2b-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21a2b-130">Header</span><span class="sxs-lookup"><span data-stu-id="21a2b-130">Header</span></span><br/>  | <dl> <span data-ttu-id="21a2b-131"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="21a2b-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="21a2b-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="21a2b-132">Library</span></span><br/> | <dl> <span data-ttu-id="21a2b-133"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="21a2b-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21a2b-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21a2b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21a2b-135">**Schnittstelle ""**</span><span class="sxs-lookup"><span data-stu-id="21a2b-135">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="21a2b-136">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="21a2b-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




