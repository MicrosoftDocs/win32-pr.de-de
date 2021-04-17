---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: d5419c40-43e9-49ff-a378-9aeb0757e400
title: Parameterinit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16cb985e746b400b1c804f21b5996352ae590e3b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104219061"
---
# <a name="parameterinit"></a>Parameterinit

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Definiert einen Wert für eine Instanz eines ParameterDef-Elements. Ein parameterinit-Element ist das Ziel des Verweises, das von einem ParameterRef-Element erstellt wird.

## <a name="element-tag"></a>Elementtag

<ParameterInit>

## <a name="xml-attributes"></a>XML-Attribute

In der folgenden Tabelle werden die XML-Attribute aufgelistet, die sich möglicherweise auf dieses Element beziehen.



| XML-Attribut   | Details                                                                                                                               |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Enthält das Name-Attribut des ParameterDef-Elements, das innerhalb des Kontexts des aktuellen Dokuments initialisiert werden soll.<br/> |



 

Weitere Informationen finden Sie im Abschnitt [XML-Attribute](xml-attributes.md) .

## <a name="element-information"></a>Elementinformationen

In der folgenden Tabelle werden die Elemente aufgelistet, die übergeordnete Elemente dieses Elements sein können, die Elemente, die möglicherweise untergeordnete Elemente dieses Elements sind, sowie alle Einschränkungen für das Element selbst.



| Category                   |                                                                                                   |
|----------------------------|---------------------------------------------------------------------------------------------------|
| Übergeordnete Elemente<br/> | Print Ticket (Print Ticket-Stamm)<br/>                                                         |
| Untergeordnete Elemente<br/>  | Wert (eins)<br/>                                                                            |
| Dieses Element<br/>    | Es sind keine Zeichendaten zulässig.<br/> Doppelte untergeordnete gleich geordnete Elemente sind nicht zulässig.<br/> |



 

## <a name="configuration-dependencies"></a>Konfigurations Abhängigkeiten

Keine

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird ein-Parameter auf 1 initialisiert. Das Beispiel in [ParameterDef](parameterdef.md) veranschaulicht, wie alle erforderlichen Eigenschaften Elemente für diesen Parameter festgelegt werden.

``` syntax
<psf:ParameterInit name="psk:PageCopyCount">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
</psf:ParameterInit>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




