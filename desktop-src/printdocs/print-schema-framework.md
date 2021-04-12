---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 05c7fd07-1c32-409d-8ca5-820038af3440
title: Print Schema Framework
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 617f747b950676f2359645684c9e672fb5c87ee3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104219042"
---
# <a name="print-schema-framework"></a>Print Schema Framework

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

In diesem Abschnitt finden Sie ausführlichere Informationen zur Bedeutung und Verwendung der Druckschema-Elementtypen. Der Hauptschwerpunkt der ersten Version des Druck Schema-Frameworks ist das darstellen von Konfigurationen und Funktionen von Geräte Attributen. Im großen Umfang bietet dieses Framework zwei unterschiedliche Arten der Beschreibung eines Geräte Attributs: als Funktions-/optionskonstrukt oder als Parameter Konstrukt. Wenn ein Geräte Attribut über eine geringe Anzahl verfügbarer Werte oder Zustände verfügt, sollte das Attribut als Feature mit den zulässigen Werten oder Zuständen gekennzeichnet werden, die als Options Elemente bezeichnet werden. Wenn dagegen ein Geräte Attribut über eine große Anzahl verfügbarer Werte oder Zustände verfügt und der Satz aller möglichen Werte leicht definiert werden kann, ohne auf eine explizite Enumeration zurückgreifen zu müssen, sollte das Geräte Attribut als Parameter charakterisiert werden. (Ein Parameter wird mithilfe eines ParameterDef-Elements definiert, und eine Parameter Instanz wird mithilfe eines parameterinit-Elements initialisiert.) Eigenschafts Elemente werden innerhalb von Feature/Option und parameterkonstrukten verwendet, um eine feinere Differenzierungs Ebene bereitzustellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



