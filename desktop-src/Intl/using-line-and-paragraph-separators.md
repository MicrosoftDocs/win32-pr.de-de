---
description: Ihre Anwendungen sollten das Zeilentrennzeichen (0x2028) und das Absatztrennzeichen (0x2029) verwenden, um Nur-Text zu teilen. Nach jeder Zeilentrennung wird eine neue Zeile begonnen. Nach jedem Absatztrennzeichen wird ein neuer Absatz begonnen.
ms.assetid: 086aca6c-8d1f-4e54-9e1c-642be50b303c
title: Verwenden von Zeilen- und Absatztrennzeichen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 857d7cae4dc7bd720ca94e9780bcb83588650b3df578cd0216e2424c1b28d5af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764630"
---
# <a name="using-line-and-paragraph-separators"></a>Verwenden von Zeilen- und Absatztrennzeichen

Ihre Anwendungen sollten das Zeilentrennzeichen (0x2028) und das Absatztrennzeichen (0x2029) verwenden, um Nur-Text zu teilen. Nach jeder Zeilentrennung wird eine neue Zeile begonnen. Nach jedem Absatztrennzeichen wird ein neuer Absatz begonnen.

Es ist nicht erforderlich, die erste Zeile oder den ersten Absatz in einer Datei mit diesen Zeichen zu starten oder die letzte Zeile oder den letzten Absatz damit zu beenden. Dies bedeutet, dass an dieser Position eine leere Zeile oder ein leerer Absatz vor sich geht.

Die Anwendung kann das Zeilentrennzeichen verwenden, um ein bedingungsloses Zeilenende anzugeben. Zeilentrennzeichen entsprechen jedoch nicht den gesonderten Wagenrücklauf- oder Zeilenvorschubzeichen oder einer Kombination dieser Zeichen. Zeilentrennzeichen müssen getrennt von Wagenrücklauf- und Zeilenvorschubzeichen verarbeitet werden.

Die Anwendung kann ein Absatztrennzeichen zwischen Textab abschnitten einfügen. Die Verwendung dieses Trennzeichens ermöglicht das Erstellen von Nur-Text-Dateien, die mit unterschiedlichen Zeilenhöhen auf verschiedenen Betriebssystemen formatiert werden können. Das Zielsystem kann Zeilentrennzeichen ignorieren und Absätze nur bei den Absatztrennzeichen umbrechen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Sonderzeichen in Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



