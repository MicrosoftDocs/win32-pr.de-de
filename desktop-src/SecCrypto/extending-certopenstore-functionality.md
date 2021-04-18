---
description: Der Zertifikat Speicher ist für alle Zertifikat Verwaltungsvorgänge von zentraler Bedeutung.
ms.assetid: e5c7c882-cbfc-4343-952c-b13c67326756
title: Erweitern der certopsstore-Funktionalität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cce198578cc482ba0488bd97ae0f1d7f923511b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104564224"
---
# <a name="extending-certopenstore-functionality"></a>Erweitern der certopsstore-Funktionalität

Der [*Zertifikat Speicher*](../secgloss/c-gly.md) ist für alle Zertifikat Verwaltungsvorgänge von zentraler Bedeutung. Die Funktionalität der [**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore) -Funktion kann durch die Verwendung einer installierbaren (oder registrierten) Zertifikat Speicher Anbieter-Funktion erweitert werden. Eine Übersicht über das Installieren oder Registrieren von Funktionen für die Verwendung mit der CryptoAPI finden Sie unter [OID Overview](oid-overview.md).

> [!Note]  
> Benutzerdefinierte Zertifikat Speicher werden beim Ausführen automatisierter bereit Stellungen nicht automatisch migriert. Wenn Sie benutzerdefinierte Zertifikat Speicher migrieren möchten, müssen Sie ein Manifest erstellen, um die benutzerdefinierten Speicher zu migrieren und die Windows-Migrationstool für den Benutzerstatus (Anwendungs-) zu verwenden. Das Windows-Tool steht im Microsoft Download Center unter zum Download zur Verfügung <https://www.microsoft.com/download/details.aspx?id=10837> .

 

[**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore) öffnet einen leeren Speicher im Arbeitsspeicher und ruft die Speicher Anbieter Funktion (sofern Sie registriert oder installiert ist) mithilfe des [*Objekt Bezeichners*](../secgloss/o-gly.md) (OID) auf, der im *lpszstoreprovider* -Parameter übergeben wurde. Eine Liste der vordefinierten Anbieter Typen, die mit der CryptoAPI bereitgestellt werden, finden Sie unter **CertOpenStore**.

Die Speicher Anbieter Funktion kopiert die Zertifikate und [*Zertifikat Sperr Listen*](../secgloss/c-gly.md) (CRLs) in den Speicher internen Speicher, der durch das an Sie übergebenen *HCERTSTORE* -handle angegeben wird. Die neue Speicher Anbieter Funktion kann jede der kryptoapi-Zertifikat Speicherfunktionen, wie z. b. [**certaddcertificr econtexttostore**](/windows/win32/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore) oder [**certaddserializedelta**](/windows/win32/api/Wincrypt/nf-wincrypt-certaddserializedelementtostore)Token, zum Hinzufügen der Zertifikate und CRLs zum Speicher internen Speicher verwenden. Außerdem gibt die Store-Provider-Funktion optional Werte für alle Datenmember der [**Zertifikat \_ Speicher- \_ Prov- \_ Informations**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) Struktur zurück. Die Funktion muss diese Struktur nur aktualisieren, wenn Sie zusätzliche Rückruf Funktionen unterstützt. Wenn der Speicher z. b. ein Schreib geschützter Speicher wäre, wäre die Unterstützung anderer Rückruf Funktionen wahrscheinlich nicht erforderlich. Ausführliche Informationen und Prototypen der möglichen Rückruf Funktionen finden Sie unter [Rückruf Funktionen für Zertifikat Speicher Anbieter](cryptography-functions.md).

Der Speicher pro Benutzer-Treuhänder ist auf vordefinierte physische Speicher beschränkt. Sie können den Trust dpeople-Speicher pro Benutzer nicht erweitern. Sie können jedoch den Trust dpeople-Speicher des lokalen Computers erweitern.

**Windows XP und Windows Server 2003:** Der Trust-People-Speicher pro Benutzer ist nicht auf vordefinierte physische Speicher beschränkt.

Eines der Datenmember der [**CERT \_ Store \_ Prov \_ Info**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) -Struktur ist das *rgpvstoreprovfunc* -Array. Wenn die Speicher Anbieter Funktion eine oder mehrere der Rückruf Funktionen unterstützen muss, muss Sie Zeiger für dieses Array bereitstellen. Diese Zeiger müssen auf die Rückruf Funktionen verweisen, die für andere Zertifikat Speicher Aktivitäten verwendet werden sollen (z. b. das Schließen des Stores). Die folgende Abbildung zeigt den Ablauf dieses Prozesses.

![certopendstore-Funktionalität](images/openstor.png)

Wie in der folgenden Abbildung gezeigt, verwenden andere CryptoAPI-Funktionen (z. [**b. certclosestore**](/windows/win32/api/Wincrypt/nf-wincrypt-certclosestore)), nachdem der Speicher geöffnet wurde, das Array von Zeigern für den Zugriff auf die Rückruf Funktionen, die die beabsichtigte Aufgabe ausführen. Die Definition der [**CERT \_ Store \_ Prov- \_ Informations**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) Struktur und die Prototypen der Standard Rückruf Funktionen, die mit der CryptoAPI bereitgestellt werden, werden in den [Rückruf Funktionen des Zertifikat Speicher Anbieters](cryptography-functions.md)angezeigt.

![certclosestore-Funktionalität](images/closstor.png)

Die Store-APIs ermöglichen es einem Speicher Anbieter, die Zertifikate, CRLs und [*Zertifikat Vertrauens Listen*](../secgloss/c-gly.md) (CTLs) außerhalb des Cache Speichers des Speichers zu verwalten (z. b. eine externe Datenbank von Zertifikaten, z. b. von der Microsoft Certificate Server-Datenbank bereitgestellt).

[**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore) sendet den *pszstoreprovider* -Parameter an die entsprechende installierbare [**certdllopenstoreprov**](/windows/win32/api/Wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func) -Anbieter Funktion. Der Anbieter gibt Informationen im *pstoreprovinfo* -Parameter zurück, der auf eine [**Zertifikat \_ Speicher- \_ Prov- \_ Informations**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) Struktur verweist. Die **CERT \_ Store \_ Prov \_ Info** -Struktur enthält einen **dwstoreprovflags** -Member. Das Flag für das \_ externe Flag "cert store \_ Prov" \_ \_ wurde hinzugefügt, damit der Anbieter angeben kann, dass die Zertifikate, CRLs und CTLs für den Cache des Speichers extern sind.

[**Certdllopenstoreprov**](/windows/win32/api/Wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func) gibt ein Array von Rückruf Funktionen zurück. Ein Anbieter kann die folgenden Rückruf Funktionen implementieren:

-   CERT \_ Store \_ Prov \_ Close \_ Func
-   CERT \_ Store \_ Prov \_ Read \_ CERT \_ Func
-   CERT \_ Store \_ Prov \_ Write \_ CERT \_ Func
-   CERT \_ Store \_ Prov \_ Delete \_ CERT \_ Func
-   CERT \_ Store \_ Prov \_ Set \_ CERT- \_ Eigenschaft \_ Func
-   CERT \_ Store \_ Prov \_ Read \_ CRL \_ Func
-   CERT \_ Store \_ Prov \_ Write \_ CRL \_ Func
-   CERT \_ Store \_ Prov \_ Delete \_ CRL \_ Func
-   Zertifikat Sperr Listen-Eigenschaft (CRL) für Zertifikat \_ Speicher \_ Prov \_ festlegen \_ \_ \_
-   CERT \_ Store \_ Prov \_ Read \_ CTL \_ Func
-   CERT \_ Store \_ Prov \_ Write \_ CTL \_ Func
-   CERT \_ Store \_ Prov \_ Delete \_ CTL \_ Func
-   Zertifikat \_ Speicher \_ Prov \_ Set \_ CTL- \_ Eigenschaft \_ Func

Bei Aufrufen von "Write \_ CERT", "Write \_ CRL" und "Write \_ CTL Callback"-Funktionen beim Festlegen des "CERT \_ Store \_ Prov \_ Write Add"- \_ \_ Flags enthalten die oberen 16 Bits des *dwFlags* -Parameters den *dwadddisposition* -Wert. Um externe Speicher zu unterstützen, kann ein Anbieter die folgenden Rückruf Funktionen implementieren:

-   CERT \_ Store \_ Prov \_ Find \_ CERT \_ Func
-   Zertifikat \_ Speicher \_ Prov \_ Free \_ Find \_ CERT \_ Func
-   Zertifikat \_ Speicher \_ Prov \_ get \_ CERT- \_ Eigenschaft \_ Func
-   CERT \_ Store \_ Prov \_ Find \_ CRL \_ Func
-   CERT \_ Store \_ Prov \_ Free \_ Find \_ CRL \_ Func
-   Zertifikat \_ Speicher \_ Prov \_ get \_ CRL- \_ Eigenschaft \_ Func
-   Zertifikat \_ Speicher- \_ Prov \_ Find \_ CTL \_ Func
-   Zertifikat \_ Speicher \_ Prov \_ Free \_ Find \_ CTL \_ Func
-   Zertifikat \_ Speicher \_ Prov \_ get \_ CTL- \_ Eigenschaft \_ Func

Die Zertifikat Rückruf Funktionen verfügen über die folgenden Signaturen:

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

Die Signaturen für die CRL-und CTL-Rückruf Funktionen sind identisch mit dem obigen, wobei der Zeiger auf den [**CERT- \_ Kontext**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) durch einen Zeiger auf einen [**CRL- \_ Kontext**](/windows/win32/api/Wincrypt/ns-wincrypt-crl_context) oder einen [**CTL- \_ Kontext**](/windows/win32/api/Wincrypt/ns-wincrypt-ctl_context)ersetzt wurde.

Der Rückruf "Zertifikat suchen" \_ wird aufgerufen, wenn die Store-APIs Zertifikate aufzählen, suchen oder hinzufügen. *pprevcertcontext* und *ppvstoreprovfindinfo* sind auf **null** festgelegt, um eine neue Suche zu initiieren. Die zurückgegebene *ppvstoreprovfindinfo* wird bei der nächsten Suche zurückgegeben, ab der Sie vom Anbieter freigegeben werden kann. Der Anbieter kann alle, einige oder keine der Zertifikat Eigenschaften festlegen. Der Anbieter kann die Option zum Zurückstellen des Zertifikats aufrufen, bis der get \_ CERT- \_ Eigenschafts Rückruf aufgerufen wird. Es wird empfohlen, dass Anbieter so viele Eigenschaften wie möglich festlegen, um das Kopieren in einen anderen Speicher zuzulassen.

Die folgenden Typen von Zertifikat suchen werden in [**certfindcertifikateinstore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)unterstützt:

-   CERT \_ Find \_ Any
-   Zertifikat \_ Suche \_ SHA1- \_ Hash
-   Zertifikat \_ Suche \_ MD5- \_ Hash
-   CERT \_ Find- \_ Eigenschaft
-   \_ \_ öffentlicher \_ Schlüssel für Zertifikat Suche
-   Zertifikat suchantrags Teller \_ \_ \_ Name
-   CERT \_ Find \_ Subject \_ attr
-   Zertifikat \_ \_ \_ Suchname suchen
-   Zertifikat \_ Suche \_ Aussteller \_ attr
-   CERT \_ Find \_ Subject \_ Str \_ A
-   CERT \_ Find \_ Subject \_ Str \_ W
-   CERT \_ Find \_ Aussteller \_ Str \_ A
-   Zertifikat \_ Suche \_ Aussteller \_ Str \_ W
-   Zertifikat \_ Suche- \_ Schlüssel \_ Spezifikation
-   CERT \_ Find \_ enhkey- \_ Verwendung

Der Rückruf "Zertifikat suchen" \_ wird für jeden der obigen Suchtypen aufgerufen. Die an " [**certfindcertifikateinstore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) " übergebenen Parameter werden direkt in die "CERT \_ Store \_ Prov Find Info"-Struktur kopiert, \_ bevor der Befehl " \_ Zertifikat suchen" \_ aufgerufen wird. Ausführliche Informationen zu den Feldwerten für die verschiedenen Suchtypen der CERT \_ Store \_ Prov Find Info-Struktur finden Sie unter \_ \_ **certfindcertifikateinstore**.

Die folgenden Typen von Zertifikat suchen unterstützen die Zertifikate [**certgetsubjetcertifipeefromstore**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) und [**CertGetIssuerCertificateFromStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetissuercertificatefromstore) und helfen, zu bestimmen, ob das Zertifikat bereits im Speicher vorhanden ist, bevor Sie Folgendes hinzufügen:

-   CERT \_ Find \_ Subject \_ CERT
-   Zertifikat \_ Suche \_ Aussteller \_ von
-   Zertifikat \_ Suche \_ vorhanden

Für CERT \_ Find \_ Subject \_ CERT zeigt der *pvfindpara* -Parameter auf eine [**CERT \_ Info**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_info) -Struktur, die den Aussteller und die serialNumber des Subjekts enthält. Für \_ den Zertifikat \_ suchaussteller \_ von verweist *pvfindpara* auf eine [**CERT- \_ Kontext**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) Struktur des Subjekts. Für \_ \_ ein vorhandenes Zertifikat suchen zeigt *pvfindpara* auf einen Zertifikat **\_ Kontext** des Zertifikats, um zu überprüfen, ob es im Speicher vorhanden ist.

Der kostenlose \_ Find \_ CERT-Rückruf wird aufgerufen, wenn das vom Zertifikat "Find CERT" zurückgegebene Zertifikat \_ nicht freigegeben wurde, indem es in einem nachfolgenden nächsten Such Zertifikat verwendet wird, sodass der \_ [*Verweis Zähler*](../secgloss/r-gly.md) auf NULL dekrementiert wurde oder durch einen Aufruf von " [**certclosestore**](/windows/win32/api/Wincrypt/nf-wincrypt-certclosestore)" freigegeben wurde. Vor dem Aufruf des schließenden Rückrufs sollten alle vom Zertifikat suchen-Rückruf zurückgegebenen Zertifikate \_ für den Anbieter freigegeben werden, indem Sie an einen Aufruf des Zertifikats zum Suchen von \_ CERT oder einen Aufruf des kostenlosen c#-Zertifikats-Rückrufs übermittelt werden \_ \_ . Das gleiche gilt für die CRL-und CTL-Rückrufe.

Der get \_ CERT- \_ Eigenschafts Rückruf wird von [**certgetcertifierecontextproperty**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) aufgerufen, wenn er die angegebene Eigenschaft für den *pcertcontext* -Parameter nicht finden kann. Das gleiche gilt für die get \_ CRL \_ -Eigenschaft und die get \_ CTL- \_ Eigenschaft.

Der get \_ CRL-Rückruf wird aufgerufen, wenn die Store-APIs CRLs aufzählen oder Abrufen und bevor Sie eine Zertifikat Sperr Liste hinzufügen. Die folgenden Arten von CRL-suchen werden definiert:

Bei \_ der von ausgegebenen CRL-Suche \_ \_ von ist *pvfindpara* ein Zeiger auf einen [**CERT- \_ Kontext**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) des Zertifikats der CRL. Wenn die CRL- \_ Suche \_ vorhanden ist, ist *pvfindpara* ein Zeiger auf einen [**CRL- \_ Kontext**](/windows/win32/api/Wincrypt/ns-wincrypt-crl_context) der CRL, um zu bestimmen, ob er bereits im Speicher vorhanden ist.

Der CTL-Rückruf "Find" \_ wird aufgerufen, wenn die Store-APIs CTLs aufzählen oder suchen. Die folgenden Typen von CTL-suchen werden in [**certfindctlinstore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindctlinstore)unterstützt:

-   CTL- \_ Suche \_
-   CTL- \_ Suche \_ SHA1- \_ Hash
-   CTL- \_ Suche \_ MD5- \_ Hash
-   Verwendung der CTL- \_ Suche \_
-   CTL-Such \_ \_ Betreff
-   CTL- \_ Suche \_ vorhanden

Der CTL-Rückruf "Find" \_ wird für jeden der obigen Suchtypen aufgerufen. Die an [**certfindctlinstore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindctlinstore) übergebenen Parameter werden direkt in die "CERT \_ Store \_ Prov Find Info"-Struktur kopiert, \_ \_ bevor der CTL-Rückruf "Find" \_ aufgerufen wird. Ausführliche Informationen zu den Feldwerten für die verschiedenen Suchtypen der CERT \_ Store \_ Prov Find Info-Struktur finden Sie unter \_ \_ **certfindctlinstore**.

Mit dem CTL- \_ \_ Suchtyp "vorhandene CTL suchen" können Sie ermitteln, ob die CTL bereits im Speicher vorhanden ist, bevor Sie ein CTL-Add-in

Für die CTL- \_ Suche \_ ist " *pvfindpara* " ein Zeiger auf die [**CTL- \_ Kontext**](/windows/win32/api/Wincrypt/ns-wincrypt-ctl_context) Struktur der CTL, um zu bestimmen, ob Sie bereits im Speicher vorhanden ist.

 

 
