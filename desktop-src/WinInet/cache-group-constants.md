---
title: Cache Gruppen Konstanten (WinInet. h)
description: Die folgende Liste enthält die Konstanten, die von den Cache Gruppenfunktionen verwendet werden.
ms.assetid: 9ca2069e-497d-4747-acf4-d5b8020b8ab7
topic_type:
- apiref
api_name:
- CACHEGROUP_ATTRIBUTE_BASIC
- CACHEGROUP_ATTRIBUTE_FLAG
- CACHEGROUP_ATTRIBUTE_GET_ALL
- CACHEGROUP_ATTRIBUTE_GROUPNAME
- CACHEGROUP_ATTRIBUTE_QUOTA
- CACHEGROUP_ATTRIBUTE_STORAGE
- CACHEGROUP_ATTRIBUTE_TYPE
- CACHEGROUP_FLAG_FLUSHURL_ONDELETE
- CACHEGROUP_FLAG_GIDONLY
- CACHEGROUP_FLAG_NONPURGEABLE
- CACHEGROUP_READWRITE_MASK
- CACHEGROUP_SEARCH_ALL
- CACHEGROUP_SEARCH_BYURL
- CACHEGROUP_TYPE_INVALID
- GROUP_OWNER_STORAGE_SIZE
- GROUPNAME_MAX_LENGTH
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a08efa37ad78fa3351d12fa43491c7b62ee64af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339582"
---
# <a name="cache-group-constants"></a><span data-ttu-id="0cc9d-103">Cache Gruppen Konstanten</span><span class="sxs-lookup"><span data-stu-id="0cc9d-103">Cache Group Constants</span></span>

<span data-ttu-id="0cc9d-104">Die folgende Liste enthält die Konstanten, die von den Cache Gruppenfunktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0cc9d-104">The following list contains the constants used by the cache group functions.</span></span>

<dl> <dt>

<span data-ttu-id="0cc9d-105"><span id="CACHEGROUP_ATTRIBUTE_BASIC"></span><span id="cachegroup_attribute_basic"></span>**cachegroup- \_ Attribut \_ Basic**</span><span class="sxs-lookup"><span data-stu-id="0cc9d-105"><span id="CACHEGROUP_ATTRIBUTE_BASIC"></span><span id="cachegroup_attribute_basic"></span>**CACHEGROUP\_ATTRIBUTE\_BASIC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cc9d-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0cc9d-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="0cc9d-107">Ruft die Attribute "Flags", "Type" und "Disk Quota" der Cache Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="0cc9d-107">Retrieves the flags, type, and disk quota attributes of the cache group.</span></span> <span data-ttu-id="0cc9d-108">Diese wird von der [**geturlcachegroupattribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="0cc9d-108">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cc9d-109"><span id="CACHEGROUP_ATTRIBUTE_FLAG"></span><span id="cachegroup_attribute_flag"></span>**cachegroup \_ - \_ attributflag**</span><span class="sxs-lookup"><span data-stu-id="0cc9d-109"><span id="CACHEGROUP_ATTRIBUTE_FLAG"></span><span id="cachegroup_attribute_flag"></span>**CACHEGROUP\_ATTRIBUTE\_FLAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cc9d-110">0x00000002</span><span class="sxs-lookup"><span data-stu-id="0cc9d-110">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="0cc9d-111">Legt die der Cache Gruppe zugeordneten Flags fest oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="0cc9d-111">Sets or retrieves the flags associated with the cache group.</span></span> <span data-ttu-id="0cc9d-112">Diese wird von den Funktionen " [**geturlcachegroupattribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) " und " [**lturlcachegroupattribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="0cc9d-112">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cc9d-113"><span id="CACHEGROUP_ATTRIBUTE_GET_ALL"></span><span id="cachegroup_attribute_get_all"></span>**cachegroup- \_ Attribut \_ get \_ all**</span><span class="sxs-lookup"><span data-stu-id="0cc9d-113"><span id="CACHEGROUP_ATTRIBUTE_GET_ALL"></span><span id="cachegroup_attribute_get_all"></span>**CACHEGROUP\_ATTRIBUTE\_GET\_ALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cc9d-114">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="0cc9d-114">0xffffffff</span></span>
</dt> <dt>



<span data-ttu-id="0cc9d-115">Ruft alle Attribute der Cache Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="0cc9d-115">Retrieves all the attributes of the cache group.</span></span> <span data-ttu-id="0cc9d-116">Diese wird von der [**geturlcachegroupattribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="0cc9d-116">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cc9d-117"><span id="CACHEGROUP_ATTRIBUTE_GROUPNAME"></span><span id="cachegroup_attribute_groupname"></span>**cachegroup- \_ Attribut \_ Gruppenname**</span><span class="sxs-lookup"><span data-stu-id="0cc9d-117"><span id="CACHEGROUP_ATTRIBUTE_GROUPNAME"></span><span id="cachegroup_attribute_groupname"></span>**CACHEGROUP\_ATTRIBUTE\_GROUPNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cc9d-118">0x000000010</span><span class="sxs-lookup"><span data-stu-id="0cc9d-118">0x000000010</span></span>
</dt> <dt>



<span data-ttu-id="0cc9d-119">Legt den Gruppennamen der Cache Gruppe fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="0cc9d-119">Sets or retrieves the group name of the cache group.</span></span> <span data-ttu-id="0cc9d-120">Diese wird von den Funktionen " [**geturlcachegroupattribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) " und " [**lturlcachegroupattribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="0cc9d-120">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cc9d-121"><span id="CACHEGROUP_ATTRIBUTE_QUOTA"></span><span id="cachegroup_attribute_quota"></span>**cachegroup- \_ Attribut \_ Kontingent**</span><span class="sxs-lookup"><span data-stu-id="0cc9d-121"><span id="CACHEGROUP_ATTRIBUTE_QUOTA"></span><span id="cachegroup_attribute_quota"></span>**CACHEGROUP\_ATTRIBUTE\_QUOTA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cc9d-122">0x00000008</span><span class="sxs-lookup"><span data-stu-id="0cc9d-122">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="0cc9d-123">Legt das der Cache Gruppe zugeordnete Datenträger Kontingent fest oder ruft es ab.</span><span class="sxs-lookup"><span data-stu-id="0cc9d-123">Sets or retrieves the disk quota associated with the cache group.</span></span> <span data-ttu-id="0cc9d-124">Diese wird von den Funktionen " [**geturlcachegroupattribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) " und " [**lturlcachegroupattribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="0cc9d-124">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cc9d-125"><span id="CACHEGROUP_ATTRIBUTE_STORAGE"></span><span id="cachegroup_attribute_storage"></span>**cachegroup- \_ Attribut \_ Speicher**</span><span class="sxs-lookup"><span data-stu-id="0cc9d-125"><span id="CACHEGROUP_ATTRIBUTE_STORAGE"></span><span id="cachegroup_attribute_storage"></span>**CACHEGROUP\_ATTRIBUTE\_STORAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cc9d-126">0x00000020</span><span class="sxs-lookup"><span data-stu-id="0cc9d-126">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="0cc9d-127">Legt den Gruppenbesitzer Speicher fest, der der Cache Gruppe zugeordnet ist, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="0cc9d-127">Sets or retrieves the group owner storage associated with the cache group.</span></span> <span data-ttu-id="0cc9d-128">Diese wird von den Funktionen " [**geturlcachegroupattribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) " und " [**lturlcachegroupattribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="0cc9d-128">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cc9d-129"><span id="CACHEGROUP_ATTRIBUTE_TYPE"></span><span id="cachegroup_attribute_type"></span>**cachegroup \_ - \_ Attributtyp**</span><span class="sxs-lookup"><span data-stu-id="0cc9d-129"><span id="CACHEGROUP_ATTRIBUTE_TYPE"></span><span id="cachegroup_attribute_type"></span>**CACHEGROUP\_ATTRIBUTE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cc9d-130">0x00000004</span><span class="sxs-lookup"><span data-stu-id="0cc9d-130">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="0cc9d-131">Legt den Cache Gruppentyp fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="0cc9d-131">Sets or retrieves the cache group type.</span></span> <span data-ttu-id="0cc9d-132">Diese wird von den Funktionen " [**geturlcachegroupattribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) " und " [**lturlcachegroupattribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="0cc9d-132">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cc9d-133"><span id="CACHEGROUP_FLAG_FLUSHURL_ONDELETE"></span><span id="cachegroup_flag_flushurl_ondelete"></span>**cachegroup- \_ Flag \_ flushurl \_ OnDelete**</span><span class="sxs-lookup"><span data-stu-id="0cc9d-133"><span id="CACHEGROUP_FLAG_FLUSHURL_ONDELETE"></span><span id="cachegroup_flag_flushurl_ondelete"></span>**CACHEGROUP\_FLAG\_FLUSHURL\_ONDELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cc9d-134">0x00000002</span><span class="sxs-lookup"><span data-stu-id="0cc9d-134">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="0cc9d-135">Gibt an, dass alle der Cache Gruppe zugeordneten Cache Einträge gelöscht werden sollen, es sei denn, der Eintrag gehört zu einer anderen Cache Gruppe.</span><span class="sxs-lookup"><span data-stu-id="0cc9d-135">Indicates that all the cache entries associated with the cache group should be deleted, unless the entry belongs to another cache group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cc9d-136"><span id="CACHEGROUP_FLAG_GIDONLY"></span><span id="cachegroup_flag_gidonly"></span>**cachegroup- \_ Flag " \_ gidonly"**</span><span class="sxs-lookup"><span data-stu-id="0cc9d-136"><span id="CACHEGROUP_FLAG_GIDONLY"></span><span id="cachegroup_flag_gidonly"></span>**CACHEGROUP\_FLAG\_GIDONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cc9d-137">0x00000004</span><span class="sxs-lookup"><span data-stu-id="0cc9d-137">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="0cc9d-138">Gibt an, dass die Funktion nur eine eindeutige GroupID für die Cache Gruppe erstellen und nicht die tatsächliche Gruppe erstellen soll.</span><span class="sxs-lookup"><span data-stu-id="0cc9d-138">Indicates that the function should only create a unique GROUPID for the cache group and not create the actual group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cc9d-139"><span id="CACHEGROUP_FLAG_NONPURGEABLE"></span><span id="cachegroup_flag_nonpurgeable"></span>**cachegroup- \_ Flag ist \_ nicht ersetzbar**</span><span class="sxs-lookup"><span data-stu-id="0cc9d-139"><span id="CACHEGROUP_FLAG_NONPURGEABLE"></span><span id="cachegroup_flag_nonpurgeable"></span>**CACHEGROUP\_FLAG\_NONPURGEABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cc9d-140">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0cc9d-140">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="0cc9d-141">Gibt an, dass die Cache Gruppe nicht gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="0cc9d-141">Indicates that the cache group cannot be purged.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cc9d-142"><span id="CACHEGROUP_READWRITE_MASK"></span><span id="cachegroup_readwrite_mask"></span>**cachegroup- \_ Lese Schreib \_ Maske**</span><span class="sxs-lookup"><span data-stu-id="0cc9d-142"><span id="CACHEGROUP_READWRITE_MASK"></span><span id="cachegroup_readwrite_mask"></span>**CACHEGROUP\_READWRITE\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cc9d-143">0x0000003c</span><span class="sxs-lookup"><span data-stu-id="0cc9d-143">0x0000003c</span></span>
</dt> <dt>



<span data-ttu-id="0cc9d-144">Legt den Typ, das Datenträger Kontingent, den Gruppennamen und die Besitzer Speicher Attribute der Cache Gruppe fest.</span><span class="sxs-lookup"><span data-stu-id="0cc9d-144">Sets the type, disk quota, group name, and owner storage attributes of the cache group.</span></span> <span data-ttu-id="0cc9d-145">Diese wird von der Funktion " [**setlcachegroupattribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="0cc9d-145">This is used by the [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cc9d-146"><span id="CACHEGROUP_SEARCH_ALL"></span><span id="cachegroup_search_all"></span>**cachegroup- \_ Suche \_ alle**</span><span class="sxs-lookup"><span data-stu-id="0cc9d-146"><span id="CACHEGROUP_SEARCH_ALL"></span><span id="cachegroup_search_all"></span>**CACHEGROUP\_SEARCH\_ALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cc9d-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0cc9d-147">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="0cc9d-148">Gibt an, dass alle Cache Gruppen im System des Benutzers aufgezählt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0cc9d-148">Indicates that all of the cache groups in the user's system should be enumerated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cc9d-149"><span id="CACHEGROUP_SEARCH_BYURL"></span><span id="cachegroup_search_byurl"></span>**cachegroup \_ - \_ suchbyurl**</span><span class="sxs-lookup"><span data-stu-id="0cc9d-149"><span id="CACHEGROUP_SEARCH_BYURL"></span><span id="cachegroup_search_byurl"></span>**CACHEGROUP\_SEARCH\_BYURL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cc9d-150">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0cc9d-150">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="0cc9d-151">Derzeit nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="0cc9d-151">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cc9d-152"><span id="CACHEGROUP_TYPE_INVALID"></span><span id="cachegroup_type_invalid"></span>**cachegroup- \_ Typ ist \_ ungültig.**</span><span class="sxs-lookup"><span data-stu-id="0cc9d-152"><span id="CACHEGROUP_TYPE_INVALID"></span><span id="cachegroup_type_invalid"></span>**CACHEGROUP\_TYPE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cc9d-153">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0cc9d-153">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="0cc9d-154">Gibt an, dass der Cache Gruppentyp ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="0cc9d-154">Indicates that the cache group type is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cc9d-155"><span id="GROUP_OWNER_STORAGE_SIZE"></span><span id="group_owner_storage_size"></span>**\_ \_ Speicher \_ Größe des Gruppen Besitzers**</span><span class="sxs-lookup"><span data-stu-id="0cc9d-155"><span id="GROUP_OWNER_STORAGE_SIZE"></span><span id="group_owner_storage_size"></span>**GROUP\_OWNER\_STORAGE\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cc9d-156">0x00000004</span><span class="sxs-lookup"><span data-stu-id="0cc9d-156">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="0cc9d-157">Länge des Gruppenbesitzer-Speicherarrays.</span><span class="sxs-lookup"><span data-stu-id="0cc9d-157">Length of the group owner storage array.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cc9d-158"><span id="GROUPNAME_MAX_LENGTH"></span><span id="groupname_max_length"></span>**\_Maximale Länge für GroupName \_**</span><span class="sxs-lookup"><span data-stu-id="0cc9d-158"><span id="GROUPNAME_MAX_LENGTH"></span><span id="groupname_max_length"></span>**GROUPNAME\_MAX\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cc9d-159">0x00000078</span><span class="sxs-lookup"><span data-stu-id="0cc9d-159">0x00000078</span></span>
</dt> <dt>



<span data-ttu-id="0cc9d-160">Maximale Anzahl von Zeichen, die für einen Cache Gruppennamen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="0cc9d-160">Maximum number of characters allowed for a cache group name.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0cc9d-161">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0cc9d-161">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0cc9d-162">WinInet unterstützt keine Server Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="0cc9d-162">WinINet does not support server implementations.</span></span> <span data-ttu-id="0cc9d-163">Außerdem sollte Sie nicht von einem Dienst verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0cc9d-163">In addition, it should not be used from a service.</span></span> <span data-ttu-id="0cc9d-164">Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="0cc9d-164">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0cc9d-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0cc9d-165">Requirements</span></span>



| <span data-ttu-id="0cc9d-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0cc9d-166">Requirement</span></span> | <span data-ttu-id="0cc9d-167">Wert</span><span class="sxs-lookup"><span data-stu-id="0cc9d-167">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0cc9d-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0cc9d-168">Minimum supported client</span></span><br/> | <span data-ttu-id="0cc9d-169">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0cc9d-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0cc9d-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0cc9d-170">Minimum supported server</span></span><br/> | <span data-ttu-id="0cc9d-171">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0cc9d-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0cc9d-172">Header</span><span class="sxs-lookup"><span data-stu-id="0cc9d-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cc9d-173"><dt>Wininet. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cc9d-173"><dt>Wininet.h</dt></span></span> </dl> |



 

