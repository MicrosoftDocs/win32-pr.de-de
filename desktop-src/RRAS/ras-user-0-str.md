---
title: RAS_USER_0 Struktur (rassapi. h)
description: Die Struktur "RAS \_ User \_ 0" wird in den rasadminuserminfo-und rasadminusergetinfo-Funktionen verwendet, um Informationen zu einem Benutzer anzugeben.
ms.assetid: a2d4a935-f46d-4bc2-ada8-beaa3ac74834
keywords:
- RAS_USER_0 Struktur-RAS
- PRAS_USER_0-Struktur Zeiger RAS
topic_type:
- apiref
api_name:
- RAS_USER_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c79a6b946ed9d10cd2bfc989f8cde27fad2ffa92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517717"
---
# <a name="ras_user_0-structure"></a><span data-ttu-id="749a3-105">RAS \_ User \_ 0-Struktur</span><span class="sxs-lookup"><span data-stu-id="749a3-105">RAS\_USER\_0 structure</span></span>

<span data-ttu-id="749a3-106">\[Diese Version der **RAS- \_ Benutzer- \_ 0** -Struktur wird ab Windows Vista nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="749a3-106">\[This version of the **RAS\_USER\_0** structure is not supported as of Windows Vista.</span></span> <span data-ttu-id="749a3-107">Verwenden Sie stattdessen den neueren [**RAS- \_ Benutzer \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) , der in MPRAPI. h definiert ist.\]</span><span class="sxs-lookup"><span data-stu-id="749a3-107">Use the newer [**RAS\_USER\_0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) defined in mprapi.h instead.\]</span></span>

<span data-ttu-id="749a3-108">Die Struktur " **RAS \_ User \_ 0** " wird in den [**rasadminuserminfo**](rasadminusersetinfo.md) -und [**rasadminusergetinfo**](rasadminusergetinfo.md) -Funktionen verwendet, um Informationen zu einem Benutzer anzugeben.</span><span class="sxs-lookup"><span data-stu-id="749a3-108">The **RAS\_USER\_0** structure is used in the [**RasAdminUserSetInfo**](rasadminusersetinfo.md) and [**RasAdminUserGetInfo**](rasadminusergetinfo.md) functions to specify information about a user.</span></span>

## <a name="syntax"></a><span data-ttu-id="749a3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="749a3-109">Syntax</span></span>


```C++
typedef struct _RAS_USER_0 {
  BYTE  bfPrivilege;
  WCHAR szPhoneNumber[RASSAPI_MAX_PHONENUMBER_SIZE + 1];
} RAS_USER_0, *PRAS_USER_0;
```



## <a name="members"></a><span data-ttu-id="749a3-110">Member</span><span class="sxs-lookup"><span data-stu-id="749a3-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="749a3-111">**BF-Berechtigung**</span><span class="sxs-lookup"><span data-stu-id="749a3-111">**bfPrivilege**</span></span>
</dt> <dd>

<span data-ttu-id="749a3-112">Ein Satz von Bitflags, die die RAS-Berechtigungen des Benutzers angeben.</span><span class="sxs-lookup"><span data-stu-id="749a3-112">A set of bit flags that specify the RAS privileges of the user.</span></span> <span data-ttu-id="749a3-113">Dieser Member kann eine Kombination aus dem raspriv \_ -Flag "dialinprivilege" und einem der rückgabeflags sein.</span><span class="sxs-lookup"><span data-stu-id="749a3-113">This member can be a combination of the RASPRIV\_DialinPrivilege flag and one of the call-back flags.</span></span> <span data-ttu-id="749a3-114">Verwenden Sie die raspriv \_ CallbackType Mask, um den Typ der dem Benutzer bereitgestellten Rückruf Berechtigung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="749a3-114">Use the RASPRIV\_CallbackType mask to identify the type of call-back privilege provided to the user.</span></span> <span data-ttu-id="749a3-115">Die folgenden Flags sind definiert.</span><span class="sxs-lookup"><span data-stu-id="749a3-115">The following flags are defined.</span></span>



| <span data-ttu-id="749a3-116">Wert</span><span class="sxs-lookup"><span data-stu-id="749a3-116">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="749a3-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="749a3-117">Meaning</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="RASPRIV_NoCallback"></span><span id="raspriv_nocallback"></span><span id="RASPRIV_NOCALLBACK"></span><dl> <span data-ttu-id="749a3-118"><dt>**Raspriv \_ NoCallback**</dt></span><span class="sxs-lookup"><span data-stu-id="749a3-118"><dt>**RASPRIV\_NoCallback**</dt></span></span> </dl>                             | <span data-ttu-id="749a3-119">Der Benutzer hat keine Rückruf Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="749a3-119">The user has no call-back privilege.</span></span><br/>                                               |
| <span id="RASPRIV_AdminSetCallback"></span><span id="raspriv_adminsetcallback"></span><span id="RASPRIV_ADMINSETCALLBACK"></span><dl> <span data-ttu-id="749a3-120"><dt>**Raspriv \_ adminsetcallback**</dt></span><span class="sxs-lookup"><span data-stu-id="749a3-120"><dt>**RASPRIV\_AdminSetCallback**</dt></span></span> </dl>     | <span data-ttu-id="749a3-121">Das Benutzerkonto ist so konfiguriert, dass der Administrator die Rückrufnummer festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="749a3-121">The user account is configured to have the administrator set the call-back number.</span></span><br/> |
| <span id="RASPRIV_CallerSetCallback"></span><span id="raspriv_callersetcallback"></span><span id="RASPRIV_CALLERSETCALLBACK"></span><dl> <span data-ttu-id="749a3-122"><dt>**Raspriv \_ callersetcallback**</dt></span><span class="sxs-lookup"><span data-stu-id="749a3-122"><dt>**RASPRIV\_CallerSetCallback**</dt></span></span> </dl> | <span data-ttu-id="749a3-123">Der Remote Benutzer kann beim Einwählen eine Telefonnummer für den Rückruf angeben.</span><span class="sxs-lookup"><span data-stu-id="749a3-123">The remote user can specify a call-back phone number when dialing in.</span></span><br/>              |
| <span id="RASPRIV_DialinPrivilege"></span><span id="raspriv_dialinprivilege"></span><span id="RASPRIV_DIALINPRIVILEGE"></span><dl> <span data-ttu-id="749a3-124"><dt>**Raspriv- \_ dialinprivilege**</dt></span><span class="sxs-lookup"><span data-stu-id="749a3-124"><dt>**RASPRIV\_DialinPrivilege**</dt></span></span> </dl>         | <span data-ttu-id="749a3-125">Der Benutzer verfügt über die Berechtigung zum Einwählen dieses Servers.</span><span class="sxs-lookup"><span data-stu-id="749a3-125">The user has permission to dial in to this server.</span></span><br/>                                 |



 

<span data-ttu-id="749a3-126">Geben Sie eines der rückgabeflags im aufrufsbefehl der [**rasadminusereintinfo**](rasadminusersetinfo.md) -Funktion an.</span><span class="sxs-lookup"><span data-stu-id="749a3-126">Specify one of the call-back flags in the call to the [**RasAdminUserSetInfo**](rasadminusersetinfo.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="749a3-127">**szphonenumber**</span><span class="sxs-lookup"><span data-stu-id="749a3-127">**szPhoneNumber**</span></span>
</dt> <dd>

<span data-ttu-id="749a3-128">Eine NULL-terminierte Unicode-Zeichenfolge, die die Rückruf Telefonnummer des Benutzers angibt.</span><span class="sxs-lookup"><span data-stu-id="749a3-128">A null-terminated Unicode string that specifies the call-back phone number for the user.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="749a3-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="749a3-129">Requirements</span></span>



| <span data-ttu-id="749a3-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="749a3-130">Requirement</span></span> | <span data-ttu-id="749a3-131">Wert</span><span class="sxs-lookup"><span data-stu-id="749a3-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="749a3-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="749a3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="749a3-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="749a3-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="749a3-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="749a3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="749a3-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="749a3-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="749a3-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="749a3-136">End of client support</span></span><br/>    | <span data-ttu-id="749a3-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="749a3-137">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="749a3-138">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="749a3-138">End of server support</span></span><br/>    | <span data-ttu-id="749a3-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="749a3-139">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="749a3-140">Header</span><span class="sxs-lookup"><span data-stu-id="749a3-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="749a3-141"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="749a3-141"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="749a3-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="749a3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="749a3-143">Remote Zugriffs Dienst (RAS) (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="749a3-143">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="749a3-144">RAS-Server-Verwaltungsstrukturen</span><span class="sxs-lookup"><span data-stu-id="749a3-144">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="749a3-145">**Rasadminusergetinfo**</span><span class="sxs-lookup"><span data-stu-id="749a3-145">**RasAdminUserGetInfo**</span></span>](rasadminusergetinfo.md)
</dt> <dt>

[<span data-ttu-id="749a3-146">**Rasadminusereintinfo**</span><span class="sxs-lookup"><span data-stu-id="749a3-146">**RasAdminUserSetInfo**</span></span>](rasadminusersetinfo.md)
</dt> </dl>

 

 





