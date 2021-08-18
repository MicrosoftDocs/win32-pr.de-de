---
description: Attribute können einer Zertifikatanforderung hinzugefügt werden, um einer Zertifizierungsstelle zusätzliche Informationen bereitzustellen, die sie beim Erstellen und Ausstellen eines Zertifikats verwenden kann.
ms.assetid: 3eba5a2f-eeac-4e38-8705-b12bc183b7eb
title: Attributfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a353b5beb5b7da048edf8712c5d82545fd326a7d1720748705ae093aaa2cc44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903112"
---
# <a name="attribute-functions"></a>Attributfunktionen

Attribute können einer Zertifikatanforderung hinzugefügt werden, um einer [*Zertifizierungsstelle*](/windows/desktop/SecGloss/c-gly) zusätzliche Informationen bereitzustellen, die sie beim Erstellen und Ausstellen eines Zertifikats verwenden kann.

CertEnroll.dll implementiert die folgenden Schnittstellen, um Attribute und Attributsammlungen zu definieren:

-   [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
-   [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
-   [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
-   [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
-   [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)
-   [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)
-   [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)
-   [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)
-   [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)
-   [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)
-   [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate)

In den folgenden Abschnitten werden von Xenroll.dll exportierte Funktionen identifiziert, um Zertifikatanforderungen kryptografische Attribute zuzuordnen. Außerdem wird erläutert, wie sie CertEnroll.dll verwenden, um die Funktion zu ersetzen, oder sie zeigen an, dass keine Zuordnung zwischen den beiden Bibliotheken vorhanden ist:

-   [addAttributeToRequestWStr](#addattributetorequestwstr)
-   [AddAuthenticatedAttributesToPKCS7Request](#addauthenticatedattributestopkcs7request)
-   [addNameValuePairToRequestWStr](#addnamevaluepairtorequestwstr)
-   [AddNameValuePairToSignatureWStr](#addnamevaluepairtosignaturewstr)
-   [Clientid](#clientid)
-   [RenewalCertificate](#renewalcertificate)
-   [resetAttributes](#resetattributes)
-   [Zugehörige Themen](#related-topics)

## <a name="addattributetorequestwstr"></a>addAttributeToRequestWStr

Die [**addAttributeToRequestWStr-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) in Xenroll.dll fügt einer Zertifikatanforderung ein Attribut hinzu.

Um einer Anforderung mithilfe der in CertEnroll.dll implementierten Objekte ein Attribut hinzuzufügen, können Sie im Allgemeinen die folgenden Aktionen ausführen:

1.  Erstellen Sie ein [**IX509Attributes-Auflistungsobjekt.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
2.  Erstellen Sie ein [**IX509Attribute-Objekt,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) und rufen Sie die [**Initialize-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attribute-initialize) auf, um ein Attribut aus einem Objektbezeichner und Attributwert zu erstellen, oder verwenden Sie eine der zuvor aufgeführten Schnittstellen, um eines der allgemeineren Attribute zu definieren.
3.  Fügen Sie jedes im vorherigen Schritt erstellte neue Attribut mithilfe der Add-Methode der [**IX509Attributes-Auflistung**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) [**hinzu.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-add)
4.  Erstellen Sie ein [**ICryptAttribute-Objekt,**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) und initialisieren Sie es, indem Sie die [**InitializeFromValues-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-icryptattribute-initializefromvalues) aufrufen und die [**IX509Attributes-Auflistung**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) bei der Eingabe angeben.
5.  Rufen Sie ein [**ICryptAttributes-Auflistungsobjekt**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) ab, indem Sie die [**CryptAttributes-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes) für ein vorhandenes [**IX509CertificateRequestPkcs10-**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) oder [**IX509CertificateRequestCmc-Anforderungsobjekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) aufrufen.
6.  Fügen Sie das [**ICryptAttribute-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) der [**ICryptAttributes-Auflistung**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) hinzu.

## <a name="addauthenticatedattributestopkcs7request"></a>AddAuthenticatedAttributesToPKCS7Request

Authentifizierte Attribute sind Name-Wert-Paare, die von signiert und einer Signatur hinzugefügt werden. Die [**AddAuthenticatedAttributesToPKCS7Request-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addauthenticatedattributestopkcs7request) in Xenroll.dll fügt einer [*PKCS \# 7-Anforderung*](/windows/desktop/SecGloss/p-gly) ein Array authentifizierter Attribute hinzu.

Wie oben für die [**addAttributeToRequestWStr-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) erläutert, können Sie CertEnroll.dll verwenden, um eine Sammlung von Attributen einfach zu definieren und einer Zertifikatanforderung hinzuzufügen. Sie können jedoch nicht auswählen, ob das Attribut authentifiziert ist. Der Registrierungsprozess trifft diese Entscheidung automatisch.

## <a name="addnamevaluepairtorequestwstr"></a>addNameValuePairToRequestWStr

Die [**addNameValuePairToRequestWStr-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addnamevaluepairtorequestwstr) in Xenroll.dll fügt einer Anforderung ein nicht authentifiziertes Name-Wert-Paar hinzu.

Sie können die [**IX509NameValuePair-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) in CertEnroll.dll verwenden, um ein Name-Wert-Paar zu definieren, und Sie können einem CMC-Anforderungsobjekt eine Auflistung von Name-Wert-Paaren hinzufügen, indem Sie die folgenden Aktionen ausführen:

1.  Erstellen und initialisieren Sie ein [**IX509CertificateRequestCmc-Objekt.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) Beim Initialisierungsprozess wird eine leere [**IX509NameValuePairs-Auflistung**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) erstellt.
2.  Rufen Sie die [**NameValuePairs-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) für ein vorhandenes CMC-Anforderungsobjekt auf, um die Auflistung abzurufen.
3.  Erstellen und initialisieren Sie ein [**IX509NameValuePair-Objekt.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)
4.  Fügen Sie jedes neue Name-Wert-Paar der [**IX509NameValuePairs-Auflistung**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) hinzu, indem Sie die [**Add-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509namevaluepairs-add) aufrufen.

Der Registrierungsprozess platziert die Auflistung von Name-Wert-Paaren in der **TaggedAttribute-Struktur** der CMC-Anforderung.

## <a name="addnamevaluepairtosignaturewstr"></a>AddNameValuePairToSignatureWStr

Die [**Funktion AddNameValuePairToSignatureWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addnamevaluepairtosignaturewstr) in Xenroll.dll fügt einer Anforderung ein authentifiziertes Name-Wert-Paar hinzu. Dies wird in der Regel verwendet, um den Anforderernamen in einer EOBO-Anforderung (Enroll-on-behalf-of) anzugeben.

Verwenden Sie in CertEnroll.dll die [**RequesterName-Eigenschaft,**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_requestername) um den Namen in einer EOBO-Anforderung anzugeben.

## <a name="clientid"></a>ClientId

Die [**ClientId-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_clientid) in Xenroll.dll gibt ein **ClientId-Attribut** an oder ruft es ab.

Verwenden Sie die [**ClientId-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_clientid) in CertEnroll.dll, um dieses Attribut einer CMC- oder PKCS \# 10-Anforderung hinzuzufügen.

## <a name="renewalcertificate"></a>RenewalCertificate

Die [**RenewalCertificate-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_renewalcertificate) in Xenroll.dll gibt ein **RenewalCertificate-Attribut** an oder ruft es ab.

In CertEnroll.dll wird beim Aufrufen [**von InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) für ein PKCS \# 7- oder PKCS -Objekt automatisch erstellt.

## <a name="resetattributes"></a>resetAttributes

Die [**resetAttributes-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-resetattributes) in Xenroll.dll entfernt die Attributauflistung aus einer Anforderung.

Um ein Attribut mithilfe von CertEnroll.dll aus einer Anforderung nach Index zu entfernen, rufen Sie die [**Remove-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-remove) für die [**IX509Attributes-Auflistung**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) auf. Um alle Attribute aus einer Anforderung zu entfernen, rufen Sie die [**Clear-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-clear) auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnen von Xenroll.dll zu CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
</dt> <dt>

[**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
</dt> <dt>

[**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
</dt> <dt>

[**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
</dt> <dt>

[**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)
</dt> <dt>

[**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs)
</dt> </dl>

 

 
