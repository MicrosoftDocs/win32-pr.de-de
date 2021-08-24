---
description: Verwenden des Schriftartfallbacks
ms.assetid: 952f33b6-ca52-40a2-b914-52c1c62ae0e0
title: Verwenden des Schriftartfallbacks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9a4e9b329e2c3257ae9fad02f1fb4774a63dc1d4b4e804c0dca8e690cbf4d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787870"
---
# <a name="using-font-fallback"></a>Verwenden des Schriftartfallbacks

> [!Note]  
> In diesem Thema gelten alle Hinweise zu [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) gleichermaßen für [**ScriptShapeOpenType.**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)

 

Ihre Anwendung muss während der Textanzeige einen Schriftartfallback verwenden, wenn einige Zeichen in einer Zeichenfolge in der Schriftart nicht unterstützt werden oder wenn die Anwendung ein [komplexes Skript](uniscribe-glossary.md) verwendet, das von der Schriftart nicht unterstützt wird. Die Anforderung eines Schriftartfallbacks wird während des Layoutprozesses für Text erkannt, wenn die Anwendung die [**ScriptShape-Funktion**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) aufruft. Informationen zur Textanzeige finden Sie unter [Anzeigen von Text mit Uniscribe.](displaying-text-with-uniscribe.md)

## <a name="determine-the-need-for-font-fallback-for-unsupported-characters"></a>Ermitteln der Notwendigkeit eines Schriftartfallbacks für nicht unterstützte Zeichen

Wenn einige der Zeichen in einer Zeichenfolge in einer angeforderten Schriftart nicht unterstützt werden, ist ein Anwendungsaufruf von [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) erfolgreich. Die Anwendung muss jedoch den Glyphenausgabepuffer auf fehlende Glyphen überprüfen. Der Glyphenindex des fehlenden Glyphens kann für eine bestimmte Schriftart bestimmt werden, indem [**ScriptGetFontProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties)aufgerufen wird. Wenn ein bestimmtes Symbol nicht verfügbar ist, muss die Anwendung entweder auf eine andere Schriftart für ein Symbol zurückgreifen oder ein Grafiksymbol rendern, das angibt, dass kein Symbol verfügbar ist.

## <a name="determine-the-need-for-font-fallback-for-unsupported-complex-scripts"></a>Ermitteln der Notwendigkeit eines Schriftartfallbacks für nicht unterstützte komplexe Skripts

Die Schriftart, die eine Anwendung für die Anzeige bevorzugt, unterstützt möglicherweise kein komplexes Skript, das für den Text erforderlich ist. In diesem Fall schlägt der Anwendungsaufruf von [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) mit dem Fehlercode E \_ SCRIPT NOT IN FONT \_ \_ \_ fehl.

## <a name="assign-a-fallback-font"></a>Zuweisen einer Fallbackschriftart

Nachdem festgestellt wurde, dass ein Schriftartfallback erforderlich ist, muss die Anwendung eine Fallbackschriftart zuweisen. Die Anwendung kann die folgenden Verfahren ausprobieren:

-   Rufen Sie [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) für jede Schriftart in einer Schriftartliste auf, bis ein Aufruf eine akzeptable Rückgabe hat.
-   Rufen Sie [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) mit jeder Schriftart in einer Liste auf, bis festgestellt werden kann, dass keine Schriftart erfolgreich ist. Wenn der Fehlercode immer E \_ SCRIPT NOT IN FONT \_ \_ \_ lautet, wird ein komplexes Skript von den Schriftarten nicht unterstützt. Rendern Sie entweder ein Grafiksymbol, das angibt, dass kein Symbol verfügbar ist, oder geben Sie das Skript als nicht definiert (keine Skriptverarbeitung) erneut an, und starten Sie es erneut. Um das Skript als nicht definiert festzulegen, legen Sie den **eScript-Member** der [**SCRIPT \_ ANALYSIS-Struktur**](/windows/win32/api/usp10/ns-usp10-script_analysis) auf SCRIPT \_ UNDEFINED fest.
-   Rufen Sie [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) mit jeder Schriftart in einer Liste auf, bis festgestellt werden kann, dass keine Schriftart erfolgreich ist. Wenn der Fehlercode angibt, dass einige der Zeichen fehlenden Glyphen zugeordnet sind, untergliedern Sie die Zeichenfolge in kleinere Bereiche. Unterbereiche können unterschiedliche Schriftarten zugewiesen werden, sodass mehr Zeichen gerendert werden können.

## <a name="generate-glyph-information"></a>Generieren von Glypheninformationen

Sobald die Anwendung eine Schriftart zugewiesen hat, die bei Aufrufen von [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)erfolgreich ist, kann sie [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) aufrufen, um Glyphen für die breite und zweidimensionale Offsetinformationen aus der Ausgabe von **ScriptShape** zu generieren. Die Schriftart sollte in diesen Aufrufen erfolgreich sein. Ein Schriftartfehler in einem Aufruf von **ScriptPlace** nach erfolgreichem **ScriptShape-Aufruf** weist auf eine fehlerhafte Schriftart hin.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



