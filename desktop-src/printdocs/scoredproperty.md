---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 0552d301-5105-490f-962b-135c8c2e936b
title: ScoredProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1605d173e0ab311841a6fcc37a46a0ba3b59b005
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106353280"
---
# <a name="scoredproperty"></a>ScoredProperty

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Ein ScoredProperty-Element deklariert eine Eigenschaft, die in einer Options Definition intrinsisch ist. Diese Eigenschaften sollten verglichen werden, wenn ausgewertet wird, wie eng eine angeforderte Option mit einer Geräte gestützten Option übereinstimmt.

## <a name="element-tag"></a>Elementtag

<ScoredProperty>

## <a name="xml-attributes"></a>XML-Attribute

In der folgenden Tabelle werden die XML-Attribute aufgelistet, die sich möglicherweise auf dieses Element beziehen.



| XML-Attribut   | Details                                                                                                                 |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Enthält das Name-Attribut der ScoredProperty, entweder eine Standard Eigenschaft oder eine privat definierte Eigenschaft. <br/> |



 

Weitere Informationen finden Sie im Abschnitt [XML-Attribute](xml-attributes.md) .

## <a name="element-information"></a>Elementinformationen

In der folgenden Tabelle werden die Elemente aufgelistet, die übergeordnete Elemente dieses Elements sein können, die Elemente, die möglicherweise untergeordnete Elemente dieses Elements sind, sowie alle Einschränkungen für das Element selbst.



| Category                   | Details                                                                                                                                                                  |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Übergeordnete Elemente<br/> | *Option*<br/> *ScoredProperty*<br/>                                                                                                                          |
| Untergeordnete Elemente<br/>  | Sowohl als auch<br/> *ParameterRef* (eins)<br/> oder<br/> *Wert* (eins)<br/> *Property* (0 (null) oder mehr)<br/> *ScoredProperty* (0 (null) oder mehr)<br/> |
| Dieses Element<br/>    | Es sind keine Zeichendaten zulässig.<br/> Doppelte untergeordnete gleich geordnete Elemente sind nicht zulässig.<br/>                                                                        |



 

## <a name="configuration-dependencies"></a>Konfigurations Abhängigkeiten

Ein ScoredProperty-Element weist möglicherweise keine Konfigurations Abhängigkeiten auf.

## <a name="example"></a>Beispiel

Deklarieren Sie ein ScoredProperty-Element mit dem Namen mediasizewidth mit dem Wert 11.

``` syntax
<psf:ScoredProperty name="psk:MediaSizeWidth">
   <psf:Value xsi:type="integer">11</psf:Value>
</psf:ScoredProperty>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




