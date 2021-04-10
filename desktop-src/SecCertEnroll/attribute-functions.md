---
description: Attribute können einer Zertifikat Anforderung hinzugefügt werden, um eine Zertifizierungsstelle (Certification Authority, ca) mit zusätzlichen Informationen bereitzustellen, die Sie beim Erstellen und Ausstellen eines Zertifikats verwenden kann.
ms.assetid: 3eba5a2f-eeac-4e38-8705-b12bc183b7eb
title: Attribut Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6413da0d43c142373e6f3cabe3d8e31636b82ef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215873"
---
# <a name="attribute-functions"></a>Attribut Funktionen

Attribute können einer Zertifikat Anforderung hinzugefügt werden, um eine [*Zertifizierungsstelle (Certification Authority*](/windows/desktop/SecGloss/c-gly) , ca) mit zusätzlichen Informationen bereitzustellen, die Sie beim Erstellen und Ausstellen eines Zertifikats verwenden kann.

CertEnroll.dll implementiert die folgenden Schnittstellen zum Definieren von Attributen und Attribut Auflistungen:

-   [**Icryptattribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
-   [**Icryptattributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
-   [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
-   [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
-   [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)
-   [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)
-   [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)
-   [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)
-   [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)
-   [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)
-   [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate)

In den folgenden Abschnitten werden die von Xenroll.dll exportierten Funktionen identifiziert, um kryptografieattribute Zertifikat Anforderungen zuzuordnen, und es wird erläutert, wie CertEnroll.dll verwendet wird, um die Funktion zu ersetzen oder anzugeben, dass keine Zuordnung zwischen den beiden Bibliotheken besteht:

-   [addattributetor equestwstr](#addattributetorequestwstr)
-   [AddAuthenticatedAttributesToPKCS7Request](#addauthenticatedattributestopkcs7request)
-   [addnamevaluepuntor equestwstr](#addnamevaluepairtorequestwstr)
-   [Addnamevaluepaar-zu-signaturewstr](#addnamevaluepairtosignaturewstr)
-   [ClientID](#clientid)
-   [Erneuerungs Zertifikat](#renewalcertificate)
-   [reantattributes](#resetattributes)
-   [Zugehörige Themen](#related-topics)

## <a name="addattributetorequestwstr"></a>addattributetor equestwstr

Die [**addattributetorequestwstr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) -Funktion in Xenroll.dll fügt einer Zertifikat Anforderung ein Attribut hinzu.

Im Allgemeinen können Sie zum Hinzufügen eines Attributs zu einer Anforderung mithilfe der in CertEnroll.dll implementierten Objekte die folgenden Aktionen ausführen:

1.  Erstellen Sie ein [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) -Sammlungsobjekt.
2.  Erstellen Sie ein [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) -Objekt, und rufen Sie die [**Initialize**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attribute-initialize) -Methode auf, um ein Attribut aus einem Objekt Bezeichner und einem Attribut Wert zu erstellen, oder verwenden Sie eine der zuvor aufgelisteten Schnittstellen, um eines der allgemeineren Attribute zu definieren.
3.  Fügen Sie jedes neue Attribut, das im vorherigen Schritt erstellt wurde, mithilfe der [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-add) -Methode der [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) -Auflistung hinzu.
4.  Erstellen Sie ein [**icryptattribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) -Objekt, und initialisieren Sie es, indem Sie die [**initializefromvalues**](/windows/desktop/api/CertEnroll/nf-certenroll-icryptattribute-initializefromvalues) -Methode aufrufen und die [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) -Auflistung bei der Eingabe angeben.
5.  Rufen Sie ein [**icryptattributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) -Sammlungsobjekt ab, indem Sie die [**cryptattributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes) -Eigenschaft für ein vorhandenes [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -oder [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) Request-Objekt aufrufen.
6.  Fügen Sie das [**icryptattribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) -Objekt der [**icryptattributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) -Auflistung hinzu.

## <a name="addauthenticatedattributestopkcs7request"></a>AddAuthenticatedAttributesToPKCS7Request

Authentifizierte Attribute sind Name-Wert-Paare, die signiert werden und einer Signatur hinzugefügt werden. Die [**AddAuthenticatedAttributesToPKCS7Request**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addauthenticatedattributestopkcs7request) -Funktion in Xenroll.dll fügt ein Array von authentifizierten Attributen zu einer [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) -Anforderung hinzu.

Wie bereits erwähnt, können [](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) Sie CertEnroll.dll verwenden, um eine Auflistung von Attributen auf einfache Weise zu definieren und einer Zertifikat Anforderung hinzuzufügen. Sie können jedoch nicht auswählen, ob das Attribut authentifiziert ist. Der Registrierungsvorgang trifft diese Entscheidung automatisch.

## <a name="addnamevaluepairtorequestwstr"></a>addnamevaluepuntor equestwstr

Die [**addnamevaluepairren torequestwstr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addnamevaluepairtorequestwstr) -Funktion in Xenroll.dll fügt einer Anforderung ein nicht authentifiziertes Name-Wert-Paar hinzu.

Sie können die [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) -Schnittstelle in CertEnroll.dll verwenden, um ein Name-Wert-Paar zu definieren, und Sie können eine Auflistung von Name-Wert-Paaren zu einem Objekt der CMC-Anforderung hinzufügen, indem Sie die folgenden Aktionen ausführen:

1.  Erstellen und initialisieren Sie ein [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) -Objekt. Der Initialisierungs Prozess erstellt eine leere [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) -Auflistung.
2.  Rufen Sie die [**NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) -Eigenschaft für ein vorhandenes Objekt "CMC Request" auf, um die Auflistung abzurufen.
3.  Erstellen und initialisieren Sie ein [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) -Objekt.
4.  Fügen Sie jedes neue Name/Wert-Paar der [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) -Auflistung hinzu, indem [**Sie die Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509namevaluepairs-add) -Methode aufrufen.

Bei der Registrierung wird die Auflistung von Name-Wert-Paaren in die **taggedattribute** -Struktur der CMC-Anforderung eingefügt.

## <a name="addnamevaluepairtosignaturewstr"></a>Addnamevaluepaar-zu-signaturewstr

Die [**addnamevaluepairitosignaturewstr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addnamevaluepairtosignaturewstr) -Funktion in Xenroll.dll fügt einer Anforderung ein authentifiziertes Name/Wert-Paar hinzu. Dies wird normalerweise verwendet, um den Anforderer Namen in einer eobo-Anforderung (ENROLL-on-Auftrag-of) anzugeben.

Verwenden Sie in CertEnroll.dll die Eigenschaft [**requestername**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_requestername) , um den Namen in einer eobo-Anforderung anzugeben.

## <a name="clientid"></a>ClientId

Die [**ClientID-**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_clientid) Funktion in Xenroll.dll gibt ein **ClientID-** Attribut an oder ruft es ab.

Verwenden Sie die [**ClientID-**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_clientid) Eigenschaft in CertEnroll.dll, um dieses Attribut einer CMC-oder PKCS 10-Anforderung hinzuzufügen \# .

## <a name="renewalcertificate"></a>Erneuerungs Zertifikat

Die [**renewalcertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_renewalcertificate) -Funktion in Xenroll.dll gibt ein **renewalcertificate** -Attribut an oder ruft es ab.

Wenn Sie in CertEnroll.dll den Befehl [**initializefromcertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) für ein PKCS \# 7-oder PKCS-Objekt aufgerufen haben, wird automatisch erstellt.

## <a name="resetattributes"></a>reantattributes

Die [**resettattributes**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-resetattributes) -Funktion in Xenroll.dll entfernt die Attribut Auflistung aus einer Anforderung.

Zum Entfernen eines Attributs aus einer Anforderung durch einen Index mithilfe von CertEnroll.dll, nennen Sie die [**Remove**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-remove) -Methode für die [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) -Auflistung. Um alle Attribute aus einer Anforderung zu entfernen, müssen Sie die [**Clear**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-clear) -Methode aufzurufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnung von Xenroll.dll zu CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**Icryptattribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
</dt> <dt>

[**Icryptattributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
</dt> <dt>

[**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
</dt> <dt>

[**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
</dt> <dt>

[**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)
</dt> <dt>

[**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs)
</dt> </dl>

 

 
