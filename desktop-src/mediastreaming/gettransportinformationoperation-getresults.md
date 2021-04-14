---
title: Gettransportinformationoperation GetResults-Methode
description: Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von gettransportinformationasync gestartet wurde.
ms.assetid: 8CC6641E-C1E6-4C64-90EC-4120ECB54135
keywords:
- GetResults-Methode Medien Streaming-API
- GetResults-Methode Medien Streaming-API, gettransportinformationoperation-Schnittstelle
- Gettransportinformationoperation-Schnittstelle Medien Streaming-API, GetResults-Methode
topic_type:
- apiref
api_name:
- GetTransportInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17f846a5824ed07bcaf849a540429eaabe46f3d2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390260"
---
# <a name="gettransportinformationoperationgetresults-method"></a><span data-ttu-id="f9e76-106">Gettransportinformationoperation:: GetResults-Methode</span><span class="sxs-lookup"><span data-stu-id="f9e76-106">GetTransportInformationOperation::GetResults method</span></span>

<span data-ttu-id="f9e76-107">Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von [**gettransportinformationasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync)gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="f9e76-107">Returns the results of the asynchronous operation started by [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync).</span></span>

## <a name="syntax"></a><span data-ttu-id="f9e76-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9e76-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] TransportInformation *value
);
```



## <a name="parameters"></a><span data-ttu-id="f9e76-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9e76-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9e76-110">*Wert* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f9e76-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f9e76-111">Ein Verweis auf eine [**Transportinformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-transportinformation) -Struktur, die die Ergebnisse des Vorgangs enthält.</span><span class="sxs-lookup"><span data-stu-id="f9e76-111">A reference to a [**TransportInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-transportinformation) structure that contains the results of the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9e76-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9e76-112">Return value</span></span>

<span data-ttu-id="f9e76-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="f9e76-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f9e76-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f9e76-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f9e76-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f9e76-115">Return code</span></span>                                                                          | <span data-ttu-id="f9e76-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9e76-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f9e76-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f9e76-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f9e76-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f9e76-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f9e76-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9e76-119">Remarks</span></span>

<span data-ttu-id="f9e76-120">Die **GetResults** -Methode wird in der Regel vom Ereignishandler aufgerufen, der durch Festlegen der [**abgeschlossenen**](gettransportinformationoperation-completed.md) Eigenschaft registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="f9e76-120">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](gettransportinformationoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="f9e76-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9e76-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9e76-122">**Gettransportinformationoperation**</span><span class="sxs-lookup"><span data-stu-id="f9e76-122">**GetTransportInformationOperation**</span></span>](gettransportinformationoperation.md)
</dt> </dl>

 

