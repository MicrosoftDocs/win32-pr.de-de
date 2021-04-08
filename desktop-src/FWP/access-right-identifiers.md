---
title: Zugriffsrechte Bezeichner ("f")
description: Die Windows-Filter Plattform (WFP) verwendet die standardmäßigen Win32-Zugriffsrechte sowie einen Satz WFP-spezifischer Zugriffsrechte, der in die Filter Plattform integriert ist.
ms.assetid: 77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c
topic_type:
- apiref
api_name:
- FWPM_ACTRL_ADD
- FWPM_ACTRL_ADD_LINK
- FWPM_ACTRL_BEGIN_READ_TXN
- FWPM_ACTRL_BEGIN_WRITE_TXN
- FWPM_ACTRL_CLASSIFY
- FWPM_ACTRL_ENUM
- FWPM_ACTRL_OPEN
- FWPM_ACTRL_READ
- FWPM_ACTRL_READ_STATS
- FWPM_ACTRL_SUBSCRIBE
- FWPM_ACTRL_WRITE
- FWPM_GENERIC_READ
- FWPM_GENERIC_EXECUTE
- FWPM_GENERIC_WRITE
- FWPM_GENERIC_ALL
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af182a087ade590e278bd3dd1d2bb1a64b5c598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957139"
---
# <a name="access-right-identifiers"></a><span data-ttu-id="d6a62-103">Zugriffsrechte Bezeichner</span><span class="sxs-lookup"><span data-stu-id="d6a62-103">Access Right Identifiers</span></span>

<span data-ttu-id="d6a62-104">Die Windows-Filter Plattform (WFP) verwendet die [standardmäßigen Win32-Zugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights) sowie einen Satz WFP-spezifischer Zugriffsrechte, der in die Filter Plattform integriert ist.</span><span class="sxs-lookup"><span data-stu-id="d6a62-104">Windows Filtering Platform (WFP) uses the [standard Win32 access rights](/windows/desktop/SecAuthZ/standard-access-rights) plus a set of WFP-specific access rights built into the filtering platform.</span></span> <span data-ttu-id="d6a62-105">Diese Zugriffsrechte werden ausschließlich zum Sichern von Objekten im Benutzermodus verwendet.</span><span class="sxs-lookup"><span data-stu-id="d6a62-105">These access rights are used to secure objects in user mode only.</span></span> <span data-ttu-id="d6a62-106">Kernelmodusaufrufer umgehen alle Zugriffs Überprüfungen.</span><span class="sxs-lookup"><span data-stu-id="d6a62-106">Kernel-mode callers bypass all access checks.</span></span>

<span data-ttu-id="d6a62-107">Die WFP-spezifischen zugriffsrechterer Bezeichner lauten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="d6a62-107">WFP specific access right identifiers are as follows.</span></span>

<dl> <dt>

<span data-ttu-id="d6a62-108"><span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**Hinzufügen von "f"- \_ actrl \_**</span><span class="sxs-lookup"><span data-stu-id="d6a62-108"><span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM\_ACTRL\_ADD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d6a62-109">Fügen Sie der Basis Filter-Engine (BFE) ein Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="d6a62-109">Add an object to the Base Filtering Engine (BFE).</span></span> <span data-ttu-id="d6a62-110">Dieses Zugriffsrecht ist erforderlich, um [**fwpm \* Add0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) -Funktionen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d6a62-110">This access right is needed in order to call [**Fwpm\*Add0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6a62-111"><span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**\_ \_ Link zum Hinzufügen von "f"-actrl \_**</span><span class="sxs-lookup"><span data-stu-id="d6a62-111"><span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM\_ACTRL\_ADD\_LINK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d6a62-112">Hinzufügen eines Objekts, auf das über einen Link verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="d6a62-112">Add an object referenced through a link.</span></span> <span data-ttu-id="d6a62-113">Beispielsweise wird dieses Zugriffsrecht für Aufrufe benötigt, auf die über GUIDs verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="d6a62-113">For example, this access right is needed for callouts referenced through GUIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6a62-114"><span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**f- \_ v-actrl \_ Begin \_ Read \_**</span><span class="sxs-lookup"><span data-stu-id="d6a62-114"><span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM\_ACTRL\_BEGIN\_READ\_TXN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d6a62-115">Beginnen Sie eine schreibgeschützte Transaktion.</span><span class="sxs-lookup"><span data-stu-id="d6a62-115">Begin a read-only transaction.</span></span> <span data-ttu-id="d6a62-116">Dieses Zugriffsrecht ist erforderlich, um [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d6a62-116">This access right is needed in order to call [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6a62-117"><span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**f/a- \_ \_ \_ Schreibvorgänge starten \_**</span><span class="sxs-lookup"><span data-stu-id="d6a62-117"><span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM\_ACTRL\_BEGIN\_WRITE\_TXN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d6a62-118">Beginnen Sie eine Transaktion mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="d6a62-118">Begin a read/write transaction.</span></span> <span data-ttu-id="d6a62-119">Dieses Zugriffsrecht ist erforderlich, um [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) für eine Lese-/Schreibtransaktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d6a62-119">This access right is needed in order to call [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) for a read/write transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6a62-120"><span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**\_kwpm-actrl- \_ Klassifizierung**</span><span class="sxs-lookup"><span data-stu-id="d6a62-120"><span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**FWPM\_ACTRL\_CLASSIFY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d6a62-121">Klassifizieren eines Remote Prozedur Aufrufs (RPC).</span><span class="sxs-lookup"><span data-stu-id="d6a62-121">Classify Remote Procedure Call (RPC).</span></span> <span data-ttu-id="d6a62-122">Dieses Zugriffsrecht wird von der RPC-Laufzeit benötigt, um RPC-Filter zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="d6a62-122">This access right is needed by the RPC run-time in order to enforce RPC filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6a62-123"><span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**WPM- \_ actrl-Aufzählung \_**</span><span class="sxs-lookup"><span data-stu-id="d6a62-123"><span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM\_ACTRL\_ENUM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d6a62-124">Auflisten.</span><span class="sxs-lookup"><span data-stu-id="d6a62-124">Enumerate.</span></span> <span data-ttu-id="d6a62-125">Dieses Zugriffsrecht ist erforderlich, um [**fwpm \* CreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutcreateenumhandle0) -Funktionen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d6a62-125">This access right is needed in order to call [**Fwpm\*CreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutcreateenumhandle0) functions.</span></span> <span data-ttu-id="d6a62-126">Zum Auflisten eines Objekts benötigt der Aufrufer ebenfalls fwpm- \_ actrl- \_ Lesezugriff auf das Objekt.</span><span class="sxs-lookup"><span data-stu-id="d6a62-126">To enumerate an object, the caller also needs FWPM\_ACTRL\_READ access to the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6a62-127"><span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**geöffnetes WPM- \_ actrl \_**</span><span class="sxs-lookup"><span data-stu-id="d6a62-127"><span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM\_ACTRL\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d6a62-128">Öffnen Sie eine Sitzung für die Filter-Engine.</span><span class="sxs-lookup"><span data-stu-id="d6a62-128">Open a session to the filter engine.</span></span> <span data-ttu-id="d6a62-129">Dieses Zugriffsrecht ist erforderlich, um [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d6a62-129">This access right is needed in order to call [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6a62-130"><span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**\_Lesezugriff auf die Datei \_**</span><span class="sxs-lookup"><span data-stu-id="d6a62-130"><span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM\_ACTRL\_READ**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d6a62-131">Lesen.</span><span class="sxs-lookup"><span data-stu-id="d6a62-131">Read.</span></span> <span data-ttu-id="d6a62-132">Dieses Zugriffsrecht ist erforderlich, um [**fwpm \* GetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbyid0) und [**fwpm \* GetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbykey0) -Funktionen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d6a62-132">This access right is needed in order to call [**Fwpm\*GetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbyid0) and [**Fwpm\*GetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbykey0) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6a62-133"><span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**Lese Statistik für das awpm- \_ actrl \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d6a62-133"><span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM\_ACTRL\_READ\_STATS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d6a62-134">Lesen von Statistiken.</span><span class="sxs-lookup"><span data-stu-id="d6a62-134">Read statistics.</span></span> <span data-ttu-id="d6a62-135">Dieses Zugriffsrecht ist erforderlich, um [**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) und [**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d6a62-135">This access right is needed in order to call [**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) and [**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6a62-136"><span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**Konto für die \_ Anmeldung mit dem \_ Anmelde Namen**</span><span class="sxs-lookup"><span data-stu-id="d6a62-136"><span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**FWPM\_ACTRL\_SUBSCRIBE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d6a62-137">Führen Sie den Schritt zum Abonnieren aus.</span><span class="sxs-lookup"><span data-stu-id="d6a62-137">Subscribe.</span></span> <span data-ttu-id="d6a62-138">Dieses Zugriffsrecht ist erforderlich, um [**fwpm \* SubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidersubscribechanges0) -Funktionen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d6a62-138">This access right is needed in order to call [**Fwpm\*SubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidersubscribechanges0) functions.</span></span> <span data-ttu-id="d6a62-139">Um eine Benachrichtigung für ein Objekt zu erhalten, benötigt ein Abonnent ebenfalls fwpm- \_ actrl- \_ Lesezugriff auf das Objekt.</span><span class="sxs-lookup"><span data-stu-id="d6a62-139">To receive a notification for an object, a subscriber also needs FWPM\_ACTRL\_READ access to the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6a62-140"><span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**f- \_ \_ /Schreibzugriff**</span><span class="sxs-lookup"><span data-stu-id="d6a62-140"><span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM\_ACTRL\_WRITE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d6a62-141">Schreiben von Engine-Optionen.</span><span class="sxs-lookup"><span data-stu-id="d6a62-141">Write engine options.</span></span> <span data-ttu-id="d6a62-142">Dieses Zugriffsrecht ist erforderlich, um [**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d6a62-142">This access right is needed in order to call [**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6a62-143"><span id="FWPM_GENERIC_READ"></span><span id="fwpm_generic_read"></span>**allgemeiner f- \_ \_ Lesevorgang**</span><span class="sxs-lookup"><span data-stu-id="d6a62-143"><span id="FWPM_GENERIC_READ"></span><span id="fwpm_generic_read"></span>**FWPM\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d6a62-144">Standard \_ Rechte \_ gelesene \| f \_ & \_ \_ \_ \| \_ \_ \| \_ \_ \| \_ \_ \| \_ \_ \_ # amp; amp; amp; amp; amp; amp; amp; amp; amp; amp; amp; amp; amp; amp; amp; amp; amp; amp; amp; quot; Lesen</span><span class="sxs-lookup"><span data-stu-id="d6a62-144">STANDARD\_RIGHTS\_READ \| FWPM\_ACTRL\_BEGIN\_READ\_TXN \| FWPM\_ACTRL\_CLASSIFY \| FWPM\_ACTRL\_OPEN \| FWPM\_ACTRL\_READ \| FWPM\_ACTRL\_READ\_STATS</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6a62-145"><span id="FWPM_GENERIC_EXECUTE"></span><span id="fwpm_generic_execute"></span>**\_Allgemeine Ausführung von "f" \_**</span><span class="sxs-lookup"><span data-stu-id="d6a62-145"><span id="FWPM_GENERIC_EXECUTE"></span><span id="fwpm_generic_execute"></span>**FWPM\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d6a62-146">Standard \_ Rechte \_ Ausführen von \| swpm \_ actrl \_ enum SS-actrl \| \_ \_ abonnieren</span><span class="sxs-lookup"><span data-stu-id="d6a62-146">STANDARD\_RIGHTS\_EXECUTE \| FWPM\_ACTRL\_ENUM \| FWPM\_ACTRL\_SUBSCRIBE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6a62-147"><span id="FWPM_GENERIC_WRITE"></span><span id="fwpm_generic_write"></span>**allgemeiner f- \_ \_ Schreibvorgang**</span><span class="sxs-lookup"><span data-stu-id="d6a62-147"><span id="FWPM_GENERIC_WRITE"></span><span id="fwpm_generic_write"></span>**FWPM\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d6a62-148">Standard \_ Rechte Schreib Berechtigung für das Löschen von Lese-/Ausgabe-/Ausgabe-/Quell-hinzufügen \_ \| \| \_ \_ \| \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_</span><span class="sxs-lookup"><span data-stu-id="d6a62-148">STANDARD\_RIGHTS\_WRITE \| DELETE \| FWPM\_ACTRL\_ADD \| FWPM\_ACTRL\_ADD\_LINK \| FWPM\_ACTRL\_BEGIN\_WRITE\_TXN \| FWPM\_ACTRL\_WRITE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6a62-149"><span id="FWPM_GENERIC_ALL"></span><span id="fwpm_generic_all"></span>**\_alle allgemeinen voll \_ ständig**</span><span class="sxs-lookup"><span data-stu-id="d6a62-149"><span id="FWPM_GENERIC_ALL"></span><span id="fwpm_generic_all"></span>**FWPM\_GENERIC\_ALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d6a62-150">Standard \_ Rechte \_ erforderlich, \| f WPM- \_ actrl \_ Add \| f WPM \_ actrl \_ Add Link f/amp; \_ \| \_ actrl \_ Begin \_ Read \_ TXn \| f. \_ \_ \_ \_ \| \_ \_ klassifizieren von \| BPM- \_ actrl \_ Enum \| f- \_ actrl \_ Open \| f \_ \_ \| \_ \_ \_ \| \_ \_ \| \_ \_ -actrl lesen Sie den Befehl zum Lesen von Daten, Lese Statistik, f</span><span class="sxs-lookup"><span data-stu-id="d6a62-150">STANDARD\_RIGHTS\_REQUIRED \| FWPM\_ACTRL\_ADD \| FWPM\_ACTRL\_ADD\_LINK \| FWPM\_ACTRL\_BEGIN\_READ\_TXN \| FWPM\_ACTRL\_BEGIN\_WRITE\_TXN \| FWPM\_ACTRL\_CLASSIFY \| FWPM\_ACTRL\_ENUM \| FWPM\_ACTRL\_OPEN \| FWPM\_ACTRL\_READ \| FWPM\_ACTRL\_READ\_STATS \| FWPM\_ACTRL\_SUBSCRIBE \| FWPM\_ACTRL\_WRITE</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d6a62-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6a62-151">Requirements</span></span>



| <span data-ttu-id="d6a62-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6a62-152">Requirement</span></span> | <span data-ttu-id="d6a62-153">Wert</span><span class="sxs-lookup"><span data-stu-id="d6a62-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d6a62-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d6a62-154">Minimum supported client</span></span><br/> | <span data-ttu-id="d6a62-155">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6a62-155">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d6a62-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d6a62-156">Minimum supported server</span></span><br/> | <span data-ttu-id="d6a62-157">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6a62-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d6a62-158">Header</span><span class="sxs-lookup"><span data-stu-id="d6a62-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6a62-159"><dt>"F"</dt></span><span class="sxs-lookup"><span data-stu-id="d6a62-159"><dt>Fwpmu.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6a62-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6a62-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6a62-161">Windows-Filter Plattform Access Control Modell</span><span class="sxs-lookup"><span data-stu-id="d6a62-161">Windows Filtering Platform Access Control Model</span></span>](access-control.md)
</dt> <dt>

[<span data-ttu-id="d6a62-162">Standard Zugriffsrechte</span><span class="sxs-lookup"><span data-stu-id="d6a62-162">Standard Access Rights</span></span>](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> </dl>

 

