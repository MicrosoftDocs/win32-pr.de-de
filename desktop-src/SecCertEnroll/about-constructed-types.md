---
description: Ein konstruierter Typ der abstrakten Syntax Notation One (ASN. 1) besteht aus grundlegenden Typen, Zeichen folgen Typen oder anderen konstruierten Typen. Beispielsweise besteht eine X. 509-Zertifikats Erweiterung aus drei grundlegenden ASN. 1-Typen, wie im folgenden Beispiel gezeigt.
ms.assetid: 90c52d71-5d5b-479c-8e29-06c9f0f6da4a
title: Konstruierte Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a515e6e03ebf3c95ff1cabc1bf7f12eb423df27d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346504"
---
# <a name="constructed-types"></a>Konstruierte Typen

Ein konstruierter Typ der [*abstrakten Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN. 1) besteht aus grundlegenden Typen, Zeichen folgen Typen oder anderen konstruierten Typen. Beispielsweise besteht eine X. 509-Zertifikats Erweiterung aus drei grundlegenden ASN. 1-Typen, wie im folgenden Beispiel gezeigt.

``` syntax
Extension ::= SEQUENCE 
{
   extnId              OBJECT IDENTIFIER,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTET STRING
}
```

Eine Erweiterung besteht aus einem [*Objekt Bezeichner*](/windows/desktop/SecGloss/o-gly) (OID), einem booleschen Wert, der angibt, ob die Erweiterung kritisch ist, und einem Bytearray, das den Wert enthält. Die Zertifikatregistrierungs-API unterstützt die folgenden erstellten ASN. 1-Typen.

## <a name="sequence-and-sequence-of"></a>Sequenz und Sequenz von

Codierungstag: 0x30

Enthält eine geordnete Reihe von Feldern von einem oder mehreren Typen. Felder können als **optional** oder **Standard** markiert werden. Um Mehrdeutigkeit beim Decodieren zu vermeiden, sollten sich aufeinander folgende optionale Felder durch Verwendung eines eindeutigen Bezeichners (eine Ganzzahl mit Klammern, wie z. b. \[ 1 \] ) und aus einem folgenden Pflichtfeld unterscheiden, wie im folgenden Beispiel gezeigt.

``` syntax
SomeValue ::= SEQUENCE 
{
   a     INTEGER,
   b     [0] INTEGER OPTIONAL,
   c     [1] INTEGER DEFAULT 1,
   d     INTEGER
}
```

Der Unterschied zwischen **Sequence** und **Sequence** besteht darin, dass die Elemente einer **Sequenz von** Construct denselben Typ aufweisen müssen. Siehe folgendes Beispiel. Beide Konstrukte haben den gleichen Tagwert (0x30), wenn Sie codiert sind.

``` syntax
PolicyQualifiers ::=  SEQUENCE OF PolicyQualifierInfo

PolicyQualifierInfo ::= SEQUENCE 
{
   policyQualifierId   OBJECT IDENTIFIER,
   qualifier           ANY OPTIONAL
}
```

Eine andere Möglichkeit, den Unterschied zwischen **Sequenz** und **Sequenz von** zu überprüfen, besteht darin, Sie mit ihren Entsprechungen in der Programmiersprache C zu vergleichen. Das heißt, die **Sequenz** entspricht ungefähr einer Struktur, und die **Sequenz von** entspricht ungefähr einem Array.

## <a name="set-and-set-of"></a>Set und Set von

Codierungstag: 0x31

Enthält eine ungeordnete Reihe von Feldern von einem oder mehreren Typen. Dies unterscheidet sich von einer **Sequenz** , die eine geordnete Liste enthält. Wenn Sie eine ungeordnete Liste angeben, kann eine Anwendung die Struktur Felder dem Encoder in der am besten geeigneten Reihenfolge bereitstellen. Wie bei **Sequence** können die **Felder eines Mengen Konstrukts** mit **optionalen** oder **Standard** Werten gekennzeichnet werden, und eindeutige Bezeichner müssen verwendet werden, um den Decodierungs Prozess zu unterscheiden. Der Unterschied zwischen **Set** und **Set von** besteht darin, dass die Elemente eines **Satzes von** Konstrukte denselben Typ aufweisen müssen.

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

Definiert eine Auswahl zwischen Alternativen. Jede Alternative muss durch eine in Klammern gesetzte Ganzzahl eindeutig identifiziert werden, um Mehrdeutigkeiten beim Decodieren zu vermeiden. Beim Codieren erhält das **Choice** -Konstrukt den Wert des Codierungs Tags der ausgewählten Alternative.

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

[ASN. 1-Typsystem](about-asn-1-type-system.md)
</dt> <dt>

[Der-Codierung von ASN. 1-Typen](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> </dl>

 

 
