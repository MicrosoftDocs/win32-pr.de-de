---
title: Übersicht über die Vergrößerungs-API
description: In diesem Thema wird die Vergrößerungs-API beschrieben und erläutert, wie sie in einer Anwendung verwendet wird.
ms.assetid: 8dcecb73-db73-4043-b922-0b92f299eb1d
keywords:
- Vergrößerung
- Bildschirmvergrößerungsanwendungen
- Vergrößerung
- Benutzerdefinierte Bildverarbeitung
- Magnification.dll
- Erstellen von Lupensteuerelementen
- Selektive Vergrößerung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb908623d6d6419925801119369f4f660110e680dd2499a1d61caa4c0c05de4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052592"
---
# <a name="magnification-api-overview"></a>Übersicht über die Vergrößerungs-API

Mit der Vergrößerungs-API können Hilfstechnologieanbieter Anwendungen zur Bildschirmvergrößerung entwickeln, die auf Microsoft-Windows. In diesem Thema wird die Vergrößerungs-API beschrieben und erläutert, wie sie in einer Anwendung verwendet wird. Sie enthält die folgenden Abschnitte:

- [Erste Schritte](#getting-started)
- [Grundlegende Konzepte](#basic-concepts)
  - [Typen von Lupen](#types-of-magnifiers)
  - [Vergrößerungsfaktor](#magnification-factor)
  - [Farbeffekte](#color-effects)
  - [Quellrechteck](#source-rectangle)
  - [Filterliste](#filter-list)
  - [Eingabetransformation](#input-transform)
  - [Systemcursor](#system-cursor)
- [Initialisieren der Laufzeitbibliothek für die Vergrößerung](#initializing-the-magnifier-run-time-library)
- [Verwenden der Full-Screen Magnifier](#using-the-full-screen-magnifier)
- [Verwenden des Steuerelements "Lupe"](#using-the-magnifier-control)
  - [Erstellen des Steuerelements "Lupe"](#creating-the-magnifier-control)
  - [Initialisieren des Steuerelements](#initializing-the-control)
  - [Festlegen des Quellrechtecks](#setting-the-source-rectangle)
  - [Anwenden von Farbeffekten](#applying-color-effects)
  - [Selektive Vergrößerung](#selective-magnification)
- [Zugehörige Themen](#related-topics)

## <a name="getting-started"></a>Erste Schritte

Die ursprüngliche Version der Vergrößerungs-API wird unter Windows Vista-Betriebssystemen und höher unterstützt. Ab Windows 8 unterstützt die API zusätzliche Features, z. B. die Vollbildvergrößerung und das Festlegen der Sichtbarkeit des vergrößerten Systemcursors.

Unterstützung für die Vergrößerungs-API wird von Magnification.dll. Um Ihre Anwendung zu kompilieren, schließen Sie Magnification.h ein, und verknüpfen Sie magnification.lib.

> [!Note]  
> Die Vergrößerungs-API wird unter WOW64 nicht unterstützt. Das heißt, eine 32-Bit-Vergrößerungsanwendung wird auf 64-Bit-Anwendungen Windows.

## <a name="basic-concepts"></a>Grundlegende Konzepte

In diesem Abschnitt werden die grundlegenden Konzepte beschrieben, auf denen die Vergrößerungs-API basiert. Sie enthält die folgenden Teile:

- [Typen von Lupen](#types-of-magnifiers)
- [Vergrößerungsfaktor](#magnification-factor)
- [Farbeffekte](#color-effects)
- [Quellrechteck](#source-rectangle)
- [Filterliste](#filter-list)
- [Eingabetransformation](#input-transform)
- [Systemcursor](#system-cursor)

### <a name="types-of-magnifiers"></a>Typen von Lupen

Die API unterstützt zwei Arten von  Bildschirmlupes: die Vollbildlupe und das *Bildschirmlupe-Steuerelement*. Die Vollbildlupe vergrößert den Inhalt des gesamten Bildschirms, während das Bildschirmlupe-Steuerelement den Inhalt eines bestimmten Bildschirmbereichs vergrößert und den Inhalt in einem Fenster anzeigt. Sowohl für Lupen als auch für Bilder und Text wird die Vergrößerung ermöglicht, und beide ermöglichen es Ihnen, die Menge der Vergrößerung zu steuern. Sie können auch Farbeffekte auf den vergrößerten Bildschirminhalt anwenden, um die Anzeige für Personen zu vereinfachen, die Farbverfälschtheiten haben oder Farben mit mehr oder weniger Kontrast benötigen.

> [!Important]  
> Die Bildschirmlupe-Steuerelement-API ist unter Windows Vista und höher verfügbar, während die Vollbildlupe-API nur unter Windows 8 und höher verfügbar ist.

### <a name="magnification-factor"></a>Vergrößerungsfaktor

Sowohl die Vollbildlupe als auch das Bildschirmlupe-Steuerelement wenden eine Skalierungstransformation an, um den Bildschirminhalt zu vergrößern. Der von der Skalierungstransformation angewendete Vergrößerungsfaktor wird als *Vergrößerungsfaktor bezeichnet.* Sie wird als Gleitkommawert ausgedrückt, wobei 1,0 keiner Vergrößerung entspricht und größere Werte zu einer entsprechenden Vergrößerung führen. Bei einem Wert von 1,5 wird der Bildschirminhalt beispielsweise um 50 Prozent größer. Ein Vergrößerungsfaktor kleiner als 1,0 ist ungültig.

### <a name="color-effects"></a>Farbeffekte

Farbeffekte werden erzielt, indem eine 5-mal-5-Farbtransformationsmatrix auf die Farben des vergrößerten Bildschirminhalts anwenden. Die Matrix bestimmt die Intensitäten der roten, blauen, grünen und Alphakomponenten des Inhalts. Weitere Informationen finden Sie unter [Verwenden einer Farbmatrix zum Transformieren](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) einer einzelnen Farbe in der Windows GDI+ Dokumentation.

### <a name="source-rectangle"></a>Quellrechteck

Die Vollbildlupe wendet die Skalierungstransformation und Farbtransformation auf den gesamten Bildschirm an. Das Bildschirmlupe-Steuerelement kopiert dagegen einen Bereich des Bildschirms, der als Quellrechteck bezeichnet *wird,* in eine Bitmap im Off-Screen-Bereich. Als Nächstes wendet das Steuerelement die Skalierungstransformation und gegebenenfalls die Farbtransformation auf die Off-Screen-Bitmap an. Schließlich zeigt das Steuerelement die skalierte und farbverwandelte Bitmap im Bildschirmlupe-Steuerelementfenster an.

### <a name="filter-list"></a>Filterliste

Standardmäßig werden alle Fenster im angegebenen Quellrechteck vom Vergrößerungssteuersystem vergrößert. Indem Sie jedoch eine *Filterliste mit Fensterhandles* bereitstellen, können Sie steuern, welche Fenster im vergrößerten Inhalt enthalten sind und welche nicht. Weitere Informationen finden Sie unter [Selektive Vergrößerung.](#selective-magnification)

Die Vollbildlupe unterstützt keine Filterliste. Es werden immer alle Fenster auf dem Bildschirm vergrößert.

### <a name="input-transform"></a>Eingabetransformation

Normalerweise ist vergrößerter Bildschirminhalt für Benutzerstift- oder Toucheingaben "unsichtbar". Wenn der Benutzer beispielsweise auf das vergrößerte Bild eines Steuerelements tippt, über gibt das System die Eingabe nicht unbedingt an das Steuerelement weiter. Stattdessen übergibt das System die Eingabe an jedes Element (sofern verfügbar), das sich an den angeknippten Bildschirmkoordinaten auf dem unvorstellbaren Desktop befindet. Mit [**der MagSetInputTransform-Funktion**](/windows/win32/api/Magnification/nf-magnification-magsetinputtransform) können  Sie eine Eingabetransformation angeben, die den Koordinatenraum des vergrößerten Bildschirminhalts dem tatsächlichen (nicht großen) Bildschirmkoordinatenraum zuteilt. Dadurch kann das System Stift- oder Toucheingaben, die in vergrößerten Bildschirminhalten eingegeben werden, an das richtige Benutzeroberflächenelement auf dem Bildschirm übergeben.

> [!Note]  
> Der aufrufende Prozess muss über UIAccess-Berechtigungen verfügen, um die Eingabetransformation festlegen zu können. Weitere Informationen finden Sie unter [Benutzeroberflächenautomatisierung Überlegungen zur](../uiauto-securityoverview.md) Sicherheit und [/MANIFESTUAC (Bettet UAC-Informationen in manifest ein).](/cpp/build/reference/manifestuac-embeds-uac-information-in-manifest)

### <a name="system-cursor"></a>Systemcursor

Mit [**der MagShowSystemCursor-Funktion**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) können Sie den Systemcursor ein- oder ausblenden. Wenn Sie den Systemcursor anzeigen, wenn die Vollbildlupe aktiv ist, wird der Systemcursor immer zusammen mit dem restlichen Bildschirminhalt vergrößert. Wenn Sie den Systemcursor ausblenden, wenn die Vollbildlupe aktiv ist, ist der Systemcursor überhaupt nicht sichtbar.

Mit dem Lupen-Steuerelement zeigt die [**MagShowSystemCursor-Funktion**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) den unvorstellbaren Systemcursor an oder blendet den Cursor aus, hat jedoch keine Auswirkungen auf den vergrößerten Systemcursor. Die Sichtbarkeit des vergrößerten Systemcursors hängt davon ab, ob das Lupen-Steuerelement den [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) hat. Wenn dieses Format verwendet wird, zeigt das Bildschirmlupe-Steuerelement den vergrößerten Systemcursor zusammen mit dem vergrößerten Bildschirminhalt an, wenn der Systemcursor in das Quellrechteck eintritt.

## <a name="initializing-the-magnifier-run-time-library"></a>Initialisieren der Laufzeitbibliothek für die Vergrößerung

Bevor Sie andere Lupen-API-Funktionen aufrufen können, müssen Sie die Lupen-Laufzeitobjekte erstellen und initialisieren, indem Sie die [**MagInitialize-Funktion**](/windows/win32/api/Magnification/nf-magnification-maginitialize) aufrufen. Wenn Sie die Verwendung der Lupen-API abgeschlossen haben, rufen Sie entsprechend die [**MagUninitialize-Funktion**](/windows/win32/api/Magnification/nf-magnification-maguninitialize) auf, um die Lupen-Laufzeitobjekte zu zerstören und die zugeordneten Systemressourcen frei zu geben.

## <a name="using-the-full-screen-magnifier"></a>Verwenden der Full-Screen Magnifier

Um die Vollbildlupe zu verwenden, rufen Sie die [**MagSetFullscreenTransform-Funktion**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) auf. Der *magLevel-Parameter* gibt den Vergrößerungsfaktor an. Die *Parameter xOffset* und *yOffset* geben an, wie der vergrößerte Bildschirminhalt relativ zum Bildschirm positioniert wird.

Wenn der Bildschirminhalt vergrößert wird, wird er größer als der Bildschirm selbst. Ein Teil des Inhalts erstreckt sich über die Bildschirmränder hinaus und wird für den Benutzer unsichtbar. Die *Parameter xOffset* und *yOffset* der [**MagSetFullscreenTransform-Funktion**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) bestimmen, welcher Teil des vergrößerten Bildschirminhalts auf dem Bildschirm angezeigt wird. Zusammen geben die Parameter die Koordinaten eines Punkts im inhalt des ungemagerten Bildschirms an. Wenn der Inhalt vergrößert wird, wird er am angegebenen Punkt in der oberen linken Ecke des Bildschirms positioniert.

Im folgenden Beispiel wird der Vergrößerungsfaktor für die Vollbildlupe festgelegt und die Mitte des vergrößerten Bildschirminhalts in der Mitte des Bildschirms platziert.

```C++
BOOL SetZoom(float magnificationFactor)
{
    // A magnification factor less than 1.0 is not valid.
    if (magnificationFactor < 1.0)
    {
        return FALSE;
    }

    // Calculate offsets such that the center of the magnified screen content 
    // is at the center of the screen. The offsets are relative to the 
    // unmagnified screen content.
    int xDlg = (int)((float)GetSystemMetrics(
            SM_CXSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);
    int yDlg = (int)((float)GetSystemMetrics(
            SM_CYSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);

    return MagSetFullscreenTransform(magnificationFactor, xDlg, yDlg);
}
```

Verwenden Sie die [**MagSetFullscreenColorEffect-Funktion,**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreencoloreffect) um Farbeffekte auf den Vollbildinhalt anzuwenden, indem Sie eine anwendungsdefinierte Farbtransformationsmatrix festlegen. Im folgenden Beispiel wird beispielsweise eine Farbtransformationsmatrix festgelegt, die Farben in Graustufen konvertiert.

```C++
// Initialize color transformation matrices used to apply grayscale and to 
// restore the original screen color.
MAGCOLOREFFECT g_MagEffectGrayscale = {0.3f,  0.3f,  0.3f,  0.0f,  0.0f,
                                       0.6f,  0.6f,  0.6f,  0.0f,  0.0f,
                                       0.1f,  0.1f,  0.1f,  0.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

MAGCOLOREFFECT g_MagEffectIdentity = {1.0f,  0.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  1.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  1.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

BOOL SetColorGrayscale(__in BOOL fGrayscaleOn)
{
    // Apply the color matrix required to either apply grayscale to the screen 
    // colors or to show the regular colors.
    PMAGCOLOREFFECT pEffect = 
                (fGrayscaleOn ? &amp;g_MagEffectGrayscale : &amp;g_MagEffectIdentity);

    return MagSetFullscreenColorEffect(pEffect);
}
```

Sie können die aktuellen Vergrößerungsfaktor- und Offsetwerte abrufen, indem Sie die [**MagGetFullscreenTransform-Funktion**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreentransform) aufrufen. Sie können die aktuelle Farbtransformationsmatrix abrufen, indem Sie die [**MagGetFullscreenColorEffect-Funktion**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreencoloreffect) aufrufen.

## <a name="using-the-magnifier-control"></a>Verwenden des Bildschirmlupe-Steuerelements

Das Bildschirmlupe-Steuerelement vergrößert den Inhalt eines bestimmten Bildschirmbereichs und zeigt den Inhalt in einem Fenster an. In diesem Abschnitt wird die Verwendung des Bildschirmlupesteuerelements beschrieben. Es enthält die folgenden Teile:

- [Erstellen des Bildschirmlupe-Steuerelements](#creating-the-magnifier-control)
- [Initialisieren des Steuerelements](#initializing-the-control)
- [Festlegen des Quellrechtecks](#setting-the-source-rectangle)
- [Anwenden von Farbeffekten](#applying-color-effects)
- [Selektive Vergrößerung](#selective-magnification)

### <a name="creating-the-magnifier-control"></a>Erstellen des Bildschirmlupe-Steuerelements

Das Bildschirmlupe-Steuerelement muss in einem Fenster gehostet werden, das mit der [**erweiterten WS_EX_LAYERED**](../../winmsg/extended-window-styles.md) erstellt wurde. Rufen Sie nach dem Erstellen des [**Hostfensters SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) auf, um die Deckkraft des Hostfensters festzulegen. Das Hostfenster ist in der Regel auf vollständige Deckkraft festgelegt, um zu verhindern, dass der zugrunde liegende Bildschirminhalt angezeigt wird. Das folgende Beispiel zeigt, wie das Hostfenster auf vollständige Deckkraft festgelegt wird:

```C++
SetLayeredWindowAttributes(hwndHost, NULL, 255, LWA_ALPHA);
```

Wenn Sie den [**WS_EX_TRANSPARENT**](../../winmsg/extended-window-styles.md) Stil auf das Hostfenster anwenden, werden Mausklicks an das Objekt hinter dem Hostfenster an der Position des Mauszeigers übergeben. Beachten Sie, dass der Benutzer das Vergrößerungsfenster nicht mit der Maus verschieben oder dessen Größe ändern kann, da das Hostfenster keine Mausklicks verarbeitet.

Die Fensterklasse des Bildschirmlupe-Steuerelementfensters muss **WC_MAGNIFIER** sein. Wenn Sie die [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) Anwenden, schließt das Bildschirmlupe-Steuerelement den Systemcursor in den vergrößerten Bildschirminhalt ein, und der Cursor wird zusammen mit dem Bildschirminhalt vergrößert.

Nachdem Sie das Bildschirmlupe-Steuerelement erstellt haben, behalten Sie das Fensterhandle bei, damit Sie es an andere Funktionen übergeben können.

Das folgende Beispiel zeigt, wie das Bildschirmlupe-Steuerelement erstellt wird.

```C++
// Description: 
//   Registers the host window class, creates the host window, sets the layered
//   window attributes, and creates the magnifier control. 
// Parameters:
//   hInstance - Instance handle of the application.
// Variables:
//   HostWndProc - Window procedure of the host window.
//   WindowClassName - Name of the window class.
//   WindowTitle - Title of the host window.
// Constants and global variables:
//   hwndHost - Handle of the host window.
//   hwndMag - Handle of the magnifier window.
//   LENS_WIDTH - Width of the magnifier window.
//   LENS_HEIGHT - Height of the magnifier window.
// 
BOOL CreateMagnifier(HINSTANCE hInstance)
{
   // Register the host window class.
    WNDCLASSEX wcex = {};
    wcex.cbSize = sizeof(WNDCLASSEX); 
    wcex.style          = 0;
    wcex.lpfnWndProc    = HostWndProc;
    wcex.hInstance      = hInstance;
    wcex.hCursor        = LoadCursor(NULL, IDC_ARROW);
    wcex.hbrBackground  = (HBRUSH)(1 + COLOR_BTNFACE);
    wcex.lpszClassName  = WindowClassName;
    
    if (RegisterClassEx(&amp;wcex) == 0)
        return FALSE;

    // Create the host window. 
    hwndHost = CreateWindowEx(WS_EX_TOPMOST | WS_EX_LAYERED | WS_EX_TRANSPARENT, 
        WindowClassName, WindowTitle, 
        WS_CLIPCHILDREN,
        0, 0, 0, 0,
        NULL, NULL, hInstance, NULL);
    if (!hwndHost)
    {
        return FALSE;
    }

    // Make the window opaque.
    SetLayeredWindowAttributes(hwndHost, 0, 255, LWA_ALPHA);

    // Create a magnifier control that fills the client area.
    hwndMag = CreateWindow(WC_MAGNIFIER, TEXT("MagnifierWindow"), 
        WS_CHILD | MS_SHOWMAGNIFIEDCURSOR | WS_VISIBLE,
        0, 0, 
        LENS_WIDTH, 
        LENS_HEIGHT, 
        hwndHost, NULL, hInstance, NULL );
    if (!hwndMag)
    {
        return FALSE;
    }

    return TRUE;
}
```

### <a name="initializing-the-control"></a>Initialisieren des Steuerelements

Nach dem Erstellen des Bildschirmlupesteuerelements müssen Sie die [**MagSetWindowTransform-Funktion**](/windows/win32/api/Magnification/nf-magnification-magsetwindowtransform) aufrufen, um den Vergrößerungsfaktor anzugeben. Dies ist lediglich eine Frage der Angabe einer Matrix von

(*n*, 0.0, 0.0)

(0.0, *n*, 0.0)

(0.0, 0.0, 1.0)

wobei *n* der Vergrößerungsfaktor ist.

Das folgende Beispiel zeigt, wie der Vergrößerungsfaktor für das Bildschirmlupesteuerelement festgelegt wird.

```C++
// Description:
//   Sets the magnification factor for a magnifier control.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   magFactor - New magnification factor.
//
BOOL SetMagnificationFactor(HWND hwndMag, float magFactor)
{
    MAGTRANSFORM matrix;
    memset(&amp;matrix, 0, sizeof(matrix));
    matrix.v[0][0] = magFactor;
    matrix.v[1][1] = magFactor;
    matrix.v[2][2] = 1.0f;

    return MagSetWindowTransform(hwndMag, &amp;matrix);  
}
```

### <a name="setting-the-source-rectangle"></a>Festlegen des Quellrechtecks

Wenn der Benutzer den Mauszeiger um den Bildschirm bewegt, ruft Ihre Anwendung die [**MagSetWindowSource-Funktion**](/windows/win32/api/Magnification/nf-magnification-magsetwindowsource) auf, um den Teil des zugrunde liegenden Bildschirms anzugeben, der vergrößert werden soll.

Die folgende Beispielfunktion berechnet die Position und die Abmessungen des Quellrechtecks (basierend auf der Mausposition und den Abmessungen des Bildschirmlupefensters geteilt durch den Vergrößerungsfaktor) und legt das Quellrechteck entsprechend fest. Die Funktion zentrt auch den Clientbereich des Hostfensters an der Mausposition. Diese Funktion wird in Intervallen aufgerufen, um das Vergrößerungsfenster zu aktualisieren.

```C++
// Description: 
//   Called by a timer to update the contents of the magnifier window and to set
//   the position of the host window. 
// Constants and global variables:
//   hwndHost - Handle of the host window.
//   hwndMag - Handle of the magnifier window.
//   LENS_WIDTH - Width of the magnifier window.
//   LENS_HEIGHT - Height of the magnifier window.
//   MAGFACTOR - The magnification factor.
//
void CALLBACK UpdateMagWindow(HWND /*hwnd*/, UINT /*uMsg*/, 
        UINT_PTR /*idEvent*/, DWORD /*dwTime*/)
{
    // Get the mouse coordinates.
    POINT mousePoint;
    GetCursorPos(&amp;mousePoint);

    // Calculate a source rectangle that is centered at the mouse coordinates. 
    // Size the rectangle so that it fits into the magnifier window (the lens).
    RECT sourceRect;
    int borderWidth = GetSystemMetrics(SM_CXFIXEDFRAME);
    int captionHeight = GetSystemMetrics(SM_CYCAPTION);
    sourceRect.left = (mousePoint.x - (int)((LENS_WIDTH / 2) / MAGFACTOR)) + 
             (int)(borderWidth / MAGFACTOR);
    sourceRect.top = (mousePoint.y - (int)((LENS_HEIGHT / 2) / MAGFACTOR)) + 
             (int)(captionHeight / MAGFACTOR) + (int)(borderWidth / MAGFACTOR); 
    sourceRect.right = LENS_WIDTH;
    sourceRect.bottom = LENS_HEIGHT;

    // Pass the source rectangle to the magnifier control.
    MagSetWindowSource(hwndMag, sourceRect);

    // Move the host window so that the origin of the client area lines up
    // with the origin of the magnified source rectangle.
    MoveWindow(hwndHost, 
        (mousePoint.x - LENS_WIDTH / 2), 
        (mousePoint.y - LENS_HEIGHT / 2), 
        LENS_WIDTH, 
        LENS_HEIGHT,
        FALSE);

    // Force the magnifier control to redraw itself.
    InvalidateRect(hwndMag, NULL, TRUE);

    return;
}
```

### <a name="applying-color-effects"></a>Anwenden von Farbeffekten

Ein Bildschirmlupesteuerelement mit dem [**MS_INVERTCOLORS**](magapi-magnifier-styles.md) Stil wendet eine integrierte Farbtransformationsmatrix an, die die Farben des vergrößerten Bildschirminhalts umkehrt. Die folgende Abbildung zeigt den Bildschirminhalt in einem Bildschirmlupe-Steuerelement mit dem **MS_INVERTCOLORS** Stil.

![Screenshot des vergrößerten Inhalts mit invertierten Farben](images/color-inversion.png)

Mit der [**MagSetColorEffect-Funktion**](/windows/win32/api/Magnification/nf-magnification-magsetcoloreffect) können Sie andere Farbeffekte anwenden, indem Sie eine anwendungsdefinierte Farbtransformationsmatrix festlegen. Die folgende Funktion legt beispielsweise eine Farbtransformationsmatrix fest, die Farben in Graustufen konvertiert.


```C++
// Description:
//   Converts the colors displayed in the magnifier window to grayscale, or
//   returns the colors to normal.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   fInvert - TRUE to convert to grayscale, or FALSE for normal colors.
//
BOOL ConvertToGrayscale(HWND hwndMag, BOOL fConvert)
{
    // Convert the screen colors in the magnifier window.
    if (fConvert)
    {
        MAGCOLOREFFECT magEffectGrayscale = 
            {{ // MagEffectGrayscale
                {  0.3f,  0.3f,  0.3f,  0.0f,  0.0f },
                {  0.6f,  0.6f,  0.6f,  0.0f,  0.0f },
                {  0.1f,  0.1f,  0.1f,  0.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  1.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  0.0f,  1.0f } 
            }};

        return MagSetColorEffect(hwndMag, &amp;magEffectGrayscale);
    }

    // Return the colors to normal.
    else
    {
        return MagSetColorEffect(hwndMag, NULL);
    }
}
```

Weitere Informationen zur Funktionsweise von Farbtransformationen finden Sie unter [Using a Color Matrix to Transform a Single Color (Verwenden einer Farbmatrix zum Transformieren einer einzelnen Farbe)](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) in der GDI+-Dokumentation.

### <a name="selective-magnification"></a>Selektive Vergrößerung

Standardmäßig wird die Vergrößerung auf alle Fenster außer dem Vergrößerungsfenster selbst angewendet. Um anzugeben, welche Fenster vergrößert werden sollen, rufen Sie die [**MagSetWindowFilterList-Funktion**](/windows/win32/api/Magnification/nf-magnification-magsetwindowfilterlist) auf. Diese Methode verwendet entweder eine Liste der zu vergrößernde Fenster oder eine Liste von Fenstern, die von der Vergrößerung ausgeschlossen werden sollen.

## <a name="related-topics"></a>Zugehörige Themen

[API zur Vergrößerung](entry-magapi-sdk.md)