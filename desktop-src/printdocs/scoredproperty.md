---
description: Hier finden Sie Informationen zum ScoredProperty-Element. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 0552d301-5105-490f-962b-135c8c2e936b
title: ScoredProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb600f3fa30c475f7bf28ab1e4c12b19875b6ef49e4f6f3537aead95bf47b999
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033888"
---
# <a name="scoredproperty"></a>ScoredProperty

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Ein ScoredProperty-Element deklariert eine Eigenschaft, die für eine Optionsdefinition intrinsisch ist. Solche Eigenschaften sollten verglichen werden, wenn bewertet wird, wie genau eine angeforderte Option mit einer vom Gerät unterstützten Option abglichen wird.

## <a name="element-tag"></a>Elementtag

<ScoredProperty>

## <a name="xml-attributes"></a>XML-Attribute

In der folgenden Tabelle sind die XML-Attribute aufgeführt, die für dieses Element gelten können.



| XML-Attribut   | Details                                                                                                                 |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Enthält das Namensattribut der ScoredProperty, entweder eine Standardeigenschaft oder eine privat definierte Eigenschaft. <br/> |



 

Weitere Informationen finden Sie im Abschnitt [XML-Attribute.](xml-attributes.md)

## <a name="element-information"></a>Elementinformationen

In der folgenden Tabelle sind die Elemente, die diesem Element unter Umständen über- und unteren Elementen liegen können, die Elemente, die diesem Element unter umständen unter stehen, und alle Einschränkungen für das Element selbst aufgeführt.



| Category                   | Details                                                                                                                                                                  |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Übergeordnete Elemente<br/> | *Option*<br/> *ScoredProperty*<br/>                                                                                                                          |
| Untergeordnete Elemente<br/>  | Sowohl als auch<br/> *ParameterRef* (eins)<br/> oder<br/> *Wert* (eins)<br/> *Eigenschaft* (null oder mehr)<br/> *ScoredProperty* (null oder mehr)<br/> |
| Dieses Element<br/>    | Zeichendaten sind nicht zulässig.<br/> Doppelte untergeordnete gleichgeordnete Elemente sind nicht zulässig.<br/>                                                                        |



 

## <a name="configuration-dependencies"></a>Konfigurationsabhängigkeiten

Ein ScoredProperty-Element hat möglicherweise keine Konfigurationsabhängigkeiten.

## <a name="example"></a>Beispiel

Deklarieren Sie ein ScoredProperty-Element mit dem Namen MediaSizeWidth mit dem Wert 11.

``` syntax
<psf:ScoredProperty name="psk:MediaSizeWidth">
   <psf:Value xsi:type="integer">11</psf:Value>
</psf:ScoredProperty>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




