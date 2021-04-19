---
description: Ruft ein Handle für bereits vorhandene Anmelde Informationen eines Sicherheits Prinzipals ab, der Kerberos verwendet.
ms.assetid: 2612bbe9-856b-4a81-bffb-6c761035883d
title: AcquireCredentialsHandle (Kerberos)-Funktion (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 05a4dd885712e89b812896684f73d60df610e41d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373230"
---
# <a name="acquirecredentialshandle-kerberos-function"></a>AcquireCredentialsHandle (Kerberos)-Funktion

Die Funktion **AcquireCredentialsHandle (Kerberos)** Ruft ein Handle für bereits vorhandene Anmelde Informationen eines [*Sicherheits Prinzipals*](../secgloss/s-gly.md)ab. Dieses Handle ist für die Funktionen [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) und [**akzeptsecuritycontext (Kerberos)**](acceptsecuritycontext--kerberos.md) erforderlich. Hierbei kann es sich um bereits vorhandene *Anmelde* Informationen handeln, die über eine System Anmeldung eingerichtet werden, die hier nicht beschrieben wird, oder der Aufrufer kann Alternative Anmelde Informationen bereitstellen.

> [!Note]  
> Dabei handelt es sich nicht um eine "beim Netzwerk anmelden", und es ist nicht beabsichtigt, Anmelde Informationen zu sammeln.

 

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

*pszprincipal* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Prinzipals angibt, auf dessen Anmelde Informationen das Handle verweist.

> [!Note]  
> Wenn der Prozess, der das Handle anfordert, keinen Zugriff auf die Anmelde Informationen hat, gibt die Funktion einen Fehler zurück. Eine NULL-Zeichenfolge gibt an, dass der Prozess ein Handle für die Anmelde Informationen des Benutzers erfordert, in dessen [*Sicherheitskontext*](../secgloss/s-gly.md) er ausgeführt wird.

 

</dd> <dt>

*pszpackage* \[ in\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des [*Sicherheitspakets*](../secgloss/s-gly.md) angibt, mit dem diese Anmelde Informationen verwendet werden. Dies ist ein [*Sicherheitspaket*](../secgloss/s-gly.md) Name, der im **Name** -Member einer [**secpkginfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) -Struktur zurückgegeben wird, die von der [**enumeratesecuritypackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) -Funktion zurückgegeben wird. Nachdem ein Kontext eingerichtet wurde, kann [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) aufgerufen werden, wobei *ulattribute* auf secpkg \_ attr Package Info festgelegt ist, \_ \_ um Informationen zum verwendeten [*Sicherheitspaket*](../secgloss/s-gly.md) zurückzugeben.

</dd> <dt>

*"f"* \[ in\]
</dt> <dd>

Ein Flag, das angibt, wie diese Anmelde Informationen verwendet werden. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                               | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_BOTH"></span><span id="secpkg_cred_both"></span><dl> <dt>**"secpkg" \_ -Funktion \_**</dt> </dl>             | Überprüfen Sie eingehende Anmelde Informationen, oder verwenden Sie lokale Anmelde Informationen, um ein Ausgeh Endes Token vorzubereiten. Dieses Flag aktiviert beide anderen Flags.<br/>                                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <dt>**secpkg-in \_ \_ eingehender Richtung**</dt> </dl>    | Überprüfen Sie die Anmelde Informationen eines eingehenden Servers. Eingehende Anmelde Informationen können mithilfe einer authentifizier enden Zertifizierungsstelle überprüft werden, wenn [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) oder [**Accept-SecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) aufgerufen wird. Wenn eine solche Autorität nicht verfügbar ist, schlägt die Funktion fehl und gibt SEK \_ \_ . E keine \_ authentifizier Ende Zertifizierungs \_ Stelle zurück. Die Validierung ist Paket spezifisch.<br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <dt>**Outbound für secpkg-Datenverkehr \_ \_**</dt> </dl> | Ermöglicht die Vorbereitung eines ausgehenden Tokens durch lokale Client Anmelde Informationen.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*pvlogonid* \[ in\]
</dt> <dd>

Ein Zeiger auf einen [*lokal eindeutigen Bezeichner*](../secgloss/l-gly.md) (LUID), der den Benutzer identifiziert. Dieser Parameter wird für Dateisystem Prozesse, z. b. netzwerkredirectors, bereitgestellt. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*pauthdata* \[ in\]
</dt> <dd>

Ein Zeiger auf Paket spezifische Daten. Dieser Parameter kann **null** sein, was darauf hinweist, dass die Standard Anmelde Informationen für das [*Sicherheitspaket*](../secgloss/s-gly.md) verwendet werden müssen. Um die angegebenen Anmelde Informationen zu verwenden, übergeben Sie eine [**sec- \_ Winnt-Authentifizierungs \_ \_ Identitäts**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) Struktur, die diese Anmelde Informationen enthält, in diesem Parameter. Die RPC-Laufzeit übergibt alle in [**rpcbindingsetauthinfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo)bereitgestellten.

</dd> <dt>

*pgetkeyfn* \[ in\]
</dt> <dd>

Dieser Parameter wird nicht verwendet und sollte auf **null** festgelegt werden.

</dd> <dt>

*pvgetkeyargument* \[ in\]
</dt> <dd>

Dieser Parameter wird nicht verwendet und sollte auf **null** festgelegt werden.

</dd> <dt>

*phcredential* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine " [kredhandle](sspi-handles.md) "-Struktur, die das Handle für die Anmelde Informationen empfängt.

</dd> <dt>

*ptsexpiry* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine [**Zeitstempel**](timestamp.md) Struktur, die die Uhrzeit empfängt, zu der die zurückgegebenen Anmelde Informationen ablaufen. Der in dieser **Zeitstempel** Struktur zurückgegebene Wert hängt von der [*eingeschränkten Delegierung*](../secgloss/s-gly.md)ab. Das [*Sicherheitspaket*](../secgloss/s-gly.md) muss diesen Wert in der Ortszeit zurückgeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion sec \_ E \_ OK zurück.

Wenn die Funktion fehlschlägt, wird einer der folgenden Fehlercodes zurückgegeben.



| Rückgabecode                                                                                                 | Beschreibung                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEK \_ b \_ nicht genügend Arbeits \_ Speicher**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abzuschließen.<br/>                                                                  |
| <dl> <dt>**Sek. \_ E ( \_ interner \_ Fehler)**</dt> </dl>      | Es ist ein Fehler aufgetreten, der keinem SSPI-Fehlercode zugeordnet wurde.<br/>                                                                               |
| <dl> <dt>**s \_ E \_ keine \_ Anmelde Informationen**</dt> </dl>      | In der [*eingeschränkten Delegierung*](../secgloss/s-gly.md)sind keine Anmelde Informationen verfügbar.<br/> |
| <dl> <dt>**Sek. \_ E \_ nicht \_ Besitzer**</dt> </dl>           | Der Aufrufer der Funktion verfügt nicht über die erforderlichen Anmelde Informationen.<br/>                                                                     |
| <dl> <dt>**Sek. \_ E \_ secpkg \_ nicht \_ gefunden**</dt> </dl>   | Das angeforderte [*Sicherheitspaket*](../secgloss/s-gly.md) ist nicht vorhanden.<br/>                                                                                          |
| <dl> <dt>**SEK \_ . \_ unbekannte \_ Anmelde Informationen**</dt> </dl> | Die für das Paket angegebenen Anmelde Informationen wurden nicht erkannt.<br/>                                                                            |



 

## <a name="remarks"></a>Bemerkungen

Die Funktion **AcquireCredentialsHandle (Kerberos)** gibt ein Handle für die Anmelde Informationen eines Prinzipals (z. b. einen Benutzer oder Client) zurück, der von einer bestimmten [*eingeschränkten Delegierung*](../secgloss/s-gly.md)verwendet wird. Dies kann das Handle für bereits vorhandene Anmelde Informationen sein, oder die Funktion kann einen neuen Satz von Anmelde Informationen erstellen und zurückgeben. Dieses Handle kann in nachfolgenden Aufrufen der Funktionen " [**Accept tsecuritycontext" (Kerberos)**](acceptsecuritycontext--kerberos.md) und " [**InitializeSecurityContext" (Kerberos)**](initializesecuritycontext--kerberos.md) verwendet werden.

Im Allgemeinen gestattet **AcquireCredentialsHandle (Kerberos)** einem Prozess nicht das Abrufen eines Handles für die Anmelde Informationen anderer Benutzer, die am gleichen Computer angemeldet sind. Allerdings hat ein Aufrufer mit der Berechtigung "SE \_ TCB \_ Name" die Option, den [*Anmelde Bezeichner*](../secgloss/l-gly.md) (LUID) eines beliebigen vorhandenen Anmelde Sitzungs Tokens anzugeben, um ein Handle für die Anmelde Informationen dieser Sitzung zu erhalten. [](../secgloss/s-gly.md) Diese wird in der Regel von Kernelmodusmodulen verwendet, die im Auftrag eines angemeldeten Benutzers agieren müssen.

Ein Paket kann die Funktion in *pgetkeyfn* aufrufen, die vom RPC-Lauf Zeit Transport bereitgestellt wird. Wenn der Transport die Rückruffunktion zum Abrufen von Anmelde Informationen nicht unterstützt, muss dieser Parameter **null** sein.

Bei kernelmodusaufrufern müssen die folgenden Unterschiede beachtet werden:

-   Die beiden Zeichen folgen Parameter müssen [*Unicode*](../secgloss/u-gly.md) -Zeichen folgen sein.
-   Die Puffer Werte müssen im virtuellen Arbeitsspeicher des Prozesses zugeordnet werden, nicht aus dem Pool.

Wenn Sie die zurückgegebenen Anmelde Informationen nicht mehr verwenden, geben Sie den von den Anmelde Informationen genutzten Arbeitsspeicher frei, indem Sie die [**freecredentialshandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>SSPI. h (Include Security. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Unicode- und ANSI-Name<br/>   | **Acquirecredentialshandlew** (Unicode) und **AcquireCredentialsHandleA** (ANSI)<br/>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[SSPI-Funktionen](authentication-functions.md#sspi-functions)
</dt> <dt>

[**Akzeptsecuritycontext (Kerberos)**](acceptsecuritycontext--kerberos.md)
</dt> <dt>

[**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md)
</dt> <dt>

[**Freecredentialshandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
