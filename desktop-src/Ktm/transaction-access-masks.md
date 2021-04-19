---
description: KTM definiert die folgenden Transaktions Zugriffs Masken, die beim Öffnen einer Transaktion verwendet werden sollen.
ms.assetid: 93ef3098-b3cc-4b24-ae82-1c10d937f14f
title: Transaktions Zugriffs Masken (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b815bcb04a97dbd059c85c6c615a7d607bf77ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348559"
---
# <a name="transaction-access-masks"></a><span data-ttu-id="afee7-103">Transaktions Zugriffs Masken</span><span class="sxs-lookup"><span data-stu-id="afee7-103">Transaction Access Masks</span></span>

<span data-ttu-id="afee7-104">KTM definiert die folgenden Transaktions Zugriffs Masken, die beim Öffnen einer Transaktion verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="afee7-104">KTM defines the following transaction access masks to be used when opening a transaction.</span></span>

<dl> <dt>

<span data-ttu-id="afee7-105"><span id="TRANSACTION_QUERY_INFORMATION"></span><span id="transaction_query_information"></span>**Transaktions \_ Abfrage \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="afee7-105"><span id="TRANSACTION_QUERY_INFORMATION"></span><span id="transaction_query_information"></span>**TRANSACTION\_QUERY\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afee7-106">0x000001</span><span class="sxs-lookup"><span data-stu-id="afee7-106">0x000001</span></span>
</dt> <dt>



<span data-ttu-id="afee7-107">Der Aufrufer kann Transaktionsinformationen Abfragen.</span><span class="sxs-lookup"><span data-stu-id="afee7-107">The caller can query transaction information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="afee7-108"><span id="TRANSACTION_SET_INFORMATION"></span><span id="transaction_set_information"></span>**Transaktions \_ Satz \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="afee7-108"><span id="TRANSACTION_SET_INFORMATION"></span><span id="transaction_set_information"></span>**TRANSACTION\_SET\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afee7-109">0x000002</span><span class="sxs-lookup"><span data-stu-id="afee7-109">0x000002</span></span>
</dt> <dt>



<span data-ttu-id="afee7-110">Der Aufrufer kann Transaktionsinformationen festlegen.</span><span class="sxs-lookup"><span data-stu-id="afee7-110">The caller can set transaction information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="afee7-111"><span id="TRANSACTION_ENLIST"></span><span id="transaction_enlist"></span>**Transaktions \_ enliste**</span><span class="sxs-lookup"><span data-stu-id="afee7-111"><span id="TRANSACTION_ENLIST"></span><span id="transaction_enlist"></span>**TRANSACTION\_ENLIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afee7-112">0x000004</span><span class="sxs-lookup"><span data-stu-id="afee7-112">0x000004</span></span>
</dt> <dt>



<span data-ttu-id="afee7-113">Der Aufrufer kann diese Transaktion eintragen.</span><span class="sxs-lookup"><span data-stu-id="afee7-113">The caller can enlist in this transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="afee7-114"><span id="TRANSACTION_COMMIT"></span><span id="transaction_commit"></span>**\_Transaktionscommit**</span><span class="sxs-lookup"><span data-stu-id="afee7-114"><span id="TRANSACTION_COMMIT"></span><span id="transaction_commit"></span>**TRANSACTION\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afee7-115">0x000008</span><span class="sxs-lookup"><span data-stu-id="afee7-115">0x000008</span></span>
</dt> <dt>



<span data-ttu-id="afee7-116">Der Aufrufer kann diese Transaktion übertragen.</span><span class="sxs-lookup"><span data-stu-id="afee7-116">The caller can commit this transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="afee7-117"><span id="TRANSACTION_ROLLBACK"></span><span id="transaction_rollback"></span>**Transaktions \_ Rollback**</span><span class="sxs-lookup"><span data-stu-id="afee7-117"><span id="TRANSACTION_ROLLBACK"></span><span id="transaction_rollback"></span>**TRANSACTION\_ROLLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afee7-118">0x000010</span><span class="sxs-lookup"><span data-stu-id="afee7-118">0x000010</span></span>
</dt> <dt>



<span data-ttu-id="afee7-119">Der Aufrufer kann diese Transaktion zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="afee7-119">The caller can roll back this transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="afee7-120"><span id="TRANSACTION_PROPAGATE"></span><span id="transaction_propagate"></span>**Transaktionsverteilung \_**</span><span class="sxs-lookup"><span data-stu-id="afee7-120"><span id="TRANSACTION_PROPAGATE"></span><span id="transaction_propagate"></span>**TRANSACTION\_PROPAGATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afee7-121">0x000020</span><span class="sxs-lookup"><span data-stu-id="afee7-121">0x000020</span></span>
</dt> <dt>



<span data-ttu-id="afee7-122">Der Aufrufer kann diese Transaktion an einen übergeordneten Ressourcen-Manager weitergeben, z. b. an den Distributed Transaction Coordinator (DTC).</span><span class="sxs-lookup"><span data-stu-id="afee7-122">The caller can propagate this transaction to a superior resource manager, such as the Distributed Transaction Coordinator (DTC).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="afee7-123"><span id="TRANSACTION_GENERIC_READ"></span><span id="transaction_generic_read"></span>**\_allgemeiner Transaktions \_ Lesevorgang**</span><span class="sxs-lookup"><span data-stu-id="afee7-123"><span id="TRANSACTION_GENERIC_READ"></span><span id="transaction_generic_read"></span>**TRANSACTION\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afee7-124">0x120001</span><span class="sxs-lookup"><span data-stu-id="afee7-124">0x120001</span></span>
</dt> <dt>



<span data-ttu-id="afee7-125">Der Aufrufer verfügt über die folgenden Berechtigungen: **Standard \_ Rechte \_ Lesen**, **Transaktions \_ Abfrage \_ Informationen** und **Synchronisieren**.</span><span class="sxs-lookup"><span data-stu-id="afee7-125">The caller has the following privileges: **STANDARD\_RIGHTS\_READ**, **TRANSACTION\_QUERY\_INFORMATION**, and **SYNCHRONIZE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="afee7-126"><span id="TRANSACTION_GENERIC_WRITE"></span><span id="transaction_generic_write"></span>**\_allgemeiner Transaktions \_ Schreibvorgang**</span><span class="sxs-lookup"><span data-stu-id="afee7-126"><span id="TRANSACTION_GENERIC_WRITE"></span><span id="transaction_generic_write"></span>**TRANSACTION\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afee7-127">0x12003e</span><span class="sxs-lookup"><span data-stu-id="afee7-127">0x12003E</span></span>
</dt> <dt>



<span data-ttu-id="afee7-128">Der Aufrufer verfügt über die folgenden Berechtigungen: **Standard \_ Rechte \_ Schreiben**, **Transaktions \_ Satz \_ Informationen**, **Transaktionscommit \_**, **Transaktions \_ Einschreibung**, **Transaktions \_ Rollback**, **Transaktions \_** Weitergabe und **Synchronisieren**.</span><span class="sxs-lookup"><span data-stu-id="afee7-128">The caller has the following privileges: **STANDARD\_RIGHTS\_WRITE**, **TRANSACTION\_SET\_INFORMATION**, **TRANSACTION\_COMMIT**, **TRANSACTION\_ENLIST**, **TRANSACTION\_ROLLBACK**, **TRANSACTION\_PROPAGATE**, and **SYNCHRONIZE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="afee7-129"><span id="TRANSACTION_GENERIC_EXECUTE"></span><span id="transaction_generic_execute"></span>**\_generische Transaktions \_ Ausführung**</span><span class="sxs-lookup"><span data-stu-id="afee7-129"><span id="TRANSACTION_GENERIC_EXECUTE"></span><span id="transaction_generic_execute"></span>**TRANSACTION\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afee7-130">0x120018</span><span class="sxs-lookup"><span data-stu-id="afee7-130">0x120018</span></span>
</dt> <dt>



<span data-ttu-id="afee7-131">Der Aufrufer verfügt über die folgenden Berechtigungen: **Standard \_ Rechte werden \_ ausgeführt**, **Transaktionscommit \_**, **Transaktions \_ Rollback** und **Synchronisieren**.</span><span class="sxs-lookup"><span data-stu-id="afee7-131">The caller has the following privileges: **STANDARD\_RIGHTS\_EXECUTE**, **TRANSACTION\_COMMIT**, **TRANSACTION\_ROLLBACK**, and **SYNCHRONIZE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="afee7-132"><span id="TRANSACTION_ALL_ACCESS"></span><span id="transaction_all_access"></span>**\_Zugriff auf alle Transaktionen \_**</span><span class="sxs-lookup"><span data-stu-id="afee7-132"><span id="TRANSACTION_ALL_ACCESS"></span><span id="transaction_all_access"></span>**TRANSACTION\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afee7-133">0x12003f</span><span class="sxs-lookup"><span data-stu-id="afee7-133">0x12003F</span></span>
</dt> <dt>



<span data-ttu-id="afee7-134">Der Aufrufer verfügt über die folgenden Berechtigungen: **Standard \_ Rechte \_ erforderlich**, **\_ allgemeiner Transaktions \_ Lese** Vorgang, **\_ allgemeiner Transaktions \_ Schreibvorgang** und **transaktionsgenerische \_ \_ Ausführung**.</span><span class="sxs-lookup"><span data-stu-id="afee7-134">The caller has the following privilege: **STANDARD\_RIGHTS\_REQUIRED**, **TRANSACTION\_GENERIC\_READ**, **TRANSACTION\_GENERIC\_WRITE**, and **TRANSACTION\_GENERIC\_EXECUTE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="afee7-135"><span id="TRANSACTION_RESOURCE_MANAGER_RIGHTS"></span><span id="transaction_resource_manager_rights"></span>**Rechte für den Transaktions \_ Ressourcen- \_ Manager \_**</span><span class="sxs-lookup"><span data-stu-id="afee7-135"><span id="TRANSACTION_RESOURCE_MANAGER_RIGHTS"></span><span id="transaction_resource_manager_rights"></span>**TRANSACTION\_RESOURCE\_MANAGER\_RIGHTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afee7-136">0x120037</span><span class="sxs-lookup"><span data-stu-id="afee7-136">0x120037</span></span>
</dt> <dt>



<span data-ttu-id="afee7-137">Der Aufrufer verfügt über die folgenden Berechtigungen: **\_ allgemeiner Transaktions \_ Lesevorgang**, **Standard \_ Rechte \_ Schreib** Vorgänge, **Transaktions \_ Satz \_ Informationen**, **Transaktions \_ Rollback**, **Transaktions \_ Einschreibung**, **Transaktions \_** Weitergabe und **Synchronisieren**.</span><span class="sxs-lookup"><span data-stu-id="afee7-137">The caller has the following privileges: **TRANSACTION\_GENERIC\_READ**, **STANDARD\_RIGHTS\_WRITE**, **TRANSACTION\_SET\_INFORMATION**, **TRANSACTION\_ROLLBACK**, **TRANSACTION\_ENLIST**, **TRANSACTION\_PROPAGATE**, and **SYNCHRONIZE**.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="afee7-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="afee7-138">Remarks</span></span>

<span data-ttu-id="afee7-139">Es wird empfohlen, dass Ressourcen-Manager beim Eintragen in eine Transaktion beim Öffnen einer Transaktion **Transaktions \_ Ressourcen-Manager- \_ \_ Rechte** angeben.</span><span class="sxs-lookup"><span data-stu-id="afee7-139">It is recommended that resource managers, when enlisting in a transaction, specify **TRANSACTION\_RESOURCE\_MANAGER\_RIGHTS** when opening a transaction.</span></span>

## <a name="requirements"></a><span data-ttu-id="afee7-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="afee7-140">Requirements</span></span>



| <span data-ttu-id="afee7-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="afee7-141">Requirement</span></span> | <span data-ttu-id="afee7-142">Wert</span><span class="sxs-lookup"><span data-stu-id="afee7-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="afee7-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="afee7-143">Minimum supported client</span></span><br/> | <span data-ttu-id="afee7-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="afee7-144">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="afee7-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="afee7-145">Minimum supported server</span></span><br/> | <span data-ttu-id="afee7-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="afee7-146">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="afee7-147">Header</span><span class="sxs-lookup"><span data-stu-id="afee7-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="afee7-148"><dt>WinNT. h</dt></span><span class="sxs-lookup"><span data-stu-id="afee7-148"><dt>WinNT.h</dt></span></span> </dl> |



 

 




