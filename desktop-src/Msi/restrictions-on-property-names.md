---
description: Alle Eigenschaftennamen müssen diesen Einschränkungen unterliegen.
ms.assetid: 4447013a-86c4-48a9-bfe1-5e758c799a2f
title: Einschränkungen für Eigenschaftsnamen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461039f62cbbd820b6ccc132551406944457784da2d4d8093a2235f5caf79104
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979270"
---
# <a name="restrictions-on-property-names"></a>Einschränkungen für Eigenschaftsnamen

Alle Eigenschaftennamen müssen diesen Einschränkungen unterliegen.

-   Ein Eigenschaftenname ist ein [Bezeichner,](identifier.md)bei dem es sich um eine Textzeichenfolge handelt, die entweder mit einem Buchstaben oder einem Unterstrich beginnen muss. Bezeichner und Eigenschaftsnamen können Buchstaben, Ziffern, Unterstriche oder Zeiträume enthalten. kann jedoch nicht mit einer Zahl oder einem Zeitraum beginnen.
-   [Öffentliche Eigenschaftsnamen](public-properties.md) dürfen keine Kleinbuchstaben enthalten.
-   [Private Eigenschaftsnamen](private-properties.md) müssen Kleinbuchstaben enthalten.
-   Eigenschaftsnamen mit dem Präfix % stellen System- und Benutzerumgebungsvariablen dar. Diese werden nie in die [Property-Tabelle eingegeben.](property-table.md) Die permanenten Einstellungen von Umgebungsvariablen können nur mithilfe der [Umgebungstabelle geändert werden.](environment-table.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Eigenschaften](using-properties.md)
</dt> </dl>

 

 



