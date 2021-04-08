---
description: 'Weitere Informationen zu: jetgeungessionparameter-Funktion'
title: Jetgeungessionparameter-Funktion
TOCTitle: JetGetSessionParameter Function
ms:assetid: 36fbcc06-a72d-4bfb-976b-1b705487732a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835039(v=EXCHG.10)
ms:contentKeyID: 49894661
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetGetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0ac02142d48009d668d903b39163b425d738b55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861932"
---
# <a name="jetgetsessionparameter-function"></a><span data-ttu-id="dbd80-103">Jetgeungessionparameter-Funktion</span><span class="sxs-lookup"><span data-stu-id="dbd80-103">JetGetSessionParameter Function</span></span>


<span data-ttu-id="dbd80-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="dbd80-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="dbd80-105">Die **jetgeungessionparameter** -Funktion liest den Sitzungs Parameter für die angegebene Sitzung.</span><span class="sxs-lookup"><span data-stu-id="dbd80-105">The **JetGetSessionParameter** function reads the session parameter for the given session.</span></span>

<span data-ttu-id="dbd80-106">Die **jetgezessionparameter** -Funktion wurde im Windows 8-Betriebssystem eingeführt.</span><span class="sxs-lookup"><span data-stu-id="dbd80-106">The **JetGetSessionParameter** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetGetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __out_cap_post_count_(cbParamMax, *pcbParamActual)  void* pvParam,
  __in          unsigned long cbParamMax,
  __out_opt_    unsigned long pcbParamActual
);
```

### <a name="parameters"></a><span data-ttu-id="dbd80-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbd80-107">Parameters</span></span>

<span data-ttu-id="dbd80-108">*-sid*</span><span class="sxs-lookup"><span data-stu-id="dbd80-108">*sesid*</span></span>

<span data-ttu-id="dbd80-109">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dbd80-109">The session to use for this call.</span></span>

<span data-ttu-id="dbd80-110">Wenn angegeben, wird die angegebene-Instanz ignoriert, und die-Instanz, die der Sitzung zugeordnet ist, wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="dbd80-110">When specified, the specified instance is ignored and the instance associated with the session will be used.</span></span>

<span data-ttu-id="dbd80-111">*sesparamid*</span><span class="sxs-lookup"><span data-stu-id="dbd80-111">*sesparamid*</span></span>

<span data-ttu-id="dbd80-112">Die ID des festzulegenden Sitzungs Parameters.</span><span class="sxs-lookup"><span data-stu-id="dbd80-112">The ID of the session parameter to set.</span></span>

<span data-ttu-id="dbd80-113">*pvParam*</span><span class="sxs-lookup"><span data-stu-id="dbd80-113">*pvParam*</span></span>

<span data-ttu-id="dbd80-114">Daten in diesem Sitzungs Parameter.</span><span class="sxs-lookup"><span data-stu-id="dbd80-114">Data in this session parameter.</span></span>

<span data-ttu-id="dbd80-115">*cbparammax*</span><span class="sxs-lookup"><span data-stu-id="dbd80-115">*cbParamMax*</span></span>

<span data-ttu-id="dbd80-116">Die maximale Größe des Datasets in diesem Sitzungs Parameter.</span><span class="sxs-lookup"><span data-stu-id="dbd80-116">The maximum size of the data set in this session parameter.</span></span>

<span data-ttu-id="dbd80-117">*pcbparamactual*</span><span class="sxs-lookup"><span data-stu-id="dbd80-117">*pcbParamActual*</span></span>

<span data-ttu-id="dbd80-118">Die tatsächliche Größe des Datasets in diesem Sitzungs Parameter.</span><span class="sxs-lookup"><span data-stu-id="dbd80-118">The actual size of the data set in this session parameter.</span></span>

### <a name="return-value"></a><span data-ttu-id="dbd80-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dbd80-119">Return value</span></span>

<span data-ttu-id="dbd80-120">Bei Erfolg wird der für den angeforderten Sitzungs Parameter geeignete Ausgabepuffer auf den Wert dieses Sitzungs Parameters festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dbd80-120">On success, the output buffer appropriate for the requested session parameter will be set to the value of that session parameter.</span></span>

<span data-ttu-id="dbd80-121">Bei einem Fehler wird der Status der Ausgabepuffer nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="dbd80-121">On failure, the state of the output buffers will be undefined.</span></span>

#### <a name="remarks"></a><span data-ttu-id="dbd80-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dbd80-122">Remarks</span></span>

<span data-ttu-id="dbd80-123">Der Session-Parameter wird für die Lebensdauer der Sitzung oder bis zum Zurücksetzen des Werts verwendet.</span><span class="sxs-lookup"><span data-stu-id="dbd80-123">The session parameter is used for the lifetime of the session or until the value is reset.</span></span>

#### <a name="requirements"></a><span data-ttu-id="dbd80-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dbd80-124">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dbd80-125"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="dbd80-125"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="dbd80-126">Erfordert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="dbd80-126">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbd80-127"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="dbd80-127"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="dbd80-128">Erfordert Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="dbd80-128">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbd80-129"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="dbd80-129"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="dbd80-130">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="dbd80-130">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbd80-131"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="dbd80-131"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="dbd80-132">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="dbd80-132">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbd80-133"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="dbd80-133"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="dbd80-134">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="dbd80-134">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="dbd80-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dbd80-135">See also</span></span>

[<span data-ttu-id="dbd80-136">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="dbd80-136">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="dbd80-137">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="dbd80-137">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="dbd80-138">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="dbd80-138">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="dbd80-139">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="dbd80-139">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="dbd80-140">Jetkreateingestance</span><span class="sxs-lookup"><span data-stu-id="dbd80-140">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="dbd80-141">JetInit</span><span class="sxs-lookup"><span data-stu-id="dbd80-141">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="dbd80-142">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="dbd80-142">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="dbd80-143">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="dbd80-143">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="dbd80-144">System Parameter</span><span class="sxs-lookup"><span data-stu-id="dbd80-144">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
