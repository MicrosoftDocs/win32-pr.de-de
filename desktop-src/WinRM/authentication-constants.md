---
title: Authentifizierungs Konstanten (WSManDisp. h)
description: Geben Sie die Authentifizierungsmethode an und wie Sie Zertifikat Server für den HTTPS-Transport von Anforderungen verarbeiten.
ms.assetid: adfefbc9-c386-48db-a0c2-145aa4f91bfa
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagCredUsernamePassword
- WSManFlagSkipCACheck
- WSManFlagSkipCNCheck
- WSManFlagUseNoAuthentication
- WSManFlagUseDigest
- WSManFlagUseNegotiate
- WSManFlagUseBasic
- WSManFlagUseKerberos
- WSManFlagNoEncryption
- WSManFlagUseClientCertificate
- WSManFlagUseCredSsp
- WSManFlagSkipRevocationCheck
- WSManFlagAllowNegotiateImplicitCredentials
- WSManFlagUseSsl
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce45d1474cf6c925149c05ae348231333c3356e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518773"
---
# <a name="authentication-constants"></a>Authentifizierungs Konstanten

Authentifizierungs Konstanten sind Konstanten in der **\_ \_ wsmansessionflags** -Enumeration, die die Authentifizierungsmethode angeben und angeben, wie Zertifikat Server für den HTTPS-Transport von Anforderungen behandelt werden.

Mindestens eine der in der folgenden Liste aufgeführten Konstanten ist im *Flags* -Parameter in Aufrufen von [**WSMAN. kreatesession**](wsman-createsession.md) oder in [**iwsman:: anatesession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) -aufrufen erforderlich, die eine Verbindung mit einem Remote Computer herstellen.

<dl> <dt>

<span id="WSManFlagCredUsernamePassword"></span><span id="wsmanflagcredusernamepassword"></span><span id="WSMANFLAGCREDUSERNAMEPASSWORD"></span>**Wsmanflagkredusernamepassword**
</dt> <dd> <dl> <dt>

4096 (0x1000)
</dt> <dt>



Verwenden Sie den Benutzernamen und das Kennwort als Anmelde Informationen. Legen Sie dieses Flag fest, wenn Sie ein [**ConnectionOptions**](connectionoptions.md) -Objekt erstellen und [**Benutzername**](connectionoptions-username.md) und [**Kennwort**](connectionoptions-password.md)angeben. Bei den Anmelde Informationen kann es sich um ein Domänen Konto oder ein Konto auf dem lokalen Computer handeln. Standardmäßig muss das Konto ein Mitglied der lokalen Gruppe "Administratoren" auf dem lokalen Computer oder dem Remote Computer sein. Der WinRM-Dienst kann jedoch so konfiguriert werden, dass er anderen Benutzern gestattet wird. Weitere Informationen finden Sie unter [Installation und Konfiguration für Windows-Remoteverwaltung](installation-and-configuration-for-windows-remote-management.md). Sie können dieses Flag festlegen, wenn Sie Anmelde Informationen für die Aushandlungs Authentifizierung (auch bekannt als [*integrierte Windows-Authentifizierung*](windows-remote-management-glossary.md)) oder für die Standard [*Authentifizierung*](windows-remote-management-glossary.md)angeben.

Die zugeordnete Skript Methode lautet " [**WSMAN. sessionflagkredusernamepassword**](wsman-sessionflagcredusernamepassword.md)", und die C++-Methode ist " [**iwsmanex. sessionflagkredusernamepassword**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagcredusernamepassword)".


</dt> </dl> </dd> <dt>

<span id="WSManFlagSkipCACheck"></span><span id="wsmanflagskipcacheck"></span><span id="WSMANFLAGSKIPCACHECK"></span>**Wsmanflagskipcacheck**
</dt> <dd> <dl> <dt>

8192 (0x2000)
</dt> <dt>



Beim Herstellen einer Verbindung über HTTPS überprüft der Client nicht, ob das Serverzertifikat von einer vertrauenswürdigen Zertifizierungsstelle (Certification Authority, ca) signiert wurde. Verwenden Sie diesen Wert nur, wenn der Remote Computer auf andere Weise vertrauenswürdig ist, z. b. wenn der Remote Computer Teil eines physisch sicheren und isolierten Netzwerks ist oder wenn der Remote Computer in der WinRM-Konfiguration als vertrauenswürdiger Host aufgeführt ist.

Die zugeordnete Skript Methode lautet [**WSMAN. sessionflagskipcacheck**](wsman-sessionflagskipcacheck.md), und die C++-Methode ist [**iwsmanex. sessionflagskipcacheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcacheck).


</dt> </dl> </dd> <dt>

<span id="WSManFlagSkipCNCheck"></span><span id="wsmanflagskipcncheck"></span><span id="WSMANFLAGSKIPCNCHECK"></span>**Wsmanflagskipcncheck**
</dt> <dd> <dl> <dt>

16384 (0x4000)
</dt> <dt>



Wenn eine Verbindung über HTTPS hergestellt wird, überprüft der Client nicht, ob der allgemeine Name (Common Name, CN) im Serverzertifikat mit dem Computernamen in der Verbindungs Zeichenfolge übereinstimmt. Nur verwenden, wenn der Remote Computer auf andere Weise vertrauenswürdig ist, z. b. wenn der Remote Computer Teil eines physisch sicheren und isolierten Netzwerks ist oder wenn der Remote Computer in der WinRM-Konfiguration als vertrauenswürdiger Host aufgeführt ist.

Die zugeordnete Skript Methode lautet " [**WSMAN. sessionflagskipcncheck**](wsman-sessionflagskipcncheck.md)", und die C++-Methode ist " [**iwsmanex. sessionflagskipcncheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcncheck)".


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseNoAuthentication"></span><span id="wsmanflagusenoauthentication"></span><span id="WSMANFLAGUSENOAUTHENTICATION"></span>**Wsmanflagusenoauthentication**
</dt> <dd> <dl> <dt>

32768 (0X8000)
</dt> <dt>



Verwenden Sie keine Authentifizierung. Geben Sie diese Konstante beim Testen einer Verbindung mit einem Remote Computer an, um zu bestimmen, ob ein Dienst, der das WS-Management Protokoll implementiert, für das Lauschen auf Datenanforderungen konfiguriert ist. " **Wsmanflagusenoauthentication** " kann nicht mit einer anderen [**Sitzungs**](session.md) Konstante kombiniert werden. Die zugeordnete Skript Methode lautet [**WSMAN. sessionflagusenoauthentication**](wsman-sessionflagusenoauthentication.md), und die C++-Methode ist [**wsmanex. sessionflagusenoauthentication**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenoauthentication).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseDigest"></span><span id="wsmanflagusedigest"></span><span id="WSMANFLAGUSEDIGEST"></span>**Wsmanflagusedigest**
</dt> <dd> <dl> <dt>

65536 (0x10000)
</dt> <dt>



Verwenden Sie die Digestauthentifizierung. Nur der Clientcomputer kann eine Anforderung der Digestauthentifizierung initiieren. Der Client sendet eine Anforderung an den Server, um eine Tokenzeichenfolge vom Server zu authentifizieren und zu empfangen. Der Client sendet dann die Ressourcen Anforderung, einschließlich des Benutzernamens und eines kryptografischen Hashs des Kennworts, in Kombination mit der Tokenzeichenfolge. Die Digest-Authentifizierung wird für http und HTTPS unterstützt. WinRM-Client Skripts und-Anwendungen können die Digestauthentifizierung angeben, jedoch nicht den-Dienst.

Die zugeordnete Skript Methode ist [**WSMAN. sessionflagusedigest**](wsman-sessionflagusedigest.md), und die C++-Methode ist [**iwsmanex. sessionflagusedigest**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusedigest).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseNegotiate"></span><span id="wsmanflagusenegotiate"></span><span id="WSMANFLAGUSENEGOTIATE"></span>**Wsmanflagusenegotiate**
</dt> <dd> <dl> <dt>

131072 (0x20000)
</dt> <dt>



Verwenden Sie die Aushandlungs Authentifizierung. Der Client sendet eine Anforderung an den Server, um sich zu authentifizieren. Der Server bestimmt, ob Kerberos oder NTLM verwendet werden soll. Kerberos wird zum Authentifizieren eines Domänen Kontos ausgewählt, und NTLM ist für lokale Computer Konten ausgewählt. Der Benutzername muss im Format Domäne \\ Benutzername für einen Domänen Benutzer oder \\ Servername Benutzername für einen lokalen Benutzer auf einem Server Computer angegeben werden.

Die [Benutzerkontensteuerung (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) wirkt sich auf den Zugriff auf den WinRM-Dienst aus. Wenn die Aushandlungs Authentifizierung in einer Arbeitsgruppe oder Domäne verwendet wird, kann nur das integrierte Administrator Konto auf den Dienst zugreifen. Damit alle Konten in der Gruppe "Administratoren" auf den Dienst zugreifen können, legen Sie den folgenden Registrierungsschlüssel auf 1 fest: **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Policies \\ System \\ LocalAccountTokenFilterPolicy**.

Die zugeordnete Skript Methode ist [**WSMAN. sessionflagusenegotiate**](wsman-sessionflagusenegotiate.md), und die C++-Methode ist [**iwsmanex. sessionflagusenegotiate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenegotiate).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseBasic"></span><span id="wsmanflagusebasic"></span><span id="WSMANFLAGUSEBASIC"></span>**Wsmanflagusebasic**
</dt> <dd> <dl> <dt>

262144 (0x40000)
</dt> <dt>



Verwenden Sie die Standard Authentifizierung. Der Client stellt Anmelde Informationen in Form eines Benutzernamens und eines Kennworts dar, die direkt in der Anforderungs Nachricht übertragen werden. Sie können nur Anmelde Informationen angeben, die ein lokales Administrator Konto auf dem Remote Computer identifizieren.

Die zugeordnete Skript Methode lautet " [**WSMAN. sessionflagusebasic**](wsman-sessionflagusebasic.md)", und die C++-Methode ist " [**iwsmanex. sessionflagusebasic**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusebasic)".


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseKerberos"></span><span id="wsmanflagusekerberos"></span><span id="WSMANFLAGUSEKERBEROS"></span>**Wsmanflagusekerberos**
</dt> <dd> <dl> <dt>

524288 (0x80000)
</dt> <dt>



Verwenden Sie Kerberos-Authentifizierung. Der Client und der Server authentifizieren sich gegenseitig mithilfe von Kerberos-Tickets.

Die zugeordnete Skript Methode lautet [**WSMAN. sessionflagusekerberos**](wsman-sessionflagusekerberos.md), und die C++-Methode ist [**iwsmanex. WSMAN. sessionflagusekerberos**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusekerberos).


</dt> </dl> </dd> <dt>

<span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**Wsmanflagnoencryption**
</dt> <dd> <dl> <dt>

1048576 (0x100000)
</dt> <dt>



Verwenden Sie keine Verschlüsselung. Unverschlüsselter Datenverkehr ist standardmäßig nicht zulässig und muss sowohl auf dem Client als auch auf dem Server aktiviert sein.

Die zugeordnete Skript Methode lautet " [**WSMAN. sessionflagnoencryption**](wsman-sessionflagnoencryption.md)", und die C++-Methode ist " [**iwsmanex. sessionflagnoencryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption)".


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseClientCertificate"></span><span id="wsmanflaguseclientcertificate"></span><span id="WSMANFLAGUSECLIENTCERTIFICATE"></span>**Wsmanflaguseclientcertificate**
</dt> <dd> <dl> <dt>

2097152 (0x200.000)
</dt> <dt>



Verwenden Sie die Zertifikat basierte Client Authentifizierung.

Die zugehörige Skript Methode lautet [**WSMAN. sessionflaguseclientcertificate**](wsman-sessionflaguseclientcert.md), und die C++-Methode ist [**IWSManEx2. sessionflaguseclientcertificate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex2-sessionflaguseclientcertificate).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseCredSsp"></span><span id="wsmanflagusecredssp"></span><span id="WSMANFLAGUSECREDSSP"></span>**Wsmanflagusecredssp**
</dt> <dd> <dl> <dt>

16777216 (0x1000000)
</dt> <dt>



Verwenden Sie die Authentifizierung der Credential Security Support Provider (kredssp).

Die zugeordnete Skript Methode ist [**WSMAN. sessionflagusecredssp**](wsman-sessionflagusecredssp.md), und die C++-Methode ist [**IWSManEx3. sessionflagusecredssp**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex3-sessionflagusecredssp).


</dt> </dl> </dd> <dt>

<span id="WSManFlagSkipRevocationCheck"></span><span id="wsmanflagskiprevocationcheck"></span><span id="WSMANFLAGSKIPREVOCATIONCHECK"></span>**Wsmanflagskiprevocationcheck**
</dt> <dd> <dl> <dt>

0x2000000
</dt> <dt>



Überprüfen Sie während der Authentifizierung nicht, ob die Zertifikat Sperre besteht.


</dt> </dl> </dd> <dt>

<span id="WSManFlagAllowNegotiateImplicitCredentials"></span><span id="wsmanflagallownegotiateimplicitcredentials"></span><span id="WSMANFLAGALLOWNEGOTIATEIMPLICITCREDENTIALS"></span>**Wsmanflagallowaushandateimplicitanmelde Informationen**
</dt> <dd> <dl> <dt>

0x4000000
</dt> <dt>



Implizite Anmelde Informationen zulassen.


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseSsl"></span><span id="wsmanflagusessl"></span><span id="WSMANFLAGUSESSL"></span>**Wsmanflagus Essl**
</dt> <dd> <dl> <dt>

0x8000000
</dt> <dt>



Verwenden Sie Secure Socket Layer, aktiviert HTTPS.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Sitzungs Konstanten](session-constants.md)
</dt> </dl>

 

 





