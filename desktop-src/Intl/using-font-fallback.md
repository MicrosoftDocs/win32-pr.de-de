---
description: Verwenden eines Schriftart-Fallbacks
ms.assetid: 952f33b6-ca52-40a2-b914-52c1c62ae0e0
title: Verwenden eines Schriftart-Fallbacks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9afb073a01cc1c5b90d4a4861a973846d3ae9ae1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760483"
---
# <a name="using-font-fallback"></a>Verwenden eines Schriftart-Fallbacks

> [!Note]  
> In diesem Thema gelten alle Hinweise zu [**scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) gleichermaßen für [**scriptshapeopentype**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype).

 

Die Anwendung muss bei der Textanzeige ein Schriftart Fall Back verwenden, wenn einige Zeichen in einer Zeichenfolge in der Schriftart nicht unterstützt werden oder wenn die Anwendung ein [komplexes Skript](uniscribe-glossary.md) verwendet, das von der Schriftart nicht unterstützt wird. Die Anforderung für einen Schriftart Fall Back wird während des Layoutprozesses für Text erkannt, wenn die Anwendung die [**scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) -Funktion aufruft. Informationen zur Textanzeige finden Sie unter [Anzeigen von Text mit uniwriter](displaying-text-with-uniscribe.md).

## <a name="determine-the-need-for-font-fallback-for-unsupported-characters"></a>Bestimmen der Notwendigkeit eines Schriftart Fallbacks für nicht unterstützte Zeichen

Wenn einige der Zeichen in einer Zeichenfolge in einer angeforderten Schriftart nicht unterstützt werden, ist ein Anwendungs Befehl von [**scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) erfolgreich. Die Anwendung muss jedoch den Ausgabepuffer des Symbols überprüfen, damit fehlende Symbole vorhanden sind. Der Glyphe-Index des fehlenden Symbols kann durch Aufrufen von [**scriptgetfontproperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties)für eine bestimmte Schriftart bestimmt werden. Wenn ein bestimmtes Symbol nicht verfügbar ist, muss die Anwendung entweder auf eine andere Schriftart für ein Symbol zurückgreifen oder ein Grafik Symbol darstellen, das angibt, dass kein Symbol verfügbar ist.

## <a name="determine-the-need-for-font-fallback-for-unsupported-complex-scripts"></a>Bestimmen der Notwendigkeit eines Schriftart Fallbacks für nicht unterstützte komplexe Skripts

Die Schriftart, die von einer Anwendung für die Anzeige bevorzugt wird, unterstützt möglicherweise kein komplexes Skript, das für den Text erforderlich ist. In diesem Fall schlägt der Anwendungs Aufrufvorgang für [**scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) mit dem Fehlercode E \_ Script \_ Not \_ in Font fehl \_ .

## <a name="assign-a-fallback-font"></a>Fall Back Schriftart zuweisen

Nachdem festgestellt wurde, dass ein Fall Back für die Schriftart erforderlich ist, muss die Anwendung eine Ausweich Schriftart zuweisen. Die Anwendung kann die folgenden Techniken ausprobieren:

-   [**Scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) wird für jede Schriftart in einer Schriftart Liste aufgerufen, bis ein Rückruf eine akzeptable Rückgabe hat.
-   Nennen Sie [**scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) mit jeder Schriftart in einer Liste, bis festgestellt werden kann, dass keine Schriftart erfolgreich ausgeführt werden kann. Wenn der Fehlercode immer das \_ Skript \_ nicht in der Schriftart ist \_ \_ , wird ein komplexes Skript nicht von den Schriftarten unterstützt. Stellen Sie entweder ein Grafik Symbol dar, das angibt, dass kein Symbol verfügbar ist, oder geben Sie das Skript erneut als nicht definiert (keine Skript Verarbeitung) an, und starten Sie es erneut. Um das Skript als nicht definiert festzulegen, legen Sie den **Escript** -Member der [**Skript \_ Analyse**](/windows/win32/api/usp10/ns-usp10-script_analysis) Struktur auf Skript nicht \_ definiert fest.
-   Nennen Sie [**scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) mit jeder Schriftart in einer Liste, bis festgestellt werden kann, dass keine Schriftart erfolgreich ausgeführt werden kann. Wenn der Fehlercode anzeigt, dass einige der Zeichen mit fehlenden Symbolen kombiniert werden, unterbrechen Sie die Zeichenfolge in kleinere Bereiche. Unterbereiche können unterschiedliche Schriftarten zugewiesen werden, sodass mehr Zeichen gerendert werden können.

## <a name="generate-glyph-information"></a>Generieren von Symbol Informationen

Nachdem die Anwendung eine Schriftart zugewiesen hat, die in Aufrufen von [**scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)erfolgreich ist, kann Sie [**scriptplace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) aufrufen, um die erweiterte Symbol Breite und die zweidimensionalen Offset Informationen aus der Ausgabe von **scriptshape** zu generieren. Die Schriftart sollte in diesen Aufrufen erfolgreich sein. Ein Schriftart Fehler in einem **scriptplace-Skript** nach erfolgreicher Ausführung in einem **scriptshape** -Rückruf weist auf eine fehlerhafte Schriftart hin.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von uniscri](using-uniscribe.md)
</dt> </dl>

 

 



