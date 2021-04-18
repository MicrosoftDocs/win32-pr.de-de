---
description: Ruft ein Array ab, das die Paket Eigenschafts Daten für den angegebenen Strich enthält.
ms.assetid: 02db48b3-edc3-4ecb-8103-79312194937a
title: 'Icontextnode:: getstrokepacketdatabyid-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokePacketDataById
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: be2e9326e2ecb20afc652776c006c8ae989c7396
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343316"
---
# <a name="icontextnodegetstrokepacketdatabyid-method"></a><span data-ttu-id="fd6fa-103">Icontextnode:: getstrokepacketdatabyid-Methode</span><span class="sxs-lookup"><span data-stu-id="fd6fa-103">IContextNode::GetStrokePacketDataById method</span></span>

<span data-ttu-id="fd6fa-104">Ruft ein Array ab, das die Paket Eigenschafts Daten für den angegebenen Strich enthält.</span><span class="sxs-lookup"><span data-stu-id="fd6fa-104">Retrieves an array containing the packet property data for the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd6fa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd6fa-105">Syntax</span></span>


```C++
HRESULT GetStrokePacketDataById(
  [in]      LONG  strokeId,
  [in, out] ULONG *pStrokePacketDataCount,
  [out]     LONG  **pplStrokePacketData
);
```



## <a name="parameters"></a><span data-ttu-id="fd6fa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd6fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd6fa-107">*strokeid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd6fa-107">*strokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6fa-108">Der Bezeichner für den Strich.</span><span class="sxs-lookup"><span data-stu-id="fd6fa-108">The identifier for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="fd6fa-109">*pstrokepacketdatacount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fd6fa-109">*pStrokePacketDataCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6fa-110">Die Länge des Paketdaten Arrays.</span><span class="sxs-lookup"><span data-stu-id="fd6fa-110">The length of the packet data array.</span></span>

</dd> <dt>

<span data-ttu-id="fd6fa-111">*pplstrokepacketdata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fd6fa-111">*pplStrokePacketData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6fa-112">Ein Zeiger auf die Paketdaten für den Strich.</span><span class="sxs-lookup"><span data-stu-id="fd6fa-112">A pointer to the packet data for the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd6fa-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fd6fa-113">Return value</span></span>

<span data-ttu-id="fd6fa-114">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="fd6fa-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fd6fa-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd6fa-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="fd6fa-116">Um einen Speicherplatz zu vermeiden, verwenden Sie " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ", um den Arbeitsspeicher aus \* *pplstrokepacketdata* freizugeben, wenn Sie die Informationen nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="fd6fa-116">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**pplStrokePacketData* when you no longer need the information.</span></span>

 

<span data-ttu-id="fd6fa-117">*plstrokepacketdata* enthält Paketdaten für alle Punkte im Strich.</span><span class="sxs-lookup"><span data-stu-id="fd6fa-117">*plStrokePacketData* contains packet data for all of the points in the stroke.</span></span> <span data-ttu-id="fd6fa-118">Verwenden Sie [**icontextnode:: getstrokepacketdescriptionbyid**](icontextnode-getstrokepacketdescriptionbyid.md), um die Typen der Paketdaten zu erhalten, die für jeden Punkt im Strich enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="fd6fa-118">To get the types of packet data included for each point in the stroke, use [**IContextNode::GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd6fa-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd6fa-119">Requirements</span></span>



| <span data-ttu-id="fd6fa-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd6fa-120">Requirement</span></span> | <span data-ttu-id="fd6fa-121">Wert</span><span class="sxs-lookup"><span data-stu-id="fd6fa-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd6fa-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd6fa-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fd6fa-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd6fa-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fd6fa-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd6fa-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fd6fa-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fd6fa-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="fd6fa-126">Header</span><span class="sxs-lookup"><span data-stu-id="fd6fa-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd6fa-127"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fd6fa-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fd6fa-128">DLL</span><span class="sxs-lookup"><span data-stu-id="fd6fa-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd6fa-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd6fa-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="fd6fa-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd6fa-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd6fa-131">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="fd6fa-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="fd6fa-132">**Icontextnode:: getstrokepacketdescriptionbyid**</span><span class="sxs-lookup"><span data-stu-id="fd6fa-132">**IContextNode::GetStrokePacketDescriptionById**</span></span>](icontextnode-getstrokepacketdescriptionbyid.md)
</dt> <dt>

[<span data-ttu-id="fd6fa-133">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="fd6fa-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

