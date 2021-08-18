---
title: Authentifizierungskonstanten (WSManDisp.h)
description: Geben Sie die Authentifizierungsmethode und die Behandlung von Zertifikatservern für den HTTPS-Transport von Anforderungen an.
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
ms.openlocfilehash: 885e3b782c4af67304f1a92eca324c0f266e71665a7a876683cbb1dbff472ee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132813"
---
# <a name="authentication-constants"></a>Authentifizierungskonstanten

Authentifizierungskonstanten sind Konstanten in der **\_ \_ WSManSessionFlags-Enumeration,** die die Authentifizierungsmethode und die Behandlung von Zertifikatservern für den HTTPS-Transport von Anforderungen angeben.

Mindestens eine der in der folgenden Liste aufgeführten Konstanten ist im *flags-Parameter* in Aufrufen von [**WSMan.CreateSession**](wsman-createsession.md) oder in [**IWSMan::CreateSession-Aufrufen**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) erforderlich, die eine Verbindung mit einem Remotecomputer herstellen.

<dl> <dt>

<span id="WSManFlagCredUsernamePassword"></span><span id="wsmanflagcredusernamepassword"></span><span id="WSMANFLAGCREDUSERNAMEPASSWORD"></span>**WSManFlagCredUsernamePassword**
</dt> <dd> <dl> <dt>

4096 (0x1000)
</dt> <dt>



Verwenden Sie den Benutzernamen und das Kennwort als Anmeldeinformationen. Legen Sie dieses Flag fest, wenn Sie ein [**ConnectionOptions-Objekt**](connectionoptions.md) erstellen und [**Benutzername**](connectionoptions-username.md) und [**Kennwort**](connectionoptions-password.md)eingeben. Die Anmeldeinformationen können ein Domänenkonto oder ein Konto auf dem lokalen Computer sein. Standardmäßig muss das Konto Mitglied der lokalen Administratorengruppe auf dem lokalen oder Remotecomputer sein. Der WinRM-Dienst kann jedoch so konfiguriert werden, dass er anderen Benutzern zulässt. Weitere Informationen finden Sie unter [Installation und Konfiguration für Windows Remoteverwaltung.](installation-and-configuration-for-windows-remote-management.md) Sie können dieses Flag festlegen, wenn Sie Anmeldeinformationen für negotiate-Authentifizierung (auch als [*Windows integrierte Authentifizierung*](windows-remote-management-glossary.md)bezeichnet) oder für [*Standardauthentifizierung*](windows-remote-management-glossary.md)angeben.

Die zugeordnete Skriptmethode ist [**WSMan.SessionFlagCredUsernamePassword,**](wsman-sessionflagcredusernamepassword.md)und die C++-Methode ist [**IWSManEx.SessionFlagCredUsernamePassword.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagcredusernamepassword)


</dt> </dl> </dd> <dt>

<span id="WSManFlagSkipCACheck"></span><span id="wsmanflagskipcacheck"></span><span id="WSMANFLAGSKIPCACHECK"></span>**WSManFlagSkipCACheck**
</dt> <dd> <dl> <dt>

8192 (0x2000)
</dt> <dt>



Beim Herstellen einer Verbindung über HTTPS überprüft der Client nicht, ob das Serverzertifikat von einer vertrauenswürdigen Zertifizierungsstelle signiert wurde. Verwenden Sie diesen Wert nur, wenn der Remotecomputer auf andere Weise als vertrauenswürdig eingestuft wird, z. B. wenn der Remotecomputer Teil eines physisch sicheren und isolierten Netzwerks ist oder der Remotecomputer in der WinRM-Konfiguration als vertrauenswürdiger Host aufgeführt ist.

Die zugeordnete Skriptmethode ist [**WSMan.SessionFlagSkipCACheck,**](wsman-sessionflagskipcacheck.md)und die C++-Methode ist [**IWSManEx.SessionFlagSkipCACheck.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcacheck)


</dt> </dl> </dd> <dt>

<span id="WSManFlagSkipCNCheck"></span><span id="wsmanflagskipcncheck"></span><span id="WSMANFLAGSKIPCNCHECK"></span>**WSManFlagSkipCNCheck**
</dt> <dd> <dl> <dt>

16384 (0x4000)
</dt> <dt>



Beim Herstellen einer Verbindung über HTTPS überprüft der Client nicht, ob der allgemeine Name (Common Name, CN) im Serverzertifikat mit dem Computernamen in der Verbindungszeichenfolge übereinstimmt. Verwenden Sie nur, wenn der Remotecomputer auf andere Weise als vertrauenswürdig eingestuft wird, z. B. wenn der Remotecomputer Teil eines physisch sicheren und isolierten Netzwerks ist oder der Remotecomputer in der WinRM-Konfiguration als vertrauenswürdiger Host aufgeführt ist.

Die zugeordnete Skriptmethode ist [**WSMan.SessionFlagSkipCNCheck,**](wsman-sessionflagskipcncheck.md)und die C++-Methode ist [**IWSManEx.SessionFlagSkipCNCheck.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcncheck)


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseNoAuthentication"></span><span id="wsmanflagusenoauthentication"></span><span id="WSMANFLAGUSENOAUTHENTICATION"></span>**WSManFlagUseNoAuthentication**
</dt> <dd> <dl> <dt>

32768 (0x8000)
</dt> <dt>



Verwenden Sie keine Authentifizierung. Geben Sie diese Konstante beim Testen einer Verbindung mit einem Remotecomputer an, um zu bestimmen, ob ein Dienst, der das WS-Management-Protokoll implementiert, für das Lauschen auf Datenanforderungen konfiguriert ist. **WSManFlagUseNoAuthentication** kann nicht mit einer anderen [**Sitzungskonstante**](session.md) kombiniert werden. Die zugeordnete Skriptmethode ist [**WSMan.SessionFlagUseNoAuthentication,**](wsman-sessionflagusenoauthentication.md)und die C++-Methode ist [**WSManEx.SessionFlagUseNoAuthentication.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenoauthentication)


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseDigest"></span><span id="wsmanflagusedigest"></span><span id="WSMANFLAGUSEDIGEST"></span>**WSManFlagUseDigest**
</dt> <dd> <dl> <dt>

65536 (0x10000)
</dt> <dt>



Verwenden Sie die Digestauthentifizierung. Nur der Clientcomputer kann eine Anforderung der Digestauthentifizierung initiieren. Der Client sendet eine Anforderung zur Authentifizierung an den Server und empfängt eine Tokenzeichenfolge vom Server. Der Client sendet dann die Ressourcenanforderung, einschließlich des Benutzernamens und eines kryptografischen Hashs des Kennworts in Kombination mit der Tokenzeichenfolge. Die Digestauthentifizierung wird für HTTP und HTTPS unterstützt. WinRM-Clientskripts und -Anwendungen können die Digestauthentifizierung angeben, aber nicht den Dienst.

Die zugeordnete Skriptmethode ist [**WSMan.SessionFlagUseDigest,**](wsman-sessionflagusedigest.md)und die C++-Methode ist [**IWSManEx.SessionFlagUseDigest.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusedigest)


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseNegotiate"></span><span id="wsmanflagusenegotiate"></span><span id="WSMANFLAGUSENEGOTIATE"></span>**WSManFlagUseNegotiate**
</dt> <dd> <dl> <dt>

131072 (0x20000)
</dt> <dt>



Verwenden Sie negotiate authentication (Aushandeln der Authentifizierung). Der Client sendet eine Anforderung zur Authentifizierung an den Server. Der Server bestimmt, ob Kerberos oder NTLM verwendet werden soll. Kerberos wird ausgewählt, um ein Domänenkonto zu authentifizieren, und NTLM wird für lokale Computerkonten ausgewählt. Der Benutzername muss im Format \\ Domänenbenutzername für einen Domänenbenutzer oder \\ Servername-Benutzername für einen lokalen Benutzer auf einem Servercomputer angegeben werden.

[Die Benutzerkontensteuerung (User Account Control, UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) wirkt sich auf den Zugriff auf den WinRM-Dienst aus. Wenn die Negotiate-Authentifizierung in einer Arbeitsgruppe oder Domäne verwendet wird, kann nur das integrierte Administratorkonto auf den Dienst zugreifen. Damit alle Konten in der Gruppe Administratoren auf den Dienst zugreifen können, legen Sie den folgenden Registrierungsschlüssel auf 1 fest: **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion Policies system \\ \\ \\ LocalAccountTokenFilterPolicy**.

Die zugeordnete Skriptmethode ist [**WSMan.SessionFlagUseNegotiate,**](wsman-sessionflagusenegotiate.md)und die C++-Methode ist [**IWSManEx.SessionFlagUseNegotiate.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenegotiate)


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseBasic"></span><span id="wsmanflagusebasic"></span><span id="WSMANFLAGUSEBASIC"></span>**WSManFlagUseBasic**
</dt> <dd> <dl> <dt>

262144 (0x40000)
</dt> <dt>



Verwenden Sie die Standardauthentifizierung. Der Client stellt Anmeldeinformationen in Form eines Benutzernamens und Kennworts dar, die direkt in der Anforderungsnachricht übertragen werden. Sie können nur Anmeldeinformationen angeben, die ein lokales Administratorkonto auf dem Remotecomputer identifizieren.

Die zugeordnete Skriptmethode ist [**WSMan.SessionFlagUseBasic,**](wsman-sessionflagusebasic.md)und die C++-Methode ist [**IWSManEx.SessionFlagUseBasic.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusebasic)


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseKerberos"></span><span id="wsmanflagusekerberos"></span><span id="WSMANFLAGUSEKERBEROS"></span>**WSManFlagUseKerberos**
</dt> <dd> <dl> <dt>

524288 (0x80000)
</dt> <dt>



Verwenden Sie Kerberos-Authentifizierung. Client und Server authentifizieren sich gegenseitig mit Kerberos-Tickets.

Die zugeordnete Skriptmethode ist [**WSMan.SessionFlagUseKerberos,**](wsman-sessionflagusekerberos.md)und die C++-Methode ist [**IWSManEx.WSMan.SessionFlagUseKerberos.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusekerberos)


</dt> </dl> </dd> <dt>

<span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**
</dt> <dd> <dl> <dt>

1048576 (0x100000)
</dt> <dt>



Verwenden Sie keine Verschlüsselung. Unverschlüsselter Datenverkehr ist standardmäßig nicht zulässig und muss sowohl auf dem Client als auch auf dem Server aktiviert sein.

Die zugeordnete Skriptmethode ist [**WSMan.SessionFlagNoEncryption,**](wsman-sessionflagnoencryption.md)und die C++-Methode ist [**IWSManEx.SessionFlagNoEncryption.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption)


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseClientCertificate"></span><span id="wsmanflaguseclientcertificate"></span><span id="WSMANFLAGUSECLIENTCERTIFICATE"></span>**WSManFlagUseClientCertificate**
</dt> <dd> <dl> <dt>

2097152 (0x200000)
</dt> <dt>



Verwenden Sie die clientzertifikatbasierte Authentifizierung.

Die zugeordnete Skriptmethode ist [**WSMan.SessionFlagUseClientCertificate,**](wsman-sessionflaguseclientcert.md)und die C++-Methode ist [**IWSManEx2.SessionFlagUseClientCertificate.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex2-sessionflaguseclientcertificate)


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseCredSsp"></span><span id="wsmanflagusecredssp"></span><span id="WSMANFLAGUSECREDSSP"></span>**WSManFlagUseCredSsp**
</dt> <dd> <dl> <dt>

16777216 (0x1000000)
</dt> <dt>



Verwenden Sie die CredSSP-Authentifizierung (Credential Security Support Provider).

Die zugeordnete Skriptmethode ist [**WSMan.SessionFlagUseCredSsp,**](wsman-sessionflagusecredssp.md)und die C++-Methode ist [**IWSManEx3.SessionFlagUseCredSsp.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex3-sessionflagusecredssp)


</dt> </dl> </dd> <dt>

<span id="WSManFlagSkipRevocationCheck"></span><span id="wsmanflagskiprevocationcheck"></span><span id="WSMANFLAGSKIPREVOCATIONCHECK"></span>**WSManFlagSkipRevocationCheck**
</dt> <dd> <dl> <dt>

0x2000000
</dt> <dt>



Überprüfen Sie während der Authentifizierung nicht auf Zertifikatsperrung.


</dt> </dl> </dd> <dt>

<span id="WSManFlagAllowNegotiateImplicitCredentials"></span><span id="wsmanflagallownegotiateimplicitcredentials"></span><span id="WSMANFLAGALLOWNEGOTIATEIMPLICITCREDENTIALS"></span>**WSManFlagAllowNegotiateImplicitCredentials**
</dt> <dd> <dl> <dt>

0x4000000
</dt> <dt>



Implizite Anmeldeinformationen zulassen.


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseSsl"></span><span id="wsmanflagusessl"></span><span id="WSMANFLAGUSESSL"></span>**WSManFlagUseSsl**
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
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Sitzungskonstanten](session-constants.md)
</dt> </dl>

 

 





