---
description: Richtet Shared Memory-Kommunikation für den Tablet-Kontext ein.
ms.assetid: 63e6b271-d89a-4c91-9a15-9e41dcdfa363
title: 'Itabletcontextp:: usenamedsharedmemorycommunications-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.UseNamedSharedMemoryCommunications
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: 81e8c653dd12600ae02fe7e6038de6e6a38786e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349313"
---
# <a name="itabletcontextpusenamedsharedmemorycommunications-method"></a><span data-ttu-id="5476b-103">Itabletcontextp:: usenamedsharedmemorycommunications-Methode</span><span class="sxs-lookup"><span data-stu-id="5476b-103">ITabletContextP::UseNamedSharedMemoryCommunications method</span></span>

<span data-ttu-id="5476b-104">Richtet Shared Memory-Kommunikation für den Tablet-Kontext ein.</span><span class="sxs-lookup"><span data-stu-id="5476b-104">Sets up shared memory communication for the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="5476b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5476b-105">Syntax</span></span>


```C++
HRESULT UseNamedSharedMemoryCommunications(
  [in]  DWORD  pid,
  [in]  LPCSTR pszCallerSid,
  [in]  LPCSTR pszCallerIntegritySid,
  [out] DWORD  *pdwEventMoreDataId,
  [out] DWORD  *pdwEventClientReadyId,
  [out] DWORD  *pdwMutexAccessId,
  [out] DWORD  *pdwFileMappingId
);
```



## <a name="parameters"></a><span data-ttu-id="5476b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5476b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5476b-107">*PID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5476b-107">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5476b-108">Die Prozess-ID des Clients, der auf den gemeinsamen Speicher zugreift.</span><span class="sxs-lookup"><span data-stu-id="5476b-108">The process ID of the client that accesses shared memory.</span></span>

</dd> <dt>

<span data-ttu-id="5476b-109">*pszcallersid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5476b-109">*pszCallerSid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5476b-110">Die Sicherheits-ID des Funktions Aufrufers.</span><span class="sxs-lookup"><span data-stu-id="5476b-110">The security identifier of the function caller.</span></span>

</dd> <dt>

<span data-ttu-id="5476b-111">*pszcallerintegratysid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5476b-111">*pszCallerIntegritySid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5476b-112">Die Sicherheits-ID, die die Integrität der aufrufenden Funktion überprüfen kann.</span><span class="sxs-lookup"><span data-stu-id="5476b-112">The security identifier that can verify the integrity of the calling function.</span></span>

</dd> <dt>

<span data-ttu-id="5476b-113">*pdweventmoredataid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5476b-113">*pdwEventMoreDataId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5476b-114">Eine ganze Zahl, die zum Erstellen des Namens eines Ereignisses verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5476b-114">An integer used to construct the name of an event.</span></span> <span data-ttu-id="5476b-115">Das Ereignis gibt an, ob weitere Daten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="5476b-115">The event indicates whether there is more data.</span></span>

</dd> <dt>

<span data-ttu-id="5476b-116">*pdweventclientleseryid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5476b-116">*pdwEventClientReadyId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5476b-117">Eine ganze Zahl, die zum Erstellen des Namens eines Ereignisses verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5476b-117">An integer used to construct the name of an event.</span></span> <span data-ttu-id="5476b-118">Das-Ereignis signalisiert, dass der Client für den Empfang von Daten bereit ist.</span><span class="sxs-lookup"><span data-stu-id="5476b-118">The event signals that the client is ready to receive data.</span></span> <span data-ttu-id="5476b-119">Das Ereignis wird signalisiert, nachdem neue Daten verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="5476b-119">The event is signaled after processing new data.</span></span>

</dd> <dt>

<span data-ttu-id="5476b-120">*pdwmutexaccessid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5476b-120">*pdwMutexAccessId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5476b-121">Ein Zeiger auf die Zugriffs-ID des freigegebenen Speichers.</span><span class="sxs-lookup"><span data-stu-id="5476b-121">A pointer to the access identifier of the shared memory.</span></span>

</dd> <dt>

<span data-ttu-id="5476b-122">*pdwfilemappingid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5476b-122">*pdwFileMappingId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5476b-123">Eine ganze Zahl, die den freigegebenen Arbeitsspeicher identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5476b-123">An integer that identifies the shared memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5476b-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5476b-124">Return value</span></span>

<span data-ttu-id="5476b-125">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="5476b-125">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5476b-126">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5476b-126">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5476b-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5476b-127">Remarks</span></span>

<span data-ttu-id="5476b-128">Die **usenamedsharedmemorycommunications** -Methode ist Teil des Tablet PC Shared Memory-Protokolls.</span><span class="sxs-lookup"><span data-stu-id="5476b-128">The **UseNamedSharedMemoryCommunications** method is part of the Tablet PC shared memory protocol.</span></span> <span data-ttu-id="5476b-129">Ein Client ohne erhöhte Rechte übergibt eine Sicherheits-ID (SID) und eine Sicherheits-ID (Integritäts Stufe, Il-sid), sodass der Tablet-Dienst Zugriffs Steuerungs Listen (Access Control Lists, ACL) für den Zugriff auf die freigegebenen Speicher Objekte verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="5476b-129">A client without elevated privileges passes in a security identifier (SID) and an integrity level security identifier (IL-SID) so that the Tablet service can use access control lists (ACL) to access the shared memory objects.</span></span> <span data-ttu-id="5476b-130">Wenn der Client über erweiterte Berechtigungen verfügt, sollte er "remoesharedmemorycommunications" verwenden, bei dem es sich um die API handelt, die aufgerufen wird, wenn der Dienst bereits über eine erhöhte Berechtigung verfügt.</span><span class="sxs-lookup"><span data-stu-id="5476b-130">If the client has elevated privileges, it should use UseSharedMemoryCommunications, which is the API that is called if the service already has an elevated privilege.</span></span>

<span data-ttu-id="5476b-131">Die [**SharedMemory- \_ Header**](sharedmemory-header.md) Struktur speichert den Shared Memory-Header.</span><span class="sxs-lookup"><span data-stu-id="5476b-131">The [**SHAREDMEMORY\_HEADER**](sharedmemory-header.md) structure stores the shared memory header.</span></span>

<span data-ttu-id="5476b-132">Die [**SharedMemory- \_ Header**](sharedmemory-header.md) Struktur wird aus den Daten umgewandelt, auf die von der Datei Zuordnung verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="5476b-132">The [**SHAREDMEMORY\_HEADER**](sharedmemory-header.md) structure is cast from the data referenced by the file mapping.</span></span> <span data-ttu-id="5476b-133">Die Rohdaten des Pakets folgen dem **SharedMemory- \_ Header**.</span><span class="sxs-lookup"><span data-stu-id="5476b-133">The raw packet data follows the **SHAREDMEMORY\_HEADER**.</span></span> <span data-ttu-id="5476b-134">Unformatierte Paketdaten können aus dem freigegebenen Speicher gelesen werden, wenn das Ereignis, auf das von *pdweventclientleseyid* verwiesen wird, ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="5476b-134">Raw packet data can be read off of the shared memory when the event referenced by *pdwEventClientReadyId* is raised.</span></span>

<span data-ttu-id="5476b-135">In der folgenden Liste wird die Abfolge von Ereignissen zum Zugreifen auf und Verwenden von frei gegebenem Speicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5476b-135">The following list describes the sequence of events for accessing and using shared memory.</span></span>

1.  <span data-ttu-id="5476b-136">Der Client löst das clientready-Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="5476b-136">The client raises the clientReady event.</span></span>
2.  <span data-ttu-id="5476b-137">Der Client wartet auf das MoreData-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5476b-137">The client waits for the moreData event.</span></span>
3.  <span data-ttu-id="5476b-138">Der Client erhält den Mutex.</span><span class="sxs-lookup"><span data-stu-id="5476b-138">The client acquires the mutex.</span></span>
4.  <span data-ttu-id="5476b-139">Der Client liest Paketdaten aus dem Abschnitt des gemeinsam genutzten Speichers, der auf den Header folgt.</span><span class="sxs-lookup"><span data-stu-id="5476b-139">The client reads packet data from the section of shared memory that follows the header.</span></span> <span data-ttu-id="5476b-140">Seriennummern werden im gemeinsam genutzten Speicher nach den Paketdaten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5476b-140">Serial numbers appear in the shared memory after the packet data.</span></span>
5.  <span data-ttu-id="5476b-141">Der Client verarbeitet Daten abhängig vom Wert von **dwevent**.</span><span class="sxs-lookup"><span data-stu-id="5476b-141">The client handles data depending on the value of **dwEvent**.</span></span>
6.  <span data-ttu-id="5476b-142">Der Client schreibt-1 (0xFFFFFFFF) in **dwevent**.</span><span class="sxs-lookup"><span data-stu-id="5476b-142">The client writes -1 (0xFFFFFFFF) into **dwEvent**.</span></span>
7.  <span data-ttu-id="5476b-143">Der Client gibt den Mutex frei.</span><span class="sxs-lookup"><span data-stu-id="5476b-143">The client releases the mutex.</span></span>
8.  <span data-ttu-id="5476b-144">Der Client löst das clientready-Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="5476b-144">The client raises the clientReady event.</span></span>

<span data-ttu-id="5476b-145">Die Ereignis Namen werden erstellt, indem die Ausgabe dieser Methode formatiert wird.</span><span class="sxs-lookup"><span data-stu-id="5476b-145">The event names are created by formatting the output of this method.</span></span> <span data-ttu-id="5476b-146">Die folgenden Definitionen können in Verbindung mit sprintf oder dem entsprechenden verwendet werden, um die Ereignis Namen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5476b-146">The following definitions can be used in conjunction with sprintf or its equivalent to create the event names.</span></span>


```C++
#define WISPTIS_SM_MORE_DATA_EVENT_NAME     _T("wisptis-1-%d-%u")
#define WISPTIS_SM_CLIENT_DONE_EVENT_NAME   _T("wisptis-2-%d-%u")
#define WISPTIS_SM_SECTION_NAME             _T("wisptis-3-%d-%u")
#define WISPTIS_SM_THREAD_EVENT_NAME        _T("wisptis-4-%u")
```



<span data-ttu-id="5476b-147">In jeder Definition wird der Abschnitt "% d" durch die Prozess-ID ersetzt, und der Abschnitt "% u" wird durch die in " *pdweventmoredataid* " oder " *pdweventclientread yid*" zurückgegebene Ganzzahl ersetzt.</span><span class="sxs-lookup"><span data-stu-id="5476b-147">In each definition, the %d section is replaced with the process ID, and the %u section is replaced with the integer returned in *pdwEventMoreDataId* or *pdwEventClientReadyId*.</span></span>

## <a name="requirements"></a><span data-ttu-id="5476b-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5476b-148">Requirements</span></span>



| <span data-ttu-id="5476b-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5476b-149">Requirement</span></span> | <span data-ttu-id="5476b-150">Wert</span><span class="sxs-lookup"><span data-stu-id="5476b-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5476b-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5476b-151">Minimum supported client</span></span><br/> | <span data-ttu-id="5476b-152">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5476b-152">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5476b-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5476b-153">Minimum supported server</span></span><br/> | <span data-ttu-id="5476b-154">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5476b-154">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5476b-155">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5476b-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="5476b-156"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5476b-156"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5476b-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5476b-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5476b-158">**"US-haredmemorycommunications"**</span><span class="sxs-lookup"><span data-stu-id="5476b-158">**UseSharedMemoryCommunications**</span></span>](itabletcontextp-usesharedmemorycommunications.md)
</dt> <dt>

[<span data-ttu-id="5476b-159">**Itabletcontextp**</span><span class="sxs-lookup"><span data-stu-id="5476b-159">**ITabletContextP**</span></span>](itabletcontextp.md)
</dt> </dl>

 

 




