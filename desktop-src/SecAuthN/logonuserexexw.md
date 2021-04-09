---
description: Die logonuserexexw-Funktion versucht, einen Benutzer auf dem lokalen Computer zu protokollieren.
ms.assetid: d90db4c6-a711-4519-8b91-5069cee07738
title: Logonuserexexw-Funktion (winbasep. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LogonUserExExW
api_type:
- DllExport
api_location:
- Advapi32.dll
ms.openlocfilehash: 35ec65e7899f45a5222ae12b08992e77ea67f306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050285"
---
# <a name="logonuserexexw-function"></a><span data-ttu-id="94494-103">Logonuserexexw-Funktion</span><span class="sxs-lookup"><span data-stu-id="94494-103">LogonUserExExW function</span></span>

<span data-ttu-id="94494-104">Die **logonuserexexw** -Funktion versucht, einen Benutzer auf dem lokalen Computer zu protokollieren.</span><span class="sxs-lookup"><span data-stu-id="94494-104">The **LogonUserExExW** function attempts to log a user on to the local computer.</span></span> <span data-ttu-id="94494-105">Der lokale Computer ist der Computer, von dem **logonuserexexw** aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="94494-105">The local computer is the computer from which **LogonUserExExW** was called.</span></span> <span data-ttu-id="94494-106">Sie können **logonuserexexw** nicht zum Anmelden an einem Remote Computer verwenden.</span><span class="sxs-lookup"><span data-stu-id="94494-106">You cannot use **LogonUserExExW** to log on to a remote computer.</span></span> <span data-ttu-id="94494-107">Geben Sie den Benutzer mithilfe eines Benutzernamens und einer Domäne an, und [*Authentifizieren*](../secgloss/a-gly.md) Sie den Benutzer mit einem nur-Text-Kennwort.</span><span class="sxs-lookup"><span data-stu-id="94494-107">Specify the user by using a user name and domain and [*authenticate*](../secgloss/a-gly.md) the user by using a plaintext password.</span></span> <span data-ttu-id="94494-108">Wenn die Funktion erfolgreich ausgeführt wird, empfängt Sie ein Handle für ein Token, das den angemeldeten Benutzer darstellt.</span><span class="sxs-lookup"><span data-stu-id="94494-108">If the function succeeds, it receives a handle to a token that represents the logged-on user.</span></span> <span data-ttu-id="94494-109">Anschließend können Sie dieses Tokenhandle verwenden, um die Identität des angegebenen Benutzers anzunehmen oder in den meisten Fällen einen [*Prozess*](../secgloss/p-gly.md) zu erstellen, der im Kontext des angegebenen Benutzers ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="94494-109">You can then use this token handle to impersonate the specified user or, in most cases, to create a [*process*](../secgloss/p-gly.md) that runs in the context of the specified user.</span></span>

<span data-ttu-id="94494-110">Diese Funktion ähnelt der [**logonuserex**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa) -Funktion, mit der Ausnahme, dass Sie den zusätzlichen Parameter " *ptokengroups*" annimmt, bei dem es sich um einen Satz von mindestens einem Sicherheits-IDs (SIDs) handelt, die dem Token hinzugefügt werden, das dem Aufrufer zurückgegeben wird, wenn die Anmeldung erfolgreich ist. [](../secgloss/s-gly.md)</span><span class="sxs-lookup"><span data-stu-id="94494-110">This function is similar to the [**LogonUserEx**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa) function, except that it takes the additional parameter, *pTokenGroups*, which is a set of one or more [*security identifiers*](../secgloss/s-gly.md) (SIDs) that are added to the token returned to the caller when the logon is successful.</span></span>

<span data-ttu-id="94494-111">Diese Funktion ist nicht in einem öffentlichen Header deklariert und besitzt keine zugehörige Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="94494-111">This function is not declared in a public header and has no associated import library.</span></span> <span data-ttu-id="94494-112">Sie müssen die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Advapi32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="94494-112">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Advapi32.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="94494-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="94494-113">Syntax</span></span>


```C++
BOOL WINAPI LogonUserExExW(
  _In_      LPTSTR        lpszUsername,
  _In_opt_  LPTSTR        lpszDomain,
  _In_opt_  LPTSTR        lpszPassword,
  _In_      DWORD         dwLogonType,
  _In_      DWORD         dwLogonProvider,
  _In_opt_  PTOKEN_GROUPS pTokenGroups,
  _Out_opt_ PHANDLE       phToken,
  _Out_opt_ PSID          *ppLogonSid,
  _Out_opt_ PVOID         *ppProfileBuffer,
  _Out_opt_ LPDWORD       pdwProfileLength,
  _Out_opt_ PQUOTA_LIMITS pQuotaLimits
);
```



## <a name="parameters"></a><span data-ttu-id="94494-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="94494-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94494-115">*lpszusername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="94494-115">*lpszUsername* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94494-116">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Benutzers angibt.</span><span class="sxs-lookup"><span data-stu-id="94494-116">A pointer to a null-terminated string that specifies the name of the user.</span></span> <span data-ttu-id="94494-117">Dies ist der Name des Benutzerkontos, bei dem Sie sich anmelden möchten.</span><span class="sxs-lookup"><span data-stu-id="94494-117">This is the name of the user account to log on to.</span></span> <span data-ttu-id="94494-118">Wenn Sie das UPN-Format ( [*User Principal Name, Benutzer Prinzipal Name*](../secgloss/u-gly.md) ) verwenden, muss der *lpszdomain* -Parameter **null** sein.</span><span class="sxs-lookup"><span data-stu-id="94494-118">If you use the [*user principal name*](../secgloss/u-gly.md) (UPN) format, the *lpszDomain* parameter must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="94494-119">*lpszdomain* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="94494-119">*lpszDomain* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="94494-120">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen der Domäne oder des Servers angibt, deren Konto Datenbank das *lpszusername* -Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="94494-120">A pointer to a null-terminated string that specifies the name of the domain or server whose account database contains the *lpszUsername* account.</span></span> <span data-ttu-id="94494-121">Wenn dieser Parameter **null** ist, muss der Benutzername im UPN-Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="94494-121">If this parameter is **NULL**, the user name must be specified in UPN format.</span></span> <span data-ttu-id="94494-122">Wenn dieser Parameter "." ist, überprüft die Funktion das Konto nur mithilfe der lokalen Konto Datenbank.</span><span class="sxs-lookup"><span data-stu-id="94494-122">If this parameter is ".", the function validates the account by using only the local account database.</span></span>

</dd> <dt>

<span data-ttu-id="94494-123">*lpszpassword* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="94494-123">*lpszPassword* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="94494-124">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die das nur-Text-Kennwort für das durch *lpszusername* angegebene Benutzerkonto angibt.</span><span class="sxs-lookup"><span data-stu-id="94494-124">A pointer to a null-terminated string that specifies the plaintext password for the user account specified by *lpszUsername*.</span></span> <span data-ttu-id="94494-125">Wenn Sie die Verwendung des Kennworts abgeschlossen haben, löschen Sie das Kennwort aus dem Arbeitsspeicher, indem Sie die [**securezeromemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="94494-125">When you have finished using the password, clear the password from memory by calling the [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function.</span></span> <span data-ttu-id="94494-126">Weitere Informationen zum Schützen von Kenn Wörtern finden Sie unter [Handling Kennwörter](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="94494-126">For more information about protecting passwords, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="94494-127">*dwlogontype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="94494-127">*dwLogonType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94494-128">Der Typ des auszuführenden Anmeldevorgangs.</span><span class="sxs-lookup"><span data-stu-id="94494-128">The type of logon operation to perform.</span></span> <span data-ttu-id="94494-129">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="94494-129">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="94494-130">Wert</span><span class="sxs-lookup"><span data-stu-id="94494-130">Value</span></span>                                                                                                                                                                                                                                                                        | <span data-ttu-id="94494-131">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="94494-131">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_LOGON_INTERACTIVE"></span><span id="logon32_logon_interactive"></span><dl> <span data-ttu-id="94494-132"><dt>**LOGON32 \_ \_Interaktiv anmelden**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="94494-132"><dt>**LOGON32\_LOGON\_INTERACTIVE**</dt> <dt>2</dt></span></span> </dl>                    | <span data-ttu-id="94494-133">Dieser Anmeldetyp richtet sich an Benutzer, die den Computer interaktiv verwenden, z. b. ein Benutzer, der von einem [*Terminal*](../secgloss/t-gly.md) Server, einer Remoteshell oder einem ähnlichen Prozess angemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="94494-133">This logon type is intended for users who will be interactively using the computer, such as a user being logged on by a [*terminal*](../secgloss/t-gly.md) server, remote shell, or similar process.</span></span> <span data-ttu-id="94494-134">Dieser Anmeldetyp hat zusätzliche Kosten für das Zwischenspeichern von Anmelde Informationen für getrennte Vorgänge. Daher ist es für einige Client/Server-Anwendungen, wie z. b. einen Mailserver, ungeeignet.</span><span class="sxs-lookup"><span data-stu-id="94494-134">This logon type has the additional expense of caching logon information for disconnected operations; therefore, it is inappropriate for some client/server applications, such as a mail server.</span></span><br/>                                  |
| <span id="LOGON32_LOGON_NETWORK"></span><span id="logon32_logon_network"></span><dl> <span data-ttu-id="94494-135"><dt>**LOGON32 \_ Anmelde \_ Netzwerk**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="94494-135"><dt>**LOGON32\_LOGON\_NETWORK**</dt> <dt>3</dt></span></span> </dl>                                | <span data-ttu-id="94494-136">Dieser Anmeldetyp eignet sich für Hochleistungsserver, um nur-Text-Kenn Wörter zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="94494-136">This logon type is intended for high performance servers to authenticate plaintext passwords.</span></span> <span data-ttu-id="94494-137">Die Anmelde Informationen für diesen Anmeldetyp werden von der **logonuserexexw** -Funktion nicht zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="94494-137">The **LogonUserExExW** function does not cache credentials for this logon type.</span></span><br/>                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_BATCH"></span><span id="logon32_logon_batch"></span><dl> <span data-ttu-id="94494-138"><dt>**LOGON32 \_ Anmelde \_ Batch**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="94494-138"><dt>**LOGON32\_LOGON\_BATCH**</dt> <dt>4</dt></span></span> </dl>                                      | <span data-ttu-id="94494-139">Dieser Anmeldetyp ist für Batch Server gedacht, bei denen Prozesse möglicherweise im Auftrag eines Benutzers ohne direkten Eingriff ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="94494-139">This logon type is intended for batch servers, where processes may be executing on behalf of a user without their direct intervention.</span></span> <span data-ttu-id="94494-140">Dieser Typ ist auch für Server mit höherer Leistung vorgesehen, die viele nur-Text-Authentifizierungs Versuche gleichzeitig verarbeiten, z. b. e-Mail-oder Webserver.</span><span class="sxs-lookup"><span data-stu-id="94494-140">This type is also for higher performance servers that process many plaintext authentication attempts at a time, such as mail or web servers.</span></span> <span data-ttu-id="94494-141">Die Anmelde Informationen für diesen Anmeldetyp werden von der **logonuserexexw** -Funktion nicht zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="94494-141">The **LogonUserExExW** function does not cache credentials for this logon type.</span></span><br/>                                                                                                           |
| <span id="LOGON32_LOGON_SERVICE"></span><span id="logon32_logon_service"></span><dl> <span data-ttu-id="94494-142"><dt>**LOGON32 \_ Anmelde \_ Dienst**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="94494-142"><dt>**LOGON32\_LOGON\_SERVICE**</dt> <dt>5</dt></span></span> </dl>                                | <span data-ttu-id="94494-143">Gibt die Anmeldung eines Dienst Typs an.</span><span class="sxs-lookup"><span data-stu-id="94494-143">Indicates a service-type logon.</span></span> <span data-ttu-id="94494-144">Für das angegebene Konto muss die Dienst Berechtigung aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="94494-144">The account provided must have the service privilege enabled.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_UNLOCK"></span><span id="logon32_logon_unlock"></span><dl> <span data-ttu-id="94494-145"><dt>**LOGON32 \_ Anmelde \_ Sperre**</dt> <dt>7</dt> aufheben</span><span class="sxs-lookup"><span data-stu-id="94494-145"><dt>**LOGON32\_LOGON\_UNLOCK**</dt> <dt>7</dt></span></span> </dl>                                   | <span data-ttu-id="94494-146">Bei diesem Anmeldetyp handelt es sich um [*Gina*](../secgloss/g-gly.md) -DLLs, die sich bei Benutzern anmelden, die den Computer interaktiv verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="94494-146">This logon type is for [*GINA*](../secgloss/g-gly.md) DLLs that log on users who will be interactively using the computer.</span></span> <span data-ttu-id="94494-147">Dieser Anmeldetyp kann einen eindeutigen Überwachungsdaten Satz generieren, der anzeigt, wann die Arbeitsstation entsperrt wurde.</span><span class="sxs-lookup"><span data-stu-id="94494-147">This logon type can generate a unique audit record that shows when the workstation was unlocked.</span></span><br/>                                                                                                                                                                                                                   |
| <span id="LOGON32_LOGON_NETWORK_CLEARTEXT"></span><span id="logon32_logon_network_cleartext"></span><dl> <span data-ttu-id="94494-148"><dt>**LOGON32 \_ Anmelde \_ Netzwerk \_ Klartext**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="94494-148"><dt>**LOGON32\_LOGON\_NETWORK\_CLEARTEXT**</dt> <dt>8</dt></span></span> </dl> | <span data-ttu-id="94494-149">Dieser Anmeldetyp behält den Namen und das Kennwort im [*Authentifizierungs Paket*](../secgloss/a-gly.md)bei, wodurch der Serververbindungen zu anderen Netzwerkservern herstellen kann, während die Identität des Clients angenommen wird.</span><span class="sxs-lookup"><span data-stu-id="94494-149">This logon type preserves the name and password in the [*authentication package*](../secgloss/a-gly.md), which allows the server to make connections to other network servers while impersonating the client.</span></span> <span data-ttu-id="94494-150">Ein Server kann Klartext-Anmelde Informationen von einem Client akzeptieren, **logonuserexexw** aufrufen, sicherstellen, dass der Benutzer über das Netzwerk auf das System zugreifen kann und weiterhin mit anderen Servern kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="94494-150">A server can accept plaintext credentials from a client, call **LogonUserExExW**, verify that the user can access the system across the network, and still communicate with other servers.</span></span> <br/> |
| <span id="LOGON32_LOGON_NEW_CREDENTIALS"></span><span id="logon32_logon_new_credentials"></span><dl> <span data-ttu-id="94494-151"><dt>**LOGON32 \_ \_Neue \_**</dt> Anmelde Informationen anmelden <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="94494-151"><dt>**LOGON32\_LOGON\_NEW\_CREDENTIALS**</dt> <dt>9</dt></span></span> </dl>       | <span data-ttu-id="94494-152">Dieser Anmeldetyp ermöglicht dem Aufrufer das Klonen seines aktuellen Tokens und das Angeben neuer Anmelde Informationen für ausgehende Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="94494-152">This logon type allows the caller to clone its current token and specify new credentials for outbound connections.</span></span> <span data-ttu-id="94494-153">Die neue Anmelde Sitzung hat denselben lokalen Bezeichner, verwendet jedoch andere Anmelde Informationen für andere Netzwerkverbindungen.</span><span class="sxs-lookup"><span data-stu-id="94494-153">The new logon session has the same local identifier but uses different credentials for other network connections.</span></span><br/> <span data-ttu-id="94494-154">Dieser Anmeldetyp wird nur vom **LOGON32 \_ Provider \_ WINNT50** -Anmelde Anbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="94494-154">This logon type is supported only by the **LOGON32\_PROVIDER\_WINNT50** logon provider.</span></span><br/>                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="94494-155">*dwlogonprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="94494-155">*dwLogonProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94494-156">Der Anmelde Anbieter.</span><span class="sxs-lookup"><span data-stu-id="94494-156">The logon provider.</span></span> <span data-ttu-id="94494-157">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="94494-157">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="94494-158">Wert</span><span class="sxs-lookup"><span data-stu-id="94494-158">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="94494-159">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="94494-159">Meaning</span></span>                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_PROVIDER_DEFAULT"></span><span id="logon32_provider_default"></span><dl> <span data-ttu-id="94494-160"><dt>**LOGON32 \_ Provider- \_ Standard**</dt></span><span class="sxs-lookup"><span data-stu-id="94494-160"><dt>**LOGON32\_PROVIDER\_DEFAULT**</dt></span></span> </dl> | <span data-ttu-id="94494-161">Verwenden Sie den Standard Anmelde Anbieter für das System.</span><span class="sxs-lookup"><span data-stu-id="94494-161">Use the standard logon provider for the system.</span></span> <span data-ttu-id="94494-162">Der Standard [*Sicherheitsanbieter*](../secgloss/s-gly.md) ist NTLM.</span><span class="sxs-lookup"><span data-stu-id="94494-162">The default [*security provider*](../secgloss/s-gly.md) is NTLM.</span></span><br/> |
| <span id="LOGON32_PROVIDER_WINNT50"></span><span id="logon32_provider_winnt50"></span><dl> <span data-ttu-id="94494-163"><dt>**LOGON32- \_ Anbieter \_ WINNT50**</dt></span><span class="sxs-lookup"><span data-stu-id="94494-163"><dt>**LOGON32\_PROVIDER\_WINNT50**</dt></span></span> </dl> | <span data-ttu-id="94494-164">Verwenden Sie den Logon-Anmelde Anbieter.</span><span class="sxs-lookup"><span data-stu-id="94494-164">Use the negotiate logon provider.</span></span> <br/>                                                                                                                                                         |
| <span id="LOGON32_PROVIDER_WINNT40"></span><span id="logon32_provider_winnt40"></span><dl> <span data-ttu-id="94494-165"><dt>**LOGON32- \_ Anbieter \_ WINNT40**</dt></span><span class="sxs-lookup"><span data-stu-id="94494-165"><dt>**LOGON32\_PROVIDER\_WINNT40**</dt></span></span> </dl> | <span data-ttu-id="94494-166">Verwenden Sie den NTLM-Anmelde Anbieter.</span><span class="sxs-lookup"><span data-stu-id="94494-166">Use the NTLM logon provider.</span></span><br/>                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="94494-167">*ptokengroups* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="94494-167">*pTokenGroups* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="94494-168">Ein Zeiger auf eine [**\_ tokengruppenstruktur**](/windows/win32/api/winnt/ns-winnt-token_groups) , die eine Liste von Gruppen-SIDs angibt, die dem Token hinzugefügt werden, das diese Funktion bei erfolgreicher Anmeldung empfängt.</span><span class="sxs-lookup"><span data-stu-id="94494-168">A pointer to a [**TOKEN\_GROUPS**](/windows/win32/api/winnt/ns-winnt-token_groups) structure that specifies a list of group SIDs that are added to the token that this function receives upon successful logon.</span></span> <span data-ttu-id="94494-169">Alle dem Token hinzugefügten SIDs wirken sich auch auf die Gruppen Erweiterung aus.</span><span class="sxs-lookup"><span data-stu-id="94494-169">Any SIDs added to the token also effect group expansion.</span></span> <span data-ttu-id="94494-170">Wenn die hinzugefügten SIDs beispielsweise Mitglieder von lokalen Gruppen sind, werden diese Gruppen auch dem empfangenen Zugriffs Token hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="94494-170">For example, if the added SIDs are members of local groups, those groups are also added to the received access token.</span></span>

<span data-ttu-id="94494-171">Wenn dieser Parameter nicht **null** ist, muss dem Aufrufer dieser Funktion die **Berechtigung "SE \_ TCB- \_ Berechtigung** erteilt und aktiviert" zugewiesen sein.</span><span class="sxs-lookup"><span data-stu-id="94494-171">If this parameter is not **NULL**, the caller of this function must have the **SE\_TCB\_PRIVILEGE** privilege granted and enabled.</span></span>

</dd> <dt>

<span data-ttu-id="94494-172">*phtoken* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="94494-172">*phToken* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="94494-173">Ein Zeiger auf eine Handle-Variable, die ein Handle für ein Token empfängt, das den angegebenen Benutzer darstellt.</span><span class="sxs-lookup"><span data-stu-id="94494-173">A pointer to a handle variable that receives a handle to a token that represents the specified user.</span></span>

<span data-ttu-id="94494-174">Sie können das zurückgegebene Handle in Aufrufen der Funktion "annehmen der Identität des Identitäts [**Benutzers**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) " verwenden.</span><span class="sxs-lookup"><span data-stu-id="94494-174">You can use the returned handle in calls to the [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) function.</span></span>

<span data-ttu-id="94494-175">In den meisten Fällen ist das zurückgegebene Handle ein [*primäres Token*](../secgloss/p-gly.md) , das Sie in Aufrufen der Funktion " [**deateprocessasuser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) " verwenden können.</span><span class="sxs-lookup"><span data-stu-id="94494-175">In most cases, the returned handle is a [*primary token*](../secgloss/p-gly.md) that you can use in calls to the [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function.</span></span> <span data-ttu-id="94494-176">Wenn Sie jedoch das LOGON32 \_ Logon Network- \_ Flag angeben, gibt **logonuserexexw** ein Identitätswechsel [*Token*](../secgloss/i-gly.md) zurück, das Sie nicht in " **kreateprocessasuser** " verwenden können, es sei denn, Sie müssen [**duplicalletokenex**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) aufrufen, um das Identitätswechsel Token in ein primäres Token zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="94494-176">However, if you specify the LOGON32\_LOGON\_NETWORK flag, **LogonUserExExW** returns an [*impersonation token*](../secgloss/i-gly.md) that you cannot use in **CreateProcessAsUser** unless you call [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) to convert the impersonation token to a primary token.</span></span>

<span data-ttu-id="94494-177">Wenn Sie dieses Handle nicht mehr benötigen, schließen Sie es, indem Sie die [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="94494-177">When you no longer need this handle, close it by calling the [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) function.</span></span>

</dd> <dt>

<span data-ttu-id="94494-178">*pplogonsid* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="94494-178">*ppLogonSid* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="94494-179">Ein Zeiger auf einen Zeiger auf eine SID, die die SID des angemeldeten Benutzers empfängt.</span><span class="sxs-lookup"><span data-stu-id="94494-179">A pointer to a pointer to a SID that receives the SID of the user logged on.</span></span>

<span data-ttu-id="94494-180">Wenn Sie die SID nicht mehr verwenden, können Sie Sie durch Aufrufen der [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) -Funktion freigeben.</span><span class="sxs-lookup"><span data-stu-id="94494-180">When you have finished using the SID, free it by calling the [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) function.</span></span>

</dd> <dt>

<span data-ttu-id="94494-181">*ppprofilebuffer* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="94494-181">*ppProfileBuffer* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="94494-182">Ein Zeiger auf einen Zeiger, der die Adresse eines Puffers empfängt, der das Profil des angemeldeten Benutzers enthält.</span><span class="sxs-lookup"><span data-stu-id="94494-182">A pointer to a pointer that receives the address of a buffer that contains the logged on user's profile.</span></span>

</dd> <dt>

<span data-ttu-id="94494-183">*pdwprofilelength* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="94494-183">*pdwProfileLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="94494-184">Ein Zeiger auf ein **DWORD** , das die Länge des Profil Puffers empfängt.</span><span class="sxs-lookup"><span data-stu-id="94494-184">A pointer to a **DWORD** that receives the length of the profile buffer.</span></span>

</dd> <dt>

<span data-ttu-id="94494-185">*pquotalimits* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="94494-185">*pQuotaLimits* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="94494-186">Ein Zeiger auf eine [**Kontingent \_ Limits**](/windows/desktop/api/Winnt/ns-winnt-quota_limits) -Struktur, die Informationen über die Kontingente für den angemeldeten Benutzer empfängt.</span><span class="sxs-lookup"><span data-stu-id="94494-186">A pointer to a [**QUOTA\_LIMITS**](/windows/desktop/api/Winnt/ns-winnt-quota_limits) structure that receives information about the quotas for the logged on user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94494-187">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="94494-187">Return value</span></span>

<span data-ttu-id="94494-188">Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion einen Wert ungleich NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="94494-188">If the function succeeds, the function returns nonzero.</span></span>

<span data-ttu-id="94494-189">Wenn die Funktion fehlschlägt, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="94494-189">If the function fails, it returns zero.</span></span> <span data-ttu-id="94494-190">Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.</span><span class="sxs-lookup"><span data-stu-id="94494-190">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="94494-191">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94494-191">Remarks</span></span>

<span data-ttu-id="94494-192">Der Anmeldetyp " **LOGON32 \_ Logon \_ Network** " ist am schnellsten, es gelten jedoch die folgenden Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="94494-192">The **LOGON32\_LOGON\_NETWORK** logon type is fastest, but it has the following limitations:</span></span>

-   <span data-ttu-id="94494-193">Die-Funktion gibt ein Identitätswechsel [*Token*](../secgloss/i-gly.md)zurück, nicht ein primäres Token.</span><span class="sxs-lookup"><span data-stu-id="94494-193">The function returns an [*impersonation token*](../secgloss/i-gly.md), not a primary token.</span></span> <span data-ttu-id="94494-194">Sie können dieses Token nicht direkt in der [**Funktion "**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) " von "" in der Funktion "|" verwenden.</span><span class="sxs-lookup"><span data-stu-id="94494-194">You cannot use this token directly in the [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function.</span></span> <span data-ttu-id="94494-195">Allerdings können Sie die [**duplicalletokenex**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) -Funktion aufrufen, um das **Token in ein** primäres Token zu konvertieren</span><span class="sxs-lookup"><span data-stu-id="94494-195">However, you can call the [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) function to convert the token to a primary token, and then use it in **CreateProcessAsUser**.</span></span>
-   <span data-ttu-id="94494-196">Wenn Sie das Token in ein primäres Token konvertieren und es in [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) verwenden, um einen Prozess zu starten, kann der neue Prozess nicht auf andere Netzwerkressourcen (z. b. Remote Server oder Drucker) über den Redirector zugreifen.</span><span class="sxs-lookup"><span data-stu-id="94494-196">If you convert the token to a primary token and use it in [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) to start a process, the new process cannot access other network resources, such as remote servers or printers, through the redirector.</span></span> <span data-ttu-id="94494-197">Eine Ausnahme besteht darin, dass der neue Prozess darauf zugreifen kann, wenn der Zugriff auf die Netzwerkressource nicht gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="94494-197">An exception is that if the network resource is not access controlled, then the new process will be able to access it.</span></span>

<span data-ttu-id="94494-198">Das von *lpszusername* angegebene Konto muss über die erforderlichen Konto Rechte verfügen.</span><span class="sxs-lookup"><span data-stu-id="94494-198">The account specified by *lpszUsername* must have the necessary account rights.</span></span> <span data-ttu-id="94494-199">Wenn Sie z. b. einen Benutzer mit dem " **LOGON32 \_ Logon \_ Interactive** "-Flag anmelden möchten, muss der Benutzer (oder eine Gruppe, zu der der Benutzer gehört) über das Konto "Konto für **\_ interaktive \_ Anmelde \_ Namen** Konto" verfügen.</span><span class="sxs-lookup"><span data-stu-id="94494-199">For example, to log on a user with the **LOGON32\_LOGON\_INTERACTIVE** flag, the user (or a group to which the user belongs) must have the **SE\_INTERACTIVE\_LOGON\_NAME** account right.</span></span> <span data-ttu-id="94494-200">Eine Liste der Konto Rechte, die sich auf die verschiedenen Anmeldevorgänge auswirken, finden Sie unter [Konto Objekt-Zugriffsrechte](../secmgmt/account-object-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="94494-200">For a list of the account rights that affect the various logon operations, see [Account Object Access Rights](../secmgmt/account-object-access-rights.md).</span></span>

<span data-ttu-id="94494-201">Ein Benutzer gilt als angemeldet, wenn mindestens ein Token vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="94494-201">A user is considered logged on if at least one token exists.</span></span> <span data-ttu-id="94494-202">Wenn Sie " [**kreateprocessasuser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) " aufrufen und dann das Token schließen, ist der Benutzer weiterhin angemeldet, bis der Prozess (und alle untergeordneten Prozesse) beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="94494-202">If you call [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) and then close the token, the user is still logged on until the process (and all child processes) have ended.</span></span>

<span data-ttu-id="94494-203">Wenn der optionale Parameter " *ptokengroups* " angegeben wird, wird die lokale sid oder die Anmelde-SID von LSA nicht automatisch hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="94494-203">If the optional *pTokenGroups* parameter is supplied, LSA will not add either the local SID or the logon SID automatically.</span></span>

## <a name="requirements"></a><span data-ttu-id="94494-204">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94494-204">Requirements</span></span>



| <span data-ttu-id="94494-205">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94494-205">Requirement</span></span> | <span data-ttu-id="94494-206">Wert</span><span class="sxs-lookup"><span data-stu-id="94494-206">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94494-207">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94494-207">Minimum supported client</span></span><br/> | <span data-ttu-id="94494-208">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94494-208">Windows Vista \[desktop apps only\]</span></span><br/>                                                                        |
| <span data-ttu-id="94494-209">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94494-209">Minimum supported server</span></span><br/> | <span data-ttu-id="94494-210">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94494-210">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="94494-211">Version</span><span class="sxs-lookup"><span data-stu-id="94494-211">Version</span></span><br/>                  | <span data-ttu-id="94494-212">Logonuserexexw ist auch unter Windows Server 2003 oder Windows xpmit der allgemeinen Verteilungs Version verfügbar.</span><span class="sxs-lookup"><span data-stu-id="94494-212">LogonUserExExW is also available onWindows Server 2003 or Windows XPwith the General Distribution Release.</span></span><br/> |
| <span data-ttu-id="94494-213">Header</span><span class="sxs-lookup"><span data-stu-id="94494-213">Header</span></span><br/>                   | <dl> <span data-ttu-id="94494-214"><dt>Winbasep. h</dt></span><span class="sxs-lookup"><span data-stu-id="94494-214"><dt>Winbasep.h</dt></span></span> </dl>                                 |
| <span data-ttu-id="94494-215">DLL</span><span class="sxs-lookup"><span data-stu-id="94494-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94494-216"><dt>Advapi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94494-216"><dt>Advapi32.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="94494-217">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94494-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94494-218">Client/Server-Access Control</span><span class="sxs-lookup"><span data-stu-id="94494-218">Client/Server Access Control</span></span>](../secauthz/client-server-access-control.md)
</dt> <dt>

[<span data-ttu-id="94494-219">Client/Server-Access Control Funktionen</span><span class="sxs-lookup"><span data-stu-id="94494-219">Client/Server Access Control Functions</span></span>](../secauthz/authorization-functions.md)
</dt> <dt>

[<span data-ttu-id="94494-220">**CloseHandle**</span><span class="sxs-lookup"><span data-stu-id="94494-220">**CloseHandle**</span></span>](/windows/win32/api/handleapi/nf-handleapi-closehandle)
</dt> <dt>

[<span data-ttu-id="94494-221">**CreateProcessAsUser**</span><span class="sxs-lookup"><span data-stu-id="94494-221">**CreateProcessAsUser**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)
</dt> <dt>

[<span data-ttu-id="94494-222">**Duplialisietokenex**</span><span class="sxs-lookup"><span data-stu-id="94494-222">**DuplicateTokenEx**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex)
</dt> <dt>

[<span data-ttu-id="94494-223">**ImpersonateLoggedOnUser**</span><span class="sxs-lookup"><span data-stu-id="94494-223">**ImpersonateLoggedOnUser**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser)
</dt> <dt>

[<span data-ttu-id="94494-224">**Logonuserex**</span><span class="sxs-lookup"><span data-stu-id="94494-224">**LogonUserEx**</span></span>](/windows/desktop/api/Winbase/nf-winbase-logonuserexa)
</dt> <dt>

[<span data-ttu-id="94494-225">**Kontingent \_ Limits**</span><span class="sxs-lookup"><span data-stu-id="94494-225">**QUOTA\_LIMITS**</span></span>](/windows/desktop/api/Winnt/ns-winnt-quota_limits)
</dt> </dl>

 

 
