---
description: Übernimmt ein Handle für bereits vorhandene Anmeldeinformationen eines Sicherheitsprinzipals, der Schannel verwendet.
ms.assetid: 0f006670-a1e5-47ed-baf5-ed55bd42b468
title: AcquireCredentialsHandle-Funktion (Schannel) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: d2fb9812817e27576667f7fa0ff5312eea8cea41743cbfc9e5b03267f837011f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101440"
---
# <a name="acquirecredentialshandle-schannel-function"></a>AcquireCredentialsHandle-Funktion (Schannel)

Die **AcquireCredentialsHandle (Schannel)-Funktion** übernimmt ein Handle für bereits vorhandene Anmeldeinformationen eines [*Sicherheitsprinzipals.*](../secgloss/s-gly.md) Dieses Handle ist für die Funktionen [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) und [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) erforderlich. Dies können entweder bereits vorhandene *Anmeldeinformationen* sein, die über eine Systemanmeldung eingerichtet werden, die hier nicht beschrieben wird, oder der Aufrufer kann alternative Anmeldeinformationen bereitstellen.

> [!Note]  
> Dies ist keine "Anmeldung beim Netzwerk" und impliziert nicht das Sammeln von Anmeldeinformationen.

 

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS SEC_Entry AcquireCredentialsHandle(
  _In_opt_  SEC_CHAR       *pszPrincipal,
  _In_      SEC_CHAR       *pszPackage,
  _In_      ULONG          fCredentialUse,
  _In_opt_  PLUID          pvLogonID,
  _In_opt_  PVOID          pAuthData,
  _In_opt_  SEC_GET_KEY_FN pGetKeyFn,
  _In_opt_  PVOID          pvGetKeyArgument,
  _Out_     PCredHandle    phCredential,
  _Out_opt_ PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszPrincipal* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Prinzipals angibt, auf dessen Anmeldeinformationen das Handle verweist.

Bei Verwendung des Schannel-SSP wird dieser Parameter nicht verwendet und sollte auf **NULL** festgelegt werden.

> [!Note]  
> Wenn der Prozess, der das Handle anfordert, keinen Zugriff auf die Anmeldeinformationen hat, gibt die Funktion einen Fehler zurück. Eine NULL-Zeichenfolge gibt an, dass der Prozess ein Handle für die Anmeldeinformationen des Benutzers erfordert, unter dessen [*Sicherheitskontext*](../secgloss/s-gly.md) er ausgeführt wird.

 

</dd> <dt>

*pszPackage* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des [*Sicherheitspakets*](../secgloss/s-gly.md) angibt, mit dem diese Anmeldeinformationen verwendet werden. Dies ist ein [*Sicherheitspaketname,*](../secgloss/s-gly.md) der im **Name-Member** einer [**SecPkgInfo-Struktur**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) zurückgegeben wird, die von der [**EnumerateSecurityPackages-Funktion**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) zurückgegeben wird. Nachdem ein Kontext eingerichtet wurde, kann [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md) aufgerufen werden, wobei *ulAttribute* auf SECPKG ATTR PACKAGE INFO festgelegt \_ \_ \_ ist, um Informationen zum verwendeten [*Sicherheitspaket*](../secgloss/s-gly.md) zurückzugeben.

Wenn Sie den Schannel-SSP verwenden, legen Sie diesen Parameter auf UNISP \_ NAME fest.

</dd> <dt>

*fCredentialUse* \[ In\]
</dt> <dd>

Ein Flag, das angibt, wie diese Anmeldeinformationen verwendet werden. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                               | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <dt>**SECPKG \_ CRED \_ INBOUND**</dt> </dl>    | Überprüfen Sie die Anmeldeinformationen eines eingehenden Servers. Eingehende Anmeldeinformationen können mithilfe einer Authentifizierungsstelle überprüft werden, wenn [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) oder [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) aufgerufen wird. Wenn eine solche Autorität nicht verfügbar ist, schlägt die Funktion fehl und gibt SEC \_ E \_ NO \_ AUTHENTICATING AUTHORITY \_ zurück. Die Überprüfung ist paketspezifisch.<br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <dt>**SECPKG \_ CRED \_ OUTBOUND**</dt> </dl> | Gestatten Sie einem lokalen Client, ein ausgehendes Token vorzubereiten.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*pvLogonID* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf einen [*lokal eindeutigen Bezeichner*](../secgloss/l-gly.md) (LUID), der den Benutzer identifiziert. Dieser Parameter wird für Dateisystemprozesse wie Netzwerkumleitungen bereitgestellt. Dieser Parameter kann **NULL** sein.

Bei Verwendung des Schannel-SSP wird dieser Parameter nicht verwendet und sollte auf **NULL** festgelegt werden.

</dd> <dt>

*pAuthData* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf paketspezifische Daten. Dieser Parameter kann **NULL** sein, was angibt, dass die Standardanmeldeinformationen für dieses [*Sicherheitspaket*](../secgloss/s-gly.md) verwendet werden müssen. Um bereitgestellte Anmeldeinformationen zu verwenden, übergeben Sie eine [**SEC \_ WINNT-AUTH \_ \_ IDENTITY-Struktur,**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) die diese Anmeldeinformationen in diesem Parameter enthält. Die RPC-Laufzeit übergibt alles, was in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo)bereitgestellt wurde.

Wenn Sie den Schannel-SSP verwenden, geben Sie eine [**SCH_CREDENTIALS**](/windows/win32/api/schannel/ns-schannel-sch_credentials) Struktur an, die das zu verwendende Protokoll und die Einstellungen für verschiedene anpassbare Kanalfeatures angibt.

</dd> <dt>

*pGetKeyFn* \[ in, optional\]
</dt> <dd>

Dieser Parameter wird nicht verwendet und sollte auf **NULL** festgelegt werden.

</dd> <dt>

*pvGetKeyArgument* \[ in, optional\]
</dt> <dd>

Dieser Parameter wird nicht verwendet und sollte auf **NULL** festgelegt werden.

</dd> <dt>

*phCredential* \[ out\]
</dt> <dd>

Ein Zeiger auf eine [CredHandle-Struktur](sspi-handles.md) zum Empfangen des Anmeldeinformationshandles.

</dd> <dt>

*ptsExpiry* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**TimeStamp-Struktur,**](timestamp.md) die den Zeitpunkt empfängt, zu dem die zurückgegebenen Anmeldeinformationen ablaufen. Der in dieser **TimeStamp-Struktur** zurückgegebene Wert hängt von der [*eingeschränkten Delegierung*](../secgloss/s-gly.md)ab. Das [*Sicherheitspaket*](../secgloss/s-gly.md) muss diesen Wert in Ortszeit zurückgeben.

Bei Verwendung des Schannel-SSP ist dieser Parameter optional. Wenn die für die Authentifizierung zu verwendenden Anmeldeinformationen ein Zertifikat sind, erhält dieser Parameter die Ablaufzeit für dieses Zertifikat. Wenn kein Zertifikat angegeben wurde, wird ein maximaler Zeitwert zurückgegeben.

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

Die **AcquireCredentialsHandle (Schannel)-Funktion** gibt ein Handle für die Anmeldeinformationen eines Prinzipals zurück, z. B. eines Benutzers oder Clients, wie von einer bestimmten [*eingeschränkten Delegierung*](../secgloss/s-gly.md)verwendet. Dies kann das Handle für bereits vorhandene Anmeldeinformationen sein, oder die Funktion kann einen neuen Satz von Anmeldeinformationen erstellen und zurückgeben. Dieses Handle kann in nachfolgenden Aufrufen der Funktionen [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) und [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) verwendet werden.

Im Allgemeinen lässt **AcquireCredentialsHandle (Schannel)** nicht zu, dass ein Prozess ein Handle für die Anmeldeinformationen anderer Benutzer erhält, die auf demselben Computer angemeldet sind. Ein Aufrufer mit SE \_ TCB \_ [*NAME-Berechtigung*](../secgloss/s-gly.md) hat jedoch die Möglichkeit, den [*Anmeldebezeichner*](../secgloss/l-gly.md) (LUID) eines vorhandenen Anmeldesitzungstokens anzugeben, um ein Handle für die Anmeldeinformationen dieser Sitzung abzurufen. In der Regel wird dies von Kernelmodusmodulen verwendet, die im Namen eines angemeldeten Benutzers agieren müssen.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md)
</dt> <dt>

[**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

[**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md)
</dt> <dt>

[**SCH_CREDENTIALS**](/windows/win32/api/schannel/ns-schannel-sch_credentials)
</dt> <dt>

[**SSPI-Funktionen**](authentication-functions.md#sspi-functions)
</dt> <dt>
 

 
