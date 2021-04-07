---
title: Informationen über Cursor
description: In diesem Thema werden die standardcursorn erläutert.
ms.assetid: 0ca8e51c-1159-47e9-ba3f-5ced0667cadb
keywords:
- Ressourcen, Cursor
- Cursor, Info
- Cursor, Standard
- Standard Cursor
- Setsystemcursor-Funktion
- Cursor, Benutzer definiert
- benutzerdefinierte Cursor
- Cursor, Hotspots
- Cursor, erstellen
- Erstellen von Cursors
- Cursor, Speicherort
- Cursor, Darstellung
- zerstören von Cursors
- Duplizieren von Cursors
- Klassen Cursor
- Einschränken von Cursorn
- Cursor, zerstören
- Cursor, duplizieren
- Cursor, Klasse
- Cursor, einschränken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2d0b91ba4670d2510413240efd742b2e0ba69b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038945"
---
# <a name="about-cursors"></a>Informationen über Cursor

Windows stellt eine Reihe von standardcursorn bereit, die für jede beliebige Anwendung jederzeit verfügbar sind. Die SDK-Header Dateien enthalten Bezeichner für die standardcursorn – die IDs beginnen mit dem **IDC \_** -Präfix.

Jedem Standardcursor ist ein entsprechendes Standardbild zugewiesen. Der Benutzer oder eine Anwendung kann das Standard Image, das einem beliebigen Standard Cursor zugeordnet ist, jederzeit ersetzen. Eine Anwendung ersetzt mithilfe der [**setsystemcursor**](/windows/desktop/api/Winuser/nf-winuser-setsystemcursor) -Funktion ein Standard Image. Die folgende Abbildung zeigt mehrere standardcursorn von Windows Vista:

![Standard Cursor, einschließlich Hand, vier Pfeil-Pluszeichen, Pfeil mit Fragezeichen, Kreis, Stift](images/cursorsstandard.png)

Eine Anwendung kann mit der [**getieninfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) -Funktion das aktuelle Bild für einen Cursor abrufen und den Cursor mithilfe der [**drawienex**](/windows/desktop/api/Winuser/nf-winuser-drawiconex) -Funktion zeichnen. Um das Standardbild für einen Standard Cursor zu zeichnen, geben Sie das **di- \_ compat** -Flag im Befehl **drawimex** an. Wenn Sie das **di- \_ compat** -Flag nicht angeben, zeichnet **drawienex** den Standard Cursor mithilfe des vom Benutzer angegebenen Bilds.

Benutzerdefinierte Cursor sind für die Verwendung in einer bestimmten Anwendung konzipiert und können von einem beliebigen Design des Entwicklers definiert werden. In der folgenden Abbildung werden mehrere benutzerdefinierte Cursor gezeigt.

![benutzerdefinierte Cursorn, einschließlich Hand, Banane, Trommel, armpuhr an Hand, Metronome](images/cursorscustom.png)

Cursor können entweder Monochrom oder Farben und entweder statisch oder animiert sein. Der Cursor, der auf einem bestimmten Computersystem verwendet wird, hängt von der Anzeige des Systems ab. Alte anzeigen, wie z. b. VGA, unterstützen keine Farben oder animierten Cursor. Neue anzeigen, deren Anzeigetreiber die geräteunabhängige Bitmap-Engine (DIB) verwenden, unterstützen diese.

Cursor und Symbole sind ähnlich und können in vielen Situationen austauschbar verwendet werden. Der einzige Unterschied besteht darin, dass ein als Cursor festgelegtes Bild das Format aufweisen muss, das von der Anzeige unterstützt werden kann. Beispielsweise muss ein Cursor für eine VGA-Anzeige monochrom sein.

Diese Übersicht enthält Informationen zu den folgenden Themen:

-   [Der Hotspot](#the-hot-spot)
-   [Die Maus und der Cursor](#the-mouse-and-the-cursor)
-   [Cursor Erstellung](#cursor-creation)
-   [Cursor Position und-Darstellung](#cursor-location-and-appearance)
-   [Cursor Sperre](#cursor-confinement)
-   [Cursor Zerstörung](#cursor-destruction)
-   [Cursor Duplizierung](#cursor-duplication)
-   [Der Fenster Klassen Cursor](#the-window-class-cursor)

## <a name="the-hot-spot"></a>Der Hotspot

Im Cursor kennzeichnet ein Pixel, das als *Hot-Spot* bezeichnet wird, die exakte Bildschirmposition, die von einem Maus Ereignis betroffen ist, z. b. das Klicken auf eine Maustaste. In der Regel ist der Hotspot der Fokuspunkt des Cursors. Das System verfolgt diesen Punkt als Position des Cursors und erkennt diesen. Typische Hotspots sind z. b. das Pixel an der Spitze eines pfeilförmigen Cursors und das Pixel in der Mitte eines kreuzförmigen Cursors. Die folgenden Bilder zeigen zwei Cursor aus einem Zeichnungsprogramm, in denen Hotspots mit dem Tipp des Pinsels verknüpft sind, und der Faden Strich der Farbe.

![Hotspots auf zwei Cursorn](images/cursorhotspot.png)

Wenn ein Mauseingabe Ereignis auftritt, übersetzt der Maustreiber das Ereignis in eine entsprechende Maus Nachricht, die die Koordinaten des Hotspots enthält. Das System sendet die Maus Nachricht an das Fenster, das den Hotspot enthält, oder an das Fenster, das die Maus Eingaben erfasst. Weitere Informationen finden Sie unter [Maus Eingaben](/windows/desktop/inputdev/mouse-input).

## <a name="the-mouse-and-the-cursor"></a>Die Maus und der Cursor

Das System spiegelt die Bewegung der Maus wider, indem der Cursor auf dem Bildschirm entsprechend bewegt wird. Wenn der Cursor über verschiedene Teile von Windows oder in verschiedene Fenster bewegt wird, ändert das System (oder eine Anwendung) die Darstellung des Cursors. Wenn der Cursor z. b. einen Hyperlink überschreitet, ändert das System den Cursor von einem Pfeil in eine Hand.

![Standard Cursor, der sich über einen Link in eine Hand ändert](images/cursorchangingstate.png)

Wenn das System nicht über eine Maus verfügt, wird der Cursor nur angezeigt und verschoben, wenn der Benutzer bestimmte Systembefehle auswählt, z. b. diejenigen, die zum Anpassen oder Verschieben eines Fensters verwendet werden. Um dem Benutzer die Möglichkeit zu geben, den Cursor anzuzeigen und zu verschieben, wenn eine Maus nicht verfügbar ist, kann eine Anwendung die Cursor Funktionen verwenden, um die Mausbewegung zu simulieren. Mit dieser Simulationsfunktion kann der Benutzer die Pfeiltasten verwenden, um den Cursor zu verschieben.

## <a name="cursor-creation"></a>Cursor Erstellung

Da standardcursorn vordefiniert sind, ist es nicht notwendig, Sie zu erstellen. Um einen Standard Cursor zu verwenden, ruft eine Anwendung mithilfe der [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) -oder [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) -Funktion ein Cursor Handle ab. Ein *Cursor Handle* ist ein eindeutiger Wert des **hcursor** -Typs, der einen Standard-oder einen benutzerdefinierten Cursor identifiziert.

Wenn Sie einen benutzerdefinierten Cursor für eine Anwendung erstellen möchten, verwenden Sie in der Regel eine Grafikanwendung, und fügen Sie den Cursor als Ressource in die Ressourcen Definitionsdatei der Anwendung ein. Rufen Sie zur Laufzeit [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) auf, um das Cursor Handle abzurufen. Cursor Ressourcen enthalten Daten für verschiedene Anzeigegeräte. Die **LoadCursor** -Funktion wählt automatisch die am besten geeigneten Daten für das aktuelle Anzeigegerät aus. , Wenn ein Cursor direkt aus einem geladen werden soll. Cur oder. ANI-Datei, verwenden Sie die [**loadcurrsorfromfile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea) -Funktion.

Sie können auch zur Laufzeit einen benutzerdefinierten Cursor erstellen, indem Sie die Funktion " [**comateideindirekt**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) " verwenden, die einen Cursor basierend auf dem Inhalt einer [**iconinfo**](/windows/desktop/api/Winuser/ns-winuser-iconinfo) -Struktur erstellt. Die Funktion [**getieninfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) füllt diese Struktur mit Hotspot-Koordinaten und Informationen zur zugeordneten Maske und Farbe aus.

Anwendungen sollten benutzerdefinierte Cursor als Ressourcen implementieren und [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora), [**loadcursorfromfile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)oder [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) verwenden, anstatt den Cursor zur Laufzeit zu erstellen. Die Verwendung von Cursor Ressourcen vermeidet Geräte Abhängigkeit, vereinfacht die Lokalisierung und ermöglicht Anwendungen das Freigeben von Cursor Entwürfen.

Mit [**der Funktion**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex) "" von "" kann eine Anwendung Symbole und Cursor auf der Grundlage von Ressourcen Daten erstellen. " **Kreateidefromresourceex** " erstellt einen Cursor, der auf binären Ressourcen Daten aus anderen ausführbaren Dateien oder DLLs basiert. Ihm müssen Aufrufe an die [**lookupiinidfromdirectoryex**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex) -Funktion sowie mehrere Ressourcen Funktionen vorangestellt werden. **Lookupienidfromdirectoriyex** identifiziert die am besten geeigneten Cursor Daten für das aktuelle Anzeigegerät. Weitere Informationen zu Ressourcen Funktionen finden Sie unter [Ressourcen](resources.md).

## <a name="cursor-location-and-appearance"></a>Cursor Position und-Darstellung

Das System zeigt automatisch einen Cursor für die Maus an und aktualisiert seine Position auf dem Bildschirm. Sie können die aktuellen Bildschirm Koordinaten des Cursors abrufen und den Cursor an eine beliebige Position auf dem Bildschirm bewegen, indem Sie die Funktionen [**GetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos) bzw. [**setcursorpos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) verwenden.

Sie können auch das Handle für den aktuellen Cursor abrufen, indem Sie die [**GetCursor**](/windows/desktop/api/Winuser/nf-winuser-getcursor) -Funktion verwenden, und Sie können den Cursor mithilfe der [**SetCursor**](/windows/desktop/api/Winuser/nf-winuser-setcursor) -Funktion festlegen. Nachdem Sie **SetCursor** aufgerufen haben, ändert sich die Darstellung des Cursors nicht, bis entweder die Maus bewegt wird, der Cursor explizit auf einen anderen Cursor festgelegt ist oder ein Systembefehl ausgeführt wird.

Wenn der Benutzer die Maus bewegt, zeichnet das System den Cursor am neuen Speicherort neu. Das System zeichnet den Cursor Entwurf, der dem Fenster zugeordnet ist, auf das der Cursor zeigt, automatisch neu.

Sie können den Cursor ausblenden und erneut anzeigen, ohne den Cursor Entwurf zu ändern, indem Sie die [**ShowCursor**](/windows/desktop/api/Winuser/nf-winuser-showcursor) -Funktion verwenden. Diese Funktion verwendet einen internen-Counter, um zu bestimmen, wann der Cursor ausgeblendet oder angezeigt werden soll. Der Versuch, den Cursor anzuzeigen, erhöht den-Wert. der Versuch, den Cursor auszublenden, verringert den-Wert. Der Cursor ist nur sichtbar, wenn dieser Wert größer oder gleich 0 (null) ist.

Die [**GetCursorInfo**](/windows/desktop/api/Winuser/nf-winuser-getcursorinfo) -Funktion Ruft die folgenden Informationen für den globalen Cursor ab: ob der Cursor ausgeblendet oder angezeigt wird, das Handle für den Cursor und die Koordinaten des Cursors.

## <a name="cursor-confinement"></a>Cursor Sperre

Sie können den Cursor auf einen rechteckigen Bereich auf dem Bildschirm beschränken, indem Sie die [**clipcursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) -Funktion verwenden. Dies ist hilfreich, wenn der Benutzer auf ein bestimmtes Ereignis innerhalb des beschränkten Bereichs des Rechtecks Antworten muss. Sie können z. b. **clipcursor** verwenden, um den Cursor auf ein modales Dialogfeld zu beschränken, wodurch verhindert wird, dass der Benutzer mit anderen Fenstern interagiert, bis das Dialogfeld geschlossen wird.

Die [**getclipcursor**](/windows/desktop/api/Winuser/nf-winuser-getclipcursor) -Funktion Ruft die Bildschirm Koordinaten des rechteckigen Bereichs ab, in den der Cursor temporär eingeschränkt ist. Wenn es erforderlich ist, den Cursor einzuschränken, können Sie diese Funktion auch verwenden, um die Koordinaten des ursprünglichen Bereichs zu speichern, in dem der Cursor verschoben werden kann. Anschließend können Sie den Cursor im ursprünglichen Bereich wiederherstellen, wenn die neue Einschließung nicht mehr erforderlich ist.

## <a name="cursor-destruction"></a>Cursor Zerstörung

Sie können das Cursor Handle zerstören und den von dem Cursor verwendeten Arbeitsspeicher freigeben, indem Sie die [**destroycursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor) -Funktion aufrufen. Diese Funktion hat jedoch keine Auswirkung auf einen freigegebenen Cursor. Ein frei gegebener Cursor ist gültig, solange das Modul, von dem es geladen wurde, im Arbeitsspeicher verbleibt. Die folgenden Funktionen erhalten einen freigegebenen Cursor:

-   [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)
-   [**LoadCursor FromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)
-   [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) (bei Verwendung des LR-Flags **\_ Shared** )
-   [**CopyImage**](/windows/desktop/api/Winuser/nf-winuser-copyimage) (wenn Sie das **LR \_ copyrückkehrer** -Flag verwenden und das *himage* ein gemeinsam genutzter Cursor ist)

Wenn Sie einen Cursor nicht mehr benötigen, den Sie mit der Funktion "" in der Funktion "" erstellt haben, sollten [**Sie den Cursor**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) zerstören. Die [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) -Funktion zerstört das Cursor Handle und gibt den vom Cursor verwendeten Arbeitsspeicher frei. Verwenden Sie diese Funktion nur bei Cursorn, **die mit "**" erstellt wurden.

## <a name="cursor-duplication"></a>Cursor Duplizierung

Die [**copycursor**](/windows/desktop/api/Winuser/nf-winuser-copycursor) -Funktion kopiert ein Cursor handle. Dies ermöglicht es dem Anwendungs-oder DLL-Code, das Handle für einen Cursor abzurufen, dessen Besitzer ein anderes Modul ist. Wenn das andere Modul freigegeben wird, kann das Modul, das den Cursor kopiert hat, den Cursor Entwurf weiterhin verwenden.

Informationen zum Hinzufügen, entfernen oder Ersetzen von Cursor Ressourcen in ausführbaren Dateien finden Sie unter [Ressourcen](resources.md).

## <a name="the-window-class-cursor"></a>Der Fenster Klassen Cursor

Wenn Sie eine Fenster Klasse mithilfe der [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) -Funktion registrieren, können Sie Ihr einen Standard Cursor zuweisen, der als *Klassen Cursor* bezeichnet wird. Nachdem die Anwendung die Fenster Klasse registriert hat, verfügt jedes Fenster dieser Klasse über den angegebenen Klassen Cursor.

Um den Klassen Cursor zu überschreiben, verarbeiten Sie die [**WM- \_ SetCursor**](wm-setcursor.md) -Nachricht. Sie können auch einen Klassen Cursor ersetzen, indem Sie die [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) -Funktion verwenden. Diese Funktion ändert die Standardfenster Einstellungen für alle Fenster einer angegebenen Klasse. Weitere Informationen finden Sie unter [Class Cursor](/windows/desktop/winmsg/about-window-classes).

 

 