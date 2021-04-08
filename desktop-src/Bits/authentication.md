---
title: Authentifizierung (Bits)
description: Bits unterstützt die Standard Authentifizierung, die Passport-Authentifizierung und mehrere Challenge/Response-Authentifizierungs Schemas.
ms.assetid: cfd4aec3-79d0-4971-93f8-df797e5c0f75
ms.topic: article
ms.date: 10/09/2018
ms.openlocfilehash: 5d970956676a3348dd4b8c4b420e044bd4714775
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103949318"
---
# <a name="authentication-bits"></a>Authentifizierung (Bits)

Bits unterstützt die Standard Authentifizierung, die Passport-Authentifizierung und mehrere Challenge/Response-Authentifizierungs Schemas. Wenn für den Server oder Proxy eine Benutzerauthentifizierung erforderlich ist, verwenden Sie die Funktion [**IBackgroundCopyJob2:: setanmelde**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) Informationen, um die Anmelde Informationen des Benutzers anzugeben. Bits verwendet die [CryptoAPI](/windows/desktop/SecCrypto/cryptography-portal) , um die Anmelde Informationen zu schützen.

Zum Festlegen von Anmelde Informationen für die Standard Authentifizierung verwenden Sie die Funktion " [**setanmelde**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) ", um den Benutzernamen und das Kennwort anzugeben Sie sollten die Standard Authentifizierung nur mit geschützten sicheren Websites von https://verwenden. Andernfalls sind der Benutzername und das Kennwort für Benutzer sichtbar. 

Es ist möglich, den Benutzernamen und das Kennwort in die URL einzubetten. Dies gilt nicht als bewährte Sicherheitsmaßnahme und wird in RFC 3986 (Abschnitt 3.2.1) als veraltet eingestuft.

Bei der [Passport](/windows/desktop/WinHttp/passport-authentication-in-winhttp) -Authentifizierung unterstützt Bits nur explizite Anmelde Informationen, keine impliziten Anmelde Informationen, die mit dem Konto verknüpft sind.

Bei der Challenge/Response-Authentifizierung nimmt Bits die Identität des Benutzers an und verwendet " [snego](../com/snego.md) ", um zu bestimmen, welche Challenge/Response-Authentifizierung verwendet werden soll, z. b. NTLM oder das Kerberos Eine Liste der von Bits unterstützten Challenge/Response-Schemas finden Sie unter [**BG \_ auth \_ Scheme**](/windows/desktop/api/Bits1_5/ne-bits1_5-bg_auth_scheme).

BITS-Aufträge können fehlschlagen, wenn das virtuelle Verzeichnis auf dem Server die anonyme Authentifizierung und ein anderes Authentifizierungsschema aktiviert ist und wenn ACLs das virtuelle Verzeichnis schützen oder Dateien herunterladen. Ein Auftrag schlägt z. b. mit "Zugriff verweigert" fehl, wenn die anonyme und integrierte Authentifizierung für das virtuelle Verzeichnis aktiviert ist und die Datei eine ACL enthält, mit der nur Ben die Datei lesen kann. Dies liegt daran, dass das virtuelle Verzeichnis den anonymen Zugriff zulässt, sodass IIS nicht explizit von Ben authentifiziert wird (die Anmelde Informationen von Ben werden nicht für den Zugriff auf die Datei verwendet, und der Zugriff wird verweigert).

## <a name="using-implicit-credentials"></a>Verwenden von impliziten Anmelde Informationen

Um die impliziten Anmelde Informationen (Anmelde Informationen) für die NTLM-oder Kerberos-Authentifizierung zu verwenden, müssen Sie die [**IBackgroundCopyJob2:: SetLogon**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) -Methode aufrufen und die Member " **username** " und " **Password** " der [**BG- \_ Basis \_ Anmelde**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_basic_credentials) Informationen auf **null** festlegen. Wenn Sie implizite Anmelde Informationen für einen Proxy angeben, verwendet Bits auch die impliziten Anmelde Informationen für die Server Authentifizierung, es sei denn, Sie geben explizite Server Anmelde Informationen an.

Weitere Informationen zu Diensten finden Sie unter [Dienst Konten und Bits](service-accounts-and-bits.md).

Sie können auch den Registrierungs Wert **LMCompatibilityLevel** oder **UseLmCompat** ändern; Sie sollten diese Werte jedoch nur ändern, wenn Sie eine vorhandene Anwendung haben, die nicht zum Aufrufen der [**setanmelde**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) -Methode geändert werden kann.

Bits verwendet implizite Anmelde Informationen für die Authentifizierung, wenn der Registrierungs Wert **LMCompatibilityLevel** zwei oder mehr ist, und Sie haben die [**setanmelde**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) -Methode nicht aufgerufen. Der vollständige Pfad zum Registrierungs Wert **LMCompatibilityLevel** ist **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **LSA** \\ **LMCompatibilityLevel**.

Beachten Sie, dass sich das Ändern des Registrierungs Werts **LMCompatibilityLevel** auf andere Anwendungen und Dienste auswirken kann, die auf dem Computer ausgeführt werden. Weitere Informationen zur Verwendung des Registrierungs Werts **LMCompatibilityLevel** finden Sie unter [KB147706](https://support.microsoft.com/kb/147706).

Wenn das Festlegen des Registrierungs Werts **LMCompatibilityLevel** ein Problem ist, können Sie den Registrierungs Wert **UseLmCompat** unter **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Bits** erstellen. Der Registrierungs Wert ist ein DWORD-Wert. In der folgenden Tabelle sind die möglichen Werte für **UseLmCompat** aufgeführt:

|Wert|BESCHREIBUNG|
|-|-|
| 0     | Bits sendet implizite Anmelde Informationen, wenn der Server zur Eingabe von NTLM-oder Kerberos-Anmelde Informationen auffordert.                                                                                           |
| 1     | Bits sendet implizite Anmelde Informationen nur dann, wenn der **LMCompatibilityLevel** -Registrierungs Wert des Client Computers größer oder gleich 2 ist.<br/>     |
| 2     | Bits sendet implizite Anmelde Informationen nur dann, wenn die Anwendung die [**setanmelde**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) -Methode aufgerufen hat.<br/> |

Bits verwendet den Standardwert "2" für den Registrierungs Wert " **UseLmCompat** ", wenn der Registrierungs Wert nicht vorhanden ist.

## <a name="using-certificates-for-clientserver-authentication"></a>Verwenden von Zertifikaten für die Client-/Serverauthentifizierung

Bei der sicheren Client-/Serverkommunikation können Clients und Server digitale Zertifikate verwenden, um sich gegenseitig zu authentifizieren. Bits unterstützt automatisch die Zertifikat basierte Server Authentifizierung für sichere HTTP-Transporte. Um Bits das Client Zertifikat für die gegenseitige Authentifizierung bereitzustellen, müssen Sie entweder die [**ibackgroundcopyjobhttpoptions:: setclientcertificatebyid**](/windows/desktop/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyid) -Methode oder die [**ibackgroundcopyjobhttpoptions:: setclientcertificatebyname**](/windows/desktop/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyname) -Methode aufrufen.

Wenn eine Website akzeptiert, aber kein SSL-Client Zertifikat benötigt, und der BITS-Auftrag kein Client Zertifikat angibt, schlägt der Auftrag mit dem **Fehler " \_ WinHTTP-Client Authentifizierungszertifikat \_ \_ \_ \_ erforderlich** " (0x80072f0c) fehl.

## <a name="how-to-handle-authenticated-proxy-scenarios-that-require-user-specific-settings"></a>Behandeln von authentifizierten Proxy Szenarien, die benutzerspezifische Einstellungen erfordern

Wenn Sie Bits in einer Umgebung verwenden, die bei Ausführung als Konto ohne verwendbare NTLM-oder Kerberos-Anmelde Informationen in der Netzwerk Domäne des Computers eine Proxy Authentifizierung erfordert, müssen Sie zusätzliche Schritte ausführen, um die Authentifizierung mithilfe der Anmelde Informationen eines anderen Benutzerkontos, das über Anmelde Informationen für die Domäne verfügt, ordnungsgemäß durchführen zu können. Dies ist ein typisches Szenario, wenn Ihr Bits-Code als Systemdienst wie LocalService, Network Service oder LocalSystem ausgeführt wird, da diese Konten keine verwendbaren NTLM-oder Kerberos-Anmelde Informationen aufweisen.

Die in Bits verwendete Proxy Erkennungs Logik führt Folgendes aus, wenn ein Netzwerk-Hilfstoken (BG \_ Token \_ Network) festgelegt ist:

-   Wenn [**ibackgroundcopyjob:: setproxysettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) mit der präconfig-Datei für die **Verwendung von BG- \_ Auftrags \_ Proxys \_ \_** aufgerufen wurde, lesen Sie die lokalen Internet Explorer-Proxy Einstellungen mithilfe von [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser). Ab Windows 10, Version 1809 (10,0; Build 17763), die hilfstokenidentität wird für diesen Schritt verwendet.
-   Wenn [**ibackgroundcopyjob:: setproxysettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) mit der automatischen **Erkennung der BG- \_ Proxy \_ Verwendung \_** aufgerufen wurde oder wenn die IE-Einstellungen aus dem Fall der **\_ \_ \_ \_ präconfig-Verwendung der BG-Auftrags Proxy Verwendung** die automatische Erkennung oder eine URL für die automatische Konfiguration angeben, führen Sie die automatische Proxy Erkennung oder das WPAD (Web Proxy Autodiscovery Protocol) mithilfe von " [**winhttpgetpro**](/windows/desktop/api/winhttp/nf-winhttp-winhttpgetproxyforurl)

Danach wird der Identitätswechsel des hilfstokendiensts für die Proxy-oder Server Authentifizierung verwendet.

Ab Windows 10, Version 1809 (10,0; Build 17763), das authentifizierte Proxy Szenario mit benutzerspezifischen Anmelde Informationen wird vereinfacht.

1.  Aufrufen der [**setanmelde**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) -Methode des Bits-Auftrags mit dem **BG \_ auth- \_ Schema \_ aushandeln**, dem auf **null** festgelegten *Benutzernamen* , dem auf **null** festgelegten *Kennwort* und dem *Ziel* auf den **BG \_ auth- \_ Ziel \_ Proxy**. Dies bewirkt, dass die impliziten Anmelde Informationen des Benutzerkontos für die NTLM-und Kerberos-Authentifizierung mit dem Proxy und dem Server verwendet werden.
2.  Rufen Sie [**ibackgroundcopyjob:: setproxysettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) mit der **\_ \_ \_ \_ präconfig**-Datei für die Verwendung von BG Job Proxy auf.
3.  QueryInterface für [**ibitstokenoptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions).
4.  Verwenden Sie die Identität des Benutzerkontos, das Sie für NTLM/Kerberos-Anmelde Informationen verwenden.
5.  Ruft [**"**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken)*" auf.
6. Nennen Sie "einstellungsflags" mit dem **BG- \_ \_ tokennetzwerk**. [](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags)
7. Identitätswechsel zurücksetzen.
8. Auftrags Einrichtung fortsetzen.
9. Der Vorgang [**wird für den**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) Auftrag fortgesetzt.

Vor Windows 10, Version 1809 (10,0; Build 17763), die korrekte Benutzeridentität (die Identität des hilfstokentokens) wird für die netzwerkbasierte Proxy Erkennung (WPAD) und für die Proxy Authentifizierung verwendet, aber die tatsächliche Erkennung der lokalen Proxy Einstellungen erfolgt immer über das Token des Auftrags Besitzers, auch wenn ein Hilfstoken konfiguriert ist. Um dieses Problem zu umgehen, können Sie die folgenden Schritte ausführen.

1.  Verwenden Sie die Identität des Benutzerkontos, das Sie für NTLM/Kerberos-Anmelde Informationen verwenden.
2.  Rufen Sie die Internet Explorer-Proxy Einstellungen des Benutzerkontos durch Aufrufen von [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)ab.
3.  Identitätswechsel zurücksetzen.
4.  Aufrufen der [**setanmelde**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) -Methode des Bits-Auftrags mit dem **BG \_ auth- \_ Schema \_ aushandeln**, dem auf **null** festgelegten *Benutzernamen* , dem auf **null** festgelegten *Kennwort* und dem *Ziel* auf den **BG \_ auth- \_ Ziel \_ Proxy**. Dies bewirkt, dass die impliziten Anmelde Informationen des Benutzerkontos für die NTLM-und Kerberos-Authentifizierung mit dem Proxy und dem Server verwendet werden.
5.  Wenn Schritt 2 benutzerspezifische Proxy Einstellungen (d. h. *lpszProxy* oder *lpszProxyBypass* sind nicht **null**) zurückgegeben hat, legen Sie die entsprechenden Auftrags Einstellungen manuell fest, indem Sie [**setproxysettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) mit der Außerkraftsetzungs Einstellung für die **BG- \_ Auftrags \_ Proxy \_ Verwendung \_** verwenden.
6.  Wenn in Schritt 2 keine benutzerspezifischen Proxy Einstellungen vorhanden sind, rufen Sie [**setproxysettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) mit **der \_ \_ \_ Vorkonfiguration der BG-Auftrags Verwendung** auf.
7.  QueryInterface für [**ibitstokenoptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions).
8.  Nimmt die Identität des Benutzerkontos erneut an.
9.  Ruft [**"**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken)*" auf.
10. Nennen Sie "einstellungsflags" mit dem **BG- \_ \_ tokennetzwerk**. [](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags)
11. Identitätswechsel zurücksetzen.
12. Auftrags Einrichtung fortsetzen.
13. Der Vorgang [**wird für den**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) Auftrag fortgesetzt.
