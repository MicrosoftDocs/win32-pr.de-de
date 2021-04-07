---
title: Imediarendererfactory-Methode "kreatemediarendererasync"
description: Erstellt asynchron eine neue Instanz eines Objekts, das die imediarenderer-Schnittstelle mit dem angegebenen eindeutigen Gerätenamen (User Name, udn) implementiert.
ms.assetid: FD1242F8-4C2E-4027-B1DE-5FD69557684C
keywords:
- Methode für die Media Streaming-API von "kreatemediarendererasync"
- Methode "Media Streaming API" der Methode "kreatemediarendererasync", imediarendererfactory-Schnittstelle
- Imediarendererfactory-Schnittstelle Medien Streaming-API, Methode "kreatemediarendererasync"
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b152e5889ad83440a48e178be0b89a97d2a9f664
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725881"
---
# <a name="imediarendererfactorycreatemediarendererasync-method"></a><span data-ttu-id="6b2dc-106">Imediarendererfactory:: kreatemediarendererasync-Methode</span><span class="sxs-lookup"><span data-stu-id="6b2dc-106">IMediaRendererFactory::CreateMediaRendererAsync method</span></span>

<span data-ttu-id="6b2dc-107">Erstellt asynchron eine neue Instanz eines Objekts, das die [**imediarenderer**](imediarenderer.md) -Schnittstelle mit dem angegebenen eindeutigen Gerätenamen (User Name, udn) implementiert.</span><span class="sxs-lookup"><span data-stu-id="6b2dc-107">Asynchronously creates a new instance of an object that implements the [**IMediaRenderer**](imediarenderer.md) interface using the specified Unique Device Name (UDN).</span></span>

## <a name="syntax"></a><span data-ttu-id="6b2dc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b2dc-108">Syntax</span></span>


```C++
HRESULT CreateMediaRendererAsync(
  [in]          HSTRING                      deviceIdentifier,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="6b2dc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b2dc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b2dc-110">Geräte Bezeichner  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b2dc-110">*deviceIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b2dc-111">Ein hstring-Wert, der einen udn enthält, der das DLNA-DMR-Gerät identifiziert, für das eine Instanz von [**imediarenderer**](imediarenderer.md) erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="6b2dc-111">An HSTRING containing a UDN that identifies the DLNA DMR device for which an instance of [**IMediaRenderer**](imediarenderer.md) will be created.</span></span>

</dd> <dt>

<span data-ttu-id="6b2dc-112">*Wert* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="6b2dc-112">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6b2dc-113">Empfängt einen Verweis auf ein Objekt vom Typ " [**kreatemediarendereroperation**](createmediarendereroperation.md) ", das verwendet wird, um Ergebnisse aus dem asynchronen Vorgang zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6b2dc-113">Receives a reference to a [**CreateMediaRendererOperation**](createmediarendereroperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b2dc-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b2dc-114">Return value</span></span>

<span data-ttu-id="6b2dc-115">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="6b2dc-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6b2dc-116">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6b2dc-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6b2dc-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6b2dc-117">Return code</span></span>                                                                          | <span data-ttu-id="6b2dc-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6b2dc-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6b2dc-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6b2dc-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6b2dc-120">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6b2dc-120">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="6b2dc-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b2dc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b2dc-122">**Imediarendererfactory**</span><span class="sxs-lookup"><span data-stu-id="6b2dc-122">**IMediaRendererFactory**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

