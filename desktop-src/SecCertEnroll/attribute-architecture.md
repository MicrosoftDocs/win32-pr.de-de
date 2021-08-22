---
description: Wird verwendet, um einer Zertifikatanforderung Attribute hinzuzufügen.
ms.assetid: 7007c751-f1a4-4ddc-a66e-d3edefc6ed97
title: Attributarchitektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c3d09a2a351635547c21357477290cb3335cb8c1da042d680762140b48b03f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903237"
---
# <a name="attribute-architecture"></a>Attributarchitektur

Die folgenden Schnittstellen werden verwendet, um einer Zertifikatanforderung Attribute hinzuzufügen:

-   [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
-   [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
-   [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
-   [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)

Die Architektur folgt der Definition im ASN.1-Modul der PKCS \# 10-Zertifizierungsanforderungssyntax.

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 ANY,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}
```

Die [**ICryptAttributes-Auflistung**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) entspricht dem **Attributfeld,** und jedes [**ICryptAttribute-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) in der Auflistung entspricht einer ASN.1-Attributstruktur. 

Jedes **Attribut** besteht aus einem Objektbezeichner (OID) und null oder mehr Werten, die der OID zugeordnet sind. Ein einzelnes OID-Wert-Paar wird durch eine [**IX509Attribute-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) dargestellt. Sie können eine [**IX509Attributes-Auflistung**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) verwenden, um ein [**ICryptAttribute-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) zu initialisieren, aber jedes Attribut in der Auflistung muss derselben OID zugeordnet sein. In der Regel hat ein Attribut nur einen Wert.

Sie können eine der folgenden Schnittstellen verwenden, die von [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)abgeleitet sind, um ein einzelnes OID-Wert-Attributpaar zu erstellen:

-   [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)
-   [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)
-   [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)
-   [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)
-   [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)
-   [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)
-   [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate)

Das folgende Verfahren zeigt z. B. das Erstellen eines **ClientId-Attributs.**

**So erstellen Sie ein **ClientId-Attribut****

1.  Rufen Sie [**ein ICryptAttributes-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) aus einem [**IX509CertificateRequestPkcs10-**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) oder [**IX509CertificateRequestCmc-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) ab.
2.  Erstellen und initialisieren Sie [**ein IX509AttributeClientId-Objekt.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)
3.  Erstellen Sie eine [**IX509Attributes-Auflistung,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) und fügen Sie das [**Objekt IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) hinzu.
4.  Verwenden Sie die [**IX509Attributes-Auflistung,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) um ein [**ICryptAttribute-Objekt zu**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) initialisieren.
5.  Fügen Sie [**das ICryptAttribute-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) der Auflistung hinzu, die Sie in Schritt 1 abgerufen haben.

Das folgende Beispiel zeigt die ASN.1-Ausgabe des **ClientId-Attributs.** Das Attribut enthält den DNS-Namen des Computers, auf dem die Anforderung generiert wurde (test3d.jdomcsc.nttest.microsoft.com), den SAM-Namen des Benutzers (JDOMCSC-Administrator) und den Namen der Anwendung, die die Anforderung \\ generiert hat (certreq).

``` syntax
0136: 30 57; SEQUENCE (57 Bytes)
0138: |  06 09                            ; OBJECT_ID (9 Bytes)
013a: |  |  2b 06 01 04 01 82 37 15  14
      |  |     ; 1.3.6.1.4.1.311.21.20 Client Information
0143: |  |  31 4a                         ; SET (4a Bytes)
0145: |  |     30 48                      ; SEQUENCE (48 Bytes)
0147: |  |        02 01                   ; INTEGER (1 Bytes)
0149: |  |        |  09
014a: |  |        0c 23                   ; UTF8_STRING (23 Bytes)
014c: |  |        |  74 65 73 74 33 64 2e 6a  64 6f 6d 63 73 63 2e 6e 
015c: |  |        |  74 74 65 73 74 2e 6d 69  63 72 6f 73 6f 66 74 2e 
016c: |  |        |  63 6f 6d                                         
      |  |        |     ; "test3d.jdomcsc.nttest.microsoft.com"
016f: |  |        0c 15                   ; UTF8_STRING (15 Bytes)
0171: |  |        |  4a 44 4f 4d 43 53 43 5c  61 64 6d 69 6e 69 73 74 
0181: |  |        |  72 61 74 6f 72                                   
      |  |        |     ; "JDOMCSC\administrator"
0186: |  |        0c 07                   ; UTF8_STRING (7 Bytes)
0188: |  |           63 65 72 74 72 65 71                             
      |  |              ; "certreq"
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
</dt> <dt>

[**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
</dt> <dt>

[**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
</dt> <dt>

[**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
</dt> </dl>

 

 



