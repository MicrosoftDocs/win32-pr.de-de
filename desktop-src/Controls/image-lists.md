---
title: Informationen zu Bildlisten
description: Eine Bildliste ist eine Auflistung von Bildern derselben Größe, auf die jeweils durch ihren Index verwiesen werden kann.
ms.assetid: vs|controls|~\controls\imagelist\imagelist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f059e89b04d16088fff1d937bd29cb23a427d4c2
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316532"
---
# <a name="about-image-lists"></a>Informationen zu Bildlisten

Eine Bildliste ist eine Auflistung von Bildern derselben Größe, auf die jeweils durch ihren Index verwiesen werden kann. Bildlisten werden verwendet, um große Mengen von Symbolen oder Bitmaps effizient zu verwalten. Alle Bilder in einer Bildliste sind in einer einzelnen, breiten Bitmap im Bildschirmformat enthalten. Eine Bildliste kann auch eine monochrome Bitmap enthalten, die Masken enthält, die zum transparenten Zeichnen von Bildern verwendet werden (Symbol Stil).

Die Microsoft Win32-API stellt Bildlisten Funktionen und-Makros bereit, mit denen Sie Bildlisten erstellen und zerstören, Bilder hinzufügen und entfernen, Bilder ersetzen und zusammenführen, Bilder zeichnen und Bilder ziehen können. Um die Abbild Listen Funktionen zu verwenden, schließen Sie die allgemeine Steuerungs Header Datei in die Quell Code Dateien ein, und verknüpfen Sie Sie mit der Common Control-Export Bibliothek. Verwenden Sie außerdem vor dem Aufrufen einer bildlist-Funktion die Funktion [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) oder [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , um sicherzustellen, dass die DLL des allgemeinen Steuer Elements geladen wird.

In diesem Abschnitt werden folgende Themen erörtert:

-   [Typen](#types)
-   [Erstellen und zerstören von Bildlisten](#creating-and-destroying-image-lists)
-   [Hinzufügen und Entfernen von Bildern](#adding-and-removing-images)
-   [Ersetzen und Zusammenführen von Bildern](#replacing-and-merging-images)
-   [Zeichnen von Bildern](#drawing-images)
-   [Ziehen von Bildern](#dragging-images)
-   [Bild Informationen](#image-information)
-   [Bildüberlagerungen](#image-overlays)
-   [32-Bit-Symbole mit Antialiasing](#32-bit-antialiased-icons)

## <a name="types"></a>Typen

Es gibt zwei Typen von Bildlisten: nicht maskiert und maskiert. Eine nicht maskierte Bildliste besteht aus einer Farb Bitmap, die ein oder mehrere Bilder enthält. Eine maskierte Bildliste besteht aus zwei Bitmaps gleicher Größe. Der erste ist eine Farb Bitmap, die die Bilder enthält, und die zweite ist eine monochrome Bitmap, die eine Reihe von Masken enthält – eine für jedes Bild in der ersten Bitmap.

Wenn ein nicht maskiertes Bild gezeichnet wird, wird es einfach in den Zielgeräte Kontext kopiert. Das heißt, Sie wird über die vorhandene Hintergrundfarbe des Geräte Kontexts gezeichnet. Wenn ein maskiertes Bild gezeichnet wird, werden die Bits des Bilds mit den Bits der Maske kombiniert, wobei in der Regel transparente Bereiche in der Bitmap erzeugt werden, in denen die Hintergrundfarbe des Zielgeräte Kontexts über angezeigt wird. Es gibt mehrere Zeichnungs Stile, die Sie angeben können, wenn Sie ein maskiertes Bild zeichnen. Beispielsweise können Sie angeben, dass das Bild ausgeblendet werden soll, um ein ausgewähltes Objekt anzugeben.

## <a name="creating-and-destroying-image-lists"></a>Erstellen und zerstören von Bildlisten

Sie erstellen eine Bildliste, indem Sie die Create-Funktion von [**ImageList \_**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) aufrufen. Zu den Parametern zählen der Typ der zu erstellenden Bildliste, die Abmessungen der einzelnen Bilder und die Anzahl der Bilder, die Sie der Liste hinzufügen möchten. Für eine nicht maskierte Bildliste erstellt die-Funktion eine einzelne Bitmap, die groß genug ist, um die angegebene Anzahl von Bildern der angegebenen Dimensionen aufzunehmen. Anschließend wird ein Bildschirm kompatibler Gerätekontext erstellt und die Bitmap darin ausgewählt. Für eine maskierte Bildliste erstellt die Funktion zwei Bitmaps und zwei Bildschirm kompatible Geräte Kontexte. Er wählt die Bild Bitmap in einem Gerätekontext und das Masken Bitmuster in das andere aus. Die allgemeine Steuerelement-DLL enthält den ausführbaren Code für die ImageList-Funktionen.

In [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create)geben Sie die anfängliche Anzahl der Bilder an, die in einer Bildliste enthalten sein sollen, sowie die Anzahl der Bilder, um die die Liste vergrößert werden kann. Wenn Sie also versuchen, mehr Bilder hinzuzufügen, als Sie anfänglich angegeben haben, wächst die Bildliste automatisch, um die neuen Images aufzunehmen.

Wenn [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) erfolgreich ist, wird ein Handle für den HIMAGELIST-Typ zurückgegeben. Sie verwenden dieses Handle in anderen Bildlisten Funktionen, um auf die Bildliste zuzugreifen und die Bilder zu verwalten. Sie können Bilder hinzufügen und entfernen, Bilder aus einer Bildliste in eine andere kopieren und Bilder aus zwei unterschiedlichen Bildlisten zusammenführen. Wenn Sie keine Bildliste mehr benötigen, können Sie Sie durch Angabe Ihres Handles in einem [**aufzurufenden Befehl der ImageList \_ Destroy**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_destroy) -Funktion zerstören.

## <a name="adding-and-removing-images"></a>Hinzufügen und Entfernen von Bildern

Sie können einer Bildliste Bitmap-Bilder, Symbole oder Cursor hinzufügen. Sie fügen Bitmap-Bilder hinzu, indem Sie die Handles für zwei Bitmaps in einem [**aufzurufenden Befehl der ImageList- \_ Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) -Funktion angeben. Die erste Bitmap enthält ein oder mehrere Bilder, die der bildinbitmap hinzugefügt werden sollen, und die zweite Bitmap enthält die Masken, die der Maske-Bitmap hinzugefügt werden sollen. Bei nicht maskierten Bildlisten wird das zweite Bitmap-Handle ignoriert. Sie kann auf **null** festgelegt werden.

Die [**ImageList-Funktion \_ addmaskierte**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addmasked) fügt auch Bitmap-Bilder einer maskierten Bildliste hinzu. Diese Funktion ähnelt [**ImageList \_ Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add), mit dem Unterschied, dass Sie keine Masken Bitmap angeben. Stattdessen geben Sie eine Farbe an, die das System mit der Bild Bitmap kombiniert, um die Masken automatisch zu generieren. Jedes Pixel der angegebenen Farbe in der Bild Bitmap wird in Schwarz geändert, und das entsprechende Bit in der Maske wird auf 1 festgelegt. Folglich ist jedes Pixel im Bild, das mit der angegebenen Farbe übereinstimmt, transparent, wenn das Bild gezeichnet wird.

Das [**ImageList \_ addicon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) -Makro fügt einer Bildliste ein Symbol oder einen Cursor hinzu. Wenn die Bildliste maskiert ist, fügt **ImageList \_ addicon** der Maske-Bitmap die Maske hinzu, die mit dem Symbol oder dem Cursor bereitgestellt wird. Wenn die Bildliste nicht maskiert ist, wird die Maske für das Symbol oder den Cursor beim Zeichnen des Bilds nicht verwendet.

Sie können ein Symbol auf der Grundlage eines Bilds und einer Maske in einer Bildliste erstellen, indem Sie die [**ImageList \_ GetIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_geticon) -Funktion verwenden. Die-Funktion gibt das Handle für das neue Symbol zurück.

[**ImageList \_ Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add), [**ImageList \_ addmaskierte**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addmasked)und [**ImageList \_ addicon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) weisen jedem Image einen Index zu, wenn es einer Bildliste hinzugefügt wird. Die Indizes sind NULL basiert. Das heißt, das erste Bild in der Liste weist einen Index von NULL auf, der nächste einen Index von 1 usw. Nachdem Sie ein einzelnes Bild hinzugefügt haben, geben die Funktionen den Index des Bilds zurück. Wenn mehr als ein Bild gleichzeitig hinzugefügt wird, geben die Funktionen den Index des ersten Bilds zurück.

Mit der Funktion zum [**\_ Entfernen von ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_remove) wird ein Bild aus einer Bildliste entfernt.

## <a name="replacing-and-merging-images"></a>Ersetzen und Zusammenführen von Bildern

Die Funktionen " [**ImageList \_ Replace**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_replace) " und " [**ImageList \_ replaceicon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_replaceicon) " Ersetzen ein Bild in einer Bildliste durch ein neues Bild. **ImageList \_ Replace** ersetzt ein Bild durch ein Bitmap-Bild und eine Maske, und **ImageList \_ replaceicon** ersetzt ein Bild durch ein Symbol oder einen Cursor.

Die [**ImageList- \_ Merge**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_merge) -Funktion führt zwei Bilder zusammen, wobei das neue Bild in einer neuen Bildliste gespeichert wird. Das neue Bild wird erstellt, indem das zweite Bild transparent über das erste gezeichnet wird. Die Maske für das neue Image ist das Ergebnis der Ausführung einer logischen **or** -Operation auf den Bits der Masken für die beiden vorhandenen Bilder.

## <a name="drawing-images"></a>Zeichnen von Bildern

Zum Zeichnen eines Bilds verwenden Sie die Funktion " [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) " oder " [**ImageList \_ drawex**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) ". Sie geben das Handle für eine Bildliste, den Index des zu zeichnenden Bilds, das Handle für den Zielgeräte Kontext, einen Speicherort innerhalb des Geräte Kontexts und einen oder mehrere Zeichnungs Stile an.

Wenn Sie den Stil " **ild \_ transparent** " angeben, wird von [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) oder [**ImageList \_ drawex**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) ein zweistufiger Prozess zum Zeichnen eines maskierten Bilds verwendet. Zuerst führt Sie eine logische **and-** Operation für die Bits des Bilds und die Bits der Maske aus. Anschließend führt er eine logische **Xor** -Operation für die Ergebnisse des ersten Vorgangs und die hintergrundbits des Zielgeräte Kontexts aus. Dieser Prozess erstellt transparente Bereiche im resultierenden Image. Das heißt, jedes weiße Bit in der Maske bewirkt, dass das entsprechende Bit im resultierenden Bild transparent ist.

Vor dem Zeichnen eines maskierten Bilds auf einem voll Tonfarben-Hintergrund sollten Sie die Funktion " [**ImageList \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setbkcolor) " verwenden, um die Hintergrundfarbe der Bildliste auf die gleiche Farbe wie das Ziel festzulegen. Wenn Sie die Farbe festlegen, entfällt die Notwendigkeit, transparente Bereiche im Bild zu erstellen, und das Zeichnen oder [**ImageList \_ drawex**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) von [**ImageList \_**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) ermöglicht das einfache Kopieren des Bilds in den Zielgeräte Kontext, was zu einer deutlichen Leistungssteigerung führt. Um das Bild zu zeichnen, geben Sie den **\_ normalen ild** -Stil in einem Aufrufen von **ImageList \_ Draw** oder **ImageList \_ drawex** an.

Sie können die Hintergrundfarbe für eine maskierte Bildliste jederzeit so festlegen, dass Sie auf einem beliebigen Solid-Hintergrund ordnungsgemäß gezeichnet wird. Das Festlegen der Hintergrundfarbe auf CLR \_ None bewirkt, dass Bilder standardmäßig transparent gezeichnet werden. Verwenden Sie die Funktion " [**ImageList \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getbkcolor) ", um die Hintergrundfarbe einer Bildliste abzurufen.

Die Stile **ild \_ BLEND25** und **ild \_ BLEND50** weisen das Bild mit der Hervorhebungs Farbe des Systems an. Diese Stile sind nützlich, wenn Sie ein maskiertes Bild verwenden, um ein Objekt darzustellen, das der Benutzer auswählen kann. Beispielsweise können Sie den **ild \_ BLEND50** -Stil zum Zeichnen des Bilds verwenden, wenn der Benutzer es auswählt.

Ein nicht maskiertes Bild wird mithilfe des srccopy-Raster Vorgangs in den Zielgeräte Kontext kopiert. Die Farben im Bild erscheinen unabhängig von der Hintergrundfarbe des Geräte Kontexts identisch. Die in [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) oder [**ImageList \_ drawex**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) angegebenen Zeichnungs Stile haben auch keine Auswirkung auf das Aussehen eines nicht maskierten Bilds.

## <a name="dragging-images"></a>Ziehen von Bildern

Die Win32-API enthält Funktionen zum Ziehen eines Bilds auf dem Bildschirm. Die Zieh Funktionen verschieben ein Bild reibungslos, in Farbe und ohne Blinken des Cursors. Sowohl maskierte als auch unmaskierte Bilder können gezogen werden.

Die [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) -Funktion beginnt einen Zieh Vorgang. Zu den Parametern gehören das Handle für die Bildliste, der Index des zu ziehenden Bilds und der Speicherort des Hotspots innerhalb des Bilds. Der Hotspot ist ein einzelnes Pixel, das von den Zieh Funktionen als exakte Bildschirmposition des Bilds erkannt wird. In der Regel legt eine Anwendung den Hotspot fest, sodass Sie mit dem Hotspot des Mauszeigers übereinstimmt. Mit der [**ImageList \_ DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) -Funktion wird das Bild an einen neuen Speicherort verschoben.

Die Funktion " [**ImageList \_ DragEnter**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragenter) " legt die Anfangsposition des Zieh Bilds innerhalb eines Fensters fest und zeichnet das Bild an der Position. Zu den Parametern gehören das Handle für das Fenster, in dem das Bild und die Koordinaten der Anfangsposition im Fenster gezeichnet werden sollen. Die Koordinaten sind relativ zur linken oberen Ecke des Fensters, nicht zum Client Bereich. Das gleiche gilt für alle Bild Zieh Funktionen, die Koordinaten als Parameter annehmen. Dies bedeutet, dass Sie die Breite der Fensterelemente, wie z. b. Rahmen, Titelleiste und Menüleiste, bei der Angabe der Koordinaten ausgleichen müssen. Wenn Sie beim Aufrufen von **ImageList \_ DragEnter** ein **null** -Fenster Handle angeben, zeichnen die Zieh Funktionen das Bild im Gerätekontext, der dem Desktop Fenster zugeordnet ist, und die Koordinaten sind relativ zur oberen linken Ecke des Bildschirms.

Die [**ImageList \_ SetDragCursorImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setdragcursorimage) -Funktion erstellt ein neues Zieh Bild, indem das angegebene Bild (in der Regel ein Mauszeiger Bild) mit dem aktuellen Zieh Bild kombiniert wird. Da die Zieh Funktionen das neue Bild während eines Zieh Vorgangs verwenden, sollten Sie die [**ShowCursor**](/windows/desktop/api/winuser/nf-winuser-showcursor) -Funktion verwenden, um den eigentlichen Mauszeiger nach dem Aufruf von **ImageList \_ SetDragCursorImage** auszublenden. Andernfalls weist das System möglicherweise zwei Mauszeiger auf die Dauer des Zieh Vorgangs auf.

Wenn eine Anwendung [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag)aufruft, erstellt das System eine temporäre, interne Bildliste und kopiert dann das angegebene Zieh Bild in die interne Liste. Sie können das Handle für die temporäre Drag-Bildliste mit der [**ImageList \_ GetDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getdragimage) -Funktion abrufen. Die-Funktion ruft außerdem die aktuelle Zieh Position und den Offset des Zieh Bilds in Relation zur Zieh Position ab.

## <a name="image-information"></a>Bild Informationen

Es gibt eine Reihe von Funktionen, mit denen Informationen aus einer Bildliste abgerufen werden. Die [**ImageList \_ getimageinfo**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getimageinfo) -Funktion füllt eine [**imageinfo**](/windows/desktop/api) -Struktur mit Informationen zu einem einzelnen Bild, einschließlich der Handles der Bild-und Masken Bitmaps, der Anzahl von Farbebenen und Bits pro Pixel und des umgebenden Rechtecks des Bilds in der Bild Bitmap. Sie können diese Informationen verwenden, um die Bitmaps für das Image direkt zu bearbeiten. Die [**ImageList \_ GetImageCount**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getimagecount) -Funktion Ruft die Anzahl der Bilder in einer Bildliste ab.

## <a name="image-overlays"></a>Bildüberlagerungen

Jede Bildliste enthält eine Liste von Indizes, die als Überlagerungen verwendet werden sollen. Ein Overlay ist ein Bild, das transparent über ein anderes Bild gezeichnet wird. Alle Images, die sich derzeit in der Bildliste befinden, können als Überlagerung verwendet werden. Sie können bis zu vier Überlagerungen pro Bildliste angeben. Diese Beschränkung wurde in Version 4,71 auf 15 erweitert.

Sie fügen den Index eines Bilds der Liste der Überlagerungen hinzu, indem Sie die [**ImageList-Funktion " \_ SetImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) " verwenden und dabei das Handle für die Bildliste, den Index des vorhandenen Bilds und den gewünschten Überlagerungs Index angeben. Dadurch wird der Bildliste in der Tat mitgeteilt, dass das Bild bei Index *x* als Overlay verwendet werden kann, und ich möchte auf das Overlay als Überlagerungs Index *y* verweisen. " Die Überlagerungs Indizes sind einbasiert und NULL basiert, da ein Überlagerungs Index von NULL bedeutet, dass kein Overlay verwendet wird.

Beim Zeichnen eines Bilds mit der Funktion " [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) " oder " [**ImageList \_ drawex**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) " geben Sie ein Overlay an. Die Überlagerung wird durch Ausführen einer logischen **or** -Operation zwischen den gewünschten zeichenflags und dem Ergebnis des [**indexdeoverlaymask**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) -Makros angegeben. Das **INDEXTOOVERLAYMASK** -Makro übernimmt den Überlagerungs Index und formatiert es für die Einbindung in die Flags für diese Funktionen. Dadurch wird das Bild mit dem angegebenen Overlay gezeichnet. Im folgenden Beispiel wird veranschaulicht, wie ein Overlay beim Zeichnen des Bilds hinzugefügt und angegeben wird.


```
ImageList_SetOverlayImage(himl, 0, 3);
ImageList_Draw(himl, 1, hdc, 0, 0, ILD_MASK | INDEXTOOVERLAYMASK(3));
```



Dies zeichnet Bild 1 und überlagert dieses Bild dann mit Bild 0. Da es sich bei 3 um den Überlagerungs Index handelt, den Sie im [**ImageList-Befehl \_ Seto-layimage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) angegeben haben, wird 3 in das [**indexyoverlaymask**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) -Makro eingefügt.

## <a name="32-bit-antialiased-icons"></a>32-Bit-Symbole mit Antialiasing

Antialiasing ist eine Technik zum weich zieren oder verwischen von Spitzen Kanten. Dadurch erhalten Bilder eine natürlichere Darstellung. Bildlisten in Windows Vista und Windows 7 unterstützen die Verwendung von 32-Bit-Symbolen mit Antialiasing und Bitmaps. Farbwerte verwenden 24 Bits, und 8 Bits werden als Alphakanal für die Symbole verwendet. Um eine Bildliste zu erstellen, die ein 32 Bits-pro-Pixel-Bild (BPP) verarbeiten kann, rufen Sie die [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) -Funktion auf, und übergeben Sie ein ILC \_ COLOR32-Flag.

Zum ordnungsgemäßen Erstellen von 32-Bit-Symbolen müssen Sie für jedes Symbol mehrere Bilder erstellen, wie in der folgenden Abbildung dargestellt.

![Abbildung, die drei Größen von Symbolen für jede der drei Farbtiefe anzeigt](images/theme2.png)

-   Die ersten drei Bilder sind im 16-Farben-Modus für die Verwendung im abgesicherten Modus.
-   Die nächsten drei Symbole werden im 256-Farben-Modus verwendet.
-   Die letzten drei Symbole haben den Alpha-Kanal und können nur in Betriebssystemen verwendet werden, auf denen eine 24-Bit-Farbe oder höher ausgeführt wird.
-   Die Reihenfolge der Bilder im Symbol Format ist wichtig. Wenn die Reihenfolge falsch ist, funktionieren ältere Versionen von Windows beim Extrahieren der Symbole schlecht. Das falsche Extrahieren der Symbole kann zu Speicher Beschädigung und fehlerhaftes Rendering führen.
-   In früheren Versionen von Windows gab es ein Ressourcen Limit von 10 Symbolen.

> [!Note]  
> Sie können Tools von Drittanbietern verwenden, um Symbol Dateien und Bitmaps zu generieren, die einen Alphakanal enthalten. Wenn Sie [**LoadImage**](/windows/desktop/api/winuser/nf-winuser-loadimagea) zum Laden einer 32 bpp-Bitmap verwenden, die Alpha enthält, müssen Sie das LR- \_ Flag "kreatedibsection" angeben.

 

 

 