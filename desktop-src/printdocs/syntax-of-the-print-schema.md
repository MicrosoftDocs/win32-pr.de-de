---
description: Erfahren Sie mehr über die Syntax des Druckschemas, das in XML-Syntax ausgedrückt wird und aus einer kleinen Anzahl von Elementtypen besteht.
ms.assetid: d67518e3-c379-4a50-aeda-31afaa7f05dd
title: Syntax des Druckschemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a55fbae9b74fe9537430c926870e422cb1a9cd0e025d4aedf702865a8822c740
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662370"
---
# <a name="syntax-of-the-print-schema"></a>Syntax des Druckschemas

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Das Druckschema wird in XML-Syntax ausgedrückt. Leser sollten daher mit der XML-Syntax und Begriffen wie Element, Elementtag, Elementinhalt, Attribut und Namespace vertraut sein. Das Druckschemaframework besteht aus einer kleinen Anzahl von Elementtypen. Jeder Elementtyp erfüllt einen bestimmten Zweck in den Technologien, die auf dem Druckschema basieren.

Elementtypen werden durch ihr XML-Elementtag unterschieden. Das Druckschemaframework definiert die Gesamtstruktur und Organisation der abhängigen Technologien, indem für jeden Elementtyp angegeben wird, welche Elementtypen als untergeordnete Elemente zulässig sind.

Viele Elementtypen unterscheiden sich von anderen Typen desselben Typs durch das Namensattribut, das eine wichtige Rolle im Schema spielt. Das Name-Attribut dient zum Identifizieren von Instanzen jedes Elementtyps. Die Druckschemaschlüsselwörter definieren einen Satz von Werten für das Name-Attribut für viele der Elementtypen. In den meisten Fällen können Anbieter dem Name-Attribut eigene Werte zuweisen. Sie müssen nur sicherstellen, dass es sich bei den Werten um XML-QNames handelt, die mit einem Namespace qualifiziert sind, der für den Anbieter eindeutig ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



