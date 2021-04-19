---
description: Ruft ein Handle für bereits vorhandene Anmelde Informationen eines Sicherheits Prinzipals ab, der "aushandeln" verwendet.
ms.assetid: ff372163-c73b-41bb-afcb-7d5de7720967
title: AcquireCredentialsHandle (Aushandlungs)-Funktion (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 80ab4b67866b60831dadb7d8eb9bf9f632c0661c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364142"
---
# <a name="acquirecredentialshandle-negotiate-function"></a>AcquireCredentialsHandle (Aushandlungs)-Funktion

Die **AcquireCredentialsHandle (Aushandlungs)** -Funktion Ruft ein Handle für bereits vorhandene Anmelde Informationen eines [*Sicherheits Prinzipals*](../secgloss/s-gly.md)ab. Dieses Handle ist für die Funktionen [**InitializeSecurityContext (aushandeln)**](initializesecuritycontext--negotiate.md) und [**akzeptsecuritycontext (aushandeln)**](acceptsecuritycontext--negotiate.md) erforderlich. Hierbei kann es sich um bereits vorhandene *Anmelde* Informationen handeln, die über eine System Anmeldung eingerichtet werden, die hier nicht beschrieben wird, oder der Aufrufer kann Alternative Anmelde Informationen bereitstellen.

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

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des [*Sicherheitspakets*](../secgloss/s-gly.md) angibt, mit dem diese Anmelde Informationen verwendet werden. Dies ist ein [*Sicherheitspaket*](../secgloss/s-gly.md) Name, der im **Name** -Member einer [**secpkginfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) -Struktur zurückgegeben wird, die von der [**enumeratesecuritypackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) -Funktion zurückgegeben wird. Nachdem ein Kontext eingerichtet wurde, kann [**QueryContextAttributes (aushandeln)**](querycontextattributes--negotiate.md) aufgerufen werden, wobei *ulattribute* auf secpkg \_ attr Package Info festgelegt wird, \_ \_ um Informationen zum verwendeten [*Sicherheitspaket*](../secgloss/s-gly.md) zurückzugeben.

Legen Sie diesen Parameter auf "aushandeln" fest, um diese Funktion mit dem Aushandlungs-SSP erfolgreich aufrufen zu können.

</dd> <dt>

*"f"* \[ in\]
</dt> <dd>

Ein Flag, das angibt, wie diese Anmelde Informationen verwendet werden. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                                                                                    | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_AUTOLOGON_RESTRICTED"></span><span id="secpkg_cred_autologon_restricted"></span><dl> <dt>**Secpkg \_ \_ \_**</dt> Von der 00000010-Authentifizierung beschränkte <dt>0x</dt> </dl> | Die-Sicherheit verwendet keine Standard Anmelde Informationen oder Anmelde Informationen von [Credential Manager](credential-manager.md).<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                    |
| <span id="SECPKG_CRED_BOTH"></span><span id="secpkg_cred_both"></span><dl> <dt>**"secpkg" \_ -Funktion \_**</dt> </dl>                                                                                                                  | Überprüfen Sie eingehende Anmelde Informationen, oder verwenden Sie lokale Anmelde Informationen, um ein Ausgeh Endes Token vorzubereiten. Dieses Flag aktiviert beide anderen Flags.<br/>                                                                                                                                                                                                                                                                                                                                  |
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <dt>**secpkg-in \_ \_ eingehender Richtung**</dt> </dl>                                                                                                         | Überprüfen Sie die Anmelde Informationen eines eingehenden Servers. Eingehende Anmelde Informationen können mithilfe einer authentifizier enden Zertifizierungsstelle überprüft werden, wenn [**InitializeSecurityContext (aushandeln)**](initializesecuritycontext--negotiate.md) oder [**Accept tsecuritycontext (aushandeln)**](acceptsecuritycontext--negotiate.md) aufgerufen wird. Wenn eine solche Autorität nicht verfügbar ist, schlägt die Funktion fehl und gibt SEK \_ \_ . E keine \_ authentifizier Ende Zertifizierungs \_ Stelle zurück. Die Validierung ist Paket spezifisch.<br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <dt>**Outbound für secpkg-Datenverkehr \_ \_**</dt> </dl>                                                                                                      | Ermöglicht die Vorbereitung eines ausgehenden Tokens durch lokale Client Anmelde Informationen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="SECPKG_CRED_PROCESS_POLICY_ONLY"></span><span id="secpkg_cred_process_policy_only"></span><dl> <dt>**Secpkg \_ Nur für \_ die \_ Prozess \_ Richtlinie**</dt> " <dt>0x00000020</dt> " </dl>   | Die Funktion verarbeitet die Server Richtlinie und gibt **Sek. \_ E \_ keine \_ Anmelde** Informationen zurück. Dies deutet darauf hin, dass die Anwendung Anmelde Informationen anfordern sollte.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                             |



 

</dd> <dt>

*pvlogonid* \[ in\]
</dt> <dd>

Ein Zeiger auf einen [*lokal eindeutigen Bezeichner*](../secgloss/l-gly.md) (LUID), der den Benutzer identifiziert. Dieser Parameter wird für Dateisystem Prozesse, z. b. netzwerkredirectors, bereitgestellt. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*pauthdata* \[ in\]
</dt> <dd>

Ein Zeiger auf Paket spezifische Daten. Dieser Parameter kann **null** sein, was darauf hinweist, dass die Standard Anmelde Informationen für das [*Sicherheitspaket*](../secgloss/s-gly.md) verwendet werden müssen. Um die angegebenen Anmelde Informationen zu verwenden, übergeben Sie eine nicht transparente PSEC-Authentifizierungs Struktur, die von einem vorherigen [**aufrufsspipromptforanmelde**](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa) -Funktion zurückgegeben wurde. **\_ \_ \_ \_**

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Der Typ der nicht transparenten PSEC-Authentifizierung und die [**sspipromptfor-Anmelde**](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa) Informationen werden nicht unterstützt. **\_ \_ \_ \_** Wenn Sie die angegebenen Anmelde Informationen verwenden möchten, übergeben Sie einen Zeiger entweder auf eine [**sec- \_ Winnt-Authentifizierungs \_ \_ Identität**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) oder eine [**Sek. \_ Winnt Authentication \_ \_ \_ Ex**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) -Struktur, die diese Anmelde Informationen enthält.

Die RPC-Laufzeit übergibt alle in [**rpcbindingsetauthinfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo)bereitgestellten.

Wenn das Aushandlungs Paket verwendet wird, sind die maximalen Zeichen Längen für Benutzername, Kennwort und Domäne 256, 256 bzw. 15.

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

Die **AcquireCredentialsHandle (Aushandlungs)** -Funktion gibt ein Handle für die Anmelde Informationen eines Prinzipals (z. b. einen Benutzer oder Client) zurück, der von einer bestimmten [*eingeschränkten Delegierung*](../secgloss/s-gly.md)verwendet wird. Dies kann das Handle für bereits vorhandene Anmelde Informationen sein, oder die Funktion kann einen neuen Satz von Anmelde Informationen erstellen und zurückgeben. Dieses Handle kann in nachfolgenden Aufrufen der Funktionen [**Accept-SecurityContext (aushandeln)**](acceptsecuritycontext--negotiate.md) und [**InitializeSecurityContext (aushandeln)**](initializesecuritycontext--negotiate.md) verwendet werden.

Im Allgemeinen gestattet **AcquireCredentialsHandle (aushandeln)** einem Prozess nicht das Abrufen eines Handles für die Anmelde Informationen anderer Benutzer, die am gleichen Computer angemeldet sind. Allerdings hat ein Aufrufer mit der Berechtigung "SE \_ TCB \_ Name" die Option, den [*Anmelde Bezeichner*](../secgloss/l-gly.md) (LUID) eines beliebigen vorhandenen Anmelde Sitzungs Tokens anzugeben, um ein Handle für die Anmelde Informationen dieser Sitzung zu erhalten. [](../secgloss/s-gly.md) Diese wird in der Regel von Kernelmodusmodulen verwendet, die im Auftrag eines angemeldeten Benutzers agieren müssen.

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

[**Akzeptsecuritycontext (aushandeln)**](acceptsecuritycontext--negotiate.md)
</dt> <dt>

[**InitializeSecurityContext (aushandeln)**](initializesecuritycontext--negotiate.md)
</dt> <dt>

[**Freecredentialshandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
