---
description: Erfahren Sie mehr über das ParameterInit-Element, das einen Wert für eine Instanz eines ParameterDef-Elements definiert.
ms.assetid: d5419c40-43e9-49ff-a378-9aeb0757e400
title: ParameterInit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0e0cadbf26d6ff516ab0ace90165e11420a9b7
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118975"
---
# <a name="parameterinit"></a>ParameterInit

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Definiert einen Wert für eine Instanz eines ParameterDef-Elements. Ein ParameterInit-Element ist das Ziel des Verweises, der von einem ParameterRef-Element erstellt wird.

## <a name="element-tag"></a>Elementtag

<ParameterInit>

## <a name="xml-attributes"></a>XML-Attribute

In der folgenden Tabelle sind die XML-Attribute aufgeführt, die möglicherweise zu diesem Element gehören.



| XML-Attribut   | Details                                                                                                                               |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Enthält das Name-Attribut des ParameterDef-Elements, das im Kontext des aktuellen Dokuments initialisiert werden soll.<br/> |



 

Weitere Informationen finden Sie im Abschnitt [XML-Attribute.](xml-attributes.md)

## <a name="element-information"></a>Elementinformationen

In der folgenden Tabelle sind die Elemente aufgeführt, die möglicherweise die untergeordneten Elemente dieses Elements sind, sowie alle Einschränkungen für das Element selbst.



| Kategorie                   | Name oder Einschränkung                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------------|
| Übergeordnete Elemente<br/> | PrintTicket (PrintTicket-Stamm)<br/>                                                         |
| Untergeordnete Elemente<br/>  | Wert (eins)<br/>                                                                            |
| Dieses Element<br/>    | Es sind keine Zeichendaten zulässig.<br/> Doppelte untergeordnete gleichgeordnete Elemente sind nicht zulässig.<br/> |



 

## <a name="configuration-dependencies"></a>Konfigurationsabhängigkeiten

Keine

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird ein Parameter mit 1 initialisiert. Das Beispiel in [ParameterDef](parameterdef.md) veranschaulicht, wie alle erforderlichen Property-Elemente für diesen Parameter festgelegt werden.

``` syntax
<psf:ParameterInit name="psk:PageCopyCount">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
</psf:ParameterInit>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




