---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 35e1ccc2-ffc1-47a6-aba8-5a5cb442e8ae
title: ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2ef6655439718c1038afe2d342910c54db45ba
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106354923"
---
# <a name="parameterref"></a>ParameterRef

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Ein ParameterRef-Element definiert einen Verweis auf ein parameterinit-Element. Ein ScoredProperty-Element, das ein ParameterRef-Element enthält, weist kein explizit festgelegtes Value-Element auf. Stattdessen empfängt das ScoredProperty-Element seinen Wert aus dem parameterinit-Element, auf das von einem ParameterRef-Element verwiesen wird.

## <a name="element-tag"></a>Elementtag

<ParameterRef>

## <a name="xml-attributes"></a>XML-Attribute

In der folgenden Tabelle werden die XML-Attribute aufgelistet, die sich möglicherweise auf dieses Element beziehen.



| XML-Attribut   | Details                                                                                                                        |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Enthält das Name-Attribut des ParameterDef-Elements, auf das innerhalb des Kontexts des aktuellen Dokuments verwiesen wird.<br/> |



 

Weitere Informationen finden Sie im Abschnitt [XML-Attribute](xml-attributes.md) .

## <a name="element-information"></a>Elementinformationen

In der folgenden Tabelle werden die Elemente aufgelistet, die übergeordnete Elemente dieses Elements sein können, die Elemente, die möglicherweise untergeordnete Elemente dieses Elements sind, sowie alle Einschränkungen für das Element selbst.



| Category                   | Details                                                                                           |
|----------------------------|---------------------------------------------------------------------------------------------------|
| Übergeordnete Elemente<br/> | ScoredProperty <br/>                                                                        |
| Untergeordnete Elemente<br/>  | Keine zulässig.<br/>                                                                        |
| Dieses Element<br/>    | Es sind keine Zeichendaten zulässig.<br/> Doppelte untergeordnete gleich geordnete Elemente sind nicht zulässig.<br/> |



 

## <a name="configuration-dependencies"></a>Konfigurations Abhängigkeiten

ParameterRef-Elemente haben möglicherweise keine Konfigurations Abhängigkeiten.

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird veranschaulicht, wie Sie ParameterRef-Elemente verwenden, um Benutzern die Eingabe von benutzerdefinierten Mediengrößen Parametern zu ermöglichen.

``` syntax
<psf:Option name="psk:CustomMediaSize" constrained="psk:None">
  <psf:ScoredProperty name="psk:MediaSizeWidth">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
  </psf:ScoredProperty>
  <psf:ScoredProperty name="psk:MediaSizeHeight">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
  </psf:ScoredProperty>
  <psf:Property name="psk:DisplayName">
    <psf:Value xsi:type="xs:string">Fabrikam User Custom</psf:Value>
  </psf:Property>
</psf:Option>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




