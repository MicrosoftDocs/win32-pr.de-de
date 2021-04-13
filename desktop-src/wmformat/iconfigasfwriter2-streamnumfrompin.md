---
title: IConfigAsfWriter2 streamnumfrompin-Methode
description: Die streamnumfrompin-Methode ruft die Datenstrom Nummer ab, die der angegebenen Eingabe-PIN zugeordnet ist.
ms.assetid: f645a742-e6dc-4041-8a56-3bbb5188a9a9
keywords:
- Streamnumfrompin-Methode Windows Media-Format
- Streamnumfrompin-Methode, Windows Media-Format, IConfigAsfWriter2-Schnittstelle
- IConfigAsfWriter2-Schnittstelle Windows Media-Format, streamnumfrompin-Methode
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.StreamNumFromPin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c63a31d515e70b0ee0ac5be617ee52fe23bd5416
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390453"
---
# <a name="iconfigasfwriter2streamnumfrompin-method"></a><span data-ttu-id="85b04-106">IConfigAsfWriter2:: streamnumfrompin-Methode</span><span class="sxs-lookup"><span data-stu-id="85b04-106">IConfigAsfWriter2::StreamNumFromPin method</span></span>

<span data-ttu-id="85b04-107">Die **streamnumfrompin** -Methode ruft die Datenstrom Nummer ab, die der angegebenen Eingabe-PIN zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="85b04-107">The **StreamNumFromPin** method retrieves the stream number associated with the specified input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="85b04-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="85b04-108">Syntax</span></span>


```C++
HRESULT StreamNumFromPin(
  [in]  IPin *pPin,
  [out] WORD *pwStreamNum
);
```



## <a name="parameters"></a><span data-ttu-id="85b04-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="85b04-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85b04-110">*ppin* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85b04-110">*pPin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85b04-111">Zeiger auf die **IPin** -Schnittstelle für die Eingabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="85b04-111">Pointer to the **IPin** interface on the input pin.</span></span>

</dd> <dt>

<span data-ttu-id="85b04-112">*pwstreamnum* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="85b04-112">*pwStreamNum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85b04-113">Ein Zeiger, der die streamnummer empfängt.</span><span class="sxs-lookup"><span data-stu-id="85b04-113">Pointer that receives the stream number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85b04-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="85b04-114">Return value</span></span>

<span data-ttu-id="85b04-115">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="85b04-115">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="85b04-116">Wenn ein Fehler auftritt, wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="85b04-116">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="85b04-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85b04-117">Remarks</span></span>

<span data-ttu-id="85b04-118">Manchmal müssen Sie die SDK-Schnittstellen des Windows Media-Formats direkt verwenden, um einen Stream vor dem Ausführen eines Filter Diagramms zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="85b04-118">Sometimes you may need to use the Windows Media Format SDK interfaces directly to manipulate a stream before running a filter graph.</span></span> <span data-ttu-id="85b04-119">Da Sie nicht davon ausgehen können, dass eine ASF-Datenstrom Nummer mit der Nummer der DirectShow-Pin übereinstimmt, wird diese Methode bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="85b04-119">Because you cannot assume that an ASF stream number is the same as the DirectShow pin number, this method is provided.</span></span>

## <a name="see-also"></a><span data-ttu-id="85b04-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85b04-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="85b04-121">[**IConfigAsfWriter2-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85b04-121">[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>
</dt> </dl>

 

 