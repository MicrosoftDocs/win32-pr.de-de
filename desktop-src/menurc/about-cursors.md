---
title: Informationen zu Cursorn
description: In diesem Thema werden die Standardcursor erläutert.
ms.assetid: 0ca8e51c-1159-47e9-ba3f-5ced0667cadb
keywords:
- resources,cursors
- cursors,about
- cursors,standard
- Standardcursor
- SetSystemCursor-Funktion
- Cursor, benutzerdefiniert
- Benutzerdefinierte Cursor
- Cursor, Hotspots
- cursors,creating
- Erstellen von Cursorn
- Cursor, Position
- Cursor, Darstellung
- Zerstören von Cursorn
- Duplizieren von Cursorn
- Klassencursor
- Confining-Cursor
- Cursor, zerstörend
- Cursor, duplizierend
- cursors,class
- cursors,confining
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8d987eb12857779ac85d34cb7e4ff7f3f5ce59ed8a750764c433c88abbccea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735404"
---
# <a name="about-cursors"></a>Informationen zu Cursorn

Windows stellt eine Reihe von Standardcursorn bereit, die für jede Anwendung jederzeit verfügbar sind. Die SDK-Headerdateien enthalten Bezeichner für die Standardcursor– die Bezeichner beginnen mit dem **\_ IDC-Präfix.**

Jedem Standardcursor ist ein entsprechendes Standardbild zugewiesen. Der Benutzer oder eine Anwendung kann das Standardbild, das jedem Standardcursor zugeordnet ist, jederzeit ersetzen. Eine Anwendung ersetzt ein Standardimage mithilfe der [**SetSystemCursor-Funktion.**](/windows/desktop/api/Winuser/nf-winuser-setsystemcursor) Die folgende Abbildung zeigt mehrere Standardcursor von Windows Vista:

![Standardcursor, einschließlich Hand, Vierpfeil plus Vorzeichen, Pfeil mit Fragezeichen, Kreis, Stift](images/cursorsstandard.png)

Eine Anwendung kann die [**GetIconInfo-Funktion**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) verwenden, um das aktuelle Bild für einen Cursor abzurufen, und den Cursor mithilfe der [**DrawIconEx-Funktion zeichnen.**](/windows/desktop/api/Winuser/nf-winuser-drawiconex) Um das Standardbild für einen Standardcursor zu zeichnen, geben Sie das **\_ DI-COMPAT-Flag** im Aufruf von **DrawIconEx an.** Wenn Sie das **\_ DI-COMPAT-Flag** nicht angeben, zeichnet **DrawIconEx** den Standardcursor mithilfe des vom Benutzer angegebenen Bilds.

Benutzerdefinierte Cursor sind für die Verwendung in einer bestimmten Anwendung konzipiert und können ein beliebiger Entwurf sein, den der Entwickler definiert. Die folgende Abbildung zeigt mehrere benutzerdefinierte Cursor.

![Benutzerdefinierte Cursor, einschließlich Hand, Banane, Banane, Handuhr, Metronom](images/cursorscustom.png)

Cursor können entweder monofarbig oder farblich sein und entweder statisch oder animiert sein. Der Cursortyp, der auf einem bestimmten Computersystem verwendet wird, hängt von der Anzeige des Systems ab. Alte Displays wie VGA unterstützen keine Farb- oder animierten Cursor. Neue Displays, deren Anzeigetreiber die DIB-Engine (Device-Independent Bitmap) verwenden, unterstützen sie.

Cursor und Symbole sind ähnlich und können in vielen Situationen austauschbar verwendet werden. Der einzige Unterschied zwischen ihnen ist, dass ein als Cursor angegebenes Bild das Format haben muss, das die Anzeige unterstützen kann. Beispielsweise muss ein Cursor für eine VGA-Anzeige monofarbig sein.

Diese Übersicht enthält Informationen zu den folgenden Themen:

-   [The Hot Spot](#the-hot-spot)
-   [Maus und Cursor](#the-mouse-and-the-cursor)
-   [Cursorerstellung](#cursor-creation)
-   [Cursorposition und -darstellung](#cursor-location-and-appearance)
-   [Cursorsperrung](#cursor-confinement)
-   [Cursorvernichtung](#cursor-destruction)
-   [Cursorduplizierung](#cursor-duplication)
-   [Der Window-Klassencursor](#the-window-class-cursor)

## <a name="the-hot-spot"></a>The Hot Spot

Im Cursor markiert ein Pixel namens Hot *Spot* die genaue Bildschirmposition, die von einem Mausereignis betroffen ist, z. B. das Klicken auf eine Maustaste. In der Regel ist der Hotspot der Fokuspunkt des Cursors. Das System verfolgt diesen Punkt und erkennt ihn als Position des Cursors. Typische Hotspots sind beispielsweise das Pixel an der Spitze eines pfeilförmigen Cursors und das Pixel in der Mitte eines übergreifenden Cursors. Die folgenden Abbildungen zeigen zwei Cursor aus einem Zeichnungsprogramm, bei denen Hotspots mit der Spitze des Pinsels und der Kreuzung der Farbe verknüpft sind.

![Hotspots auf zwei Cursorn](images/cursorhotspot.png)

Wenn ein Mauseingabeereignis auftritt, übersetzt der Maustreiber das Ereignis in eine entsprechende Mausnachricht, die die Koordinaten des Hotspots enthält. Das System sendet die Mausnachricht an das Fenster, das den Hotspot enthält, oder an das Fenster, in dem die Mauseingabe erfasst wird. Weitere Informationen finden Sie unter [Mauseingabe.](/windows/desktop/inputdev/mouse-input)

## <a name="the-mouse-and-the-cursor"></a>Maus und Cursor

Das System spiegelt die Bewegung der Maus wider, indem der Cursor auf dem Bildschirm entsprechend bewegt wird. Wenn der Cursor über verschiedene Teile von Fenstern oder in andere Fenster bewegt wird, ändert das System (oder eine Anwendung) die Darstellung des Cursors. Wenn der Cursor z. B. einen Link überkreuzt, ändert das System den Cursor von einem Pfeil in eine Hand.

![Standardcursorwechsel in eine Hand, wenn über einen Link](images/cursorchangingstate.png)

Wenn das System nicht über eine Maus verfügt, wird der Cursor nur angezeigt und bewegt, wenn der Benutzer bestimmte Systembefehle auswählt, z. B. die, die zum Ändern der Größe oder zum Verschieben eines Fensters verwendet werden. Um dem Benutzer eine Methode zum Anzeigen und Bewegen des Cursors zur Verfügung zu stellen, wenn keine Maus verfügbar ist, kann eine Anwendung die Cursorfunktionen verwenden, um Mausbewegungen zu simulieren. Aufgrund dieser Simulationsfunktion kann der Benutzer die Pfeiltasten verwenden, um den Cursor zu verschieben.

## <a name="cursor-creation"></a>Cursorerstellung

Da Standardcursor vordefiniert sind, ist es nicht erforderlich, sie zu erstellen. Um einen Standardcursor zu verwenden, ruft eine Anwendung ein Cursorhandle mithilfe der [**LoadCursor-**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) oder [**LoadImage-Funktion**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) ab. Ein *Cursorhandle* ist ein eindeutiger Wert des **HCURSOR-Typs,** der einen Standardcursor oder einen benutzerdefinierten Cursor identifiziert.

Um einen benutzerdefinierten Cursor für eine Anwendung zu erstellen, verwenden Sie in der Regel eine Grafikanwendung und fügen den Cursor als Ressource in die Ressourcendefinitionsdatei der Anwendung ein. Rufen Sie zur Laufzeit [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) auf, um das Cursorhandle abzurufen. Cursorressourcen enthalten Daten für verschiedene Anzeigegeräte. Die **LoadCursor-Funktion** wählt automatisch die am besten geeigneten Daten für das aktuelle Anzeigegerät aus. So laden Sie einen Cursor direkt aus einem . CUR oder . ANI-Datei, verwenden Sie die [**LoadCursorFromFile-Funktion.**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)

Sie können zur Laufzeit auch einen benutzerdefinierten Cursor erstellen, indem Sie die [**CreateIconIndirect-Funktion**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) verwenden, die einen Cursor basierend auf dem Inhalt einer [**ICONINFO-Struktur**](/windows/desktop/api/Winuser/ns-winuser-iconinfo) erstellt. Die [**GetIconInfo-Funktion**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) füllt diese Struktur mit Hotspotkoordinaten und Informationen zur zugeordneten Maske und Farbe auf.

Anwendungen sollten benutzerdefinierte Cursor als Ressourcen implementieren und [**LoadCursor,**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)oder [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) verwenden, anstatt den Cursor zur Laufzeit zu erstellen. Die Verwendung von Cursorressourcen vermeidet Geräteabhängigkeiten, vereinfacht die Lokalisierung und ermöglicht Anwendungen das Freigeben von Cursorentwürfen.

Mit [**der CreateIconFromResourceEx-Funktion**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex) kann eine Anwendung Symbole und Cursor basierend auf Ressourcendaten erstellen. **CreateIconFromResourceEx** erstellt einen Cursor basierend auf binären Ressourcendaten aus anderen ausführbaren Dateien (.exe) oder DLLs. Ihm müssen Aufrufe der [**LookupIconIdFromDirectoryEx-Funktion**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex) sowie mehrere Ressourcenfunktionen voran stehen. **LookupIconIdFromDirectoryEx** identifiziert die am besten geeigneten Cursordaten für das aktuelle Anzeigegerät. Weitere Informationen zu Ressourcenfunktionen finden Sie unter [Ressourcen](resources.md).

## <a name="cursor-location-and-appearance"></a>Cursorposition und -darstellung

Das System zeigt automatisch einen Cursor für die Maus an und aktualisiert seine Position auf dem Bildschirm. Sie können die aktuellen Bildschirmkoordinaten des Cursors abrufen und den Cursor mithilfe der [**Funktionen GetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos) bzw. [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) an eine beliebige Position auf dem Bildschirm verschieben.

Sie können das Handle auch mithilfe der [**GetCursor-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getcursor) an den aktuellen Cursor abrufen, und Sie können den Cursor mithilfe der [**SetCursor-Funktion**](/windows/desktop/api/Winuser/nf-winuser-setcursor) festlegen. Nachdem Sie **SetCursor aufrufen,** ändert sich die Darstellung des Cursors erst, wenn sich der Mauszeiger bewegt, der Cursor explizit auf einen anderen Cursor festgelegt oder ein Systembefehl ausgeführt wird.

Wenn der Benutzer die Maus bewegt, wird der Cursor vom System an der neuen Position neu gedraht. Das System erstellt den Cursorentwurf, der dem Fenster zugeordnet ist, auf das der Cursor zeigt, automatisch neu.

Sie können den Cursor mithilfe der [**ShowCursor-Funktion**](/windows/desktop/api/Winuser/nf-winuser-showcursor) ausblenden und erneut anzeigen, ohne den Cursorentwurf zu ändern. Diese Funktion verwendet einen internen Zähler, um zu bestimmen, wann der Cursor aus- oder angezeigt werden soll. Beim Versuch, den Cursor zu zeigen, wird der Zähler inkrementiert. Ein Versuch, den Cursor auszublenden, dekrementiert den Zähler. Der Cursor ist nur sichtbar, wenn dieser Indikator größer oder gleich 0 (null) ist.

Die [**GetCursorInfo-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getcursorinfo) ruft die folgenden Informationen für den globalen Cursor ab: ob der Cursor ausgeblendet oder angezeigt wird, das Handle für den Cursor und die Koordinaten des Cursors.

## <a name="cursor-confinement"></a>Cursoreingrenzung

Sie können den Cursor auf einen rechteckigen Bereich auf dem Bildschirm beschränken, indem Sie die [**ClipCursor-Funktion**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) verwenden. Dies ist nützlich, wenn der Benutzer auf ein bestimmtes Ereignis innerhalb des eingeschränkten Bereichs des Rechtecks reagieren muss. Beispielsweise können Sie **ClipCursor** verwenden, um den Cursor auf ein modales Dialogfeld zu beschränken, wodurch verhindert wird, dass der Benutzer mit anderen Fenstern interagiert, bis das Dialogfeld geschlossen wird.

Die [**GetClipCursor-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getclipcursor) ruft die Bildschirmkoordinaten des rechteckigen Bereichs ab, auf den der Cursor vorübergehend beschränkt ist. Wenn der Cursor eingeschränkt werden muss, können Sie diese Funktion auch verwenden, um die Koordinaten des ursprünglichen Bereichs zu speichern, in dem sich der Cursor bewegen kann. Anschließend können Sie den Cursor im ursprünglichen Bereich wiederherstellen, wenn die neue Eingrenzung nicht mehr erforderlich ist.

## <a name="cursor-destruction"></a>Cursorvernichtung

Sie können das Cursorhandle zerstören und den Vom Cursor verwendeten Arbeitsspeicher freigeben, indem Sie die [**DestroyCursor-Funktion**](/windows/desktop/api/Winuser/nf-winuser-destroycursor) aufrufen. Diese Funktion hat jedoch keine Auswirkungen auf einen freigegebenen Cursor. Ein freigegebener Cursor ist gültig, solange das Modul, aus dem er geladen wurde, im Arbeitsspeicher verbleibt. Die folgenden Funktionen rufen einen freigegebenen Cursor ab:

-   [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)
-   [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)
-   [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) (bei Verwendung des **LR \_ SHARED-Flags)**
-   [**CopyImage**](/windows/desktop/api/Winuser/nf-winuser-copyimage) (wenn Sie das **LR \_ COPYRETURNORG-Flag** verwenden und *hImage* ein freigegebener Cursor ist)

Wenn Sie keinen Cursor mehr benötigen, den Sie mit der [**CreateIconIndirect-Funktion**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) erstellt haben, sollten Sie den Cursor zerstören. Die [**DestroyIcon-Funktion**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) zerstört das Cursorhandle und gibt den vom Cursor verwendeten Arbeitsspeicher frei. Verwenden Sie diese Funktion nur für Cursor, die mit **CreateIconIndirect** erstellt wurden.

## <a name="cursor-duplication"></a>Cursorduplizierung

Die [**CopyCursor-Funktion**](/windows/desktop/api/Winuser/nf-winuser-copycursor) kopiert ein Cursorhandle. Dadurch kann Anwendungs- oder DLL-Code das Handle zu einem Cursor abrufen, der sich im Besitz eines anderen Moduls befindet. Wenn das andere Modul freigegeben wird, kann das Modul, das den Cursor kopiert hat, weiterhin den Cursorentwurf verwenden.

Informationen zum Hinzufügen, Entfernen oder Ersetzen von Cursorressourcen in ausführbaren Dateien finden Sie unter [Ressourcen](resources.md).

## <a name="the-window-class-cursor"></a>Der Window-Klassencursor

Wenn Sie eine Fensterklasse mithilfe der [**RegisterClass-Funktion**](/windows/desktop/api/winuser/nf-winuser-registerclassa) registrieren, können Sie ihr einen Standardcursor zuweisen, der als *Klassencursor* bezeichnet wird. Nachdem die Anwendung die Fensterklasse registriert hat, verfügt jedes Fenster dieser Klasse über den angegebenen Klassencursor.

Um den Klassencursor zu überschreiben, verarbeiten Sie die [**WM \_ SETCURSOR-Meldung.**](wm-setcursor.md) Sie können einen Klassencursor auch mithilfe der [**SetClassLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) ersetzen. Diese Funktion ändert die Standardfenstereinstellungen für alle Fenster einer angegebenen Klasse. Weitere Informationen finden Sie unter [Klassencursor.](/windows/desktop/winmsg/about-window-classes)

 

 