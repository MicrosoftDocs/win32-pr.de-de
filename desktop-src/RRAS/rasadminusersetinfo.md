---
title: Rasadminusermentinfo-Funktion (rassapi. h)
description: Die rasadminusersetinfo-Funktion legt die RAS-Berechtigungen und die Rückruf Telefonnummer für einen angegebenen Benutzer fest.
ms.assetid: 5b049dfd-ecc8-47e4-82cc-71a875752714
keywords:
- Rasadminusereintinfo-Funktion (RAS)
topic_type:
- apiref
api_name:
- RasAdminUserSetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16d35f62713a3f4669db191891d2fb6b1694cabe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364962"
---
# <a name="rasadminusersetinfo-function"></a><span data-ttu-id="a72e0-104">Rasadminusermentinfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="a72e0-104">RasAdminUserSetInfo function</span></span>

<span data-ttu-id="a72e0-105">\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4,0 bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="a72e0-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="a72e0-106">Es wird ein Fehler zurückgegeben, \_ \_ \_ der auf Windows Server 2003 nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="a72e0-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="a72e0-107">Anwendungen sollten die [**mpradminusermentinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) -Funktion verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="a72e0-107">Applications should use the [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) function.\]</span></span>

<span data-ttu-id="a72e0-108">Die **rasadminusersetinfo** -Funktion legt die RAS-Berechtigungen und die Rückruf Telefonnummer für einen angegebenen Benutzer fest.</span><span class="sxs-lookup"><span data-stu-id="a72e0-108">The **RasAdminUserSetInfo** function sets the RAS permissions and call-back phone number for a specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="a72e0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a72e0-109">Syntax</span></span>


```C++
DWORD RasAdminUserSetInfo(
  _In_ const WCHAR       *lpszUserAccountServer,
  _In_ const WCHAR       *lpszUser,
  _In_ const PRAS_USER_0 pRasUser0
);
```



## <a name="parameters"></a><span data-ttu-id="a72e0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a72e0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a72e0-111">*lpszuseraccountserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a72e0-111">*lpszUserAccountServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a72e0-112">Zeiger auf eine mit NULL endenden Unicode-Zeichenfolge, die den Namen des primären oder Sicherungs Domänen Controllers mit der Benutzerkonten Datenbank angibt.</span><span class="sxs-lookup"><span data-stu-id="a72e0-112">Pointer to a null-terminated Unicode string that specifies the name of the primary or backup domain controller that has the user account database.</span></span> <span data-ttu-id="a72e0-113">Verwenden Sie die [**rasadmingetuseraccountserver**](rasadmingetuseraccountserver.md) -Funktion, um diesen Servernamen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a72e0-113">Use the [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) function to get this server name.</span></span>

</dd> <dt>

<span data-ttu-id="a72e0-114">*lpszuser* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a72e0-114">*lpszUser* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a72e0-115">Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge, die den Namen des Benutzers angibt, für den RAS-Informationen festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a72e0-115">Pointer to a null-terminated Unicode string that specifies the name of the user for whom RAS information is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="a72e0-116">*pRasUser0* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a72e0-116">*pRasUser0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a72e0-117">Ein Zeiger auf die [**RAS- \_ Benutzer- \_ 0**](ras-user-0-str.md) -Struktur, die die neuen RAS-Daten für den angegebenen Benutzer angibt.</span><span class="sxs-lookup"><span data-stu-id="a72e0-117">Pointer to the [**RAS\_USER\_0**](ras-user-0-str.md) structure that specifies the new RAS data for the specified user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a72e0-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a72e0-118">Return value</span></span>

<span data-ttu-id="a72e0-119">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a72e0-119">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="a72e0-120">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Fehlercodes sein.</span><span class="sxs-lookup"><span data-stu-id="a72e0-120">If the function fails, the return value can be one of the following error codes.</span></span>



| <span data-ttu-id="a72e0-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a72e0-121">Value</span></span>                                                                                                           | <span data-ttu-id="a72e0-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a72e0-122">Description</span></span>                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a72e0-123"><dt>**\_ungültige \_ Daten**</dt></span><span class="sxs-lookup"><span data-stu-id="a72e0-123"><dt>**ERROR\_INVALID\_DATA**</dt></span></span> </dl>             | <span data-ttu-id="a72e0-124">Der *pRasUser0* -Puffer enthält ungültige Daten.</span><span class="sxs-lookup"><span data-stu-id="a72e0-124">The *pRasUser0* buffer contains invalid data.</span></span><br/>                                        |
| <dl> <span data-ttu-id="a72e0-125"><dt>**Fehler \_ ungültige \_ Rückruf \_ Nummer.**</dt></span><span class="sxs-lookup"><span data-stu-id="a72e0-125"><dt>**ERROR\_INVALID\_CALLBACK\_NUMBER**</dt></span></span> </dl> | <span data-ttu-id="a72e0-126">Die im *pRasUser0* -Puffer angegebene Rückrufnummer enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="a72e0-126">The callback number specified in the *pRasUser0* buffer contains invalid characters.</span></span><br/> |
| <dl> <span data-ttu-id="a72e0-127"><dt>**NERR \_ Buf-osmall**</dt></span><span class="sxs-lookup"><span data-stu-id="a72e0-127"><dt>**NERR\_BufTooSmall** </dt></span></span> </dl>               | <span data-ttu-id="a72e0-128">Nicht genügend Arbeitsspeicher zum Ausführen dieser Funktion.</span><span class="sxs-lookup"><span data-stu-id="a72e0-128">Insufficient memory to perform this function.</span></span><br/>                                        |



 

<span data-ttu-id="a72e0-129">Es sind keine erweiterten Fehlerinformationen für diese Funktion vorhanden. " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)" nicht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a72e0-129">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="a72e0-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a72e0-130">Remarks</span></span>

<span data-ttu-id="a72e0-131">Beim Festlegen der RAS-Berechtigungen für einen Benutzer muss der **bfprivilege** -Member der [**RAS-Benutzer- \_ \_ 0**](ras-user-0-str.md) -Struktur mindestens eines der rückgabeflags angeben.</span><span class="sxs-lookup"><span data-stu-id="a72e0-131">When setting the RAS permissions for a user, the **bfPrivilege** member of the [**RAS\_USER\_0**](ras-user-0-str.md) structure must specify at least one of the call-back flags.</span></span> <span data-ttu-id="a72e0-132">Um z. b. die Berechtigungen eines Benutzers so festzulegen, dass Einwählberechtigungen, aber keine Rückruf Berechtigung zulässig sind, legen Sie **bfprivilege** auf raspriv \_ dialinprivilege \| raspriv \_ NoCallback fest.</span><span class="sxs-lookup"><span data-stu-id="a72e0-132">For example, to set a user's privileges to allow dial-in privilege but no call-back privilege, set **bfPrivilege** to RASPRIV\_DialinPrivilege \| RASPRIV\_NoCallback.</span></span>

## <a name="requirements"></a><span data-ttu-id="a72e0-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a72e0-133">Requirements</span></span>



| <span data-ttu-id="a72e0-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a72e0-134">Requirement</span></span> | <span data-ttu-id="a72e0-135">Wert</span><span class="sxs-lookup"><span data-stu-id="a72e0-135">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a72e0-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="a72e0-136">End of client support</span></span><br/> | <span data-ttu-id="a72e0-137">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a72e0-137">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="a72e0-138">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="a72e0-138">End of server support</span></span><br/> | <span data-ttu-id="a72e0-139">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a72e0-139">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="a72e0-140">Header</span><span class="sxs-lookup"><span data-stu-id="a72e0-140">Header</span></span><br/>                | <dl> <span data-ttu-id="a72e0-141"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a72e0-141"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="a72e0-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a72e0-142">Library</span></span><br/>               | <dl> <span data-ttu-id="a72e0-143"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a72e0-143"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="a72e0-144">DLL</span><span class="sxs-lookup"><span data-stu-id="a72e0-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a72e0-145"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a72e0-145"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a72e0-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a72e0-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a72e0-147">Remote Zugriffs Dienst (RAS) (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="a72e0-147">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="a72e0-148">RAS-Server-Verwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="a72e0-148">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="a72e0-149">**RAS- \_ Benutzer \_ 0**</span><span class="sxs-lookup"><span data-stu-id="a72e0-149">**RAS\_USER\_0**</span></span>](ras-user-0-str.md)
</dt> <dt>

[<span data-ttu-id="a72e0-150">**Rasadmingetuseraccountserver**</span><span class="sxs-lookup"><span data-stu-id="a72e0-150">**RasAdminGetUserAccountServer**</span></span>](rasadmingetuseraccountserver.md)
</dt> <dt>

[<span data-ttu-id="a72e0-151">**Rasadminusergetinfo**</span><span class="sxs-lookup"><span data-stu-id="a72e0-151">**RasAdminUserGetInfo**</span></span>](rasadminusergetinfo.md)
</dt> </dl>

 

