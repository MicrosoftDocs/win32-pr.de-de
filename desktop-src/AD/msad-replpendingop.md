---
title: MSAD_ReplPendingOp-Klasse
description: Stellt die DS- \_ repl- \_ op-Struktur dar, die eine Replikations Aufgabe beschreibt, die gerade ausgeführt wird oder deren Ausführung aussteht
ms.assetid: d1c101fa-ae33-48da-9b00-93fde553a4f9
ms.tgt_platform: multiple
keywords:
- MSAD_ReplPendingOp-Klasse Active Directory
- MSAD_ReplPendingOp Klasse Active Directory, beschrieben
topic_type:
- apiref
api_name:
- MSAD_ReplPendingOp
- MSAD_ReplPendingOp.SerialNumber
- MSAD_ReplPendingOp.PositionInQ
- MSAD_ReplPendingOp.OpStartTime
- MSAD_ReplPendingOp.TimeEnqueued
- MSAD_ReplPendingOp.Priority
- MSAD_ReplPendingOp.OpType
- MSAD_ReplPendingOp.Options
- MSAD_ReplPendingOp.NamingContextDN
- MSAD_ReplPendingOp.NamingContextObjGuid
- MSAD_ReplPendingOp.DsaDN
- MSAD_ReplPendingOp.DsaAddress
- MSAD_ReplPendingOp.DsaObjGuid
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f1c3faddac915f602104d7e5dc4e9b6bc7d6944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391923"
---
# <a name="msad_replpendingop-class"></a><span data-ttu-id="26f45-105">MSAD \_ replpdingop-Klasse</span><span class="sxs-lookup"><span data-stu-id="26f45-105">MSAD\_ReplPendingOp class</span></span>

<span data-ttu-id="26f45-106">Stellt die [**DS- \_ repl- \_ op**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw) -Struktur dar, die eine Replikations Aufgabe beschreibt, die gerade ausgeführt wird oder deren Ausführung aussteht</span><span class="sxs-lookup"><span data-stu-id="26f45-106">Represents the [**DS\_REPL\_OP**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw) structure, which describes a replication task that is currently executing or pending execution.</span></span> <span data-ttu-id="26f45-107">Diese Struktur wird von der [**dsreplicagetinfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="26f45-107">This structure is returned by the [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="26f45-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="26f45-108">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplPendingOp
{
  uint32   SerialNumber;
  uint32   PositionInQ;
  datetime OpStartTime;
  datetime TimeEnqueued;
  uint32   Priority;
  uint32   OpType;
  uint32   Options;
  String   NamingContextDN;
  String   NamingContextObjGuid;
  String   DsaDN;
  String   DsaAddress;
  String   DsaObjGuid;
};
```

## <a name="members"></a><span data-ttu-id="26f45-109">Member</span><span class="sxs-lookup"><span data-stu-id="26f45-109">Members</span></span>

<span data-ttu-id="26f45-110">Die **MSAD \_ replpdingop** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="26f45-110">The **MSAD\_ReplPendingOp** class has these types of members:</span></span>

-   [<span data-ttu-id="26f45-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="26f45-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="26f45-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="26f45-112">Properties</span></span>

<span data-ttu-id="26f45-113">Die **MSAD \_ replpdingop** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="26f45-113">The **MSAD\_ReplPendingOp** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="26f45-114">**Dsaaddress**</span><span class="sxs-lookup"><span data-stu-id="26f45-114">**DsaAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f45-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="26f45-115">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="26f45-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26f45-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26f45-117">Ruft die Transport spezifische Netzwerkadresse des Remote Servers ab, der diesem Vorgang zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="26f45-117">Gets the transport-specific network address of the remote server that is associated with this operation.</span></span> <span data-ttu-id="26f45-118">**Null** , wenn kein Remote Server vorhanden ist, der diesem Vorgang zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="26f45-118">**NULL** if there is no remote server that is associated with this operation.</span></span>

</dd> <dt>

<span data-ttu-id="26f45-119">**Dsadn**</span><span class="sxs-lookup"><span data-stu-id="26f45-119">**DsaDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f45-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="26f45-120">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="26f45-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26f45-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26f45-122">Ruft den X. 500-Pfad des DSA ab, der dem Remote Server zugeordnet ist, der diesem Vorgang entspricht.</span><span class="sxs-lookup"><span data-stu-id="26f45-122">Gets the X.500 path of the DSA that is associated with the remote server that corresponds to this operation.</span></span> <span data-ttu-id="26f45-123">**Null** , wenn kein Remote Server diesem Vorgang entspricht.</span><span class="sxs-lookup"><span data-stu-id="26f45-123">**NULL** if no remote server corresponds to this operation.</span></span>

</dd> <dt>

<span data-ttu-id="26f45-124">**Dsaobjguid**</span><span class="sxs-lookup"><span data-stu-id="26f45-124">**DsaObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f45-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="26f45-125">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="26f45-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26f45-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26f45-127">Ruft den Wert des [**objectGUID**](/windows/desktop/ADSchema/a-objectguid) -Attributs des DSA ab, das durch die **dsadn** -Eigenschaft identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="26f45-127">Gets the value of the [**objectGuid**](/windows/desktop/ADSchema/a-objectguid) attribute of the DSA that is identified by the **DsaDN** property.</span></span>

</dd> <dt>

<span data-ttu-id="26f45-128">**Namingcontextdn**</span><span class="sxs-lookup"><span data-stu-id="26f45-128">**NamingContextDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f45-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="26f45-129">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="26f45-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26f45-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26f45-131">Ruft den X. 500-Pfad des Namens Kontexts (NC) ab, der diesem Vorgang zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="26f45-131">Gets the X.500 path of the naming context (NC) that is associated with this operation.</span></span>

</dd> <dt>

<span data-ttu-id="26f45-132">**Namingcontextobjguid**</span><span class="sxs-lookup"><span data-stu-id="26f45-132">**NamingContextObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f45-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="26f45-133">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="26f45-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26f45-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26f45-135">Ruft das [**objectGUID**](/windows/desktop/ADSchema/a-objectguid) -Attribut des NC ab, das durch die **namingcontextdn** -Eigenschaft identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="26f45-135">Gets the [**objectGuid**](/windows/desktop/ADSchema/a-objectguid) attribute of the NC that is identified by the **NamingContextDN** property.</span></span>

</dd> <dt>

<span data-ttu-id="26f45-136">**Opstarttime**</span><span class="sxs-lookup"><span data-stu-id="26f45-136">**OpStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f45-137">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="26f45-137">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="26f45-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26f45-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26f45-139">Ruft die Zeit ab, zu der der Vorgang gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="26f45-139">Gets the time when the operation was started.</span></span> <span data-ttu-id="26f45-140">**Null** , wenn sich dieser Vorgang noch in der Warteschlange befindet.</span><span class="sxs-lookup"><span data-stu-id="26f45-140">**NULL** if this operation is still in the queue.</span></span>

</dd> <dt>

<span data-ttu-id="26f45-141">**Optionen**</span><span class="sxs-lookup"><span data-stu-id="26f45-141">**Options**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f45-142">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26f45-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26f45-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26f45-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26f45-144">Ruft den Satz von Flags ab, der zusätzliche Daten über den Vorgang bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="26f45-144">Gets the set of flags that provides additional data about the operation.</span></span> <span data-ttu-id="26f45-145">Der Inhalt dieses Elements wird durch den Wert der **optype** -Eigenschaft bestimmt.</span><span class="sxs-lookup"><span data-stu-id="26f45-145">The contents of this member are determined by the value of the **OpType** property.</span></span>

<dt>

<span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>

<span data-ttu-id="26f45-146"><span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>**DS \_ repl- \_ op- \_ \_ typsynchronisierung**</span><span class="sxs-lookup"><span data-stu-id="26f45-146"><span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>**DS\_REPL\_OP\_TYPE\_SYNC**</span></span>


</dt> <dd>

<span data-ttu-id="26f45-147">Enthält 0 (null) oder eine Kombination aus einem oder mehreren der \**DS \_ \_ \* repsync* _-Werte, wie für den _Options \*-Parameter in [**dsreplicasync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca)definiert.</span><span class="sxs-lookup"><span data-stu-id="26f45-147">Contains zero or a combination of one or more of the **DS\_REPSYNC\_\** _ values as defined for the _Options* parameter in [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca).</span></span>

</dd> <dt>

<span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>

<span data-ttu-id="26f45-148"><span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>**DS \_ repl \_ op- \_ Typ \_ Hinzufügen**</span><span class="sxs-lookup"><span data-stu-id="26f45-148"><span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>**DS\_REPL\_OP\_TYPE\_ADD**</span></span>


</dt> <dd>

<span data-ttu-id="26f45-149">Enthält 0 (null) oder eine Kombination aus einem oder mehreren der \**DS \_ \_ \**-Werte, die für den Parameter "_Options \*" in " [**dsreplicaadd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda)" definiert sind.</span><span class="sxs-lookup"><span data-stu-id="26f45-149">Contains zero or a combination of one or more of the **DS\_REPADD\_\** _ values as defined for the _Options* parameter in [**DsReplicaAdd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda).</span></span>

</dd> <dt>

<span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>

<span data-ttu-id="26f45-150"><span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>**DS \_ repl- \_ op- \_ Typ \_ Löschen**</span><span class="sxs-lookup"><span data-stu-id="26f45-150"><span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>**DS\_REPL\_OP\_TYPE\_DELETE**</span></span>


</dt> <dd>

<span data-ttu-id="26f45-151">Enthält 0 (null) oder eine Kombination aus einem oder mehreren der \**DS- \_ \_ \* repdel* _-Werte, wie für den _Options \*-Parameter in [**dsreplicadel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela)definiert.</span><span class="sxs-lookup"><span data-stu-id="26f45-151">Contains zero or a combination of one or more of the **DS\_REPDEL\_\** _ values as defined for the _Options* parameter in [**DsReplicaDel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela).</span></span>

</dd> <dt>

<span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>

<span data-ttu-id="26f45-152"><span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>**DS \_ repl- \_ op- \_ \_ Typänderung**</span><span class="sxs-lookup"><span data-stu-id="26f45-152"><span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>**DS\_REPL\_OP\_TYPE\_MODIFY**</span></span>


</dt> <dd>

<span data-ttu-id="26f45-153">Enthält 0 (null) oder eine Kombination aus einem oder mehreren der \**DS- \_ repmod \_ \** _-Werte, wie für den _Options \*-Parameter in [**dsreplicamodify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya)definiert.</span><span class="sxs-lookup"><span data-stu-id="26f45-153">Contains zero or a combination of one or more of the **DS\_REPMOD\_\** _ values as defined for the _Options* parameter in [**DsReplicaModify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya).</span></span>

</dd> <dt>

<span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>

<span data-ttu-id="26f45-154"><span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>**DS \_ repl \_ - \_ \_ typupdate- \_ Refs**</span><span class="sxs-lookup"><span data-stu-id="26f45-154"><span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>**DS\_REPL\_OP\_TYPE\_UPDATE\_REFS**</span></span>


</dt> <dd>

<span data-ttu-id="26f45-155">Enthält 0 (null) oder eine Kombination aus einem oder mehreren der \**DS- \_ \_ \* repsupd* _-Werte, wie für den Parameter "_Options \*" in [**dsreplicaupdaterefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa)definiert.</span><span class="sxs-lookup"><span data-stu-id="26f45-155">Contains zero or a combination of one or more of the **DS\_REPSUPD\_\** _ values as defined for the _Options* parameter in [**DsReplicaUpdateRefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="26f45-156">**OpType**</span><span class="sxs-lookup"><span data-stu-id="26f45-156">**OpType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f45-157">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26f45-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26f45-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26f45-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26f45-159">Ruft den Wert des [**DS- \_ repl- \_ op- \_ Typs**](/windows/desktop/api/Ntdsapi/ne-ntdsapi-ds_repl_op_type) ab, der den Typ des Vorgangs angibt, den diese Klasse darstellt.</span><span class="sxs-lookup"><span data-stu-id="26f45-159">Gets the [**DS\_REPL\_OP\_TYPE**](/windows/desktop/api/Ntdsapi/ne-ntdsapi-ds_repl_op_type) value that indicates the type of operation that this class represents.</span></span>

</dd> <dt>

<span data-ttu-id="26f45-160">**Positioninq**</span><span class="sxs-lookup"><span data-stu-id="26f45-160">**PositionInQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f45-161">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26f45-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26f45-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26f45-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26f45-163">Ruft die Position dieses Vorgangs in der Warteschlange ab.</span><span class="sxs-lookup"><span data-stu-id="26f45-163">Gets the position of this operation in the queue.</span></span>

</dd> <dt>

<span data-ttu-id="26f45-164">**Priority**</span><span class="sxs-lookup"><span data-stu-id="26f45-164">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f45-165">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26f45-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26f45-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26f45-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26f45-167">Ruft die Priorität dieses Vorgangs ab.</span><span class="sxs-lookup"><span data-stu-id="26f45-167">Gets the priority of this operation.</span></span> <span data-ttu-id="26f45-168">Aufgaben mit höherer Priorität werden zuerst ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="26f45-168">Higher-priority tasks are executed first.</span></span> <span data-ttu-id="26f45-169">Die Priorität wird vom Server basierend auf dem Typ des Vorgangs, der von dieser Klasse dargestellt wird, und den Parametern des Vorgangs berechnet.</span><span class="sxs-lookup"><span data-stu-id="26f45-169">The priority is calculated by the server based on the type of operation that this class represents and the parameters of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="26f45-170">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="26f45-170">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f45-171">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26f45-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26f45-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26f45-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26f45-173">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="26f45-173">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="26f45-174">Ruft die ID des Vorgangs ab, der pro Computer und pro Start eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="26f45-174">Gets the ID of the operation, which is unique per-machine and per-boot.</span></span>

</dd> <dt>

<span data-ttu-id="26f45-175">**Zeit in Warteschlange eingereiht**</span><span class="sxs-lookup"><span data-stu-id="26f45-175">**TimeEnqueued**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f45-176">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="26f45-176">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="26f45-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26f45-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26f45-178">Ruft den Zeitpunkt ab, zu dem dieser Vorgang der Warteschlange hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="26f45-178">Gets the time at which this operation was added to the queue.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26f45-179">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26f45-179">Requirements</span></span>



| <span data-ttu-id="26f45-180">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26f45-180">Requirement</span></span> | <span data-ttu-id="26f45-181">Wert</span><span class="sxs-lookup"><span data-stu-id="26f45-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26f45-182">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="26f45-182">Minimum supported client</span></span><br/> | <span data-ttu-id="26f45-183">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="26f45-183">None supported</span></span><br/>                                                               |
| <span data-ttu-id="26f45-184">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="26f45-184">Minimum supported server</span></span><br/> | <span data-ttu-id="26f45-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26f45-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="26f45-186">Namespace</span><span class="sxs-lookup"><span data-stu-id="26f45-186">Namespace</span></span><br/>                | <span data-ttu-id="26f45-187">\\Microsoftactivedirectory-Stammverzeichnis</span><span class="sxs-lookup"><span data-stu-id="26f45-187">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="26f45-188">MOF</span><span class="sxs-lookup"><span data-stu-id="26f45-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26f45-189"><dt>ReplProv. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="26f45-189"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="26f45-190">DLL</span><span class="sxs-lookup"><span data-stu-id="26f45-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26f45-191"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26f45-191"><dt>Replprov.dll</dt></span></span> </dl> |



 

