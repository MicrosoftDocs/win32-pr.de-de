---
description: Ein konstruierter ASN.1-Typ (Abstract Syntax Notation One) besteht aus grundlegenden Typen, Zeichenfolgentypen oder anderen konstruierten Typen. Beispielsweise besteht eine X.509-Zertifikaterweiterung aus drei grundlegenden ASN.1-Typen, wie im folgenden Beispiel gezeigt.
ms.assetid: 90c52d71-5d5b-479c-8e29-06c9f0f6da4a
title: Konstruierte Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ed62c4a59bfc0944ad5e31673ab0ea9031c0175014c8fc1c6b6f2cc071b153
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904489"
---
# <a name="constructed-types"></a>Konstruierte Typen

Ein konstruierter ASN.1-Typ [*(Abstract Syntax Notation One)*](/windows/desktop/SecGloss/a-gly) besteht aus grundlegenden Typen, Zeichenfolgentypen oder anderen konstruierten Typen. Beispielsweise besteht eine X.509-Zertifikaterweiterung aus drei grundlegenden ASN.1-Typen, wie im folgenden Beispiel gezeigt.

``` syntax
Extension ::= SEQUENCE 
{
   extnId              OBJECT IDENTIFIER,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTET STRING
}
```

Eine Erweiterung besteht aus einem [*Objektbezeichner*](/windows/desktop/SecGloss/o-gly) (OID), einem booleschen Wert, der angibt, ob die Erweiterung kritisch ist, und einem Bytearray, das den Wert enthält. Die Zertifikatregistrierungs-API unterstützt die folgenden konstruierten ASN.1-Typen.

## <a name="sequence-and-sequence-of"></a>SEQUENCE und SEQUENCE OF

Codierungstag: 0x30

Enthält eine geordnete Reihe von Feldern eines oder mehrerer Typen. Felder können als **OPTIONAL** oder **DEFAULT** gekennzeichnet werden. Um Mehrdeutigkeiten beim Decodieren zu vermeiden, sollten sich aufeinander folgende optionale Felder unterscheiden, indem sie einen eindeutigen Bezeichner (eine ganze Zahl in Klammern wie \[ 1) und ein folgendes erforderliches Feld verwenden, \] wie im folgenden Beispiel gezeigt.

``` syntax
SomeValue ::= SEQUENCE 
{
   a     INTEGER,
   b     [0] INTEGER OPTIONAL,
   c     [1] INTEGER DEFAULT 1,
   d     INTEGER
}
```

Der Unterschied zwischen **SEQUENCE** und **SEQUENCE OF** besteht darin, dass die Elemente eines **SEQUENCE OF-Konstrukts** denselben Typ aufweisen müssen. Siehe folgendes Beispiel. Beide Konstrukte haben bei der Codierung denselben Tagwert (0x30).

``` syntax
PolicyQualifiers ::=  SEQUENCE OF PolicyQualifierInfo

PolicyQualifierInfo ::= SEQUENCE 
{
   policyQualifierId   OBJECT IDENTIFIER,
   qualifier           ANY OPTIONAL
}
```

Eine weitere Möglichkeit, den Unterschied zwischen **SEQUENCE** und **SEQUENCE OF** zu untersuchen, besteht darin, sie mit ihren Entsprechungen in der Programmiersprache C zu vergleichen. Das heißt, **SEQUENCE** entspricht ungefähr einer -Struktur und **SEQUENCE OF** entspricht ungefähr einem Array.

## <a name="set-and-set-of"></a>SET und SET OF

Codierungstag: 0x31

Enthält eine ungeordnete Reihe von Feldern eines oder mehrerer Typen. Dies unterscheidet  sich von einem SEQUENCE-Wert, der eine sortierte Liste enthält. Durch die Angabe einer unsortierten Liste kann eine Anwendung die Strukturfelder dem Encoder in der am besten geeigneten Reihenfolge bereitstellen. Wie bei **SEQUENCE** können die Felder eines **SET-Konstrukts** mit **OPTIONAL** oder **DEFAULT** gekennzeichnet werden, und eindeutige Bezeichner müssen verwendet werden, um den Decodierungsprozess eindeutig zu unterscheiden. Der Unterschied zwischen **SET** und **SET OF** besteht darin, dass die Elemente eines **SET OF-Konstrukts** denselben Typ aufweisen müssen.

``` syntax
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       OBJECT IDENTIFIER,
   value      ANY 
}
```

## <a name="choice"></a>Wahl

Codierungstag: nicht zutreffend

Definiert eine Auswahl zwischen Alternativen. Jede Alternative muss durch eine ganze Zahl in Klammern eindeutig identifiziert werden, um Mehrdeutigkeiten beim Decodieren zu vermeiden. Bei der Codierung hat das **CHOICE-Konstrukt** den Codierungstagwert der ausgewählten Alternative.

``` syntax
AltNames ::= SEQUENCE OF GeneralName

GeneralNames ::= AltNames

GeneralName ::= CHOICE 
{
   otherName               [0] IMPLICIT OtherName,
   rfc822Name              [1] IMPLICIT IA5String,
   dNSName                 [2] IMPLICIT IA5String,
   x400Address             [3] IMPLICIT SeqOfAny,
   directoryName           [4] EXPLICIT Name,
   ediPartyName            [5] IMPLICIT SEQUENCE OF ANY,
   uniformResourceLocator  [6] IMPLICIT IA5String,
   iPAddress               [7] IMPLICIT OCTET STRING,
   registeredID            [8] IMPLICIT OBJECT IDENTIFIER
}
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASN.1-Typsystem](about-asn-1-type-system.md)
</dt> <dt>

[DER-Codierung von ASN.1-Typen](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> </dl>

 

 
