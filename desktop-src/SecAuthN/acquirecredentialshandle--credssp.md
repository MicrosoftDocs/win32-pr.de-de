---
description: Die Funktion AcquireCredentialsHandle (CredSSP) erhält ein Handle für bereits vorhandene Anmeldeinformationen eines Sicherheitsprinzipals.
ms.assetid: 3b73decf-75d4-4bc4-b7ca-5f16aaadff29
title: AcquireCredentialsHandle (CredSSP)-Funktion
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 22ab5b4f9696e266e6d07b3085cafe10384e8b6b266c9e20672021fa04e97998
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101480"
---
# <a name="acquirecredentialshandle-credssp-function"></a>AcquireCredentialsHandle (CredSSP)-Funktion

Die **Funktion AcquireCredentialsHandle (CredSSP)** erhält ein Handle für bereits vorhandene Anmeldeinformationen eines Sicherheitsprinzipals. Dieses Handle ist für die [**Funktionen InitializeSecurityContext (CredSSP) und**](initializesecuritycontext--credssp.md) [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) erforderlich. Dies können entweder bereits vorhandene Anmeldeinformationen *sein,* die über eine Systemanmeldung eingerichtet werden, die hier nicht beschrieben wird, oder der Aufrufer kann alternative Anmeldeinformationen bereitstellen.

> [!Note]  
> Dies ist keine "Anmeldung beim Netzwerk" und impliziert nicht das Sammeln von Anmeldeinformationen.

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

*pszPrincipal* \[ in, optional\]

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Prinzipals angibt, auf dessen Anmeldeinformationen das Handle verweist.

> [!Note]  
> Wenn der Prozess, der das Handle angibt, keinen Zugriff auf die Anmeldeinformationen hat, gibt die Funktion einen Fehler zurück. Eine NULL-Zeichenfolge gibt an, dass der Prozess ein Handle für die Anmeldeinformationen des Benutzers erfordert, unter dessen Sicherheitskontext er ausgeführt wird.

*pszPackage* \[ In\]

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Sicherheitspakets angibt, mit dem diese Anmeldeinformationen verwendet werden. Dies ist ein Sicherheitspaketname, der im **Name-Member** einer [**SecPkgInfo-Struktur**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) zurückgegeben wird, die von der [**EnumerateSecurityPackages-Funktion zurückgegeben**](/windows/win32/api/sspi/nf-sspi-enumeratesecuritypackagesa) wird. Nachdem ein Kontext eingerichtet wurde, kann [**QueryContextAttributes (CredSSP)**](querycontextattributes--credssp.md) aufgerufen werden, während *ulAttribute* auf **SECPKG \_ ATTR \_ PACKAGE \_ INFO** festgelegt ist, um Informationen über das verwendete Sicherheitspaket zurück zu geben.

*fCredentialUse* \[ In\]

Ein Flag, das angibt, wie diese Anmeldeinformationen verwendet werden. Dieser Parameter kann einen der folgenden Werte annehmen.

| Wert                                                                                                                                                                                                                                        | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SECPKG \_ CRED \_ EINGEHEND**<br/>0x1  | Überprüfen Sie die Anmeldeinformationen eines eingehenden Servers. Eingehende Anmeldeinformationen können mithilfe einer Authentifizierungsstelle überprüft werden, wenn [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) oder [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) aufgerufen wird. Wenn eine solche Autorität nicht verfügbar ist, ist die Funktion nicht verfügbar und gibt **SEC \_ E NO \_ \_ AUTHENTICATING AUTHORITY \_ zurück.** Die Validierung ist paketspezifisch. |
| **SECPKG \_ CRED \_ OUTBOUND**<br/>0x0 | Ermöglichen Sie es lokalen Client-Anmeldeinformationen, ein ausgehendes Token vorzubereiten. |

*pvLogonId* \[ in, optional\]

Ein Zeiger auf einen lokal [*eindeutigen Bezeichner*](../secgloss/l-gly.md#_security_locally_unique_identifier_gly) (LUID), der den Benutzer identifiziert. Dieser Parameter wird für Dateisystemprozesse wie Netzwerkumleitungen bereitgestellt. Dieser Parameter kann **NULL** sein.

*pAuthData* \[ in, optional\]

Ein Zeiger auf eine [**CREDSSP \_ CRED-Struktur,**](/windows/win32/api/credssp/ns-credssp-credssp_cred) die Authentifizierungsdaten für Schannel- und Negotiate-Pakete angibt.

*pGetKeyFn* \[ in, optional\]

Reserviert. Dieser Parameter wird nicht verwendet und sollte auf NULL **festgelegt werden.**

*pvGetKeyArgument* \[ in, optional\]

Reserviert. Dieser Parameter muss auf NULL **festgelegt werden.**

*phCredential* \[ out\]

Ein Zeiger auf die [CredHandle-Struktur,](sspi-handles.md) die das Anmeldeinformationshandle erhält.

*ptsExpiry* \[ out, optional\]

Ein Zeiger auf eine [**TimeStamp-Struktur,**](timestamp.md) die den Zeitpunkt empfängt, zu dem die zurückgegebenen Anmeldeinformationen ablaufen. Der empfangene Strukturwert hängt vom Sicherheitspaket ab, das den Wert in Ortszeit angeben muss.

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, wird **SEC \_ E OK \_ zurückgegeben.**

Wenn die Funktion fehlschlägt, wird einer der folgenden Fehlercodes zurückgegeben.

| Rückgabecode                      | Beschreibung                                                              |
|----------------------------------|--------------------------------------------------------------------------|
| **\_S.E \_ NICHT GENÜGEND \_ ARBEITSSPEICHER** | Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abschließen zu können. |
| **INTERNER \_ FEHLER IN SEKUNDE E \_ \_**      | Es ist ein Fehler aufgetreten, der einem SSPI-Fehlercode nicht zuordnen konnte.                |
| **SEC \_ E \_ NO \_ CREDENTIALS**      | Im Sicherheitspaket sind keine Anmeldeinformationen verfügbar.                    |
| **SEC \_ E \_ NOT \_ OWNER**           | Der Aufrufer der Funktion verfügt nicht über die erforderlichen Anmeldeinformationen.      |
| **SEC \_ E \_ SECPKG \_ NICHT \_ GEFUNDEN**   | Das angeforderte Sicherheitspaket ist nicht vorhanden.                           |
| **SEC \_ E \_ UNKNOWN \_ CREDENTIALS** | Die für das Paket angegebenen Anmeldeinformationen wurden nicht erkannt.             |

## <a name="remarks"></a>Hinweise

Die **Funktion AcquireCredentialsHandle (CredSSP)** gibt ein Handle für die Anmeldeinformationen eines Prinzipals zurück, z. B. eines Benutzers oder Clients, wie von einem bestimmten Sicherheitspaket verwendet. Die Funktion kann das Handle entweder an bereits vorhandene Anmeldeinformationen oder neu erstellte Anmeldeinformationen zurückgeben und zurückgeben. Dieses Handle kann in nachfolgenden Aufrufen der [**Funktionen AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) und [**InitializeSecurityContext (CredSSP) verwendet**](initializesecuritycontext--credssp.md) werden.

Im Allgemeinen stellt **AcquireCredentialsHandle (CredSSP)** nicht die Anmeldeinformationen anderer Benutzer zur Verfügung, die auf demselben Computer angemeldet sind. Ein Aufrufer mit SE TCB NAME-Berechtigung kann jedoch die Anmeldeinformationen einer vorhandenen Anmeldesitzung abrufen, indem er den Anmeldebezeichner \_ \_ (LUID) dieser Sitzung anknöpf. [](../secgloss/p-gly.md#_security_privilege_gly) [](../secgloss/l-gly.md#_security_logon_identifier_gly) In der Regel wird dies von Kernelmodusmodulen verwendet, die im Auftrag eines angemeldeten Benutzers agieren müssen.

Ein Paket kann die Funktion in *pGetKeyFn* aufrufen, die vom RPC-Laufzeittransport bereitgestellt wird. Wenn der Transport das Konzept des Rückrufs zum Abrufen von Anmeldeinformationen nicht unterstützt, muss dieser Parameter **NULL sein.**

Für Aufrufer im Kernelmodus müssen die folgenden Unterschiede beachtet werden:

- Die beiden Zeichenfolgenparameter müssen [*Unicode-Zeichenfolgen*](../secgloss/u-gly.md#_security_unicode_gly) sein.
- Die Pufferwerte müssen im virtuellen Prozessspeicher und nicht aus dem Pool zugeordnet werden.

Wenn Sie die zurückgegebenen Anmeldeinformationen nicht mehr verwenden, geben Sie den von den Anmeldeinformationen verwendeten Arbeitsspeicher frei, indem Sie die [**FreeCredentialsHandle-Funktion**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) aufrufen.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows Nur \[ Vista-Desktop-Apps\]                                              |
| Unterstützte Mindestversion (Server) | Windows Nur Server \[ 2008-Desktop-Apps\]                                        |
| Header                   | Sspi.h (einschließlich Security.h)                                                      |
| Bibliothek                  | Secur32.lib                                                                      |
| DLL                      | Secur32.dll                                                                      |
| Unicode- und ANSI-Name   | **AcquireCredentialsHandleW** (Unicode) und **AcquireCredentialsHandleA** (ANSI) |

## <a name="see-also"></a>Siehe auch

- [SSPI-Funktionen](authentication-functions.md#sspi-functions)
- [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md)
- [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md)
- [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
