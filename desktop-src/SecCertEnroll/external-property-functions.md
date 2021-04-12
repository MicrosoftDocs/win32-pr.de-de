---
description: Eigenschaften werden verwendet, um einem Zertifikat einen Wert zuzuordnen.
ms.assetid: a6433416-fe77-4bb0-bd8e-9410a49ab861
title: Externe Eigenschaften Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26c8148022bf604aa90780787c068b330c469ae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217638"
---
# <a name="external-property-functions"></a>Externe Eigenschaften Funktionen

Eigenschaften werden verwendet, um einem Zertifikat einen Wert zuzuordnen. Eigenschaften werden niemals an eine Zertifizierungsstelle ( [*Certification Authority*](/windows/desktop/SecGloss/c-gly) , ca) gesendet oder von dieser verarbeitet. Sie werden nicht in einem Zertifikat gespeichert. Normalerweise werden Sie einem Zertifikat zugeordnet, nachdem das Zertifikat von der Zertifizierungsstelle empfangen wurde und bevor es in einem Speicher gespeichert wird. Die Eigenschaften werden zusammen mit dem Zertifikat im Speicher gespeichert. CertEnroll.dll implementiert die [**icertproperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) -Schnittstelle und die folgenden Schnittstellen, die von **icertproperty** abgeleitet sind:

-   [**Icertpropertyarchiviert**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchived)
-   [**Icertpropertyarchivedkeyhash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchivedkeyhash)
-   [**Icertpropertyautoenroll**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyautoenroll)
-   [**Icertpropertybackedup**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertybackedup)
-   [**Icertpropertydescription**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertydescription)
-   [**Icertpropertyeinschreibung**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyenrollment)
-   [**Icertpropertyfriendlyname**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyfriendlyname)
-   [**Icertpropertykeyprovinfo**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertykeyprovinfo)
-   [**Icertpropertyrenewal**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrenewal)
-   [**Icertpropertyrequestoriginator**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrequestoriginator)
-   [**ICertPropertySHA1Hash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertysha1hash)

In den folgenden Abschnitten wird eine Funktion identifiziert, die von Xenroll.dll zum Verwalten externer Zertifikat Eigenschaften exportiert wird. Außerdem wird in jedem Abschnitt erläutert, wie CertEnroll.dll verwendet wird, um die Funktion zu ersetzen, oder es wird angegeben, dass keine Zuordnung zwischen den beiden Bibliotheken besteht:

-   [addblobpropertytcertificatewstr](#addblobpropertytocertificatewstr)
-   [Getprivatekeyarchivecertificate](#getprivatekeyarchivecertificate)
-   [resetblobproperties](#resetblobproperties)
-   [Setprivatekeyarchivecertificate](#setprivatekeyarchivecertificate)
-   [Setsignercertificate](#setsignercertificate)
-   [Thumbprintwstr](#thumbprintwstr)
-   [Zugehörige Themen](#related-topics)

## <a name="addblobpropertytocertificatewstr"></a>addblobpropertytcertificatewstr

Die [**addblobpropertytocertificatewstr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addblobpropertytocertificatewstr) -Funktion in Xenroll.dll fügt dem Zertifikat eine Eigenschaft hinzu.

In CertEnroll.dll implementieren alle von [**icertproperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) abgeleiteten Objekte eine [**setvalueoncertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-icertproperty-setvalueoncertificate) -Methode, die Sie verwenden können, um eine Eigenschaft einem Zertifikat zuzuordnen. Außerdem implementiert das [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt die Eigenschaften [**certificatefriendlyname**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificatefriendlyname) und [**certificatedescription**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificatedescription) direkt.

## <a name="getprivatekeyarchivecertificate"></a>Getprivatekeyarchivecertificate

Die Funktion " [**getprivatekeyarchivecertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getprivatekeyarchivecertificate) " in Xenroll.dll ruft das Exchange-Zertifikat ab, das zum Archivieren eines [*privaten Schlüssels*](/windows/desktop/SecGloss/p-gly)verwendet wird.

Sie können das [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) -Objekt in CertEnroll.dll verwenden, um eine Anforderung für eine Zertifizierungsstelle zum Archivieren Ihres privaten Schlüssels zu erstellen. Sie müssen ein Exchange-Zertifikat von der Zertifizierungsstelle abrufen und den [*öffentlichen*](/windows/desktop/SecGloss/p-gly) Schlüssel, der in diesem Zertifikat enthalten ist, verwenden, um den privaten Schlüssel zu verschlüsseln, den Sie für die Archivierung übermitteln. Rufen Sie zum angeben oder Abrufen eines Zertifizierungsstellen-Exchange-Zertifikats die [**keyarchivalcertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_keyarchivalcertificate) -Eigenschaft für dieses Objekt auf.

## <a name="resetblobproperties"></a>resetblobproperties

Die [**resetblobproperties**](/windows/desktop/api/xenroll/nf-xenroll-icenroll4-resetblobproperties) -Funktion in Xenroll.dll entfernt die Eigenschaften Auflistung aus dem Zertifikat.

In CertEnroll.dll implementieren alle Eigenschaften Objekte, die von [**icertproperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) abgeleitet werden, die [**removefromcertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-icertproperty-removefromcertificate) -Eigenschaft, die Sie verwenden können, um die Zuordnung einer Eigenschaft zu einem Zertifikat aufzuheben.

## <a name="setprivatekeyarchivecertificate"></a>Setprivatekeyarchivecertificate

Die [**setprivatekeyarchivecertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-setprivatekeyarchivecertificate) -Funktion in Xenroll.dll gibt ein Exchange-Zertifikat an, das zum Archivieren eines privaten Schlüssels verwendet wird.

Sie können das [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) -Objekt in CertEnroll.dll verwenden, um eine Anforderung für eine Zertifizierungsstelle zum Archivieren Ihres privaten Schlüssels zu erstellen. Sie müssen ein Exchange-Zertifikat von der Zertifizierungsstelle abrufen und den öffentlichen Schlüssel, der in diesem Zertifikat enthalten ist, verwenden, um den privaten Schlüssel zu verschlüsseln, den Sie für die Archivierung übermitteln. Rufen Sie zum angeben oder Abrufen eines Zertifizierungsstellen-Exchange-Zertifikats die [**keyarchivalcertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_keyarchivalcertificate) -Eigenschaft für dieses Objekt auf.

## <a name="setsignercertificate"></a>Setsignercertificate

Die Funktion " [**setsignercertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-setsignercertificate) " in Xenroll.dll gibt ein Signatur Geber Zertifikat an.

Das [**isignercertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) -Objekt in CertEnroll.dll kann verwendet werden, um eine [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly)-, CMC-oder selbst signierte [*Zertifikat Anforderung*](/windows/desktop/SecGloss/c-gly)zu signieren. Sie können das Objekt mit einem vorhandenen Signaturzertifikat initialisieren und es einer Anforderung zuordnen, indem Sie eine der folgenden Eigenschaften aufrufen:

-   [**Signerzertifikate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_signercertificates) auf [ **IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
-   [**SignerCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_signercertificate) auf [ **IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
-   [**SignerCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcertificate-get_signercertificate) auf [ **IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)

Außerdem kann das Signaturzertifikat festgelegt werden, wenn Sie eine CMC-Anforderung aus einer inneren Anforderung und einer Vorlage initialisieren oder eine PKCS \# 7-Anforderung aus einer vorhandenen Anforderung initialisieren.

## <a name="thumbprintwstr"></a>Thumbprintwstr

Die Funktion [**thumbprintwstr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_thumbprintwstr) in Xenroll.dll gibt den Wert des Zertifikat Hash an oder ruft ihn ab.

In CertEnroll.dll können Sie das [**ICertPropertySHA1Hash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertysha1hash) -Objekt verwenden, um einen [*Hashwert*](/windows/desktop/SecGloss/h-gly) ([*Fingerabdruck*](/windows/desktop/SecGloss/t-gly)) abzurufen, der durch Aufrufen der [**initializefromcertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) -Methode erstellt wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnung von Xenroll.dll zu CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> </dl>

 

 
