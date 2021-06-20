---
description: Erfahren Sie mehr über das Value-Element, das einem Typ ein Literal zuteilt. Der Datentyp von Value muss string, integer, decimal oder QName sein.
ms.assetid: 933528f6-8f34-4509-887c-c7c223c79367
title: Wert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 272bee4d7a5f88899f83e439d8e1630b4026713d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405983"
---
# <a name="value"></a>Wert

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Ein Value-Element ordnet einem Typ ein Literal zu.

## <a name="element-tag"></a>Elementtag

<Value>

## <a name="xml-attributes"></a>XML-Attribute

In der folgenden Tabelle sind die XML-Attribute aufgeführt, die für dieses Element gelten können.



| XML-Attribut       | Details                                                                                                                                                                          |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| xsi:type<br/> | Gibt den Datentyp von Value an, bei dem es sich um einen der folgenden XSD-definierten Typen handelt: string, integer, decimal, QName. Wenn der Datentyp fehlt, ist der Standarddatentyp string.<br/> |



 

Weitere Informationen finden Sie im Abschnitt [XML-Attribute.](xml-attributes.md)

## <a name="element-information"></a>Elementinformationen

In der folgenden Tabelle sind die Elemente, die diesem Element unter Umständen über- und unteren Elementen liegen können, die Elemente, die diesem Element unter umständen unter stehen, und alle Einschränkungen für das Element selbst aufgeführt.



| Category                   | Details                                                                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Übergeordnete Elemente<br/> | ParameterInit <br/> Eigenschaft<br/> ScoredProperty<br/>                                                                                   |
| Untergeordnete Elemente<br/>  | Nur Zeichen- oder Ganzzahlinhalte sind zulässig.<br/>                                                                                                |
| Dieses Element<br/>    | NULL-Inhalt ist zulässig. Der Zeicheninhalt muss der vom Datentyp definierten Syntax entsprechen.<br/> Doppelte untergeordnete gleichgeordnete Elemente sind nicht zulässig.<br/> |



 

## <a name="configuration-dependencies"></a>Konfigurationsabhängigkeiten

Wertelemente, die im ScoredProperty-Element angezeigt werden, verfügen möglicherweise nicht über Konfigurationsabhängigkeiten. Wertelemente, die in Property-Elementen angezeigt werden, können beliebige Abhängigkeiten von der Konfiguration aufweisen.

## <a name="element-usage"></a>Elementverwendung

Ein Value-Element kann innerhalb eines Property- oder ScoredProperty-Elements angezeigt werden. Der Zweck des Value-Elements besteht in der Darstellung eines Werts als XML-Standarddatentyp. Der Datentyp wird als XML-Attribut des Value-Elements xsi:type angegeben. Beachten Sie, dass nicht alle XSD-definierten oder XML-definierten Typen unterstützt werden. Eine Liste der unterstützten Typen finden Sie unter [Zusammenfassung der Elementtypen](summary-of-element-types.md). Ein Value-Element kann nur Zeicheninhalte enthalten. Nichts anderes kann als Inhalt in einem Value-Element angezeigt werden.

> [!Note]  
> Einige Vom Druckschema definierte Property- und ScoredProperty-Elemente enthalten kein Value-Element, da ihr Zweck einfach die über- und untergeordneten Eigenschaften sein soll. Sie sollten solchen Eigenschaften wie diesen, Eigenschaften, die kein Value-Element enthalten, kein Value-Element hinzufügen.

 

Um dem Druckschemaframework zu entsprechen, das erfordert, dass entweder ein Value-Element oder Unterelemente in den Elementen vorhanden sind, die Werte unterstützen, sollte ein fehlender oder nicht definierter Wert dargestellt werden, indem das Value-Element als leeres Element dargestellt wird. das heißt, als <Value></Value>.

## <a name="example"></a>Beispiel

Definieren Sie einen Wert vom Typ decimal, und initialisieren Sie ihn mit "128.5".

``` syntax
<Value xsi:type="decimal">128.5</Value>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




