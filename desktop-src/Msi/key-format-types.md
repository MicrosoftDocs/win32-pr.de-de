---
description: Die Schlüsselformattypen konfigurierbarer Daten können in Textfeldern verwendet werden, um einen Schlüssel in einer Datenbanktabelle bereitzustellen.
ms.assetid: 9f3ce218-1243-4eba-9866-113200fefa30
title: Schlüsselformattypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a22c4149ec89bd9a1745c28fe17cdafcbcfeaee827dcb35bd8c6badbf2acfb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692490"
---
# <a name="key-format-types"></a>Schlüsselformattypen

Die Schlüsselformattypen konfigurierbarer Daten können in Textfeldern verwendet werden, um einen Schlüssel in einer Datenbanktabelle bereitzustellen. Das msmConfigItemNonNullable-Attribut ist in diesem Datenformat implizit und muss nicht festgelegt werden. NULL ist nie ein gültiger Wert für diesen Typ. Antworten auf alle Schlüsselformatelemente müssen im [CMSM-Sonderformat vorliegen.](cmsm-special-format.md)

Die folgenden Schlüsselformattypen sind vorhanden:

[Verzeichnistyp](directory-type.md)

[Dateityp](file-type.md)

[Eigenschaftentyp](property-type.md)

[Dialogtyp](dialog-type.md)

[Binärtyp](binary-type.md)

[Symboltyp](icon-type.md)

Konfigurierbare Elemente des Schlüsselformattyps werden in Textspalten verwendet, um einen Datenbankschlüssel bereitzustellen, und können im Allgemeinen durch eine beliebige Textzeichenfolge ersetzt werden. Die einzelnen Typen können zusätzliche syntaktische Einschränkungen aufweisen, diese Einschränkungen werden jedoch nicht von Mergemod.dll erzwungen. Bestimmte konfigurierbare Elemente können auch typischen semantischen Einschränkungen unterliegen. Beispielsweise kann ein bestimmtes konfigurierbares Element erforderlich sein, um ein Schlüssel in der [Binärtabelle](binary-table.md) für eine Zeile zu sein, die ein Bitmapbild enthält. Solche Einschränkungen werden von Mergemod.dll nicht erzwungen. Daher sollten Modulautoren darauf vorbereitet sein, Zeichenfolgen zu verarbeiten, die dem angegebenen Schlüsselformattyp entsprechen. Sofern nicht durch semantische Bedeutung oder Attribute anders angegeben, ist NULL eine gültige Antwort.

 

 



