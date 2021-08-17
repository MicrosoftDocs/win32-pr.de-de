---
description: Implementiert die IX509Enrollment-Schnittstelle.
ms.assetid: bcf5c2f0-b99f-4de5-83f4-44f17dc31cd4
title: Zertifikatantwortfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f82922ce2b0cdfad370bbfbf4d1fd3a135c19d5ba613110364f7283ec12a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902400"
---
# <a name="certificate-response-functions"></a>Zertifikatantwortfunktionen

CertEnroll.dll implementiert die [**IX509Enrollment-Schnittstelle,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) um eine Clientzertifikatanforderung zu übermitteln und die Antwort von einer [*Zertifizierungsstelle*](/windows/desktop/SecGloss/c-gly) zu installieren.

Der Registrierungsprozess kann die folgenden drei Szenarien unterstützen:

<dl> Out-of-Band-Registrierung

1.  Rufen Sie eine beliebige Initialisierungsmethode auf, die vom [**IX509Enrollment-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) implementiert wird.
2.  Rufen Sie die [**CreateRequest-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) auf, um die Anforderung abzurufen.
3.  Übermitteln Sie die Anforderung out-of-band (manuell oder mithilfe eines anderen Prozesses).
4.  Empfangen der Antwort von einer Zertifizierungsstelle.
5.  Rufen Sie die [**InstallResponse-Methode auf.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)

  
Automatische Registrierung

1.  Rufen Sie eine beliebige Initialisierungsmethode auf, die vom [**IX509Enrollment-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) implementiert wird.
2.  Rufen Sie die [**Enroll-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) auf.

  
Verzögerte Registrierung

1.  Rufen Sie eine beliebige Initialisierungsmethode auf, die vom [**IX509Enrollment-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) implementiert wird.
2.  Rufen Sie die [**CreateRequest-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) auf, um die Anforderung abzurufen.
3.  Store die Anforderung, bis Sie bereit sind, sie zu übermitteln.
4.  Wenn Sie zur Registrierung bereit sind, rufen Sie die [**Initialize-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-initialize) auf, um das Registrierungsobjekt erneut zu initialisieren.
5.  Rufen Sie die [**InstallResponse-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) auf, wenn die Zertifizierungsstelle ein Zertifikat zurückgibt.

  
</dl>

Während des Registrierungsprozesses können Sie die [**Status-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_status) für das [**IX509Enrollment-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) aufrufen, um einen [**EnrollmentEnrollStatus-Enumerationswert**](/windows/desktop/api/CertEnroll/ne-certenroll-enrollmentenrollstatus) abzurufen, der angibt, ob die Registrierung erfolgreich war, aussteht, übersprungen wurde, einen Fehler generiert hat oder verweigert wurde.

Jeder der folgenden Abschnitte identifiziert eine Funktion, die von Xenroll.dll exportiert wird, um eine Zertifikatantwort von einer Zertifizierungsstelle zu installieren. In jedem Abschnitt wird auch erläutert, wie CertEnroll.dll verwendet wird, um die Funktion zu ersetzen, oder gibt an, dass keine Zuordnung zwischen den beiden Bibliotheken vorhanden ist:

-   [acceptFilePKCS7WStr](#acceptfilepkcs7wstr)
-   [acceptFileResponseWStr](#acceptfileresponsewstr)
-   [acceptPKCS7Blob](#acceptpkcs7blob)
-   [acceptResponseBlob](#acceptresponseblob)
-   [getCertContextFromFileResponseWStr](#getcertcontextfromfileresponsewstr)
-   [getCertContextFromPKCS7](#getcertcontextfrompkcs7)
-   [getCertContextFromResponseBlob](#getcertcontextfromresponseblob)
-   [InstallPKCS7Blob](#installpkcs7blobex)
-   [InstallPKCS7BlobEx](#installpkcs7blobex)
-   [SPCFileNameWStr](#spcfilenamewstr)
-   [WriteCertToCSP](#writecerttocsp)
-   [WriteCertToUserDS](#writecerttouserds)
-   [Zugehörige Themen](#related-topics)

## <a name="acceptfilepkcs7wstr"></a>acceptFilePKCS7WStr

Die [**acceptFilePKCS7WStr-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptfilepkcs7wstr) in Xenroll.dll installiert eine [*PKCS \# 7-Antwort*](/windows/desktop/SecGloss/p-gly) aus einer Datei.

Die CertEnroll.dll-Bibliothek implementiert die Funktionalität zum Installieren einer PKCS \# 7-Zertifikatantwort aus einer Datei nicht direkt. Sie können jedoch eine benutzerdefinierte Funktion erstellen, um die Dateidaten in ein Bytearray zu lesen und [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) aufzurufen, um die Antwort zu installieren.

Wenn Sie den **AllowNoOutstandingRequest-Wert** der [**InstallResponseRestrictionFlags-Enumeration**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) für den ersten Parameter von [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)angeben, muss kein Dummyzertifikat vorhanden sein, sodass Sie ein Zertifikat installieren können, ohne zuerst [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) oder [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest)aufzurufen. Wenn Sie jedoch ein Zertifikat mithilfe eines Webskripts installieren, muss ein Dummyzertifikat im Anforderungsspeicher vorhanden sein. Daher müssen Sie **AllowNone** für den ersten Parameter angeben.

## <a name="acceptfileresponsewstr"></a>acceptFileResponseWStr

Die [**acceptFileResponseWStr-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-acceptfileresponsewstr) in Xenroll.dll installiert eine PKCS \# 7- oder CMC-Zertifikatantwort aus einer Datei.

Die CertEnroll.dll Bibliothek implementiert die Funktionalität zum Installieren einer Zertifikatantwort aus einer Datei nicht direkt. Sie können jedoch eine benutzerdefinierte Funktion erstellen, um die Dateidaten in ein Bytearray zu lesen und [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) aufzurufen, um die PKCS \# 7- oder CMC-Antwort zu installieren.

Wenn Sie den **AllowNoOutstandingRequest-Wert** der [**InstallResponseRestrictionFlags-Enumeration**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) für den ersten Parameter von [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)angeben, muss kein Dummyzertifikat vorhanden sein, sodass Sie ein Zertifikat installieren können, ohne zuerst [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) oder [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest)aufzurufen. Wenn Sie jedoch ein Zertifikat mithilfe eines Webskripts installieren, muss ein Dummyzertifikat im Anforderungsspeicher vorhanden sein. Daher müssen Sie **AllowNone** für den ersten Parameter angeben.

## <a name="acceptpkcs7blob"></a>acceptPKCS7Blob

Die [**acceptPKCS7Blob-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptpkcs7blob) in Xenroll.dll installiert eine PKCS \# 7-Antwort, die in einem Bytearray enthalten ist.

Sie können [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) aufrufen, um eine PKCS \# 7-Nachricht zu installieren. Wenn Sie den **AllowNoOutstandingRequest-Wert** der [**InstallResponseRestrictionFlags-Enumeration**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) für den ersten Parameter von [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)angeben, muss kein Dummyzertifikat vorhanden sein, sodass Sie die PKCS 7-Antwort installieren können, \# ohne zuerst Enroll oder [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) [**aufzurufen.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) Wenn Sie jedoch ein Zertifikat mithilfe eines Webskripts installieren, muss ein Dummyzertifikat im Anforderungsspeicher vorhanden sein. Daher müssen Sie **AllowNone** für den ersten Parameter angeben.

## <a name="acceptresponseblob"></a>acceptResponseBlob

Die [**acceptResponseBlob-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-acceptresponseblob) in Xenroll.dll installiert eine PKCS \# 7- oder CMC-Zertifikatantwort, die in einem Bytearray enthalten ist.

Sie können [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) aufrufen, um eine PKCS \# 7- oder CMC-Antwort zu installieren. Wenn Sie den **AllowNoOutstandingRequest-Wert** der [**InstallResponseRestrictionFlags-Enumeration**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) für den ersten Parameter von [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)angeben, muss kein Dummyzertifikat vorhanden sein, sodass Sie die Antwort installieren können, ohne zuerst Enroll oder [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) [**aufzurufen.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) Wenn Sie jedoch ein Zertifikat mithilfe eines Webskripts installieren, muss ein Dummyzertifikat im Anforderungsspeicher vorhanden sein. Daher müssen Sie **AllowNone** für den ersten Parameter angeben.

## <a name="getcertcontextfromfileresponsewstr"></a>getCertContextFromFileResponseWStr

Die [**getCertContextFromFileResponseWStr-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getcertcontextfromfileresponsewstr) in Xenroll.dll ruft das Clientzertifikat aus einer Datei ab.

Die CertEnroll.dll Bibliothek implementiert nicht direkt Funktionen zum Abrufen eines Zertifikats aus einer in einer Datei gespeicherten Antwort der Zertifizierungsstelle. Sie können jedoch eine benutzerdefinierte Funktion erstellen, um die Dateidaten in ein Bytearray zu lesen und [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) aufzurufen, um die PKCS \# 7- oder CMC-Antwort zu installieren, und die [**Certificate-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificate) aufrufen, um das Zertifikat abzurufen.

Wenn Sie den **AllowNoOutstandingRequest-Wert** der [**InstallResponseRestrictionFlags-Enumeration**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) für den ersten Parameter von [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)angeben, muss kein Dummyzertifikat vorhanden sein, sodass Sie ein Zertifikat installieren können, ohne zuerst [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) oder [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest)aufzurufen. Wenn Sie jedoch ein Zertifikat mithilfe eines Webskripts installieren, muss ein Dummyzertifikat im Anforderungsspeicher vorhanden sein. Daher müssen Sie **AllowNone** für den ersten Parameter angeben.

## <a name="getcertcontextfrompkcs7"></a>getCertContextFromPKCS7

Die [**getCertContextFromPKCS7-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-getcertcontextfrompkcs7) in Xenroll.dll ruft das Clientzertifikat aus einer PKCS \# 7-Antwort ab.

Sie können die [**Certificate-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificate) für das [**IX509Enrollment-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) aufrufen, um ein Zertifikat abzurufen, nachdem Sie die [**Enroll-**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) oder [**InstallResponse-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) aufgerufen haben.

## <a name="getcertcontextfromresponseblob"></a>getCertContextFromResponseBlob

Die [**getCertContextFromResponseBlob-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getcertcontextfromresponseblob) in Xenroll.dll ruft ein Clientzertifikat aus einer PKCS \# 7- oder CMC-Antwort ab.

Sie können die [**Certificate-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificate) für das [**IX509Enrollment-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) aufrufen, um ein Zertifikat abzurufen, nachdem Sie die [**Enroll-**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) oder [**InstallResponse-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) aufgerufen haben.

## <a name="installpkcs7blob"></a>InstallPKCS7Blob

Die [**InstallPKCS7Blob-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-installpkcs7blob) in Xenroll.dll installiert eine PKCS \# 7-Antwort.

Sie können [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) aufrufen, um eine PKCS \# 7- oder CMC-Antwort zu installieren. Wenn Sie den **AllowNoOutstandingRequest-Wert** der [**InstallResponseRestrictionFlags-Enumeration**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) für den ersten Parameter von [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)angeben, muss kein Dummyzertifikat vorhanden sein, sodass Sie die Antwort installieren können, ohne zuerst Enroll oder [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) [**aufzurufen.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) Wenn Sie jedoch ein Zertifikat mithilfe eines Webskripts installieren, muss ein Dummyzertifikat im Anforderungsspeicher vorhanden sein. Daher müssen Sie **AllowNone** für den ersten Parameter angeben.

## <a name="installpkcs7blobex"></a>InstallPKCS7BlobEx

Die [**InstallPKCS7BlobEx-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-installpkcs7blobex) in Xenroll.dll installiert eine PKCS \# 7-Antwort und gibt die Anzahl der installierten Zertifikate zurück.

Sie können [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) aufrufen, um eine PKCS \# 7- oder CMC-Antwort zu installieren. Wenn Sie den **AllowNoOutstandingRequest-Wert** der [**InstallResponseRestrictionFlags-Enumeration**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) für den ersten Parameter von [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)angeben, muss kein Dummyzertifikat vorhanden sein, sodass Sie die Antwort installieren können, ohne zuerst Enroll oder [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) [**aufzurufen.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) Wenn Sie jedoch ein Zertifikat mithilfe eines Webskripts installieren, muss ein Dummyzertifikat im Anforderungsspeicher vorhanden sein. Daher müssen Sie **AllowNone** für den ersten Parameter angeben.

## <a name="spcfilenamewstr"></a>SPCFileNameWStr

Die [**SPCFileNameWStr-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_spcfilenamewstr) in Xenroll.dll gibt den Namen der Datei an, in der die Zertifikatantwort gespeichert werden soll, oder ruft diesen ab. Die bibliothek CertEnroll.dll implementiert keine Funktionen, mit denen Sie ein Zertifikat in eine bestimmte Datei kopieren können. Beim Registrierungsprozess wird die Zertifikatkette automatisch in Dateien in den entsprechenden Speichern installiert.

## <a name="writecerttocsp"></a>WriteCertToCSP

Die [**WriteCertToCSP-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_writecerttocsp) in Xenroll.dll gibt einen booleschen Wert an oder ruft einen booleschen Wert ab, der angibt, ob ein Zertifikat in einen [*Kryptografiedienstanbieter (Cryptographic Service Provider,*](/windows/desktop/SecGloss/c-gly) CSP) geschrieben werden soll. Wenn diese Funktion aufgerufen wird, ist der Anbieter in der Regel eine [*Smartcard.*](/windows/desktop/SecGloss/s-gly)

Wenn ein Client in CertEnroll.dll die [**Enroll-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) aufruft, um eine Anforderung für ein Smartcardzertifikat zu übermitteln, und ein Zertifikat ausgestellt wird, installiert [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) das Zertifikat automatisch auf der Smartcard, vorausgesetzt, die Karte wird im Reader installiert. Die [**InstallResponse-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) schreibt das Zertifikat auch automatisch auf die Smartcard.

## <a name="writecerttouserds"></a>WriteCertToUserDS

Die [**WriteCertToUserDS-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_writecerttouserds) in Xenroll.dll gibt einen booleschen Wert an oder ruft einen booleschen Wert ab, der angibt, ob ein Zertifikat im Active Directory-Speicher gespeichert werden soll. Die CertEnroll.dll-Bibliothek implementiert keine Funktionen, mit denen Sie einen Speicher angeben können, in den ein Zertifikat kopiert werden soll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnen Xenroll.dll zu CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

 
