---
description: Ermöglicht einer Transportanwendung das Abfragen des CredSSP-Sicherheitspakets (Credential Security Support Provider) nach bestimmten Attributen eines Sicherheitskontexts.
ms.assetid: 4956c4ab-b71e-4960-b750-f3a79b87baac
title: QueryContextAttributes (CredSSP)-Funktion (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: b8ff421a2173f2ce2c5521e0706b53c3f6c326038179345d139acd0a157c7d61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920229"
---
# <a name="querycontextattributes-credssp-function"></a>QueryContextAttributes(CredSSP)-Funktion

Mit **der Funktion QueryContextAttributes (CredSSP)** kann eine Transportanwendung das CredSSP-Sicherheitspaket (Credential Security Support Provider) nach bestimmten Attributen eines Sicherheitskontexts abfragen. [](../secgloss/a-gly.md#_security_attribute_gly)

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

Ein Handle für den sicherheitskontext, der abgefragt werden soll.

</dd> <dt>

*ulAttribute* \[ In\]
</dt> <dd>

Das Attribut des Kontexts, der zurückgegeben werden soll. Dieser Parameter kann einen der folgenden Werte annehmen. Sofern nicht anders angegeben, gelten die Attribute sowohl für den Client als auch für den Server.



| Wert                                                                                                                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_ATTR_C_ACCESS_TOKEN"></span><span id="secpkg_attr_c_access_token"></span><dl> <dt>**SECPKG \_ ATTR \_ C ACCESS TOKEN \_ \_ 0x80000012**</dt> <dt></dt> </dl>                                 | Der *pBuffer-Parameter* enthält einen Zeiger auf eine [**SecPkgContext \_ AccessToken-Struktur,**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_accesstoken) die das Zugriffstoken für den aktuellen Sicherheitskontext angibt.<br/> Dieses Attribut wird nur auf dem Server unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="SECPKG_ATTR_C_FULL_ACCESS_TOKEN"></span><span id="secpkg_attr_c_full_access_token"></span><dl> <dt>**SECPKG \_ ATTR \_ C FULL ACCESS TOKEN \_ \_ \_ 0x80000082**</dt> <dt></dt> </dl>                 | Der *pBuffer-Parameter* enthält einen Zeiger auf eine [**SecPkgContext \_ AccessToken-Struktur,**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_accesstoken) die das Zugriffstoken für den aktuellen Sicherheitskontext angibt.<br/> Dieses Attribut wird nur auf dem Server unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="SECPKG_ATTR_CERT_TRUST_STATUS"></span><span id="secpkg_attr_cert_trust_status"></span><dl> <dt>**SECPKG \_ ATTR \_ CERT \_ TRUST STATUS \_ 0X80000084**</dt> <dt></dt> </dl>                        | Der *pBuffer-Parameter* enthält einen Zeiger auf eine [**CERT \_ TRUST \_ STATUS-Struktur,**](/windows/win32/api/wincrypt/ns-wincrypt-cert_trust_status) die Vertrauensinformationen zum Zertifikat angibt.<br/> Dieses Attribut wird nur auf dem Client unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="SECPKG_ATTR_CREDS"></span><span id="secpkg_attr_creds"></span><dl> <dt>**SECPKG \_ ATTR \_ CREDS**</dt> <dt>0x80000080</dt> </dl>                                                              | Der *pBuffer-Parameter* enthält einen Zeiger auf eine [**SecPkgContext \_ ClientCreds-Struktur,**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds) die Clientanmeldeinformationen angibt.<br/> Die Clientanmeldeinformationen können entweder Benutzername und Kennwort oder Benutzername und Smartcard-PIN sein.<br/> Dieses Attribut wird nur auf dem Server unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SECPKG_ATTR_CREDS_2"></span><span id="secpkg_attr_creds_2"></span><dl> <dt>**SECPKG \_ ATTR \_ CREDS \_ 2**</dt> <dt>0x80000086</dt> </dl>                                                       | Der *pBuffer-Parameter* enthält einen Zeiger auf eine [**SecPkgContext \_ ClientCreds-Struktur,**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds) die Clientanmeldeinformationen angibt. <br/> Wenn die Client-Anmeldeinformationen Benutzername und Kennwort sind, ist der Puffer eine gepackte [**KERB \_ INTERACTIVE \_ LOGON-Struktur.**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_interactive_logon)<br/> Wenn die Client-Anmeldeinformationen Benutzername und Smartcard-PIN sind, ist der Puffer eine gepackte [**KERB \_ CERTIFICATE \_ LOGON-Struktur.**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_certificate_logon)<br/> Wenn es sich bei den Client-Anmeldeinformationen um Anmeldeinformationen für die Onlineidentität handelt, handelt es sich bei dem Puffer um eine gemarshallte [**SEC \_ WINNT \_ AUTH \_ IDENTITY \_ EX2-Struktur.**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2)<br/> Dieses Attribut wird nur auf dem CredSSP-Server unterstützt.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003** und Windows XP: Dieser Wert wird nicht unterstützt.<br/> |
| <span id="SECPKG_ATTR_NEGOTIATION_PACKAGE"></span><span id="secpkg_attr_negotiation_package"></span><dl> <dt>**SECPKG \_ ATTR \_ NEGOTIATION \_ PACKAGE**</dt> <dt>0x80000081</dt> </dl>                   | Der *pBuffer-Parameter* enthält einen Zeiger auf eine [**SecPkgContext \_ PackageInfo-Struktur,**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) die den Namen des Authentifizierungspakets angibt, das vom [Microsoft Negotiate-Anbieter ausgehandelt](microsoft-negotiate.md) wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_ATTR_PACKAGE_INFO"></span><span id="secpkg_attr_package_info"></span><dl> <dt>**SECPKG \_ \_ \_ ATTR-PAKETINFORMATIONEN**</dt> <dt>10</dt> </dl>                                                | Der *pBuffer-Parameter* enthält einen Zeiger auf eine [**SecPkgContext \_ PackageInfo-Struktur.**](/windows/win32/api/sspi/ns-sspi-secpkginfoa)<br/> Gibt Informationen zum SSP zurück, der verwendet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_SERVER_AUTH_FLAGS"></span><span id="secpkg_attr_server_auth_flags"></span><dl> <dt>**SECPKG \_ \_ \_ \_ ATTR-SERVERAUTHENTIFIZIERUNGSFLAGS**</dt> <dt>0x80000083</dt> </dl>                        | Der *pBuffer-Parameter* enthält einen Zeiger auf eine [**SecPkgContext-Flags-Struktur, \_**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_flags) die Informationen zu den Flags im aktuellen Sicherheitskontext angibt.<br/> Dieses Attribut wird nur auf dem Client unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SECPKG_ATTR_SIZES"></span><span id="secpkg_attr_sizes"></span><dl> <dt>**SECPKG \_ \_ATTR-GRÖßEN**</dt> <dt>0x0</dt> </dl>                                                                     | Der *pBuffer-Parameter* enthält einen Zeiger auf eine [**SecPkgContext \_ Sizes-Struktur.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes)<br/> Fragt die Größe der Strukturen ab, die in den Nachrichtenfunktionen und dem Authentifizierungsaustausch verwendet werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="SECPKG_ATTR_SUBJECT_SECURITY_ATTRIBUTES"></span><span id="secpkg_attr_subject_security_attributes"></span><dl> <dt>**SECPKG \_ ATTR \_ SUBJECT \_ SECURITY \_ ATTRIBUTES**</dt> <dt>124</dt> </dl> | Der *pBuffer-Parameter* enthält einen Zeiger auf eine [**SecPkgContext \_ SubjectAttributes-Struktur.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_subjectattributes)<br/> Dieser Wert gibt Informationen zu den Sicherheitsattributen für die Verbindung zurück.<br/> Dieser Wert wird nur auf dem CredSSP-Server unterstützt.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

*pBuffer* \[ out\]
</dt> <dd>

Ein Zeiger auf eine -Struktur, die die Attribute empfängt. Der Strukturtyp hängt vom Wert des *ulAttribute-Parameters* ab.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, wird SEC \_ E \_ OK zurückgegeben.

Wenn die Funktion fehlschlägt, kann sie die folgenden Fehlercodes zurückgeben.



| Rückgabecode/-wert                                                                                                                                                            | BESCHREIBUNG                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ INVALID \_ HANDLE**</dt> <dt>0x80100003</dt> </dl>       | Fehler bei der Funktion. Der *phContext-Parameter* gibt ein Handle für einen unvollständigen Kontext an.<br/> |
| <dl> <dt>**SEC \_ E \_ NICHT \_ UNTERSTÜTZTE**</dt> <dt>0X80090302</dt> </dl> | Fehler bei der Funktion. Der Wert des *ulAttribute-Parameters* ist ungültig.<br/>                 |



 

## <a name="remarks"></a>Hinweise

Die Struktur, auf die der *pBuffer-Parameter* zeigt, variiert je nach abgefragten Attribut.

Während der Aufrufer die *pBuffer-Struktur* selbst zuordnen muss, weist der SSP jeglichen Arbeitsspeicher zu, der für Member variabler Größe der *pBuffer-Struktur erforderlich* ist. Der vom SSP zugeordnete Arbeitsspeicher muss durch Aufrufen der [**FreeContextBuffer-Funktion freigegeben**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                   |
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

[**SecPkgContext \_ ClientCreds**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds)
</dt> <dt>

[**\_SecPkgContext-Größen**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes)
</dt> </dl>

 

 
