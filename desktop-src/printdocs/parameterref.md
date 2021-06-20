---
description: Erfahren Sie mehr über das ParameterRef-Element, das einen Verweis auf ein ParameterInit-Element definiert, und wie es mit ScoredProperty funktioniert.
ms.assetid: 35e1ccc2-ffc1-47a6-aba8-5a5cb442e8ae
title: ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff3b0e16f53e8399a5bbbb5974a05fd6886cdd2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407183"
---
# <a name="parameterref"></a>ParameterRef

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Ein ParameterRef-Element definiert einen Verweis auf ein ParameterInit-Element. Ein ScoredProperty-Element, das ein ParameterRef-Element enthält, verfügt nicht über ein explizit festgelegtes Value-Element. Stattdessen empfängt das ScoredProperty-Element seinen Wert aus dem ParameterInit-Element, auf das ein ParameterRef-Element verweist.

## <a name="element-tag"></a>Elementtag

<ParameterRef>

## <a name="xml-attributes"></a>XML-Attribute

In der folgenden Tabelle sind die XML-Attribute aufgeführt, die für dieses Element gelten können.



| XML-Attribut   | Details                                                                                                                        |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Enthält das Namensattribut des ParameterDef-Elements, auf das im Kontext des aktuellen Dokuments verwiesen wird.<br/> |



 

Weitere Informationen finden Sie im Abschnitt [XML-Attribute.](xml-attributes.md)

## <a name="element-information"></a>Elementinformationen

In der folgenden Tabelle sind die Elemente aufgeführt, die diesem Element unter Umständen über- oder unteren Elementen liegen, sowie alle Einschränkungen für das Element selbst.



| Category                   | Details                                                                                           |
|----------------------------|---------------------------------------------------------------------------------------------------|
| Übergeordnete Elemente<br/> | ScoredProperty <br/>                                                                        |
| Untergeordnete Elemente<br/>  | Keine zulässig.<br/>                                                                        |
| Dieses Element<br/>    | Zeichendaten sind nicht zulässig.<br/> Doppelte untergeordnete gleichgeordnete Elemente sind nicht zulässig.<br/> |



 

## <a name="configuration-dependencies"></a>Konfigurationsabhängigkeiten

ParameterRef-Elemente verfügen möglicherweise nicht über Konfigurationsabhängigkeiten.

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird veranschaulicht, wie ParameterRef-Elemente verwendet werden, um Benutzern die Eingabe benutzerdefinierter Mediengrößenparameter zu ermöglichen.

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

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




