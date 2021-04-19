---
description: Die AcquireCredentialsHandle (kredssp)-Funktion Ruft ein Handle für bereits vorhandene Anmelde Informationen eines Sicherheits Prinzipals ab.
ms.assetid: 3b73decf-75d4-4bc4-b7ca-5f16aaadff29
title: AcquireCredentialsHandle (CredSSP)-Funktion
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 0dbece18bc7a7de8ec35764c9879380e29292e92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349280"
---
# <a name="acquirecredentialshandle-credssp-function"></a>AcquireCredentialsHandle (CredSSP)-Funktion

Die **AcquireCredentialsHandle (kredssp)** -Funktion Ruft ein Handle für bereits vorhandene Anmelde Informationen eines Sicherheits Prinzipals ab. Dieses Handle ist für die Funktionen [**InitializeSecurityContext (**](initializesecuritycontext--credssp.md) Auflistungs Kontext) und [**accepted (kredssp)**](acceptsecuritycontext--credssp.md) erforderlich. Hierbei kann es sich um bereits vorhandene *Anmelde* Informationen handeln, die über eine System Anmeldung eingerichtet werden, die hier nicht beschrieben wird, oder der Aufrufer kann Alternative Anmelde Informationen bereitstellen.

> [!Note]  
> Dabei handelt es sich nicht um eine "beim Netzwerk anmelden", und es ist nicht beabsichtigt, Anmelde Informationen zu sammeln.

## <a name="syntax"></a>Syntax

```C++
SECURITY_STATUS SEC_ENTRY AcquireCredentialsHandle(
  _In_opt_   SEC_CHAR       *pszPrincipal,
  _In_       SEC_CHAR       *pszPackage,
  _In_       unsigned long  fCredentialUse,
  _In_opt_   void           *pvLogonID,
  _In_opt_   void           *pAuthData,
  _In_opt_   SEC_GET_KEY_FN pGetKeyFn,
  _Reserved_ void           *pvGetKeyArgument,
  _Out_      PCredHandle    phCredential,
  _Out_opt_  PTimeStamp     ptsExpiry
);
```

## <a name="parameters"></a>Parameter

*pszprincipal* \[ in, optional\]

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Prinzipals angibt, auf dessen Anmelde Informationen das Handle verweist.

> [!Note]  
> Wenn der Prozess, der das Handle anfordert, keinen Zugriff auf die Anmelde Informationen hat, gibt die Funktion einen Fehler zurück. Eine NULL-Zeichenfolge gibt an, dass der Prozess ein Handle für die Anmelde Informationen des Benutzers erfordert, in dessen Sicherheitskontext er ausgeführt wird.

*pszpackage* \[ in\]

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Sicherheitspakets angibt, mit dem diese Anmelde Informationen verwendet werden. Dies ist ein Sicherheitspaket Name, der im **Name** -Member einer [**secpkginfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) -Struktur zurückgegeben wird, die von der [**enumeratesecuritypackages**](/windows/win32/api/sspi/nf-sspi-enumeratesecuritypackagesa) -Funktion zurückgegeben wird. Nach dem Einrichten eines Kontexts kann [**QueryContextAttributes (kredssp)**](querycontextattributes--credssp.md) aufgerufen werden, wobei *ulattribute* auf **secpkg \_ attr \_ Package \_ Info** festgelegt ist, um Informationen zum verwendeten Sicherheitspaket zurückzugeben.

*"f"* \[ in\]

Ein Flag, das angibt, wie diese Anmelde Informationen verwendet werden. Dieser Parameter kann einen der folgenden Werte annehmen.

| Wert                                                                                                                                                                                                                                        | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **secpkg-in \_ \_ eingehender Richtung**<br/>0x1  | Überprüfen Sie die Anmelde Informationen eines eingehenden Servers. Eingehende Anmelde Informationen können mithilfe einer authentifizier enden Zertifizierungsstelle überprüft werden, wenn [**InitializeSecurityContext (aufzurufen)**](initializesecuritycontext--credssp.md) oder [**Accept-SecurityContext (kredssp)**](acceptsecuritycontext--credssp.md) aufgerufen wird. Wenn eine solche Autorität nicht verfügbar ist, schlägt die Funktion fehl und gibt **Sek. \_ E \_ keine \_ authentifizier Ende Zertifizierungs \_** Stelle zurück. Validierung ist Paket spezifisch |
| **Outbound für secpkg-Datenverkehr \_ \_**<br/>0x0 | Ermöglicht die Vorbereitung eines ausgehenden Tokens durch lokale Client Anmelde Informationen. |

*pvlogonid* \[ in, optional\]

Ein Zeiger auf einen [*lokal eindeutigen Bezeichner*](../secgloss/l-gly.md#_security_locally_unique_identifier_gly) (LUID), der den Benutzer identifiziert. Dieser Parameter wird für Dateisystem Prozesse, z. b. netzwerkredirectors, bereitgestellt. Dieser Parameter kann **NULL** sein.

*pauthdata* \[ in, optional\]

Ein Zeiger auf eine [**kredssp \_ -**](/windows/win32/api/credssp/ns-credssp-credssp_cred) Erstellungs Struktur, die Authentifizierungsdaten für SChannel-und Aushandlungs Pakete angibt.

*pgetkeyfn* \[ in, optional\]

Reserviert. Dieser Parameter wird nicht verwendet und sollte auf **null** festgelegt werden.

*pvgetkeyargument* \[ in, optional\]

Reserviert. Dieser Parameter muss auf **null** festgelegt werden.

*phcredential* \[ vorgenommen\]

Ein Zeiger auf die [kredhandle](sspi-handles.md) -Struktur, die das Handle für die Anmelde Informationen empfängt.

*ptsexpiry* \[ Out, optional\]

Ein Zeiger auf eine [**Zeitstempel**](timestamp.md) Struktur, die die Uhrzeit empfängt, zu der die zurückgegebenen Anmelde Informationen ablaufen. Der empfangene Struktur Wert hängt vom Sicherheitspaket ab, das den Wert in Ortszeit angeben muss.

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird **Sek. \_ E \_ OK** zurückgegeben.

Wenn die Funktion fehlschlägt, wird einer der folgenden Fehlercodes zurückgegeben.

| Rückgabecode                      | Beschreibung                                                              |
|----------------------------------|--------------------------------------------------------------------------|
| **SEK \_ b \_ nicht genügend Arbeits \_ Speicher** | Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abzuschließen. |
| **Sek. \_ E ( \_ interner \_ Fehler)**      | Es ist ein Fehler aufgetreten, der keinem SSPI-Fehlercode zugeordnet wurde.                |
| **s \_ E \_ keine \_ Anmelde Informationen**      | Im Sicherheitspaket sind keine Anmelde Informationen verfügbar.                    |
| **Sek. \_ E \_ nicht \_ Besitzer**           | Der Aufrufer der Funktion verfügt nicht über die erforderlichen Anmelde Informationen.      |
| **Sek. \_ E \_ secpkg \_ nicht \_ gefunden**   | Das angeforderte Sicherheitspaket ist nicht vorhanden.                           |
| **SEK \_ . \_ unbekannte \_ Anmelde Informationen** | Die für das Paket angegebenen Anmelde Informationen wurden nicht erkannt.             |

## <a name="remarks"></a>Bemerkungen

Die **AcquireCredentialsHandle (kredssp)** -Funktion gibt ein Handle für die Anmelde Informationen eines Prinzipals (z. b. einen Benutzer oder Client) zurück, wie er von einem bestimmten Sicherheitspaket verwendet wird. Die Funktion kann das Handle entweder für bereits vorhandene Anmelde Informationen oder für neu erstellte Anmelde Informationen zurückgeben und zurückgeben. Dieses Handle kann in nachfolgenden Aufrufen der Funktionen " [**Accept tsecuritycontext (**](acceptsecuritycontext--credssp.md) aufzurufen)" und " [**InitializeSecurityContext (aufzurufen)**](initializesecuritycontext--credssp.md) " verwendet werden.

Im Allgemeinen gibt **AcquireCredentialsHandle (kredssp)** nicht die Anmelde Informationen anderer Benutzer an, die am gleichen Computer angemeldet sind. Ein Aufrufer mit SE \_ TCB- \_ namens [*Berechtigung*](../secgloss/p-gly.md#_security_privilege_gly) kann jedoch die Anmelde Informationen einer vorhandenen Anmelde Sitzung abrufen, indem er den [*Anmelde Bezeichner*](../secgloss/l-gly.md#_security_logon_identifier_gly) (LUID) der Sitzung angibt. Diese wird in der Regel von Kernelmodusmodulen verwendet, die im Auftrag eines angemeldeten Benutzers agieren müssen.

Ein Paket kann die Funktion in *pgetkeyfn* aufrufen, die vom RPC-Lauf Zeit Transport bereitgestellt wird. Wenn der Transport die Rückruffunktion zum Abrufen von Anmelde Informationen nicht unterstützt, muss dieser Parameter **null** sein.

Bei kernelmodusaufrufern müssen die folgenden Unterschiede beachtet werden:

- Die beiden Zeichen folgen Parameter müssen [*Unicode*](../secgloss/u-gly.md#_security_unicode_gly) -Zeichen folgen sein.
- Die Puffer Werte müssen im virtuellen Arbeitsspeicher des Prozesses zugeordnet werden, nicht aus dem Pool.

Wenn Sie die zurückgegebenen Anmelde Informationen nicht mehr verwenden, geben Sie den von den Anmelde Informationen genutzten Arbeitsspeicher frei, indem Sie die [**freecredentialshandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Nur Windows Vista \[ -Desktop-Apps\]                                              |
| Unterstützte Mindestversion (Server) | Nur Windows Server 2008 \[ -Desktop-Apps\]                                        |
| Header                   | SSPI. h (Include Security. h)                                                      |
| Bibliothek                  | Secur32. lib                                                                      |
| DLL                      | Secur32.dll                                                                      |
| Unicode- und ANSI-Name   | **Acquirecredentialshandlew** (Unicode) und **AcquireCredentialsHandleA** (ANSI) |

## <a name="see-also"></a>Siehe auch

- [SSPI-Funktionen](authentication-functions.md#sspi-functions)
- [**Accept-SecurityContext (kredssp)**](acceptsecuritycontext--credssp.md)
- [**InitializeSecurityContext (kredssp)**](initializesecuritycontext--credssp.md)
- [**Freecredentialshandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
