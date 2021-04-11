---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 055e502d-631f-49d2-8577-65396373d478
title: Darstellen von Attributen als Feature/Options-Konstrukte oder als Parameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2c24843a175337f40a84dcdacc41e1a2ab1e15e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104050730"
---
# <a name="representing-attributes-as-featureoption-constructs-or-as-parameters"></a>Darstellen von Attributen als Feature/Options-Konstrukte oder als Parameter

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Der Autor eines printfunktionalitäten-Dokuments definiert Geräte Attribute, die die Konfiguration bilden. Im printfunktionalitäten-Dokument kann der Autor ein Geräte Attribut entweder als Funktions-/optionskonstrukt oder als Parameter Konstrukt darstellen.

Wenn ein Geräte Attribut über eine relativ kleine Anzahl möglicher Zustände verfügt, die nicht in irgendeiner Art von offensichtlichem Muster vorkommen, ist ein Funktions-/optionskonstrukt normalerweise die bessere Wahl. Wenn z. b. die zulässigen Werte für das PageMediaSize-Geräte Attribut die Werte Letter, Legal, A4ISO, Boulevard und Envelope10 sind, wäre ein Funktions-/optionskonstrukt die bessere Wahl für die Darstellung. Aufgrund der Schwierigkeit und Mehrdeutigkeit im Zusammenhang mit dem Ausdrücken der zulässigen Werte ohne explizite Enumeration ist das Parameter Konstrukt für das PageMediaSize-Attribut nicht geeignet.

Wenn ein Geräte Attribut durch einen Bereich von ganzen Zahlen dargestellt werden kann, ist die Parameter Darstellung normalerweise die bessere Wahl, insbesondere für Bereiche, die viele Werte enthalten. Wenn das CopyCount-Geräte Attribut für ein bestimmtes Drucker Modell z. b. zwischen 1 und 99.999 liegen kann, sollte dieses Attribut als Parameter kategorisiert werden, indem eine ParameterDef-Instanz definiert wird. Weisen Sie den MinValue-und MaxValue-Standard Eigenschafts Instanzen des ParameterDef-Elements Werte zu, um den Wertebereich für das jobcopycount-Attribut zu definieren. Aufgrund der großen Anzahl von Werten, die explizit als Options Elemente aufgeführt werden müssen, eignet sich die Funktions-/Options-Darstellung nicht für das jobcopycount-Geräte Attribut.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



