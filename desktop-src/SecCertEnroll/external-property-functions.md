---
description: Eigenschaften werden verwendet, um einem Zertifikat einen Wert zu zuordnen.
ms.assetid: a6433416-fe77-4bb0-bd8e-9410a49ab861
title: Externe Eigenschaftenfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40196f4f42823ad44debeccc0fa85dc4615d58d1a0ccf521b2dd796e72574db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117779630"
---
# <a name="external-property-functions"></a>Externe Eigenschaftenfunktionen

Eigenschaften werden verwendet, um einem Zertifikat einen Wert zu zuordnen. Eigenschaften werden nie an eine Zertifizierungsstelle [*gesendet*](/windows/desktop/SecGloss/c-gly) oder von ihr verarbeitet, und sie werden nicht in einem Zertifikat gespeichert. In der Regel werden sie einem Zertifikat zugeordnet, nachdem das Zertifikat von der Zertifizierungsstelle empfangen und bevor es in einem Speicher gespeichert wird. Die Eigenschaften werden zusammen mit dem Zertifikat im Speicher gespeichert. CertEnroll.dll implementiert die [**ICertProperty-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) und die folgenden Schnittstellen, die von **ICertProperty abgeleitet wurden:**

-   [**ICertPropertyArchived**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchived)
-   [**ICertPropertyArchivedKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchivedkeyhash)
-   [**ICertPropertyAutoEnroll**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyautoenroll)
-   [**ICertPropertyBackedUp**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertybackedup)
-   [**ICertPropertyDescription**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertydescription)
-   [**ICertPropertyEnrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyenrollment)
-   [**ICertPropertyFriendlyName**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyfriendlyname)
-   [**ICertPropertyKeyProvInfo**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertykeyprovinfo)
-   [**ICertPropertyRenewal**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrenewal)
-   [**ICertPropertyRequestOriginator**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrequestoriginator)
-   [**ICertPropertySHA1Hash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertysha1hash)

In jedem der folgenden Abschnitte wird eine Funktion identifiziert, die von Xenroll.dll zum Verwalten externer Zertifikateigenschaften exportiert wird. In jedem Abschnitt wird auch erläutert, wie sie CertEnroll.dll funktion ersetzen, oder gibt an, dass keine Zuordnung zwischen den beiden Bibliotheken vorhanden ist:

-   [addBlobPropertyToCertificateWStr](#addblobpropertytocertificatewstr)
-   [GetPrivateKeyArchiveCertificate](#getprivatekeyarchivecertificate)
-   [resetBlobProperties](#resetblobproperties)
-   [SetPrivateKeyArchiveCertificate](#setprivatekeyarchivecertificate)
-   [SetSignerCertificate](#setsignercertificate)
-   [ThumbPrintWStr](#thumbprintwstr)
-   [Zugehörige Themen](#related-topics)

## <a name="addblobpropertytocertificatewstr"></a>addBlobPropertyToCertificateWStr

Die [**addBlobPropertyToCertificateWStr-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addblobpropertytocertificatewstr) in Xenroll.dll dem Zertifikat eine -Eigenschaft hinzu.

In CertEnroll.dll implementieren alle von [**ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) abgeleiteten Objekte eine [**SetValueOnCertificate-Methode,**](/windows/desktop/api/CertEnroll/nf-certenroll-icertproperty-setvalueoncertificate) mit der Sie eine Eigenschaft einem Zertifikat zuordnen können. Außerdem implementiert das [**IX509Enrollment-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) direkt die [**CertificateFriendlyName-**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificatefriendlyname) und [**CertificateDescription-Eigenschaften.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificatedescription)

## <a name="getprivatekeyarchivecertificate"></a>GetPrivateKeyArchiveCertificate

Die [**GetPrivateKeyArchiveCertificate-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getprivatekeyarchivecertificate) in Xenroll.dll das Exchange-Zertifikat ab, das zum Archivieren eines privaten [*Schlüssels verwendet wird.*](/windows/desktop/SecGloss/p-gly)

Sie können das [**IX509CertificateRequestCmc-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) in CertEnroll.dll, um eine Anforderung für eine Zertifizierungsstelle zum Archivieren Ihres privaten Schlüssels zu erstellen. Sie müssen ein Austauschzertifikat von der [](/windows/desktop/SecGloss/p-gly) Zertifizierungsstelle abrufen und den in diesem Zertifikat enthaltenen öffentlichen Schlüssel verwenden, um den privaten Schlüssel zu verschlüsseln, den Sie zur Archivierung übermitteln. Rufen Sie zum Angeben oder Abrufen eines Zertifizierungsstellenaustauschzertifikats die [**KeyArchivalCertificate-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_keyarchivalcertificate) für dieses Objekt auf.

## <a name="resetblobproperties"></a>resetBlobProperties

Die [**resetBlobProperties-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-icenroll4-resetblobproperties) in Xenroll.dll entfernt die Eigenschaftensammlung aus dem Zertifikat.

In CertEnroll.dll implementieren alle von [**ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) abgeleiteten Eigenschaftenobjekte die [**RemoveFromCertificate-Eigenschaft,**](/windows/desktop/api/CertEnroll/nf-certenroll-icertproperty-removefromcertificate) mit der Sie die Zuordnung einer Eigenschaft zu einem Zertifikat entfernen können.

## <a name="setprivatekeyarchivecertificate"></a>SetPrivateKeyArchiveCertificate

Die [**Funktion SetPrivateKeyArchiveCertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-setprivatekeyarchivecertificate) in Xenroll.dll ein Austauschzertifikat an, das zum Archivieren eines privaten Schlüssels verwendet wird.

Sie können das [**IX509CertificateRequestCmc-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) in CertEnroll.dll, um eine Anforderung für eine Zertifizierungsstelle zum Archivieren Ihres privaten Schlüssels zu erstellen. Sie müssen ein Austauschzertifikat von der Zertifizierungsstelle abrufen und den in diesem Zertifikat enthaltenen öffentlichen Schlüssel verwenden, um den privaten Schlüssel zu verschlüsseln, den Sie zur Archivierung übermitteln. Rufen Sie zum Angeben oder Abrufen eines Zertifizierungsstellenaustauschzertifikats die [**KeyArchivalCertificate-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_keyarchivalcertificate) für dieses Objekt auf.

## <a name="setsignercertificate"></a>SetSignerCertificate

Die [**SetSignerCertificate-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-setsignercertificate) in Xenroll.dll Gibt ein Signiererzertifikat an.

Das [**ISignerCertificate-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) in CertEnroll.dll kann verwendet werden, um eine [*PKCS \# 7-,*](/windows/desktop/SecGloss/p-gly)CMC- oder selbstsignierte [*Zertifikatanforderung zu signieren.*](/windows/desktop/SecGloss/c-gly) Sie können das -Objekt mithilfe eines vorhandenen Signaturzertifikats initialisieren und es einer Anforderung zuordnen, indem Sie eine der folgenden Eigenschaften aufrufen:

-   [**SignerCertificates**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_signercertificates) auf [ **IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
-   [**SignerCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_signercertificate) auf [ **IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
-   [**SignerCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcertificate-get_signercertificate) auf [ **IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)

Wenn Sie eine CMC-Anforderung aus einer inneren Anforderung und einer Vorlage initialisieren oder eine PKCS 7-Anforderung aus einer vorhandenen Anforderung initialisieren, kann das Signaturzertifikat \# festgelegt werden.

## <a name="thumbprintwstr"></a>ThumbPrintWStr

Die [**ThumbPrintWStr-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_thumbprintwstr) in Xenroll.dll gibt den Wert des Zertifikathashs an oder ruft den Wert ab.

In CertEnroll.dll können Sie das [**ICertPropertySHA1Hash-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertysha1hash) verwenden, um einen Hashwert [*(*](/windows/desktop/SecGloss/t-gly)Fingerabdruck ) abzurufen, der durch Aufrufen der [**InitializeFromCertificate-Methode erstellt**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) wurde. [](/windows/desktop/SecGloss/h-gly)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnen Xenroll.dll zu CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> </dl>

 

 
