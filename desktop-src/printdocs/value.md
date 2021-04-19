---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 933528f6-8f34-4509-887c-c7c223c79367
title: Wert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15a8f8c5bf9e2ec1696d6282b859fc99b7701159
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106370353"
---
# <a name="value"></a>Wert

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Ein Value-Element ordnet ein Literale einem Typ zu.

## <a name="element-tag"></a>Elementtag

<Value>

## <a name="xml-attributes"></a>XML-Attribute

In der folgenden Tabelle werden die XML-Attribute aufgelistet, die sich möglicherweise auf dieses Element beziehen.



| XML-Attribut       | Details                                                                                                                                                                          |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| xsi:type<br/> | Gibt den Datentyp des Werts an, bei dem es sich um einen der folgenden XSD-definierten Typen handeln muss: String, Integer, Decimal, QName. Wenn Sie nicht vorhanden ist, ist der Standard Datentyp String.<br/> |



 

Weitere Informationen finden Sie im Abschnitt [XML-Attribute](xml-attributes.md) .

## <a name="element-information"></a>Elementinformationen

In der folgenden Tabelle werden die Elemente aufgelistet, die übergeordnete Elemente dieses Elements sein können, die Elemente, die möglicherweise untergeordnete Elemente dieses Elements sind, sowie alle Einschränkungen für das Element selbst.



| Category                   | Details                                                                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Übergeordnete Elemente<br/> | Parameterinit <br/> Eigenschaft<br/> ScoredProperty<br/>                                                                                   |
| Untergeordnete Elemente<br/>  | Nur Zeichen-oder ganzzahlige Inhalte sind zulässig.<br/>                                                                                                |
| Dieses Element<br/>    | NULL-Inhalt ist zulässig. Der Zeichen Inhalt muss der durch den-Datentyp definierten Syntax entsprechen.<br/> Doppelte untergeordnete gleich geordnete Elemente sind nicht zulässig.<br/> |



 

## <a name="configuration-dependencies"></a>Konfigurations Abhängigkeiten

Werte Elemente, die im ScoredProperty-Element angezeigt werden, verfügen möglicherweise nicht über Konfigurations Abhängigkeiten. Werte Elemente, die innerhalb von Eigenschafts Elementen angezeigt werden, haben möglicherweise beliebige Abhängigkeiten von der Konfiguration.

## <a name="element-usage"></a>Element Verwendung

Ein Value-Element kann in einer Eigenschaft oder einem ScoredProperty-Element vorkommen. Der Zweck des Value-Elements ist die Darstellung eines Werts als Standard-XML-Datentyp. Der-Datentyp wird als XML-Attribut des Value-Elements, xsi: Type, angegeben. Beachten Sie, dass nicht alle XSD-definierten oder XML-definierten Typen unterstützt werden. Eine Liste der unterstützten Typen finden Sie unter [Zusammenfassung der Element Typen](summary-of-element-types.md). Ein Value-Element kann nur Zeichen Inhalte enthalten. In einem Value-Element kann nichts anderes als Inhalt angezeigt werden.

> [!Note]  
> Einige vom Druck Schema definierte Eigenschaft und ScoredProperty-Elemente enthalten kein Value-Element, da ihr Zweck lediglich übergeordnete Elemente von untergeordneten Eigenschaften ist. Sie sollten diesen Eigenschaften nicht ein Value-Element hinzufügen, da diese Eigenschaften nicht ein Value-Element enthalten.

 

Um dem Print Schema-Framework zu entsprechen, das entweder ein Value-Element oder unter Elemente in den Elementen enthalten muss, die-Werte unterstützen, sollte ein fehlender oder nicht definierter Wert durch Darstellung des Value-Elements als leeres Element dargestellt werden. Das heißt, als <Value></Value>.

## <a name="example"></a>Beispiel

Definieren Sie einen Wert vom Typ Decimal, und initialisieren Sie ihn mit "128,5".

``` syntax
<Value xsi:type="decimal">128.5</Value>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




