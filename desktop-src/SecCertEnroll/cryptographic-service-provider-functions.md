---
description: Funktionen, die von Xenroll.dll, die zum Verwalten eines Kryptografieanbieters verwendet werden können.
ms.assetid: 4f6f353d-6b06-45b4-8808-56998d3727a4
title: Funktionen des Kryptografiedienstanbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 947d9c4f2529071b28052ae5ca34f811d4657c3fd4cede23285999cbaa13a72c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883080"
---
# <a name="cryptographic-service-provider-functions"></a>Funktionen des Kryptografiedienstanbieters

In jedem der folgenden Abschnitte wird eine Funktion identifiziert, die von Xenroll.dll, die zum Verwalten eines Kryptografieanbieters verwendet werden kann. In jedem Thema wird auch erläutert, wie sie CertEnroll.dll funktion ersetzen, oder gibt an, dass keine Zuordnung zwischen den beiden Bibliotheken vorhanden ist:

-   [EnumAlgs](#enumalgs)
-   [enumContainersWStr](#enumcontainerswstr)
-   [enumProvidersWStr](#enumproviderswstr)
-   [GetAlgNameWStr](#getalgnamewstr)
-   [getProviderTypeWStr](#getprovidertypewstr)
-   [HashAlgID](#hashalgid)
-   [HashAlgorithmWStr](#hashalgorithmwstr)
-   [ProviderFlags](#providerflags)
-   [ProviderNameWStr](#providernamewstr)
-   [ProviderType](#getprovidertypewstr)
-   [Zugehörige Themen](#related-topics)

## <a name="enumalgs"></a>EnumAlgs

Die [**EnumAlgs-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-enumalgs) in Xenroll.dll eine Kryptografiealgorithmussammlung ab.

Wenn Sie CertEnroll.dll, können Sie die folgenden Aktionen ausführen, um Informationen zu den Algorithmen abzurufen, die von einem Kryptografiedienstanbieter (Cryptographic [*Service Provider,*](/windows/desktop/SecGloss/c-gly) CSP) unterstützt werden:

1.  Rufen Sie [**die Request-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) für ein [**vorhandenes IX509Enrollment-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) auf.
2.  Rufen Sie [**die GetInnerRequest-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) für die anforderung auf, die aus Schritt 1 zurückgegeben wurde, um die innerste Anforderung abzurufen.
3.  Rufen **Sie QueryInterface** für [**das ix509CertificateRequest-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) auf, das aus Schritt 2 zurückgegeben wurde, um in ein [**IX509CertificateRequestPkcs10-Objekt zu**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) casten.
4.  Rufen Sie die [**PrivateKey-Eigenschaft**](/windows/desktop/SecCrypto/privatekey) in der PKCS \# 10-Anforderung auf.
5.  Rufen Sie [**die CspInformations-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_cspinformations) für das [**IX509PrivateKey-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) auf, das aus Schritt 4 abgerufen wurde.
6.  Rufen Sie [**die CspAlgorithms-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-icspinformation-get_cspalgorithms) für ein bestimmtes [**ICspInformation-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) in der [**ICspInformations-Auflistung**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) auf, die in Schritt 5 abgerufen wurde.

## <a name="enumcontainerswstr"></a>enumContainersWStr

Die [**enumContainersWStr-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-enumcontainerswstr) in Xenroll.dll ruft einen Schlüsselcontainer nach Index aus der Auflistung ab.

Die CertEnroll.dll-Bibliothek implementiert diese Funktionalität nicht direkt.

## <a name="enumproviderswstr"></a>enumProvidersWStr

Die [**enumProvidersWStr-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-enumproviderswstr) in Xenroll.dll ruft einen CSP nach Index aus der Auflistung ab.

Wenn Sie CertEnroll.dll, können Sie die folgenden Aktionen ausführen, um die Sammlung kryptografischer Container abzurufen:

1.  Rufen Sie [**die Request-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) für ein [**vorhandenes IX509Enrollment-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) auf.
2.  Rufen Sie [**die GetInnerRequest-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) für die anforderung auf, die aus Schritt 1 zurückgegeben wurde, um die innerste Anforderung abzurufen.
3.  Rufen **Sie QueryInterface** für [**das ix509CertificateRequest-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) auf, das aus Schritt 2 zurückgegeben wurde, um in ein [**IX509CertificateRequestPkcs10-Objekt zu**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) casten.
4.  Rufen Sie die [**PrivateKey-Eigenschaft**](/windows/desktop/SecCrypto/privatekey) in der PKCS \# 10-Anforderung auf.
5.  Rufen Sie [**die CspInformations-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_cspinformations) für das [**IX509PrivateKey-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) auf, das aus Schritt 4 abgerufen wurde.

## <a name="getalgnamewstr"></a>GetAlgNameWStr

Die [**GetAlgNameWStr-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getalgnamewstr) in Xenroll.dll ruft den Namen eines kryptografischen [*Algorithmus ab.*](/windows/desktop/SecGloss/c-gly)

Wenn Sie CertEnroll.dll, können Sie die folgenden Aktionen ausführen, um den Algorithmusnamen abzurufen:

1.  Rufen Sie [**die Request-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) für ein [**vorhandenes IX509Enrollment-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) auf.
2.  Rufen Sie [**die GetInnerRequest-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) für die anforderung auf, die aus Schritt 1 zurückgegeben wurde, um die innerste Anforderung abzurufen.
3.  Rufen **Sie QueryInterface** für [**das ix509CertificateRequest-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) auf, das aus Schritt 2 zurückgegeben wurde, um in ein [**IX509CertificateRequestPkcs10-Objekt zu**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) casten.
4.  Rufen Sie die [**PrivateKey-Eigenschaft**](/windows/desktop/SecCrypto/privatekey) in der PKCS \# 10-Anforderung auf.
5.  Rufen Sie die [**Algorithm-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_algorithm) für das [**IX509PrivateKey-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) auf, um den Algorithmusobjektbezeichner abzurufen.
6.  Rufen Sie die [**FriendlyName-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-iobjectid-get_friendlyname) auf der [**IObjectId-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) auf, um den Anzeigenamen des Algorithmus abzurufen.

## <a name="getprovidertypewstr"></a>getProviderTypeWStr

Die [**getProviderTypeWStr-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getprovidertypewstr) in Xenroll.dll ruft den Kryptografieanbietertyp ab.

Wenn Sie CertEnroll.dll, können Sie die folgenden Aktionen ausführen, um den Anbietertyp abzurufen:

1.  Rufen Sie [**die Request-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) für ein [**vorhandenes IX509Enrollment-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) auf.
2.  Rufen Sie [**die GetInnerRequest-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) für die anforderung auf, die aus Schritt 1 zurückgegeben wurde, um die innerste Anforderung abzurufen.
3.  Rufen **Sie QueryInterface** für [**das ix509CertificateRequest-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) auf, das aus Schritt 2 zurückgegeben wurde, um in ein [**IX509CertificateRequestPkcs10-Objekt zu**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) casten.
4.  Rufen Sie die [**PrivateKey-Eigenschaft**](/windows/desktop/SecCrypto/privatekey) in der PKCS \# 10-Anforderung auf.
5.  Rufen Sie [**die ProviderType-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providertype) für das [**IX509PrivateKey-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) auf, das aus Schritt 4 abgerufen wurde.

## <a name="hashalgid"></a>HashAlgID

Die [**HashAlgID-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_hashalgid) in Xenroll.dll ruft einen ganzzahligen Wert ab, der die ID des Algorithmus enthält, der zum Signieren einer Anforderung verwendet wird.

Wenn Sie CertEnroll.dll, können Sie die folgenden Aktionen ausführen, um den Hashalgorithmus abzurufen:

-   Rufen Sie eine [**IX509SignatureInformation-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) ab, indem Sie die [**SignatureInformation-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_signatureinformation) für eine PKCS 10- oder CMC-Anforderung oder die \# [**SignerCertificate-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_signercertificate) in einer [*PKCS \# 7-Anforderung*](/windows/desktop/SecGloss/p-gly) aufrufen.
-   Rufen Sie die [**HashAlgorithm-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509signatureinformation-get_hashalgorithm) für das Signaturinformationsobjekt auf, um den Hashalgorithmus-Objektbezeichner abzurufen.

## <a name="hashalgorithmwstr"></a>HashAlgorithmWStr

Die [**HashAlgorithmWStr-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_hashalgorithmwstr) in Xenroll.dll gibt einen Zeichenfolgenwert an oder ruft einen Zeichenfolgenwert ab, der den Hashalgorithmus identifiziert, der zum Signieren einer Anforderung verwendet wird.

Wenn Sie CertEnroll.dll, können Sie die folgenden Aktionen ausführen, um den Hashalgorithmus abzurufen:

-   Rufen Sie eine [**IX509SignatureInformation-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) ab, indem Sie die [**SignatureInformation-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_signatureinformation) für eine PKCS 10- oder CMC-Anforderung oder die \# [**SignerCertificate-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_signercertificate) in einer PKCS \# 7-Anforderung aufrufen.
-   Rufen Sie die [**HashAlgorithm-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509signatureinformation-get_hashalgorithm) für das Signaturinformationsobjekt auf, um den Hashalgorithmus-Objektbezeichner abzurufen.
-   Rufen Sie die [**FriendlyName-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-iobjectid-get_friendlyname) auf der [**IObjectId-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) auf, die in Schritt 2 zurückgegeben wurde, um den Anzeigenamen des Algorithmus abzurufen.

## <a name="providerflags"></a>ProviderFlags

Die [**ProviderFlags-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providerflags) in Xenroll.dll die Flags an, die beim Abrufen eines Handle für einen CSP verwendet werden, oder ruft sie ab.

Die CertEnroll.dll-Bibliothek lässt diese Funktion nicht perfekt zu, aber Sie können umfassende Eigenschaftsinformationen aus dem Registrierungsobjekt und dem [*privaten Schlüssel abrufen.*](/windows/desktop/SecGloss/p-gly) Weitere Informationen finden Sie in den Eigenschaften, die von den [**Schnittstellen IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) und [**IX509PrivateKey verfügbar gemacht**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) werden.

## <a name="providernamewstr"></a>ProviderNameWStr

Die [**ProviderNameWStr-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providernamewstr) in Xenroll.dll gibt den Namen eines CSP an oder ruft den Namen ab.

Wenn Sie CertEnroll.dll, können Sie die folgenden Aktionen ausführen, um den Anbieternamen abzurufen:

1.  Rufen Sie [**die Request-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) für ein [**vorhandenes IX509Enrollment-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) auf.
2.  Rufen Sie [**die GetInnerRequest-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) für die anforderung auf, die aus Schritt 1 zurückgegeben wurde, um die innerste Anforderung abzurufen.
3.  Rufen **Sie QueryInterface** für [**das ix509CertificateRequest-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) auf, das aus Schritt 2 zurückgegeben wurde, um in ein [**IX509CertificateRequestPkcs10-Objekt zu**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) casten.
4.  Rufen Sie die [**PrivateKey-Eigenschaft**](/windows/desktop/SecCrypto/privatekey) in der PKCS \# 10-Anforderung auf.
5.  Rufen Sie [**die ProviderName-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providername) für das [**IX509PrivateKey-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) auf, das aus Schritt 4 abgerufen wurde.

## <a name="providertype"></a>ProviderType

Die [**ProviderType-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providertype) in Xenroll.dll gibt einen ganzzahligen Wert an, der den Typ des CSP identifiziert, oder ruft diesen ab.

Wenn Sie CertEnroll.dll, können Sie die folgenden Aktionen ausführen, um den Anbietertyp abzurufen:

1.  Rufen Sie [**die Request-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) für ein [**vorhandenes IX509Enrollment-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) auf.
2.  Rufen Sie [**die GetInnerRequest-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) für die anforderung auf, die aus Schritt 1 zurückgegeben wurde, um die innerste Anforderung abzurufen.
3.  Rufen **Sie QueryInterface** für [**das ix509CertificateRequest-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) auf, das aus Schritt 2 zurückgegeben wurde, um in ein [**IX509CertificateRequestPkcs10-Objekt zu**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) casten.
4.  Rufen Sie die [**PrivateKey-Eigenschaft**](/windows/desktop/SecCrypto/privatekey) in der PKCS \# 10-Anforderung auf.
5.  Rufen Sie [**die ProviderType-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providertype) für das [**IX509PrivateKey-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) auf, das aus Schritt 4 abgerufen wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnen Xenroll.dll zu CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithm)
</dt> <dt>

[**ICspAlgorithms**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithms)
</dt> <dt>

[**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation)
</dt> <dt>

[**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations)
</dt> <dt>

[**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> <dt>

[**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)
</dt> </dl>

 

 
