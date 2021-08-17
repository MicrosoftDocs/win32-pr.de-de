---
description: Erstellt eine benutzerdefinierte PKCS \# 10-Anforderung, sendet sie an eine eigenständige Zertifizierungsstelle und installiert das ausgestellte Zertifikat im Zertifikatspeicher.
ms.assetid: dcb69d7e-457e-457b-9eea-15676ed710aa
title: enrollCustomPKCS10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 937b1e955ecd369794e832f16afff1594ed1df1271494d7172832132d4cb7863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780029"
---
# <a name="enrollcustompkcs10"></a>enrollCustomPKCS10

Im Beispiel enrollCustomPKCS10 wird eine benutzerdefinierte PKCS \# 10-Anforderung erstellt, an eine eigenständige Zertifizierungsstelle übermittelt und das ausgestellte Zertifikat im Zertifikatspeicher installiert. Für eine eigenständige Zertifizierungsstelle ist Active Directory nicht erforderlich, und es werden keine Vorlagen verwendet.

## <a name="location"></a>Standort

Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner *%ProgramFiles%* \\ Microsoft SDKs Windows \\ \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ enrollCustomPKCS10 installiert.

## <a name="discussion"></a>Diskussion (Discussion)

Das Beispiel enrollCustomPKCS10:

1.  Verarbeitet die Befehlszeilenargumente. Die Befehlszeile sollte den X.500-Zertifikatssubjektnamen, den E-Mail-Namen (RFC822) und einen EKU-Objektbezeichner (Enhanced Key Usage, erweiterte Schlüsselverwendung) enthalten. Sie können z. B. die folgenden Argumente angeben, um zu *user1@example.com* registrieren:
    -   Antragstellername: "*CN=user1,DC=example,DC=com*"
    -   RFC822-Name: *user1@example.com*
    -   EKU-OID für Clientauthentifizierung: 1.3.6.1.5.5.7.3.2
2.  Erstellt ein [**IX509CertificateRequestPkcs10-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) und initialisiert es für den Endbenutzer, indem der **ContextUser-Wert** der [**X509CertificateEnrollmentContext-Enumeration**](/windows/desktop/api/CertEnroll/ne-certenroll-x509certificateenrollmentcontext) angegeben wird.
3.  Erstellt ein [**IX500DistinguishedName-Objekt,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) verwendet das -Objekt, um den Antragstellernamen in ein Bytearray zu codieren, und fügt das Array dem PKCS \# 10-Anforderungsobjekt hinzu.
4.  Erstellt ein [**IObjectId-Objekt,**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) initialisiert es mithilfe des in der Befehlszeile angegebenen EKU-Objektbezeichners (OID), erstellt eine [**IObjectIds-Auflistung,**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectids) fügt der Auflistung das neue **IObjectId-Objekt** (EKU) hinzu, verwendet die Auflistung, um ein [**IX509ExtensionEnhancedKeyUsage-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) zu initialisieren, und fügt dieses Objekt der Anforderung hinzu.
5.  Erstellt ein [**IAlternativeName-Objekt,**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) initialisiert es mit dem in der Befehlszeile angegebenen RFC822-Namen, erstellt eine [**IAlternativeNames-Auflistung,**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) fügt der Auflistung das neue **IAlternativeName** -Objekt (RFC822-Name ) hinzu, erstellt ein [**IX509ExtensionAlternativeNames-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) und fügt dieses Objekt der Anforderung hinzu.
6.  Erstellt ein [**IX509Enrollment-Objekt,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) initialisiert es mit dem [**IX509CertificateRequestPkcs10-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) und ruft eine Zeichenfolge ab, die eine Base64-codierte Anforderung enthält.
7.  Erstellt ein [**ICertConfig-Objekt**](/windows/desktop/api/certcli/nn-certcli-icertconfig) und verwendet es, um eine Zeichenfolge abzurufen, die die Zertifizierungsstellenkonfiguration enthält.
8.  Erstellt ein [**CryptoAPI-ICertRequest2-Objekt**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) und verwendet es sowie die Zeichenfolgen, die die Zertifizierungsstellenkonfiguration und die Zertifikatanforderung enthalten, um die Anforderung an die Zertifizierungsstelle zu übermitteln.
9.  Überprüft den Übermittlungsstatus und installiert bei erfolgreicher Registrierung das Zertifikat im Zertifikatspeicher.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[PKCS \# 10-Anforderung](pkcs--10-request.md)
</dt> <dt>

[Verwenden der enthaltenen Beispiele](using-the-included-samples.md)
</dt> </dl>

 

 
