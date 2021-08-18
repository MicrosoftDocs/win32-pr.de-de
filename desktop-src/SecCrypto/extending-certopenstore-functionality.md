---
description: Der Zertifikatspeicher ist für alle Zertifikatverwaltungsvorgänge von zentraler Bedeutung.
ms.assetid: e5c7c882-cbfc-4343-952c-b13c67326756
title: Erweitern der CertOpenStore-Funktionalität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c770ae56ff597f51248486db2c9eb2d74bea8d63d2e8daad83d5938594b2f1a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007087"
---
# <a name="extending-certopenstore-functionality"></a>Erweitern der CertOpenStore-Funktionalität

Der [*Zertifikatspeicher*](../secgloss/c-gly.md) ist für alle Zertifikatverwaltungsvorgänge von zentraler Bedeutung. Die Funktionalität der [**CertOpenStore-Funktion**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore) kann durch die Verwendung einer installierbaren (oder registrierten) Zertifikatspeicheranbieterfunktion erweitert werden. Eine Übersicht über das Installieren oder Registrieren von Funktionen für die Verwendung mit cryptoAPI finden Sie unter [Übersicht über OID.](oid-overview.md)

> [!Note]  
> Benutzerdefinierte Zertifikatspeicher werden bei automatisierten Bereitstellungen nicht automatisch migriert. Um benutzerdefinierte Zertifikatspeicher zu migrieren, müssen Sie ein Manifest für die Migration der benutzerdefinierten Speicher erstellen und die Windows Migrationstool für den Benutzerstatus (USMT) verwenden. Das USMT steht im Microsoft Download Center unter zum Download zur <https://www.microsoft.com/download/details.aspx?id=10837> Verfügung.

 

[**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore) öffnet einen leeren Speicher im Arbeitsspeicher und ruft die Speicheranbieterfunktion auf (sofern registriert oder installiert), indem der [*Objektbezeichner*](../secgloss/o-gly.md) (OID) verwendet wird, der im *lpszStoreProvider-Parameter* übergeben wurde. Eine Liste der vordefinierten Anbietertypen, die mit cryptoAPI bereitgestellt werden, finden Sie unter **CertOpenStore**.

Die Speicheranbieterfunktion kopiert ihre Zertifikate und [*Zertifikatsperrlisten (Certificate Revocation Lists,*](../secgloss/c-gly.md) CRLs) in den Speicher im Arbeitsspeicher, der durch das *hCertStore-Handle* angegeben wird, das an ihn übergeben wird. Die neue Speicheranbieterfunktion kann jede der CryptoAPI-Zertifikatspeicherfunktionen verwenden, z. B. [**CertAddCertificateContextToStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore) oder [**CertAddSerializedElementToStore,**](/windows/win32/api/Wincrypt/nf-wincrypt-certaddserializedelementtostore)um dem Speicher im Arbeitsspeicher die zugehörigen Zertifikate und CRLs hinzuzufügen. Darüber hinaus gibt die store-provider-Funktion optional Werte für alle Datenmember der [**CERT \_ STORE \_ PROV \_ INFO-Struktur**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) zurück. Die Funktion muss diese Struktur nur aktualisieren, wenn sie zusätzliche Rückruffunktionen unterstützt. Wenn es sich bei dem Speicher beispielsweise um einen schreibgeschützten Speicher handelt, ist die Unterstützung anderer Rückruffunktionen wahrscheinlich nicht erforderlich. Details und Prototypen der möglichen Rückruffunktionen finden Sie unter [Certificate Store Provider Callback Functions](cryptography-functions.md).

Der TrustedPeople-Speicher pro Benutzer ist auf vordefinierte physische Speicher beschränkt. Sie können den TrustedPeople-Speicher pro Benutzer nicht erweitern. Sie können jedoch den TrustedPeople-Speicher des lokalen Computers erweitern.

**Windows XP und Windows Server 2003:** Der TrustedPeople-Speicher pro Benutzer ist nicht auf vordefinierte physische Speicher beschränkt.

Einer der Datenmember der [**CERT \_ STORE \_ PROV \_ INFO-Struktur**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) ist das *rgpvStoreProvFunc-Array.* Wenn die Speicheranbieterfunktion eine oder mehrere rückruffunktionen unterstützen muss, muss sie Zeiger für dieses Array bereitstellen. Diese Zeiger müssen auf die Rückruffunktionen verweisen, die für andere Zertifikatspeicheraktivitäten (z. B. das Schließen des Speichers) verwendet werden sollen. Die folgende Abbildung zeigt den Ablauf dieses Prozesses.

![Certopenstore-Funktionalität](images/openstor.png)

Wie in der folgenden Abbildung dargestellt, verwenden andere CryptoAPI-Funktionen (z. B. [**CertCloseStore)**](/windows/win32/api/Wincrypt/nf-wincrypt-certclosestore)nach dem Öffnen des Speichers das Array von Zeigern, um auf die Rückruffunktionen zuzugreifen, die die beabsichtigte Aufgabe ausführen. Die Definition der [**CERT \_ STORE \_ PROV \_ INFO-Struktur**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) und die Prototypen der Standardrückruffunktionen, die mit der CryptoAPI bereitgestellt werden, werden unter [Certificate Store Provider Callback Functions (Rückruffunktionen des Zertifikatanbieters)](cryptography-functions.md)angezeigt.

![certclosestore-Funktionalität](images/closstor.png)

Die Speicher-APIs ermöglichen es einem Speicheranbieter, die Zertifikate, CRLs und [*Zertifikatvertrauenslisten*](../secgloss/c-gly.md) (Certificate Trust Lists, CTLs) außerhalb des Caches des Speichers zu verwalten (z. B. eine externe Datenbank mit Zertifikaten, wie sie von der Microsoft Certificate Server-Datenbank bereitgestellt werden).

[**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore) wird über den *pszStoreProvider-Parameter* an die entsprechende [**installierbare Anbieterfunktion CertDllOpenStoreProv**](/windows/win32/api/Wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func) gesendet. Der Anbieter gibt Informationen im *pStoreProvInfo-Parameter* zurück, die auf eine [**CERT \_ STORE \_ PROV \_ INFO-Struktur**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) verweist. Die **CERT \_ STORE \_ PROV \_ INFO-Struktur** enthält einen **dwStoreProvFlags-Member.** Das \_ Flag \_ CERT STORE PROV EXTERNAL FLAG wurde \_ \_ hinzugefügt, damit der Anbieter angeben kann, dass die Zertifikate, CRLs und CTLs für den Cache des Speichers extern sind.

[**CertDllOpenStoreProv**](/windows/win32/api/Wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func) gibt ein Array von Rückruffunktionen zurück. Ein Anbieter kann die folgenden Rückruffunktionen implementieren:

-   CERT \_ STORE \_ PROV \_ CLOSE \_ FUNC
-   CERT \_ STORE \_ PROV \_ READ \_ CERT \_ FUNC
-   CERT \_ STORE \_ PROV \_ WRITE \_ CERT \_ FUNC
-   CERT \_ STORE \_ PROV \_ DELETE \_ CERT \_ FUNC
-   CERT \_ STORE \_ PROV \_ SET \_ CERT \_ PROPERTY \_ FUNC
-   CERT \_ STORE \_ PROV \_ READ \_ CRL \_ FUNC
-   CERT \_ STORE \_ PROV \_ WRITE \_ CRL \_ FUNC
-   CERT \_ STORE \_ PROV \_ DELETE \_ CRL \_ FUNC
-   CERT \_ STORE \_ PROV \_ SET \_ CRL \_ PROPERTY \_ FUNC
-   CERT \_ STORE \_ PROV \_ READ \_ CTL \_ FUNC
-   CERT \_ STORE \_ PROV \_ WRITE \_ CTL \_ FUNC
-   CERT \_ STORE \_ PROV \_ DELETE \_ CTL \_ FUNC
-   CERT \_ STORE \_ PROV \_ SET \_ CTL \_ PROPERTY \_ FUNC

Bei Aufrufen der Rückruffunktionen WRITE \_ CERT, WRITE \_ CRL und WRITE \_ CTL, wenn das CERT \_ STORE \_ PROV WRITE ADD \_ FLAG \_ festgelegt \_ ist, enthalten die oberen 16 Bits des *dwFlags-Parameters* den *dwAddDisposition-Wert.* Zur Unterstützung externer Speicher kann ein Anbieter die folgenden Rückruffunktionen implementieren:

-   CERT \_ STORE \_ PROV \_ FIND \_ CERT \_ FUNC
-   CERT \_ STORE \_ PROV \_ FREE \_ FIND \_ CERT \_ FUNC
-   CERT \_ STORE \_ PROV \_ GET \_ CERT \_ PROPERTY \_ FUNC
-   CERT \_ STORE \_ PROV \_ FIND \_ CRL \_ FUNC
-   CERT \_ STORE \_ PROV \_ FREE \_ FIND \_ CRL \_ FUNC
-   CERT \_ STORE \_ PROV \_ GET \_ CRL \_ PROPERTY \_ FUNC
-   CERT \_ STORE \_ PROV \_ FIND \_ CTL \_ FUNC
-   CERT \_ STORE \_ PROV \_ FREE \_ FIND \_ CTL \_ FUNC
-   CERT \_ STORE \_ PROV \_ GET \_ CTL \_ PROPERTY \_ FUNC

Die Zertifikatrückruffunktionen verfügen über die folgenden Signaturen:

``` syntax
typedef struct _CERT_STORE_PROV_FIND_INFO {
    DWORD               cbSize;
    DWORD               dwMsgAndCertEncodingType;
    DWORD               dwFindFlags;
    DWORD               dwFindType;
    const void          *pvFindPara;
} CERT_STORE_PROV_FIND_INFO, *PCERT_STORE_PROV_FIND_INFO;
typedef const CERT_STORE_PROV_FIND_INFO CCERT_STORE_PROV_FIND_INFO,
    *PCCERT_STORE_PROV_FIND_INFO;

typedef BOOL (WINAPI *PFN_CERT_STORE_PROV_FIND_CERT)(
        IN HCERTSTOREPROV hStoreProv,
        IN PCCERT_STORE_PROV_FIND_INFO pFindInfo,
        IN PCCERT_CONTEXT pPrevCertContext,
        IN DWORD dwFlags,
        IN OUT void **ppvStoreProvFindInfo,
        OUT PCCERT_CONTEXT *ppProvCertContext
        );

typedef BOOL (WINAPI *PFN_CERT_STORE_PROV_FREE_FIND_CERT)(
        IN HCERTSTOREPROV hStoreProv,
        IN PCCERT_CONTEXT pCertContext,
        IN void *pvStoreProvFindInfo,
        IN DWORD dwFlags
        );

typedef BOOL (WINAPI *PFN_CERT_STORE_PROV_GET_CERT_PROPERTY)(
        IN HCERTSTOREPROV hStoreProv,
        IN PCCERT_CONTEXT pCertContext,
        IN DWORD dwPropId,
        IN DWORD dwFlags,
        OUT void *pvData,
        IN OUT DWORD *pcbData
        );
```

Die Signaturen für die CRL- und CTL-Rückruffunktionen sind mit dem oben genannten identisch, wobei der Zeiger auf den [**CERT \_ CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) durch einen Zeiger auf einen [**CRL \_ CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-crl_context) oder [**CTL \_ CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-ctl_context)ersetzt wird.

Der FIND \_ CERT-Rückruf wird aufgerufen, wenn die Speicher-APIs Zertifikate aufzählen, suchen oder hinzufügen. *pPrevCertContext* und *ppvStoreProvFindInfo* werden auf **NULL** festgelegt, um ein neues FIND zu initiieren. Die zurückgegebene *ppvStoreProvFindInfo* wird bei der nächsten Suche zurückgegeben, zu der sie vom Anbieter freigegeben werden kann. Der Anbieter kann alle, einige oder keine der Zertifikateigenschaften festlegen. Der Anbieter kann zurückstellen, bis der GET \_ CERT \_ PROPERTY-Rückruf aufgerufen wird. Es wird empfohlen, dass Anbieter so viele Eigenschaften wie möglich festlegen, um das Kopieren in einen anderen Speicher zu ermöglichen.

Die folgenden Zertifikatssuchetypen werden in [**CertFindCertificateInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)unterstützt:

-   CERT \_ FIND \_ ANY
-   CERT \_ FIND \_ SHA1 \_ HASH
-   CERT \_ FIND \_ MD5 \_ HASH
-   CERT \_ \_ FIND-EIGENSCHAFT
-   CERT \_ FIND \_ PUBLIC \_ KEY
-   CERT \_ FIND \_ SUBJECT \_ NAME
-   CERT \_ FIND \_ SUBJECT \_ ATTR
-   CERT \_ FIND \_ ISSUER \_ NAME
-   CERT \_ FIND \_ ISSUER \_ ATTR
-   CERT \_ FIND \_ SUBJECT \_ STR \_ A
-   CERT \_ FIND \_ SUBJECT \_ STR \_ W
-   \_ZERTIFIKATSSUCHE \_ AUSSTELLER STR \_ \_ A
-   CERT \_ FIND \_ ISSUER \_ STR \_ W
-   CERT \_ FIND \_ KEY \_ SPEC
-   CERT \_ FIND \_ ENHKEY \_ USAGE

Der FIND \_ CERT-Rückruf wird für jeden der oben genannten Suchtypen aufgerufen. Die an [**CertFindCertificateInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) übergebenen Parameter werden direkt in die CERT \_ STORE \_ PROV FIND INFO-Struktur kopiert, bevor der \_ FIND \_ \_ CERT-Rückruf aufgerufen wird. Ausführliche Informationen zu den Feldwerten für die verschiedenen Suchtypen der CERT \_ STORE \_ PROV \_ FIND \_ INFO-Struktur finden Sie unter **CertFindCertificateInStore**.

Die folgenden Zertifikatssuchetypen unterstützen die [**APIs CertGetSubjectCertificateFromStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) und [**CertGetIssuerCertificateFromStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetissuercertificatefromstore) und können ermitteln, ob das Zertifikat bereits im Speicher vorhanden ist, bevor Sie hinzufügen:

-   CERT \_ FIND \_ SUBJECT \_ CERT
-   CERT \_ FIND \_ ISSUER \_ OF
-   CERT \_ FIND \_ EXISTING

Für CERT \_ FIND \_ SUBJECT \_ CERT zeigt der *pvFindPara-Parameter* auf eine [**CERT \_ INFO-Struktur,**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_info) die den Issuer und SerialNumber des Antragstellers enthält. Für CERT \_ FIND ISSUER OF verweist \_ \_ *pvFindPara* auf eine [**CERT \_ CONTEXT-Struktur**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) des Antragstellers. Für CERT \_ FIND \_ EXISTING verweist *pvFindPara* auf einen **CERT \_ CONTEXT** des Zertifikats, um zu überprüfen, ob es im Speicher vorhanden ist.

Der FREE \_ FIND \_ CERT-Rückruf wird aufgerufen, wenn das vom FIND CERT-Rückruf zurückgegebene Zertifikat \_ nicht freigegeben wurde, indem es in einem nachfolgenden \_ FIND-CERT verwendet wurde, wodurch der [*Verweiszähler*](../secgloss/r-gly.md) auf 0 (null) dekrementiert oder durch einen Aufruf von [**CertCloseStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certclosestore)freigegeben wurde. Bevor der CLOSE-Rückruf aufgerufen wird, sollten alle vom FIND CERT-Rückruf zurückgegebenen Zertifikate \_ an den Anbieter freigegeben werden, indem sie an einen Aufruf des FIND \_ CERT-Rückrufs oder einen Aufruf des FREE \_ FIND \_ CERT-Rückrufs übergeben werden. Dasselbe gilt für die CRL- und CTL-Rückrufe.

Der GET \_ CERT \_ PROPERTY-Rückruf wird von [**CertGetCertificateContextProperty**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) aufgerufen, wenn die angegebene Eigenschaft für den *pCertContext-Parameter* nicht gefunden werden kann. Dasselbe gilt für GET \_ CRL \_ PROPERTY und GET \_ CTL \_ PROPERTY.

Der \_ FIND-CRL-Rückruf wird aufgerufen, wenn die Speicher-APIs CRLs auflisten oder abrufen und bevor sie eine Sperrliste hinzufügen. Die folgenden CRL-Suchtypen werden definiert:

Für CRL \_ FIND \_ ISSUED \_ BY ist *pvFindPara* ein Zeiger auf einen [**CERT \_ CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) des Zertifikatsperrlistenausstellers. Für CRL \_ FIND \_ EXISTING ist *pvFindPara* ein Zeiger auf einen [**\_ CRL-KONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-crl_context) der Sperrliste, um zu bestimmen, ob sie bereits im Speicher vorhanden ist.

Der \_ FIND-CTL-Rückruf wird aufgerufen, wenn die Store-APIs CTLs auflisten oder suchen. Die folgenden CTL-Suchtypen werden in [**CertFindCTLInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindctlinstore)unterstützt:

-   CTL \_ FIND \_ ANY
-   CTL \_ FIND \_ SHA1 \_ HASH
-   CTL \_ FIND \_ MD5 \_ HASH
-   VERWENDUNG \_ DER CTL-SUCHE \_
-   CTL \_ FIND \_ SUBJECT
-   CTL \_ FIND \_ EXISTING

Der \_ FIND-CTL-Rückruf wird für jeden der oben genannten Suchtypen aufgerufen. Die an [**CertFindCTLInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindctlinstore) übergebenen Parameter werden direkt in die CERT \_ STORE \_ PROV FIND INFO-Struktur kopiert, bevor der \_ FIND \_ \_ CTL-Rückruf aufgerufen wird. Ausführliche Informationen zu den Feldwerten für die verschiedenen Suchtypen der CERT \_ STORE \_ PROV \_ FIND \_ INFO-Struktur finden Sie unter **CertFindCTLInStore**.

Der CTL \_ \_ FIND EXISTING CTL-Suchtyp hilft zu bestimmen, ob die CTL bereits im Speicher vorhanden ist, bevor eine CTL hinzugefügt wird.

Für CTL \_ FIND \_ EXISTING ist *pvFindPara* ein Zeiger auf die [**CTL \_ CONTEXT-Struktur**](/windows/win32/api/Wincrypt/ns-wincrypt-ctl_context) der CTL, um zu bestimmen, ob sie bereits im Speicher vorhanden ist.

 

 
