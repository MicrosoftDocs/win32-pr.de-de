---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: d67518e3-c379-4a50-aeda-31afaa7f05dd
title: Syntax des Druck Schemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2503b3f44ff8b4bdda41f0feefe374c27d78bd41
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106350604"
---
# <a name="syntax-of-the-print-schema"></a>Syntax des Druck Schemas

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Das Druck Schema wird in der XML-Syntax ausgedrückt. Leser werden daher wahrscheinlich mit XML-Syntax und Begriffen wie Element, Elementtag, Element Inhalt, Attribut und Namespace vertraut sein. Das Print Schema-Framework besteht aus einer kleinen Anzahl von Elementtypen. Jeder Elementtyp dient einem bestimmten Zweck in den Technologien, die auf dem Druck Schema basieren.

Element Typen werden durch Ihr XML-Elementtag unterschieden. Das Print Schema-Framework definiert die allgemeine Struktur und Organisation der abhängigen Technologien, indem für jeden Elementtyp angegeben wird, welche Elementtypen als untergeordnete Elemente zulässig sind.

Viele Elementtypen unterscheiden sich von anderen Elementen desselben Typs durch das Name-Attribut, das eine bedeutende Rolle im Schema spielt. Das Name-Attribut dient zum Identifizieren von Instanzen der einzelnen Elementtypen. Die Schlüsselwörter des Druck Schemas definieren einen Satz von Werten für das Name-Attribut für viele der Elementtypen. In den meisten Fällen können Anbieter dem Name-Attribut eigene Werte zuweisen. Sie müssen nur sicherstellen, dass die Werte XML-QNames sind, die mit einem Namespace qualifiziert sind, der für den Anbieter eindeutig ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



