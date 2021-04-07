---
title: Imediarendererfactory-Methode "kreatemediarendererfrombasicdeviceasync"
description: Erstellt asynchron eine neue Instanz eines Objekts, das die imediarenderer-Schnittstelle mithilfe der angegebenen ibasicdevice-Schnittstelle implementiert.
ms.assetid: 14A83789-0F3C-467B-8EFD-3BB421C54217
keywords:
- Methode "kreatemediarendererfrombasicdeviceasync" Medien Streaming-API
- Methode "kreatemediarendererfrombasicdeviceasync" Media Streaming API, imediarendererfactory-Schnittstelle
- Imediarendererfactory-Schnittstelle Medien Streaming-API, Methode "kreatemediarendererfrombasicdeviceasync"
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererFromBasicDeviceAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e4ee614cca9a03ca203ecde9203e019fab38ab4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038891"
---
# <a name="imediarendererfactorycreatemediarendererfrombasicdeviceasync-method"></a><span data-ttu-id="5c258-106">Imediarendererfactory:: kreatemediarendererfrombasicdeviceasync-Methode</span><span class="sxs-lookup"><span data-stu-id="5c258-106">IMediaRendererFactory::CreateMediaRendererFromBasicDeviceAsync method</span></span>

<span data-ttu-id="5c258-107">Erstellt asynchron eine neue Instanz eines Objekts, das die [**imediarenderer**](imediarenderer.md) -Schnittstelle mithilfe der angegebenen [**ibasicdevice**](ibasicdevice.md) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="5c258-107">Asynchronously creates a new instance of an object that implements the [**IMediaRenderer**](imediarenderer.md) interface using the specified [**IBasicDevice**](ibasicdevice.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c258-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c258-108">Syntax</span></span>


```C++
HRESULT CreateMediaRendererFromBasicDeviceAsync(
  [in]          IBasicDevice                 *basicDevice,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="5c258-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c258-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c258-110">*basicdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5c258-110">*basicDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c258-111">Ein Zeiger auf eine [**ibasicdevice**](ibasicdevice.md) -Schnittstelle, die das Gerät darstellt, für das eine Instanz von [**imediarenderer**](imediarenderer.md) erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="5c258-111">A pointer to an [**IBasicDevice**](ibasicdevice.md) interface representing the device for which an instance of [**IMediaRenderer**](imediarenderer.md) will be created.</span></span>

</dd> <dt>

<span data-ttu-id="5c258-112">*Wert* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5c258-112">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5c258-113">Empfängt einen Verweis auf ein Objekt vom Typ " [**kreatemediarendereroperation**](createmediarendereroperation.md) ", das verwendet wird, um Ergebnisse aus dem asynchronen Vorgang zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5c258-113">Receives a reference to a [**CreateMediaRendererOperation**](createmediarendereroperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c258-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c258-114">Return value</span></span>

<span data-ttu-id="5c258-115">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="5c258-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5c258-116">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5c258-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5c258-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5c258-117">Return code</span></span>                                                                          | <span data-ttu-id="5c258-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c258-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5c258-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5c258-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5c258-120">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5c258-120">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="5c258-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c258-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c258-122">**Imediarendererfactory**</span><span class="sxs-lookup"><span data-stu-id="5c258-122">**IMediaRendererFactory**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

