---
description: Übernimmt ein Handle für bereits vorhandene Anmeldeinformationen eines Sicherheitsprinzipals, der NTLM verwendet.
ms.assetid: 8a51ca50-0e05-4f1e-9dfc-c5d0118f65ed
title: AcquireCredentialsHandle-Funktion (NTLM) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 59e1e0142a53e0baaadd8cdf9d35b3b8fa4a3eae3abf843064c77732ad35afbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141533"
---
# <a name="acquirecredentialshandle-ntlm-function"></a>AcquireCredentialsHandle-Funktion (NTLM)

Die **Funktion AcquireCredentialsHandle (NTLM)** erhält ein Handle für bereits vorhandene Anmeldeinformationen eines [*Sicherheitsprinzipals.*](../secgloss/s-gly.md) Dieses Handle ist für die Funktionen [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md) und [**AcceptSecurityContext (NTLM)**](acceptsecuritycontext--ntlm.md) erforderlich. Dies können entweder bereits vorhandene *Anmeldeinformationen* sein, die über eine Systemanmeldung eingerichtet werden, die hier nicht beschrieben wird, oder der Aufrufer kann alternative Anmeldeinformationen bereitstellen.

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

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Prinzipals angibt, auf dessen Anmeldeinformationen das Handle verweist.

> [!Note]  
> Wenn der Prozess, der das Handle anfordert, keinen Zugriff auf die Anmeldeinformationen hat, gibt die Funktion einen Fehler zurück. Eine NULL-Zeichenfolge gibt an, dass der Prozess ein Handle für die Anmeldeinformationen des Benutzers erfordert, unter dessen [*Sicherheitskontext*](../secgloss/s-gly.md) er ausgeführt wird.

 

</dd> <dt>

*pszPackage* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des [*Sicherheitspakets*](../secgloss/s-gly.md) angibt, mit dem diese Anmeldeinformationen verwendet werden. Dies ist ein [*Sicherheitspaketname,*](../secgloss/s-gly.md) der im **Name-Member** einer [**SecPkgInfo-Struktur**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) zurückgegeben wird, die von der [**EnumerateSecurityPackages-Funktion**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) zurückgegeben wird. Nachdem ein Kontext eingerichtet wurde, kann [**QueryContextAttributes (NTLM)**](querycontextattributes--ntlm.md) aufgerufen werden, wobei *ulAttribute* auf SECPKG ATTR PACKAGE INFO festgelegt \_ \_ \_ ist, um Informationen zum verwendeten [*Sicherheitspaket*](../secgloss/s-gly.md) zurückzugeben.

</dd> <dt>

*fCredentialUse* \[ In\]
</dt> <dd>

Ein Flag, das angibt, wie diese Anmeldeinformationen verwendet werden. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                               | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_BOTH"></span><span id="secpkg_cred_both"></span><dl> <dt>**SECPKG \_ CRED \_ BOTH**</dt> </dl>             | Überprüfen Sie eingehende Anmeldeinformationen, oder verwenden Sie lokale Anmeldeinformationen, um ein ausgehendes Token vorzubereiten. Dieses Flag aktiviert beide anderen Flags.<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <dt>**SECPKG \_ CRED \_ INBOUND**</dt> </dl>    | Überprüfen Sie die Anmeldeinformationen eines eingehenden Servers. Eingehende Anmeldeinformationen können mithilfe einer Authentifizierungsstelle überprüft werden, wenn [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md) oder [**AcceptSecurityContext (NTLM)**](acceptsecuritycontext--ntlm.md) aufgerufen wird. Wenn eine solche Autorität nicht verfügbar ist, schlägt die Funktion fehl und gibt SEC \_ E \_ NO \_ AUTHENTICATING AUTHORITY \_ zurück. Die Überprüfung ist paketspezifisch.<br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <dt>**SECPKG \_ CRED \_ OUTBOUND**</dt> </dl> | Gestatten Sie einem lokalen Client, ein ausgehendes Token vorzubereiten.<br/>                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*pvLogonID* \[ In\]
</dt> <dd>

Ein Zeiger auf einen [*lokal eindeutigen Bezeichner*](../secgloss/l-gly.md) (LUID), der den Benutzer identifiziert. Dieser Parameter wird für Dateisystemprozesse wie Netzwerkumleitungen bereitgestellt. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*pAuthData* \[ In\]
</dt> <dd>

Ein Zeiger auf paketspezifische Daten. Dieser Parameter kann **NULL** sein, was angibt, dass die Standardanmeldeinformationen für dieses [*Sicherheitspaket*](../secgloss/s-gly.md) verwendet werden müssen. Um bereitgestellte Anmeldeinformationen zu verwenden, übergeben Sie eine [**SEC \_ WINNT-AUTH \_ \_ IDENTITY-Struktur,**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) die diese Anmeldeinformationen in diesem Parameter enthält. Die RPC-Laufzeit übergibt alles, was in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo)bereitgestellt wurde.

Bei Verwendung des NTLM-Pakets beträgt die maximale Zeichenlänge für Benutzername, Kennwort und Domäne 256, 256 bzw. 15.

</dd> <dt>

*pGetKeyFn* \[ In\]
</dt> <dd>

Dieser Parameter wird nicht verwendet und sollte auf **NULL** festgelegt werden.

</dd> <dt>

*pvGetKeyArgument* \[ In\]
</dt> <dd>

Dieser Parameter wird nicht verwendet und sollte auf **NULL** festgelegt werden.

</dd> <dt>

*phCredential* \[ out\]
</dt> <dd>

Ein Zeiger auf eine [CredHandle-Struktur](sspi-handles.md) zum Empfangen des Anmeldeinformationshandles.

</dd> <dt>

*ptsExpiry* \[ out\]
</dt> <dd>

Ein Zeiger auf eine [**TimeStamp-Struktur,**](timestamp.md) die den Zeitpunkt empfängt, zu dem die zurückgegebenen Anmeldeinformationen ablaufen. Der in dieser **TimeStamp-Struktur** zurückgegebene Wert hängt von der [*eingeschränkten Delegierung*](../secgloss/s-gly.md)ab. Das [*Sicherheitspaket*](../secgloss/s-gly.md) muss diesen Wert in Ortszeit zurückgeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt die Funktion SEC \_ E \_ OK zurück.

Wenn die Funktion fehlschlägt, wird einer der folgenden Fehlercodes zurückgegeben.



| Rückgabecode                                                                                                 | Beschreibung                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ INSUFFICIENT \_ MEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abzuschließen.<br/>                                                                  |
| <dl> <dt>**\_INTERNER \_ SEC \_ E-FEHLER**</dt> </dl>      | Fehler, der keinem SSPI-Fehlercode zugeordnet wurde.<br/>                                                                               |
| <dl> <dt>**SEC \_ E \_ NO \_ CREDENTIALS**</dt> </dl>      | In der [*eingeschränkten Delegierung*](../secgloss/s-gly.md)sind keine Anmeldeinformationen verfügbar.<br/> |
| <dl> <dt>**SEC \_ E \_ NOT \_ OWNER**</dt> </dl>           | Der Aufrufer der Funktion verfügt nicht über die erforderlichen Anmeldeinformationen.<br/>                                                                     |
| <dl> <dt>**SEC \_ E \_ SECPKG \_ NICHT \_ GEFUNDEN**</dt> </dl>   | Das angeforderte [*Sicherheitspaket*](../secgloss/s-gly.md) ist nicht vorhanden.<br/>                                                                                          |
| <dl> <dt>**SEC \_ E \_ UNKNOWN \_ CREDENTIALS**</dt> </dl> | Die für das Paket angegebenen Anmeldeinformationen wurden nicht erkannt.<br/>                                                                            |



 

## <a name="remarks"></a>Hinweise

Die **Funktion AcquireCredentialsHandle (NTLM)** gibt ein Handle für die Anmeldeinformationen eines Prinzipals zurück, z. B. eines Benutzers oder Clients, das von einer bestimmten [*eingeschränkten Delegierung*](../secgloss/s-gly.md)verwendet wird. Dies kann das Handle für bereits vorhandene Anmeldeinformationen sein, oder die Funktion kann einen neuen Satz von Anmeldeinformationen erstellen und zurückgeben. Dieses Handle kann in nachfolgenden Aufrufen der Funktionen [**AcceptSecurityContext (NTLM)**](acceptsecuritycontext--ntlm.md) und [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md) verwendet werden.

Im Allgemeinen lässt **AcquireCredentialsHandle (NTLM)** nicht zu, dass ein Prozess ein Handle für die Anmeldeinformationen anderer Benutzer erhält, die auf demselben Computer angemeldet sind. Ein Aufrufer mit SE \_ TCB \_ [*NAME-Berechtigung*](../secgloss/s-gly.md) hat jedoch die Möglichkeit, den [*Anmeldebezeichner*](../secgloss/l-gly.md) (LUID) eines vorhandenen Anmeldesitzungstokens anzugeben, um ein Handle für die Anmeldeinformationen dieser Sitzung abzurufen. In der Regel wird dies von Kernelmodusmodulen verwendet, die im Namen eines angemeldeten Benutzers agieren müssen.

Ein Paket ruft möglicherweise die Funktion in *pGetKeyFn auf,* die vom RPC-Laufzeittransport bereitgestellt wird. Wenn der Transport das Konzept des Rückrufs zum Abrufen von Anmeldeinformationen nicht unterstützt, muss dieser Parameter **NULL** sein.

Bei Kernelmodusaufrufern müssen die folgenden Unterschiede beachtet werden:

-   Die beiden Zeichenfolgenparameter müssen [*Unicode-Zeichenfolgen*](../secgloss/u-gly.md) sein.
-   Die Pufferwerte müssen im virtuellen Prozessspeicher und nicht aus dem Pool zugeordnet werden.

Wenn Sie die zurückgegebenen Anmeldeinformationen verwendet haben, können Sie den von den Anmeldeinformationen verwendeten Arbeitsspeicher freigeben, indem Sie die [**FreeCredentialsHandle-Funktion**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Sspi.h (include Security.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Unicode- und ANSI-Name<br/>   | **AcquireCredentialsHandleW** (Unicode) und **AcquireCredentialsHandleA** (ANSI)<br/>            |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[SSPI-Funktionen](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (NTLM)**](acceptsecuritycontext--ntlm.md)
</dt> <dt>

[**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md)
</dt> <dt>

[**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
