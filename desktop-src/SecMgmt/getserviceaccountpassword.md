---
description: Ruft das Dienst Konto Kennwort ab.
ms.assetid: B3D3842F-ACEB-4979-B336-BA3D0143044C
title: Getserviceaccountpassword-Funktion (secpkg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetServiceAccountPassword
api_type:
- HeaderDef
api_location:
- Secpkg.h
ms.openlocfilehash: 08719fb2b7e4a775df890f20cd640d059cb44475
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368913"
---
# <a name="getserviceaccountpassword-function"></a><span data-ttu-id="411fb-103">Getserviceaccountpassword-Funktion</span><span class="sxs-lookup"><span data-stu-id="411fb-103">GetServiceAccountPassword function</span></span>

<span data-ttu-id="411fb-104">Ruft das Dienst Konto Kennwort ab, das für SSPs ( [*Security Support Providers*](/windows/desktop/SecGloss/s-gly) ) verfügbar ist, z. b. Kerberos SSP.</span><span class="sxs-lookup"><span data-stu-id="411fb-104">Retrieves the service account password, available to [*security support providers*](/windows/desktop/SecGloss/s-gly) (SSPs), such as Kerberos SSP.</span></span>

## <a name="syntax"></a><span data-ttu-id="411fb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="411fb-105">Syntax</span></span>


```C++
NTSTATUS NTAPI GetServiceAccountPassword(
  _In_        PUNICODE_STRING AccountName,
  _In_opt_    PUNICODE_STRING DomainName,
  _In_        CRED_FETCH      CredFetch,
  _Inout_opt_ FILETIME        *FileTimeExpiry,
  _Out_       PUNICODE_STRING CurrentPassword,
  _Out_       PUNICODE_STRING PreviousPassword,
  _Out_opt_   FILETIME        *FileTimeCurrPwdValidForOutbound
);
```



## <a name="parameters"></a><span data-ttu-id="411fb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="411fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="411fb-107">*Accountname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="411fb-107">*AccountName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="411fb-108">Mit NULL endender Kontoname des Gruppen verwalteten Dienst Konto Kontos (GMSA).</span><span class="sxs-lookup"><span data-stu-id="411fb-108">Null-terminated account name of the Group Managed Service Account (gMSA) account.</span></span> <span data-ttu-id="411fb-109">Der Benutzername kann eine der folgenden Formen aufweisen:</span><span class="sxs-lookup"><span data-stu-id="411fb-109">The user name can be one of the following forms:</span></span>

-   <span data-ttu-id="411fb-110">SAM-Kontoname des GMSA.</span><span class="sxs-lookup"><span data-stu-id="411fb-110">SAM account name of the gMSA.</span></span>
-   <span data-ttu-id="411fb-111">Benutzername in einem voll qualifizierten Domänen Namen (Fully Qualified Domain Name, FQDN), z *. b. Domain Name \* **\\** _username_ oder **www.** _Domäne_* _. com \\_ \* _Name_.</span><span class="sxs-lookup"><span data-stu-id="411fb-111">User name in a fully qualified domain name (FQDN), such as *DomainName\***\\**_UserName_ or **www.**_domain_*_.com\\_\*_name_.</span></span> <span data-ttu-id="411fb-112">Der Benutzername darf nur ein SAM-Name sein.</span><span class="sxs-lookup"><span data-stu-id="411fb-112">The user name must be a SAM name only.</span></span> <span data-ttu-id="411fb-113">Der Domänen Name kann ein DNS-Name oder ein NetBIOS-Name sein.</span><span class="sxs-lookup"><span data-stu-id="411fb-113">The domain name can be a DNS name or a NetBIOS name.</span></span>
-   <span data-ttu-id="411fb-114">Impliziter Benutzer Prinzipal Name (User Principal Name, UPN) für das GMSA-Konto, z. b. *somename \* **@** _Domain_*_. com_\*, wobei die *Domäne \* \* *. com** der tatsächliche DNS-Domänen Name ist.</span><span class="sxs-lookup"><span data-stu-id="411fb-114">Implicit user principal name (UPN) for the gMSA account, for example, *SomeName\***@**_Domain_*_.com_\* where, according to the definition of an implicit UPN, the *Domain\*\*\*.com*\* is the actual domain DNS name.</span></span>

</dd> <dt>

<span data-ttu-id="411fb-115">*Domain Name* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="411fb-115">*DomainName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="411fb-116">Optionaler null-terminierter Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="411fb-116">Optional null-terminated domain name.</span></span> <span data-ttu-id="411fb-117">Dies ist nur gültig, wenn der *Accountname* -Parameter ein SAM-Konto Name ist.</span><span class="sxs-lookup"><span data-stu-id="411fb-117">This is valid only if the *AccountName* parameter is a SAM account name.</span></span> <span data-ttu-id="411fb-118">Der Domänen Name darf nur ein NetBIOS-Name oder ein voll qualifizierter Domänen Name (Fully Qualified Domain Name, FQDN) sein.</span><span class="sxs-lookup"><span data-stu-id="411fb-118">The domain name can only be a NetBIOS name or a fully qualified domain name (FQDN).</span></span>

</dd> <dt>

<span data-ttu-id="411fb-119">" *Fedfetch* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="411fb-119">*CredFetch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="411fb-120">Ein Wert der [**Fed- \_ Fetch-**](cred-fetch.md) Enumeration, der angibt, wie die Anmelde Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="411fb-120">A value of the [**CRED\_FETCH**](cred-fetch.md) enumeration that specifies how to retrieve the credential.</span></span>



| <span data-ttu-id="411fb-121">Wert</span><span class="sxs-lookup"><span data-stu-id="411fb-121">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="411fb-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="411fb-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span><dl> <span data-ttu-id="411fb-123"><dt>**"Kredfetchdefault"**</dt></span><span class="sxs-lookup"><span data-stu-id="411fb-123"><dt>**CredFetchDefault**</dt></span></span> </dl> | <span data-ttu-id="411fb-124">Das Betriebssystem versucht zunächst, das Kennwort aus dem lokalen Cache abzurufen, wenn das Kennwort nicht abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="411fb-124">The operating system first attempts to retrieve the password from the local cache if it is not time to fetch the password.</span></span> <span data-ttu-id="411fb-125">Wenn es an der Zeit ist, das Kennwort abzurufen, kontaktiert das Betriebssystem den Domänen Controller, andernfalls werden alle zwischengespeicherten Kenn Wörter mit dem Statuswert Erfolg zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="411fb-125">If it is time to fetch the password, then the operating system contacts the domain controller, otherwise, return any cached passwords with a status value of success.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span><dl> <span data-ttu-id="411fb-126"><dt>**"Kredfetchdpapi"**</dt></span><span class="sxs-lookup"><span data-stu-id="411fb-126"><dt>**CredFetchDPAPI**</dt></span></span> </dl>         | <span data-ttu-id="411fb-127">Gibt die lokalen DPAPI-Anmelde Informationen an den Aufrufer zurück.</span><span class="sxs-lookup"><span data-stu-id="411fb-127">Returns the local DPAPI credential to the caller.</span></span> <span data-ttu-id="411fb-128">Für SSPs ist es im Allgemeinen nicht erforderlich, diesen Wert zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="411fb-128">SSPs generally would not require use of this value.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span><dl> <span data-ttu-id="411fb-129"><dt>**"Kredfetchforced"**</dt></span><span class="sxs-lookup"><span data-stu-id="411fb-129"><dt>**CredFetchForced**</dt></span></span> </dl>     | <span data-ttu-id="411fb-130">Erzwingt, dass das Betriebssystem versucht, das Kennwort vom Domänen Controller zu lesen.</span><span class="sxs-lookup"><span data-stu-id="411fb-130">Forces the operating system to attempt to read the password from the domain controller.</span></span> <span data-ttu-id="411fb-131">Während der Kenn Wort rolloverzeit wurde das Kennwort möglicherweise auf dem Domänen Controller und anderen Mitglieds Hosts geändert, aber der GMSA-Mitglieds Host erkennt das Kennwort als noch gültig.</span><span class="sxs-lookup"><span data-stu-id="411fb-131">During the password rollover time, the password may have changed at the domain controller and other member hosts, but the gMSA member host recognizes the password as still valid.</span></span> <span data-ttu-id="411fb-132">Dies kann auf Probleme mit der Takt Abweichung zwischen verschiedenen Domänen Controllern zurückzuführen sein.</span><span class="sxs-lookup"><span data-stu-id="411fb-132">This can happen due to clock skew issues between different domain controllers.</span></span> <span data-ttu-id="411fb-133">Wenn dieser Wert angegeben ist, bestimmt das Betriebssystem, ob eine mögliche Kenn Wort Änderung aufgrund von Zeit Schiefe möglicherweise möglich ist, und ruft das Kennwort ab, wenn dies der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="411fb-133">When this value is specified, the operating system determines if there could be a possible password change due to clock skew and if so, retrieves the password.</span></span> <span data-ttu-id="411fb-134">Andernfalls werden die zwischengespeicherten Anmelde Informationen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="411fb-134">Otherwise, the cached credential is returned.</span></span> <span data-ttu-id="411fb-135">Wenn keine zwischengespeicherten Anmelde Informationen vorhanden sind, versucht das Betriebssystem, eine vom Domänen Controller zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="411fb-135">If there is no cached credential, then the operating system attempts to get one from the domain controller.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="411fb-136">*Filetimeablauf* \[ in, out, optional\]</span><span class="sxs-lookup"><span data-stu-id="411fb-136">*FileTimeExpiry* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="411fb-137">Wenn bei der Eingabe dieser Wert nicht NULL ist und keine **Datei** mit dem Wert 0 (null) ist, enthält *filetimestamp* die Ablaufzeit der Dienst Konto-Anmelde Informationen, die dem Aufrufer bekannt sind.</span><span class="sxs-lookup"><span data-stu-id="411fb-137">On input, if this value is nonnull and is not a zero **FILETIME**, *FileTimeExpiry* contains the expiry time of the service account credentials as known to the caller.</span></span> <span data-ttu-id="411fb-138">Wenn der *filetimesink* -Parameter mit einem der aktuellen Anmelde Informationen übereinstimmt, schlägt dieser Vorgang fehl.</span><span class="sxs-lookup"><span data-stu-id="411fb-138">If the *FileTimeExpiry* parameter is the same as one of the current credentials, this call fails.</span></span> <span data-ttu-id="411fb-139">Bei der Ausgabe enthält der *filetimesink* -Parameter die Ablaufzeit der zurückgegebenen Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="411fb-139">On output, the *FileTimeExpiry* parameter contains the expiry time of the credential being returned.</span></span>

</dd> <dt>

<span data-ttu-id="411fb-140">*CurrentPassword* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="411fb-140">*CurrentPassword* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="411fb-141">Das aktuelle Kennwort des GMSA.</span><span class="sxs-lookup"><span data-stu-id="411fb-141">The current password of the gMSA.</span></span>

</dd> <dt>

<span data-ttu-id="411fb-142">*Previouspassword* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="411fb-142">*PreviousPassword* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="411fb-143">Das vorherige Kennwort des GMSA.</span><span class="sxs-lookup"><span data-stu-id="411fb-143">The previous password of the gMSA.</span></span>

</dd> <dt>

<span data-ttu-id="411fb-144">*Filetimecurrpwdvalidforoutbound* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="411fb-144">*FileTimeCurrPwdValidForOutbound* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="411fb-145">Gibt die Zeit an, nach der das aktuelle Kennwort für ausgehende Anforderungen gültig ist.</span><span class="sxs-lookup"><span data-stu-id="411fb-145">Denotes the time after which the current password is valid for outbound requests.</span></span> <span data-ttu-id="411fb-146">Der Aufrufer sollte die aktuelle Uhrzeit mit diesem Wert vergleichen und das aktuelle Kennwort verwenden, das nur dann zurückgegeben wird, wenn die aktuelle Zeit größer oder gleich dem Wert ist, der von diesem Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="411fb-146">The caller should compare the current time with this value and use the current password returned only if the current time is greater than or equal to the value returned by this parameter.</span></span> <span data-ttu-id="411fb-147">Die Verwendung dieses Parameters wurde für Aufrufer entworfen, die keinen Wiederholungsversuch in der ausgehenden Logik haben, z. b. NTLM.</span><span class="sxs-lookup"><span data-stu-id="411fb-147">The use of this parameter is designed for callers that do not have retry in the outbound logic, for example, NTLM.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="411fb-148">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="411fb-148">Return value</span></span>

<span data-ttu-id="411fb-149">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert Status \_ Success.</span><span class="sxs-lookup"><span data-stu-id="411fb-149">If the function succeeds, the return value is STATUS\_SUCCESS.</span></span>

<span data-ttu-id="411fb-150">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein NTSTATUS-Code.</span><span class="sxs-lookup"><span data-stu-id="411fb-150">If the function fails, the return value is an NTSTATUS code.</span></span> <span data-ttu-id="411fb-151">Weitere Informationen finden Sie unter [Rückgabewerte von LSA-Richtlinien Funktionen](management-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="411fb-151">For more information, see [LSA Policy Function Return Values](management-return-values.md).</span></span>

<span data-ttu-id="411fb-152">Sie können die [**lsantstatustowinerror**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror) -Funktion verwenden, um den NTSTATUS-Code in einen Windows-Fehlercode zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="411fb-152">You can use the [**LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror) function to convert the NTSTATUS code to a Windows error code.</span></span>

<span data-ttu-id="411fb-153">Wenn Sie mit der Verwendung der in den Parametern *CurrentPassword* und *previouspassword* zurückgegebenen Puffer fertig sind, können Sie diese freigeben, indem Sie die [**freelsaheap**](/windows/desktop/api/ntlsa/nc-ntlsa-lsa_free_lsa_heap) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="411fb-153">When you have finished using the buffers returned in the *CurrentPassword* and *PreviousPassword* parameters, free them by calling the [**FreeLsaHeap**](/windows/desktop/api/ntlsa/nc-ntlsa-lsa_free_lsa_heap) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="411fb-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="411fb-154">Remarks</span></span>

<span data-ttu-id="411fb-155">Die **getserviceaccountpassword** -Funktion kann in den folgenden Szenarien aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="411fb-155">The **GetServiceAccountPassword** function can be called in the following scenarios:</span></span>

-   <span data-ttu-id="411fb-156">Aus den Anmelde Funktionen von Security Support Providers (SSP) sollte der SSP erkennen, dass das Kennwort des Dienst Kontos für die \_ \_ Anmeldung bei der Entität verwendet wird, und überprüfen, ob der Aufrufer über TCB-Berechtigungen verfügt oder ein Netzwerkdienst ist.</span><span class="sxs-lookup"><span data-stu-id="411fb-156">From the logon functions of Security Support Providers (SSP), the SSP should detect that the SERVICE\_ACCOUNT\_PASSWORD is being used to log on to the entity and should check that the caller has TCB privilege or is a network service.</span></span> <span data-ttu-id="411fb-157">Anschließend sollte der SSP zulassen, dass der Anmeldevorgang fortgesetzt wird, indem die aktuellen Anmelde Informationen abgerufen werden, indem die **getserviceaccountpassword** -Funktion mit dem **credfetchdefault** -Wert in der [**cred- \_ Fetch-**](cred-fetch.md) Enumeration aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="411fb-157">Then the SSP should allow the log on process to proceed by getting the latest credential by calling the **GetServiceAccountPassword** function with the **CredFetchDefault** value in the [**CRED\_FETCH**](cred-fetch.md) enumeration.</span></span>

-   <span data-ttu-id="411fb-158">Von SSPs in Ihren [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) -und [**Accept-SecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) -aufrufen.</span><span class="sxs-lookup"><span data-stu-id="411fb-158">From SSPs in their [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) and [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) calls.</span></span> <span data-ttu-id="411fb-159">SSPs sollten erkennen, dass das \_ Kennwort des Dienst Kontos \_ für diese Aufrufe verwendet wird. wenn der Aufruf nicht primäre Anmelde Informationen ist, sollte der SSP sicherstellen, dass der Aufrufer entweder über eine TCB-Berechtigung verfügt oder ein Netzwerkdienst ist.</span><span class="sxs-lookup"><span data-stu-id="411fb-159">SSPs should detect that the SERVICE\_ACCOUNT\_PASSWORD is being used for these calls, and if the call is for nonprimary credentials, then the SSP should ensure that the caller has either TCB privilege or is a network service.</span></span> <span data-ttu-id="411fb-160">Anschließend sollte der SSP die **getserviceaccountpassword** -Funktion mit dem Wert " **kredfetchdefault** " in der " [**Fed \_ Fetch**](cred-fetch.md) "-Enumeration aufrufen und den-Befehl fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="411fb-160">Then the SSP should call the **GetServiceAccountPassword** function with the **CredFetchDefault** value in the [**CRED\_FETCH**](cred-fetch.md) enumeration and proceed with the call.</span></span> <span data-ttu-id="411fb-161">Wenn die **InitializeSecurityContext** -und die **Accept-SecurityContext** -Aufrufe fehlschlagen, sollte der SSP den aus dem vorherigen Aufruf von **getserviceaccountpassword** abgerufenen *filetimeablauf* verwenden und ihn als Eingabe für den Aufruf von **getserviceaccountpassword** mithilfe des **credfetchforced** -Werts in der **cred- \_ Fetch-** Enumeration verwenden.</span><span class="sxs-lookup"><span data-stu-id="411fb-161">If the **InitializeSecurityContext** and **AcceptSecurityContext** calls fail, then the SSP should use the *FileTimeExpiry* retrieved from the previous call to **GetServiceAccountPassword** and use it as input to calling **GetServiceAccountPassword** again using the **CredFetchForced** value in the **CRED\_FETCH** enumeration.</span></span> <span data-ttu-id="411fb-162">Wenn ein neues GMSA-Anmelde Informationssystem verfügbar ist, wird der zweite-Befehl mit neuen Anmelde Informationen erfolgreich ausgeführt, und der SSP sollte dann mit den neuen Anmelde Informationen erneut versuchen.</span><span class="sxs-lookup"><span data-stu-id="411fb-162">If a new gMSA credential is available, the second call will succeed with new credentials, and the SSP should then retry with the new credentials.</span></span>

## <a name="requirements"></a><span data-ttu-id="411fb-163">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="411fb-163">Requirements</span></span>



| <span data-ttu-id="411fb-164">Anforderung</span><span class="sxs-lookup"><span data-stu-id="411fb-164">Requirement</span></span> | <span data-ttu-id="411fb-165">Wert</span><span class="sxs-lookup"><span data-stu-id="411fb-165">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="411fb-166">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="411fb-166">Minimum supported client</span></span><br/> | <span data-ttu-id="411fb-167">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="411fb-167">Windows 8 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="411fb-168">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="411fb-168">Minimum supported server</span></span><br/> | <span data-ttu-id="411fb-169">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="411fb-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="411fb-170">Header</span><span class="sxs-lookup"><span data-stu-id="411fb-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="411fb-171"><dt>Secpkg. h</dt></span><span class="sxs-lookup"><span data-stu-id="411fb-171"><dt>Secpkg.h</dt></span></span> </dl> |



 

