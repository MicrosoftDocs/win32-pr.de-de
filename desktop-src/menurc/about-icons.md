---
title: Informationen zu Symbolen
description: In diesem Thema werden Symbole erläutert.
ms.assetid: 67867460-07f6-460f-9263-05bbf3474744
keywords:
- Ressourcen, Symbole
- Symbole, Hotspots
- Symbole, Standard
- Standardsymbole
- Symbole, Benutzer definiert
- benutzerdefinierte Symbole
- Symbole, Größen
- Erstellen von Symbolen
- Symbole, anzeigen
- Symbole, zerstören
- Symbole, duplizieren
- Symbole, erstellen
- Anzeigen von Symbolen
- zerstören von Symbolen
- Duplizieren von Symbolen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bda00540d613b6d0efd4a080251ebd6407560ed
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315003"
---
# <a name="about-icons"></a>Informationen zu Symbolen

Das System verwendet Symbole in der gesamten Benutzeroberfläche, um Objekte wie Dateien, Ordner, Verknüpfungen, Anwendungen und Dokumente darzustellen. Mit den Symbol Funktionen können Anwendungen Symbole erstellen, laden, anzeigen, anordnen, animieren und zerstören. Weitere Informationen zum Angeben von Symbolen für Dateitypen finden Sie unter [**ExtractIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extracticona).

Diese Übersicht enthält Informationen zu den folgenden Themen:

-   [Symbol "Hotspot"](#icon-hot-spot)
-   [Symboltypen](#icon-types)
-   [Symbolgrößen](#icon-sizes)
    -   [So ändern Sie die Größe des kleinen System Symbols](#to-change-the-size-of-the-system-small-icon)
    -   [So rufen Sie die Größe des kleinen System Symbols ab](#to-retrieve-the-size-of-the-system-small-icon)
    -   [So rufen Sie die Größe des großen System Symbols ab](#to-retrieve-the-size-of-the-system-large-icon)
    -   [So rufen Sie die Größe des Symbols "Small Shell Small" ab](#to-retrieve-the-size-of-the-shell-small-icon)
    -   [So ändern Sie die Größe des großen Symbols](#to-change-the-size-of-the-large-icon)
    -   [So rufen Sie die Größe des Symbols für große Shell ab](#to-retrieve-the-size-of-the-shell-large-icon)
-   [Symbol Erstellung](#icon-creation)
-   [Symbol Anzeige](#icon-display)
-   [Symbol Zerstörung](#icon-destruction)
-   [Symbol Duplizierung](#icon-duplication)

## <a name="icon-hot-spot"></a>Symbol "Hotspot"

Einer der Pixel in einem Symbol wird als [Hot-Spot](#icon-hot-spot)festgelegt. Dies ist der Punkt, den das System nachverfolgt und als Position des Symbols erkennt. Der Hotspot eines Symbols ist in der Regel das Pixel in der Mitte des Symbols. Wenn Sie zum Erstellen eines Symbols die Funktion " [**kreateienindirekte**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) " verwenden, können Sie ein beliebiges Pixel als Hotspot angeben.

## <a name="icon-types"></a>Symboltypen

Das Betriebssystem stellt eine Reihe von *Standardsymbolen* bereit, die für jede beliebige Anwendung jederzeit verfügbar sind. Die Software Development Kit-Header Dateien (SDK) enthalten Bezeichner für die Standardsymbole – die IDs beginnen mit dem **IDI \_** -Präfix.

Jedem Standard Symbol ist ein entsprechendes Standardbild zugeordnet. Der Benutzer kann das Standard Image, das einem beliebigen Standard Cursor zugeordnet ist, jederzeit ersetzen.

*Benutzerdefinierte Symbole* sind für die Verwendung in einer bestimmten Anwendung konzipiert und können ein beliebiger Entwurf sein. Im folgenden sind mehrere benutzerdefinierte Symbole dargestellt.

![mehrere benutzerdefinierte Symbole](images/csicn-02.png)

## <a name="icon-sizes"></a>Symbolgrößen

Das System verwendet vier Symbolgrößen:

-   System klein
-   System groß
-   Shell klein
-   Shell (groß)

Das *kleine System Symbol* wird in der Fenster Beschriftung angezeigt.

### <a name="to-change-the-size-of-the-system-small-icon"></a>So ändern Sie die Größe des kleinen System Symbols

1.  Klicken Sie in der Systemsteuerung auf anzeigen, und klicken Sie dann **auf die Register** Karte **Darstellung**.
2.  Wählen **Sie** Untertitel Schaltflächen aus der Liste **Element** aus, und legen Sie dann das **Größen** Feld

### <a name="to-retrieve-the-size-of-the-system-small-icon"></a>So rufen Sie die Größe des kleinen System Symbols ab

-   Aufrufen der [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) -Funktion mit **SM \_ cxsmicon** und **SM \_ cysmicon**.

Das *Symbol "großes System* " wird hauptsächlich von Anwendungen verwendet, es wird jedoch auch im Dialogfeld "Alt + Tab" angezeigt. Die Funktionen " [**kreateikonfromresource**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresource)", " [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon)", " [**ExtractAssociatedIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extractassociatedicona)", " [**ExtractIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extracticona)", " [**extractireex**](/windows/desktop/api/Shellapi/nf-shellapi-extracticonexa)" und " [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) " verwenden alle System große Symbole. Die Größe des Symbols für das große System wird vom Videotreiber definiert und kann daher nicht geändert werden.

### <a name="to-retrieve-the-size-of-the-system-large-icon"></a>So rufen Sie die Größe des großen System Symbols ab

-   [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) mit **SM \_ cxicon** und **SM \_ cyicon** aufrufen.

Die Funktionen "| [**ateicon**](/windows/desktop/api/Winuser/nf-winuser-createicon) [**", "", "**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex)", "", "", "", "", " [**", "**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect)", "", "", "", "" und " [**shgetfileinfo**](/windows/win32/api/shellapi/nf-shellapi-shgetfileinfoa) " können für

Das *Symbol "Shell Small* " wird im Windows-Explorer und in den allgemeinen Dialogfeldern verwendet. Derzeit wird standardmäßig die Größe des Systems kleiner.

### <a name="to-retrieve-the-size-of-the-shell-small-icon"></a>So rufen Sie die Größe des Symbols "Small Shell Small" ab

1.  Verwenden Sie die [shgetfilinput FO](/windows/win32/api/shellapi/nf-shellapi-shgetfileinfoa) -Funktion mit `SHGFI_SHELLICONSIZE | SHGFI_SMALLICON` , um ein Handle für die System Abbild Liste abzurufen.
2.  Anschließend können Sie die Funktion " [**ImageList \_ getikonsistze**](/windows/win32/api/commctrl/nf-commctrl-imagelist_geticonsize) " aufrufen, um die Symbolgröße abzurufen.

Das Shell Large-Symbol wird auf dem Desktop verwendet.

### <a name="to-change-the-size-of-the-large-icon"></a>So ändern Sie die Größe des großen Symbols

1.  Klicken Sie in der Systemsteuerung auf anzeigen, und klicken Sie dann **auf die Register** Karte **Darstellung**.
2.  Wählen Sie in der Liste **Element** das **Symbol** aus, und legen Sie dann das Feld **Größe** fest (diese Größe wird in der Registrierung gespeichert, und zwar unter **HKEY \_ Current \_ User \\ Control Panel, Desktop \\ WindowMetrics \\ Shell Icon size**).
3.  Klicken Sie auf das **plus!** , und aktivieren Sie dann das Kontrollkästchen **große Symbole verwenden** .

### <a name="to-retrieve-the-size-of-the-shell-large-icon"></a>So rufen Sie die Größe des Symbols für große Shell ab

1.  Verwenden Sie die [**shgetfilinput FO**](/windows/win32/api/shellapi/nf-shellapi-shgetfileinfoa) -Funktion mit **shgfi \_ shelliconsize** , um ein Handle für die System Abbild Liste abzurufen.
2.  Anschließend können Sie die Funktion " [**ImageList \_ getikonsistze**](/windows/win32/api/commctrl/nf-commctrl-imagelist_geticonsize) " aufrufen, um die Symbolgröße abzurufen.

Das Startmenü verwendet entweder Shell Small-Symbole oder große shellsymbole, je nachdem, ob das Kontrollkästchen **große Symbole verwenden** aktiviert ist.

Die Anwendung sollte Gruppen von Symbolbildern in folgenden Größen bereitstellen:

-   48x48, 256 Farbe
-   32x32, 16 Farben
-   16x16 Pixel, 16 Farben

Wenn Sie die [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur ausfüllen, die beim Registrieren der Fenster Klasse verwendet werden soll, legen Sie den **HICON** -Member auf das Symbol 32x32 und das **hikonsm** -Element auf das 16x16-Symbol fest. Weitere Informationen zu Klassen Symbolen finden Sie unter [Klassen Symbole](/windows/desktop/winmsg/about-window-classes).

## <a name="icon-creation"></a>Symbol Erstellung

Standard Symbole sind vordefiniert, sodass es nicht notwendig ist, Sie zu erstellen. Um ein Standard Symbol zu verwenden, kann eine Anwendung das Handle mithilfe der [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) -Funktion abrufen. Ein *Symbol Handle* ist ein eindeutiger Wert des **HICON** -Typs, der ein Standard Symbol oder ein benutzerdefiniertes Symbol identifiziert.

Wenn Sie ein benutzerdefiniertes Symbol für eine Anwendung erstellen möchten, verwenden Sie in der Regel eine Grafikanwendung, und fügen Sie die [Symbol Ressource](./icon-resource.md) in die Ressourcen Definitionsdatei der Anwendung ein. Zur Laufzeit können Sie [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) oder [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) aufrufen, um ein Handle für das Symbol abzurufen. Eine Symbol Ressource kann eine Gruppe von Bildern für verschiedene Anzeigegeräte enthalten. " **LoadIcon** " und " **LoadImage** " wählen automatisch das am besten geeignete Symbol aus der Gruppe für das aktuelle Anzeigegerät aus.

Eine Anwendung kann auch zur Laufzeit ein benutzerdefiniertes Symbol erstellen, indem Sie die Funktion " [**comateideindirekt**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) " verwendet, die ein Symbol basierend auf dem Inhalt einer [**iconinfo**](/windows/desktop/api/Winuser/ns-winuser-iconinfo) -Struktur erstellt. Die [**getieninfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) -Funktion füllt die-Struktur mit den Hot-Spot-Koordinaten und Informationen über die Bitmap-und Farb Bitmap der Bitmaske für das Symbol auf.

Anwendungen sollten benutzerdefinierte Symbole als Ressourcen implementieren und [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) oder [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea)verwenden, anstatt das Symbol zur Laufzeit zu erstellen. Die Verwendung von Symbol Ressourcen vermeidet Geräte Abhängigkeit, vereinfacht die Lokalisierung und ermöglicht Anwendungen das Freigeben von Symbol Formen.

Die Funktion [**createienfromresourceex**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex) ermöglicht einer Anwendung, die Ressourcen des Systems zu durchsuchen und Symbole und Cursor auf der Grundlage von Ressourcen Daten zu erstellen. " **Kreateidefromresourceex** " erstellt ein Symbol, das auf binären Ressourcen Daten aus anderen ausführbaren Dateien oder DLLs basiert. Eine Anwendung muss dieser Funktion mit Aufrufen der [**lookupiinidfromdirectoryex**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex) -Funktion und mehrerer der Ressourcen Funktionen vorangestellt sein. **Lookupienidfromdirector yex** gibt den Bezeichner der am besten geeigneten Symbol Daten für das aktuelle Anzeigegerät zurück.

## <a name="icon-display"></a>Symbol Anzeige

Sie können das Bild für ein Symbol mithilfe der Funktion [**getieninfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) abrufen und mithilfe der [**drawienex**](/windows/desktop/api/Winuser/nf-winuser-drawiconex) -Funktion zeichnen. Um das Standardbild für ein Symbol zu zeichnen, geben Sie das **di- \_ compat** -Flag im Befehl **drawimex** an. Wenn Sie das **di- \_ compat** -Flag nicht angeben, zeichnet **drawimex** das Symbol mithilfe des vom Benutzer angegebenen Bilds.

Wenn das System ein Symbol anzeigt, muss es das entsprechende Symbolbild aus der exe-oder DLL-Datei extrahieren. Das System verwendet die folgenden Schritte, um das Symbol Image auszuwählen:

1.  Wählen Sie die **RT- \_ Gruppen \_ Symbol** Ressource aus. Wenn mehr als eine solche Ressource vorhanden ist, verwendet das System die erste Ressource, die in der ressourcenscrip aufgeführt ist.
2.  Wählen Sie das entsprechende **RT- \_ Symbol** Bild aus der **RT- \_ Gruppen \_ Symbol** Ressource aus. Wenn mehr als ein Abbild vorhanden ist, verwendet das System die folgenden Kriterien, um ein Image auszuwählen:
    -   -   Das Bild, das der Größe der angeforderten Größe am nächsten ist, wird ausgewählt.
        -   Wenn mindestens zwei Bilder dieser Größe vorhanden sind, wird der Wert, der mit der Farbtiefe der Anzeige übereinstimmt, ausgewählt.
        -   Wenn keine Bilder genau mit der Farbtiefe der Anzeige übereinstimmen, wird das Bild mit der größten Farbtiefe ausgewählt, die die Farbtiefe der Anzeige nicht überschreitet. Wenn alle die Farbtiefe überschreiten, wird der Wert mit der niedrigsten Farbtiefe ausgewählt.

> [!Note]  
> Das System behandelt alle Farbtiefe von 8 oder mehr bpp als gleich. Aus diesem Grund besteht kein Vorteil darin, ein 16x16-Bild mit 256-farbiger Farbe und ein 16x16-16-farbiges Bild in derselben Ressource einzuschließen – das System wählt einfach nur das erste aus. Wenn sich die Anzeige im 8-bpp-Modus befindet, wählt das System ein 16-farbiges Symbol über einem 256-Farben-Symbol und zeigt alle Symbole mit der Standardpalette des Systems an.

 

Verwenden Sie zum Anzeigen eines animierten Symbols ein statisches-Steuerelement, wie im folgenden Code Fragment gezeigt.


```
hIcon = LoadImage(NULL, "ico.ani", IMAGE_ICON, 0, 0, LR_LOADFROMFILE);
SendMessage( hStatic, STM_SETIMAGE, IMAGE_ICON, (LPARAM)(UINT)hIcon);
```



## <a name="icon-destruction"></a>Symbol Zerstörung

Wenn eine Anwendung kein Symbol mehr benötigt [**, das Sie mithilfe der Funktion "**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) " in der Funktion "" erstellt hat, sollte Sie das Symbol zerstören. Die [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) -Funktion zerstört das Symbol Handle und gibt den vom Symbol verwendeten Arbeitsspeicher frei. Anwendungen sollten diese Funktion nur für Symbole **verwenden, die** mit "" erstellt werden. andere Symbole müssen nicht zerstört werden.

## <a name="icon-duplication"></a>Symbol Duplizierung

Die [**copyicon**](/windows/desktop/api/Winuser/nf-winuser-copyicon) -Funktion kopiert ein Symbol handle. Dadurch kann eine Anwendung oder dll ein eigenes Handle für ein Symbol erhalten, das im Besitz eines anderen Moduls ist. Wenn das andere Modul freigegeben wird, kann die Anwendung, die das Symbol kopiert hat, weiterhin das Symbol verwenden.

Die [**CopyImage**](/windows/desktop/api/Winuser/nf-winuser-copyimage) -Funktion erstellt ein neues Symbol auf der Grundlage des angegebenen Quell symbols. Das neue Symbol kann größer oder kleiner als das Quell Symbol sein.

Weitere Informationen zum Hinzufügen, entfernen oder Ersetzen von Symbol Ressourcen in ausführbaren Dateien (exe-Dateien) finden Sie unter [Ressourcen](resources.md).

Die [**duplialisieicon**](/windows/desktop/api/Shellapi/nf-shellapi-duplicateicon) -Funktion erstellt eine tatsächliche Kopie des Symbols.

 

 