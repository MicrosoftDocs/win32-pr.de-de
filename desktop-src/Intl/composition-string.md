---
description: Die Kompositionszeichenfolge ist der aktuelle Text im Kompositionsfenster.
ms.assetid: ab226567-f68d-4fa4-9ead-e9bfabde927e
title: Kompositionszeichenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05a547b4383c95b99025b779de2950c8325af56a3397603db10199474dfe20ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430990"
---
# <a name="composition-string"></a>Kompositionszeichenfolge

Die Kompositionszeichenfolge ist der aktuelle Text im Kompositionsfenster. Dies ist der Text, den die IME in endgültige Zeichen konvertiert. Jede Kompositionszeichenfolge besteht aus einer oder mehreren "Klauseln". Eine -Klausel ist die kleinste Kombination von Zeichen, die der IME in ein endgültiges Zeichen konvertieren kann. Um die Kompositionszeichenfolge abzurufen und festzulegen, ruft die Anwendung die Funktionen [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) bzw. [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) auf.

Wenn der Benutzer Text in das Kompositionsfenster eingibt, verfolgt der IME den Status der Kompositionszeichenfolge nach. Dieser Status umfasst Attributinformationen, Klauselinformationen, Eingabeinformationen und Cursorposition. Die Anwendung kann den Kompositionsstatus mithilfe der [**ImmGetCompositionString-Funktion**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) abrufen.

Attributinformationen werden in einem Array von 8-Bit-Werten gerendert, das den Status von Zeichen in der Kompositionszeichenfolge angibt. Alle Zeichen einer Klausel müssen das gleiche Attribut aufweisen. Das Array enthält einen Wert für jedes Byte in der Zeichenfolge, einschließlich jeweils eines Bytes für das Lead- und zweite Byte aller Doppelbytezeichen in der Zeichenfolge. Für jeden Wert im Array können die Bits 0 bis 3 eine Kombination der folgenden Werte sein.



| Wert                      | Bedeutung                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| \_ATTR-EINGABE                | Vom Benutzer eingegebenes Zeichen. Die IME muss dieses Zeichen noch konvertieren.                           |
| \_ATTR-EINGABEFEHLER \_         | Ein Fehlerzeichen, das die IME nicht konvertieren kann. Beispielsweise kann die IME einige Konsonanten nicht zusammenstellen. |
| \_ATTR-ZIEL \_ KONVERTIERT    | Vom Benutzer ausgewähltes und dann vom IME konvertiertes Zeichen.                                             |
| ATTR \_ CONVERTED            | Zeichen, das die IME bereits konvertiert hat.                                                             |
| \_ATTR-ZIEL \_ NOTCONVERTED | Zeichen, das konvertiert wird. Der Benutzer hat dieses Zeichen ausgewählt, aber der IME hat es noch nicht konvertiert.     |
| ATTR \_ FIXEDCONVERTED       | Zeichen, die vom IME nicht mehr konvertiert werden.                                                           |



 

Alle anderen Werte sind reserviert. In Japanisch ist jedes unkonvertierte Zeichen mit dem ATTR \_ INPUT-Attribut ein Hiragana-, Katakana- oder alphanumerisches Zeichen. In Koreanisch stellt dieses Attribut ein Hangul-Zeichen dar, das die IME noch nicht konvertiert hat. In traditionellem chinesisch und vereinfachtem Chinesisch kann jede IME ihr Zeichen innerhalb eines bestimmten Bereichs einschränken.

Die im Kompositionszeichenfolgenstatus enthaltenen Klauselinformationen sind ein Array von 32-Bit-Werten, das die Positionen der Klauseln in der Kompositionszeichenfolge angibt. Das Array enthält einen Wert für jede Klausel und einen endgültigen Wert, der die Länge der vollständigen Zeichenfolge angibt. Jeder Wert im Array gibt den Offset in Bytes vom Anfang der Zeichenfolge bis zur -Klausel an. Der erste Wert ist immer 0, da die erste Klausel immer am Anfang der Zeichenfolge beginnt. Wenn eine Zeichenfolge beispielsweise über zwei Klauseln verfügt, haben die Klauselinformationen drei Werte: der erste Wert ist 0, der zweite Wert ist der Offset der zweiten Klausel und der dritte Wert die Länge der Zeichenfolge. Für Unicode wird die Position einer -Klausel in Unicode-Zeichen gezählt, und die Länge einer Zeichenfolge entspricht der Größe in Unicode-Zeichen.

Die im Status der Kompositionszeichenfolge enthaltenen Eingabeinformationen sind eine auf NULL endende Zeichenfolge, die die Zeichen darstellt, die der Benutzer an der Tastatur eingibt.

Die Im Kompositionszeichenfolgenstatus enthaltene Cursorposition ist ein Wert, der die Position des Cursors relativ zu den Zeichen in der Kompositionszeichenfolge angibt. Der Wert ist der Offset vom Anfang der Zeichenfolge in Bytes. Wenn dieser Wert 0 ist, befindet sich der Cursor unmittelbar vor dem ersten Zeichen in der Zeichenfolge. Wenn der Wert gleich der Länge der Zeichenfolge ist, befindet sich der Cursor unmittelbar nach dem letzten Zeichen. Wenn der Wert 1 ist, ist der Cursor nicht vorhanden. Für Unicode werden Position und Länge in Unicode-Zeichen gemessen.

Ihre Anwendung kann die Kompositionszeichenfolge oder Elemente des Kompositionsstatus mithilfe der [**ImmSetCompositionString-Funktion**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) festlegen. Um sicherzustellen, dass das Kompositionsfenster seine Darstellung basierend auf diesen Änderungen aktualisiert, ermöglicht die Funktion der Anwendung, eine Benachrichtigung an das Fenster zu senden. Anwendungen, die eine Kombination von Kompositionsstatuselementen festlegen, deaktivieren in der Regel Benachrichtigungen für alle bis auf den letzten Aufruf dieser Funktion, sodass nur eine Benachrichtigungsmeldung für das Kompositionsfenster generiert wird.

Schließlich unterstützt das Bearbeitungssteuerelement zwei Meldungen zum Ändern der Behandlung von Kompositionszeichenfolgen durch die IME. Weitere Informationen finden Sie unter [**EM \_ GETIMESTATUS**](../controls/em-getimestatus.md) und [**EM \_ SETIMESTATUS**](../controls/em-setimestatus.md). Weitere Informationen zum Bearbeitungssteuerelement finden Sie unter Bearbeiten von [Steuerelementen.](../controls/edit-controls.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum Eingabemethoden-Manager](about-input-method-manager.md)
</dt> </dl>

 

 
