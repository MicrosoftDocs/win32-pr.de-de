---
title: Schannel
description: Das Sicherheitspaket Secure Channel (SChannel), dessen Authentifizierungsdienst Bezeichner RPC \_ C \_ authn \_ GSS \_ SChannel ist, unterstützt die folgenden öffentlichen Schlüssel basierten Protokolle SSL (Secure Sockets Layer), Version 2,0 und 3,0, Transport Layer Security (TLS) 1,0 und private Kommunikationstechnologie (PCT) 1,0. TLS 1,0 ist eine standardisierte, leicht geänderte Version von SSL 3,0, die von der Internet Engineering Task Force (IETF) im Januar 1999 im Dokument RFC 2246 ausgegeben wurde. Da TLS standardisiert ist, wird empfohlen, TLS anstelle von SSL zu verwenden. PCT ist nur aus Gründen der Abwärtskompatibilität enthalten und sollte nicht für die neue Entwicklung verwendet werden. Wenn das SChannel-Sicherheitspaket verwendet wird, aushandt DCOM automatisch das beste Protokoll, abhängig von den Client-und Serverfunktionen.
ms.assetid: 03a5f987-f668-4f19-9b58-d62711f58734
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eccc9f82a05d1542e7585426128f10cdf452d31d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316569"
---
# <a name="schannel"></a>Schannel

Das Sicherheitspaket Secure Channel (SChannel), dessen Authentifizierungsdienst Bezeichner RPC \_ C \_ authn \_ GSS \_ SChannel ist, unterstützt die folgenden öffentlichen Schlüssel basierten Protokolle: SSL (Secure Sockets Layer) Version 2,0 und 3,0, Transport Layer Security (TLS) 1,0 und private Kommunikationstechnologie (PCT) 1,0. TLS 1,0 ist eine standardisierte, leicht geänderte Version von SSL 3,0, die von der Internet Engineering Task Force (IETF) im Januar 1999 im Dokument [RFC 2246](https://www.ietf.org/rfc/rfc2246.txt)ausgegeben wurde. Da TLS standardisiert ist, wird empfohlen, TLS anstelle von SSL zu verwenden. PCT ist nur aus Gründen der Abwärtskompatibilität enthalten und sollte nicht für die neue Entwicklung verwendet werden. Wenn das SChannel-Sicherheitspaket verwendet wird, aushandt DCOM automatisch das beste Protokoll, abhängig von den Client-und Serverfunktionen.

In den folgenden Themen wird das TLS-Protokoll kurz beschrieben und erläutert, wie es mit DCOM funktioniert.

-   [Verwendung von TLS](#when-to-use-tls)
-   [Kurze Übersicht über die Funktionsweise von TLS](#brief-overview-of-how-tls-works)
-   [X. 509-Zertifikate](#x509-certificates)
    -   [Clientzertifikate](#client-certificates)
-   [Verwenden von TLS in com](#using-tls-in-com)
    -   [Festlegen der Sicherheits Pauschale durch einen Server](#how-a-server-sets-the-security-blanket)
    -   [Festlegen der Sicherheits Pauschale durch einen Client](#how-a-client-sets-the-security-blanket)
    -   [Ändern der Sicherheits Pauschale durch einen Client](#how-a-client-changes-the-security-blanket)
    -   [Beispiel: Client ändert die Sicherheits Pauschale](#example-client-changes-the-security-blanket)
-   [Zugehörige Themen](#related-topics)

> [!Note]  
> Alle Informationen über das TLS-Protokoll in diesen Abschnitten gelten auch für die Protokolle SSL und PCT.

 

## <a name="when-to-use-tls"></a>Verwendung von TLS

TLS ist die einzige Sicherheitsoption, die verfügbar ist, wenn Server Ihre Identität anonymen Clients nachweisen müssen. Dies ist besonders wichtig für Websites, die an e-Commerce teilnehmen möchten, da Sie dabei helfen, die Übertragung vertraulicher Informationen, wie Kreditkartennummern, zu schützen. TLS stellt sicher, dass die e-Commerce-Kunden sicher sein können, mit wem Sie Geschäfte betreiben, weil Sie einen Nachweis für die Identität des Servers erhalten. Außerdem ist der e-Commerce-Server der Effizienz, dass er sich nicht mit der Authentifizierung der Identität seiner Kunden befassen muss.

TLS erfordert, dass alle Server deren Identität für Clients nachweisen. Außerdem bietet TLS die Möglichkeit, Clients die Identität der Server nachzuweisen. Diese gegenseitige Authentifizierung kann nützlich sein, um den Zugriff auf bestimmte Webseiten in einem großen Unternehmens Intranet einzuschränken.

TLS unterstützt die stärksten Authentifizierungs Ebenen und bietet eine offene Architektur, mit der sich die Verschlüsselungsstärke im Laufe der Zeit erhöhen lässt, um technologische Innovationen aufrechtzuerhalten. TLS ist die beste Wahl für Umgebungen, in denen das höchste Maß an Sicherheit für die Daten während der Übertragung gewünscht ist.

## <a name="brief-overview-of-how-tls-works"></a>Kurze Übersicht über die Funktionsweise von TLS

TLS basiert auf einer Public Key-Infrastruktur (PKI), die öffentliche/private Schlüsselpaare zum Aktivieren der Datenverschlüsselung und zum Einrichten der Datenintegrität verwendet und X. 509-Zertifikate für die Authentifizierung verwendet.

Viele Sicherheitsprotokolle, z. b. das Kerberos V5-Protokoll, sind von einem einzigen Schlüssel zum Verschlüsseln und Entschlüsseln von Daten abhängig. Solche Protokolle hängen daher vom sicheren Austausch der Verschlüsselungsschlüssel ab. im Kerberos-Protokoll erfolgt dies über Tickets, die aus dem Schlüsselverteilungscenter (KDC) abgerufen wurden. Dies erfordert, dass jeder, der das Kerberos-Protokoll verwendet, beim KDC registriert wird. Dies wäre eine unpraktische Einschränkung für einen e-Commerce-Webserver, der Millionen von Kunden aus der ganzen Welt gewinnen soll. TLS basiert daher auf einer PKI, die zwei Schlüssel für die Datenverschlüsselung verwendet: Wenn ein Schlüssel des Paars die Daten verschlüsselt, kann er nur vom anderen Schlüssel des Paars entschlüsselt werden. Der Grund Vorteil dieses Entwurfs ist, dass die Verschlüsselung ohne den sicheren Austausch von Verschlüsselungsschlüsseln ausgeführt werden kann.

Eine PKI verwendet eine Technik, bei der einer der Schlüssel privat gehalten wird und nur für den Prinzipal verfügbar ist, für den er registriert ist, während der andere Schlüssel für jeden zugänglich gemacht wird. Wenn jemand eine private Nachricht an den Besitzer eines Schlüssel Paars senden möchte, kann die Nachricht mit dem öffentlichen Schlüssel verschlüsselt werden, und nur der private Schlüssel kann zum Entschlüsseln der Nachricht verwendet werden.

Schlüsselpaare werden auch verwendet, um die Integrität der Daten zu überprüfen, die gesendet werden. Zu diesem Zweck kann der Besitzer des Schlüssel Paars eine digitale Signatur an die Daten anfügen, bevor Sie gesendet wird. Das Erstellen einer digitalen Signatur umfasst das Berechnen eines Hash der Daten und das Verschlüsseln des Hashs mit dem privaten Schlüssel. Jeder Benutzer, der den öffentlichen Schlüssel verwendet, um die digitale Signatur zu entschlüsseln, ist sicher, dass die digitale Signatur nur von der Person stammen muss, die den privaten Schlüssel besitzt. Außerdem kann der Empfänger einen Hash der Daten mit dem gleichen Algorithmus wie der Absender berechnen, und wenn der berechnete Hash mit dem Wert übereinstimmt, der in der digitalen Signatur gesendet wurde, kann der Empfänger sicher sein, dass die Daten nicht geändert wurden, nachdem Sie digital signiert wurden.

Ein Nachteil bei der Verwendung einer PKI für die Verschlüsselung großer Datenmengen ist die relativ langsame Leistung. Aufgrund der intensiven Mathematik kann die Verschlüsselung und Entschlüsselung von Daten mithilfe einer asymmetrischen Chiffre, die von einem Schlüsselpaar abhängt, bis zu 1.000 mal langsamer sein als die Verschlüsselung und Entschlüsselung mithilfe einer symmetrischen Chiffre, die nur von einem einzelnen Schlüssel abhängt. TLS verwendet daher eine PKI nur zum Erstellen digitaler Signaturen und zum Aushandeln des Sitzungs spezifischen Single Key, der sowohl vom Client als auch vom Server für die Verschlüsselung und Entschlüsselung von Massendaten verwendet wird. TLS unterstützt eine Vielzahl von symmetrischen symmetrischen Chiffren mit einem einzelnen Schlüssel, und in Zukunft können weitere Chiffren hinzugefügt werden.

Weitere Informationen zum TLS-Handshake-Protokoll finden Sie unter [TLS-Handshake-Protokoll](/windows/desktop/SecAuthN/tls-handshake-protocol).

Weitere Informationen zur Kryptografie hinter dem TLS-Protokoll finden Sie unter [Kryptografie Essentials](/windows/desktop/SecCrypto/cryptography-essentials).

## <a name="x509-certificates"></a>X.509-Zertifikate

Ein wichtiges Problem, das von einer PKI behandelt werden muss, ist die Fähigkeit, der Authentizität des verwendeten öffentlichen Schlüssels zu vertrauen. Wenn Sie einen öffentlichen Schlüssel verwenden, der für ein Unternehmen ausgestellt wurde, mit dem Sie Geschäfte ausführen möchten, sollten Sie sicher sein, dass der Schlüssel eigentlich zum Unternehmen gehört und nicht zu einem Dieb, der Ihre Kreditkartennummer ermitteln möchte.

Um die Identität eines Prinzipals zu gewährleisten, der ein Schlüsselpaar enthält, wird dem Prinzipal ein X. 509-Zertifikat von einer Zertifizierungsstelle (Certification Authority, ca) ausgestellt. Dieses Zertifikat enthält Informationen, mit denen der Prinzipal identifiziert wird, der öffentliche Schlüssel des Prinzipals enthält und von der Zertifizierungsstelle digital signiert wurde. Diese digitale Signatur gibt an, dass die Zertifizierungsstelle der Ansicht ist, dass der im Zertifikat enthaltene öffentliche Schlüssel wirklich dem Prinzipal angehört, der durch das Zertifikat identifiziert wird.

Und wie Vertrauen Sie der Zertifizierungsstelle? Da die Zertifizierungsstelle selbst ein X. 509-Zertifikat enthält, das von einer Zertifizierungsstelle höherer Ebene signiert wurde. Diese Kette von Zertifikat Signaturen wird so lange fortgesetzt, bis eine Stamm Zertifizierungsstelle erreicht wird. Dies ist eine Zertifizierungsstelle, die eigene Zertifikate signiert Wenn Sie der Integrität der Stamm Zertifizierungsstelle eines Zertifikats vertrauen, sollten Sie die Echtheit des Zertifikats als vertrauenswürdig einstufen. Daher ist die Auswahl von Stamm Zertifizierungsstellen, denen Sie vertrauen möchten, eine wichtige Aufgabe für einen Systemadministrator.

### <a name="client-certificates"></a>Clientzertifikate

Als erster Grund für das Übertragen von Sicherheitsprotokollen war es, sicherzustellen, dass ein Client eine Verbindung mit einem authentischen Server hergestellt und den Datenschutz während der Übertragung schützt. SSL 3,0 und TLS 1,0 enthalten jedoch auch Unterstützung für die Übertragung eines Client Zertifikats während des Protokoll Handshakes. Diese optionale Funktion ermöglicht die gegenseitige Authentifizierung des Clients und des Servers.

Die Entscheidung, ob ein Client Zertifikat verwendet werden soll, sollte im Kontext der Anwendung vorgenommen werden. Client Zertifikate sind nicht erforderlich, wenn der Server von der primären Anforderung authentifiziert wird. Wenn die Client Authentifizierung jedoch unverzichtbar ist, kann das Zertifikat eines Clients verwendet werden, anstatt sich auf die benutzerdefinierte Authentifizierung innerhalb der Anwendung zu verlassen. Die Verwendung von Client Zertifikaten ist besser als die benutzerdefinierte Authentifizierung, da Sie Benutzern ein Single Sign-on Szenario bietet.

## <a name="using-tls-in-com"></a>Verwenden von TLS in com

TLS unterstützt nur die Identitätswechsel Ebene des Identitäts Wechsels (RPC- \_ C- \_ IMP- \_ Ebene \_ ). Wenn com TLS als Authentifizierungsdienst auf einem Proxy aushandt, wird die Identitätswechsel Ebene von com unabhängig von der ProzessStandard Einstellung so festgelegt, dass der Identitätswechsel durchgeführt wird. Damit der Identitätswechsel in TLS ordnungsgemäß funktioniert, muss der Client ein X. 509-Zertifikat für den Server bereitstellen, und der Server muss über dieses Zertifikat verfügen, das einem bestimmten Benutzerkonto auf dem Server zugeordnet ist. Weitere Informationen finden [Sie in der Schritt-für-Schritt-Anleitung zum Mapping von Zertifikaten zu Benutzerkonten](https://www.microsoft.com/isapi/redir.dll?prd=windows2000&sbp=technicallibrary&ar=security&sba=mappingcertificates).

TLS unterstützt keine [Cloaking](cloaking.md). Wenn ein Cloaking-Flag und TLS in einem [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) -oder einem [**IClientSecurity:: setblanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) -Befehl angegeben werden, \_ wird E invalidArg zurückgegeben.

TLS funktioniert nicht, wenn die Authentifizierungs Ebene auf None festgelegt ist. Der Handshake zwischen Client und Server überprüft die von jedem festgelegte Authentifizierungs Ebene und wählt die höhere Sicherheitseinstellung für die Verbindung aus.

Die Sicherheitsparameter für TLS können durch Aufrufen von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) und [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)festgelegt werden. In den folgenden Abschnitten werden die für diese Aufrufe beteiligten Aspekte beschrieben.

### <a name="how-a-server-sets-the-security-blanket"></a>Festlegen der Sicherheits Pauschale durch einen Server

Wenn ein Server TLS verwenden möchte, muss er Schannel (RPC \_ C \_ authn \_ GSS \_ SChannel) als Authentifizierungsdienst im *asAuthSvc* -Parameter von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)angeben. Um zu verhindern, dass Clients mithilfe eines weniger sicheren Authentifizierungs Dienstanbieter eine Verbindung mit dem Server herstellen, sollte der Server nur SChannel als Authentifizierungsdienst angeben, wenn **CoInitializeSecurity** aufgerufen wird. Der Server kann die Sicherheits Pauschale nicht ändern, nachdem **CoInitializeSecurity** aufgerufen wurde.

Um TLS zu verwenden, sollten die folgenden Parameter angegeben werden, wenn ein Server [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)aufruft:

-   *pVoid* muss entweder ein Zeiger auf ein [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) -Objekt oder ein Zeiger auf eine [**Sicherheits \_ Beschreibung**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)sein. Er darf nicht **null** oder ein Zeiger auf eine AppID sein.
-   *cauthsvc* darf nicht 0 oder-1 sein. Wenn *cauthsvc* den Wert-1 hat, wählt der com-Server SChannel nie aus.
-   *asAuthSvc* muss SChannel als möglichen Authentifizierungsdienst angeben. Dies erfolgt durch Festlegen der folgenden [**einzigen \_ Authentifizierungs \_ Dienst**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) Parameter für das SChannel-Mitglied der [**einzigen \_ Authentifizierungs \_ Liste**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list):
    -   *dwauthnsvc* muss RPC \_ C \_ authn \_ GSS \_ SChannel sein.
    -   *dwauthzsvc* sollte RPC \_ C \_ Authz \_ None lauten. Derzeit wird Sie ignoriert.
    -   *pprincipalname* muss ein Zeiger auf einen [**CERT- \_ Kontext**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)sein, der als Zeiger auf OLECHAR umgewandelt wird, der das X. 509-Zertifikat des Servers darstellt.
-   *dwauthnlevel* gibt die minimale Authentifizierungs Ebene an, die von Clients für eine erfolgreiche Verbindung akzeptiert wird. Es kann keine RPC- \_ C- \_ authn-Ebene " \_ \_ None" sein
-   für *DW-Funktionen* sollte das eoac- \_ AppID-Flag nicht festgelegt sein. Das eoac \_ - \_ Flag für die Zugriffs Steuerung sollte festgelegt werden, wenn *pVoid* auf ein [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) -Objekt verweist. es sollte nicht festgelegt werden, wenn *pVoid* auf eine Sicherheits \_ Beschreibung verweist. Weitere Flags, die festgelegt werden können, finden Sie unter [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

Weitere Informationen zur Verwendung von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)finden Sie unter [Festlegen der Processwide-Sicherheit mit CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md).

### <a name="how-a-client-sets-the-security-blanket"></a>Festlegen der Sicherheits Pauschale durch einen Client

Wenn ein Client TLS verwenden möchte, muss er Schannel (RPC \_ C \_ authn \_ GSS \_ SChannel) in der Liste der Authentifizierungsdienste im *pauthlist* -Parameter von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)angeben. Wenn SChannel nicht als möglicher Authentifizierungsdienst angegeben wird, wenn **CoInitializeSecurity** aufgerufen wird, schlägt ein späterer Aufruf von [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) (oder [**IClientSecurity:: setblanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)) fehl, wenn versucht wird, SChannel als Authentifizierungsdienst anzugeben.

Die folgenden Parameter müssen angegeben werden, wenn ein Client [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)aufruft:

-   *dwauthnlevel* gibt die Standard Authentifizierungs Ebene an, die vom Client verwendet werden soll. Es kann keine RPC- \_ C- \_ authn-Ebene " \_ \_ None" sein
-   *dwimplevel* muss ein RPC- \_ C- \_ IMP-Stufen Identitätswechsel sein \_ \_ .
-   *pauthlist* muss die folgenden [**einzigen \_ Authentifizierungs \_ Informations**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) Parameter als Mitglied der Liste aufweisen:
    -   *dwauthnsvc* muss RPC \_ C \_ authn \_ GSS \_ SChannel sein.
    -   *dwauthzsvc* muss RPC \_ C \_ Authz \_ None lauten.
    -   *pAuthInfo* ist ein Zeiger auf einen [**CERT- \_ Kontext**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context), der als Zeiger auf "void" umgewandelt wird, der das X. 509-Zertifikat des Clients darstellt. Wenn der Client kein Zertifikat hat oder das Zertifikat nicht auf dem Server präsentieren möchte, muss *pAuthInfo* **null** sein, und es wird eine anonyme Verbindung mit dem Server hergestellt.
-   *DW-Funktionen* sind ein Satz von Flags, die zusätzliche Client Funktionen angeben. Informationen dazu, welche Flags festgelegt werden sollten, finden Sie unter [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) .

Weitere Informationen zur Verwendung von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)finden Sie unter [Festlegen der Processwide-Sicherheit mit CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md).

### <a name="how-a-client-changes-the-security-blanket"></a>Ändern der Sicherheits Pauschale durch einen Client

Wenn ein Client TLS verwenden und die Sicherheitsdecke nach dem Aufrufen von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)ändern möchte, muss er entweder [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) oder [**IClientSecurity:: setblanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) mit Parametern aufrufen, die mit den im Aufruf von **CoInitializeSecurity** verwendeten Parametern vergleichbar sind, mit den folgenden unterschieden:

-   *pserverprincname* gibt den Prinzipal Namen des Servers im msstd-oder fullsic-Format an. Weitere Informationen zu diesen Formaten finden Sie unter [Prinzipal Namen](/windows/desktop/Rpc/principal-names). Wenn der Client über das X. 509-Zertifikat des Servers verfügt, kann der Prinzipal Name durch Aufrufen von [**rpccertgenerateprincipalname**](/windows/desktop/api/rpcssl/nf-rpcssl-rpccertgenerateprincipalname)gefunden werden.
-   *pAuthInfo* ist ein Zeiger auf einen [**CERT- \_ Kontext**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context), der als Zeiger auf \_ das RPC-Authentifizierungs Identitäts handle umgewandelt wird \_ \_ , das das X. 509-Zertifikat des Clients darstellt. Wenn der Client kein Zertifikat hat oder das Zertifikat nicht auf dem Server präsentieren möchte, muss *pAuthInfo* **null** sein, und es wird eine anonyme Verbindung mit dem Server hergestellt.
-   *DW-Funktionen* bestehen aus Flags, die zusätzliche Client Funktionen angeben. Es können nur vier Flags verwendet werden, um sicherheitspauseeinstellungen zu ändern: eoac \_ Default, eoac \_ gegenseitige Authentifizierung \_ , eoac \_ Any \_ Authority (dieses Flag ist veraltet) und eoac \_ machen \_ fullsic. Weitere Informationen finden Sie unter [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).

Weitere Informationen zur Verwendung von [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)finden Sie unter [Festlegen der Sicherheit auf der Ebene der Schnittstellen Proxys](setting-security-at-the-interface-proxy-level.md).

### <a name="example-client-changes-the-security-blanket"></a>Beispiel: Client ändert die Sicherheits Pauschale

Im folgenden Beispiel wird veranschaulicht, wie ein Client die Sicherheits Pauschale ändern kann, um eine Anforderung vom Server für die Bereitstellung des X. 509-Zertifikats durch den Client zu erfüllen. Der Fehler Behandlungs Code wird aus Gründen der Kürze ausgelassen.


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

[COM-und Sicherheitspakete](com-and-security-packages.md)
</dt> </dl>

 

 