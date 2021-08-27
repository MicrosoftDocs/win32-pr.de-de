---
description: Erfahren Sie mehr über das PrintCapabilities-Element, das den Stamm des PrintCapabilities-Dokuments darstellt.
ms.assetid: f503b62f-02e1-4621-8799-a8b6ad12f489
title: PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef035015e8024954b32d17dd87bab929221ac78
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883925"
---
# <a name="printcapabilities"></a>PrintCapabilities

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Ein PrintCapabilities-Element stellt den Stamm des PrintCapabilities-Dokuments dar. Das PrintCapabilities-Dokument enthält alle Informationen, die erforderlich sind, um die unterstützten Geräteattribute bei einer bestimmten Gerätekonfiguration zu beschreiben.

## <a name="element-tag"></a>Elementtag

&lt;PrintCapabilities&gt;

## <a name="xml-attributes"></a>XML-Attribute

In der folgenden Tabelle sind die XML-Attribute aufgeführt, die für dieses Element gelten können.



| XML-Attribut      | Details                                                                                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| version<br/> | Gibt die Version des Schemas an, das Elementtypen und deren Struktur definiert. Das Versionsattribut ist vom Typ integer. Die aktuelle Schemaversion ist als "1" festgelegt. Dieses Attribut ist erforderlich. <br/> |



 

Weitere Informationen finden Sie im Abschnitt [XML-Attribute.](xml-attributes.md)

## <a name="element-information"></a>Elementinformationen

In der folgenden Tabelle sind die Elemente, die diesem Element unter Umständen über- und unteren Elementen liegen können, die Elemente, die diesem Element unter umständen unter stehen, und alle Einschränkungen für das Element selbst aufgeführt.



| Category                   | Details                                                                                                           |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| Übergeordnete Elemente<br/> | Nur Dokumentstamm.<br/>                                                                                    |
| Untergeordnete Elemente<br/>  | *Feature* (null oder mehr)<br/> *ParameterDef* (null oder mehr)<br/> *Eigenschaft* (null oder mehr)<br/> |
| Dieses Element<br/>    | Zeichendaten sind nicht zulässig.<br/> Doppelte untergeordnete gleichgeordnete Elemente sind nicht zulässig.<br/>                 |



 

## <a name="configuration-dependencies"></a>Konfigurationsabhängigkeiten

Das Stammelement hat möglicherweise keine Konfigurationsabhängigkeiten.

## <a name="example"></a>Beispiel

Weitere Informationen finden Sie unter PrintCapabilities Document Example (Beispiel [für ein PrintCapabilities-Dokument).](printcapabilities-document-example.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




