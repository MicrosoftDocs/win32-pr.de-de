---
description: Erfahren Sie mehr über das ParameterInit-Element, das einen Wert für eine Instanz eines ParameterDef-Elements definiert.
ms.assetid: d5419c40-43e9-49ff-a378-9aeb0757e400
title: ParameterInit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b961ede78b313e7fb3655024705a13f04edb947344493be4fe49ff14b5d00843
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947856"
---
# <a name="parameterinit"></a>ParameterInit

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Definiert einen Wert für eine Instanz eines ParameterDef-Elements. Ein ParameterInit-Element ist das Ziel des Verweises, der von einem ParameterRef-Element vorgenommen wird.

## <a name="element-tag"></a>Elementtag

<ParameterInit>

## <a name="xml-attributes"></a>XML-Attribute

In der folgenden Tabelle sind die XML-Attribute aufgeführt, die für dieses Element gelten können.



| XML-Attribut   | Details                                                                                                                               |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Enthält das Name-Attribut des ParameterDef-Elements, das im Kontext des aktuellen Dokuments initialisiert werden soll.<br/> |



 

Weitere Informationen finden Sie im Abschnitt [XML-Attribute.](xml-attributes.md)

## <a name="element-information"></a>Elementinformationen

In der folgenden Tabelle sind die Elemente aufgeführt, die diesem Element unter Umständen über- oder unteren Elementen liegen, sowie alle Einschränkungen für das Element selbst.



| Kategorie                   | Name oder Einschränkung                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------------|
| Übergeordnete Elemente<br/> | PrintTicket (PrintTicket root)<br/>                                                         |
| Untergeordnete Elemente<br/>  | Wert (eins)<br/>                                                                            |
| Dieses Element<br/>    | Zeichendaten sind nicht zulässig.<br/> Doppelte untergeordnete gleichgeordnete Elemente sind nicht zulässig.<br/> |



 

## <a name="configuration-dependencies"></a>Konfigurationsabhängigkeiten

Keine

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird ein -Parameter mit 1 initialisiert. Im Beispiel in [ParameterDef](parameterdef.md) wird veranschaulicht, wie alle erforderlichen Property-Elemente für diesen Parameter festgelegt werden.

``` syntax
<psf:ParameterInit name="psk:PageCopyCount">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
</psf:ParameterInit>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




