---
description: Die setdynamikreconnectlevel-Methode legt die Ebene der dynamischen erneuten Verbindung während des Renderings fest.
ms.assetid: 092f3464-84a2-48b0-9647-66fe27e9706d
title: 'Unenderengine:: setdynamikreconnectlevel-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetDynamicReconnectLevel
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ae02fb6158b58cd5785aa7df539651acfbea5db8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368662"
---
# <a name="irenderenginesetdynamicreconnectlevel-method"></a><span data-ttu-id="913d0-103">Unenderengine:: setdynamikreconnectlevel-Methode</span><span class="sxs-lookup"><span data-stu-id="913d0-103">IRenderEngine::SetDynamicReconnectLevel method</span></span>

> [!Note]  
> <span data-ttu-id="913d0-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="913d0-104">\[Deprecated.</span></span> <span data-ttu-id="913d0-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="913d0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="913d0-106">Die- `SetDynamicReconnectLevel` Methode legt die Ebene der dynamischen erneuten Verbindung während des Renderings fest.</span><span class="sxs-lookup"><span data-stu-id="913d0-106">The `SetDynamicReconnectLevel` method sets the level of dynamic reconnection during rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="913d0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="913d0-107">Syntax</span></span>


```C++
HRESULT SetDynamicReconnectLevel(
   DWORD Level
);
```



## <a name="parameters"></a><span data-ttu-id="913d0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="913d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="913d0-109">*Level*</span><span class="sxs-lookup"><span data-stu-id="913d0-109">*Level*</span></span> 
</dt> <dd>

<span data-ttu-id="913d0-110">Kombination [**dynamischer reverbindungsflags**](dynamic-reconnection-flags.md), die die Ebene der dynamischen erneuten Verbindung angeben.</span><span class="sxs-lookup"><span data-stu-id="913d0-110">Combination of [**Dynamic Reconnection Flags**](dynamic-reconnection-flags.md), specifying the level of dynamic reconnection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="913d0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="913d0-111">Return value</span></span>

<span data-ttu-id="913d0-112">Gibt einen der folgenden **HRESULT** -Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="913d0-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="913d0-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="913d0-113">Return code</span></span>                                                                               | <span data-ttu-id="913d0-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="913d0-114">Description</span></span>                 |
|-------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <span data-ttu-id="913d0-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="913d0-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="913d0-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="913d0-116">Success.</span></span><br/>         |
| <dl> <span data-ttu-id="913d0-117"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="913d0-117"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="913d0-118">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="913d0-118">Not implemented.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="913d0-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="913d0-119">Remarks</span></span>

<span data-ttu-id="913d0-120">Standardmäßig lädt die einfache Renderingengine jede Quelle, bevor ein Projekt gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="913d0-120">By default, the basic render engine loads every source before rendering a project.</span></span> <span data-ttu-id="913d0-121">Dies kann zu einer langen Start Zeit führen.</span><span class="sxs-lookup"><span data-stu-id="913d0-121">This can result in a long start-up time.</span></span> <span data-ttu-id="913d0-122">Bei der dynamischen erneuten Verbindungs Herstellung werden Quellen nur bei Bedarf geladen.</span><span class="sxs-lookup"><span data-stu-id="913d0-122">With dynamic reconnection, sources are loaded only when needed.</span></span> <span data-ttu-id="913d0-123">Dies kann die Startzeit verkürzen, aber möglicherweise die reibungslose Wiedergabe beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="913d0-123">This can shorten the start-up time, but possibly interfere with smooth playback.</span></span> <span data-ttu-id="913d0-124">Im Allgemeinen können Sie von der dynamischen erneuten Verbindung profitieren, umso mehr Quell Clips werden von einem Projekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="913d0-124">Generally, the more source clips that a project uses, the more you might benefit from dynamic reconnection.</span></span>

<span data-ttu-id="913d0-125">Diese Methode wird von der Smart-Rendering-Engine nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="913d0-125">The smart render engine does not implement this method.</span></span>

> [!Note]  
> <span data-ttu-id="913d0-126">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="913d0-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="913d0-127">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="913d0-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="913d0-128">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="913d0-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="913d0-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="913d0-129">Requirements</span></span>



| <span data-ttu-id="913d0-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="913d0-130">Requirement</span></span> | <span data-ttu-id="913d0-131">Wert</span><span class="sxs-lookup"><span data-stu-id="913d0-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="913d0-132">Header</span><span class="sxs-lookup"><span data-stu-id="913d0-132">Header</span></span><br/>  | <dl> <span data-ttu-id="913d0-133"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="913d0-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="913d0-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="913d0-134">Library</span></span><br/> | <dl> <span data-ttu-id="913d0-135"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="913d0-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="913d0-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="913d0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="913d0-137">**Schnittstelle ""**</span><span class="sxs-lookup"><span data-stu-id="913d0-137">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="913d0-138">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="913d0-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




