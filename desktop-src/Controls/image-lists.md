---
title: Informationen zu Bildlisten
description: Eine Bildliste ist eine Sammlung von Bildern der gleichen Größe, auf die jeweils durch ihren Index verwiesen werden kann.
ms.assetid: vs|controls|~\controls\imagelist\imagelist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbfbb55ecd972e7f7e257eebabdb94ee40846a4f1b70b2a725ae1b67c6e69e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672205"
---
# <a name="about-image-lists"></a>Informationen zu Bildlisten

Eine Bildliste ist eine Sammlung von Bildern der gleichen Größe, auf die jeweils durch ihren Index verwiesen werden kann. Bildlisten werden verwendet, um große Mengen von Symbolen oder Bitmaps effizient zu verwalten. Alle Bilder in einer Bildliste sind in einer einzelnen, breiten Bitmap im Bildschirmgeräteformat enthalten. Eine Bildliste kann auch eine monocolore Bitmap enthalten, die Masken enthält, die zum transparenten Zeichnen von Bildern verwendet werden (Symbolformat).

Die Microsoft Win32-API bietet Bildlistenfunktionen und Makros, mit denen Sie Bildlisten erstellen und zerstören, Bilder hinzufügen und entfernen, Bilder ersetzen und zusammenführen, Bilder zeichnen und Bilder ziehen können. Um die Bildlistenfunktionen zu verwenden, schließen Sie die allgemeine Steuerelementheaderdatei in Ihre Quellcodedateien ein, und verknüpfen Sie sie mit der allgemeinen Steuerelementexportbibliothek. Verwenden Sie außerdem vor dem Aufrufen einer Bildlistenfunktion die Funktion [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) oder [**InitCommonControlsEx,**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) um sicherzustellen, dass die allgemeine Steuerelement-DLL geladen wird.

In diesem Abschnitt werden folgende Themen erörtert:

-   [Typen](#types)
-   [Erstellen und Zerstören von Bildlisten](#creating-and-destroying-image-lists)
-   [Hinzufügen und Entfernen von Bildern](#adding-and-removing-images)
-   [Ersetzen und Zusammenführen von Bildern](#replacing-and-merging-images)
-   [Zeichnen von Bildern](#drawing-images)
-   [Ziehen von Bildern](#dragging-images)
-   [Bildinformationen](#image-information)
-   [Bildüberlagerungen](#image-overlays)
-   [32-Bit-Symbole mit Antialiasing](#32-bit-antialiased-icons)

## <a name="types"></a>Typen

Es gibt zwei Arten von Bildlisten: nicht maskiert und maskiert. Eine nicht maskierte Bildliste besteht aus einer Farbbitmap, die ein oder mehrere Bilder enthält. Eine maskierte Bildliste besteht aus zwei Bitmaps gleicher Größe. Die erste ist eine Farbbitmap, die die Bilder enthält, und die zweite ist eine monocolore Bitmap, die eine Reihe von Masken enthält – eine für jedes Bild in der ersten Bitmap.

Wenn ein nicht maskiertes Bild gezeichnet wird, wird es einfach in den Zielgerätekontext kopiert. Das heißt, sie wird über die vorhandene Hintergrundfarbe des Gerätekontexts gezeichnet. Wenn ein maskiertes Bild gezeichnet wird, werden die Bits des Bilds mit den Bits der Maske kombiniert, wodurch in der Regel transparente Bereiche in der Bitmap erzeugt werden, in denen die Hintergrundfarbe des Zielgerätekontexts angezeigt wird. Es gibt mehrere Zeichnungsstile, die Sie beim Zeichnen eines maskierten Bilds angeben können. Sie können z. B. angeben, dass das Bild erweitert werden soll, um ein ausgewähltes Objekt anzugeben.

## <a name="creating-and-destroying-image-lists"></a>Erstellen und Zerstören von Bildlisten

Sie erstellen eine Bildliste, indem Sie die [**ImageList \_ Create-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) aufrufen. Zu den Parametern gehören der Typ der zu erstellende Bildliste, die Dimensionen der einzelnen Bilder und die Anzahl der Bilder, die Sie der Liste hinzufügen möchten. Für eine Nichtmaskenbildliste erstellt die Funktion eine einzelne Bitmap, die groß genug ist, um die angegebene Anzahl von Bildern der angegebenen Dimensionen aufzunehmen. Anschließend wird ein bildschirmkompatibeler Gerätekontext erstellt und die Bitmap darin ausgewählt. Für eine maskierte Bildliste erstellt die Funktion zwei Bitmaps und zwei bildschirmkompatible Gerätekontexte. Sie wählt die Bildbitmap in einem Gerätekontext und die Maskierungsbitmap in den anderen aus. Die allgemeine Steuerelement-DLL enthält den ausführbaren Code für die Bildlistenfunktionen.

[**In ImageList \_ Erstellen**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create)geben Sie die anfängliche Anzahl von Bildern an, die in einer Bildliste enthalten sein werden, sowie die Anzahl der Bilder, um die die Liste vergrößert werden kann. Wenn Sie also versuchen, mehr Bilder hinzuzufügen, als Sie ursprünglich angegeben haben, wird die Bildliste automatisch vergrößert, um die neuen Bilder aufzunehmen.

Wenn ImageList Create erfolgreich [**\_ ist,**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) wird ein Handle für den HIMAGELIST-Typ zurückgegeben. Sie verwenden dieses Handle in anderen Bildlistenfunktionen, um auf die Bildliste zuzugreifen und die Images zu verwalten. Sie können Bilder hinzufügen und entfernen, Bilder aus einer Bildliste in eine andere kopieren und Bilder aus zwei verschiedenen Bildlisten zusammenführen. Wenn Sie eine Bildliste nicht mehr benötigen, können Sie sie zerstören, indem Sie ihr Handle in einem Aufruf der [**ImageList \_ Destroy-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_destroy) angeben.

## <a name="adding-and-removing-images"></a>Hinzufügen und Entfernen von Bildern

Sie können Bitmapbilder, Symbole oder Cursor zu einer Bildliste hinzufügen. Sie fügen Bitmapbilder hinzu, indem Sie die Handles für zwei Bitmaps in einem Aufruf der [**Funktion ImageList \_ Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) angeben. Die erste Bitmap enthält ein oder mehrere Bilder, die der Bildbitmap hinzugefügt werden sollen, und die zweite Bitmap enthält die Masken, die der Maskenbitmap hinzugefügt werden sollen. Bei Bildlisten ohne Maskierung wird das zweite Bitmaphandle ignoriert. sie kann auf **NULL** festgelegt werden.

Die [**Funktion ImageList \_ AddMasked**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addmasked) fügt einer maskierten Bildliste auch Bitmapbilder hinzu. Diese Funktion ähnelt [**ImageList \_ Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add), mit der Ausnahme, dass Sie keine Maskenbitmap angeben. Stattdessen geben Sie eine Farbe an, die das System mit der Bildbitmap kombiniert, um die Masken automatisch zu generieren. Jedes Pixel der angegebenen Farbe in der Bildbitmap wird in Schwarz geändert, und das entsprechende Bit in der Maske wird auf 1 festgelegt. Daher ist jedes Pixel im Bild, das der angegebenen Farbe entspricht, transparent, wenn das Bild gezeichnet wird.

Das [**ImageList \_ AddIcon-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) fügt einer Bildliste ein Symbol oder einen Cursor hinzu. Wenn die Bildliste maskiert ist, fügt **ImageList \_ AddIcon** die Maske hinzu, die mit dem Symbol oder Cursor zur Maskenbitmap bereitgestellt wird. Wenn die Bildliste nicht maskiert ist, wird die Maske für das Symbol oder den Cursor beim Zeichnen des Bilds nicht verwendet.

Sie können ein Symbol basierend auf einem Bild und einer Maske in einer Bildliste erstellen, indem Sie die [**\_ GetIcon-Funktion ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_geticon) verwenden. Die Funktion gibt das Handle an das neue Symbol zurück.

[**ImageList \_ Fügen Sie**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add), [**ImageList \_ AddMasked**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addmasked)und [**ImageList \_ AddIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) hinzu, um jedem Bild einen Index zuzuweisen, während es einer Bildliste hinzugefügt wird. Die Indizes sind nullbasiert. Das heißt, das erste Bild in der Liste weist einen Index von 0 (null) auf, das nächste hat einen Index von 1 usw. Nach dem Hinzufügen eines einzelnen Bilds geben die Funktionen den Index des Bilds zurück. Wenn mehrere Bilder gleichzeitig hinzugefügt werden, geben die Funktionen den Index des ersten Bilds zurück.

Die [**Funktion ImageList \_ Remove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_remove) entfernt ein Bild aus einer Bildliste.

## <a name="replacing-and-merging-images"></a>Ersetzen und Zusammenführen von Bildern

Die Funktionen [**ImageList \_ Replace**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_replace) und [**ImageList \_ ReplaceIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_replaceicon) ersetzen ein Bild in einer Bildliste durch ein neues Image. **ImageList \_ Ersetzen** ersetzt ein Bild durch ein Bitmapbild und eine Maske, und **ImageList \_ ReplaceIcon** ersetzt ein Bild durch ein Symbol oder einen Cursor.

Die [**Funktion ImageList \_ Merge**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_merge) führt zwei Bilder zusammen und speichert das neue Bild in einer neuen Bildliste. Das neue Bild wird erstellt, indem das zweite Bild transparent über dem ersten gezeichnet wird. Die Maske für das neue Bild ist das Ergebnis einer logischen **OR-Operation** für die Bits der Masken für die beiden vorhandenen Bilder.

## <a name="drawing-images"></a>Zeichnen von Bildern

Um ein Bild zu zeichnen, verwenden Sie die [**Funktion ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) oder [**ImageList \_ DrawEx.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) Sie geben das Handle für eine Bildliste, den Index des zu zeichnende Bilds, das Handle für den Zielgerätekontext, eine Position im Gerätekontext und mindestens einen Zeichnungsstil an.

Wenn Sie den **ILD \_** TRANSPARENT-Stil angeben, verwendet [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) oder [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) einen zweistufigen Prozess, um ein maskiertes Bild zu zeichnen. Zunächst wird ein logischer **AND-Vorgang** für die Bits des Bilds und die Bits der Maske ausgeführt. Anschließend wird ein logischer **XOR-Vorgang** für die Ergebnisse des ersten Vorgangs und die Hintergrundbits des Zielgerätekontexts ausgeführt. Dieser Prozess erstellt transparente Bereiche im resultierenden Bild. Das heißt, jedes weiße Bit in der Maske bewirkt, dass das entsprechende Bit im resultierenden Bild transparent ist.

Bevor Sie ein maskiertes Bild auf einem Volltonfarbhintergrund zeichnen, sollten Sie die [**ImageList \_ SetBkColor-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setbkcolor) verwenden, um die Hintergrundfarbe der Bildliste auf die gleiche Farbe wie das Ziel festzulegen. Durch Festlegen der Farbe müssen keine transparenten Bereiche im Bild erstellt werden, und [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) kann das Bild einfach in den Zielgerätekontext kopiert werden, was zu einer erheblichen Leistungssteigerung führt. [**\_**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) Um das Bild zu zeichnen, geben Sie den **ILD \_ NORMAL-Stil** in einem Aufruf von **ImageList \_ Draw** oder **ImageList \_ DrawEx** an.

Sie können die Hintergrundfarbe für eine Maskierungsbildliste jederzeit festlegen, sodass sie ordnungsgemäß auf einem soliden Hintergrund zeichnet. Wenn die Hintergrundfarbe auf CLR NONE festgelegt \_ wird, werden Bilder standardmäßig transparent gezeichnet. Verwenden Sie die [**ImageList \_ GetBkColor-Funktion,**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getbkcolor) um die Hintergrundfarbe einer Bildliste abzurufen.

Die **ILD \_ BLEND25-** und **ILD \_ BLEND50-Stile** fügen das Bild mit der Hervorhebungsfarbe des Systems ein. Diese Stile sind nützlich, wenn Sie ein maskiertes Bild verwenden, um ein Objekt darzustellen, das der Benutzer auswählen kann. Beispielsweise können Sie das **ILD \_ BLEND50-Format** verwenden, um das Bild zu zeichnen, wenn der Benutzer es auswählt.

Ein nicht maskiertes Bild wird mithilfe des SRCCOPY-Rastervorgangs in den Zielgerätekontext kopiert. Die Farben im Bild werden unabhängig von der Hintergrundfarbe des Gerätekontexts gleich angezeigt. Die in [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) oder [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) angegebenen Zeichnungsstile haben auch keine Auswirkungen auf die Darstellung eines nicht maskierten Bilds.

## <a name="dragging-images"></a>Ziehen von Bildern

Die Win32-API enthält Funktionen zum Ziehen eines Bilds auf dem Bildschirm. Die Ziehfunktionen verschieben ein Bild reibungslos, in Farbe und ohne Blinken des Cursors. Maskierte und nicht maskierte Bilder können gezogen werden.

Die [**ImageList \_ BeginDrag-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) startet einen Ziehvorgang. Zu den Parametern gehören das Handle für die Bildliste, der Index des zu ziehende Bilds und die Position des Hotspots innerhalb des Bilds. Der Hot Spot ist ein einzelnes Pixel, das die Ziehfunktionen als genaue Bildschirmposition des Bilds erkennen. In der Regel legt eine Anwendung den Hotspots so fest, dass er mit dem Hot Spot des Mauscursors übereinstimmt. Die [**Funktion ImageList \_ DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) verschiebt das Bild an eine neue Position.

Die [**ImageList \_ DragEnter-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragenter) legt die Anfangsposition des Ziehbilds innerhalb eines Fensters fest und zeichnet das Bild an der Position. Die Parameter enthalten das Handle für das Fenster, in dem das Bild gezeichnet werden soll, und die Koordinaten der Anfangsposition innerhalb des Fensters. Die Koordinaten sind relativ zur oberen linken Ecke des Fensters und nicht zum Clientbereich. Dasselbe gilt für alle Bildziehfunktionen, die Koordinaten als Parameter annehmen. Dies bedeutet, dass Sie die Breite von Fensterelementen wie Rahmen, Titelleiste und Menüleiste kompensieren müssen, wenn Sie die Koordinaten angeben. Wenn Sie beim Aufrufen von **ImageList \_ DragEnter** ein NULL-Fensterhandle angeben, zeichnen die Ziehfunktionen das Bild im Gerätekontext, der dem Desktopfenster zugeordnet ist, und die Koordinaten sind relativ zur oberen linken Ecke des Bildschirms. 

Die [**ImageList \_ SetDragCursorImage-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setdragcursorimage) erstellt ein neues Ziehbild, indem das angegebene Bild (normalerweise ein Mauszeigerbild) mit dem aktuellen Ziehbild kombiniert wird. Da die Ziehfunktionen das neue Bild während eines Ziehvorgangs verwenden, sollten Sie die [**ShowCursor-Funktion**](/windows/desktop/api/winuser/nf-winuser-showcursor) verwenden, um den tatsächlichen Mauszeiger nach dem Aufruf von **ImageList \_ SetDragCursorImage auszublenden.** Andernfalls scheint das System für die Dauer des Ziehvorgangs über zwei Mauscursor zu verfügen.

Wenn eine Anwendung [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag)aufruft, erstellt das System eine temporäre interne Bildliste und kopiert dann das angegebene Ziehbild in die interne Liste. Sie können das Handle mithilfe der [**ImageList \_ GetDragImage-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getdragimage) in die temporäre Bildliste ziehen. Die Funktion ruft auch die aktuelle Ziehposition und den Offset des Ziehbilds relativ zur Ziehposition ab.

## <a name="image-information"></a>Bildinformationen

Es gibt eine Reihe von Funktionen, die Informationen aus einer Bildliste abrufen. Die [**ImageList \_ GetImageInfo-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getimageinfo) füllt eine [**IMAGEINFO-Struktur**](/windows/desktop/api) mit Informationen zu einem einzelnen Bild, einschließlich der Handles des Bilds und der Maskierungsbitmaps, der Anzahl der Farbebenen und Bits pro Pixel und des umschließenden Rechtecks des Bilds innerhalb der Bildbitmap. Sie können diese Informationen verwenden, um die Bitmaps für das Bild direkt zu bearbeiten. Die [**ImageList \_ GetImageCount-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getimagecount) ruft die Anzahl der Bilder in einer Bildliste ab.

## <a name="image-overlays"></a>Bildüberlagerungen

Jede Bildliste enthält eine Liste von Indizes, die als Überlagerungen verwendet werden sollen. Eine Überlagerung ist ein Bild, das transparent über ein anderes Bild gezeichnet wird. Jedes Bild, das sich derzeit in der Bildliste befindet, kann als Überlagerung verwendet werden. Sie können bis zu vier Überlagerungen pro Bildliste angeben. Dieser Grenzwert wurde in Version 4.71 auf 15 erweitert.

Sie fügen den Index eines Bilds der Liste der Überlagerungen hinzu, indem Sie die [**ImageList \_ SetOverlayImage-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) verwenden und das Handle für die Bildliste, den Index des vorhandenen Bilds und den gewünschten Überlagerungsindex angeben. Dadurch wird der Bildliste mitgeteilt, dass "das Bild am Index *x* als Überlagerung verwendet werden kann, und ich möchte die Überlagerung als Überlagerungsindex *y* bezeichnen". Die Überlagerungsindizes sind ein- statt nullbasiert, da ein Überlagerungsindex von 0 bedeutet, dass keine Überlagerung verwendet wird.

Sie geben beim Zeichnen eines Bilds mit der [**Funktion ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) oder [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) eine Überlagerung an. Die Überlagerung wird durch  Ausführen eines logischen OR-Vorgangs zwischen den gewünschten Zeichnungsflags und dem Ergebnis des [**INDEXTOOVERLAYMASK-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) angegeben. Das **INDEXTOOVERLAYMASK-Makro** verwendet den Überlagerungsindex und formatiert ihn für die Aufnahme mit den Flags für diese Funktionen. Dadurch wird das Bild mit der angegebenen Überlagerung gezeichnet. Im folgenden Beispiel wird veranschaulicht, wie beim Zeichnen des Bilds eine Überlagerung hinzugefügt und angegeben wird.


```
ImageList_SetOverlayImage(himl, 0, 3);
ImageList_Draw(himl, 1, hdc, 0, 0, ILD_MASK | INDEXTOOVERLAYMASK(3));
```



Dadurch wird Bild 1 gezeichnet und dann mit Bild 0 überlagert. Da 3 der Overlayindex ist, den Sie im [**ImageList \_ SetOverlayImage-Aufruf**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) angegeben haben, wird 3 im [**INDEXTOOVERLAYMASK-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) platziert.

## <a name="32-bit-antialiased-icons"></a>32-Bit-Symbole mit Antialiasing

Antialiasing ist eine Technik zum Aufweichen oder Weichzeichnen von spitzen Kanten. Dadurch erhalten Bilder eine natürlichere Darstellung. Bildlisten in Windows Vista und Windows 7 unterstützen die Verwendung von Symbolen und Bitmaps mit 32-Bit-Antialiasing. Farbwerte verwenden 24 Bits, und 8 Bits werden als Alphakanal auf den Symbolen verwendet. Um eine Bildliste zu erstellen, die ein Bild mit 32 Bits pro Pixel (bpp) verarbeiten kann, rufen Sie die [**ImageList \_ Create-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) auf, und übergeben Sie ein ILC \_ COLOR32-Flag.

Um 32-Bit-Symbole ordnungsgemäß zu erstellen, müssen Sie mehrere Bilder für jedes Symbol erstellen, wie in der folgenden Abbildung dargestellt.

![Abbildung mit drei Größen von Symbolen für jede von drei Farbtiefe](images/theme2.png)

-   Die ersten drei Bilder befinden sich im 16-Farben-Modus für die Verwendung im abgesicherten Modus.
-   Die nächsten drei Symbole werden im 256-Farben-Modus verwendet.
-   Die letzten drei Symbole verfügen über den Alphakanal und können nur in Betriebssystemen mit 24-Bit-Farben oder höher verwendet werden.
-   Die Reihenfolge der Bilder im Symbolformat spielt eine Rolle. Wenn die Reihenfolge falsch ist, funktionieren ältere Versionen von Windows beim Extrahieren der Symbole schlecht. Das falsche Extrahieren der Symbole kann zu Speicherbeschädigung und falschem Rendering führen.
-   Frühere Versionen von Windows hatten ein Ressourcenlimit von 10 Symbolen.

> [!Note]  
> Sie können Tools von Drittanbietern verwenden, um Symboldateien und Bitmaps zu generieren, die einen Alphakanal enthalten. Wenn Sie [**LoadImage**](/windows/desktop/api/winuser/nf-winuser-loadimagea) verwenden, um eine 32-BPP-Bitmap zu laden, die Alpha enthält, müssen Sie das LR \_ CREATEDIBSECTION-Flag angeben.

 

 

 