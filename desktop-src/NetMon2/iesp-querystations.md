---
description: Die querystations-Methode enthält eine Liste aller Computer, die derzeit Netzwerkmonitor zum Erfassen von Netzwerkdaten verwenden.
ms.assetid: 5ad99810-e463-4477-a542-cf4dfa6967a4
title: 'IESP:: querystations-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 5287f472b2a0641eb29e4f1b37b6fe4e089dfa86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346073"
---
# <a name="iespquerystations-method"></a><span data-ttu-id="07ad5-103">IESP:: querystations-Methode</span><span class="sxs-lookup"><span data-stu-id="07ad5-103">IESP::QueryStations method</span></span>

<span data-ttu-id="07ad5-104">Die **querystations** -Methode enthält eine Liste aller Computer, die derzeit Netzwerkmonitor zum Erfassen von Netzwerkdaten verwenden.</span><span class="sxs-lookup"><span data-stu-id="07ad5-104">The **QueryStations** method provides a list of all computers that currently use Network Monitor to capture network data.</span></span>

## <a name="syntax"></a><span data-ttu-id="07ad5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="07ad5-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStations(
  [in, out] QUERYTABLE *lpQueryTable
);
```



## <a name="parameters"></a><span data-ttu-id="07ad5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="07ad5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07ad5-107">*lpquerytable* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="07ad5-107">*lpQueryTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="07ad5-108">Zeiger auf eine [QueryTable](querytable.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="07ad5-108">Pointer to a [QUERYTABLE](querytable.md) structure.</span></span> <span data-ttu-id="07ad5-109">Bei der Eingabe muss diese Struktur die maximale Anzahl von Computern enthalten, die Netzwerkmonitor zurückgegeben werden sollen, sowie ein Array von [stationquery](stationquery.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="07ad5-109">On input, this structure must contain the maximum number of computers you want Network Monitor to return and an array of [STATIONQUERY](stationquery.md) structures.</span></span>

<span data-ttu-id="07ad5-110">Bei der Ausgabe gibt diese Struktur die Anzahl der Computer zurück, die Daten erfassen, und eine [stationquery](stationquery.md) -Struktur für jeden gefundenen Computer.</span><span class="sxs-lookup"><span data-stu-id="07ad5-110">On output, this structure returns the number of computers that are capturing data and a [STATIONQUERY](stationquery.md) structure for each computer found.</span></span> <span data-ttu-id="07ad5-111">Beachten Sie, dass diese Summe Computer enthalten kann, die Versionen von Netzwerkmonitor, für die die Version 2,0 in der Vorschauversion</span><span class="sxs-lookup"><span data-stu-id="07ad5-111">Note that this total may include computers using versions of Network Monitor that predate version 2.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07ad5-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="07ad5-112">Return value</span></span>

<span data-ttu-id="07ad5-113">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="07ad5-113">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="07ad5-114">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert der folgende Fehlercode:</span><span class="sxs-lookup"><span data-stu-id="07ad5-114">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="07ad5-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="07ad5-115">Return code</span></span>                                                                                           | <span data-ttu-id="07ad5-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07ad5-116">Description</span></span>                                                         |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="07ad5-117"><dt>**nicht genügend Arbeits \_ \_ Speicher für nmerr \_**</dt></span><span class="sxs-lookup"><span data-stu-id="07ad5-117"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="07ad5-118">Der für die Verarbeitung dieser Abfrage erforderliche Arbeitsspeicher war nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="07ad5-118">The memory needed to process this query was unavailable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="07ad5-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07ad5-119">Remarks</span></span>

<span data-ttu-id="07ad5-120">Diese Methode kann jederzeit aufgerufen werden, nachdem die Methode " [comatenppinterface](createnppinterface.md) " aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="07ad5-120">This method can be called at any time after the [CreateNPPInterface](createnppinterface.md) method is called.</span></span> <span data-ttu-id="07ad5-121">Ein Rückruf für diese Methode ist ein synchroner Vorgang, der einige Sekunden in Anspruch nehmen kann, da Netzwerkmonitor darauf wartet, dass Remote Computer auf die Abfrage antworten.</span><span class="sxs-lookup"><span data-stu-id="07ad5-121">A call to this method is a synchronous call, which may take several seconds to complete as Network Monitor waits for remote computers to respond to the query.</span></span> <span data-ttu-id="07ad5-122">Nur Computer im lokalen Subnetz können abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="07ad5-122">Only computers on the local subnet can be queried.</span></span>

<span data-ttu-id="07ad5-123">Es liegt in ihrer Verantwortung, den Arbeitsspeicher für die [QueryTable](querytable.md) -Struktur zuzuordnen und diesen Arbeitsspeicher freizugeben, nachdem die Tabelle nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="07ad5-123">It is your responsibility to allocate the memory for the [QUERYTABLE](querytable.md) structure and free that memory after the table is no longer needed.</span></span> <span data-ttu-id="07ad5-124">Diese Anforderung enthält den Arbeitsspeicher, der für das in QueryTable verwendete [stationquery](stationquery.md) -Array benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="07ad5-124">This requirement includes the memory needed for the [STATIONQUERY](stationquery.md) array used in QUERYTABLE.</span></span>

## <a name="requirements"></a><span data-ttu-id="07ad5-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07ad5-125">Requirements</span></span>



| <span data-ttu-id="07ad5-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07ad5-126">Requirement</span></span> | <span data-ttu-id="07ad5-127">Wert</span><span class="sxs-lookup"><span data-stu-id="07ad5-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07ad5-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="07ad5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="07ad5-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07ad5-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="07ad5-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="07ad5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="07ad5-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07ad5-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="07ad5-132">Header</span><span class="sxs-lookup"><span data-stu-id="07ad5-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="07ad5-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="07ad5-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="07ad5-134">DLL</span><span class="sxs-lookup"><span data-stu-id="07ad5-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07ad5-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07ad5-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07ad5-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07ad5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07ad5-137">IESP</span><span class="sxs-lookup"><span data-stu-id="07ad5-137">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="07ad5-138">QueryTable</span><span class="sxs-lookup"><span data-stu-id="07ad5-138">QUERYTABLE</span></span>](querytable.md)
</dt> <dt>

[<span data-ttu-id="07ad5-139">Stationquery</span><span class="sxs-lookup"><span data-stu-id="07ad5-139">STATIONQUERY</span></span>](stationquery.md)
</dt> </dl>

 

 




