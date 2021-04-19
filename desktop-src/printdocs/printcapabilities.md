---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: f503b62f-02e1-4621-8799-a8b6ad12f489
title: PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10c6dd8ce98b071f1eb239762544a9b72160035
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106355117"
---
# <a name="printcapabilities"></a>PrintCapabilities

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Ein printfunktionen-Element stellt den Stamm des printfunktionalitäten-Dokuments dar. Das Dokument printfunktionen enthält alle Informationen, die zum Beschreiben der unterstützten Geräte Attribute erforderlich sind, wenn eine bestimmte Gerätekonfiguration erforderlich ist.

## <a name="element-tag"></a>Elementtag

<PrintCapabilities>

## <a name="xml-attributes"></a>XML-Attribute

In der folgenden Tabelle werden die XML-Attribute aufgelistet, die sich möglicherweise auf dieses Element beziehen.



| XML-Attribut      | Details                                                                                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| version<br/> | Gibt die Version des Schemas an, das Elementtypen und deren Struktur definiert. Das Versions Attribut ist vom Typ Integer. Die aktuelle Schema Version ist "1". Dieses Attribut ist erforderlich. <br/> |



 

Weitere Informationen finden Sie im Abschnitt [XML-Attribute](xml-attributes.md) .

## <a name="element-information"></a>Elementinformationen

In der folgenden Tabelle werden die Elemente aufgelistet, die übergeordnete Elemente dieses Elements sein können, die Elemente, die möglicherweise untergeordnete Elemente dieses Elements sind, sowie alle Einschränkungen für das Element selbst.



| Category                   | Details                                                                                                           |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| Übergeordnete Elemente<br/> | Nur Dokument Stamm.<br/>                                                                                    |
| Untergeordnete Elemente<br/>  | *Feature* (0 (null) oder mehr)<br/> *ParameterDef* (0 (null) oder mehr)<br/> *Property* (0 (null) oder mehr)<br/> |
| Dieses Element<br/>    | Es sind keine Zeichendaten zulässig.<br/> Doppelte untergeordnete gleich geordnete Elemente sind nicht zulässig.<br/>                 |



 

## <a name="configuration-dependencies"></a>Konfigurations Abhängigkeiten

Das root-Element weist möglicherweise keine Konfigurations Abhängigkeiten auf.

## <a name="example"></a>Beispiel

Weitere Informationen finden Sie unter [Beispiel für printfunktionen](printcapabilities-document-example.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




