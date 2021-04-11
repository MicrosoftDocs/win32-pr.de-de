---
description: Zum Abrufen von Anmelde Informationen, die nicht mit der aktuellen Anmelde Sitzung verknüpft sind, geben Sie eine sec- \_ Winnt-Authentifizierungs \_ \_ Identitäts Struktur mit Informationen für den alternativen Sicherheits Prinzipal ein.
ms.assetid: f590ddb5-39a1-4d0c-a787-da938a63c206
title: Abrufen alternativer Digest-Anmelde Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ed7daa2a3179822929e8c2df8077ee55afaadb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217317"
---
# <a name="obtaining-alternate-digest-credentials"></a><span data-ttu-id="6924d-103">Abrufen alternativer Digest-Anmelde Informationen</span><span class="sxs-lookup"><span data-stu-id="6924d-103">Obtaining Alternate Digest Credentials</span></span>

<span data-ttu-id="6924d-104">Zum Abrufen von [*Anmelde*](../secgloss/c-gly.md) Informationen, die nicht mit der aktuellen Anmelde [*Sitzung*](../secgloss/s-gly.md)verknüpft sind, geben Sie eine sec- [**\_ Winnt-Authentifizierungs \_ \_ Identitäts**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) Struktur mit Informationen für den alternativen [*Sicherheits Prinzipal*](../secgloss/s-gly.md)ein.</span><span class="sxs-lookup"><span data-stu-id="6924d-104">To obtain [*credentials*](../secgloss/c-gly.md) other than those associated with the current logon [*session*](../secgloss/s-gly.md), populate a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure with information for the alternate [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="6924d-105">Übergeben Sie die Struktur mithilfe des *pauthdata* -Parameters an die Funktion [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) .</span><span class="sxs-lookup"><span data-stu-id="6924d-105">Pass the structure to the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function using the *pAuthData* parameter.</span></span>

<span data-ttu-id="6924d-106">In der folgenden Tabelle werden die Mitglieder der [**Identitäts Struktur "sec \_ Winnt \_ auth \_**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) " beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6924d-106">The following table describes the members of the [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure.</span></span>



| <span data-ttu-id="6924d-107">Member</span><span class="sxs-lookup"><span data-stu-id="6924d-107">Member</span></span>             | <span data-ttu-id="6924d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6924d-108">Description</span></span>                                                                                                                          |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6924d-109">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="6924d-109">**User**</span></span>           | <span data-ttu-id="6924d-110">Eine auf NULL endende Zeichenfolge mit dem Namen des Sicherheits Prinzipals, dessen Anmelde Informationen zum Einrichten eines Sicherheits Kontexts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6924d-110">Null-terminated string containing the name of the security principal whose credentials will be used to establish a security context.</span></span> |
| <span data-ttu-id="6924d-111">**User length**</span><span class="sxs-lookup"><span data-stu-id="6924d-111">**UserLength**</span></span>     | <span data-ttu-id="6924d-112">Die Länge des **Benutzer** Members in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="6924d-112">The length of the **User** member, in characters.</span></span> <span data-ttu-id="6924d-113">Lassen Sie den abschließenden NULL-Wert aus.</span><span class="sxs-lookup"><span data-stu-id="6924d-113">Omit the terminating null.</span></span>                                                         |
| <span data-ttu-id="6924d-114">**Domäne**</span><span class="sxs-lookup"><span data-stu-id="6924d-114">**Domain**</span></span>         | <span data-ttu-id="6924d-115">NULL-terminierte Zeichenfolge, die die Domäne angibt, die das Konto des Sicherheits Prinzipals enthält.</span><span class="sxs-lookup"><span data-stu-id="6924d-115">Null-terminated string that identifies the domain containing the account of the security principal.</span></span>                                  |
| <span data-ttu-id="6924d-116">**Domänen Länge**</span><span class="sxs-lookup"><span data-stu-id="6924d-116">**DomainLength**</span></span>   | <span data-ttu-id="6924d-117">Die Länge des **Domänen** Mitglieds in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="6924d-117">The length of the **Domain** member, in characters.</span></span> <span data-ttu-id="6924d-118">Lassen Sie den abschließenden NULL-Wert aus.</span><span class="sxs-lookup"><span data-stu-id="6924d-118">Omit the terminating null.</span></span>                                                       |
| <span data-ttu-id="6924d-119">**Kennwort**</span><span class="sxs-lookup"><span data-stu-id="6924d-119">**Password**</span></span>       | <span data-ttu-id="6924d-120">NULL-terminierte Zeichenfolge mit dem Kennwort des Sicherheits Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="6924d-120">Null-terminated string containing the password of the security principal.</span></span>                                                            |
| <span data-ttu-id="6924d-121">**Passwordlength**</span><span class="sxs-lookup"><span data-stu-id="6924d-121">**PasswordLength**</span></span> | <span data-ttu-id="6924d-122">Die Länge des Kenn **Wort** Members in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="6924d-122">The length of the **Password** member, in characters.</span></span> <span data-ttu-id="6924d-123">Lassen Sie den abschließenden NULL-Wert aus.</span><span class="sxs-lookup"><span data-stu-id="6924d-123">Omit the terminating null.</span></span>                                                     |
| <span data-ttu-id="6924d-124">**Flags**</span><span class="sxs-lookup"><span data-stu-id="6924d-124">**Flags**</span></span>          | <span data-ttu-id="6924d-125">Gibt an, ob die Zeichen folgen Elemente im ANSI-oder [*Unicode*](../secgloss/u-gly.md) -Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="6924d-125">Indicates whether the string members are in ANSI or [*Unicode*](../secgloss/u-gly.md) format.</span></span>  |



 

<span data-ttu-id="6924d-126">In der folgenden Tabelle sind die gültigen Werte für den **Flags** -Member der-Struktur aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6924d-126">The following table lists the valid values for the **Flags** member of the structure.</span></span>



| <span data-ttu-id="6924d-127">Konstante</span><span class="sxs-lookup"><span data-stu-id="6924d-127">Constant</span></span>                            | <span data-ttu-id="6924d-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6924d-128">Description</span></span>                                                                                                      |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6924d-129">SEK \_ . WinNT-Authentifizierungs \_ \_ Identität \_ ANSI</span><span class="sxs-lookup"><span data-stu-id="6924d-129">SEC\_WINNT\_AUTH\_IDENTITY\_ANSI</span></span>    | <span data-ttu-id="6924d-130">Zeichen folgen in dieser Struktur weisen das ANSI-Format auf.</span><span class="sxs-lookup"><span data-stu-id="6924d-130">Strings in this structure are in ANSI format.</span></span>                                                                    |
| <span data-ttu-id="6924d-131">SEK \_ . WinNT-Authentifizierungs \_ \_ Identität ( \_ Unicode)</span><span class="sxs-lookup"><span data-stu-id="6924d-131">SEC\_WINNT\_AUTH\_IDENTITY\_UNICODE</span></span> | <span data-ttu-id="6924d-132">Zeichen folgen in dieser Struktur haben das [*Unicode*](../secgloss/u-gly.md) -Format.</span><span class="sxs-lookup"><span data-stu-id="6924d-132">Strings in this structure are in [*Unicode*](../secgloss/u-gly.md) format.</span></span> |



 

<span data-ttu-id="6924d-133">Die Struktur und Konstanten werden in der Header Datei "rpcdce. h" deklariert, die mit dem Platform Software Development Kit (SDK) verteilt wird.</span><span class="sxs-lookup"><span data-stu-id="6924d-133">The structure and constants are declared in the Rpcdce.h header file distributed with the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="6924d-134">Im folgenden Beispiel wird ein Client seitiger-Abruf zum Abrufen der Digest-Anmelde Informationen für ein bestimmtes Benutzerkonto veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="6924d-134">The following example demonstrates a client-side call to obtain Digest credentials for a specific user account.</span></span>


```C++
#include <windows.h>

#ifdef UNICODE
  ClientAuthID.Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;
#else
  ClientAuthID.Flags = SEC_WINNT_AUTH_IDENTITY_ANSI;
#endif

void main()
{
    SECURITY_STATUS SecStatus; 
    TimeStamp tsLifetime; 
    CredHandle hCred;
    SEC_WINNT_AUTH_IDENTITY ClientAuthID;
    LPTSTR UserName = TEXT("ASecurityPrinciple");
    LPTSTR DomainName = TEXT("AnAuthenticatingDomain");

    // Initialize the memory.
    ZeroMemory( &ClientAuthID, sizeof(ClientAuthID) );

    // Specify string format for the ClientAuthID structure.


    // Specify an alternate user, domain and password.
      ClientAuthID.User = (unsigned char *) UserName;
      ClientAuthID.UserLength = _tcslen(UserName);

      ClientAuthID.Domain = (unsigned char *) DomainName;
      ClientAuthID.DomainLength = _tcslen(DomainName);

    // Password is an application-defined LPTSTR variable
    // containing the user password.
      ClientAuthID.Password = Password;
      ClientAuthID.PasswordLength = _tcslen(Password);

    // Get the client side credential handle.
    SecStatus = AcquireCredentialsHandle (
      NULL,                  // Default principal.
      WDIGEST_SP_NAME,       // The Digest SSP. 
      SECPKG_CRED_OUTBOUND,  // Client will use the credentials.
      NULL,                  // Do not specify LOGON id.
      &ClientAuthID,         // User information.
      NULL,                  // Not used with Digest SSP.
      NULL,                  // Not used with Digest SSP.
      &hCred,                // Receives the credential handle.
      &tsLifetime            // Receives the credential time limit.
    );
}
```



<span data-ttu-id="6924d-135">Die **\_ tcslen** -Funktion gibt die Zeichen folgen Länge in Zeichen zurück, ohne das abschließende Null Zeichen.</span><span class="sxs-lookup"><span data-stu-id="6924d-135">The **\_tcslen** function returns the string length in characters, not including the terminating null character.</span></span>

<span data-ttu-id="6924d-136">Wenn Ihre Anwendung die bei der Anmeldung eingerichteten Anmelde Informationen verwenden kann, finden Sie weitere Informationen unter Abrufen von [standardmäßigen Digest](obtaining-default-digest-credentials.md)-</span><span class="sxs-lookup"><span data-stu-id="6924d-136">If your application can use the credentials established at logon, see [Obtaining Default Digest Credentials](obtaining-default-digest-credentials.md).</span></span>

 

 
