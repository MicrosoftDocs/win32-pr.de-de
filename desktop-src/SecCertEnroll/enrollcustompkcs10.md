---
description: Erstellt eine benutzerdefinierte PKCS \# 10-Anforderung, übergibt sie an eine eigenständige Zertifizierungsstelle (Certification Authority, ca) und installiert das ausgegebene Zertifikat im Zertifikat Speicher.
ms.assetid: dcb69d7e-457e-457b-9eea-15676ed710aa
title: enrollCustomPKCS10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86ad95f483d4bc82136865e94a70ad46e90e1c24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359891"
---
# <a name="enrollcustompkcs10"></a>enrollCustomPKCS10

Das enrollCustomPKCS10-Beispiel erstellt eine benutzerdefinierte PKCS \# 10-Anforderung, sendet Sie an eine eigenständige Zertifizierungsstelle (Certification Authority, ca) und installiert das ausgegebene Zertifikat im Zertifikat Speicher. Eine eigenständige Zertifizierungsstelle erfordert keine Active Directory und verwendet keine Vorlagen.

## <a name="location"></a>Standort

Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner *% Program Files%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Einschreibung \\ VC \\ enrollCustomPKCS10 installiert.

## <a name="discussion"></a>Diskussion

Das enrollCustomPKCS10-Beispiel:

1.  Verarbeitet die Befehlszeilenargumente. Die Befehlszeile muss den Antragsteller Namen des X. 500-Zertifikats, den e-Mail-Namen (RFC822) und eine EKU-Objekt Kennung (Enhanced Key Usage, EKU) enthalten. Sie können z. b. die folgenden Argumente angeben, die registriert werden sollen *user1@example.com* :
    -   Antragsteller Name: "*CN = user1, DC = example, DC = com*"
    -   RFC822 Name: *user1@example.com*
    -   Clientauthentifizierungs-EKU-OID: 1.3.6.1.5.5.7.3.2
2.  Erstellt ein [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -Objekt und initialisiert es für den Endbenutzer, indem der **contextUser** -Wert der [**X509CertificateEnrollmentContext**](/windows/desktop/api/CertEnroll/ne-certenroll-x509certificateenrollmentcontext) -Enumeration angegeben wird.
3.  Erstellt ein [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) -Objekt, verwendet das-Objekt, um den Betreffnamen in ein Bytearray zu codieren, und fügt das Array dem PKCS \# 10-Anforderungs Objekt hinzu.
4.  Erstellt ein [**iobjectid**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) -Objekt, initialisiert es mithilfe der in der Befehlszeile angegebenen EKU-Objekt Kennung (OID), erstellt eine [**iobjectids**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectids) -Auflistung, fügt das neue **iobjectid** -Objekt (EKU) der Auflistung hinzu, verwendet die-Auflistung, um ein [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) -Objekt zu initialisieren, und fügt dieses-Objekt der Anforderung hinzu.
5.  Erstellt ein [**ialternativename**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) -Objekt, initialisiert es mit dem in der Befehlszeile angegebenen RFC822-Namen, erstellt eine [**ialternativenames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) -Auflistung, fügt das neue **ialternativename** (RFC822 Name)-Objekt der-Auflistung hinzu, erstellt ein [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) -Objekt und fügt dieses-Objekt der Anforderung hinzu.
6.  Erstellt ein [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt, initialisiert es mit dem [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -Objekt und ruft eine Zeichenfolge ab, die eine Base64-codierte Anforderung enthält.
7.  Erstellt ein [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) -Objekt und verwendet es, um eine Zeichenfolge abzurufen, die die Zertifizierungsstellen Konfiguration enthält.
8.  Erstellt ein CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) -Objekt und verwendet es sowie die Zeichen folgen, die die Zertifizierungsstellen Konfiguration enthalten, und die Zertifikat Anforderung zum übermitteln der Anforderung an die Zertifizierungsstelle.
9.  Überprüft den Übermittlungs Status und installiert das Zertifikat im Zertifikat Speicher, wenn die Registrierung erfolgreich ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[PKCS \# 10-Anforderung](pkcs--10-request.md)
</dt> <dt>

[Verwenden der enthaltenen Beispiele](using-the-included-samples.md)
</dt> </dl>

 

 
