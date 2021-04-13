---
title: Syncnamingcontext-Methode der MSAD_ReplNeighbor-Klasse
description: Ruft die dsreplicasync-Funktion auf, die einen Ziel namens Kontext mit einer seiner Quellen synchronisiert.
ms.assetid: 005053c4-8d9c-42f6-bae6-3ecdedd5ac2b
ms.tgt_platform: multiple
keywords:
- Syncnamingcontext-Methode Active Directory
- Syncnamingcontext-Methode Active Directory, MSAD_ReplNeighbor-Klasse
- MSAD_ReplNeighbor-Klasse Active Directory, syncnamingcontext-Methode
topic_type:
- apiref
api_name:
- MSAD_ReplNeighbor.SyncNamingContext
api_location:
- replprov.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 691bd3e943f491ba93d867097ac0167c97be6108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478285"
---
# <a name="syncnamingcontext-method-of-the-msad_replneighbor-class"></a><span data-ttu-id="fa79b-106">Syncnamingcontext-Methode der MSAD \_ ReplNeighbor-Klasse</span><span class="sxs-lookup"><span data-stu-id="fa79b-106">SyncNamingContext method of the MSAD\_ReplNeighbor class</span></span>

<span data-ttu-id="fa79b-107">Ruft die [**dsreplicasync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca) -Funktion auf, die einen Ziel namens Kontext mit einer seiner Quellen synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="fa79b-107">Calls the [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca) function that synchronizes a destination naming context with one of its sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa79b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa79b-108">Syntax</span></span>


```mof
void SyncNamingContext(
  [in] uint32 Options
);
```



## <a name="parameters"></a><span data-ttu-id="fa79b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa79b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa79b-110">*Optionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa79b-110">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa79b-111">Zusätzliche Daten, die bestimmen, wie die-Methode die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="fa79b-111">Additional data that determines how the method processes the request.</span></span> <span data-ttu-id="fa79b-112">Dieser Parameter kann eine Kombination der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="fa79b-112">This parameter can be a combination of the following values.</span></span>

<dt>

<span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>

<span data-ttu-id="fa79b-113"><span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>**DS \_ repsync \_ Verweis hinzufügen \_**</span><span class="sxs-lookup"><span data-stu-id="fa79b-113"><span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>**DS\_REPSYNC\_ADD\_REFERENCE**</span></span>


</dt> <dd>

<span data-ttu-id="fa79b-114">Bewirkt, dass der Quellverzeichnis System-Agent (DSA) überprüft, ob das lokale DSA in der Liste Quell Replikate vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="fa79b-114">Causes the source directory system agent (DSA) to verify that the local DSA is present in the source replicates-to list.</span></span> <span data-ttu-id="fa79b-115">Wenn das lokale DSA nicht vorhanden ist, wird es hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fa79b-115">If the local DSA is not present, it is added.</span></span> <span data-ttu-id="fa79b-116">Dadurch wird sichergestellt, dass die Quelle Änderungs Benachrichtigungen sendet.</span><span class="sxs-lookup"><span data-stu-id="fa79b-116">This ensures that the source sends change notifications.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>

<span data-ttu-id="fa79b-117"><span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>**DS \_ repsync \_ alle \_ Quellen**</span><span class="sxs-lookup"><span data-stu-id="fa79b-117"><span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>**DS\_REPSYNC\_ALL\_SOURCES**</span></span>


</dt> <dd>

<span data-ttu-id="fa79b-118">Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fa79b-118">This value is not supported.</span></span>

<span data-ttu-id="fa79b-119">**Windows Server 2008 R2, Windows Server 2008 und Windows Server 2003:** Synchronisiert von allen Quellen.</span><span class="sxs-lookup"><span data-stu-id="fa79b-119">**Windows Server 2008 R2, Windows Server 2008 and Windows Server 2003:** Synchronizes from all sources.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>

<span data-ttu-id="fa79b-120"><span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>**\_asynchroner DS repsync- \_ \_ Vorgang**</span><span class="sxs-lookup"><span data-stu-id="fa79b-120"><span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>**DS\_REPSYNC\_ASYNCHRONOUS\_OPERATION**</span></span>


</dt> <dd>

<span data-ttu-id="fa79b-121">Führt diesen Vorgang asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="fa79b-121">Performs this operation asynchronously.</span></span>

<span data-ttu-id="fa79b-122">**Windows Server 2008 R2, Windows Server 2008 und Windows Server 2003:** Erforderlich, wenn " **DS \_ repsync \_ All \_**"-Quellen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fa79b-122">**Windows Server 2008 R2, Windows Server 2008 and Windows Server 2003:** Required when using **DS\_REPSYNC\_ALL\_SOURCES**.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>

<span data-ttu-id="fa79b-123"><span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>**DS \_ repsync- \_ Force**</span><span class="sxs-lookup"><span data-stu-id="fa79b-123"><span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>**DS\_REPSYNC\_FORCE**</span></span>


</dt> <dd>

<span data-ttu-id="fa79b-124">Wird synchronisiert, auch wenn der Link zurzeit deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fa79b-124">Synchronizes even if the link is currently disabled.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>

<span data-ttu-id="fa79b-125"><span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>**DS \_ repsync \_ voll**</span><span class="sxs-lookup"><span data-stu-id="fa79b-125"><span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>**DS\_REPSYNC\_FULL**</span></span>


</dt> <dd>

<span data-ttu-id="fa79b-126">Wird beginnend mit der ersten Update Sequenznummer (Update Sequence Number, US) synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="fa79b-126">Synchronizes starting from the first Update Sequence Number (USN).</span></span>

</dd> <dt>

<span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>

<span data-ttu-id="fa79b-127"><span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>**DS \_ repsync- \_ standortübergreifende \_ Messaging**</span><span class="sxs-lookup"><span data-stu-id="fa79b-127"><span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>**DS\_REPSYNC\_INTERSITE\_MESSAGING**</span></span>


</dt> <dd>

<span data-ttu-id="fa79b-128">Wird mithilfe eines ISM synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="fa79b-128">Synchronizes using an ISM.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>

<span data-ttu-id="fa79b-129"><span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>**DS \_ repsync \_ nicht \_ verwerfen**</span><span class="sxs-lookup"><span data-stu-id="fa79b-129"><span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>**DS\_REPSYNC\_NO\_DISCARD**</span></span>


</dt> <dd>

<span data-ttu-id="fa79b-130">Diese Synchronisierungs Anforderung wird von nicht verworfen, auch wenn eine ähnliche Synchronisierung aussteht.</span><span class="sxs-lookup"><span data-stu-id="fa79b-130">Does not discard this synchronization request, even if a similar synchronization is pending.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>

<span data-ttu-id="fa79b-131"><span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>**DS \_ repsync \_ periodisch**</span><span class="sxs-lookup"><span data-stu-id="fa79b-131"><span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>**DS\_REPSYNC\_PERIODIC**</span></span>


</dt> <dd>

<span data-ttu-id="fa79b-132">Gibt an, dass dieser Vorgang eine regelmäßige Synchronisierungs Anforderung ist, die vom Administrator geplant wird.</span><span class="sxs-lookup"><span data-stu-id="fa79b-132">Indicates that this operation is a periodic synchronization request that is scheduled by the administrator.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>

<span data-ttu-id="fa79b-133"><span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>**DS \_ repsync ( \_ dringlich)**</span><span class="sxs-lookup"><span data-stu-id="fa79b-133"><span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>**DS\_REPSYNC\_URGENT**</span></span>


</dt> <dd>

<span data-ttu-id="fa79b-134">Gibt an, dass dieser Vorgang eine Benachrichtigung über ein Update ist, das als dringlich markiert ist.</span><span class="sxs-lookup"><span data-stu-id="fa79b-134">Indicates that this operation is a notification of an update that is marked as urgent.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>

<span data-ttu-id="fa79b-135"><span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>**DS \_ repsync- \_ beschreibbares Element**</span><span class="sxs-lookup"><span data-stu-id="fa79b-135"><span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>**DS\_REPSYNC\_WRITEABLE**</span></span>


</dt> <dd>

<span data-ttu-id="fa79b-136">Gibt an, dass dieses Replikat geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="fa79b-136">Indicates that this replica is writable.</span></span> <span data-ttu-id="fa79b-137">Wenn dieses Flag nicht festgelegt ist, ist das Replikat schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="fa79b-137">If this flag is not set, the replica is read-only.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa79b-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fa79b-138">Return value</span></span>

<span data-ttu-id="fa79b-139">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fa79b-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa79b-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa79b-140">Requirements</span></span>



| <span data-ttu-id="fa79b-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa79b-141">Requirement</span></span> | <span data-ttu-id="fa79b-142">Wert</span><span class="sxs-lookup"><span data-stu-id="fa79b-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa79b-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fa79b-143">Minimum supported client</span></span><br/> | <span data-ttu-id="fa79b-144">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fa79b-144">None supported</span></span><br/>                                                               |
| <span data-ttu-id="fa79b-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fa79b-145">Minimum supported server</span></span><br/> | <span data-ttu-id="fa79b-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa79b-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fa79b-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="fa79b-147">Namespace</span></span><br/>                | <span data-ttu-id="fa79b-148">\\Microsoftactivedirectory-Stammverzeichnis</span><span class="sxs-lookup"><span data-stu-id="fa79b-148">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="fa79b-149">MOF</span><span class="sxs-lookup"><span data-stu-id="fa79b-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa79b-150"><dt>ReplProv. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fa79b-150"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa79b-151">DLL</span><span class="sxs-lookup"><span data-stu-id="fa79b-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa79b-152"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa79b-152"><dt>Replprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa79b-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa79b-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa79b-154">**MSAD \_ ReplNeighbor**</span><span class="sxs-lookup"><span data-stu-id="fa79b-154">**MSAD\_ReplNeighbor**</span></span>](msad-replneighbor.md)
</dt> </dl>

 

 





