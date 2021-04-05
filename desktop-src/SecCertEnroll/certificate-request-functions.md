---
description: Die CertEnroll.dll-Bibliothek implementiert fünf Schnittstellen, die verwendet werden können, um eine Zertifikat Anforderung zu erstellen und zu verwalten.
ms.assetid: f4630095-6ba2-46f7-8825-e7a5b1cb185a
title: Zertifikat Anforderungs Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04191f49949f662a9b9d780726f7ac7a40b370ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041829"
---
# <a name="certificate-request-functions"></a>Zertifikat Anforderungs Funktionen

Die CertEnroll.dll-Bibliothek implementiert fünf Schnittstellen, die verwendet werden können, um eine Zertifikat Anforderung zu erstellen und zu verwalten. Die [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) -Schnittstelle stellt ein abstraktes Basisobjekt dar, das Methoden Signaturen definiert, die von den folgenden vier Schnittstellen geerbt werden.

| Schnittstelle                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) | Ermöglicht es Ihnen, ein Zertifikat direkt zu erstellen, ohne eine Zertifizierungsstelle ( [*Certification Authority*](/windows/desktop/SecGloss/c-gly) , ca) anwenden zu müssen.<br/>                                                                                                            |
| [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                 | Stellt eine Zertifikat [*Verwaltung über CMS*](/windows/desktop/SecGloss/c-gly) (SMTP)-Zertifikat Anforderung (Certificate Management Message over CMS) dar, die eine geduckte PKCS \# 10-Anforderung oder ein anderes Objekt vom Typ "CMC Request" enthalten kann.<br/> |
| [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)             | Stellt ein Anforderungs Objekt der [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) -Zertifikat Nachrichten Syntax (CMS) dar, das eine geduckte PKCS 10-Anforderung enthalten muss \# .<br/>                                                                                                         |
| [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)           | Stellt eine PKCS \# 10-Zertifikat Anforderung dar. Eine PKCS \# 10-Anforderung kann direkt an eine Zertifizierungsstelle gesendet werden, oder Sie kann von einer PKCS 7-oder einer CMC-Anforderung umschließt werden \# .<br/>                                                                                                                                                            |



 

Sie können ein Zertifikat Anforderungs Objekt verwenden, um ein [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt zu initialisieren, um einen Client in einer Zertifikat Hierarchie zu registrieren und die von der Zertifizierungsstelle zurückgegebene Zertifikats Antwort zu installieren.

Jeder der folgenden Abschnitte gibt eine Funktion an, die von Xenroll.dll zum Erstellen, aufzählen oder Löschen von Zertifikat Anforderungen exportiert wurde. Außerdem wird in jedem Abschnitt erläutert, wie CertEnroll.dll verwendet wird, um die Funktion zu ersetzen, oder es wird angegeben, dass keine Zuordnung zwischen den beiden Bibliotheken besteht:

-   [createFilePKCS10WStr](#createfilepkcs10wstr)
-   ["kreatefilerequestwstr"](#createfilerequestwstr)
-   [createPKCS10WStr](#createpkcs10wstr)
-   [CreatePKCS7RequestFromRequest](#createpkcs7requestfromrequest)
-   ["kreaterequestwstr"](#createrequestwstr)
-   [Deleterequestcert](#deleterequestcert)
-   [enumpdingrequestwstr](#enumpendingrequestwstr)
-   [removepkodingrequestwstr](#removependingrequestwstr)
-   [Zurücksetzen](#reset)
-   [setpdingrequestinfowstr](#setpendingrequestinfowstr)
-   [Zugehörige Themen](#related-topics)

## <a name="createfilepkcs10wstr"></a>createFilePKCS10WStr

Die [**createFilePKCS10WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createfilepkcs10wstr) -Funktion in Xenroll.dll erstellt eine Base64-codierte PKCS \# 10-Zertifikat Anforderung und speichert Sie in einer Datei.

Die CertEnroll.dll Bibliothek implementiert die Funktionalität nicht direkt, um eine Anforderung in eine Datei zu schreiben. Sie können jedoch eine Zertifikat Anforderung abrufen, indem Sie die [**rawData**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_rawdata) -Eigenschaft des [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) -Objekts aufrufen und eine benutzerdefinierte Funktion erstellen, um den Wert in eine Datei zu kopieren.

## <a name="createfilerequestwstr"></a>"kreatefilerequestwstr"

Die Funktion " [**foratefilerequestwstr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilerequestwstr) " in Xenroll.dll erstellt eine PKCS \# 7-, PKCS \# 10-oder CMC-Zertifikat Anforderung und speichert Sie in einer Datei.

Die CertEnroll.dll Bibliothek implementiert die Funktionalität nicht direkt, um eine Anforderung in eine Datei zu schreiben. Sie können jedoch eine Zertifikat Anforderung abrufen, indem Sie die [**rawData**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_rawdata) -Eigenschaft des [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) -Objekts aufrufen und eine benutzerdefinierte Funktion erstellen, um den Wert in eine Datei zu kopieren.

## <a name="createpkcs10wstr"></a>createPKCS10WStr

Die [**createPKCS10WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs10wstr) -Funktion in Xenroll.dll erstellt eine PKCS \# 10-Zertifikat Anforderung und kopiert sie in ein Bytearray.

Sie können ein [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -Objekt verwenden, um eine PKCS \# 10-Anforderung über eine vorhandene Anforderung, ein vorhandenes Zertifikat, einen [*privaten Schlüssel*](/windows/desktop/SecGloss/p-gly), einen [*öffentlichen Schlüssel*](/windows/desktop/SecGloss/p-gly)oder eine Vorlage zu initialisieren.

## <a name="createpkcs7requestfromrequest"></a>CreatePKCS7RequestFromRequest

Die [**CreatePKCS7RequestFromRequest**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs7requestfromrequest) -Funktion in Xenroll.dll erstellt eine PKCS \# 7-Zertifikat Anforderung und kopiert sie in ein Bytearray.

Sie können ein [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) -Objekt verwenden, um eine PKCS \# 7-Anforderung aus einer vorhandenen Anforderung, einem vorhandenen Zertifikat, einem inneren Anforderungs Objekt oder einer Vorlage zu initialisieren.

## <a name="createrequestwstr"></a>"kreaterequestwstr"

Die Funktion " [**foraterequestwstr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createrequestwstr) " in Xenroll.dll erstellt eine PKCS \# 7-, PKCS \# 10-oder CMC-Zertifikat Anforderung und kopiert sie in ein Bytearray.

Wenn Sie die CertEnroll.dll-Bibliothek zum Erstellen von PKCS \# 7-, PKCS \# 10-oder CMC-Anforderungen verwenden möchten, können Sie Instanzen der [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)-, [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)-oder [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) -Objekte erstellen und initialisieren.

## <a name="deleterequestcert"></a>Deleterequestcert

Mit der [**deleterequestcert**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_deleterequestcert) -Funktion in Xenroll.dll wird ein boolescher Wert angegeben oder abgerufen, der angibt, ob ein dummyzertifikat nach der Installation einer Zertifikat Antwort entfernt wird.

Das [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt in CertEnroll.dll erstellt automatisch Dummy-Zertifikate im Anforderungs Speicher, um verschiedene Zertifikat Eigenschaften zu speichern, die während des Registrierungsvorgangs initialisiert werden. Nachdem ein Zertifikat von einer Zertifizierungsstelle ausgestellt wurde, werden die Eigenschaften in das neue Zertifikat kopiert, und das Dummy-Zertifikat wird gelöscht. In der CertEnroll.dll-Bibliothek ist es nicht zulässig, dass ein dummyzertifikat nach der Installation der Zertifikat Antwort beibehalten wird.

## <a name="enumpendingrequestwstr"></a>enumpdingrequestwstr

Die [**enumpdingrequestwstr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-enumpendingrequestwstr) -Funktion in Xenroll.dll ruft einen angegebenen Eigenschafts Wert für eine ausstehende Anforderung ab.

Die CertEnroll.dll Bibliothek implementiert keine direkte Funktionalität zum Entfernen einer ausstehenden Zertifikat Anforderung.

## <a name="removependingrequestwstr"></a>removepkodingrequestwstr

Die [**removependingrequestwstr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-removependingrequestwstr) -Funktion in Xenroll.dll entfernt eine ausstehende Anforderung aus dem Anforderungs Speicher.

Die CertEnroll.dll Bibliothek implementiert keine direkte Funktionalität zum Entfernen einer ausstehenden Zertifikat Anforderung.

## <a name="reset"></a>Reset

Die [**Reset**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-reset) -Funktion in Xenroll.dll gibt das Zertifikat Registrierungs Steuerelement in einen Ausgangszustand zurück.

Sie können das gleiche Ergebnis erzielen, indem Sie Certenroll.dll verwenden, um ein neues Anforderungs Objekt des erforderlichen Typs zu erstellen.

## <a name="setpendingrequestinfowstr"></a>setpdingrequestinfowstr

Die [**setpdingrequestinfowstr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-setpendingrequestinfowstr) -Funktion in Xenroll.dll gibt Eigenschaften für die ausstehende Anforderung an.

Die CertEnroll.dll Bibliothek implementiert keine direkte Funktionalität zum Entfernen einer ausstehenden Zertifikat Anforderung. Sie können die [**caconfigstring**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_caconfigstring) -Eigenschaft des [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekts aufrufen, um eine Konfigurations Zeichenfolge abzurufen, aber nur für ein aktives Registrierungs Objekt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnung von Xenroll.dll zu CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**Isignercertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)
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

 

