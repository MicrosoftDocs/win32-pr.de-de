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
# <a name="obtaining-alternate-digest-credentials"></a>Abrufen alternativer Digest-Anmelde Informationen

Zum Abrufen von [*Anmelde*](../secgloss/c-gly.md) Informationen, die nicht mit der aktuellen Anmelde [*Sitzung*](../secgloss/s-gly.md)verknüpft sind, geben Sie eine sec- [**\_ Winnt-Authentifizierungs \_ \_ Identitäts**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) Struktur mit Informationen für den alternativen [*Sicherheits Prinzipal*](../secgloss/s-gly.md)ein. Übergeben Sie die Struktur mithilfe des *pauthdata* -Parameters an die Funktion [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) .

In der folgenden Tabelle werden die Mitglieder der [**Identitäts Struktur "sec \_ Winnt \_ auth \_**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) " beschrieben.



| Member             | BESCHREIBUNG                                                                                                                          |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| **Benutzer**           | Eine auf NULL endende Zeichenfolge mit dem Namen des Sicherheits Prinzipals, dessen Anmelde Informationen zum Einrichten eines Sicherheits Kontexts verwendet werden. |
| **User length**     | Die Länge des **Benutzer** Members in Zeichen. Lassen Sie den abschließenden NULL-Wert aus.                                                         |
| **Domäne**         | NULL-terminierte Zeichenfolge, die die Domäne angibt, die das Konto des Sicherheits Prinzipals enthält.                                  |
| **Domänen Länge**   | Die Länge des **Domänen** Mitglieds in Zeichen. Lassen Sie den abschließenden NULL-Wert aus.                                                       |
| **Kennwort**       | NULL-terminierte Zeichenfolge mit dem Kennwort des Sicherheits Prinzipals.                                                            |
| **Passwordlength** | Die Länge des Kenn **Wort** Members in Zeichen. Lassen Sie den abschließenden NULL-Wert aus.                                                     |
| **Flags**          | Gibt an, ob die Zeichen folgen Elemente im ANSI-oder [*Unicode*](../secgloss/u-gly.md) -Format vorliegen.  |



 

In der folgenden Tabelle sind die gültigen Werte für den **Flags** -Member der-Struktur aufgeführt.



| Konstante                            | BESCHREIBUNG                                                                                                      |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| SEK \_ . WinNT-Authentifizierungs \_ \_ Identität \_ ANSI    | Zeichen folgen in dieser Struktur weisen das ANSI-Format auf.                                                                    |
| SEK \_ . WinNT-Authentifizierungs \_ \_ Identität ( \_ Unicode) | Zeichen folgen in dieser Struktur haben das [*Unicode*](../secgloss/u-gly.md) -Format. |



 

Die Struktur und Konstanten werden in der Header Datei "rpcdce. h" deklariert, die mit dem Platform Software Development Kit (SDK) verteilt wird.

Im folgenden Beispiel wird ein Client seitiger-Abruf zum Abrufen der Digest-Anmelde Informationen für ein bestimmtes Benutzerkonto veranschaulicht.


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



Die **\_ tcslen** -Funktion gibt die Zeichen folgen Länge in Zeichen zurück, ohne das abschließende Null Zeichen.

Wenn Ihre Anwendung die bei der Anmeldung eingerichteten Anmelde Informationen verwenden kann, finden Sie weitere Informationen unter Abrufen von [standardmäßigen Digest](obtaining-default-digest-credentials.md)-

 

 
