---
description: Wird verwendet, um einer Zertifikat Anforderung Attribute hinzuzufügen.
ms.assetid: 7007c751-f1a4-4ddc-a66e-d3edefc6ed97
title: Attribut Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64d83171985c062fd2d8d4ae968c2ef4d36a29ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344949"
---
# <a name="attribute-architecture"></a>Attribut Architektur

Die folgenden Schnittstellen werden verwendet, um einer Zertifikat Anforderung Attribute hinzuzufügen:

-   [**Icryptattribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
-   [**Icryptattributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
-   [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
-   [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)

Die Architektur folgt, die im ASN. 1-Modul der PKCS \# 10-Zertifizierungs Anforderungs Syntax definiert ist.

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

Die [**icryptattributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) -Auflistung entspricht dem Feld **Attribute** , und jedes [**icryptattribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) -Objekt in der Auflistung entspricht der ASN. 1- **Attribut** Struktur.

Jedes **Attribut** besteht aus einem Objekt Bezeichner (OID) und 0 (null) oder Mehrwerten, die mit der OID verknüpft sind. Ein einzelnes OID-Wert-Paar wird durch eine [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) -Schnittstelle dargestellt. Sie können eine [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) -Auflistung verwenden, um ein [**icryptattribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) -Objekt zu initialisieren, aber jedes Attribut in der Auflistung muss derselben OID zugeordnet werden. In der Regel hat ein Attribut nur einen Wert.

Sie können eine der folgenden Schnittstellen verwenden, die von [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)abgeleitet werden, um ein einzelnes OID/Wert-Attribut paar zu erstellen:

-   [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)
-   [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)
-   [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)
-   [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)
-   [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)
-   [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)
-   [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate)

Das folgende Verfahren zeigt beispielsweise, wie Sie ein **ClientID-** Attribut erstellen.

**So erstellen Sie ein **ClientID-** Attribut**

1.  Rufen Sie ein [**icryptattributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) -Objekt aus einem [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -oder [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) -Objekt ab.
2.  Erstellen und initialisieren Sie ein [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) -Objekt.
3.  Erstellen Sie eine [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) Collection, und fügen Sie das [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) -Objekt hinzu.
4.  Verwenden Sie die [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) -Auflistung, um ein [**icryptattribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) -Objekt zu initialisieren.
5.  Fügen Sie das [**icryptattribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) -Objekt der Auflistung hinzu, die Sie in Schritt 1 abgerufen haben.

Das folgende Beispiel zeigt die ASN. 1-Ausgabe des **ClientID-** Attributs. Das-Attribut enthält den DNS-Namen des Computers, auf dem die Anforderung generiert wurde (test3d.jdomcsc.nttest.Microsoft.com), den SAM-Namen des Benutzers (jdomcsc \\ -Administrator) und den Namen der Anwendung, die die Anforderung generiert hat (Certreq).

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

[**Icryptattribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
</dt> <dt>

[**Icryptattributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
</dt> <dt>

[**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
</dt> <dt>

[**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
</dt> </dl>

 

 



