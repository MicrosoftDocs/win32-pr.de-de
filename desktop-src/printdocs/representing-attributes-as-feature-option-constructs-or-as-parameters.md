---
description: Stellen Sie Attribute als Feature-/Optionskonstrukte oder als Parameter dar. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 055e502d-631f-49d2-8577-65396373d478
title: Darstellen von Attributen als Feature-/Optionskonstrukte oder als Parameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c93f4de56709ed310a7f0aa259b1dbfd3377ed42
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120055"
---
# <a name="representing-attributes-as-featureoption-constructs-or-as-parameters"></a>Darstellen von Attributen als Feature-/Optionskonstrukte oder als Parameter

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Der Autor eines PrintCapabilities-Dokuments definiert Geräteattribute, aus denen sich die Konfiguration setzt. Im PrintCapabilities-Dokument kann der Autor ein Geräteattribut entweder als Feature-/Optionskonstrukt oder als Parameterkonstrukt darstellen.

Wenn ein Geräteattribut über eine relativ kleine Anzahl möglicher Zustände verfügt, die nicht in ein offensichtliches Muster fallen, ist ein Feature/Option-Konstrukt in der Regel die bessere Wahl. Wenn beispielsweise die zulässigen Werte für das PageMediaSize-Geräteattribut die Werte Letter, Legal, A4ISO,Oid und Envelope10 sind, ist ein Feature/Option-Konstrukt die bessere Wahl für die Darstellung. Aufgrund der Schwierigkeiten und Mehrdeutigkeiten, die mit dem Ausdrücken der zulässigen Werte ohne explizite Enumeration verbunden sind, ist das Parameterkonstrukt für das PageMediaSize-Attribut nicht geeignet.

Wenn ein Geräteattribut durch einen Bereich von ganzen Zahlen dargestellt werden kann, ist die Parameterdarstellung in der Regel die bessere Wahl, insbesondere für Bereiche, die viele Werte enthalten. Wenn das CopyCount-Geräteattribut für ein bestimmtes Druckermodell beispielsweise zwischen 1 und 99.999 liegen kann, sollte dieses Attribut als Parameter kategorisiert werden, indem eine ParameterDef-Instanz definiert wird. Weisen Sie den Standardeigenschafteninstanzen MinValue und MaxValue Werte des ParametersDef-Elements zu, um den Wertebereich für das JobCopyCount-Attribut zu definieren. Aufgrund der großen Anzahl von Werten, die explizit als Option-Elemente aufgeführt werden müssen, ist die Feature-/Optionsdarstellung für das JobCopyCount-Geräteattribut nicht geeignet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



