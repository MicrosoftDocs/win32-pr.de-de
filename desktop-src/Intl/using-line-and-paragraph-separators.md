---
description: Ihre Anwendungen sollten das Zeilen Trennzeichen (0x2028) und das Absatz Trennzeichen (0x2029) verwenden, um nur-Text aufzuteilen. Nach jeder Zeilentrennung wird eine neue Zeile begonnen. Nach jedem Absatztrennzeichen wird ein neuer Absatz begonnen.
ms.assetid: 086aca6c-8d1f-4e54-9e1c-642be50b303c
title: Verwenden von Zeilen-und Absatz Trennzeichen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c9511ba2a8889b3c9139daf1d088d91ed746db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218690"
---
# <a name="using-line-and-paragraph-separators"></a>Verwenden von Zeilen-und Absatz Trennzeichen

Ihre Anwendungen sollten das Zeilen Trennzeichen (0x2028) und das Absatz Trennzeichen (0x2029) verwenden, um nur-Text aufzuteilen. Nach jeder Zeilentrennung wird eine neue Zeile begonnen. Nach jedem Absatztrennzeichen wird ein neuer Absatz begonnen.

Es ist nicht erforderlich, die erste Zeile oder den Absatz in einer Datei mit diesen Zeichen zu starten oder die letzte Zeile bzw. den letzten Absatz mit Ihnen zu beenden. Dies deutet darauf hin, dass es eine leere Zeile oder einen leeren Absatz an diesem Speicherort gibt.

Die Anwendung kann das Zeilen Trennzeichen verwenden, um ein unbedingtes Zeilenende anzugeben. Zeilentrennzeichen entsprechen jedoch nicht den gesonderten Wagenrücklauf- oder Zeilenvorschubzeichen oder einer Kombination dieser Zeichen. Zeilentrennzeichen müssen getrennt von Wagenrücklauf- und Zeilenvorschubzeichen verarbeitet werden.

Die Anwendung kann ein Absatz Trennzeichen zwischen Text Absätzen einfügen. Die Verwendung dieses Trennzeichens ermöglicht das Erstellen von Nur-Text-Dateien, die mit unterschiedlichen Zeilenhöhen auf verschiedenen Betriebssystemen formatiert werden können. Das Zielsystem kann Zeilentrennzeichen ignorieren und Absätze nur bei den Absatztrennzeichen umbrechen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Sonderzeichen in Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



