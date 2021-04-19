---
description: Die Schlüssel Formatierungs Typen konfigurierbarer Daten können in Textfeldern verwendet werden, um einen Schlüssel in einer Datenbanktabelle bereitzustellen.
ms.assetid: 9f3ce218-1243-4eba-9866-113200fefa30
title: Schlüssel Format Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96687299a57ddebbb90b422ad5311c4bed1db332
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348408"
---
# <a name="key-format-types"></a>Schlüssel Format Typen

Die Schlüssel Formatierungs Typen konfigurierbarer Daten können in Textfeldern verwendet werden, um einen Schlüssel in einer Datenbanktabelle bereitzustellen. Das msmconfigitemnonable-Attribut ist in diesem Datenformat implizit und muss nicht festgelegt werden. NULL ist nie ein gültiger Wert für diesen Typ. Antworten auf alle Schlüssel Formatierungs Elemente müssen das [spezielle cmsm-Format](cmsm-special-format.md)aufweisen.

Die folgenden Schlüssel Format Typen sind vorhanden:

[Verzeichnistyp](directory-type.md)

[Dateityp](file-type.md)

[Eigenschaftentyp](property-type.md)

[Dialog Feld-Typ](dialog-type.md)

[Binary-Typ](binary-type.md)

[Symboltyp](icon-type.md)

Konfigurierbare Elemente des Schlüssel Formattyps werden in Textspalten verwendet, um einen Daten Bank Schlüssel bereitzustellen, und können im Allgemeinen durch eine beliebige Text Zeichenfolge ersetzt werden. Die einzelnen Typen verfügen möglicherweise über zusätzliche syntaktische Einschränkungen, aber diese Einschränkungen werden von Mergemod.dll nicht erzwungen. Bestimmte konfigurierbare Elemente können auch über charakteristische Semantik Einschränkungen verfügen. Beispielsweise kann ein bestimmtes konfigurierbares Element ein Schlüssel in die [binäre Tabelle](binary-table.md) für eine Zeile sein, die ein Bitmapbild enthält. Solche Einschränkungen werden von Mergemod.dll nicht erzwungen. Daher sollten Modul Autoren darauf vorbereitet sein, jede beliebige Zeichenfolge zu verarbeiten, die dem angegebenen Schlüssel Formattyp entspricht. Sofern nicht anderweitig durch die semantische Bedeutung oder Attribute angegeben, ist NULL eine gültige Antwort.

 

 



