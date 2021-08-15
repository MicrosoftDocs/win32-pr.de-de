---
title: Das abstrakte Schema
description: Der Schemacontainer enthält alle classSchema- und attributeSchema-Objekte, die die Klassen und Attribute definieren, die in einer Verzeichnisstruktur vorhanden sein können.
ms.assetid: 688fccf7-37ce-4eea-b4ff-b0b3223a964e
ms.tgt_platform: multiple
keywords:
- Das abstrakte Schema-AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b46e4fefd52e786829e051a14714d2fec118b2ad42cdd95afcaa78b098b0f04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182781"
---
# <a name="the-abstract-schema"></a>Das abstrakte Schema

Der Schemacontainer enthält alle **classSchema-** und **attributeSchema-Objekte,** die die Klassen und Attribute definieren, die in einer Verzeichnisstruktur vorhanden sein können. Der Schemacontainer enthält auch ein Objekt mit dem Namen Aggregate der Klasse **subSchema.** Dieses **subSchema-Objekt** wird als abstraktes Schema bezeichnet.

Das abstrakte Schema enthält eine Teilmenge der Daten, die in den **Objekten classSchema** und **attributeSchema gespeichert** sind. Der Zweck besteht in der Bereitstellung eines einfachen und effizienten Mechanismus zum Abrufen der häufig verwendeten Elemente der Klassen- und Attributdefinitionen. Um beispielsweise die optionalen und obligatorischen Attribute einer Objektklasse abzurufen, binden Sie an mehrere Objekte, um die **Werte mayContain**, **mustContain,** **systemMayContain** und **systemMustContain** aus der Klasse und allen ihren Übergeordneten Klassen sowie aus allen Hilfsklassen der Klasse und ihrer Übergeordneten klassen zu sammeln. Das abstrakte Schema sammelt alle diese Daten bequem in einem einzelnen -Objekt.

Wie bei jedem Objekt in Active Directory Domain Services können Sie eine Bindung an das **subSchema-Objekt** erstellen und dessen Attribute lesen und die Zeichenfolgenwerte so analysen, dass die gewünschten Daten abgerufen werden. ADSI stellt jedoch eine Reihe von Schnittstellen bereit, die das Lesen des abstrakten Schemas erheblich vereinfachen. Weitere Informationen finden Sie unter [Lesen des abstrakten Schemas.](reading-the-abstract-schema.md)

In der folgenden Tabelle sind die wichtigsten Attribute eines **subSchema-Objekts** aufgeführt.



| attribute                 | BESCHREIBUNG                                                                                                                                                                                                                                                                               |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **attributeTypes**        | Ein mehrwertiges Attribut, das Zeichenfolgen enthält, die jedes Attribut im Schema darstellen. Jeder Wert enthält **die AttributeID**, **lDAPDisplayName**, **attributeSyntax**, **rangeLower**, **rangeUpper** und ein Element, das angibt, ob das Attribut mehrere Werte aufweisen kann. |
| **extendedAttributeInfo** | Ein mehrwertiges Attribut, das Zeichenfolgen enthält, die zusätzliche Daten für jedes Attribut darstellen. Jeder Wert enthält **die AttributeID**, **lDAPDisplayName**, **schemaIDGUID** und **attributeSecurityGUID**.                                                                          |
| **extendedClassInfo**     | Ein mehrwertiges Attribut, das Zeichenfolgen enthält, die zusätzliche Daten für jede Klasse darstellen. Jeder Wert enthält die **governsID,** **lDAPDisplayName** und **schemaIDGUID** der -Klasse.                                                                                              |
| **objectClasses**         | Ein mehrwertiges Attribut, das Zeichenfolgen enthält, die jede Klasse im Schema darstellen. Jeder Wert enthält **die governsID,** **lDAPDisplayName**, **mustContain**, **mayContain** und so weiter.                                                                                           |



 

 

 




