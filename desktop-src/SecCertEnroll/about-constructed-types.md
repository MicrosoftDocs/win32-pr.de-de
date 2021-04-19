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
# <a name="constructed-types"></a><span data-ttu-id="931ee-104">Konstruierte Typen</span><span class="sxs-lookup"><span data-stu-id="931ee-104">Constructed Types</span></span>

<span data-ttu-id="931ee-105">Ein konstruierter Typ der [*abstrakten Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN. 1) besteht aus grundlegenden Typen, Zeichen folgen Typen oder anderen konstruierten Typen.</span><span class="sxs-lookup"><span data-stu-id="931ee-105">A constructed [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) type is made up from basic types, string types, or other constructed types.</span></span> <span data-ttu-id="931ee-106">Beispielsweise besteht eine X. 509-Zertifikats Erweiterung aus drei grundlegenden ASN. 1-Typen, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="931ee-106">For example, an X.509 certificate extension is composed from three basic ASN.1 types as shown by the following example.</span></span>

``` syntax
Extension ::= SEQUENCE 
{
   extnId              OBJECT IDENTIFIER,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTET STRING
}
```

<span data-ttu-id="931ee-107">Eine Erweiterung besteht aus einem [*Objekt Bezeichner*](/windows/desktop/SecGloss/o-gly) (OID), einem booleschen Wert, der angibt, ob die Erweiterung kritisch ist, und einem Bytearray, das den Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="931ee-107">An extension consists of an [*object identifier*](/windows/desktop/SecGloss/o-gly) (OID), a Boolean value that identifies whether the extension is critical, and a byte array that contains the value.</span></span> <span data-ttu-id="931ee-108">Die Zertifikatregistrierungs-API unterstützt die folgenden erstellten ASN. 1-Typen.</span><span class="sxs-lookup"><span data-stu-id="931ee-108">The Certificate Enrollment API supports the following constructed ASN.1 types.</span></span>

## <a name="sequence-and-sequence-of"></a><span data-ttu-id="931ee-109">Sequenz und Sequenz von</span><span class="sxs-lookup"><span data-stu-id="931ee-109">SEQUENCE and SEQUENCE OF</span></span>

<span data-ttu-id="931ee-110">Codierungstag: 0x30</span><span class="sxs-lookup"><span data-stu-id="931ee-110">Encoding tag: 0x30</span></span>

<span data-ttu-id="931ee-111">Enthält eine geordnete Reihe von Feldern von einem oder mehreren Typen.</span><span class="sxs-lookup"><span data-stu-id="931ee-111">Contains an ordered series of fields of one or more types.</span></span> <span data-ttu-id="931ee-112">Felder können als **optional** oder **Standard** markiert werden.</span><span class="sxs-lookup"><span data-stu-id="931ee-112">Fields can be marked **OPTIONAL** or **DEFAULT**.</span></span> <span data-ttu-id="931ee-113">Um Mehrdeutigkeit beim Decodieren zu vermeiden, sollten sich aufeinander folgende optionale Felder durch Verwendung eines eindeutigen Bezeichners (eine Ganzzahl mit Klammern, wie z. b. \[ 1 \] ) und aus einem folgenden Pflichtfeld unterscheiden, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="931ee-113">Also, to avoid ambiguity when decoding, successive optional fields should differ from one another by use of a unique identifier (a bracketed integer such as \[1\]) and from a following required field as shown by the following example.</span></span>

``` syntax
SomeValue ::= SEQUENCE 
{
   a     INTEGER,
   b     [0] INTEGER OPTIONAL,
   c     [1] INTEGER DEFAULT 1,
   d     INTEGER
}
```

<span data-ttu-id="931ee-114">Der Unterschied zwischen **Sequence** und **Sequence** besteht darin, dass die Elemente einer **Sequenz von** Construct denselben Typ aufweisen müssen.</span><span class="sxs-lookup"><span data-stu-id="931ee-114">The difference between **SEQUENCE** and **SEQUENCE OF** is that the elements of a **SEQUENCE OF** construct must be of the same type.</span></span> <span data-ttu-id="931ee-115">Siehe folgendes Beispiel.</span><span class="sxs-lookup"><span data-stu-id="931ee-115">See the following example.</span></span> <span data-ttu-id="931ee-116">Beide Konstrukte haben den gleichen Tagwert (0x30), wenn Sie codiert sind.</span><span class="sxs-lookup"><span data-stu-id="931ee-116">Both constructs have the same tag value (0x30) when encoded.</span></span>

``` syntax
PolicyQualifiers ::=  SEQUENCE OF PolicyQualifierInfo

PolicyQualifierInfo ::= SEQUENCE 
{
   policyQualifierId   OBJECT IDENTIFIER,
   qualifier           ANY OPTIONAL
}
```

<span data-ttu-id="931ee-117">Eine andere Möglichkeit, den Unterschied zwischen **Sequenz** und **Sequenz von** zu überprüfen, besteht darin, Sie mit ihren Entsprechungen in der Programmiersprache C zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="931ee-117">Another way to look at the difference between **SEQUENCE** and **SEQUENCE OF** is to compare them to their counterparts in the C programming language.</span></span> <span data-ttu-id="931ee-118">Das heißt, die **Sequenz** entspricht ungefähr einer Struktur, und die **Sequenz von** entspricht ungefähr einem Array.</span><span class="sxs-lookup"><span data-stu-id="931ee-118">That is, **SEQUENCE** is roughly equivalent to a structure and **SEQUENCE OF** is roughly equivalent to an array.</span></span>

## <a name="set-and-set-of"></a><span data-ttu-id="931ee-119">Set und Set von</span><span class="sxs-lookup"><span data-stu-id="931ee-119">SET and SET OF</span></span>

<span data-ttu-id="931ee-120">Codierungstag: 0x31</span><span class="sxs-lookup"><span data-stu-id="931ee-120">Encoding tag: 0x31</span></span>

<span data-ttu-id="931ee-121">Enthält eine ungeordnete Reihe von Feldern von einem oder mehreren Typen.</span><span class="sxs-lookup"><span data-stu-id="931ee-121">Contains an unordered series of fields of one or more types.</span></span> <span data-ttu-id="931ee-122">Dies unterscheidet sich von einer **Sequenz** , die eine geordnete Liste enthält.</span><span class="sxs-lookup"><span data-stu-id="931ee-122">This differs from a **SEQUENCE** which contains an ordered list.</span></span> <span data-ttu-id="931ee-123">Wenn Sie eine ungeordnete Liste angeben, kann eine Anwendung die Struktur Felder dem Encoder in der am besten geeigneten Reihenfolge bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="931ee-123">Specifying an unordered list enables an application to provide the structure fields to the encoder in the most appropriate order.</span></span> <span data-ttu-id="931ee-124">Wie bei **Sequence** können die **Felder eines Mengen Konstrukts** mit **optionalen** oder **Standard** Werten gekennzeichnet werden, und eindeutige Bezeichner müssen verwendet werden, um den Decodierungs Prozess zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="931ee-124">As with **SEQUENCE**, the fields of a **SET** construct can be marked with **OPTIONAL** or **DEFAULT**, and unique identifiers must be used to disambiguate the decoding process.</span></span> <span data-ttu-id="931ee-125">Der Unterschied zwischen **Set** und **Set von** besteht darin, dass die Elemente eines **Satzes von** Konstrukte denselben Typ aufweisen müssen.</span><span class="sxs-lookup"><span data-stu-id="931ee-125">The difference between **SET** and **SET OF** is that the elements of a **SET OF** construct must be of the same type.</span></span>

``` syntax
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       OBJECT IDENTIFIER,
   value      ANY 
}
```

## <a name="choice"></a><span data-ttu-id="931ee-126">Wahl</span><span class="sxs-lookup"><span data-stu-id="931ee-126">CHOICE</span></span>

<span data-ttu-id="931ee-127">Codierungstag: nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="931ee-127">Encoding tag: not applicable</span></span>

<span data-ttu-id="931ee-128">Definiert eine Auswahl zwischen Alternativen.</span><span class="sxs-lookup"><span data-stu-id="931ee-128">Defines a choice between alternatives.</span></span> <span data-ttu-id="931ee-129">Jede Alternative muss durch eine in Klammern gesetzte Ganzzahl eindeutig identifiziert werden, um Mehrdeutigkeiten beim Decodieren zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="931ee-129">Each alternative must be uniquely identified by a bracketed integer to avoid ambiguity when decoding.</span></span> <span data-ttu-id="931ee-130">Beim Codieren erhält das **Choice** -Konstrukt den Wert des Codierungs Tags der ausgewählten Alternative.</span><span class="sxs-lookup"><span data-stu-id="931ee-130">When encoded, the **CHOICE** construct will have the encoding tag value of the chosen alternative.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="931ee-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="931ee-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="931ee-132">ASN. 1-Typsystem</span><span class="sxs-lookup"><span data-stu-id="931ee-132">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="931ee-133">Der-Codierung von ASN. 1-Typen</span><span class="sxs-lookup"><span data-stu-id="931ee-133">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[<span data-ttu-id="931ee-134">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="931ee-134">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> </dl>

 

 
