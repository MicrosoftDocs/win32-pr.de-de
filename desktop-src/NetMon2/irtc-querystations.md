---
description: Enthält eine Liste aller Computer, die derzeit Netzwerkmonitor zum Erfassen von Netzwerkdaten verwenden.
ms.assetid: 57e7b8e1-99b8-4194-b6dc-401235be4ef4
title: 'Untc:: querystations-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 1a0cebd789284dd41c293424a70686f30eb4601d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959385"
---
# <a name="irtcquerystations-method"></a><span data-ttu-id="20ee7-103">"Iritc:: querystations"-Methode</span><span class="sxs-lookup"><span data-stu-id="20ee7-103">IRTC::QueryStations method</span></span>

<span data-ttu-id="20ee7-104">Die **querystations** -Methode enthält eine Liste aller Computer, die derzeit Netzwerkmonitor zum Erfassen von Netzwerkdaten verwenden.</span><span class="sxs-lookup"><span data-stu-id="20ee7-104">The **QueryStations** method provides a list of all computers currently using Network Monitor to capture network data.</span></span>

## <a name="syntax"></a><span data-ttu-id="20ee7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="20ee7-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStations(
  [in, out] QUERYTABLE *lpQueryTable
);
```



## <a name="parameters"></a><span data-ttu-id="20ee7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="20ee7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20ee7-107">*lpquerytable* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="20ee7-107">*lpQueryTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="20ee7-108">Ein Zeiger auf eine [**QueryTable**](querytable.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="20ee7-108">A pointer to a [**QUERYTABLE**](querytable.md) structure.</span></span> <span data-ttu-id="20ee7-109">Bei der Eingabe muss diese Struktur die maximale Anzahl von Computern enthalten, die Netzwerkmonitor zurückgegeben werden sollen, sowie ein Array von [**stationquery**](stationquery.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="20ee7-109">On input, this structure must contain the maximum number of computers you want Network Monitor to return and an array of [**STATIONQUERY**](stationquery.md) structures.</span></span>

<span data-ttu-id="20ee7-110">Bei der Ausgabe gibt diese Struktur die Anzahl der Computer zurück, die Daten erfassen, und eine [**stationquery**](stationquery.md) -Struktur für jeden gefundenen Computer.</span><span class="sxs-lookup"><span data-stu-id="20ee7-110">On output, this structure returns the number of computers capturing data and a [**STATIONQUERY**](stationquery.md) structure for each computer found.</span></span> <span data-ttu-id="20ee7-111">Beachten Sie, dass dies möglicherweise Computer mit Versionen von Netzwerkmonitor ist, die das prädate Version 2,0 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="20ee7-111">Be aware that this may include computers using versions of Network Monitor that predate version 2.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20ee7-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="20ee7-112">Return value</span></span>

<span data-ttu-id="20ee7-113">Wenn die Methode erfolgreich ist, ist der Rückgabewert **nmerr \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="20ee7-113">If the method is successful, the return value is **NMERR\_SUCCESS**.</span></span>

<span data-ttu-id="20ee7-114">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="20ee7-114">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="20ee7-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="20ee7-115">Return code</span></span>                                                                                           | <span data-ttu-id="20ee7-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20ee7-116">Description</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="20ee7-117"><dt>**nicht genügend Arbeits \_ \_ Speicher für nmerr \_**</dt></span><span class="sxs-lookup"><span data-stu-id="20ee7-117"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="20ee7-118">Der für die Verarbeitung dieser Abfrage erforderliche Arbeitsspeicher ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="20ee7-118">The memory required to process this query is unavailable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="20ee7-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="20ee7-119">Remarks</span></span>

<span data-ttu-id="20ee7-120">Diese Methode kann jederzeit aufgerufen werden, nachdem die Methode " [**comatenppinterface**](createnppinterface.md) " aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="20ee7-120">This method can be called at any time after the [**CreateNPPInterface**](createnppinterface.md) method is called.</span></span> <span data-ttu-id="20ee7-121">Ein Rückruf für diese Methode ist ein synchroner Vorgang, der einige Sekunden in Anspruch nehmen kann, während Netzwerkmonitor darauf wartet, dass Remote Computer auf die Abfrage antworten.</span><span class="sxs-lookup"><span data-stu-id="20ee7-121">A call to this method is a synchronous call, which may take several seconds to complete while Network Monitor waits for remote computers to respond to the query.</span></span> <span data-ttu-id="20ee7-122">Nur Computer im lokalen Subnetz können abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="20ee7-122">Only computers on the local subnet can be queried.</span></span>

<span data-ttu-id="20ee7-123">Der Benutzer muss den Speicher für die [**QueryTable**](querytable.md) -Struktur zuordnen und diesen Arbeitsspeicher freigeben, nachdem die Tabelle nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="20ee7-123">The user must allocate the memory for the [**QUERYTABLE**](querytable.md) structure and free that memory after the table is no longer required.</span></span> <span data-ttu-id="20ee7-124">Diese Anforderung umfasst den Arbeitsspeicher, der für das in **QueryTable** verwendete [**stationquery**](stationquery.md) -Array benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="20ee7-124">This requirement includes memory needed for the [**STATIONQUERY**](stationquery.md) array used in **QUERYTABLE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="20ee7-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20ee7-125">Requirements</span></span>



| <span data-ttu-id="20ee7-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20ee7-126">Requirement</span></span> | <span data-ttu-id="20ee7-127">Wert</span><span class="sxs-lookup"><span data-stu-id="20ee7-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ee7-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="20ee7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="20ee7-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20ee7-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="20ee7-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="20ee7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="20ee7-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20ee7-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="20ee7-132">Header</span><span class="sxs-lookup"><span data-stu-id="20ee7-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="20ee7-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="20ee7-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="20ee7-134">DLL</span><span class="sxs-lookup"><span data-stu-id="20ee7-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20ee7-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20ee7-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20ee7-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20ee7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20ee7-137">**"Iran"**</span><span class="sxs-lookup"><span data-stu-id="20ee7-137">**IRTC**</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="20ee7-138">**QueryTable**</span><span class="sxs-lookup"><span data-stu-id="20ee7-138">**QUERYTABLE**</span></span>](querytable.md)
</dt> <dt>

[<span data-ttu-id="20ee7-139">**Stationquery**</span><span class="sxs-lookup"><span data-stu-id="20ee7-139">**STATIONQUERY**</span></span>](stationquery.md)
</dt> </dl>

 

 




