---
description: Implementiert die IX509Enrollment-Schnittstelle.
ms.assetid: bcf5c2f0-b99f-4de5-83f4-44f17dc31cd4
title: Funktionen für Zertifikat Antworten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15eec71d0493fa4961988b86db0397d0fd516508
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347476"
---
# <a name="certificate-response-functions"></a>Funktionen für Zertifikat Antworten

CertEnroll.dll implementiert die [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Schnittstelle, um eine Client Zertifikat Anforderung zu senden und die Antwort von einer Zertifizierungsstelle ( [*Certification Authority*](/windows/desktop/SecGloss/c-gly) , ca) zu installieren.

Der Registrierungsvorgang kann die folgenden drei Szenarien erfüllen:

<dl> Out-of-Band-Registrierung

1.  Ruft eine beliebige Initialisierungs Methode auf, die vom [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt implementiert wird.
2.  Rufen Sie die Methode " [**kreaterequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) " auf, um die Anforderung abzurufen.
3.  Senden Sie die Anforderung out-of-Band (manuell oder mithilfe eines anderen Prozesses).
4.  Empfangen Sie die Antwort von einer Zertifizierungsstelle.
5.  Nennen Sie die [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) -Methode.

  
Automatische Registrierung

1.  Ruft eine beliebige Initialisierungs Methode auf, die vom [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt implementiert wird.
2.  Ruft die [**ENROLL**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) -Methode auf.

  
Verzögerte Registrierung

1.  Ruft eine beliebige Initialisierungs Methode auf, die vom [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt implementiert wird.
2.  Rufen Sie die Methode " [**kreaterequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) " auf, um die Anforderung abzurufen.
3.  Speichern Sie die Anforderung, bis Sie bereit sind, Sie zu senden.
4.  Wenn Sie zur Registrierung bereit sind, können Sie die [**Initialize**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-initialize) -Methode zum erneuten Initialisieren des anmeldungsobjekts aufzurufen.
5.  Ruft die [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) -Methode auf, wenn die Zertifizierungsstelle ein Zertifikat zurückgibt.

  
</dl>

Während des Registrierungsvorgangs können Sie die [**Status**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_status) -Eigenschaft für das [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt aufrufen, um einen-Registrierungs Registrierungs [**Status**](/windows/desktop/api/CertEnroll/ne-certenroll-enrollmentenrollstatus) -Enumerationswert abzurufen, der angibt, ob die Registrierung erfolgreich war, aussteht, abgebrochen wurde, ein Fehler generiert wurde oder verweigert wurde.

In den folgenden Abschnitten wird eine Funktion identifiziert, die von Xenroll.dll exportiert wird, um eine Zertifikat Antwort von einer Zertifizierungsstelle zu installieren. Außerdem wird in jedem Abschnitt erläutert, wie CertEnroll.dll verwendet wird, um die Funktion zu ersetzen, oder es wird angegeben, dass keine Zuordnung zwischen den beiden Bibliotheken besteht:

-   [acceptFilePKCS7WStr](#acceptfilepkcs7wstr)
-   [Accept-fileresponabwstr](#acceptfileresponsewstr)
-   [acceptPKCS7Blob](#acceptpkcs7blob)
-   [akzeptresponseeblob](#acceptresponseblob)
-   [getcertcontextfromfileresponabwstr](#getcertcontextfromfileresponsewstr)
-   [getCertContextFromPKCS7](#getcertcontextfrompkcs7)
-   [getcertcontextfromresponse-BLOB](#getcertcontextfromresponseblob)
-   [InstallPKCS7Blob](#installpkcs7blobex)
-   [InstallPKCS7BlobEx](#installpkcs7blobex)
-   [Spcdateinamewstr](#spcfilenamewstr)
-   ["Schreibcertto"](#writecerttocsp)
-   ["Schreibcerttouserds"](#writecerttouserds)
-   [Zugehörige Themen](#related-topics)

## <a name="acceptfilepkcs7wstr"></a>acceptFilePKCS7WStr

Die [**acceptFilePKCS7WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptfilepkcs7wstr) -Funktion in Xenroll.dll installiert eine [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) -Antwort aus einer Datei.

Die CertEnroll.dll Bibliothek implementiert nicht direkt Funktionen zum Installieren einer PKCS \# 7-Zertifikats Antwort aus einer Datei. Sie können jedoch eine benutzerdefinierte Funktion erstellen, um die Datei Daten in ein Bytearray zu lesen und [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) zum Installieren der Antwort aufzurufen.

Wenn Sie für den ersten Parameter von [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)den Wert **allownooutstandingrequest** der [**installresponserestrictionflags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) -Enumeration angeben, ist ein dummyzertifikat nicht vorhanden. Dadurch können Sie ein Zertifikat installieren, ohne zuerst " [**ENROLL**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) " oder " [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest)" aufrufen zu müssen. Wenn Sie ein Zertifikat jedoch mithilfe eines Webskripts installieren, muss im Anforderungs Speicher ein dummyzertifikat vorhanden sein. Daher müssen Sie für den ersten Parameter " **allownone** " angeben.

## <a name="acceptfileresponsewstr"></a>Accept-fileresponabwstr

Mit der Funktion " [**Accept-fileresponabwstr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-acceptfileresponsewstr) " in Xenroll.dll wird eine PKCS \# 7-oder CMC-Zertifikats Antwort aus einer Datei installiert.

Die CertEnroll.dll Bibliothek implementiert die Funktionalität nicht direkt, um eine Zertifikat Antwort aus einer Datei zu installieren. Sie können jedoch eine benutzerdefinierte Funktion erstellen, um die Datei Daten in ein Bytearray zu lesen und [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) zum Installieren der PKCS 7-oder der CMC-Antwort aufzurufen \# .

Wenn Sie für den ersten Parameter von [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)den Wert **allownooutstandingrequest** der [**installresponserestrictionflags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) -Enumeration angeben, ist ein dummyzertifikat nicht vorhanden. Dadurch können Sie ein Zertifikat installieren, ohne zuerst " [**ENROLL**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) " oder " [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest)" aufrufen zu müssen. Wenn Sie ein Zertifikat jedoch mithilfe eines Webskripts installieren, muss im Anforderungs Speicher ein dummyzertifikat vorhanden sein. Daher müssen Sie für den ersten Parameter " **allownone** " angeben.

## <a name="acceptpkcs7blob"></a>acceptPKCS7Blob

Die [**acceptPKCS7Blob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptpkcs7blob) -Funktion in Xenroll.dll installiert eine PKCS 7-Antwort, die \# in einem Bytearray enthalten ist.

Sie können " [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) " zum Installieren einer PKCS \# 7-Nachricht anrufen. Wenn Sie für den ersten Parameter von " [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)" den Wert " **allownooutstandingrequest** " der [**installresponserestrictionflags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) -Enumeration angeben, ist ein dummyzertifikat nicht vorhanden. Dadurch können Sie die PKCS 7-Antwort installieren, \# ohne zuerst " [**ENROLL**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) " oder " [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest)" aufrufen zu müssen. Wenn Sie ein Zertifikat jedoch mithilfe eines Webskripts installieren, muss im Anforderungs Speicher ein dummyzertifikat vorhanden sein. Daher müssen Sie für den ersten Parameter " **allownone** " angeben.

## <a name="acceptresponseblob"></a>akzeptresponseeblob

Die Funktion " [**Accept trespontarblob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-acceptresponseblob) " in Xenroll.dll installiert eine PKCS \# 7-oder CMC-Zertifikats Antwort, die in einem Bytearray enthalten ist.

Sie können " [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) " anrufen, um eine PKCS 7-oder eine CMC-Antwort zu installieren \# . Wenn Sie für den ersten Parameter von [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)den Wert **allownooutstandingrequest** der [**installresponserestrictionflags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) -Enumeration angeben, ist ein dummyzertifikat nicht vorhanden. Dadurch können Sie die Antwort installieren, ohne zuerst " [**ENROLL**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) " oder " [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest)" aufrufen zu müssen. Wenn Sie ein Zertifikat jedoch mithilfe eines Webskripts installieren, muss im Anforderungs Speicher ein dummyzertifikat vorhanden sein. Daher müssen Sie für den ersten Parameter " **allownone** " angeben.

## <a name="getcertcontextfromfileresponsewstr"></a>getcertcontextfromfileresponabwstr

Die [**getcertcontextfromfileresponcwstr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getcertcontextfromfileresponsewstr) -Funktion in Xenroll.dll ruft das Client Zertifikat aus einer Datei ab.

Die CertEnroll.dll Bibliothek implementiert die Funktionalität zum Abrufen eines Zertifikats aus einer in einer Datei gespeicherten Zertifizierungsstellen Antwort nicht direkt. Sie können jedoch eine benutzerdefinierte Funktion erstellen, um die Datei Daten in ein Bytearray zu lesen, und [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) aufrufen, um die PKCS \# 7-oder die CMC-Antwort zu installieren, und die [**Zertifikat**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificate) Eigenschaft aufrufen, um das Zertifikat abzurufen.

Wenn Sie für den ersten Parameter von [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)den Wert **allownooutstandingrequest** der [**installresponserestrictionflags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) -Enumeration angeben, ist ein dummyzertifikat nicht vorhanden. Dadurch können Sie ein Zertifikat installieren, ohne zuerst " [**ENROLL**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) " oder " [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest)" aufrufen zu müssen. Wenn Sie ein Zertifikat jedoch mithilfe eines Webskripts installieren, muss im Anforderungs Speicher ein dummyzertifikat vorhanden sein. Daher müssen Sie für den ersten Parameter " **allownone** " angeben.

## <a name="getcertcontextfrompkcs7"></a>getCertContextFromPKCS7

Die [**getCertContextFromPKCS7**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-getcertcontextfrompkcs7) -Funktion in Xenroll.dll ruft das Client Zertifikat aus einer PKCS \# 7-Antwort ab.

Sie können die [**Certificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificate) -Eigenschaft für das [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt aufrufen, um ein Zertifikat abzurufen, nachdem Sie die Methode [**ENROLL**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) oder [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) aufgerufen haben.

## <a name="getcertcontextfromresponseblob"></a>getcertcontextfromresponse-BLOB

Die [**getcertcontextfromresponcblob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getcertcontextfromresponseblob) -Funktion in Xenroll.dll ruft ein Client Zertifikat von einer PKCS \# 7-oder CMC-Antwort ab.

Sie können die [**Certificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificate) -Eigenschaft für das [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt aufrufen, um ein Zertifikat abzurufen, nachdem Sie die Methode [**ENROLL**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) oder [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) aufgerufen haben.

## <a name="installpkcs7blob"></a>InstallPKCS7Blob

Mit der [**InstallPKCS7Blob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-installpkcs7blob) -Funktion in Xenroll.dll wird eine PKCS \# 7-Antwort installiert.

Sie können " [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) " anrufen, um eine PKCS 7-oder eine CMC-Antwort zu installieren \# . Wenn Sie für den ersten Parameter von [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)den Wert **allownooutstandingrequest** der [**installresponserestrictionflags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) -Enumeration angeben, ist ein dummyzertifikat nicht vorhanden. Dadurch können Sie die Antwort installieren, ohne zuerst " [**ENROLL**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) " oder " [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest)" aufrufen zu müssen. Wenn Sie ein Zertifikat jedoch mithilfe eines Webskripts installieren, muss im Anforderungs Speicher ein dummyzertifikat vorhanden sein. Daher müssen Sie für den ersten Parameter " **allownone** " angeben.

## <a name="installpkcs7blobex"></a>InstallPKCS7BlobEx

Mit der [**InstallPKCS7BlobEx**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-installpkcs7blobex) -Funktion in Xenroll.dll wird eine PKCS \# 7-Antwort installiert, und die Anzahl der installierten Zertifikate wird zurückgegeben.

Sie können " [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) " anrufen, um eine PKCS 7-oder eine CMC-Antwort zu installieren \# . Wenn Sie für den ersten Parameter von [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)den Wert **allownooutstandingrequest** der [**installresponserestrictionflags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) -Enumeration angeben, ist ein dummyzertifikat nicht vorhanden. Dadurch können Sie die Antwort installieren, ohne zuerst " [**ENROLL**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) " oder " [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest)" aufrufen zu müssen. Wenn Sie ein Zertifikat jedoch mithilfe eines Webskripts installieren, muss im Anforderungs Speicher ein dummyzertifikat vorhanden sein. Daher müssen Sie für den ersten Parameter " **allownone** " angeben.

## <a name="spcfilenamewstr"></a>Spcdateinamewstr

Die [**spcfileamewstr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_spcfilenamewstr) -Funktion in Xenroll.dll gibt den Namen der Datei an, in der die Zertifikats Antwort gespeichert werden soll, oder ruft ihn ab. Die CertEnroll.dll Bibliothek implementiert keine Funktionen, mit denen Sie ein Zertifikat in eine bestimmte Datei kopieren können. Bei der Registrierung wird die Zertifikatskette automatisch in Dateien in den entsprechenden speichern installiert.

## <a name="writecerttocsp"></a>"Schreibcertto"

Die Funktion " [**Write-certtocsp**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_writecerttocsp) " in Xenroll.dll gibt einen booleschen Wert an oder ruft ihn ab, der angibt, ob ein Zertifikat in einen [*Kryptografiedienstanbieter (kryptografischen Service Provider*](/windows/desktop/SecGloss/c-gly) , CSP) geschrieben wird. Wenn diese Funktion aufgerufen wird, ist der Anbieter in der Regel eine [*Smartcard*](/windows/desktop/SecGloss/s-gly).

Wenn ein Client in CertEnroll.dll die [**Registrierungsmethode aufruft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) , um eine Anforderung für ein Smartcardzertifikat zu senden, und ein Zertifikat ausgestellt wird, wird das Zertifikat bei der [**Anmeldung**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) automatisch auf der Smartcard installiert, vorausgesetzt, dass die Karte im Reader installiert ist. Die [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) -Methode schreibt das Zertifikat auch automatisch auf die Smartcard.

## <a name="writecerttouserds"></a>"Schreibcerttouserds"

Die Funktion " [**schreitecerttouserds**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_writecerttouserds) " in Xenroll.dll gibt einen booleschen Wert an, der angibt, ob ein Zertifikat im Active Directory Speicher gespeichert werden soll, oder ruft ihn ab. Die CertEnroll.dll Bibliothek implementiert keine Funktionen, mit denen Sie einen Speicher angeben können, in den ein Zertifikat kopiert werden soll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnung von Xenroll.dll zu CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

 
