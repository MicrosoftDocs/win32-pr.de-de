---
title: Rasadminusergetinfo-Funktion (rassapi. h)
description: Die rasadminusergetinfo-Funktion Ruft die RAS-Berechtigungen und Rückruf Telefonnummer-Informationen für einen angegebenen Benutzer ab.
ms.assetid: 178ff775-9cd2-43f0-9a9a-dbae337c5fe8
keywords:
- Rasadminusergetinfo-Funktion (RAS)
topic_type:
- apiref
api_name:
- RasAdminUserGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89fe08a918a958ffb5a656ce2c76cecec31cbb61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352981"
---
# <a name="rasadminusergetinfo-function"></a><span data-ttu-id="ac201-104">Rasadminusergetinfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="ac201-104">RasAdminUserGetInfo function</span></span>

<span data-ttu-id="ac201-105">\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4,0 bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ac201-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="ac201-106">Es wird ein Fehler zurückgegeben, \_ \_ \_ der auf Windows Server 2003 nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="ac201-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="ac201-107">Anwendungen sollten die [**mpradminusergetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) -Funktion verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="ac201-107">Applications should use the [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) function.\]</span></span>

<span data-ttu-id="ac201-108">Die **rasadminusergetinfo** -Funktion Ruft die RAS-Berechtigungen und Rückruf Telefonnummer-Informationen für einen angegebenen Benutzer ab.</span><span class="sxs-lookup"><span data-stu-id="ac201-108">The **RasAdminUserGetInfo** function gets the RAS permissions and callback phone number information for a specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac201-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac201-109">Syntax</span></span>


```C++
DWORD RasAdminUserGetInfo(
  _In_ const WCHAR       *lpszUserAccountServer,
  _In_ const WCHAR       *lpszUser,
             PRAS_USER_0 pRasUser0
);
```



## <a name="parameters"></a><span data-ttu-id="ac201-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac201-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac201-111">*lpszuseraccountserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac201-111">*lpszUserAccountServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac201-112">Zeiger auf eine mit NULL endenden Unicode-Zeichenfolge, die den Namen des primären oder Sicherungs Domänen Controllers mit der Benutzerkonten Datenbank angibt.</span><span class="sxs-lookup"><span data-stu-id="ac201-112">Pointer to a null-terminated Unicode string that specifies the name of the primary or backup domain controller that has the user account database.</span></span> <span data-ttu-id="ac201-113">Verwenden Sie die [**rasadmingetuseraccountserver**](rasadmingetuseraccountserver.md) -Funktion, um diesen Servernamen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ac201-113">Use the [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) function to get this server name.</span></span>

</dd> <dt>

<span data-ttu-id="ac201-114">*lpszuser* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac201-114">*lpszUser* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac201-115">Ein Zeiger auf eine mit NULL endenden Unicode-Zeichenfolge, die den Namen des Benutzers angibt, für den RAS-Informationen zu erhalten sind.</span><span class="sxs-lookup"><span data-stu-id="ac201-115">Pointer to a null-terminated Unicode string that specifies the name of the user for whom to get RAS information.</span></span>

</dd> <dt>

<span data-ttu-id="ac201-116">*pRasUser0*</span><span class="sxs-lookup"><span data-stu-id="ac201-116">*pRasUser0*</span></span> 
</dt> <dd>

<span data-ttu-id="ac201-117">Ein Zeiger auf die [**RAS- \_ Benutzer- \_ 0**](ras-user-0-str.md) -Struktur, die die RAS-Daten für den angegebenen Benutzer empfängt.</span><span class="sxs-lookup"><span data-stu-id="ac201-117">Pointer to the [**RAS\_USER\_0**](ras-user-0-str.md) structure that receives the RAS data for the specified user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac201-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac201-118">Return value</span></span>

<span data-ttu-id="ac201-119">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="ac201-119">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="ac201-120">Wenn die Funktion fehlschlägt, kann der folgende Fehlercode als Rückgabewert zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ac201-120">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="ac201-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ac201-121">Value</span></span>                                                                                            | <span data-ttu-id="ac201-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ac201-122">Meaning</span></span>                                                  |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="ac201-123"><dt>**Nr \_ buf**</dt></span><span class="sxs-lookup"><span data-stu-id="ac201-123"><dt>**NERR\_BufTooSmall**</dt></span></span> </dl> | <span data-ttu-id="ac201-124">Nicht genügend Arbeitsspeicher zum Ausführen dieser Funktion.</span><span class="sxs-lookup"><span data-stu-id="ac201-124">Insufficient memory to perform this function.</span></span><br/> |



 

<span data-ttu-id="ac201-125">Es sind keine erweiterten Fehlerinformationen für diese Funktion vorhanden. " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)" nicht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ac201-125">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac201-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac201-126">Requirements</span></span>



| <span data-ttu-id="ac201-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac201-127">Requirement</span></span> | <span data-ttu-id="ac201-128">Wert</span><span class="sxs-lookup"><span data-stu-id="ac201-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac201-129">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ac201-129">End of client support</span></span><br/> | <span data-ttu-id="ac201-130">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ac201-130">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="ac201-131">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="ac201-131">End of server support</span></span><br/> | <span data-ttu-id="ac201-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ac201-132">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="ac201-133">Header</span><span class="sxs-lookup"><span data-stu-id="ac201-133">Header</span></span><br/>                | <dl> <span data-ttu-id="ac201-134"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac201-134"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="ac201-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ac201-135">Library</span></span><br/>               | <dl> <span data-ttu-id="ac201-136"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac201-136"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="ac201-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ac201-137">DLL</span></span><br/>                   | <dl> <span data-ttu-id="ac201-138"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac201-138"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac201-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac201-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac201-140">Remote Zugriffs Dienst (RAS) (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="ac201-140">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="ac201-141">RAS-Server-Verwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="ac201-141">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="ac201-142">**RAS- \_ Benutzer \_ 0**</span><span class="sxs-lookup"><span data-stu-id="ac201-142">**RAS\_USER\_0**</span></span>](ras-user-0-str.md)
</dt> <dt>

[<span data-ttu-id="ac201-143">**Rasadmingetuseraccountserver**</span><span class="sxs-lookup"><span data-stu-id="ac201-143">**RasAdminGetUserAccountServer**</span></span>](rasadmingetuseraccountserver.md)
</dt> <dt>

[<span data-ttu-id="ac201-144">**Rasadminusereintinfo**</span><span class="sxs-lookup"><span data-stu-id="ac201-144">**RasAdminUserSetInfo**</span></span>](rasadminusersetinfo.md)
</dt> </dl>

 

