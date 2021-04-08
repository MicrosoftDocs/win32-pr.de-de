---
description: Von Xenroll.dll exportierte Funktionen, die zum Verwalten eines Kryptografieanbieters verwendet werden können.
ms.assetid: 4f6f353d-6b06-45b4-8808-56998d3727a4
title: Kryptografiedienstanbieter-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a981b418271ba834352c0301c005b39742729a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750024"
---
# <a name="cryptographic-service-provider-functions"></a>Kryptografiedienstanbieter-Funktionen

Jeder der folgenden Abschnitte gibt eine Funktion an, die von Xenroll.dll exportiert und zum Verwalten eines Kryptografieanbieters verwendet werden kann. Jedes Thema erläutert auch, wie CertEnroll.dll verwendet wird, um die Funktion zu ersetzen, oder gibt an, dass keine Zuordnung zwischen den beiden Bibliotheken vorhanden ist:

-   [Enumalgs](#enumalgs)
-   [enumcontainertaustr](#enumcontainerswstr)
-   [enumprovidertaustr](#enumproviderswstr)
-   [Getalgnamewstr](#getalgnamewstr)
-   [getprovidertypewstr](#getprovidertypewstr)
-   [HashAlgId](#hashalgid)
-   [Hashalgorithmwstr](#hashalgorithmwstr)
-   [Providerflags](#providerflags)
-   [Providernamewstr](#providernamewstr)
-   [ProviderType](#getprovidertypewstr)
-   [Zugehörige Themen](#related-topics)

## <a name="enumalgs"></a>Enumalgs

Die [**enumalgs**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-enumalgs) -Funktion in Xenroll.dll ruft eine kryptografiealgorithmusauflistung ab.

Wenn Sie CertEnroll.dll verwenden, können Sie die folgenden Aktionen ausführen, um Informationen zu den von einem [*Kryptografiedienstanbieter*](/windows/desktop/SecGloss/c-gly) (CSP) unterstützten Algorithmen abzurufen:

1.  Ruft die [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) -Eigenschaft für ein vorhandenes [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt auf.
2.  Rufen Sie die [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) -Methode für die Anforderung auf, die in Schritt 1 zurückgegeben wurde, um die innerste Anforderung abzurufen.
3.  Ruft **QueryInterface** für das [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) -Objekt auf, das von Schritt 2 zum Umwandeln in ein [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -Objekt zurückgegeben wird.
4.  Aufrufen der [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) -Eigenschaft für die PKCS \# 10-Anforderung.
5.  Nennen Sie die [**cspinformation**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_cspinformations) -Eigenschaft für das [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) -Objekt, das aus Schritt 4 abgerufen wurde.
6.  Nennen Sie die [**cspalgorithmen**](/windows/desktop/api/CertEnroll/nf-certenroll-icspinformation-get_cspalgorithms) -Eigenschaft für ein bestimmtes [**icspinformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) -Objekt in der [**icspinformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) -Auflistung, die Sie in Schritt 5 abgerufen haben.

## <a name="enumcontainerswstr"></a>enumcontainertaustr

Die [**enumcontainertaustr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-enumcontainerswstr) -Funktion in Xenroll.dll ruft einen Schlüssel Container aus der Auflistung nach Index ab.

Diese Funktion wird von der CertEnroll.dll Bibliothek nicht direkt implementiert.

## <a name="enumproviderswstr"></a>enumprovidertaustr

Die [**enumprovidertaustr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-enumproviderswstr) -Funktion in Xenroll.dll ruft einen CSP aus der Auflistung nach Index ab.

Wenn Sie CertEnroll.dll verwenden, können Sie die folgenden Aktionen ausführen, um die Sammlung der Kryptografiecontainer abzurufen:

1.  Ruft die [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) -Eigenschaft für ein vorhandenes [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt auf.
2.  Rufen Sie die [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) -Methode für die Anforderung auf, die in Schritt 1 zurückgegeben wurde, um die innerste Anforderung abzurufen.
3.  Ruft **QueryInterface** für das [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) -Objekt auf, das von Schritt 2 zum Umwandeln in ein [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -Objekt zurückgegeben wird.
4.  Aufrufen der [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) -Eigenschaft für die PKCS \# 10-Anforderung.
5.  Nennen Sie die [**cspinformation**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_cspinformations) -Eigenschaft für das [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) -Objekt, das aus Schritt 4 abgerufen wurde.

## <a name="getalgnamewstr"></a>Getalgnamewstr

Die [**getalgnamewstr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getalgnamewstr) -Funktion in Xenroll.dll ruft den Namen eines [*kryptografischen Algorithmus*](/windows/desktop/SecGloss/c-gly)ab.

Wenn Sie CertEnroll.dll verwenden, können Sie die folgenden Aktionen ausführen, um den Algorithmusnamen abzurufen:

1.  Ruft die [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) -Eigenschaft für ein vorhandenes [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt auf.
2.  Rufen Sie die [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) -Methode für die Anforderung auf, die in Schritt 1 zurückgegeben wurde, um die innerste Anforderung abzurufen.
3.  Ruft **QueryInterface** für das [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) -Objekt auf, das von Schritt 2 zum Umwandeln in ein [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -Objekt zurückgegeben wird.
4.  Aufrufen der [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) -Eigenschaft für die PKCS \# 10-Anforderung.
5.  Rufen Sie die [**algorithmuseigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_algorithm) des [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) -Objekts auf, um den algorithmusobjektbezeichner abzurufen.
6.  Rufen Sie die [**FriendlyName**](/windows/desktop/api/CertEnroll/nf-certenroll-iobjectid-get_friendlyname) -Eigenschaft für die [**iobjectid**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) -Schnittstelle auf, um den anzeigen amen des Algorithmus abzurufen.

## <a name="getprovidertypewstr"></a>getprovidertypewstr

Die [**getprovidertypewstr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getprovidertypewstr) -Funktion in Xenroll.dll ruft den Typ des Kryptografieanbieters ab.

Wenn Sie CertEnroll.dll verwenden, können Sie die folgenden Aktionen ausführen, um den Anbietertyp abzurufen:

1.  Ruft die [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) -Eigenschaft für ein vorhandenes [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt auf.
2.  Rufen Sie die [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) -Methode für die Anforderung auf, die in Schritt 1 zurückgegeben wurde, um die innerste Anforderung abzurufen.
3.  Ruft **QueryInterface** für das [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) -Objekt auf, das von Schritt 2 zum Umwandeln in ein [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -Objekt zurückgegeben wird.
4.  Aufrufen der [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) -Eigenschaft für die PKCS \# 10-Anforderung.
5.  Nennen Sie die [**ProviderType**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providertype) -Eigenschaft für das [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) -Objekt, das aus Schritt 4 abgerufen wurde.

## <a name="hashalgid"></a>HashAlgId

Die [**HashAlgId**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_hashalgid) -Funktion in Xenroll.dll ruft einen ganzzahligen Wert ab, der die ID des Algorithmus enthält, der zum Signieren einer Anforderung verwendet wird.

Wenn Sie CertEnroll.dll verwenden, können Sie die folgenden Aktionen ausführen, um den Hash Algorithmus abzurufen:

-   Rufen Sie eine [**IX509SignatureInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) -Schnittstelle ab, indem Sie die [**signatureinformation**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_signatureinformation) -Eigenschaft für eine PKCS \# 10-oder eine CMC-Anforderung oder die [**SignerCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_signercertificate) -Eigenschaft einer [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) -Anforderung aufrufen.
-   Rufen Sie die [**HashAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509signatureinformation-get_hashalgorithm) -Eigenschaft für das Signatur Informationsobjekt auf, um den Objekt Bezeichner für den Hash Algorithmus abzurufen.

## <a name="hashalgorithmwstr"></a>Hashalgorithmwstr

Die [**hashalgorithmwstr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_hashalgorithmwstr) -Funktion in Xenroll.dll gibt einen Zeichen folgen Wert an oder ruft ihn ab, der den Hash Algorithmus identifiziert, der zum Signieren einer Anforderung verwendet wird.

Wenn Sie CertEnroll.dll verwenden, können Sie die folgenden Aktionen ausführen, um den Hash Algorithmus abzurufen:

-   Rufen Sie eine [**IX509SignatureInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) -Schnittstelle ab, indem Sie die [**signatureinformation**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_signatureinformation) -Eigenschaft für eine PKCS \# 10-oder eine CMC-Anforderung oder die [**SignerCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_signercertificate) -Eigenschaft einer PKCS \# 7-Anforderung aufrufen.
-   Rufen Sie die [**HashAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509signatureinformation-get_hashalgorithm) -Eigenschaft für das Signatur Informationsobjekt auf, um den Objekt Bezeichner für den Hash Algorithmus abzurufen.
-   Rufen Sie die [**FriendlyName**](/windows/desktop/api/CertEnroll/nf-certenroll-iobjectid-get_friendlyname) -Eigenschaft der [**iobjectid**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) -Schnittstelle auf, die in Schritt 2 zurückgegeben wurde, um den anzeigen amen des Algorithmus abzurufen

## <a name="providerflags"></a>Providerflags

Die [**providerflags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providerflags) -Funktion in Xenroll.dll gibt die Flags an, die beim Abrufen eines Handles für einen CSP verwendet werden, oder ruft Sie ab.

Diese Funktion wird von der CertEnroll.dll Bibliothek nicht perfekt zugeordnet, aber Sie können umfangreiche Eigenschafts Informationen aus dem Registrierungs Objekt und dem [*privaten Schlüssel*](/windows/desktop/SecGloss/p-gly)abrufen. Weitere Informationen finden Sie unter Überprüfen der Eigenschaften, die von den Schnittstellen [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) und [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) verfügbar gemacht werden.

## <a name="providernamewstr"></a>Providernamewstr

Die [**providernamewstr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providernamewstr) -Funktion in Xenroll.dll gibt den Namen eines CSP an oder ruft ihn ab.

Wenn Sie CertEnroll.dll verwenden, können Sie die folgenden Aktionen ausführen, um den Anbieter Namen abzurufen:

1.  Ruft die [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) -Eigenschaft für ein vorhandenes [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt auf.
2.  Rufen Sie die [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) -Methode für die Anforderung auf, die in Schritt 1 zurückgegeben wurde, um die innerste Anforderung abzurufen.
3.  Ruft **QueryInterface** für das [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) -Objekt auf, das von Schritt 2 zum Umwandeln in ein [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -Objekt zurückgegeben wird.
4.  Aufrufen der [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) -Eigenschaft für die PKCS \# 10-Anforderung.
5.  Nennen Sie die [**providerName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providername) -Eigenschaft für das [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) -Objekt, das aus Schritt 4 abgerufen wurde.

## <a name="providertype"></a>ProviderType

Die [**ProviderType**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providertype) -Funktion in Xenroll.dll gibt einen ganzzahligen Wert an, der den Typ des CSP identifiziert, oder ruft ihn ab.

Wenn Sie CertEnroll.dll verwenden, können Sie die folgenden Aktionen ausführen, um den Anbietertyp abzurufen:

1.  Ruft die [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) -Eigenschaft für ein vorhandenes [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt auf.
2.  Rufen Sie die [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) -Methode für die Anforderung auf, die in Schritt 1 zurückgegeben wurde, um die innerste Anforderung abzurufen.
3.  Ruft **QueryInterface** für das [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) -Objekt auf, das von Schritt 2 zum Umwandeln in ein [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -Objekt zurückgegeben wird.
4.  Aufrufen der [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) -Eigenschaft für die PKCS \# 10-Anforderung.
5.  Nennen Sie die [**ProviderType**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providertype) -Eigenschaft für das [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) -Objekt, das aus Schritt 4 abgerufen wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnung von Xenroll.dll zu CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**Icspalgorithmus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithm)
</dt> <dt>

[**Icspalgorithmen**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithms)
</dt> <dt>

[**Icspinformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation)
</dt> <dt>

[**Icspinformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations)
</dt> <dt>

[**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> <dt>

[**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)
</dt> </dl>

 

 
