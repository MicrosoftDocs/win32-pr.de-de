---
title: Authentifizierung (BITS)
description: BITS unterstützt die Standardauthentifizierung, die Passport-Authentifizierung und mehrere Authentifizierungsschemas für Herausforderungen/Antworten.
ms.assetid: cfd4aec3-79d0-4971-93f8-df797e5c0f75
ms.topic: article
ms.date: 10/09/2018
ms.openlocfilehash: 9cb3d50f6689ed28889c68388969c1cb7d06ea912bc5d5ed4384f45a4e740f79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021288"
---
# <a name="authentication-bits"></a>Authentifizierung (BITS)

BITS unterstützt die Standardauthentifizierung, die Passport-Authentifizierung und mehrere Authentifizierungsschemas für Herausforderungen/Antworten. Wenn der Server oder Proxy eine Benutzerauthentifizierung erfordert, verwenden Sie die [**IBackgroundCopyJob2::SetCredentials-Funktion,**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) um die Anmeldeinformationen des Benutzers anzugeben. BITS verwendet die [CryptoAPI,](/windows/desktop/SecCrypto/cryptography-portal) um die Anmeldeinformationen zu schützen.

Verwenden Sie zum Festlegen von Anmeldeinformationen für die Standardauthentifizierung die [**Funktion SetCredentials,**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) um den Benutzernamen und das Kennwort anzugeben. Sie sollten die Standardauthentifizierung nur mit geschützten https:// verwenden. Andernfalls sind Benutzername und Kennwort für Benutzer sichtbar. 

Es ist möglich, den Benutzernamen und das Kennwort in die URL einbetten. Dies gilt nicht als bewährte Sicherheitsmaßnahmen und ist in RFC 3986 (Abschnitt 3.2.1) veraltet.

Für [die Passport-Authentifizierung](/windows/desktop/WinHttp/passport-authentication-in-winhttp) unterstützt BITS nur explizite Anmeldeinformationen, keine impliziten Anmeldeinformationen, die an das Konto gebunden sind.

Für die Abfrage-/Antwortauthentifizierung wird von BITS die Identität des Benutzers angenommen und [Snego](../com/snego.md) verwendet, um zu bestimmen, welche Abfrage-/Antwortauthentifizierung verwendet werden soll, z. B. NTLM oder das Kerberos-Protokoll. Eine Liste der Von BITS unterstützten Challenge/Response-Schemas finden Sie unter [**BG \_ AUTH \_ SCHEME**](/windows/desktop/api/Bits1_5/ne-bits1_5-bg_auth_scheme).

BITS-Aufträge können fehlschlagen, wenn für das virtuelle Verzeichnis auf dem Server anonyme Authentifizierung und ein anderes Authentifizierungsschema aktiviert ist und ACLs das virtuelle Verzeichnis schützen oder Dateien herunterladen. Beispielsweise schlägt ein Auftrag mit "Zugriff verweigert" fehl, wenn für das virtuelle Verzeichnis die anonyme und integrierte Authentifizierung aktiviert ist und die Datei eine Zugriffssteuerungsliste enthält, mit der nur Ben die Datei lesen kann. Dies tritt auf, weil das virtuelle Verzeichnis anonymen Zugriff zulässt, sodass IIS Ben nicht explizit authentifiziert (bens Anmeldeinformationen werden nicht für den Zugriff auf die Datei verwendet, und der Zugriff wird verweigert).

## <a name="using-implicit-credentials"></a>Verwenden impliziter Anmeldeinformationen

Um die impliziten Anmeldeinformationen des Benutzers für die NTLM- oder Kerberos-Authentifizierung zu verwenden, rufen Sie die [**IBackgroundCopyJob2::SetCredentials-Methode**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) auf, und legen Sie die **Member UserName** und **Password** der [**BG BASIC \_ \_ CREDENTIALS-Struktur**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_basic_credentials) auf **NULL** fest. Wenn Sie implizite Anmeldeinformationen für einen Proxy angeben, verwendet BITS auch die impliziten Anmeldeinformationen für die Serverauthentifizierung, es sei denn, Sie geben explizite Serveranmeldeinformationen an.

Weitere Informationen zu Diensten finden Sie unter [Dienstkonten und BITS](service-accounts-and-bits.md).

Sie können auch den **Registrierungswert LMCompatibilityLevel** oder **UseLMCompat** ändern. Sie sollten diese Werte jedoch nur ändern, wenn Sie über eine vorhandene Anwendung verfügen, die nicht zum Aufrufen der [**SetCredentials-Methode geändert werden**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) kann.

BITS verwendet implizite Anmeldeinformationen für die Authentifizierung, wenn der **Registrierungswert LMCompatibilityLevel** zwei oder höher ist und Sie die [**SetCredentials-Methode nicht aufgerufen**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) haben. Der vollständige Pfad zum **Registrierungswert LMCompatibilityLevel** ist **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **LSA** \\ **LmCompatibilityLevel.**

Beachten Sie, dass sich das **Ändern des Registrierungswerts LMCompatibilityLevel** auf andere Anwendungen und Dienste auswirken kann, die auf dem Computer ausgeführt werden. Weitere Informationen zur Verwendung des **Registrierungswerts LMCompatibilityLevel** finden Sie unter [KB147706](https://support.microsoft.com/kb/147706).

Wenn das Festlegen **des Registrierungswerts LMCompatibilityLevel** ein Problem ist, können Sie den **UseLMCompat-Registrierungswert** unter **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **BITS erstellen.** Der Registrierungswert ist ein DWORD. In der folgenden Tabelle sind die möglichen Werte für **UseLMCompat aufgeführt:**

|Wert|Beschreibung|
|-|-|
| 0     | BITS sendet implizite Anmeldeinformationen, wenn der Server zur Eingabe von NTLM- oder Kerberos-Anmeldeinformationen aufgefordert wird.                                                                                           |
| 1     | BITS sendet implizite Anmeldeinformationen nur, wenn der **LMCompatibilityLevel-Registrierungswert** des Clientcomputers größer oder gleich 2 ist.<br/>     |
| 2     | BITS sendet implizite Anmeldeinformationen nur, wenn die Anwendung die [**SetCredentials-Methode aufgerufen**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) hat.<br/> |

BITS verwendet den Standardwert "2" für den **UseLMCompat-Registrierungswert,** wenn der Registrierungswert nicht vorhanden ist.

## <a name="using-certificates-for-clientserver-authentication"></a>Verwenden von Zertifikaten für die Client-/Serverauthentifizierung

Bei der sicheren Client-/Serverkommunikation können Clients und Server digitale Zertifikate verwenden, um sich gegenseitig zu authentifizieren. BITS unterstützt automatisch die zertifikatbasierte Serverauthentifizierung für sichere HTTP-Transporte. Rufen Sie entweder die [**IBackgroundCopyJobHttpOptions::SetClientCertificateByID-**](/windows/desktop/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyid) oder [**IBackgroundCopyJobHttpOptions::SetClientCertificateByName-Methode**](/windows/desktop/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyname) auf, um BITS für das Clientzertifikat für die gegenseitige Authentifizierung bereitstellen zu können.

Wenn eine Website ein SSL-Clientzertifikat akzeptiert, aber nicht erfordert und der BITS-Auftrag kein Clientzertifikat an gibt, tritt für den Auftrag ein Fehler mit DEM FEHLER **\_ WINHTTP \_ CLIENT \_ \_ AUTH CERT \_ NEEDED** (0x80072f0c) auf.

## <a name="how-to-handle-authenticated-proxy-scenarios-that-require-user-specific-settings"></a>Behandeln authentifizierter Proxyszenarien, die benutzerspezifische Einstellungen erfordern

Wenn Sie BITS in einer Umgebung verwenden, die eine Proxyauthentifizierung erfordert, während sie als Konto ohne nutzbare NTLM- oder Kerberos-Anmeldeinformationen in der Netzwerkdomäne des Computers ausgeführt wird, müssen Sie zusätzliche Schritte ausführen, um sich ordnungsgemäß mit den Anmeldeinformationen eines anderen Benutzerkontos zu authentifizieren, das über Anmeldeinformationen für die Domäne verfügt. Dies ist ein typisches Szenario, wenn Ihr BITS-Code als Systemdienst wie LocalService, NetworkService oder LocalSystem ausgeführt wird, da diese Konten nicht über nutzbare NTLM- oder Kerberos-Anmeldeinformationen verfügen.

Die in BITS verwendete Proxyerkennungslogik führt folgende Schritte aus, wenn ein Netzwerk-Hilfstoken (BG \_ TOKEN \_ NETWORK) festgelegt ist:

-   Wenn [**IBackgroundCopyJob::SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) mit **BG JOB PROXY USAGE \_ \_ \_ \_ PRECONFIG** aufgerufen wurde, lesen Sie lokale IE-Proxyeinstellungen mithilfe des Tokenkontextwechsels des Auftragsbesitzers über [**WinHttpGetIEProxyConfigForCurrentUser.**](/windows/desktop/api/winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) Ab Windows 10, Version 1809 (10.0; Build 17763), wird die Hilfstokenidentität für diesen Schritt verwendet.
-   Wenn [**IBackgroundCopyJob::SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) mit **BG PROXY USAGE \_ \_ \_ AUTODETECT** aufgerufen wurde oder die IE-Einstellungen aus dem **\_ \_ \_ \_ PRECONFIG-Fall BG JOB PROXY USAGE** auto-detect oder eine AUTOCONFIG-URL angeben, führen Sie die automatische Proxyerkennung oder das Web Proxy Autodiscovery Protocol (WPAD) mithilfe des Identitätswechsels von Hilfstoken über [**WinHttpGetProxyForUrl**](/windows/desktop/api/winhttp/nf-winhttp-winhttpgetproxyforurl)durch.

Danach wird der Identitätswechsel des Hilfstokens für die Proxy- oder Serverauthentifizierung verwendet.

Ab Windows 10, Version 1809 (10.0; Build 17763): Das Szenario mit authentifizierten Proxys mit benutzerspezifischen Anmeldeinformationen wird vereinfacht.

1.  Rufen Sie die [**SetCredentials-Methode**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) des BITS-Auftrags auf, bei der **BG \_ AUTH \_ SCHEME \_ NEGOTIATE,** *UserName* auf **NULL,** *Password* auf **NULL** und *Target* auf **BG \_ AUTH TARGET PROXY festgelegt \_ \_ ist.** Dies bewirkt, dass die impliziten Anmeldeinformationen des Benutzerkontos für die NTLM- und Kerberos-Authentifizierung beim Proxy und Server verwendet werden.
2.  Rufen [**Sie IBackgroundCopyJob::SetProxySettings mit**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) BG JOB PROXY USAGE **\_ \_ \_ \_ PRECONFIG auf.**
3.  QueryInterface für [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions).
4.  Geben Sie die Identität des Benutzerkontos an, das Sie für NTLM-/Kerberos-Anmeldeinformationen verwenden.
5.  Rufen Sie [**SetHelperToken auf.**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken)
6. Rufen [**Sie SetHelperTokenFlags mit**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) BG TOKEN NETWORK **\_ \_ auf.**
7. Änderst du den Identitätswechsel.
8. Setzen Sie die Auftragseinrichtung fort.
9. Rufen [**Sie Für**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) den Auftrag fortsetzen auf.

Vor Windows 10, Version 1809 (10.0; Build 17763), die richtige Benutzeridentität (die Identität des Hilfstokens) wird für die netzwerkbasierte Proxyerkennung (WPAD) und für die Proxyauthentifizierung verwendet. Die tatsächliche Erkennung lokaler Proxyeinstellungen (IE) erfolgt jedoch immer mithilfe des Token des Auftragsbesitzers, selbst wenn ein Hilfstoken konfiguriert ist. Um diesen Nachteil zu beheben, können Sie diese Schritte ausführen.

1.  Geben Sie die Identität des Benutzerkontos an, das Sie für NTLM-/Kerberos-Anmeldeinformationen verwenden.
2.  Rufen Sie die IE-Proxyeinstellungen des Benutzerkontos ab, indem [**Sie WinHttpGetIEProxyConfigForCurrentUser aufrufen.**](/windows/desktop/api/winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)
3.  Änderst du den Identitätswechsel.
4.  Rufen Sie die [**SetCredentials-Methode**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) des BITS-Auftrags auf, bei der **BG \_ AUTH \_ SCHEME \_ NEGOTIATE,** *UserName* auf **NULL,** *Password* auf **NULL** und *Target* auf **BG \_ AUTH TARGET PROXY festgelegt \_ \_ ist.** Dies bewirkt, dass die impliziten Anmeldeinformationen des Benutzerkontos für die NTLM- und Kerberos-Authentifizierung beim Proxy und Server verwendet werden.
5.  Wenn Schritt 2 benutzerspezifische Proxyeinstellungen ergeben hat (d.h. *lpszProxy* oder *lpszProxyBypass* sind nicht **NULL),** legen Sie die entsprechenden Auftragseinstellungen manuell fest, indem [**Sie SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) mit der EINSTELLUNG AUßERKRAFTSETZUNG der **BG JOB PROXY \_ \_ \_ \_ USAGE** verwenden.
6.  Wenn Schritt 2 keine benutzerspezifischen Proxyeinstellungen ergeben hat, rufen Sie [**SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) mit **BG JOB USAGE \_ \_ \_ PRECONFIG auf.**
7.  QueryInterface für [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions).
8.  Identität des Benutzerkontos erneut angenommen.
9.  Rufen Sie [**SetHelperToken auf.**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken)
10. Rufen [**Sie SetHelperTokenFlags mit**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) BG TOKEN NETWORK **\_ \_ auf.**
11. Änderst du den Identitätswechsel.
12. Setzen Sie die Auftragseinrichtung fort.
13. Rufen [**Sie Für**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) den Auftrag fortsetzen auf.
