---
description: Abrufen von Informationen zum Option-Element. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: feda78d9-58e7-4668-8a25-40e5fd8ad456
title: Option
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1f02f506c61353698bc4386541ea96dbf858790dd7c34c6d80b8dc2542c46a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098974"
---
# <a name="option"></a>Option

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Ein Option-Element enthält alle Property- und ScoredProperty-Elemente, die dieser Option zugeordnet sind.

## <a name="element-tag"></a>Elementtag

<Option>

## <a name="xml-attributes"></a>XML-Attribute

In der folgenden Tabelle sind die XML-Attribute aufgeführt, die möglicherweise zu diesem Element gehören.



| XML-Attribut          | Details                                                                                                                                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Eingeschränkt<br/> | Dieses Attribut ist für ein PrintCapabilities-Dokument optional.<br/> Dieses Attribut gibt an, ob die Option zur Auswahl oder Verwendung verfügbar ist. Dieses XML-Attribut kann auf einen der folgenden Werte festgelegt werden: None, PrintTicketSettings, AdminSetting oder DeviceSettings. <br/> Siehe [XML-Attribute.](xml-attributes.md)<br/> |
| name<br/>        | Enthält den Namen der Option, entweder eine Standardoption oder eine privat definierte Option. Das XML-Attribut wird auf diese Weise verwendet, um zwischen Option-Instanzen zu unterscheiden. <br/>                                                                                                                                                        |



 

Weitere Informationen finden Sie im Abschnitt [XML-Attribute.](xml-attributes.md)

## <a name="element-information"></a>Elementinformationen

In der folgenden Tabelle sind die Elemente aufgeführt, die möglicherweise die untergeordneten Elemente dieses Elements sind, sowie alle Einschränkungen für das Element selbst.



| Category                   | Details                                                                                                                                                                                                                                                                                          |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Übergeordnete Elemente<br/> | Komponente <br/>                                                                                                                                                                                                                                                                              |
| Untergeordnete Elemente<br/>  | *Eigenschaft* (null oder mehr)<br/> *ScoredProperty* (null oder mehr für Optionen mit dem XML-Attribut 'Name'; mindestens eine für Optionen ohne Verwendung des XML-Attributs 'name' \* )<br/> \* nur öffentliche Optionen, die im Druckschema definiert sind, dürfen kein "name"-Attribut aufweisen, z. B. DocumentNUp)<br/> |
| Dieses Element<br/>    | Es sind keine Zeichendaten zulässig.<br/> Doppelte untergeordnete gleichgeordnete Elemente sind nicht zulässig.<br/>                                                                                                                                                                                                |



 

## <a name="configuration-dependencies"></a>Konfigurationsabhängigkeiten

Ein Optionsdefinitionselement hat möglicherweise keine Konfigurationsabhängigkeiten.

## <a name="element-usage"></a>Elementverwendung

Der Zweck des Option-Elements besteht darin, einen der Zustände zu charakterisieren, die ein Durch ein Feature-Element dargestelltes Gerätekonfigurationsattribut annehmen kann. Jede Option-Elementdefinition enthält mindestens ein ScoredProperty-Element, das ein intrinsisches oder wesentliches Merkmal dieser Option beschreibt. Zur Vereinfachung der Portabilität und Beibehaltung der Absicht definiert das Druckschema viele allgemeine Featureelemente und eine Vielzahl von Optionselementen für jedes Feature. Daher ist es wichtig, nach Möglichkeit ausdrucksschemadefinierte Optionselemente zu verwenden, bevor Sie ihre eigenen Optionsdefinitionen erstellen. Das Verständnis des Prozesses zum Definieren von Optionselementen bietet nützliche Einblicke in die Verwendung des PrintCapabilities-Dokuments und von PrintTickets in der Druckarchitektur von Microsoft .NET Framework Version 3.0 und Windows Vista.

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird ein Name für die Option definiert.

``` syntax
<psf:Option name="psk:PrintFront" />
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




