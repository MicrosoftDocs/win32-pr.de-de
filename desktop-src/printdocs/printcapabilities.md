---
description: Erfahren Sie mehr über das PrintCapabilities-Element, das den Stamm des PrintCapabilities-Dokuments darstellt.
ms.assetid: f503b62f-02e1-4621-8799-a8b6ad12f489
title: PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2158fd651849df2e4ea24c640065f1041569741a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407023"
---
# <a name="printcapabilities"></a>PrintCapabilities

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Ein PrintCapabilities-Element stellt den Stamm des PrintCapabilities-Dokuments dar. Das PrintCapabilities-Dokument enthält alle Informationen, die zur Beschreibung der unterstützten Geräteattribute bei einer bestimmten Gerätekonfiguration erforderlich sind.

## <a name="element-tag"></a>Elementtag

<PrintCapabilities>

## <a name="xml-attributes"></a>XML-Attribute

In der folgenden Tabelle sind die XML-Attribute aufgeführt, die zu diesem Element gehören können.



| XML-Attribut      | Details                                                                                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| version<br/> | Gibt die Version des Schemas an, das Elementtypen und deren Struktur definiert. Das Versionsattribut ist vom Typ integer. Die aktuelle Schemaversion wird als "1" festgelegt. Dieses Attribut ist erforderlich. <br/> |



 

Weitere Informationen finden Sie im Abschnitt [XML-Attribute.](xml-attributes.md)

## <a name="element-information"></a>Elementinformationen

In der folgenden Tabelle sind die Elemente aufgeführt, die möglicherweise die untergeordneten Elemente dieses Elements sind, sowie alle Einschränkungen für das Element selbst.



| Category                   | Details                                                                                                           |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| Übergeordnete Elemente<br/> | Nur Dokumentstamm.<br/>                                                                                    |
| Untergeordnete Elemente<br/>  | *Feature* (null oder mehr)<br/> *ParameterDef* (null oder mehr)<br/> *Eigenschaft* (null oder mehr)<br/> |
| Dieses Element<br/>    | Es sind keine Zeichendaten zulässig.<br/> Doppelte untergeordnete gleichgeordnete Elemente sind nicht zulässig.<br/>                 |



 

## <a name="configuration-dependencies"></a>Konfigurationsabhängigkeiten

Das Stammelement hat möglicherweise keine Konfigurationsabhängigkeiten.

## <a name="example"></a>Beispiel

Weitere Informationen finden Sie im [PrintCapabilities-Dokumentbeispiel.](printcapabilities-document-example.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




