---
description: KTM definiert die folgenden Eintragung-Zugriffs Masken, die beim Öffnen eines Transaktions-Managers (TM) verwendet werden.
ms.assetid: 8f9b9d3d-e7ea-4df2-82b1-2d4c3e0766c0
title: Zugriffs Masken für den Transaktions-Manager (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efae6c0bac1fc2bfa117e74e38aff8d439eb2f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864567"
---
# <a name="transaction-manager-access-masks"></a><span data-ttu-id="68a82-103">Zugriffs Masken für den Transaktions-Manager</span><span class="sxs-lookup"><span data-stu-id="68a82-103">Transaction Manager Access Masks</span></span>

<span data-ttu-id="68a82-104">KTM definiert die folgenden Eintragung-Zugriffs Masken, die beim Öffnen eines Transaktions-Managers (TM) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="68a82-104">KTM defines the following enlistment access masks to be used when opening a transaction manager (TM).</span></span>

<dl> <dt>

<span data-ttu-id="68a82-105"><span id="TRANSACTIONMANAGER_QUERY_INFORMATION"></span><span id="transactionmanager_query_information"></span>**transaktionmanager- \_ Abfrage \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="68a82-105"><span id="TRANSACTIONMANAGER_QUERY_INFORMATION"></span><span id="transactionmanager_query_information"></span>**TRANSACTIONMANAGER\_QUERY\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68a82-106">0x00001 beginnt</span><span class="sxs-lookup"><span data-stu-id="68a82-106">0x00001</span></span>
</dt> <dt>



<span data-ttu-id="68a82-107">Der Aufrufer kann Informationen zu diesem TM Abfragen.</span><span class="sxs-lookup"><span data-stu-id="68a82-107">The caller can query information about this TM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="68a82-108"><span id="TRANSACTIONMANAGER_SET_INFORMATION"></span><span id="transactionmanager_set_information"></span>**Informationen zum transaktionmanager- \_ Satz \_**</span><span class="sxs-lookup"><span data-stu-id="68a82-108"><span id="TRANSACTIONMANAGER_SET_INFORMATION"></span><span id="transactionmanager_set_information"></span>**TRANSACTIONMANAGER\_SET\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68a82-109">0x00002</span><span class="sxs-lookup"><span data-stu-id="68a82-109">0x00002</span></span>
</dt> <dt>



<span data-ttu-id="68a82-110">Der Aufrufer kann Informationen zu diesem TM festlegen.</span><span class="sxs-lookup"><span data-stu-id="68a82-110">The caller can set information about this TM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="68a82-111"><span id="TRANSACTIONMANAGER_RECOVER"></span><span id="transactionmanager_recover"></span>**Wiederherstellung durch transaktionmanager \_**</span><span class="sxs-lookup"><span data-stu-id="68a82-111"><span id="TRANSACTIONMANAGER_RECOVER"></span><span id="transactionmanager_recover"></span>**TRANSACTIONMANAGER\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68a82-112">0x00004</span><span class="sxs-lookup"><span data-stu-id="68a82-112">0x00004</span></span>
</dt> <dt>



<span data-ttu-id="68a82-113">Der Aufrufer kann dieses TM wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="68a82-113">The caller can recover this TM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="68a82-114"><span id="TRANSACTIONMANAGER_RENAME"></span><span id="transactionmanager_rename"></span>**Umbenennen von transaktionmanager \_**</span><span class="sxs-lookup"><span data-stu-id="68a82-114"><span id="TRANSACTIONMANAGER_RENAME"></span><span id="transactionmanager_rename"></span>**TRANSACTIONMANAGER\_RENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68a82-115">0x00008</span><span class="sxs-lookup"><span data-stu-id="68a82-115">0x00008</span></span>
</dt> <dt>



<span data-ttu-id="68a82-116">Der Aufrufer kann eine TM-Instanz umbenennen.</span><span class="sxs-lookup"><span data-stu-id="68a82-116">The caller can rename a TM instance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="68a82-117"><span id="TRANSACTIONMANAGER_CREATE_RM"></span><span id="transactionmanager_create_rm"></span>**transaktionmanager \_ Create \_ RM**</span><span class="sxs-lookup"><span data-stu-id="68a82-117"><span id="TRANSACTIONMANAGER_CREATE_RM"></span><span id="transactionmanager_create_rm"></span>**TRANSACTIONMANAGER\_CREATE\_RM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68a82-118">0x00010</span><span class="sxs-lookup"><span data-stu-id="68a82-118">0x00010</span></span>
</dt> <dt>



<span data-ttu-id="68a82-119">Der Aufrufer kann einen Ressourcen-Manager erstellen, der mit diesem TM verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="68a82-119">The caller can create a resource manager that is associated with this TM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="68a82-120"><span id="TRANSACTIONMANAGER_BIND_TRANSACTION"></span><span id="transactionmanager_bind_transaction"></span>**Transaktions-Manager- \_ Bindungs \_ Transaktion**</span><span class="sxs-lookup"><span data-stu-id="68a82-120"><span id="TRANSACTIONMANAGER_BIND_TRANSACTION"></span><span id="transactionmanager_bind_transaction"></span>**TRANSACTIONMANAGER\_BIND\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68a82-121">0x00020</span><span class="sxs-lookup"><span data-stu-id="68a82-121">0x00020</span></span>
</dt> <dt>



<span data-ttu-id="68a82-122">Dieser Wert ist reserviert.</span><span class="sxs-lookup"><span data-stu-id="68a82-122">This value is reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="68a82-123"><span id="TRANSACTIONMANAGER_GENERIC_READ"></span><span id="transactionmanager_generic_read"></span>**allgemeiner transaktionmanager- \_ \_ Lesevorgang**</span><span class="sxs-lookup"><span data-stu-id="68a82-123"><span id="TRANSACTIONMANAGER_GENERIC_READ"></span><span id="transactionmanager_generic_read"></span>**TRANSACTIONMANAGER\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68a82-124">0x20001</span><span class="sxs-lookup"><span data-stu-id="68a82-124">0x20001</span></span>
</dt> <dt>



<span data-ttu-id="68a82-125">Der Aufrufer verfügt über die folgenden Berechtigungen: **Standard \_ Rechte \_ Lesen** und **transaktionmanager- \_ Abfrage \_ Informationen**.</span><span class="sxs-lookup"><span data-stu-id="68a82-125">The caller has the following privileges: **STANDARD\_RIGHTS\_READ** and **TRANSACTIONMANAGER\_QUERY\_INFORMATION**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="68a82-126"><span id="TRANSACTIONMANAGER_GENERIC_WRITE"></span><span id="transactionmanager_generic_write"></span>**allgemeiner transaktionmanager- \_ \_ Schreibvorgang**</span><span class="sxs-lookup"><span data-stu-id="68a82-126"><span id="TRANSACTIONMANAGER_GENERIC_WRITE"></span><span id="transactionmanager_generic_write"></span>**TRANSACTIONMANAGER\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68a82-127">0x2001e</span><span class="sxs-lookup"><span data-stu-id="68a82-127">0x2001E</span></span>
</dt> <dt>



<span data-ttu-id="68a82-128">Der Aufrufer verfügt über die folgenden Berechtigungen: **Standard \_ Rechte \_ Schreiben**, **Transaktions-Manager-Set- \_ \_ Informationen**, **transaktionmanager- \_ Wiederherstellung**, **Transaktions-umbenennen \_** und **Transaktionsmanager \_ Create \_ RM**.</span><span class="sxs-lookup"><span data-stu-id="68a82-128">The caller has the following privileges: **STANDARD\_RIGHTS\_WRITE**, **TRANSACTIONMANAGER\_SET\_INFORMATION**, **TRANSACTIONMANAGER\_RECOVER**, **TRANSACTIONMANAGER\_RENAME**, and **TRANSACTIONMANAGER\_CREATE\_RM**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="68a82-129"><span id="TRANSACTIONMANAGER_GENERIC_EXECUTE"></span><span id="transactionmanager_generic_execute"></span>**generische transaktionmanager- \_ \_ Ausführung**</span><span class="sxs-lookup"><span data-stu-id="68a82-129"><span id="TRANSACTIONMANAGER_GENERIC_EXECUTE"></span><span id="transactionmanager_generic_execute"></span>**TRANSACTIONMANAGER\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68a82-130">0x20000</span><span class="sxs-lookup"><span data-stu-id="68a82-130">0x20000</span></span>
</dt> <dt>



<span data-ttu-id="68a82-131">Der Aufrufer verfügt über die folgenden Berechtigungen: **Standard \_ Rechte werden \_ ausgeführt**.</span><span class="sxs-lookup"><span data-stu-id="68a82-131">The caller has the following privilege: **STANDARD\_RIGHTS\_EXECUTE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="68a82-132"><span id="TRANSACTIONMANAGER_ALL_ACCESS"></span><span id="transactionmanager_all_access"></span>**transaktionmanager \_ alle \_ Zugriffe**</span><span class="sxs-lookup"><span data-stu-id="68a82-132"><span id="TRANSACTIONMANAGER_ALL_ACCESS"></span><span id="transactionmanager_all_access"></span>**TRANSACTIONMANAGER\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68a82-133">0xF 003F</span><span class="sxs-lookup"><span data-stu-id="68a82-133">0xF003F</span></span>
</dt> <dt>



<span data-ttu-id="68a82-134">Dieser Wert legt alle gültigen Bits für einen TM-Zugriffs Wert fest.</span><span class="sxs-lookup"><span data-stu-id="68a82-134">This value sets all valid bits for a TM access value.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="68a82-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68a82-135">Requirements</span></span>



| <span data-ttu-id="68a82-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68a82-136">Requirement</span></span> | <span data-ttu-id="68a82-137">Wert</span><span class="sxs-lookup"><span data-stu-id="68a82-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="68a82-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68a82-138">Minimum supported client</span></span><br/> | <span data-ttu-id="68a82-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68a82-139">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="68a82-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68a82-140">Minimum supported server</span></span><br/> | <span data-ttu-id="68a82-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68a82-141">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="68a82-142">Header</span><span class="sxs-lookup"><span data-stu-id="68a82-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="68a82-143"><dt>WinNT. h</dt></span><span class="sxs-lookup"><span data-stu-id="68a82-143"><dt>WinNT.h</dt></span></span> </dl> |



 

 




