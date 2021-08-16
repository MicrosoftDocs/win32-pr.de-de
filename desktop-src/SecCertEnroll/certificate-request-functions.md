---
description: Die CertEnroll.dll-Bibliothek implementiert fünf Schnittstellen, die zum Erstellen und Verwalten einer Zertifikatanforderung verwendet werden können.
ms.assetid: f4630095-6ba2-46f7-8825-e7a5b1cb185a
title: Zertifikatanforderungsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e07fb348b335562863f04226a2fb729bfbcbdaba27cb574a04c87075a64653a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902569"
---
# <a name="certificate-request-functions"></a>Zertifikatanforderungsfunktionen

Die CertEnroll.dll-Bibliothek implementiert fünf Schnittstellen, die zum Erstellen und Verwalten einer Zertifikatanforderung verwendet werden können. Von diesen stellt die [**IX509CertificateRequest-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) ein abstraktes Basisobjekt dar, das Methodensignaturen definiert, die von den folgenden vier Schnittstellen geerbt werden.

| Schnittstelle                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) | Ermöglicht es Ihnen, ein Zertifikat direkt zu erstellen, ohne es bei einer [*Zertifizierungsstelle*](/windows/desktop/SecGloss/c-gly) (Ca) anzuwenden.<br/>                                                                                                            |
| [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                 | Stellt eine Zertifikatanforderung der [*Zertifikatverwaltung über CMS*](/windows/desktop/SecGloss/c-gly) (Certificate Management Message over CMS) dar, die eine geschachtelte PKCS \# 10-Anforderung oder ein anderes CMC-Anforderungsobjekt enthalten kann.<br/> |
| [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)             | Stellt ein CMS-Anforderungsobjekt (Certificate Message Syntax) von [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) dar, das eine geschachtelte PKCS \# 10-Anforderung enthalten muss.<br/>                                                                                                         |
| [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)           | Stellt eine PKCS \# 10-Zertifikatanforderung dar. Eine PKCS \# 10-Anforderung kann direkt an eine Zertifizierungsstelle gesendet oder von einer PKCS \# 7- oder CMC-Anforderung umschlossen werden.<br/>                                                                                                                                                            |



 

Sie können ein Zertifikatanforderungsobjekt verwenden, um ein [**IX509Enrollment-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) zu initialisieren, um einen Client in einer Zertifikathierarchie zu registrieren und die von der Zertifizierungsstelle zurückgegebene Zertifikatantwort zu installieren.

Jeder der folgenden Abschnitte identifiziert eine Funktion, die von Xenroll.dll exportiert wird, um Zertifikatanforderungen zu erstellen, aufzuzählen oder zu löschen. In jedem Abschnitt wird auch erläutert, wie sie CertEnroll.dll verwenden, um die Funktion zu ersetzen, oder gibt an, dass keine Zuordnung zwischen den beiden Bibliotheken vorhanden ist:

-   [createFilePKCS10WStr](#createfilepkcs10wstr)
-   [createFileRequestWStr](#createfilerequestwstr)
-   [createPKCS10WStr](#createpkcs10wstr)
-   [CreatePKCS7RequestFromRequest](#createpkcs7requestfromrequest)
-   [createRequestWStr](#createrequestwstr)
-   [DeleteRequestCert](#deleterequestcert)
-   [enumPendingRequestWStr](#enumpendingrequestwstr)
-   [removePendingRequestWStr](#removependingrequestwstr)
-   [Zurücksetzen](#reset)
-   [setPendingRequestInfoWStr](#setpendingrequestinfowstr)
-   [Zugehörige Themen](#related-topics)

## <a name="createfilepkcs10wstr"></a>createFilePKCS10WStr

Die [**createFilePKCS10WStr-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createfilepkcs10wstr) in Xenroll.dll erstellt eine Base64-codierte PKCS \# 10-Zertifikatanforderung und speichert sie in einer Datei.

Die CertEnroll.dll Bibliothek implementiert nicht direkt Funktionen zum Schreiben einer Anforderung in eine Datei. Sie können jedoch eine Zertifikatanforderung abrufen, indem Sie die [**RawData-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_rawdata) für das [**IX509CertificateRequest-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) aufrufen und eine benutzerdefinierte Funktion erstellen, um den Wert in eine Datei zu kopieren.

## <a name="createfilerequestwstr"></a>createFileRequestWStr

Die [**createFileRequestWStr-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilerequestwstr) in Xenroll.dll erstellt eine PKCS \# 7-, PKCS \# 10- oder CMC-Zertifikatanforderung und speichert sie in einer Datei.

Die CertEnroll.dll Bibliothek implementiert nicht direkt Funktionen zum Schreiben einer Anforderung in eine Datei. Sie können jedoch eine Zertifikatanforderung abrufen, indem Sie die [**RawData-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_rawdata) für das [**IX509CertificateRequest-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) aufrufen und eine benutzerdefinierte Funktion erstellen, um den Wert in eine Datei zu kopieren.

## <a name="createpkcs10wstr"></a>createPKCS10WStr

Die [**createPKCS10WStr-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs10wstr) in Xenroll.dll erstellt eine PKCS \# 10-Zertifikatanforderung und kopiert sie in ein Bytearray.

Sie können ein [**IX509CertificateRequestPkcs10-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) verwenden, um eine PKCS \# 10-Anforderung aus einer vorhandenen Anforderung, einem vorhandenen Zertifikat, einem [*privaten Schlüssel,*](/windows/desktop/SecGloss/p-gly)einem [*öffentlichen Schlüssel*](/windows/desktop/SecGloss/p-gly)oder einer Vorlage zu initialisieren.

## <a name="createpkcs7requestfromrequest"></a>CreatePKCS7RequestFromRequest

Die [**CreatePKCS7RequestFromRequest-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs7requestfromrequest) in Xenroll.dll erstellt eine PKCS \# 7-Zertifikatanforderung und kopiert sie in ein Bytearray.

Sie können ein [**IX509CertificateRequestPkcs7-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) verwenden, um eine PKCS \# 7-Anforderung aus einer vorhandenen Anforderung, einem vorhandenen Zertifikat, einem inneren Anforderungsobjekt oder einer Vorlage zu initialisieren.

## <a name="createrequestwstr"></a>createRequestWStr

Die [**createRequestWStr-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createrequestwstr) in Xenroll.dll erstellt eine PKCS \# 7-, PKCS \# 10- oder CMC-Zertifikatanforderung und kopiert sie in ein Bytearray.

Um die CertEnroll.dll Bibliothek zum Erstellen von PKCS \# 7-, PKCS \# 10- oder CMC-Anforderungen zu verwenden, können Sie Instanzen der [**IX509CertificateRequestPkcs7-,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) [**IX509CertificateRequestPkcs10-**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)oder [**IX509CertificateRequestCmc-Objekte**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) erstellen und initialisieren.

## <a name="deleterequestcert"></a>DeleteRequestCert

Die [**DeleteRequestCert-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_deleterequestcert) in Xenroll.dll gibt einen booleschen Wert an oder ruft einen booleschen Wert ab, der angibt, ob ein Dummyzertifikat nach der Installation einer Zertifikatantwort entfernt wird.

Das [**IX509Enrollment-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) in CertEnroll.dll erstellt automatisch Dummyzertifikate im Anforderungsspeicher, um verschiedene Zertifikateigenschaften vorübergehend zu speichern, die während des Registrierungsvorgangs initialisiert werden. Nachdem ein Zertifikat von einer Zertifizierungsstelle ausgestellt wurde, werden die Eigenschaften in das neue Zertifikat kopiert, und das Dummyzertifikat wird gelöscht. Mit der CertEnroll.dll Bibliothek können Sie nicht erzwingen, dass ein Dummyzertifikat verbleibt, nachdem die Zertifikatantwort installiert wurde.

## <a name="enumpendingrequestwstr"></a>enumPendingRequestWStr

Die [**enumPendingRequestWStr-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-enumpendingrequestwstr) in Xenroll.dll ruft einen angegebenen Eigenschaftswert für eine ausstehende Anforderung ab.

Die CertEnroll.dll Bibliothek implementiert nicht direkt Funktionen zum Entfernen einer ausstehenden Zertifikatanforderung.

## <a name="removependingrequestwstr"></a>removePendingRequestWStr

Die [**removePendingRequestWStr-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-removependingrequestwstr) in Xenroll.dll entfernt eine ausstehende Anforderung aus dem Anforderungsspeicher.

Die CertEnroll.dll Bibliothek implementiert nicht direkt Funktionen zum Entfernen einer ausstehenden Zertifikatanforderung.

## <a name="reset"></a>Reset

Die [**Reset-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-reset) in Xenroll.dll gibt die Zertifikatregistrierungssteuerung in einen Anfangszustand zurück.

Sie können das gleiche Ergebnis erzielen, indem Sie Certenroll.dll verwenden, um ein neues Anforderungsobjekt des erforderlichen Typs zu erstellen.

## <a name="setpendingrequestinfowstr"></a>setPendingRequestInfoWStr

Die [**setPendingRequestInfoWStr-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-setpendingrequestinfowstr) in Xenroll.dll gibt Eigenschaften für die ausstehende Anforderung an.

Die CertEnroll.dll Bibliothek implementiert nicht direkt Funktionen zum Entfernen einer ausstehenden Zertifikatanforderung. Sie können die [**CAConfigString-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_caconfigstring) für das [**IX509Enrollment-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) aufrufen, um eine Konfigurationszeichenfolge abzurufen, jedoch nur für ein aktives Registrierungsobjekt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnen Xenroll.dll zu CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)
</dt> <dt>

[**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)
</dt> <dt>

[**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)
</dt> <dt>

[**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
</dt> <dt>

[**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
</dt> <dt>

[**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
</dt> <dt>

[**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

