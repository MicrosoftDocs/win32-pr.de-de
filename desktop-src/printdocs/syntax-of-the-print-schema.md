---
description: Erfahren Sie mehr über die Syntax des Druckschemas, das in XML-Syntax ausgedrückt wird und aus einer kleinen Anzahl von Elementtypen besteht.
ms.assetid: d67518e3-c379-4a50-aeda-31afaa7f05dd
title: Syntax des Druckschemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ef52dbdbdfacc2d3cc947b46558319577a75b1b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405293"
---
# <a name="syntax-of-the-print-schema"></a>Syntax des Druckschemas

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Das Druckschema wird in XML-Syntax ausgedrückt. Daher wird erwartet, dass Leser mit xml-Syntax und Begriffen wie Element, Elementtag, Elementinhalt, Attribut und Namespace vertraut sind. Das Druckschemaframework besteht aus einer kleinen Anzahl von Elementtypen. Jeder Elementtyp erfüllt einen bestimmten Zweck in den Technologien, die auf dem Druckschema aufgebaut sind.

Elementtypen werden durch ihr XML-Elementtag unterschieden. Das Druckschemaframework definiert die Gesamtstruktur und Organisation der abhängigen Technologien, indem für jeden Elementtyp angegeben wird, welche Elementtypen als untergeordnete Elemente zulässig sind.

Viele Elementtypen unterscheiden sich durch das Namensattribut, das eine wichtige Rolle im Schema spielt, von anderen Elementtypen desselben Typs. Das Name-Attribut dient zum Identifizieren von Instanzen der einzelnen Elementtypen. Die Print Schema Keywords definiert einen Satz von Werten für das Name-Attribut für viele der Elementtypen. In den meisten Fällen können Anbieter dem Namensattribut eigene Werte zuweisen. Sie müssen nur sicherstellen, dass die Werte XML QNames sind, die mit einem Namespace qualifiziert sind, der für den Anbieter eindeutig ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



