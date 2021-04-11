---
description: Alle Eigenschaftsnamen müssen diese Einschränkungen einhalten.
ms.assetid: 4447013a-86c4-48a9-bfe1-5e758c799a2f
title: Einschränkungen für Eigenschaftsnamen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c137bc4902bdd62b42e4f3888243a11de43399b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217342"
---
# <a name="restrictions-on-property-names"></a>Einschränkungen für Eigenschaftsnamen

Alle Eigenschaftsnamen müssen diese Einschränkungen einhalten.

-   Ein Eigenschaften Name ist ein [Bezeichner](identifier.md), bei dem es sich um eine Text Zeichenfolge handelt, die mit einem Buchstaben oder einem Unterstrich beginnen muss. Bezeichner und Eigenschaftsnamen dürfen Buchstaben, Ziffern, Unterstriche oder Punkte enthalten. darf jedoch nicht mit einer Ziffer oder einem bestimmten Zeitraum beginnen.
-   [Öffentliche Eigenschafts](public-properties.md) Namen dürfen keine Kleinbuchstaben enthalten.
-   [Private Eigenschafts](private-properties.md) Namen müssen Kleinbuchstaben enthalten.
-   Eigenschaftsnamen mit dem Präfix% stellen System-und Benutzer Umgebungsvariablen dar. Diese werden nie in die [Eigenschaften Tabelle](property-table.md)eingegeben. Die permanenten Einstellungen von Umgebungsvariablen können nur mithilfe der [Umgebungs Tabelle](environment-table.md)geändert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Eigenschaften](using-properties.md)
</dt> </dl>

 

 



