---
description: Ermöglicht einer Transportanwendung das Abfragen [](../secgloss/s-gly.md) des NTLM-Sicherheitspakets nach bestimmten Attributen eines [Sicherheitskontexts.](../secgloss/s-gly.md)
ms.assetid: cfa545e7-c5d9-4ffd-bbba-669d2bd3df2d
title: QueryContextAttributes (NTLM)-Funktion (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 6e392f492ddb4b8cc2878e58e60b1f0bdc84d3e65d8a06019586d204ca6a9ff6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920098"
---
# <a name="querycontextattributes-ntlm-function"></a>QueryContextAttributes-Funktion (NTLM)

Mit **der NTLM-Funktion (QueryContextAttributes)** kann eine Transportanwendung das NTLM-Sicherheitspaket nach bestimmten Attributen eines [Sicherheitskontexts abfragen.](../secgloss/s-gly.md) [](../secgloss/s-gly.md) [](../secgloss/a-gly.md#_security_attribute_gly)

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS SEC_ENTRY QueryContextAttributes(
  _In_  PCtxtHandle phContext,
  _In_  ULONG       ulAttribute,
  _Out_ PVOID       pBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*phContext* \[ In\]
</dt> <dd>

Ein Handle für den [sicherheitskontext,](../secgloss/s-gly.md) der abgefragt werden soll.

</dd> <dt>

*ulAttribute* \[ In\]
</dt> <dd>

Gibt das Attribut des Kontexts an, der zurückgegeben werden soll. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                                                                                          | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_ATTR_ACCESS_TOKEN"></span><span id="secpkg_attr_access_token"></span><dl> <dt>**SECPKG \_ \_ \_ ATTR-ZUGRIFFSTOKEN**</dt> <dt>18</dt> </dl>                                       | Der *pBuffer-Parameter* enthält einen Zeiger auf eine [**SecPkgContext \_ AccessToken-Struktur.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_accesstoken)<br/> Gibt ein Handle für das Zugriffstoken zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_AUTHORITY"></span><span id="secpkg_attr_authority"></span><dl> <dt>**SECPKG \_ ATTR \_ AUTHORITY**</dt> <dt>6</dt> </dl>                                                  | Der *pBuffer-Parameter* enthält einen Zeiger auf eine [**SecPkgContext \_ Authority-Struktur.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_authoritya)<br/> Fragt den Namen der Authentifizierungsstelle ab.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="SECPKG_ATTR_CLIENT_SPECIFIED_TARGET"></span><span id="secpkg_attr_client_specified_target"></span><dl> <dt>**SECPKG \_ VOM \_ ATTR-CLIENT \_ \_ ANGEGEBENES ZIEL**</dt> <dt>27</dt> </dl>     | Der *pBuffer-Parameter* enthält einen Zeiger auf eine [**SecPkgContext-ClientSpecifiedTarget-Struktur, \_**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_clientspecifiedtarget) die den Dienstprinzipalnamen (SERVICE Principal Name, SPN) des ursprünglichen Ziels darstellt, das vom Client bereitgestellt wird. <br/> Dieser Wert wird nur unterstützt, wenn Kanalbindungen verwendet werden.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SECPKG_ATTR_CREDS_2"></span><span id="secpkg_attr_creds_2"></span><dl> <dt>**SECPKG \_ ATTR \_ CREDS \_ 2**</dt> <dt>0x80000086</dt> </dl>                                              | Der *pBuffer-Parameter* enthält einen Zeiger auf eine [**SecPkgContext \_ ClientCreds-Struktur,**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds) die Clientanmeldeinformationen angibt. <br/> Wenn die Client-Anmeldeinformationen Benutzername und Kennwort sind, ist der Puffer eine gepackte [**KERB \_ INTERACTIVE \_ LOGON-Struktur.**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_interactive_logon)<br/> Wenn die Client-Anmeldeinformationen Benutzername und Smartcard-PIN sind, ist der Puffer eine gepackte [**KERB \_ CERTIFICATE \_ LOGON-Struktur.**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_certificate_logon)<br/> Wenn es sich bei den Client-Anmeldeinformationen um Anmeldeinformationen für die Onlineidentität handelt, handelt es sich bei dem Puffer um eine gemarshallte [**SEC \_ WINNT \_ AUTH \_ IDENTITY \_ EX2-Struktur.**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2)<br/> Dieses Attribut wird nur auf dem CredSSP-Server unterstützt.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003** und Windows XP: Dieser Wert wird nicht unterstützt.<br/> |
| <span id="SECPKG_ATTR_DCE_INFO"></span><span id="secpkg_attr_dce_info"></span><dl> <dt>**SECPKG \_ ATTR \_ DCE \_ INFO**</dt> <dt>3</dt> </dl>                                                    | Der *pBuffer-Parameter* enthält einen Zeiger auf eine [**SecPkgContext \_ DceInfo-Struktur.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_dceinfo)<br/> Abfragen von Autorisierungsdaten, die von DCE-Diensten verwendet werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="SECPKG_ATTR_FLAGS"></span><span id="secpkg_attr_flags"></span><dl> <dt>**SECPKG \_ \_ATTR-FLAGS**</dt> <dt>14</dt> </dl>                                                             | Der *pBuffer-Parameter* enthält einen Zeiger auf eine [**SecPkgContext-Flags-Struktur. \_**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_flags)<br/> Gibt Informationen zu den ausgehandelten Kontextflags zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="SECPKG_ATTR_KEY_INFO"></span><span id="secpkg_attr_key_info"></span><dl> <dt>**SECPKG \_ ATTR \_ KEY \_ INFO**</dt> <dt>5</dt> </dl>                                                    | Der *pBuffer-Parameter* enthält einen Zeiger auf eine [**SecPkgContext \_ KeyInfo-Struktur.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_keyinfoa)<br/> Fragt Informationen zu den Schlüsseln ab, die in einem [Sicherheitskontext verwendet werden.](../secgloss/s-gly.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SECPKG_ATTR_LAST_CLIENT_TOKEN_STATUS"></span><span id="secpkg_attr_last_client_token_status"></span><dl> <dt>**SECPKG \_ ATTR \_ LAST CLIENT TOKEN \_ \_ \_ STATUS**</dt> <dt>30</dt> </dl> | Der *pBuffer-Parameter* enthält einen Zeiger auf eine [**SecPkgContext \_ LastClientTokenStatus-Struktur,**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_lastclienttokenstatus) die angibt, ob das Token aus dem letzten Aufruf der [**InitializeSecurityContext-Funktion**](initializesecuritycontext--general.md) das letzte Token vom Client ist.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="SECPKG_ATTR_LIFESPAN"></span><span id="secpkg_attr_lifespan"></span><dl> <dt>**SECPKG \_ ATTR \_ LIFESPAN**</dt> <dt>2</dt> </dl>                                                     | Der *pBuffer-Parameter* enthält einen Zeiger auf eine [**SecPkgContext \_ Lifespan-Struktur.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_lifespan)<br/> Fragt die Lebensdauer des Kontexts ab.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="SECPKG_ATTR_LOCAL_CRED"></span><span id="secpkg_attr_local_cred"></span><dl> <dt>**SECPKG \_ ATTR \_ LOCAL \_ CRED**</dt> </dl>                                                                                                     | Der *pBuffer-Parameter* enthält einen Zeiger auf eine **SecPkgContext \_ LocalCredentialInfo-Struktur.** (Veraltet)<br/> Ersetzt durch SECPKG \_ ATTR \_ LOCAL \_ CERT \_ CONTEXT.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="SECPKG_ATTR_NAMES"></span><span id="secpkg_attr_names"></span><dl> <dt>**SECPKG \_ \_ATTR-NAMEN**</dt> <dt>1</dt> </dl>                                                              | Der *pBuffer-Parameter* enthält einen Zeiger auf eine [**SecPkgContext \_ Names-Struktur.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_namesa)<br/> Fragt den Namen ab, der dem Kontext zugeordnet ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="SECPKG_ATTR_NATIVE_NAMES"></span><span id="secpkg_attr_native_names"></span><dl> <dt>**SECPKG \_ ATTR \_ NATIVE \_ NAMES**</dt> <dt>13</dt> </dl>                                       | Der *pBuffer-Parameter* enthält einen Zeiger auf eine [**SecPkgContext \_ NativeNames-Struktur.**](https://docs.microsoft.com/windows/win32/api/sspi/ns-sspi-_secpkgcontext_nativenamesa)<br/> Gibt den Prinzipalnamen (CNAME) aus dem ausgehenden Ticket zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="SECPKG_ATTR_NEGOTIATION_INFO"></span><span id="secpkg_attr_negotiation_info"></span><dl> <dt>**SECPKG \_ \_ \_ ATTR-AUSHANDLUNGSINFORMATIONEN**</dt> <dt>12</dt> </dl>                           | Der *pBuffer-Parameter* enthält einen Zeiger auf eine [**SecPkgContext \_ NegotiationInfo-Struktur.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_negotiationinfoa)<br/> Gibt Informationen über das [*Sicherheitspaket zurück,*](../secgloss/s-gly.md) das mit dem Aushandlungsprozess verwendet werden soll, und den aktuellen Status der Aushandlung für die Verwendung dieses Pakets.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_ATTR_PACKAGE_INFO"></span><span id="secpkg_attr_package_info"></span><dl> <dt>**SECPKG \_ \_ \_ ATTR-PAKETINFORMATIONEN**</dt> <dt>10</dt> </dl>                                       | Der *pBuffer-Parameter* enthält einen Zeiger auf eine [**SecPkgContext \_ PackageInfo-Struktur.**](/windows/win32/api/sspi/ns-sspi-secpkginfoa)<br/> Gibt Informationen zum SSP zurück, der verwendet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_PASSWORD_EXPIRY"></span><span id="secpkg_attr_password_expiry"></span><dl> <dt>**SECPKG \_ ATTR \_ PASSWORD \_ EXPIRY**</dt> <dt>8</dt> </dl>                               | Der *pBuffer-Parameter* enthält einen Zeiger auf eine [**SecPkgContext \_ PasswordExpiry-Struktur.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_passwordexpiry)<br/> Gibt Informationen zum Kennwortablauf zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SECPKG_ATTR_ROOT_STORE"></span><span id="secpkg_attr_root_store"></span><dl> <dt>**SECPKG \_ ATTR \_ ROOT \_ STORE**</dt> <dt>0x55</dt> </dl>                                           | Der *pBuffer-Parameter* enthält einen Zeiger auf einen **HCERTCONTEXT.** <br/> Sucht einen Zertifikatkontext, der ein vom Stammspeicher bereitgestelltes Zertifikat enthält.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="SECPKG_ATTR_SESSION_KEY"></span><span id="secpkg_attr_session_key"></span><dl> <dt>**SECPKG \_ \_ \_ ATTR-SITZUNGSSCHLÜSSEL**</dt> <dt>9</dt> </dl>                                           | Der *pBuffer-Parameter* enthält einen Zeiger auf eine [**SecPkgContext \_ SessionKey-Struktur.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sessionkey)<br/> Gibt Informationen zu den [*Sitzungsschlüsseln*](../secgloss/s-gly.md)zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SECPKG_ATTR_SIZES"></span><span id="secpkg_attr_sizes"></span><dl> <dt>**SECPKG \_ \_ATTR-GRÖßEN**</dt> <dt>0</dt> </dl>                                                              | Der *pBuffer-Parameter* enthält einen Zeiger auf eine [**SecPkgContext \_ Sizes-Struktur.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes)<br/> Fragt die Größen der Strukturen ab, die in den Nachrichtenfunktionen verwendet werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="SECPKG_ATTR_TARGET_INFORMATION"></span><span id="secpkg_attr_target_information"></span><dl> <dt>**SECPKG \_ \_ \_ ATTR-ZIELINFORMATIONEN**</dt> <dt>17</dt> </dl>                     | Der *pBuffer-Parameter* enthält einen Zeiger auf eine [**SecPkgContext \_ TargetInformation-Struktur.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_targetinformation)<br/> Gibt Informationen zum Namen des Remoteservers zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

*pBuffer* \[ out\]
</dt> <dd>

Ein Zeiger auf eine -Struktur, die die Attribute empfängt. Der Typ der Struktur, auf die verwiesen wird, hängt vom Im *ulAttribute-Parameter angegebenen Wert* ab.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert SEC \_ E \_ OK.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null).

## <a name="remarks"></a>Hinweise

Die Struktur, auf die der *pBuffer-Parameter* zeigt, variiert je nach abgefragten Attribut. Der Aufrufer muss die *pBuffer-Struktur* selbst zuordnen, aber der SSP weist jeglichen Arbeitsspeicher zu, der für Member variabler Größe der *pBuffer-Struktur erforderlich* ist. Der vom SSP zugeordnete Arbeitsspeicher kann durch Aufrufen der [**FreeContextBuffer-Funktion freigegeben**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) werden.

Nachdem der SECPKG \_ ATTR \_ REMOTE \_ CERT CONTEXT- oder \_ SECPKG ATTR LOCAL CERT CONTEXT-Wert gelesen wurde, wird das \_ \_ \_ \_ **hCertStore-Mitglied** auf ein Handle für einen Zertifikatspeicher festgelegt, der die Zwischenzertifikate enthält(sofern verfügbar). Außerdem ist die Anwendung für den Aufruf von [**CertFreeCertificateContext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) verantwortlich, um den vom Zertifikatkontext verwendeten Arbeitsspeicher frei zu geben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Sspi.h (einschließlich Security.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Unicode- und ANSI-Name<br/>   | **QueryContextAttributesW** (Unicode) und **QueryContextAttributesA** (ANSI)<br/>                |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[SSPI-Funktionen](authentication-functions.md#sspi-functions)
</dt> <dt>

[**\_CERT-KONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)
</dt> <dt>

[**SecPkgContext-Autorität \_**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_authoritya)
</dt> <dt>

[**SecPkgContext \_ ConnectionInfo**](/windows/win32/api/schannel/ns-schannel-secpkgcontext_connectioninfo)
</dt> <dt>

[**SecPkgContext \_ DceInfo**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_dceinfo)
</dt> <dt>

[**SecPkgContext \_ IssuerListInfoEx**](/windows/win32/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex)
</dt> <dt>

[**SecPkgContext \_ KeyInfo**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_keyinfoa)
</dt> <dt>

[**\_SecPkgContext-Lebensdauer**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_lifespan)
</dt> <dt>

[**SecPkgContext-Namen \_**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_namesa)
</dt> <dt>

[**\_SecPkgContext-Größen**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes)
</dt> <dt>

[**SecPkgContext \_ StreamSizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes)
</dt> </dl>

 

 
