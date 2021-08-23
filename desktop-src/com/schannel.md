---
title: Schannel
description: Das Sicherheitspaket Secure Channel (Schannel), dessen Authentifizierungsdienstbezeichner RPC \_ C \_ AUTHN \_ GSS \_ SCHANNEL lautet, unterstützt die folgenden ssl-basierten Protokolle mit öffentlichem Schlüssel (Secure Sockets Layer) Version 2.0 und 3.0, Transport Layer Security (TLS) 1.0 und Private Communication Technology (PCT) 1.0. TLS 1.0 ist eine standardisierte, leicht geänderte Version von SSL 3.0, die von der Internet Engineering Task Force (IETF) im Januar 1999 im Dokument RFC 2246 ausgegeben wurde. Da TLS standardisiert wurde, wird Entwicklern empfohlen, TLS anstelle von SSL zu verwenden. PCT ist nur aus Gründen der Abwärtskompatibilität enthalten und sollte nicht für die Neuentwicklung verwendet werden. Wenn das Schannel-Sicherheitspaket verwendet wird, handelt DCOM abhängig von den Client- und Serverfunktionen automatisch das beste Protokoll aus.
ms.assetid: 03a5f987-f668-4f19-9b58-d62711f58734
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ab40ed9d87013f646137e23ccc755dfdf9ab6b8f2ded367940b4ae630d7b4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047848"
---
# <a name="schannel"></a>Schannel

Das Sicherheitspaket Secure Channel (Schannel), dessen Authentifizierungsdienstbezeichner RPC \_ C \_ AUTHN \_ GSS \_ SCHANNEL lautet, unterstützt die folgenden Protokolle mit öffentlichem Schlüssel: SSL(Secure Sockets Layer) Versionen 2.0 und 3.0, Transport Layer Security (TLS) 1.0 und Private Communication Technology (PCT) 1.0. TLS 1.0 ist eine standardisierte, leicht geänderte Version von SSL 3.0, die von der Internet Engineering Task Force (IETF) im Januar 1999 im Dokument [RFC 2246](https://www.ietf.org/rfc/rfc2246.txt)ausgegeben wurde. Da TLS standardisiert wurde, wird Entwicklern empfohlen, TLS anstelle von SSL zu verwenden. PCT ist nur aus Gründen der Abwärtskompatibilität enthalten und sollte nicht für die Neuentwicklung verwendet werden. Wenn das Schannel-Sicherheitspaket verwendet wird, handelt DCOM abhängig von den Client- und Serverfunktionen automatisch das beste Protokoll aus.

In den folgenden Themen werden das TLS-Protokoll und seine Funktionsweise mit DCOM kurz beschrieben.

-   [Verwendung von TLS](#when-to-use-tls)
-   [Kurze Übersicht über die Funktionsweise von TLS](#brief-overview-of-how-tls-works)
-   [X.509-Zertifikate](#x509-certificates)
    -   [Clientzertifikate](#client-certificates)
-   [Verwenden von TLS in COM](#using-tls-in-com)
    -   [So legt ein Server die Sicherheitssicherheit fest](#how-a-server-sets-the-security-blanket)
    -   [So legt ein Client den Sicherheitsvorsatz fest](#how-a-client-sets-the-security-blanket)
    -   [Ändern der Sicherheit durch einen Client](#how-a-client-changes-the-security-blanket)
    -   [Beispiel: Client ändert die Sicherheitslage](#example-client-changes-the-security-blanket)
-   [Zugehörige Themen](#related-topics)

> [!Note]  
> Alle Informationen zum TLS-Protokoll in diesen Abschnitten gelten auch für die PROTOKOLLE SSL und PCT.

 

## <a name="when-to-use-tls"></a>Verwendung von TLS

TLS ist die einzige verfügbare Sicherheitsoption, wenn Server ihre Identität anonymen Clients nachweisen müssen. Dies ist besonders wichtig für Websites, die am E-Commerce teilnehmen möchten, da sie die Übertragung vertraulicher Informationen wie Kreditkartennummern schützen. TLS stellt sicher, dass die E-Commerce-Kunden sicher sein können, mit wem sie Geschäfte machen, da ihnen der Nachweis der Serveridentität erteilt wird. Außerdem erhält der E-Commerce-Server die Effizienz, sich nicht mit der Authentifizierung der Identität der einzelnen Kunden befassen zu müssen.

TLS erfordert, dass alle Server ihre Identität gegenüber Clients nachweisen. Darüber hinaus bietet TLS die Möglichkeit, dass Clients ihre Identität gegenüber Servern nachweisen können. Diese gegenseitige Authentifizierung kann nützlich sein, um den Zugriff auf bestimmte Webseiten in einem großen Unternehmensintranet einzuschränken.

TLS unterstützt die stärksten Authentifizierungsebenen und bietet eine offene Architektur, die es ermöglicht, die Verschlüsselungsstärke im Laufe der Zeit zu erhöhen, um mit technologischen Innovationen Schritt zu halten. TLS ist die beste Wahl für Umgebungen, in denen für die Daten während der Übertragung die höchste Sicherheitsstufe gewünscht wird.

## <a name="brief-overview-of-how-tls-works"></a>Kurze Übersicht über die Funktionsweise von TLS

TLS basiert auf einer Public Key-Infrastruktur (PKI), die öffentliche/private Schlüsselpaare zum Aktivieren der Datenverschlüsselung und zum Einrichten der Datenintegrität verwendet und X.509-Zertifikate für die Authentifizierung verwendet.

Viele Sicherheitsprotokolle, z. B. das Kerberos v5-Protokoll, hängen von einem einzelnen Schlüssel ab, um Daten zu verschlüsseln und zu entschlüsseln. Solche Protokolle hängen daher vom sicheren Austausch von Verschlüsselungsschlüsseln ab. Im Kerberos-Protokoll erfolgt dies über Tickets, die vom Schlüsselverteilungscenter (KDC) abgerufen werden. Dies erfordert, dass alle Benutzer, die das Kerberos-Protokoll verwenden, beim KDC registriert werden. Dies wäre eine unpraktische Einschränkung für einen E-Commerce-Webserver, der Millionen von Kunden aus der ganzen Welt gewinnen soll. TLS basiert daher auf einer PKI, die zwei Schlüssel für die Datenverschlüsselung verwendet, wenn ein Schlüssel des Paars die Daten verschlüsselt, kann nur der andere Schlüssel des Paars diese entschlüsseln. Der Hauptvorteil dieses Entwurfs besteht darin, dass die Verschlüsselung ohne sicheren Austausch von Verschlüsselungsschlüsseln erfolgen kann.

Eine PKI verwendet eine Technik, bei der einer der Schlüssel privat gehalten wird und nur für den Prinzipal verfügbar ist, für den er registriert ist, während der andere Schlüssel für jeden zugänglich gemacht wird. Wenn jemand eine private Nachricht an den Besitzer eines Schlüsselpaars senden möchte, kann die Nachricht mit dem öffentlichen Schlüssel verschlüsselt werden, und nur der private Schlüssel kann zum Entschlüsseln der Nachricht verwendet werden.

Schlüsselpaare werden auch verwendet, um die Integrität der gesendeten Daten zu überprüfen. Hierzu kann der Besitzer des Schlüsselpaars vor dem Senden eine digitale Signatur an die Daten anfügen. Das Erstellen einer digitalen Signatur umfasst das Berechnen eines Hashs der Daten und das Verschlüsseln des Hashs mit dem privaten Schlüssel. Jeder, der den öffentlichen Schlüssel zum Entschlüsseln der digitalen Signatur verwendet, ist sicher, dass die digitale Signatur nur von der Person stammen darf, die den privaten Schlüssel besitzt. Darüber hinaus kann der Empfänger einen Hash der Daten mit demselben Algorithmus wie der Absender berechnen. Wenn der berechnete Hash mit dem in der digitalen Signatur gesendeten Hash übereinstimmt, kann der Empfänger sicher sein, dass die Daten nach der digitalen Signatur nicht geändert wurden.

Ein Nachteil der Verwendung einer PKI für die Datenverschlüsselung mit hohem Volumen ist die relativ langsame Leistung. Aufgrund der intensiven Mathematik kann die Verschlüsselung und Entschlüsselung von Daten mithilfe einer asymmetrischen Verschlüsselung, die von einem Schlüsselpaar abhängt, bis zu 1.000-mal langsamer sein als die Verschlüsselung und Entschlüsselung mithilfe eines symmetrischen Verschlüsselungsverfahren, das nur von einem einzelnen Schlüssel abhängt. TLS verwendet daher eine PKI nur zum Generieren digitaler Signaturen und zum Aushandeln des sitzungsspezifischen einzelnen Schlüssels, der sowohl vom Client als auch vom Server für die Verschlüsselung und Entschlüsselung von Massendaten verwendet wird. TLS unterstützt eine Vielzahl von symmetrischen Einzelschlüsselchiffren, und in Zukunft können weitere Verschlüsselungen hinzugefügt werden.

Weitere Informationen zum TLS-Handshakeprotokoll finden Sie unter [TLS Handshake-Protokoll.](/windows/desktop/SecAuthN/tls-handshake-protocol)

Weitere Informationen zur Kryptografie hinter dem TLS-Protokoll finden Sie unter [Cryptography Essentials](/windows/desktop/SecCrypto/cryptography-essentials).

## <a name="x509-certificates"></a>X.509-Zertifikate

Ein kritisches Problem, das von einer PKI behandelt werden muss, ist die Fähigkeit, der Authentizität des verwendeten öffentlichen Schlüssels zu vertrauen. Wenn Sie einen öffentlichen Schlüssel verwenden, der für ein Unternehmen ausgestellt wurde, mit dem Sie Geschäfte machen möchten, möchten Sie sicher sein, dass der Schlüssel tatsächlich zum Unternehmen gehört, anstatt zu einem Schläger, der Ihre Kreditkartennummer ermitteln möchte.

Um die Identität eines Prinzipals mit einem Schlüsselpaar zu gewährleisten, wird dem Prinzipal von einer Zertifizierungsstelle ein X.509-Zertifikat ausgestellt. Dieses Zertifikat enthält Informationen, die den Prinzipal identifizieren, den öffentlichen Schlüssel des Prinzipals enthalten und von der Zertifizierungsstelle digital signiert werden. Diese digitale Signatur gibt an, dass die Zertifizierungsstelle der Meinung ist, dass der im Zertifikat enthaltene öffentliche Schlüssel tatsächlich zu dem prinzipalen Schlüssel gehört, der durch das Zertifikat identifiziert wird.

Und wie vertrauen Sie der Zertifizierungsstelle? Da die Zertifizierungsstelle selbst über ein X.509-Zertifikat verfügt, das von einer höheren Zertifizierungsstelle signiert wurde. Diese Kette von Zertifikatsignaturen wird fortgesetzt, bis sie eine Stammzertifizierungsstelle erreicht, bei der es sich um eine Zertifizierungsstelle handelt, die ihre eigenen Zertifikate signiert. Wenn Sie der Integrität der Stammzertifizierungsstelle eines Zertifikats vertrauen, sollten Sie der Authentizität des Zertifikats selbst vertrauen können. Daher ist die Auswahl von Stammzertifizierungsstellen, denen Sie vertrauen möchten, eine wichtige Aufgabe für einen Systemadministrator.

### <a name="client-certificates"></a>Clientzertifikate

Als sicherheitliche Transportebenenprotokolle zum ersten Mal auftraten, bestand ihr Hauptzweck darin, sicherzustellen, dass ein Client eine Verbindung mit einem authentifikatorischen Server herstellte und dabei half, den Datenschutz während der Übertragung zu schützen. SSL 3.0 und TLS 1.0 enthalten jedoch auch Unterstützung für die Übertragung eines Clientzertifikats während des Handshakes des Protokolls. Dieses optionale Feature ermöglicht die gegenseitige Authentifizierung von Client und Server.

Die Entscheidung, ob ein Clientzertifikat verwendet werden soll, sollte im Kontext der Anwendung getroffen werden. Clientzertifikate sind nicht erforderlich, wenn die primäre Anforderung die Authentifizierung des Servers ist. Wenn die Clientauthentifizierung jedoch wichtig ist, kann das Zertifikat eines Clients verwendet werden, anstatt sich auf die benutzerdefinierte Authentifizierung innerhalb der Anwendung zu verlassen. Die Verwendung von Clientzertifikaten ist der benutzerdefinierten Authentifizierung vorzuziehen, da sie Benutzern ein Szenario mit einmaligem Anmelden bietet.

## <a name="using-tls-in-com"></a>Verwenden von TLS in COM

TLS unterstützt nur die Identitätswechselebene (RPC \_ C \_ IMP \_ LEVEL \_ IMPERSONATE). Wenn COM TLS als Authentifizierungsdienst auf einem Proxy aushandelt, legt COM die Identitätswechselebene so fest, dass die Identität unabhängig vom Prozessstandard angenommen wird. Damit der Identitätswechsel in TLS ordnungsgemäß funktioniert, muss der Client dem Server ein X.509-Zertifikat bereitstellen, und auf dem Server muss dieses Zertifikat einem bestimmten Benutzerkonto auf dem Server zugeordnet sein. Weitere Informationen finden Sie in der [schrittweisen Anleitung zum Zuordnen von Zertifikaten zu Benutzerkonten.](https://www.microsoft.com/isapi/redir.dll?prd=windows2000&sbp=technicallibrary&ar=security&sba=mappingcertificates)

TLS unterstützt keine [Verdeckung von](cloaking.md). Wenn ein Verdeckungsflag und TLS in einem [**CoInitializeSecurity-**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) oder [**einem IClientSecurity::SetBlanket-Aufruf**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) angegeben sind, wird E \_ INVALIDARG zurückgegeben.

TLS funktioniert nicht, wenn die Authentifizierungsebene auf Keine festgelegt ist. Der Handshake zwischen Client und Server überprüft die jeweils festgelegte Authentifizierungsebene und wählt die höhere Sicherheitseinstellung für die Verbindung aus.

Die Sicherheitsparameter für TLS können durch Aufrufen von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) und [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)festgelegt werden. In den folgenden Abschnitten werden die Feinheiten beschrieben, die bei diesen Aufrufen zu verzeichnen sind.

### <a name="how-a-server-sets-the-security-blanket"></a>So legt ein Server die Sicherheitssicherheit fest

Wenn ein Server TLS verwenden möchte, muss er Schannel (RPC \_ C \_ AUTHN \_ GSS \_ SCHANNEL) als Authentifizierungsdienst im *asAuthSvc-Parameter* von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)angeben. Um zu verhindern, dass Clients mithilfe eines weniger sicheren Authentifizierungsdiensts eine Verbindung mit dem Server herstellen, sollte der Server beim Aufrufen von **CoInitializeSecurity** nur Schannel als Authentifizierungsdienst angeben. Der Server kann die Sicherheitslösung nach dem Aufruf **von CoInitializeSecurity** nicht mehr ändern.

Um TLS zu verwenden, sollten die folgenden Parameter angegeben werden, wenn ein Server [**CoInitializeSecurity aufruft:**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)

-   *pVoid* sollte entweder ein Zeiger auf ein [**IAccessControl-Objekt**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) oder ein Zeiger auf einen [**SECURITY \_ DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)sein. Er darf nicht **NULL** oder ein Zeiger auf eine AppID sein.
-   *cAuthSvc* darf nicht 0 oder -1 sein. COM-Server wählen Schannel nie aus, wenn *cAuthSvc*-1 ist.
-   *asAuthSvc* muss Schannel als möglichen Authentifizierungsdienst angeben. Legen Sie hierzu die folgenden [**SOLE \_ AUTHENTICATION \_ SERVICE-Parameter**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) für den Schannel-Member der [**SOLE AUTHENTICATION \_ \_ LIST**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list)fest:
    -   *dwAuthnSvc* muss RPC \_ C \_ AUTHN \_ GSS \_ SCHANNEL sein.
    -   *dwAuthzSvc* sollte RPC \_ C \_ AUTHZ \_ NONE lauten. Derzeit wird sie ignoriert.
    -   *pPrincipalName* muss ein Zeiger auf einen [**CERT \_ CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)sein, der als Zeiger auf OLECHAR dargestellt wird, das das X.509-Zertifikat des Servers darstellt.
-   *dwAuthnLevel* gibt die minimale Authentifizierungsebene an, die von Clients für eine erfolgreiche Verbindung akzeptiert wird. Es darf nicht RPC \_ C \_ AUTHN \_ LEVEL NONE \_ sein.
-   *Für dwCapabilities* sollte das \_ EOAC-APPID-Flag nicht festgelegt sein. Das EOAC \_ ACCESS \_ CONTROL-Flag sollte festgelegt werden, wenn *pVoid* auf ein [**IAccessControl-Objekt**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) zeigt. Es sollte nicht festgelegt werden, wenn *pVoid* auf einen SECURITY \_ DESCRIPTOR verweist. Weitere Flags, die festgelegt werden können, finden Sie unter [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

Weitere Informationen zur Verwendung von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)finden Sie unter [Festlegen der prozessweiten Sicherheit mit CoInitializeSecurity.](setting-processwide-security-with-coinitializesecurity.md)

### <a name="how-a-client-sets-the-security-blanket"></a>So legt ein Client den Sicherheitsvorsatz fest

Wenn ein Client TLS verwenden möchte, muss er Schannel (RPC \_ C \_ AUTHN \_ GSS \_ SCHANNEL) in der Liste der Authentifizierungsdienste im *pAuthList-Parameter* von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)angeben. Wenn Schannel beim Aufruf von **CoInitializeSecurity** nicht als möglicher Authentifizierungsdienst angegeben wird, schlägt ein späterer Aufruf von [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) (oder [**IClientSecurity::SetBlanket)**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)fehl, wenn versucht wird, Schannel als Authentifizierungsdienst anzugeben.

Die folgenden Parameter sollten angegeben werden, wenn ein Client [**CoInitializeSecurity aufruft:**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)

-   *dwAuthnLevel* gibt die Standardauthentifizierungsebene an, die der Client verwenden möchte. Es darf nicht RPC \_ C \_ AUTHN \_ LEVEL NONE \_ sein.
-   *dwImpLevel* muss RPC \_ C \_ IMP \_ LEVEL \_ IMPERSONATE sein.
-   *pAuthList* muss über die folgenden [**SOLE \_ AUTHENTICATION \_ INFO-Parameter**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) als Mitglied der Liste verfügen:
    -   *dwAuthnSvc* muss RPC \_ C \_ AUTHN \_ GSS \_ SCHANNEL sein.
    -   *dwAuthzSvc* muss RPC \_ C \_ RPHZ \_ NONE sein.
    -   *pAuthInfo* ist ein Zeiger auf einen [**CERT \_ CONTEXT,**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)der als Zeiger auf void dargestellt wird, der das X.509-Zertifikat des Clients darstellt. Wenn der Client kein Zertifikat besitzt oder sein Zertifikat dem Server nicht präsentieren möchte, muss *pAuthInfo* **NULL** sein, und es wird versucht, eine anonyme Verbindung mit dem Server herzustellen.
-   *dwCapabilities* ist ein Satz von Flags, die zusätzliche Clientfunktionen angeben. Informationen dazu, welche Flags festgelegt werden sollen, finden Sie unter [**CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)

Weitere Informationen zur Verwendung von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)finden Sie unter [Festlegen der prozessweiten Sicherheit mit CoInitializeSecurity.](setting-processwide-security-with-coinitializesecurity.md)

### <a name="how-a-client-changes-the-security-blanket"></a>Ändern der Sicherheit durch einen Client

Wenn ein Client TLS verwenden, aber die Sicherheitslösung nach dem Aufruf von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)ändern möchte, muss er entweder [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) oder [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) mit Parametern aufrufen, die denen im Aufruf von **CoInitializeSecurity** ähneln, mit den folgenden Unterschieden:

-   *pServerPrincName* gibt den Prinzipalnamen des Servers im msstd- oder fullsic-Format an. Informationen zu diesen Formaten finden Sie unter [Prinzipalnamen.](/windows/desktop/Rpc/principal-names) Wenn der Client über das X.509-Zertifikat des Servers verfügt, kann er den Prinzipalnamen durch Aufrufen von [**RpcCertGeneratePrincipalName**](/windows/desktop/api/rpcssl/nf-rpcssl-rpccertgenerateprincipalname)ermitteln.
-   *pAuthInfo* ist ein Zeiger auf einen [**CERT \_ CONTEXT,**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)der als Zeiger auf RPC AUTH IDENTITY HANDLE dargestellt \_ \_ \_ wird, das das X.509-Zertifikat des Clients darstellt. Wenn der Client kein Zertifikat besitzt oder sein Zertifikat dem Server nicht präsentieren möchte, muss *pAuthInfo* **NULL** sein, und es wird versucht, eine anonyme Verbindung mit dem Server herzustellen.
-   *dwCapabilities* besteht aus Flags, die zusätzliche Clientfunktionen angeben. Es können nur vier Flags zum Ändern der Sicherheitseinstellungen verwendet werden: EOAC \_ DEFAULT, EOAC \_ MUTUAL \_ AUTH, EOAC \_ ANY AUTHORITY \_ (dieses Flag ist veraltet) und EOAC \_ MAKE \_ FULLSIC. Weitere Informationen finden Sie unter [**CoSetProxyBlanket.**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)

Weitere Informationen zur Verwendung von [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)finden Sie unter [Festlegen der Sicherheit auf Schnittstellenproxyebene.](setting-security-at-the-interface-proxy-level.md)

### <a name="example-client-changes-the-security-blanket"></a>Beispiel: Client ändert die Sicherheitslage

Im folgenden Beispiel wird veranschaulicht, wie ein Client die Sicherheitsanpassung ändern kann, um eine Anforderung des Servers zur Bereitstellung des X.509-Zertifikats durch den Client zu berücksichtigen. Fehlerbehandlungscode wird aus Gründen der Kürze ausgelassen.


```C++
void ClientChangesSecurity ()
{
  HCRYPTPROV                   provider           = 0;
  HCERTSTORE                   cert_store         = NULL;
  PCCERT_CONTEXT               client_cert        = NULL;
  PCCERT_CONTEXT               server_cert        = NULL;
  WCHAR                        *server_princ_name = NULL;
  ISecret                      *pSecret           = NULL;
  MULTI_QI                     server_instance;
  COSERVERINFO                 server_machine;
  SOLE_AUTHENTICATION_LIST     auth_list;
  SOLE_AUTHENTICATION_INFO     auth_info[1];



  // Specify all the authentication info. 
  // The client is willing to connect using SChannel,
  //   with no client certificate.
  auth_list.cAuthInfo     = 1;
  auth_list.aAuthInfo     = auth_info;
  auth_info[0].dwAuthnSvc = RPC_C_AUTHN_GSS_SCHANNEL;
  auth_info[0].dwAuthzSvc = RPC_C_AUTHZ_NONE;
  auth_info[0].pAuthInfo  = NULL;  // No certificate

  // Initialize client security with no client certificate.
  CoInitializeSecurity( NULL, -1, NULL, NULL,
                        RPC_C_AUTHN_LEVEL_PKT,
                        RPC_C_IMP_LEVEL_IMPERSONATE, &auth_list,
                        EOAC_NONE, NULL );
  
  // Specify info for the proxy.
  server_instance = {&IID_ISecret, NULL, S_OK};
  server_machine  = {0, L"ServerMachineName", NULL, 0};
  
  // Create a proxy.
  CoCreateInstanceEx( CLSID_Secret, NULL, CLSCTX_REMOTE_SERVER, 
                      &server_machine, 1, &server_instance);
  pSecret = (ISecret *) server_instance.pItf;

  //** The client obtained the server's certificate during the handshake.
  //** The server requests a certificate from the client.

  // Get the default certificate provider.
  CryptAcquireContext( &provider, NULL, NULL, PROV_RSA_SCHANNEL, 0 );

  // Open the certificate store.
  cert_store = CertOpenSystemStore( provider, L"my" );

  // Find the client's certificate.
  client_cert = 
    CertFindCertificateInStore( cert_store,
                                X509_ASN_ENCODING | PKCS_7_ASN_ENCODING,
                                0,
                                CERT_FIND_SUBJECT_STR,
                                L"ClientName",  // Use the principal name
                                NULL );

  // Find the fullsic principal name of the server.
  RpcCertGeneratePrincipalName( server_cert, RPC_C_FULL_CERT_CHAIN, 
                                &server_princ_name );

  // Change the client's security: 
  // Increase the authentication level and attach a certificate.
  CoSetProxyBlanket( pSecret, RPC_C_AUTHN_GSS_SCHANNEL,
                     RPC_C_AUTHZ_NONE,
                     server_princ_name, RPC_C_AUTHN_LEVEL_PKT_PRIVACY,
                     RPC_C_IMP_LEVEL_IMPERSONATE, 
                     (RPC_AUTH_IDENTITY_HANDLE *) client_cert,
                     EOAC_NONE );

  cleanup:
  if (server_princ_name != NULL)
    RpcStringFree( &server_princ_name );
  if (client_cert != NULL)
    CertFreeCertificateContext(client_cert);
  if (server_cert != NULL)
    CertFreeCertificateContext(server_cert);
  if (cert_store != NULL)
    CertCloseStore( cert_store, CERT_CLOSE_STORE_CHECK_FLAG );
  if (provider != 0 )
    CryptReleaseContext( provider, 0 );
  if (pSecret != NULL)
    pSecret->Release();
  CoUninitialize();
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM- und Sicherheitspakete](com-and-security-packages.md)
</dt> </dl>

 

 