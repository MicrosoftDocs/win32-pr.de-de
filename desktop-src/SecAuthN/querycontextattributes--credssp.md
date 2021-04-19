---
description: Ermöglicht es einer Transport Anwendung, das Sicherheitspaket für die Anmelde Informationen Security Support Provider (kredssp) für bestimmte Attribute eines Sicherheits Kontexts abzufragen.
ms.assetid: 4956c4ab-b71e-4960-b750-f3a79b87baac
title: QueryContextAttributes (CredSSP)-Funktion (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 191c3c8d3b2b5bd829aaf8eb45bacadbbd2bbade
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356226"
---
# <a name="querycontextattributes-credssp-function"></a>QueryContextAttributes (kredssp)-Funktion

Mithilfe der **QueryContextAttributes (kredssp)** -Funktion kann eine Transport Anwendung das Sicherheitspaket für Anmelde Informationen Security Support Provider (kredssp) für bestimmte [*Attribute*](../secgloss/a-gly.md#_security_attribute_gly) eines Sicherheits Kontexts Abfragen.

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

*phcontext* \[ in\]
</dt> <dd>

Ein Handle für den Sicherheitskontext, der abgefragt werden soll.

</dd> <dt>

*ulattribute* \[ in\]
</dt> <dd>

Das Attribut des Kontexts, der zurückgegeben werden soll. Dieser Parameter kann einen der folgenden Werte annehmen. Sofern nicht anders angegeben, gelten die Attribute sowohl für den Client als auch für den Server.



| Wert                                                                                                                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_ATTR_C_ACCESS_TOKEN"></span><span id="secpkg_attr_c_access_token"></span><dl> <dt>**Secpkg \_ Attr \_ C- \_ Zugriffs \_ Token**</dt> <dt>0x80000012</dt> </dl>                                 | Der *pbuffer* -Parameter enthält einen Zeiger auf eine [**secpkgcontext \_ accesstoken**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_accesstoken) -Struktur, die das Zugriffs Token für den aktuellen Sicherheitskontext angibt.<br/> Dieses Attribut wird nur auf dem Server unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="SECPKG_ATTR_C_FULL_ACCESS_TOKEN"></span><span id="secpkg_attr_c_full_access_token"></span><dl> <dt>**Secpkg \_ Attr \_ C \_ - \_ \_ Token für Vollzugriff**</dt> <dt>0x80000082</dt> </dl>                 | Der *pbuffer* -Parameter enthält einen Zeiger auf eine [**secpkgcontext \_ accesstoken**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_accesstoken) -Struktur, die das Zugriffs Token für den aktuellen Sicherheitskontext angibt.<br/> Dieses Attribut wird nur auf dem Server unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="SECPKG_ATTR_CERT_TRUST_STATUS"></span><span id="secpkg_attr_cert_trust_status"></span><dl> <dt>**Secpkg \_ Attr \_ CERT \_ Trust \_ Status**</dt> <dt>0x80000084</dt> </dl>                        | Der *pbuffer* -Parameter enthält einen Zeiger auf eine [**CERT \_ Trust- \_ Status**](/windows/win32/api/wincrypt/ns-wincrypt-cert_trust_status) Struktur, die Vertrauensstellungs Informationen über das Zertifikat angibt.<br/> Dieses Attribut wird nur auf dem Client unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="SECPKG_ATTR_CREDS"></span><span id="secpkg_attr_creds"></span><dl> <dt>**Secpkg \_ Attr \_**</dt> -Fehler <dt>0x80000080</dt> </dl>                                                              | Der *pbuffer* -Parameter enthält einen Zeiger auf eine [**secpkgcontext- \_ clientkreds**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds) -Struktur, die Client Anmelde Informationen angibt.<br/> Die Client Anmelde Informationen können entweder Benutzername und Kennwort oder Benutzername und Smartcard-PIN sein.<br/> Dieses Attribut wird nur auf dem Server unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SECPKG_ATTR_CREDS_2"></span><span id="secpkg_attr_creds_2"></span><dl> <dt>**Secpkg \_ Attr \_ \_**</dt> -Erstellungs-2 <dt>0x80000086</dt> </dl>                                                       | Der *pbuffer* -Parameter enthält einen Zeiger auf eine [**secpkgcontext- \_ clientkreds**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds) -Struktur, die Client Anmelde Informationen angibt. <br/> Wenn die Client Anmelde Informationen "Benutzername" und "Kennwort" sind, handelt es sich bei dem Puffer um [**eine gepackte \_ \_**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_interactive_logon) , gepackte<br/> Wenn es sich bei den Client [**\_ \_ Anmelde**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_certificate_logon) Informationen um den Benutzernamen und die Smartcard-PIN handelt, ist der Puffer eine gepackte Struktur für das KERB Zertifikat<br/> Handelt es sich bei den Client Anmelde Informationen um Online-Identitäts Anmelde Informationen, ist der Puffer eine gemarshallte [**Sek. \_ Winnt \_ auth \_ Identity \_ ex2**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) -Struktur.<br/> Dieses Attribut wird nur auf dem-Server mit dem-Server unterstützt.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.<br/> |
| <span id="SECPKG_ATTR_NEGOTIATION_PACKAGE"></span><span id="secpkg_attr_negotiation_package"></span><dl> <dt>**Secpkg \_ Attr \_ \_**</dt> -Aushandlungs Paket <dt>0x80000081</dt> </dl>                   | Der *pbuffer* -Parameter enthält einen Zeiger auf eine [**secpkgcontext \_ PackageInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) -Struktur, die den Namen des vom [Microsoft Aushandlungs](microsoft-negotiate.md) Anbieter ausgehandelten Authentifizierungs Pakets angibt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_ATTR_PACKAGE_INFO"></span><span id="secpkg_attr_package_info"></span><dl> <dt>**Secpkg \_ Attr- \_ Paket \_ Informationen**</dt> <dt>10</dt> </dl>                                                | Der *pbuffer* -Parameter enthält einen Zeiger auf eine [**secpkgcontext \_ PackageInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa)-Struktur.<br/> Gibt Informationen zum verwendeten SSP zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_SERVER_AUTH_FLAGS"></span><span id="secpkg_attr_server_auth_flags"></span><dl> <dt>**Secpkg \_ Attr \_ Server \_ auth \_ Flags**</dt> <dt>0x80000083</dt> </dl>                        | Der *pbuffer* -Parameter enthält einen Zeiger auf eine [**secpkgcontext- \_ Flags**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_flags) -Struktur, die Informationen zu den Flags im aktuellen Sicherheitskontext angibt.<br/> Dieses Attribut wird nur auf dem Client unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SECPKG_ATTR_SIZES"></span><span id="secpkg_attr_sizes"></span><dl> <dt>**Secpkg \_ Attr- \_ Größen**</dt> <dt>0x0</dt> </dl>                                                                     | Der *pbuffer* -Parameter enthält einen Zeiger auf eine [**secpkgcontext \_ sizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) -Struktur.<br/> Fragt die Größen der Strukturen ab, die in den Funktionen pro Nachricht und Authentifizierungs Austausch verwendet werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="SECPKG_ATTR_SUBJECT_SECURITY_ATTRIBUTES"></span><span id="secpkg_attr_subject_security_attributes"></span><dl> <dt>**Secpkg \_ Attr- \_ Themen \_ Sicherheits \_ Attribute**</dt> <dt>124</dt> </dl> | Der *pbuffer* -Parameter enthält einen Zeiger auf eine [**secpkgcontext-Struktur " \_ subjetattributes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_subjectattributes) ".<br/> Dieser Wert gibt Informationen zu den Sicherheits Attributen für die Verbindung zurück.<br/> Dieser Wert wird nur auf dem-Server unterstützt.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

*pbuffer* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine-Struktur, die die Attribute empfängt. Der Strukturtyp hängt vom Wert des *ulattribute* -Parameters ab.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird \_ SEK \_ . E OK zurückgegeben.

Wenn die Funktion fehlschlägt, können die folgenden Fehlercodes zurückgegeben werden.



| Rückgabecode/-wert                                                                                                                                                            | BESCHREIBUNG                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEK \_ . E \_ ungültiges \_ handle**</dt> <dt>0x80100003</dt> </dl>       | Die Funktion ist fehlgeschlagen. Der Parameter " *phcontext* " gibt ein Handle für einen unvollständigen Kontext an.<br/> |
| <dl> <dt>**SEK \_ . E \_ nicht unterstützte \_ Funktion**</dt> <dt>0x80090302</dt> </dl> | Die Funktion ist fehlgeschlagen. Der Wert des *ulattribute* -Parameters ist ungültig.<br/>                 |



 

## <a name="remarks"></a>Bemerkungen

Die Struktur, auf die durch den *pbuffer* -Parameter gezeigt wird, variiert je nach dem abgefragten Attribut.

Während der Aufrufer die *pbuffer* -Struktur selbst zuordnen muss, ordnet der SSP den Speicher zu, der zum Speichern der Elemente variabler Größe der *pbuffer* -Struktur erforderlich ist. Der durch den SSP zugewiesene Arbeitsspeicher muss freigegeben werden, indem die [**freecontextbuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) -Funktion aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>SSPI. h (Include Security. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Unicode- und ANSI-Name<br/>   | **Querycontextattributesw** (Unicode) und **querycontextattributesa** (ANSI)<br/>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[SSPI-Funktionen](authentication-functions.md#sspi-functions)
</dt> <dt>

[**CERT- \_ Kontext**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**Freecontextbuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)
</dt> <dt>

[**Secpkgcontext- \_ Clientbuilds**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds)
</dt> <dt>

[**Secpkgcontext- \_ Größen**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes)
</dt> </dl>

 

 
