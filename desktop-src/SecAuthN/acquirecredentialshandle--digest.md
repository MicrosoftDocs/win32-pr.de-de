---
description: Übernimmt ein Handle für bereits vorhandene Anmeldeinformationen eines Sicherheitsprinzipals, der digest verwendet.
ms.assetid: 79f49240-e394-4584-8db7-ef721672ba6b
title: AcquireCredentialsHandle(Digest)-Funktion (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 561bb4c6fd95bfd22d36091a6f9d23b59720618a13eb7e994f74e77c87849abc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141583"
---
# <a name="acquirecredentialshandle-digest-function"></a>AcquireCredentialsHandle(Digest)-Funktion

Die **AcquireCredentialsHandle-Funktion (Digest)** erhält ein Handle für bereits vorhandene Anmeldeinformationen eines [*Sicherheitsprinzipals.*](../secgloss/s-gly.md) Dieses Handle ist für die [**Funktionen AcceptSecurityContext (Digest) und**](acceptsecuritycontext--digest.md) [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) erforderlich. Dies können entweder bereits vorhandene Anmeldeinformationen *sein,* die über eine Systemanmeldung eingerichtet werden, die hier nicht beschrieben wird, oder der Aufrufer kann alternative Anmeldeinformationen bereitstellen.

> [!Note]  
> Dies ist keine "Anmeldung beim Netzwerk" und impliziert nicht das Sammeln von Anmeldeinformationen.

 

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS SEC_Entry AcquireCredentialsHandle(
  _In_  SEC_CHAR       *pszPrincipal,
  _In_  SEC_CHAR       *pszPackage,
  _In_  ULONG          fCredentialUse,
  _In_  PLUID          pvLogonID,
  _In_  PVOID          pAuthData,
  _In_  SEC_GET_KEY_FN pGetKeyFn,
  _In_  PVOID          pvGetKeyArgument,
  _Out_ PCredHandle    phCredential,
  _Out_ PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszPrincipal* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Prinzipals angibt, auf dessen Anmeldeinformationen das Handle verweist.

Bei Verwendung des Digest-SSP ist dieser Parameter optional.

> [!Note]  
> Wenn der Prozess, der das Handle angibt, keinen Zugriff auf die Anmeldeinformationen hat, gibt die Funktion einen Fehler zurück. Eine NULL-Zeichenfolge gibt an, dass der Prozess ein Handle für die Anmeldeinformationen des Benutzers erfordert, unter dessen Sicherheitskontext [*er*](../secgloss/s-gly.md) ausgeführt wird.

 

</dd> <dt>

*pszPackage* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Sicherheitspakets angibt, mit dem diese Anmeldeinformationen verwendet werden. [](../secgloss/s-gly.md) Dies ist ein [*Sicherheitspaketname,*](../secgloss/s-gly.md) der im **Name-Member** einer [**SecPkgInfo-Struktur**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) zurückgegeben wird, die von der [**EnumerateSecurityPackages-Funktion zurückgegeben**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) wird. Nachdem ein Kontext eingerichtet wurde, [**kann QueryContextAttributes (Digest)**](querycontextattributes--digest.md) mit *ulAttribute* aufgerufen werden, das auf SECPKG ATTR PACKAGE INFO festgelegt ist, um Informationen zum sicherheitspaket zurück zu geben, das \_ verwendet \_ \_ wird. [](../secgloss/s-gly.md)

Wenn Sie den Digest-SSP verwenden, legen Sie diesen Parameter auf WDIGEST \_ SP \_ NAME fest.

</dd> <dt>

*fCredentialUse* \[ In\]
</dt> <dd>

Ein Flag, das angibt, wie diese Anmeldeinformationen verwendet werden. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                               | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <dt>**SECPKG \_ CRED \_ EINGEHEND**</dt> </dl>    | Überprüfen Sie die Anmeldeinformationen eines eingehenden Servers. Eingehende Anmeldeinformationen können mithilfe einer Authentifizierungsstelle überprüft werden, wenn [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) oder [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) aufgerufen wird. Wenn eine solche Autorität nicht verfügbar ist, ist die Funktion nicht verfügbar und gibt SEC \_ E \_ NO \_ AUTHENTICATING AUTHORITY \_ zurück. Die Validierung ist paketspezifisch.<br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <dt>**SECPKG \_ CRED \_ OUTBOUND**</dt> </dl> | Ermöglichen Sie es lokalen Client-Anmeldeinformationen, ein ausgehendes Token vorzubereiten.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

*pvLogonID* \[ In\]
</dt> <dd>

Ein Zeiger auf einen lokal [*eindeutigen Bezeichner*](../secgloss/l-gly.md) (LUID), der den Benutzer identifiziert. Dieser Parameter wird für Dateisystemprozesse wie Netzwerkumleitungen bereitgestellt. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*pAuthData* \[ In\]
</dt> <dd>

Ein Zeiger auf paketspezifische Daten. Dieser Parameter kann **NULL sein,** was angibt, dass die Standardanmeldeinformationen für [*dieses*](../secgloss/s-gly.md) Sicherheitspaket verwendet werden müssen. Um die angegebenen Anmeldeinformationen zu verwenden, übergeben Sie eine [**SEC \_ WINNT \_ AUTH \_ IDENTITY-Struktur,**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) die diese Anmeldeinformationen in diesem Parameter enthält. Die RPC-Laufzeit übergibt das, was in [**RpcBindingSetAuthInfo bereitgestellt wurde.**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo)

Bei Verwendung des Digest-SSP ist dieser Parameter ein Zeiger auf eine [**SEC \_ WINNT \_ AUTH \_ IDENTITY-Struktur,**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) die Authentifizierungsinformationen enthält, die zum Suchen der Anmeldeinformationen verwendet werden.

</dd> <dt>

*pGetKeyFn* \[ In\]
</dt> <dd>

Dieser Parameter wird nicht verwendet und sollte auf NULL **festgelegt werden.**

</dd> <dt>

*pvGetKeyArgument* \[ In\]
</dt> <dd>

Dieser Parameter wird nicht verwendet und sollte auf NULL **festgelegt werden.**

</dd> <dt>

*phCredential* \[ out\]
</dt> <dd>

Ein Zeiger auf eine [CredHandle-Struktur,](sspi-handles.md) um das Anmeldeinformationshandle zu empfangen.

</dd> <dt>

*ptsExpiry* \[ out\]
</dt> <dd>

Ein Zeiger auf eine [**TimeStamp-Struktur,**](timestamp.md) die den Zeitpunkt empfängt, zu dem die zurückgegebenen Anmeldeinformationen ablaufen. Der in dieser **TimeStamp-Struktur zurückgegebene** Wert hängt von der [*eingeschränkten Delegierung ab.*](../secgloss/s-gly.md) Das [*Sicherheitspaket*](../secgloss/s-gly.md) muss diesen Wert in Ortszeit zurückgeben.

Dieser Parameter wird auf eine konstante maximale Zeit festgelegt. Es gibt keine Ablaufzeit für [*Digestsicherheitskontexte*](../secgloss/s-gly.md)oder Anmeldeinformationen oder bei Verwendung des Digest-SSP.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt die Funktion SEC \_ E \_ OK zurück.

Wenn die Funktion fehlschlägt, wird einer der folgenden Fehlercodes zurückgegeben.



| Rückgabecode                                                                                                 | Beschreibung                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_S.E \_ NICHT GENÜGEND \_ ARBEITSSPEICHER**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abschließen zu können.<br/>                                                                  |
| <dl> <dt>**INTERNER \_ FEHLER IN SEKUNDE E \_ \_**</dt> </dl>      | Es ist ein Fehler aufgetreten, der einem SSPI-Fehlercode nicht zuordnen konnte.<br/>                                                                               |
| <dl> <dt>**SEC \_ E \_ NO \_ CREDENTIALS**</dt> </dl>      | In der eingeschränkten Delegierung sind [*keine Anmeldeinformationen verfügbar.*](../secgloss/s-gly.md)<br/> |
| <dl> <dt>**SEC \_ E \_ NOT \_ OWNER**</dt> </dl>           | Der Aufrufer der Funktion verfügt nicht über die erforderlichen Anmeldeinformationen.<br/>                                                                     |
| <dl> <dt>**SEC \_ E \_ SECPKG \_ NICHT \_ GEFUNDEN**</dt> </dl>   | Das [*angeforderte Sicherheitspaket*](../secgloss/s-gly.md) ist nicht vorhanden.<br/>                                                                                          |
| <dl> <dt>**SEC \_ E \_ UNKNOWN \_ CREDENTIALS**</dt> </dl> | Die für das Paket angegebenen Anmeldeinformationen wurden nicht erkannt.<br/>                                                                            |



 

## <a name="remarks"></a>Hinweise

Die **AcquireCredentialsHandle-Funktion (Digest)** gibt ein Handle für die Anmeldeinformationen eines Prinzipals zurück, z. B. eines Benutzers oder Clients, wie es von einer bestimmten eingeschränkten [*Delegierung verwendet wird.*](../secgloss/s-gly.md) Dies kann das Handle für bereits vorhandene Anmeldeinformationen sein, oder die Funktion kann einen neuen Satz von Anmeldeinformationen erstellen und zurückgeben. Dieses Handle kann in nachfolgenden Aufrufen der [**Funktionen AcceptSecurityContext (Digest) und**](acceptsecuritycontext--digest.md) [**InitializeSecurityContext (Digest) verwendet**](initializesecuritycontext--digest.md) werden.

Im Allgemeinen lässt **AcquireCredentialsHandle (Digest)** nicht zu, dass ein Prozess ein Handle für die Anmeldeinformationen anderer Benutzer erhält, die auf demselben Computer angemeldet sind. Ein Aufrufer mit SE TCB NAME-Berechtigung hat jedoch die Möglichkeit, die \_ \_ Anmelde-ID (LUID) [](../secgloss/s-gly.md) [](../secgloss/l-gly.md) eines vorhandenen Anmeldesitzungstokens anzugeben, um ein Handle für die Anmeldeinformationen dieser Sitzung zu erhalten. In der Regel wird dies von Kernelmodusmodulen verwendet, die im Auftrag eines angemeldeten Benutzers agieren müssen.

Ein Paket kann die Funktion in *pGetKeyFn* aufrufen, die vom RPC-Laufzeittransport bereitgestellt wird. Wenn der Transport das Konzept des Rückrufs zum Abrufen von Anmeldeinformationen nicht unterstützt, muss dieser Parameter **NULL sein.**

Für Aufrufer im Kernelmodus müssen die folgenden Unterschiede beachtet werden:

-   Die beiden Zeichenfolgenparameter müssen [*Unicode-Zeichenfolgen*](../secgloss/u-gly.md) sein.
-   Die Pufferwerte müssen im virtuellen Prozessspeicher und nicht aus dem Pool zugeordnet werden.

Wenn Sie die zurückgegebenen Anmeldeinformationen nicht mehr verwenden, geben Sie den von den Anmeldeinformationen verwendeten Arbeitsspeicher frei, indem Sie die [**FreeCredentialsHandle-Funktion**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Sspi.h (einschließlich Security.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Unicode- und ANSI-Name<br/>   | **AcquireCredentialsHandleW** (Unicode) und **AcquireCredentialsHandleA** (ANSI)<br/>            |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[SSPI-Funktionen](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md)
</dt> <dt>

[**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md)
</dt> <dt>

[**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
