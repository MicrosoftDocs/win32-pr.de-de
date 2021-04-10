---
description: Die geteventdata-Methode ordnet Speicherplatz für die nmeventdata-und nmcolumninfo-Strukturen zu.
ms.assetid: b24a2a30-4543-4311-87ec-66872463aed7
title: 'Imonitoreventer:: geteventdata-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.GetEventData
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: be1654c38f51fa62909e10c12900c087bf0842fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214532"
---
# <a name="imonitoreventergeteventdata-method"></a><span data-ttu-id="22b72-103">Imonitoreventer:: geteventdata-Methode</span><span class="sxs-lookup"><span data-stu-id="22b72-103">IMonitorEventer::GetEventData method</span></span>

<span data-ttu-id="22b72-104">Die **geteventdata** -Methode ordnet Speicherplatz für die [nmeventdata](nmeventdata.md) -und [nmcolumninfo](nmcolumninfo.md) -Strukturen zu.</span><span class="sxs-lookup"><span data-stu-id="22b72-104">The **GetEventData** method allocates space for the [NMEVENTDATA](nmeventdata.md) and [NMCOLUMNINFO](nmcolumninfo.md) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="22b72-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="22b72-105">Syntax</span></span>


```C++
HRESULT GetEventData(
  [in]  BYTE         bNumColumns,
  [out] PNMEVENTDATA *ppNMEventData
);
```



## <a name="parameters"></a><span data-ttu-id="22b72-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="22b72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22b72-107">*bnumcolumns* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22b72-107">*bNumColumns* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22b72-108">Anzahl der **nmcolumninfo** -Strukturen, die benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="22b72-108">Number of **NMCOLUMNINFO** structures needed.</span></span>

</dd> <dt>

<span data-ttu-id="22b72-109">*ppnmeventdata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="22b72-109">*ppNMEventData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22b72-110">Die Adresse der **nmeventdata** -Struktur, die zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="22b72-110">Address of the **NMEVENTDATA** structure that is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22b72-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22b72-111">Return value</span></span>

<span data-ttu-id="22b72-112">Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="22b72-112">If the method is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="22b72-113">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert nmerr nicht genügend Arbeits \_ \_ \_ Speicher.</span><span class="sxs-lookup"><span data-stu-id="22b72-113">If the method is unsuccessful, the return value is NMERR\_OUT\_OF\_MEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="22b72-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22b72-114">Remarks</span></span>

<span data-ttu-id="22b72-115">Monitore verwenden diese Methode, um Speicher für die Struktur von Ereignisdaten und Spalten Informationen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="22b72-115">Monitors call this method to allocate memory for the event data and column information structures.</span></span> <span data-ttu-id="22b72-116">Informationen zum Freigeben von Arbeitsspeicher, der einer **nmeventdata** -Struktur zugeordnet ist, finden Sie unter [imonitoreventer:: freeeventdata](imonitoreventer-freeeventdata.md).</span><span class="sxs-lookup"><span data-stu-id="22b72-116">To free memory allocated for an **NMEVENTDATA** structure, see [IMonitorEventer::FreeEventData](imonitoreventer-freeeventdata.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="22b72-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22b72-117">Requirements</span></span>



| <span data-ttu-id="22b72-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22b72-118">Requirement</span></span> | <span data-ttu-id="22b72-119">Wert</span><span class="sxs-lookup"><span data-stu-id="22b72-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="22b72-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="22b72-120">Minimum supported client</span></span><br/> | <span data-ttu-id="22b72-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22b72-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="22b72-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="22b72-122">Minimum supported server</span></span><br/> | <span data-ttu-id="22b72-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22b72-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="22b72-124">Header</span><span class="sxs-lookup"><span data-stu-id="22b72-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="22b72-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="22b72-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22b72-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22b72-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22b72-127">Imonitoreventer Enter</span><span class="sxs-lookup"><span data-stu-id="22b72-127">IMonitorEventer</span></span>](imonitoreventer.md)
</dt> <dt>

[<span data-ttu-id="22b72-128">Imonitoreventer:: freeventdata</span><span class="sxs-lookup"><span data-stu-id="22b72-128">IMonitorEventer::FreeEventData</span></span>](imonitoreventer-freeeventdata.md)
</dt> <dt>

[<span data-ttu-id="22b72-129">Nmeventdata</span><span class="sxs-lookup"><span data-stu-id="22b72-129">NMEVENTDATA</span></span>](nmeventdata.md)
</dt> <dt>

[<span data-ttu-id="22b72-130">Nmcolumninfo</span><span class="sxs-lookup"><span data-stu-id="22b72-130">NMCOLUMNINFO</span></span>](nmcolumninfo.md)
</dt> </dl>

 

 




