---
title: Das abstrakte Schema
description: Der Schema Container enthält alle classSchema-und attributeSchema-Objekte, die die Klassen und Attribute definieren, die in einer Verzeichnis Gesamtstruktur vorhanden sein können.
ms.assetid: 688fccf7-37ce-4eea-b4ff-b0b3223a964e
ms.tgt_platform: multiple
keywords:
- Das abstrakte Schema AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9123c72cc4cc38eafa77e0ad0c6384940667e54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036336"
---
# <a name="the-abstract-schema"></a>Das abstrakte Schema

Der Schema Container enthält alle **classSchema** -und **attributeSchema** -Objekte, die die Klassen und Attribute definieren, die in einer Verzeichnis Gesamtstruktur vorhanden sein können. Der Schema Container enthält auch ein Objekt mit dem Namen Aggregate of Class **subschema**. Dieses **unter Schema** Objekt wird als abstraktes Schema bezeichnet.

Das abstrakte Schema enthält eine Teilmenge der Daten, die in den **classSchema** -und **attributeSchema** -Objekten gespeichert sind. Der Zweck besteht darin, einen einfachen und effizienten Mechanismus zum Abrufen der häufig verwendeten Elemente der Klassen-und Attribut Definitionen bereitzustellen. Wenn Sie z. b. die optionalen und obligatorischen Attribute einer Objektklasse abrufen möchten, binden Sie an mehrere Objekte, um die Werte " **mayare**", " **mustare**", " **systemmayare**" und " **systemmustare** " aus der Klasse und allen zugehörigen übergeordneten Klassen sowie aus beliebigen Hilfsklassen der Klasse und ihren übergeordneten Klassen zu sammeln. Das abstrakte Schema sammelt alle diese Daten bequem in einem einzelnen-Objekt.

Wie bei jedem Objekt in Active Directory Domain Services können Sie eine Bindung an das **unter Schema** Objekt und dessen Attribute lesen und die Zeichen folgen Werte zum Abrufen der gewünschten Daten auswerten. ADSI bietet jedoch eine Reihe von Schnittstellen, die das Lesen des abstrakten Schemas erheblich vereinfachen. Weitere Informationen finden Sie unter [Lesen des abstrakten Schemas](reading-the-abstract-schema.md).

In der folgenden Tabelle sind die Schlüssel Attribute eines **unter Schema** Objekts aufgeführt.



| Attribut                 | BESCHREIBUNG                                                                                                                                                                                                                                                                               |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **attributetypes**        | Ein mehr wertiges Attribut, das Zeichen folgen enthält, die die einzelnen Attribute im Schema darstellen. Jeder Wert enthält die **Attribute "AttributeID**", " **ldapDisplayName**", " **attributeSyntax**", " **rangeLower**", " **rangeUpper**" und ein Element, das angibt, ob das Attribut mehrere Werte aufweisen kann. |
| **extendedattributeinfo** | Ein mehr wertiges Attribut, das Zeichen folgen enthält, die zusätzliche Daten für jedes Attribut darstellen. Jeder Wert enthält die **Attribute "AttributeID**", " **ldapDisplayName**", " **schemaIdGUID**" und " **attributeSecurityGuid**".                                                                          |
| **extendedclassinfo**     | Ein mehr wertiges Attribut, das Zeichen folgen enthält, die zusätzliche Daten für jede Klasse darstellen. Jeder Wert enthält die **governsId**, den **ldapDisplayName** und die **schemaIdGUID** der Klasse.                                                                                              |
| **ObjectClasses**         | Ein mehr wertiges Attribut, das Zeichen folgen enthält, die jede Klasse im Schema darstellen. Jeder Wert enthält die **governsId**, den **ldapDisplayName**, **mustare**, **mayare** und so weiter.                                                                                           |



 

 

 




