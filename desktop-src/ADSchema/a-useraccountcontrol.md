---
title: User-Account-Control-Attribut
description: Flags, die das Verhalten des Benutzerkontos steuern.
ms.assetid: fc81a16a-f537-44cc-957c-5d7ca66b9755
ms.tgt_platform: multiple
keywords:
- AD-Schema des Attributs "User-Account-Control"
- AD-Schema des userAccountControl-Attributs
topic_type:
- apiref
api_name:
- User-Account-Control
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76ab64d0d93ce7523c3d91d6f4a3ebb5f4d200f0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468797"
---
# <a name="user-account-control-attribute"></a>User-Account-Control-Attribut

Flags, die das Verhalten des Benutzerkontos steuern.



| Eingabe | Wert |
|-------------------|---------------------------------------|
| CN                | Benutzerkontensteuerung                  |
| Ldap-Anzeigename | userAccountControl                    |
| Size              | 4 Bytes.                              |
| Aktualisieren von Berechtigungen  | Dieser Wert wird vom System festgelegt.      |
| Updatehäufigkeit  | Jedes Mal, wenn sich die Kontorichtlinie ändert. |
| Attribute-Id      | 1.2.840.113556.1.4.8                  |
| System-Id-Guid    | bf967a68-0de6-11d0-a285-00aa003049e2  |
| Syntax            | [**Enumeration**](s-enumeration.md)  |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Is-Single-Valued       | True                              |
| Ist indiziert             | True                              |
| Im globalen Katalog      | True                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Is-Single-Valued       | True                              |
| Ist indiziert             | True                              |
| Im globalen Katalog      | True                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Is-Single-Valued       | True                              |
| Ist indiziert             | True                              |
| Im globalen Katalog      | True                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Ist einwertig       | True                              |
| Ist indiziert             | True                              |
| Im globalen Katalog      | True                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Ist einwertig       | True                              |
| Ist indiziert             | True                              |
| Im globalen Katalog      | True                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Ist einwertig       | True                              |
| Ist indiziert             | True                              |
| Im globalen Katalog      | True                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="remarks"></a>Hinweise

Dieser Attributwert kann 0 (null) oder eine Kombination aus einem oder mehreren der folgenden Werte sein.




| Hexadezimalwert | Bezeichner (definiert in iads.h) | Beschreibung | 
|-------------------|--------------------------------|-------------|
| 0x00000001 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SCRIPT</strong></a> | Das Anmeldeskript wird ausgeführt. | 
| 0x00000002 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ACCOUNTDISABLE</strong></a> | Das Benutzerkonto ist deaktiviert. | 
| 0x00000008 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_HOMEDIR_REQUIRED</strong></a> | Das Stammverzeichnis ist erforderlich. | 
| 0x00000010 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_LOCKOUT</strong></a> | Das Konto ist derzeit gesperrt. | 
| 0x00000020 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_NOTREQD</strong></a> | Es ist kein Kennwort erforderlich. | 
| 0x00000040 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_CANT_CHANGE</strong></a> | Der Benutzer kann das Kennwort nicht ändern.<blockquote>[!Note]<br />Sie können die Berechtigungseinstellungen von PASSWD_CANT_CHANGE nicht zuweisen, indem Sie das UserAccountControl-Attribut direkt ändern. Weitere Informationen und ein Codebeispiel, das zeigt, wie verhindert wird, dass ein Benutzer das Kennwort ändert, finden Sie unter <a href="/windows/desktop/ADSI/user-cannot-change-password">User Cannot Change Password</a>.</blockquote><br /> : | 
| 0x00000080 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED</strong></a> | Der Benutzer kann ein verschlüsseltes Kennwort senden. | 
| 0x00000100 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TEMP_DUPLICATE_ACCOUNT</strong></a> | Dies ist ein Konto für Benutzer, deren primäres Konto sich in einer anderen Domäne befindet. Dieses Konto ermöglicht den Benutzerzugriff auf diese Domäne, jedoch nicht auf eine Domäne, die dieser Domäne vertraut. Wird auch als lokales Benutzerkonto bezeichnet. | 
| 0x00000200 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NORMAL_ACCOUNT</strong></a> | Dies ist ein Standardkontotyp, der einen typischen Benutzer darstellt. | 
| 0x00000800 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_INTERDOMAIN_TRUST_ACCOUNT</strong></a> | Dies ist eine Zulassung zum Vertrauenswürdigkeitskonto für eine Systemdomäne, die anderen Domänen vertraut. | 
| 0x00001000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_WORKSTATION_TRUST_ACCOUNT</strong></a> | Dies ist ein Computerkonto für einen Computer, der Mitglied dieser Domäne ist. | 
| 0x00002000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SERVER_TRUST_ACCOUNT</strong></a> | Dies ist ein Computerkonto für einen Systemsicherungsdomänencontroller, der Mitglied dieser Domäne ist. | 
| 0x00004000 | – | Nicht verwendet. | 
| 0x00008000 | – | Nicht verwendet. | 
| 0x00010000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_EXPIRE_PASSWD</strong></a> | Das Kennwort für dieses Konto läuft nie ab. | 
| 0x00020000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_MNS_LOGON_ACCOUNT</strong></a> | Dies ist ein MNS-Anmeldekonto. | 
| 0x00040000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SMARTCARD_REQUIRED</strong></a> | Der Benutzer muss sich mit einer Smartcard anmelden. | 
| 0x00080000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_FOR_DELEGATION</strong></a> | Das Dienstkonto (Benutzer- oder Computerkonto), unter dem ein Dienst ausgeführt wird, wird für die Kerberos-Delegierung als vertrauenswürdig eingestuft. Jeder dieser Dienste kann die Identität eines Clients annehmen, der den Dienst anfordert. | 
| 0x00100000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NOT_DELEGATED</strong></a> | Der Sicherheitskontext des Benutzers wird nicht an einen Dienst delegiert, auch wenn das Dienstkonto für die Kerberos-Delegierung als vertrauenswürdig festgelegt ist. | 
| 0x00200000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_USE_DES_KEY_ONLY</strong></a> | Schränken Sie diesen Prinzipal so ein, dass nur Verschlüsselungstypen vom Typ Data Encryption Standard (DES) für Schlüssel verwendet werden. | 
| 0x00400000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_REQUIRE_PREAUTH</strong></a> | Für dieses Konto ist keine Kerberos-Vorauthentifizierung für die Anmeldung erforderlich. | 
| 0x00800000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWORD_EXPIRED</strong></a> | Das Benutzerkennwort ist abgelaufen. Dieses Flag wird vom System mithilfe von Daten aus dem <a href="a-pwdlastset.md"><strong>Pwd-Last-Set-Attribut</strong></a> und der Domänenrichtlinie erstellt. | 
| 0x01000000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION</strong></a> | Das Konto ist für die Delegierung aktiviert. Dies ist eine sicherheitsbezogene Einstellung. Konten, für die diese Option aktiviert ist, sollten streng kontrolliert werden. Mit dieser Einstellung kann ein Dienst, der unter dem Konto ausgeführt wird, eine Clientidentität annehmen und sich als dieser Benutzer bei anderen Remoteservern im Netzwerk authentifizieren. | 




 

