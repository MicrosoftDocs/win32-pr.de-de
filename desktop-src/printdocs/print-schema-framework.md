---
description: Diese Artikel enthalten ausführlichere Informationen zur Bedeutung und Verwendung der Print Schema-Elementtypen.
ms.assetid: 05c7fd07-1c32-409d-8ca5-820038af3440
title: Druckschemaframework
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 986308ae2ce1308c7df090da295f8b5473efe99219339a906490299ec33b2ea6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718600"
---
# <a name="print-schema-framework"></a>Druckschemaframework

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Dieser Abschnitt enthält ausführlichere Informationen zur Bedeutung und Verwendung der Print Schema-Elementtypen. Der Schwerpunkt der anfänglichen Version des Druckschemaframeworks liegt auf der Darstellung von Konfigurationen und Funktionen von Geräteattributen. Auf hoher Ebene bietet dieses Framework zwei verschiedene Stile zur Beschreibung eines Geräteattributs: als Feature-/Optionskonstrukt oder als Parameterkonstrukt. Wenn ein Geräteattribut über eine kleine Anzahl verfügbarer Werte oder Zustände verfügt, sollte das Attribut als Feature mit den zulässigen Werten oder Zuständen gekennzeichnet werden, die als Optionselemente bezeichnet werden. Wenn ein Geräteattribut dagegen über eine große Anzahl verfügbarer Werte oder Zustände verfügt und der Satz aller möglichen Werte leicht definiert werden kann, ohne auf eine explizite Enumeration zurückzugreifen, sollte das Geräteattribut als Parameter gekennzeichnet werden. (Ein Parameter wird mithilfe eines ParameterDef-Elements definiert, und eine Parameterinstanz wird mithilfe eines ParameterInit-Elements initialisiert.) Eigenschaftselemente werden in Feature-/Options- und Parameterkonstrukten verwendet, um eine differenziertere Unterscheidung zu ermöglichen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



