---
title: Rasadmingetuseraccountserver-Funktion (rassapi. h)
description: Die rasadmingetuseraccountserver-Funktion Ruft den Namen des Servers ab, der über die Benutzerkonten Datenbank verfügt. Verwenden Sie den zurückgegebenen Servernamen in den rasadminusergetinfo-und rasadminusersetinfo-Funktionen, um Informationen zu einem angegebenen Benutzer abzurufen oder festzulegen.
ms.assetid: db91aa48-32af-49ac-87ed-8c484926ca15
keywords:
- Rasadmingetuseraccountserver-Funktion (RAS)
topic_type:
- apiref
api_name:
- RasAdminGetUserAccountServer
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c506287d94c5ec64445c74d8364a04db98100751
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354164"
---
# <a name="rasadmingetuseraccountserver-function"></a><span data-ttu-id="bf7cd-105">Rasadmingetuseraccountserver-Funktion</span><span class="sxs-lookup"><span data-stu-id="bf7cd-105">RasAdminGetUserAccountServer function</span></span>

<span data-ttu-id="bf7cd-106">\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4,0 bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-106">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="bf7cd-107">Es wird ein Fehler zurückgegeben, \_ \_ \_ der auf Windows Server 2003 nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-107">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="bf7cd-108">Anwendungen sollten die [**mpradmingetpdcserver**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) -Funktion verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="bf7cd-108">Applications should use the [**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) function.\]</span></span>

<span data-ttu-id="bf7cd-109">Die **rasadmingetuseraccountserver** -Funktion Ruft den Namen des Servers ab, der über die Benutzerkonten Datenbank verfügt.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-109">The **RasAdminGetUserAccountServer** function retrieves the name of the server that has the user account database.</span></span> <span data-ttu-id="bf7cd-110">Verwenden Sie den zurückgegebenen Servernamen in den [**rasadminusergetinfo**](rasadminusergetinfo.md) -und [**rasadminusersetinfo**](rasadminusersetinfo.md) -Funktionen, um Informationen zu einem angegebenen Benutzer abzurufen oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-110">Use the returned server name in the [**RasAdminUserGetInfo**](rasadminusergetinfo.md) and [**RasAdminUserSetInfo**](rasadminusersetinfo.md) functions to get or set information about a specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf7cd-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf7cd-111">Syntax</span></span>


```C++
DWORD RasAdminGetUserAccountServer(
  _In_  const WCHAR  *lpszDomain,
  _In_  const WCHAR  *lpszServer,
  _Out_       LPWSTR lpszUserAccountServer
);
```



## <a name="parameters"></a><span data-ttu-id="bf7cd-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf7cd-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf7cd-113">*lpszdomain* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf7cd-113">*lpszDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf7cd-114">Zeiger auf eine mit **null** endenden Unicode-Zeichenfolge, die den Namen der Domäne angibt, zu der der RAS-Server gehört.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-114">Pointer to a **null**-terminated Unicode string that specifies the name of the domain to which the RAS server belongs.</span></span> <span data-ttu-id="bf7cd-115">Dieser Parameter ist **null** für die RAS-Verwaltungs Anwendungen, die auf Arbeitsstationen oder Servern ausgeführt werden, die keine Mitglieder einer Domäne sind.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-115">This parameter is **NULL** for the RAS administration applications running on workstations or servers that are not members of a domain.</span></span> <span data-ttu-id="bf7cd-116">Wenn dieser Parameter **null** ist, muss der *lpszserver* -Parameter nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-116">If this parameter is **NULL**, the *lpszServer* parameter must be non-**NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bf7cd-117">*lpszserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf7cd-117">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf7cd-118">Zeiger auf eine mit **null** endenden Unicode-Zeichenfolge, die den Namen des RAS-Servers angibt.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-118">Pointer to a **null**-terminated Unicode string that specifies the name of the RAS server.</span></span> <span data-ttu-id="bf7cd-119">Geben Sie den Namen mit führenden " \\ \\ " Zeichen im folgenden Format an: \\ \\ *Servername*.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-119">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span> <span data-ttu-id="bf7cd-120">Dieser Parameter kann **null** sein, wenn der *lpszdomain* -Parameter nicht **null** ist.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-120">This parameter can be **NULL** if the *lpszDomain* parameter is not **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bf7cd-121">*lpszuseraccountserver* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bf7cd-121">*lpszUserAccountServer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf7cd-122">Ein Zeiger auf einen Puffer, der eine **null**-terminierte Unicode-Zeichenfolge empfängt, die den Namen eines Domänen Controllers mit der Benutzerkonten Datenbank angibt.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-122">Pointer to a buffer that receives a **null**-terminated Unicode string that specifies the name of a domain controller that has the user account database.</span></span> <span data-ttu-id="bf7cd-123">Der Puffer sollte groß genug sein, um den Servernamen zu speichern (unclen + 1).</span><span class="sxs-lookup"><span data-stu-id="bf7cd-123">The buffer should be big enough to hold the server name (UNCLEN +1).</span></span> <span data-ttu-id="bf7cd-124">Die Funktion stellt den zurückgegebenen Servernamen mit führenden " \\ \\ "-Zeichen im Format " \\ \\ *Server* Name" als Präfix bereit.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-124">The function prefixes the returned server name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf7cd-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bf7cd-125">Return value</span></span>

<span data-ttu-id="bf7cd-126">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-126">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="bf7cd-127">Wenn die Funktion fehlschlägt, kann der folgende Fehlercode als Rückgabewert zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-127">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="bf7cd-128">Wert</span><span class="sxs-lookup"><span data-stu-id="bf7cd-128">Value</span></span>                                                                                                    | <span data-ttu-id="bf7cd-129">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="bf7cd-129">Meaning</span></span>                                                     |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="bf7cd-130"><dt>**Fehler bei \_ ungültigem \_ Parameter**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7cd-130"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="bf7cd-131">Sowohl " *lpszdomain* " als auch " *lpszserver* " sind **null**.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-131">Both *lpszDomain* and *lpszServer* are **NULL**.</span></span><br/> |



 

<span data-ttu-id="bf7cd-132">Es sind keine erweiterten Fehlerinformationen für diese Funktion vorhanden. " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)" nicht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-132">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="bf7cd-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf7cd-133">Remarks</span></span>

<span data-ttu-id="bf7cd-134">Die **rasadmingetuseraccountserver** -Funktion Ruft den Namen des Servers mit der Benutzerkonten Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-134">The **RasAdminGetUserAccountServer** function obtains the name of the server with the user accounts database.</span></span> <span data-ttu-id="bf7cd-135">Diese Funktion erfordert den Namen des RAS-Servers oder den Namen der Domäne, in der sich der RAS-Server befindet.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-135">This function requires the name of the RAS server or the name of the domain in which the RAS server resides.</span></span>

<span data-ttu-id="bf7cd-136">Der *lpszdomain* -Parameter muss einen gültigen Domänen Namen angeben.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-136">The *lpszDomain* parameter should specify a valid domain name.</span></span> <span data-ttu-id="bf7cd-137">Dieser Parameter ist **null** für RAS-Verwaltungs Anwendungen, die auf Servern ausgeführt werden, die nicht Mitglied einer Domäne sind (z. b. befindet sich der Server in seiner eigenen Arbeitsgruppe).</span><span class="sxs-lookup"><span data-stu-id="bf7cd-137">This parameter is **NULL** for RAS administration applications running on servers that are not members of a domain (for example, the server is in its own workgroup).</span></span> <span data-ttu-id="bf7cd-138">In diesem Fall muss der *lpszserver* -Parameter den Servernamen angeben.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-138">In this case, the *lpszServer* parameter must specify the server name.</span></span> <span data-ttu-id="bf7cd-139">Um den Servernamen abzurufen, nennen Sie die [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-139">To get the server name, call the [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea) function.</span></span> <span data-ttu-id="bf7cd-140">Stellen Sie sicher, dass Sie dem Servernamen die Zeichen "" als Präfix voranstellen \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="bf7cd-140">Be sure to prefix the server name with the "\\\\" characters.</span></span>

<span data-ttu-id="bf7cd-141">Handelt es sich bei dem von *lpszserver* angegebenen Servernamen um einen eigenständigen Server (d. h., der Server oder die Arbeitsstation ist kein Mitglied einer Domäne), wird der Servername selbst im *lpszuseraccountserver* -Puffer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-141">If the server name specified by *lpszServer* is a stand-alone server (that is, the server or workstation is not a member of a domain), then the server name itself is returned in the *lpszUserAccountServer* buffer.</span></span>

<span data-ttu-id="bf7cd-142">Verwenden Sie dann den Namen des Benutzerkonto Servers in einem aufzurufenden Befehl der Funktion [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) , um die Benutzer in der Benutzerkonten Datenbank aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-142">Then use the name of the user account server in a call to the [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) function to enumerate the users in the user account database.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf7cd-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bf7cd-143">Requirements</span></span>



| <span data-ttu-id="bf7cd-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bf7cd-144">Requirement</span></span> | <span data-ttu-id="bf7cd-145">Wert</span><span class="sxs-lookup"><span data-stu-id="bf7cd-145">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf7cd-146">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="bf7cd-146">End of client support</span></span><br/> | <span data-ttu-id="bf7cd-147">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bf7cd-147">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="bf7cd-148">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="bf7cd-148">End of server support</span></span><br/> | <span data-ttu-id="bf7cd-149">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bf7cd-149">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="bf7cd-150">Header</span><span class="sxs-lookup"><span data-stu-id="bf7cd-150">Header</span></span><br/>                | <dl> <span data-ttu-id="bf7cd-151"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf7cd-151"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="bf7cd-152">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bf7cd-152">Library</span></span><br/>               | <dl> <span data-ttu-id="bf7cd-153"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf7cd-153"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="bf7cd-154">DLL</span><span class="sxs-lookup"><span data-stu-id="bf7cd-154">DLL</span></span><br/>                   | <dl> <span data-ttu-id="bf7cd-155"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf7cd-155"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf7cd-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf7cd-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf7cd-157">Remote Zugriffs Dienst (RAS) (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="bf7cd-157">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="bf7cd-158">RAS-Server-Verwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="bf7cd-158">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="bf7cd-159">**GetComputerName**</span><span class="sxs-lookup"><span data-stu-id="bf7cd-159">**GetComputerName**</span></span>](/windows/win32/api/winbase/nf-winbase-getcomputernamea)
</dt> <dt>

[<span data-ttu-id="bf7cd-160">**Rasadminusergetinfo**</span><span class="sxs-lookup"><span data-stu-id="bf7cd-160">**RasAdminUserGetInfo**</span></span>](rasadminusergetinfo.md)
</dt> <dt>

[<span data-ttu-id="bf7cd-161">**Rasadminusereintinfo**</span><span class="sxs-lookup"><span data-stu-id="bf7cd-161">**RasAdminUserSetInfo**</span></span>](rasadminusersetinfo.md)
</dt> </dl>

 

