---
description: Die Kompositions Zeichenfolge ist der aktuelle Text im Zusammenfassungs Fenster.
ms.assetid: ab226567-f68d-4fa4-9ead-e9bfabde927e
title: Kompositions Zeichenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5cb63163ca9a8076edc4d01053e4baeffc619c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959875"
---
# <a name="composition-string"></a>Kompositions Zeichenfolge

Die Kompositions Zeichenfolge ist der aktuelle Text im Zusammenfassungs Fenster. Dies ist der Text, den der IME in abschließende Zeichen konvertiert. Jede Kompositions Zeichenfolge besteht aus einer oder mehreren "Klauseln". Eine-Klausel ist die kleinste Kombination von Zeichen, die von IME in ein endgültiges Zeichen konvertiert werden kann. Um die Kompositions Zeichenfolge zu erhalten und festzulegen, ruft die Anwendung die Funktionen " [**immgetcompositionstring**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) " bzw. " [**immsetcompositionstring**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) " auf.

Wenn der Benutzer Text im Kompositionsfenster eingibt, verfolgt der IME den Status der Kompositions Zeichenfolge. Dieser Status umfasst Attributinformationen, klauselinformationen, Typisierungs Informationen und Cursorposition. Die Anwendung kann den Kompositions Status mithilfe der [**immgetcompositionstring**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) -Funktion abrufen.

Attributinformationen werden in einem Array von 8-Bit-Werten gerendert, das den Status der Zeichen in der Kompositions Zeichenfolge angibt. Alle Zeichen einer-Klausel müssen das gleiche-Attribut aufweisen. Das Array enthält einen Wert für jedes Byte in der Zeichenfolge, einschließlich jeweils einem Byte für die führenden und zweiten Bytes von Doppelbyte Zeichen in der Zeichenfolge. Für jeden Wert im Array können Bits 0 bis 3 eine Kombination der folgenden Werte sein.



| Wert                      | Bedeutung                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| attr- \_ Eingabe                | Das Zeichen, das vom Benutzer eingegeben wird. Der IME muss dieses Zeichen noch konvertieren.                           |
| attr- \_ Eingabe \_ Fehler         | Ein Fehler Zeichen, das vom IME nicht konvertiert werden kann. Der IME kann z. b. einige Konsonanten nicht kombinieren. |
| attr- \_ Ziel \_ konvertiert    | Das Zeichen, das vom Benutzer ausgewählt und dann vom IME konvertiert wurde.                                             |
| konvertiert in attr \_            | Zeichen, das der IME bereits konvertiert hat.                                                             |
| attr- \_ Ziel als \_ notkonvertiert | Das Zeichen, das konvertiert wird. Der Benutzer hat dieses Zeichen ausgewählt, aber es wurde noch nicht von IME konvertiert.     |
| attr \_ fixedkonvertierte       | Zeichen, die vom IME nicht mehr konvertiert werden.                                                           |



 

Alle anderen Werte sind reserviert. In Japanisch handelt es sich bei allen nicht konvertierten Zeichen, die über das Eingabe Attribut "attr" verfügen, \_ um ein Hiragana-, Katakana-oder alphanumerisches Zeichen. In Koreanisch stellt dieses Attribut ein Hangul-Zeichen dar, das der IME noch nicht konvertiert hat. In traditionellem Chinesisch und Chinesisch (vereinfacht) kann jede IME Ihr Zeichen innerhalb eines Bereichs einschränken.

Die im Kompositions Zeichen folgen Status enthaltenen klauselinformationen sind ein Array von 32-Bit-Werten, das die Positionen der Klauseln in der Kompositions Zeichenfolge angibt. Das Array enthält einen Wert für jede Klausel und einen Endwert, der die Länge der vollständigen Zeichenfolge angibt. Jeder Wert im Array gibt den Offset (in Bytes) vom Anfang der Zeichenfolge bis zur-Klausel an. Der erste Wert ist immer 0, da die erste Klausel immer am Anfang der Zeichenfolge beginnt. Wenn eine Zeichenfolge z. b. über zwei Klauseln verfügt, enthält die klauselinformationen drei Werte: der erste Wert ist 0, der zweite Wert der Offset der zweiten Klausel, und der dritte Wert ist die Länge der Zeichenfolge. Bei Unicode wird die Position einer Klausel in Unicode-Zeichen gezählt, und die Länge einer Zeichenfolge entspricht der Größe in Unicode-Zeichen.

Die im Kompositions Zeichen folgen Status enthaltenen Typisierungs Informationen sind eine auf NULL endenden Zeichenfolge, die die Zeichen darstellt, die der Benutzer auf der Tastatur eingibt.

Die Cursorposition, die in den Kompositions Zeichen folgen Status eingeschlossen ist, ist ein Wert, der die Position des Cursors relativ zu den Zeichen in der Kompositions Zeichenfolge angibt. Der Wert ist der Offset (in Bytes) vom Anfang der Zeichenfolge. Wenn dieser Wert 0 ist, befindet sich der Cursor unmittelbar vor dem ersten Zeichen in der Zeichenfolge. Wenn der Wert gleich der Länge der Zeichenfolge ist, liegt der Cursor unmittelbar hinter dem letzten Zeichen. Wenn der Wert 1 ist, ist der Cursor nicht vorhanden. Bei Unicode werden sowohl Position als auch Länge in Unicode-Zeichen gemessen.

Die Anwendung kann die Kompositions Zeichenfolge oder Elemente des Kompositions Status mithilfe der [**immsetcompositionstring**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) -Funktion festlegen. Um sicherzustellen, dass das Kompositionsfenster seine Darstellung anhand dieser Änderungen aktualisiert, ermöglicht die Funktion der Anwendung, eine Benachrichtigungs Meldung an das Fenster zu senden. Anwendungen, die eine Kombination aus Kompositions Status Elementen festlegen, deaktivieren in der Regel Benachrichtigungen für alle außer den letzten Aufrufe dieser Funktion, sodass nur eine Benachrichtigungs Meldung für das Kompositionsfenster generiert wird.

Zum Schluss unterstützt das Bearbeitungs Steuerelement zwei Nachrichten zum Ändern der Verarbeitung von Kompositions Zeichenfolgen durch den IME. Weitere Informationen finden Sie unter [**EM \_ getimestatus**](../controls/em-getimestatus.md) und [**EM- \_ Zeit Status**](../controls/em-setimestatus.md). Weitere Informationen zum Bearbeitungs Steuerelement finden Sie unter [Edit Control](../controls/edit-controls.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen über den Eingabemethoden-Manager](about-input-method-manager.md)
</dt> </dl>

 

 
