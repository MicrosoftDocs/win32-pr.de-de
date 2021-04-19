---
description: Ruft ein Array ab, das die Paket Eigenschaften Bezeichner für den angegebenen Strich enthält.
ms.assetid: 169e3ce3-fb81-4ed6-b380-ef0d12444ba7
title: 'Icontextnode:: getstrokepacketdescriptionbyid-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokePacketDescriptionById
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e1633cd2097e256d389a2c86e450bf221f0546f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348195"
---
# <a name="icontextnodegetstrokepacketdescriptionbyid-method"></a><span data-ttu-id="471dd-103">Icontextnode:: getstrokepacketdescriptionbyid-Methode</span><span class="sxs-lookup"><span data-stu-id="471dd-103">IContextNode::GetStrokePacketDescriptionById method</span></span>

<span data-ttu-id="471dd-104">Ruft ein Array ab, das die Paket Eigenschaften Bezeichner für den angegebenen Strich enthält.</span><span class="sxs-lookup"><span data-stu-id="471dd-104">Retrieves an array containing the packet property identifiers for the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="471dd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="471dd-105">Syntax</span></span>


```C++
HRESULT GetStrokePacketDescriptionById(
  [in]      LONG  lStrokeId,
  [in, out] ULONG *pulStrokePacketDescriptionCount,
  [out]     GUID  **ppStrokePacketDescriptionGuids
);
```



## <a name="parameters"></a><span data-ttu-id="471dd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="471dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="471dd-107">*lstrokeid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="471dd-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="471dd-108">Der Bezeichner für den Strich.</span><span class="sxs-lookup"><span data-stu-id="471dd-108">The identifier for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="471dd-109">*pulstrokepacketdescriptioncount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="471dd-109">*pulStrokePacketDescriptionCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="471dd-110">Die Anzahl der Paket Eigenschaften in jedem Paket.</span><span class="sxs-lookup"><span data-stu-id="471dd-110">The number of packet properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="471dd-111">*ppstrokepacketdescriptionguids* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="471dd-111">*ppStrokePacketDescriptionGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="471dd-112">Ein Array, das die Paket Eigenschaften Bezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="471dd-112">An array containing the packet property identifiers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="471dd-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="471dd-113">Return value</span></span>

<span data-ttu-id="471dd-114">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="471dd-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="471dd-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="471dd-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="471dd-116">Um einen Speicherplatz zu vermeiden, verwenden Sie " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ", um den Arbeitsspeicher von \* *ppstrokepacketdescriptionguids* freizugeben, wenn Sie die Informationen nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="471dd-116">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppStrokePacketDescriptionGuids* when you no longer need the information.</span></span>

 

<span data-ttu-id="471dd-117">\**ppstrokepacketdescriptionguids* enthält die global eindeutigen Bezeichner (GUIDs), die die Typen der Paketdaten beschreiben, die für jeden Punkt im Strich enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="471dd-117">\**ppStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in the stroke.</span></span> <span data-ttu-id="471dd-118">Eine umfassende Liste der verfügbaren Paket Eigenschaften finden Sie unter [packetpropertyguids-Konstanten](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="471dd-118">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="471dd-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="471dd-119">Requirements</span></span>



| <span data-ttu-id="471dd-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="471dd-120">Requirement</span></span> | <span data-ttu-id="471dd-121">Wert</span><span class="sxs-lookup"><span data-stu-id="471dd-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="471dd-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="471dd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="471dd-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="471dd-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="471dd-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="471dd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="471dd-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="471dd-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="471dd-126">Header</span><span class="sxs-lookup"><span data-stu-id="471dd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="471dd-127"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="471dd-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="471dd-128">DLL</span><span class="sxs-lookup"><span data-stu-id="471dd-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="471dd-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="471dd-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="471dd-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="471dd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="471dd-131">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="471dd-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="471dd-132">**Icontextnode:: getstrokepacketdatabyid**</span><span class="sxs-lookup"><span data-stu-id="471dd-132">**IContextNode::GetStrokePacketDataById**</span></span>](icontextnode-getstrokepacketdatabyid.md)
</dt> <dt>

[<span data-ttu-id="471dd-133">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="471dd-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

