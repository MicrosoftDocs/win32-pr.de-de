---
description: Ermöglicht es einer Transport Anwendung, das Aushandlungs [*Sicherheitspaket*](../secgloss/s-gly.md) für bestimmte Attribute eines [*Sicherheits Kontexts*](../secgloss/s-gly.md)abzufragen.
ms.assetid: 9e499161-d5fb-4a64-ac36-f82031a3a7c9
title: QueryContextAttributes (Negotiate)-Funktion (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: e46d49a8e1219c35073df96193612b2e3497b87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348156"
---
# <a name="querycontextattributes-negotiate-function"></a>QueryContextAttributes (aushandeln)-Funktion

Mithilfe der **QueryContextAttributes (Aushandlungs)** -Funktion kann eine Transport Anwendung das Aushandlungs [*Sicherheitspaket*](../secgloss/s-gly.md) für bestimmte [*Attribute*](../secgloss/a-gly.md#_security_attribute_gly) eines [*Sicherheits Kontexts*](../secgloss/s-gly.md)Abfragen.

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

Ein Handle für den [*Sicherheitskontext*](../secgloss/s-gly.md) , der abgefragt werden soll.

</dd> <dt>

*ulattribute* \[ in\]
</dt> <dd>

Gibt das Attribut des Kontexts an, der zurückgegeben werden soll. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                                                                                          | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_ATTR_ACCESS_TOKEN"></span><span id="secpkg_attr_access_token"></span><dl> <dt>**Secpkg \_ Attr- \_ Zugriffs \_ Token**</dt> <dt>18</dt> </dl>                                       | Der *pbuffer* -Parameter enthält einen Zeiger auf eine [**secpkgcontext \_ accesstoken**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_accesstoken) -Struktur.<br/> Gibt ein Handle für das Zugriffs Token zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_AUTHORITY"></span><span id="secpkg_attr_authority"></span><dl> <dt>**Secpkg \_ Attr- \_ Autorität**</dt> <dt>6</dt> </dl>                                                  | Der *pbuffer* -Parameter enthält einen Zeiger auf eine [**secpkgcontext- \_ Autorität**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_authoritya) -Struktur.<br/> Fragt den Namen der authentifizier enden Zertifizierungsstelle ab.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="SECPKG_ATTR_CLIENT_SPECIFIED_TARGET"></span><span id="secpkg_attr_client_specified_target"></span><dl> <dt>**Secpkg \_ Der attr- \_ Client hat \_ \_ Ziel**</dt> <dt>27</dt> angegeben. </dl>     | Der *pbuffer* -Parameter enthält einen Zeiger auf eine [**secpkgcontext- \_ clientspezifiedtarget**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_clientspecifiedtarget) -Struktur, die den Dienst Prinzipal Namen (SPN) des ursprünglichen Ziels darstellt, das vom Client bereitgestellt wird. <br/> Dieser Wert wird nur unterstützt, wenn Channel-Bindungen verwendet werden.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SECPKG_ATTR_CREDS_2"></span><span id="secpkg_attr_creds_2"></span><dl> <dt>**Secpkg \_ Attr \_ \_**</dt> -Erstellungs-2 <dt>0x80000086</dt> </dl>                                              | Der *pbuffer* -Parameter enthält einen Zeiger auf eine [**secpkgcontext- \_ clientkreds**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds) -Struktur, die Client Anmelde Informationen angibt. <br/> Wenn die Client Anmelde Informationen "Benutzername" und "Kennwort" sind, handelt es sich bei dem Puffer um [**eine gepackte \_ \_**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_interactive_logon) , gepackte<br/> Wenn es sich bei den Client [**\_ \_ Anmelde**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_certificate_logon) Informationen um den Benutzernamen und die Smartcard-PIN handelt, ist der Puffer eine gepackte Struktur für das KERB Zertifikat<br/> Handelt es sich bei den Client Anmelde Informationen um Online-Identitäts Anmelde Informationen, ist der Puffer eine gemarshallte [**Sek. \_ Winnt \_ auth \_ Identity \_ ex2**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) -Struktur.<br/> Dieses Attribut wird nur auf dem-Server mit dem-Server unterstützt.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.<br/> |
| <span id="SECPKG_ATTR_DCE_INFO"></span><span id="secpkg_attr_dce_info"></span><dl> <dt>**Secpkg \_ Attr- \_ DCE- \_ Informationen**</dt> <dt>3</dt> </dl>                                                    | Der *pbuffer* -Parameter enthält einen Zeiger auf eine [**secpkgcontext \_ dceinfo**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_dceinfo) -Struktur.<br/> Abfragen von Autorisierungs Daten, die von DCE-Diensten verwendet werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="SECPKG_ATTR_FLAGS"></span><span id="secpkg_attr_flags"></span><dl> <dt>**Secpkg \_ Attr- \_ Flags**</dt> <dt>14</dt> </dl>                                                             | Der *pbuffer* -Parameter enthält einen Zeiger auf eine [**secpkgcontext- \_ Flags**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_flags) -Struktur.<br/> Gibt Informationen zu den ausgehandelten kontextflags zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="SECPKG_ATTR_KEY_INFO"></span><span id="secpkg_attr_key_info"></span><dl> <dt>**Secpkg \_ Attr- \_ Schlüssel \_ Informationen**</dt> <dt>5</dt> </dl>                                                    | Der *pbuffer* -Parameter enthält einen Zeiger auf eine [**secpkgcontext- \_ KeyInfo**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_keyinfoa) -Struktur.<br/> Fragt Informationen zu den Schlüsseln ab, die in einem [*Sicherheitskontext*](../secgloss/s-gly.md)verwendet werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SECPKG_ATTR_LAST_CLIENT_TOKEN_STATUS"></span><span id="secpkg_attr_last_client_token_status"></span><dl> <dt>**Secpkg \_ Status des \_ letzten \_ Client \_ \_ Tokens für attr**</dt> <dt>30</dt> </dl> | Der *pbuffer* -Parameter enthält einen Zeiger auf eine [**secpkgcontext \_ lastclienttokenstatus**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_lastclienttokenstatus) -Struktur, die angibt, ob das Token vom letzten Aufrufen der [**InitializeSecurityContext**](initializesecuritycontext--general.md) -Funktion das letzte Token des Clients ist.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="SECPKG_ATTR_LIFESPAN"></span><span id="secpkg_attr_lifespan"></span><dl> <dt>**Secpkg \_ Attr- \_ Lebensdauer**</dt> <dt>2</dt> </dl>                                                     | Der *pbuffer* -Parameter enthält einen Zeiger auf eine [**secpkgcontext- \_ Lebensdauer**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_lifespan) -Struktur.<br/> Fragt die Lebensdauer des Kontexts ab.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="SECPKG_ATTR_LOCAL_CRED"></span><span id="secpkg_attr_local_cred"></span><dl> <dt>**secpkg \_ attr \_ local \_ -Setup**</dt> </dl>                                                                                                     | Der *pbuffer* -Parameter enthält einen Zeiger auf eine **secpkgcontext \_ localkredentialinfo** -Struktur. (Veraltet)<br/> Wird durch \_ \_ den lokalen \_ Zertifikat Kontext von secpkg attr abgelöst \_ .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="SECPKG_ATTR_NAMES"></span><span id="secpkg_attr_names"></span><dl> <dt>**Secpkg \_ Attr- \_ Namen**</dt> <dt>1</dt> </dl>                                                              | Der *pbuffer* -Parameter enthält einen Zeiger auf eine [**secpkgcontext \_ Names**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_namesa) -Struktur.<br/> Fragt den Namen ab, der dem Kontext zugeordnet ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="SECPKG_ATTR_NATIVE_NAMES"></span><span id="secpkg_attr_native_names"></span><dl> <dt>**Secpkg \_ Attr \_ native \_ Namen**</dt> <dt>13</dt> </dl>                                       | Der *pbuffer* -Parameter enthält einen Zeiger auf eine [**secpkgcontext \_ nativenames**](https://docs.microsoft.com/windows/win32/api/sspi/ns-sspi-_secpkgcontext_nativenamesa) -Struktur.<br/> Gibt den Prinzipal Namen (CNAME) aus dem ausgehenden Ticket zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="SECPKG_ATTR_NEGOTIATION_INFO"></span><span id="secpkg_attr_negotiation_info"></span><dl> <dt>**Secpkg \_ Attr \_ \_**</dt> -Aushandlungs Informationen <dt>12</dt> </dl>                           | Der *pbuffer* -Parameter enthält einen Zeiger auf eine [**secpkgcontext \_ aushandationinfo**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_negotiationinfoa) -Struktur.<br/> Gibt Informationen über das [*Sicherheitspaket*](../secgloss/s-gly.md) zurück, das mit dem Aushandlungs Prozess verwendet werden soll, und den aktuellen Status der Aushandlung für die Verwendung dieses Pakets.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_ATTR_PACKAGE_INFO"></span><span id="secpkg_attr_package_info"></span><dl> <dt>**Secpkg \_ Attr- \_ Paket \_ Informationen**</dt> <dt>10</dt> </dl>                                       | Der *pbuffer* -Parameter enthält einen Zeiger auf eine [**secpkgcontext \_ PackageInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) -Struktur.<br/> Gibt Informationen zum verwendeten SSP zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_PASSWORD_EXPIRY"></span><span id="secpkg_attr_password_expiry"></span><dl> <dt>**Secpkg \_ Attr-Kenn \_ Wort \_ Ablauf**</dt> <dt>8</dt> </dl>                               | Der *pbuffer* -Parameter enthält einen Zeiger auf eine [**secpkgcontext \_ passwordexpiry**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_passwordexpiry) -Struktur.<br/> Gibt Informationen zum Kenn Wort Ablauf zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SECPKG_ATTR_ROOT_STORE"></span><span id="secpkg_attr_root_store"></span><dl> <dt>**Secpkg \_ Attr-Stamm \_ \_ Speicher**</dt> <dt>0x55</dt> </dl>                                           | Der *pbuffer* -Parameter enthält einen Zeiger auf einen **hcertcontext**. <br/> Sucht einen Zertifikat Kontext, der ein vom Stamm Speicher bereitgestelltes Zertifikat enthält.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="SECPKG_ATTR_SESSION_KEY"></span><span id="secpkg_attr_session_key"></span><dl> <dt>**Secpkg \_ Attr- \_ Sitzungs \_ Schlüssel**</dt> <dt>9</dt> </dl>                                           | Der *pbuffer* -Parameter enthält einen Zeiger auf eine [**secpkgcontext \_ SessionKey**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sessionkey) -Struktur.<br/> Gibt Informationen über die [*Sitzungsschlüssel*](../secgloss/s-gly.md)s zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SECPKG_ATTR_SIZES"></span><span id="secpkg_attr_sizes"></span><dl> <dt>**Secpkg \_ Attr- \_ Größen**</dt> <dt>0</dt> </dl>                                                              | Der *pbuffer* -Parameter enthält einen Zeiger auf eine [**secpkgcontext \_ sizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) -Struktur.<br/> Fragt die Größen der in den Funktionen pro Nachricht verwendeten Strukturen ab.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="SECPKG_ATTR_TARGET_INFORMATION"></span><span id="secpkg_attr_target_information"></span><dl> <dt>**Secpkg \_ Attr \_ - \_ Zielinformationen**</dt> <dt>17</dt> </dl>                     | Der *pbuffer* -Parameter enthält einen Zeiger auf eine [**secpkgcontext \_ targetinformation**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_targetinformation) -Struktur.<br/> Gibt Informationen zum Namen des Remote Servers zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

*pbuffer* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine-Struktur, die die Attribute empfängt. Der Typ der Struktur, auf die verwiesen wird, hängt von dem im *ulattribute* -Parameter angegebenen Wert ab.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert sec \_ E \_ OK.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null).

## <a name="remarks"></a>Bemerkungen

Die Struktur, auf die durch den *pbuffer* -Parameter gezeigt wird, variiert je nach dem abgefragten Attribut. Der Aufrufer muss die *pbuffer* -Struktur selbst zuordnen, aber der SSP ordnet den erforderlichen Arbeitsspeicher zu, um die Elemente variabler Größe der *pbuffer* -Struktur zu speichern. Der vom SSP zugeordnete Arbeitsspeicher kann durch Aufrufen der [**freecontextbuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) -Funktion freigegeben werden.

Nachdem der Kontextwert von "secpkg \_ attr- \_ Remote \_ Zertifikat" oder " \_ secpkg \_ attr \_ local CERT" gelesen wurde \_ \_ , wird das **HCERTSTORE** -Mitglied auf ein Handle für einen Zertifikat Speicher festgelegt, der die zwischen Zertifikate enthält (sofern vorhanden). Außerdem ist die Anwendung für den Aufruf von [**certfreecertifipriecontext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) zuständig, um den vom Zertifikat Kontext genutzten Speicher freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                   |
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

[**Secpkgcontext- \_ Autorität**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_authoritya)
</dt> <dt>

[**Secpkgcontext \_ ConnectionInfo**](/windows/win32/api/schannel/ns-schannel-secpkgcontext_connectioninfo)
</dt> <dt>

[**Secpkgcontext \_ dceingefo**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_dceinfo)
</dt> <dt>

[**Secpkgcontext \_ issuerlistinfoex**](/windows/win32/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex)
</dt> <dt>

[**Secpkgcontext- \_ KeyInfo**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_keyinfoa)
</dt> <dt>

[**Lebensdauer von "secpkgcontext" \_**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_lifespan)
</dt> <dt>

[**Secpkgcontext- \_ Namen**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_namesa)
</dt> <dt>

[**Secpkgcontext- \_ Größen**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes)
</dt> <dt>

[**Secpkgcontext- \_ streamsizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes)
</dt> </dl>

 

 
