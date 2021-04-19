---
description: KTM definiert die folgenden Eintragung-Zugriffs Masken, die beim Öffnen von Eintragung verwendet werden.
ms.assetid: 93773eb7-141a-49f3-9306-ffbda2f4ab9f
title: Eintragung von Zugriffs Masken (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63e4ebd67f93368215ebcdcd362595d0341adb52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369046"
---
# <a name="enlistment-access-masks"></a><span data-ttu-id="eed40-103">Eintragung von Zugriffs Masken</span><span class="sxs-lookup"><span data-stu-id="eed40-103">Enlistment Access Masks</span></span>

<span data-ttu-id="eed40-104">KTM definiert die folgenden Eintragung-Zugriffs Masken, die beim Öffnen von Eintragung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eed40-104">KTM defines the following enlistment access masks to be used when opening enlistments.</span></span>

<dl> <dt>

<span data-ttu-id="eed40-105"><span id="ENLISTMENT_QUERY_INFORMATION"></span><span id="enlistment_query_information"></span>**Eintragung von \_ Abfrage \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="eed40-105"><span id="ENLISTMENT_QUERY_INFORMATION"></span><span id="enlistment_query_information"></span>**ENLISTMENT\_QUERY\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eed40-106">0x00001 beginnt</span><span class="sxs-lookup"><span data-stu-id="eed40-106">0x00001</span></span>
</dt> <dt>



<span data-ttu-id="eed40-107">Der Aufrufer kann KTM nach Informationen zur Eintragung Abfragen.</span><span class="sxs-lookup"><span data-stu-id="eed40-107">The caller can query KTM for information about the enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eed40-108"><span id="ENLISTMENT_SET_INFORMATION"></span><span id="enlistment_set_information"></span>**Informationen zu Eintragung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eed40-108"><span id="ENLISTMENT_SET_INFORMATION"></span><span id="enlistment_set_information"></span>**ENLISTMENT\_SET\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eed40-109">0x00002</span><span class="sxs-lookup"><span data-stu-id="eed40-109">0x00002</span></span>
</dt> <dt>



<span data-ttu-id="eed40-110">Der Aufrufer kann Informationen über die Eintragung festlegen.</span><span class="sxs-lookup"><span data-stu-id="eed40-110">The caller can set information about the enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eed40-111"><span id="ENLISTMENT_RECOVER"></span><span id="enlistment_recover"></span>**Eintragung der Eintragung \_**</span><span class="sxs-lookup"><span data-stu-id="eed40-111"><span id="ENLISTMENT_RECOVER"></span><span id="enlistment_recover"></span>**ENLISTMENT\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eed40-112">0x00004</span><span class="sxs-lookup"><span data-stu-id="eed40-112">0x00004</span></span>
</dt> <dt>



<span data-ttu-id="eed40-113">Der Aufrufer kann eine Eintragung wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="eed40-113">The caller can recover an enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eed40-114"><span id="ENLISTMENT_SUBORDINATE_RIGHTS"></span><span id="enlistment_subordinate_rights"></span>**unter \_ geordnete Rechte der \_ Eintragung**</span><span class="sxs-lookup"><span data-stu-id="eed40-114"><span id="ENLISTMENT_SUBORDINATE_RIGHTS"></span><span id="enlistment_subordinate_rights"></span>**ENLISTMENT\_SUBORDINATE\_RIGHTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eed40-115">0x00008</span><span class="sxs-lookup"><span data-stu-id="eed40-115">0x00008</span></span>
</dt> <dt>



<span data-ttu-id="eed40-116">Der Aufrufer kann Aktionen ausführen, die ein Ressourcen-Manager für die Transaktion ausführt.</span><span class="sxs-lookup"><span data-stu-id="eed40-116">The caller can complete actions that a resource manager does on behalf of the transaction.</span></span> <span data-ttu-id="eed40-117">Im folgenden finden Sie eine Liste von Aktionen:</span><span class="sxs-lookup"><span data-stu-id="eed40-117">The following is a list of actions:</span></span>

-   [<span data-ttu-id="eed40-118">**Commitcomplete**</span><span class="sxs-lookup"><span data-stu-id="eed40-118">**CommitComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [<span data-ttu-id="eed40-119">**Preparecomplete**</span><span class="sxs-lookup"><span data-stu-id="eed40-119">**PrepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [<span data-ttu-id="eed40-120">**Prepreparecomplete**</span><span class="sxs-lookup"><span data-stu-id="eed40-120">**PrePrepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)
-   [<span data-ttu-id="eed40-121">**Rollbackcomplete**</span><span class="sxs-lookup"><span data-stu-id="eed40-121">**RollbackComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete)
-   [<span data-ttu-id="eed40-122">**Read onlyeintragung**</span><span class="sxs-lookup"><span data-stu-id="eed40-122">**ReadOnlyEnlistment**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)
-   [<span data-ttu-id="eed40-123">**Rollbackeintragung**</span><span class="sxs-lookup"><span data-stu-id="eed40-123">**RollbackEnlistment**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)
-   [<span data-ttu-id="eed40-124">**Singlephasereject**</span><span class="sxs-lookup"><span data-stu-id="eed40-124">**SinglePhaseReject**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)


</dt> </dl> </dd> <dt>

<span data-ttu-id="eed40-125"><span id="ENLISTMENT_SUPERIOR_RIGHTS"></span><span id="enlistment_superior_rights"></span>**Erweiterte Rechte Eintragung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eed40-125"><span id="ENLISTMENT_SUPERIOR_RIGHTS"></span><span id="enlistment_superior_rights"></span>**ENLISTMENT\_SUPERIOR\_RIGHTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eed40-126">0x00010</span><span class="sxs-lookup"><span data-stu-id="eed40-126">0x00010</span></span>
</dt> <dt>



<span data-ttu-id="eed40-127">Der Aufrufer kann sich als übergeordneter Transaktions-Manager in die Transaktion eintragen.</span><span class="sxs-lookup"><span data-stu-id="eed40-127">The caller can enlist in the transaction as a superior transaction manager.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eed40-128"><span id="ENLISTMENT_GENERIC_READ"></span><span id="enlistment_generic_read"></span>**allgemeiner Einschreibungs \_ \_ Lesevorgang**</span><span class="sxs-lookup"><span data-stu-id="eed40-128"><span id="ENLISTMENT_GENERIC_READ"></span><span id="enlistment_generic_read"></span>**ENLISTMENT\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eed40-129">0x20001</span><span class="sxs-lookup"><span data-stu-id="eed40-129">0x20001</span></span>
</dt> <dt>



<span data-ttu-id="eed40-130">Der Aufrufer verfügt über die folgenden Berechtigungen: **Standard \_ Rechte \_ Lese** -und Eintragung von **\_ Abfrage \_ Informationen**.</span><span class="sxs-lookup"><span data-stu-id="eed40-130">The caller has the following privileges: **STANDARD\_RIGHTS\_READ** and **ENLISTMENT\_QUERY\_INFORMATION**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eed40-131"><span id="ENLISTMENT_GENERIC_WRITE"></span><span id="enlistment_generic_write"></span>**\_allgemeiner \_ Schreibzugriff**</span><span class="sxs-lookup"><span data-stu-id="eed40-131"><span id="ENLISTMENT_GENERIC_WRITE"></span><span id="enlistment_generic_write"></span>**ENLISTMENT\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eed40-132">0x2001e</span><span class="sxs-lookup"><span data-stu-id="eed40-132">0x2001E</span></span>
</dt> <dt>



<span data-ttu-id="eed40-133">Der Aufrufer verfügt über die folgenden Berechtigungen: **Standard \_ Rechte \_ Schreiben**, **\_ \_ Informationen** zu Eintragung und **Eintragung \_ Wiederherstellen**.</span><span class="sxs-lookup"><span data-stu-id="eed40-133">The caller has the following privileges: **STANDARD\_RIGHTS\_WRITE**, **ENLISTMENT\_SET\_INFORMATION**, and **ENLISTMENT\_RECOVER**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eed40-134"><span id="ENLISTMENT_GENERIC_EXECUTE"></span><span id="enlistment_generic_execute"></span>**\_generische Eintragung \_ Ausführen**</span><span class="sxs-lookup"><span data-stu-id="eed40-134"><span id="ENLISTMENT_GENERIC_EXECUTE"></span><span id="enlistment_generic_execute"></span>**ENLISTMENT\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eed40-135">0x2001c</span><span class="sxs-lookup"><span data-stu-id="eed40-135">0x2001C</span></span>
</dt> <dt>



<span data-ttu-id="eed40-136">Der Aufrufer verfügt über die folgenden Berechtigungen: **Standard \_ Rechte werden \_ ausgeführt**, **Eintragung werden \_ wieder hergestellt**, und Eintragung von unter **\_ geordneten \_ rechten**.</span><span class="sxs-lookup"><span data-stu-id="eed40-136">The caller has the following privileges: **STANDARD\_RIGHTS\_EXECUTE**, **ENLISTMENT\_RECOVER**, and **ENLISTMENT\_SUBORDINATE\_RIGHTS**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eed40-137"><span id="ENLISTMENT_ALL_ACCESS"></span><span id="enlistment_all_access"></span>**Eintragung für den \_ gesamten \_ Zugriff**</span><span class="sxs-lookup"><span data-stu-id="eed40-137"><span id="ENLISTMENT_ALL_ACCESS"></span><span id="enlistment_all_access"></span>**ENLISTMENT\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eed40-138">0xF 001F</span><span class="sxs-lookup"><span data-stu-id="eed40-138">0xF001F</span></span>
</dt> <dt>



<span data-ttu-id="eed40-139">Dieser Wert legt alle gültigen Bits für einen Eintragung-Zugriffs Wert fest.</span><span class="sxs-lookup"><span data-stu-id="eed40-139">This value sets all valid bits for an enlistment access value.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eed40-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eed40-140">Requirements</span></span>



| <span data-ttu-id="eed40-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eed40-141">Requirement</span></span> | <span data-ttu-id="eed40-142">Wert</span><span class="sxs-lookup"><span data-stu-id="eed40-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eed40-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eed40-143">Minimum supported client</span></span><br/> | <span data-ttu-id="eed40-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eed40-144">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="eed40-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eed40-145">Minimum supported server</span></span><br/> | <span data-ttu-id="eed40-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eed40-146">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="eed40-147">Header</span><span class="sxs-lookup"><span data-stu-id="eed40-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="eed40-148"><dt>WinNT. h</dt></span><span class="sxs-lookup"><span data-stu-id="eed40-148"><dt>WinNT.h</dt></span></span> </dl> |



 

 




