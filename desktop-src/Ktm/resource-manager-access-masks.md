---
description: KTM definiert die folgenden Eintragung-Zugriffs Masken, die beim Öffnen eines Ressourcen-Managers verwendet werden.
ms.assetid: 6b901b73-516d-4f27-b258-3b93a8f9675f
title: Ressourcen-Manager Zugriffs Masken (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f0f579a96ed80de100a5cb41cb9c4e9b847a060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131517"
---
# <a name="resource-manager-access-masks"></a><span data-ttu-id="ef3ab-103">Ressourcen-Manager Zugriffs Masken</span><span class="sxs-lookup"><span data-stu-id="ef3ab-103">Resource Manager Access Masks</span></span>

<span data-ttu-id="ef3ab-104">KTM definiert die folgenden Eintragung-Zugriffs Masken, die beim Öffnen eines Ressourcen-Managers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef3ab-104">KTM defines the following enlistment access masks to be used when opening a resource manager.</span></span>

<dl> <dt>

<span data-ttu-id="ef3ab-105"><span id="RESOURCEMANAGER_QUERY_INFORMATION"></span><span id="resourcemanager_query_information"></span>**ResourceManager- \_ Abfrage \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="ef3ab-105"><span id="RESOURCEMANAGER_QUERY_INFORMATION"></span><span id="resourcemanager_query_information"></span>**RESOURCEMANAGER\_QUERY\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef3ab-106">Der Aufrufer kann die Informationen des Ressourcen-Managers (RM) Abfragen.</span><span class="sxs-lookup"><span data-stu-id="ef3ab-106">The caller can query for the resource manager (RM) information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef3ab-107"><span id="RESOURCEMANAGER_SET_INFORMATION"></span><span id="resourcemanager_set_information"></span>**Informationen zum ResourceManager- \_ Satz \_**</span><span class="sxs-lookup"><span data-stu-id="ef3ab-107"><span id="RESOURCEMANAGER_SET_INFORMATION"></span><span id="resourcemanager_set_information"></span>**RESOURCEMANAGER\_SET\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef3ab-108">Der Aufrufer kann die RM-Informationen festlegen.</span><span class="sxs-lookup"><span data-stu-id="ef3ab-108">The caller can set the RM information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef3ab-109"><span id="RESOURCEMANAGER_RECOVER"></span><span id="resourcemanager_recover"></span>**ResourceManager- \_ Wiederherstellung**</span><span class="sxs-lookup"><span data-stu-id="ef3ab-109"><span id="RESOURCEMANAGER_RECOVER"></span><span id="resourcemanager_recover"></span>**RESOURCEMANAGER\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef3ab-110">Der Aufrufer kann das angegebene RM wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="ef3ab-110">The caller can recover the specified RM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef3ab-111"><span id="RESOURCEMANAGER_ENLIST"></span><span id="resourcemanager_enlist"></span>**ResourceManager- \_ Enlist**</span><span class="sxs-lookup"><span data-stu-id="ef3ab-111"><span id="RESOURCEMANAGER_ENLIST"></span><span id="resourcemanager_enlist"></span>**RESOURCEMANAGER\_ENLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef3ab-112">Der Aufrufer kann eine RM in eine Transaktion eintragen.</span><span class="sxs-lookup"><span data-stu-id="ef3ab-112">The caller can enlist an RM in a transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef3ab-113"><span id="RESOURCEMANAGER_GET_NOTIFICATION"></span><span id="resourcemanager_get_notification"></span>**ResourceManager- \_ get- \_ Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="ef3ab-113"><span id="RESOURCEMANAGER_GET_NOTIFICATION"></span><span id="resourcemanager_get_notification"></span>**RESOURCEMANAGER\_GET\_NOTIFICATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef3ab-114">Der Aufrufer kann eine Benachrichtigung für einen RM erhalten.</span><span class="sxs-lookup"><span data-stu-id="ef3ab-114">The caller can receive a notification for an RM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef3ab-115"><span id="RESOURCEMANAGER_GENERIC_READ"></span><span id="resourcemanager_generic_read"></span>**generischer ResourceManager- \_ \_ Lesevorgang**</span><span class="sxs-lookup"><span data-stu-id="ef3ab-115"><span id="RESOURCEMANAGER_GENERIC_READ"></span><span id="resourcemanager_generic_read"></span>**RESOURCEMANAGER\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef3ab-116">Der Aufrufer verfügt über die folgenden Berechtigungen: Standard \_ Rechte \_ lesen, Abfrage Informationen von ResourceManager \_ \_ und ResourceManager- \_ Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="ef3ab-116">The caller has the following privileges: STANDARD\_RIGHTS\_READ, RESOURCEMANAGER\_QUERY\_INFORMATION, and RESOURCEMANAGER\_RECOVER.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef3ab-117"><span id="RESOURCEMANAGER_GENERIC_WRITE"></span><span id="resourcemanager_generic_write"></span>**\_generischer Schreibvorgang von ResourceManager \_**</span><span class="sxs-lookup"><span data-stu-id="ef3ab-117"><span id="RESOURCEMANAGER_GENERIC_WRITE"></span><span id="resourcemanager_generic_write"></span>**RESOURCEMANAGER\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef3ab-118">Der Aufrufer verfügt über die folgenden Berechtigungen: Standard \_ Rechte \_ schreiben, Informationen zum ResourceManager \_ \_ -Satz, ResourceManager \_ Enlist und ResourceManager \_ get- \_ Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="ef3ab-118">The caller has the following privileges: STANDARD\_RIGHTS\_WRITE, RESOURCEMANAGER\_SET\_INFORMATION, RESOURCEMANAGER\_ENLIST, and RESOURCEMANAGER\_GET\_NOTIFICATION.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef3ab-119"><span id="RESOURCEMANAGER_GENERIC_EXECUTE"></span><span id="resourcemanager_generic_execute"></span>**generische ResourceManager- \_ \_ Ausführung**</span><span class="sxs-lookup"><span data-stu-id="ef3ab-119"><span id="RESOURCEMANAGER_GENERIC_EXECUTE"></span><span id="resourcemanager_generic_execute"></span>**RESOURCEMANAGER\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef3ab-120">Der Aufrufer verfügt über die folgenden Berechtigungen: Standard \_ Rechte \_ Execute, ResourceManager \_ Enlist und ResourceManager \_ get \_ Notification.</span><span class="sxs-lookup"><span data-stu-id="ef3ab-120">The caller has the following privileges: STANDARD\_RIGHTS\_EXECUTE, RESOURCEMANAGER\_ENLIST, and RESOURCEMANAGER\_GET\_NOTIFICATION.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef3ab-121"><span id="RESOURCEMANAGER_ALL_ACCESS"></span><span id="resourcemanager_all_access"></span>**ResourceManager \_ - \_ Zugriff**</span><span class="sxs-lookup"><span data-stu-id="ef3ab-121"><span id="RESOURCEMANAGER_ALL_ACCESS"></span><span id="resourcemanager_all_access"></span>**RESOURCEMANAGER\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef3ab-122">Der Aufrufer verfügt über die folgenden Berechtigungen: Standard \_ Rechte sind \_ erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ef3ab-122">The caller has the following privilege: STANDARD\_RIGHTS\_REQUIRED.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ef3ab-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef3ab-123">Requirements</span></span>



| <span data-ttu-id="ef3ab-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef3ab-124">Requirement</span></span> | <span data-ttu-id="ef3ab-125">Wert</span><span class="sxs-lookup"><span data-stu-id="ef3ab-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ef3ab-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef3ab-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ef3ab-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef3ab-127">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="ef3ab-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef3ab-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ef3ab-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef3ab-129">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="ef3ab-130">Header</span><span class="sxs-lookup"><span data-stu-id="ef3ab-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef3ab-131"><dt>WinNT. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef3ab-131"><dt>WinNT.h</dt></span></span> </dl> |



 

 




