---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: feda78d9-58e7-4668-8a25-40e5fd8ad456
title: Option
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 379834d12cd01847c95783d727be5dcdc6c575bf
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106354293"
---
# <a name="option"></a>Option

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Ein Option-Element enthält alle Eigenschaften-und ScoredProperty-Elemente, die dieser Option zugeordnet sind.

## <a name="element-tag"></a>Elementtag

<Option>

## <a name="xml-attributes"></a>XML-Attribute

In der folgenden Tabelle werden die XML-Attribute aufgelistet, die sich möglicherweise auf dieses Element beziehen.



| XML-Attribut          | Details                                                                                                                                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| schwierige<br/> | Dieses Attribut ist für ein printfunktionalitäten-Dokument optional.<br/> Dieses Attribut gibt an, ob die Option zur Auswahl oder Verwendung verfügbar ist. Dieses XML-Attribut kann auf einen der folgenden Werte festgelegt werden: None, printticketsettings, adminsetting oder devicesettings. <br/> Siehe [XML-Attribute](xml-attributes.md)<br/> |
| name<br/>        | Enthält den Namen der Option, entweder eine Standardoption oder eine privat definierte Option. Das XML-Attribut wird auf diese Weise verwendet, um zwischen Options Instanzen zu unterscheiden. <br/>                                                                                                                                                        |



 

Weitere Informationen finden Sie im Abschnitt [XML-Attribute](xml-attributes.md) .

## <a name="element-information"></a>Elementinformationen

In der folgenden Tabelle werden die Elemente aufgelistet, die übergeordnete Elemente dieses Elements sein können, die Elemente, die möglicherweise untergeordnete Elemente dieses Elements sind, sowie alle Einschränkungen für das Element selbst.



| Category                   | Details                                                                                                                                                                                                                                                                                          |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Übergeordnete Elemente<br/> | Funktion <br/>                                                                                                                                                                                                                                                                              |
| Untergeordnete Elemente<br/>  | *Property* (0 (null) oder mehr)<br/> *ScoredProperty* (0 (null) oder mehr für Optionen mit dem XML-Attribut ' Name '; mindestens eine for-Option, die das XML-Attribut ' Name ' nicht nutzt \* )<br/> \* nur öffentliche Optionen, die im Druck Schema definiert sind, dürfen kein "Name"-Attribut haben, z. b. "DocumentNUp"<br/> |
| Dieses Element<br/>    | Es sind keine Zeichendaten zulässig.<br/> Doppelte untergeordnete gleich geordnete Elemente sind nicht zulässig.<br/>                                                                                                                                                                                                |



 

## <a name="configuration-dependencies"></a>Konfigurations Abhängigkeiten

Ein Options Definitions Element weist möglicherweise keine Konfigurations Abhängigkeiten auf.

## <a name="element-usage"></a>Element Verwendung

Der Zweck des Option-Elements besteht darin, einen der Zustände zu bezeichnen, die von einem Geräte Konfigurations Attribut, das von einem Feature-Element dargestellt wird, angenommen werden kann. Jede Options Element Definition enthält ein oder mehrere ScoredProperty-Elemente, die eine intrinsische oder wesentliche Eigenschaft dieser Option beschreiben. Um die Portabilität und die Beibehaltung der Absicht zu vereinfachen, definiert das Druck Schema viele gängige Funktionselemente und eine Vielzahl von Options Elementen für jede Funktion. Daher ist es wichtig, dass Sie, wenn überhaupt möglich, Schema definierte Options Elemente verwenden, bevor Sie eigene Options Definitionen erstellen. Das Verständnis des Prozesses zum Definieren von Options Elementen bietet nützliche Einblicke in die Art und Weise, in der die Printworks-Dokumente und-PrintTickets in der Microsoft .NET Framework-Version 3,0 und Windows Vista-Druck Architektur verwendet werden.

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird ein Name für die Option definiert.

``` syntax
<psf:Option name="psk:PrintFront" />
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




