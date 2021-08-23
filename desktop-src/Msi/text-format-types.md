---
description: Die Textformattypen konfigurierbarer Daten können Textzeichenfolgen beliebiger Länge sein. Eingebettete NULL-Werte sind nicht zulässig.
ms.assetid: 71b89f87-43ba-41cd-a969-765d45da4ba4
title: Textformattypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a77ef5e6948320deba8df992e2cf9447cbda82d6a20fc4329f97e761f425164
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626330"
---
# <a name="text-format-types"></a>Textformattypen

Die Textformattypen konfigurierbarer Daten können Textzeichenfolgen beliebiger Länge sein. Eingebettete NULL-Werte sind nicht zulässig.

Die folgenden Textformattypen sind vorhanden:

[Beliebiger Text](arbitrary-text-type.md)

[RTF](rtf-type.md)

[Formatiert](formatted-type.md)

[Enum](enum-type.md)

[Bezeichnertyp](identifier-type.md)

Konfigurierbare Elemente des Textformattyps werden in nicht binären Datenbankfeldern verwendet und können im Allgemeinen durch eine beliebige Zeichenfolge beliebiger Länge ersetzt werden. Bestimmte konfigurierbare Elemente weisen jedoch auch semantische Einschränkungen auf. Beispielsweise weist ein konfigurierbares Element, das als Fremdschlüssel in einer bestimmten Tabelle erforderlich ist, zusätzliche semantische Einschränkungen auf. Solche semantischen Einschränkungen werden von Mergemod.dll nicht erzwungen. Daher sollten Modulautoren darauf vorbereitet sein, alle Zeichenfolgen zu verarbeiten, die den angegebenen Textformattyp erfüllen.

 

 



