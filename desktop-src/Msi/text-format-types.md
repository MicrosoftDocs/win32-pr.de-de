---
description: Bei den Textformat Typen von konfigurierbaren Daten kann es sich um Text Zeichenfolgen beliebiger Länge handeln. Eingebettete Nullen sind nicht zulässig.
ms.assetid: 71b89f87-43ba-41cd-a969-765d45da4ba4
title: Text Format Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a8f05a0804569667a74c52392d322f3fed2818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363801"
---
# <a name="text-format-types"></a>Text Format Typen

Bei den Textformat Typen von konfigurierbaren Daten kann es sich um Text Zeichenfolgen beliebiger Länge handeln. Eingebettete Nullen sind nicht zulässig.

Die folgenden Text Format Typen sind vorhanden:

[Beliebiger Text](arbitrary-text-type.md)

[RTF](rtf-type.md)

[Großformatige](formatted-type.md)

[Enum](enum-type.md)

[Bezeichnertyp](identifier-type.md)

Konfigurierbare Elemente des Text Format Typs werden in nicht binären Datenbankfeldern verwendet und können im Allgemeinen durch eine beliebige Zeichenfolge beliebiger Länge ersetzt werden. Bestimmte konfigurierbare Elemente haben jedoch auch semantische Einschränkungen. Beispielsweise weist ein konfigurierbares Element, das als Fremdschlüssel für eine bestimmte Tabelle erforderlich ist, zusätzliche Semantik Einschränkungen auf. Solche semantischen Einschränkungen werden von Mergemod.dll nicht erzwungen. Daher sollten Modul Autoren darauf vorbereitet sein, jede beliebige Zeichenfolge zu verarbeiten, die dem angegebenen Text Formattyp entspricht.

 

 



