---
description: Ermöglicht den Zugriff auf Arbeitsspeicher, der für tablettthreads freigegeben
ms.assetid: 047ff598-7d20-49d7-bdd3-498fe5c778c6
title: 'Itabletcontextp:: geesharedmemorycommunications-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.UseSharedMemoryCommunications
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: d7880e1d0377d9d0140a0c82509abd31182c724e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353989"
---
# <a name="itabletcontextpusesharedmemorycommunications-method"></a><span data-ttu-id="09242-103">Itabletcontextp:: geesharedmemorycommunications-Methode</span><span class="sxs-lookup"><span data-stu-id="09242-103">ITabletContextP::UseSharedMemoryCommunications method</span></span>

<span data-ttu-id="09242-104">Ermöglicht den Zugriff auf Arbeitsspeicher, der für tablettthreads freigegeben</span><span class="sxs-lookup"><span data-stu-id="09242-104">Provides access to memory shared between tablet threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="09242-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="09242-105">Syntax</span></span>


```C++
HRESULT UseSharedMemoryCommunications(
  [in]  DWORD pid,
  [out] DWORD *phEventMoreData,
  [out] DWORD *phEventClientReady,
  [out] DWORD *phMutexAccess,
  [out] DWORD *phFileMapping
);
```



## <a name="parameters"></a><span data-ttu-id="09242-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="09242-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09242-107">*PID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="09242-107">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09242-108">Prozess-ID.</span><span class="sxs-lookup"><span data-stu-id="09242-108">Process id.</span></span>

</dd> <dt>

<span data-ttu-id="09242-109">*pheventmoredata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="09242-109">*phEventMoreData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09242-110">Ereignis handle, das signalisiert, wann neue Daten zur Verarbeitung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="09242-110">Event handle that signals when new data is available to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="09242-111">*pheventclientready* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="09242-111">*phEventClientReady* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09242-112">Zurück gegebenes Ereignis handle, mit dem signalisiert wird, dass der Client für den Empfang von Daten bereit ist.</span><span class="sxs-lookup"><span data-stu-id="09242-112">Returned event handle used to signal that the client is ready to receive data.</span></span> <span data-ttu-id="09242-113">Wird signalisiert, nachdem neue Daten verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="09242-113">Signaled after processing new data.</span></span>

</dd> <dt>

<span data-ttu-id="09242-114">*phmutexaccess* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="09242-114">*phMutexAccess* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09242-115">Der Mutex, der Zugriff auf den gemeinsamen Speicher gewährt.</span><span class="sxs-lookup"><span data-stu-id="09242-115">The mutex granting access to shared memory.</span></span>

</dd> <dt>

<span data-ttu-id="09242-116">*phfilemapping* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="09242-116">*phFileMapping* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09242-117">Zeiger auf den freigegebenen Speicherblock.</span><span class="sxs-lookup"><span data-stu-id="09242-117">Pointer to the shared memory block.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09242-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="09242-118">Return value</span></span>

<span data-ttu-id="09242-119">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="09242-119">This method can return one of these values.</span></span>



| <span data-ttu-id="09242-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="09242-120">Return code</span></span>                                                                            | <span data-ttu-id="09242-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09242-121">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="09242-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="09242-122"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="09242-123">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="09242-123">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="09242-124"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="09242-124"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="09242-125">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="09242-125">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="09242-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09242-126">Remarks</span></span>

<span data-ttu-id="09242-127">Die Methode " **toharedmemorycommunications** " wird als Teil des Tablet PC Shared Memory-Protokolls verwendet.</span><span class="sxs-lookup"><span data-stu-id="09242-127">The **UseSharedMemoryCommunications** method is used as part of the Tablet PC shared memory protocol.</span></span> <span data-ttu-id="09242-128">Da der wisptis-Dienst über eine hohe Integritäts Ebene (High Integrity Level, IL) verfügt, kann er Daten, die im freigegebenen Speicher gespeichert sind, speichern und darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="09242-128">Since the Wisptis service has a high integrity level (IL), it can store and access data stored in shared memory without needing to elevate its privileges.</span></span>

<span data-ttu-id="09242-129">Die [**SharedMemory- \_ Header**](sharedmemory-header.md) Struktur wird aus den Daten, auf die die Datei Zuordnung verweist, umgewandelt, und die unformatierten Paketdaten folgen dem **SharedMemory- \_ Header**.</span><span class="sxs-lookup"><span data-stu-id="09242-129">The [**SHAREDMEMORY\_HEADER**](sharedmemory-header.md) structure is cast from the data referenced by the file mapping and the raw packet data follows the **SHAREDMEMORY\_HEADER**.</span></span> <span data-ttu-id="09242-130">Rohdaten von Paketen können aus dem freigegebenen Speicher gelesen werden, wenn das Ereignis, auf das *pdweventclientready* verweist, ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="09242-130">Raw packet data can be read off of the shared memory when the event referenced by *pdwEventClientReady* is raised.</span></span>

<span data-ttu-id="09242-131">In der folgenden Liste wird die Abfolge von Ereignissen zum Zugreifen auf und Verwenden von frei gegebenem Speicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="09242-131">The following list describes the sequence of events for accessing and using shared memory.</span></span>

-   <span data-ttu-id="09242-132">Der Client legt das clientready-Ereignis fest.</span><span class="sxs-lookup"><span data-stu-id="09242-132">The client sets the clientReady event.</span></span>
-   <span data-ttu-id="09242-133">Der Client wartet auf das MoreData-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="09242-133">The client waits for the moreData event.</span></span>
-   <span data-ttu-id="09242-134">Der Client erhält den Mutex.</span><span class="sxs-lookup"><span data-stu-id="09242-134">The client acquires the mutex.</span></span>
-   <span data-ttu-id="09242-135">Der Client liest Paketdaten aus dem Abschnitt des gemeinsam genutzten Speichers nach dem Header und den Seriennummern nach den Paketen.</span><span class="sxs-lookup"><span data-stu-id="09242-135">The client reads packet data from the section of shared memory after the header and serial numbers after the packets.</span></span>
-   <span data-ttu-id="09242-136">Der Client verarbeitet Daten abhängig vom Wert von **dwevent**.</span><span class="sxs-lookup"><span data-stu-id="09242-136">The client handles data depending on the value of **dwEvent**.</span></span>
-   <span data-ttu-id="09242-137">Der Client schreibt-1 (0xFFFFFFFF) in **dwevent**.</span><span class="sxs-lookup"><span data-stu-id="09242-137">The client writes -1 (0xFFFFFFFF) into **dwEvent**.</span></span>
-   <span data-ttu-id="09242-138">Der Client gibt den Mutex frei.</span><span class="sxs-lookup"><span data-stu-id="09242-138">The client releases the mutex.</span></span>
-   <span data-ttu-id="09242-139">Der Client legt das clientready-Ereignis fest.</span><span class="sxs-lookup"><span data-stu-id="09242-139">The client sets the clientReady event.</span></span>

## <a name="requirements"></a><span data-ttu-id="09242-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09242-140">Requirements</span></span>



| <span data-ttu-id="09242-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09242-141">Requirement</span></span> | <span data-ttu-id="09242-142">Wert</span><span class="sxs-lookup"><span data-stu-id="09242-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="09242-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="09242-143">Minimum supported client</span></span><br/> | <span data-ttu-id="09242-144">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09242-144">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="09242-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="09242-145">Minimum supported server</span></span><br/> | <span data-ttu-id="09242-146">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="09242-146">None supported</span></span><br/>                                                              |
| <span data-ttu-id="09242-147">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="09242-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="09242-148"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="09242-148"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09242-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09242-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09242-150">**Itabletcontextp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="09242-150">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> <dt>

[<span data-ttu-id="09242-151">**Usenamedsharedmemorycommunications**</span><span class="sxs-lookup"><span data-stu-id="09242-151">**UseNamedSharedMemoryCommunications**</span></span>](itabletcontextp-usenamedsharedmemorycommunications.md)
</dt> </dl>

 

 




