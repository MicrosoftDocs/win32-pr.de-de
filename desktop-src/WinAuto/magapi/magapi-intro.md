---
title: Übersicht über die Vergrößerung
description: In diesem Thema wird die Vergrößerungs-API beschrieben und erläutert, wie Sie in einer Anwendung verwendet wird.
ms.assetid: 8dcecb73-db73-4043-b922-0b92f299eb1d
keywords:
- Vergrößern
- Anwendungen zur Bildschirm Vergrößerung
- Vergrößern
- benutzerdefinierte Abbild Verarbeitung
- Magnification.dll
- Erstellen von Lupe Steuerelementen
- selektive Vergrößerung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d66595cc2f5fdd8402ecd9d525e6deb1d07078
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106342356"
---
# <a name="magnification-api-overview"></a>Übersicht über die Vergrößerung

Die Vergrößerungs-API ermöglicht hilfstechnologieanbietern, Bildschirm Vergrößerungs Anwendungen zu entwickeln, die unter Microsoft Windows ausgeführt werden. In diesem Thema wird die Vergrößerungs-API beschrieben und erläutert, wie Sie in einer Anwendung verwendet wird. Sie enthält die folgenden Abschnitte:

- [Erste Schritte](#getting-started)
- [Grundlegende Konzepte](#basic-concepts)
  - [Typen von Bildschirmlupe](#types-of-magnifiers)
  - [Vergrößerungsfaktor](#magnification-factor)
  - [Farbeffekte](#color-effects)
  - [Quell Rechteck](#source-rectangle)
  - [Filter Liste](#filter-list)
  - [Eingabe Transformation](#input-transform)
  - [System Cursor](#system-cursor)
- [Initialisieren der Lauf Zeit Bibliothek für die Bildschirmlupe](#initializing-the-magnifier-run-time-library)
- [Verwenden der Full-Screen Bildschirmlupe](#using-the-full-screen-magnifier)
- [Verwenden des Vergrößerungs Steuer Elements](#using-the-magnifier-control)
  - [Erstellen des Vergrößerungs Steuer Elements](#creating-the-magnifier-control)
  - [Initialisieren des Steuerelements](#initializing-the-control)
  - [Festlegen des Quell Rechtecks](#setting-the-source-rectangle)
  - [Anwenden von Farbeffekten](#applying-color-effects)
  - [Selektive Vergrößerung](#selective-magnification)
- [Zugehörige Themen](#related-topics)

## <a name="getting-started"></a>Erste Schritte

Die ursprüngliche Version der Vergrößerungs-API wird unter Windows Vista und höheren Betriebssystemen unterstützt. Unter Windows 8 und höher unterstützt die API zusätzliche Funktionen, darunter die voll Bildvergrößerung und das Festlegen der Sichtbarkeit des vergrößerten System Cursors.

Die Unterstützung für die Vergrößerungs-API wird von Magnification.dll bereitgestellt. Wenn Sie die Anwendung kompilieren möchten, schließen Sie "Vergrößerung. h" ein, und verknüpfen Sie Sie mit "

> [!Note]  
> Die Vergrößerungs-API wird unter WOW64 nicht unterstützt. Das heißt, eine 32-Bit-Bildschirmlupe wird auf 64-Bit-Fenstern nicht ordnungsgemäß ausgeführt.

## <a name="basic-concepts"></a>Grundlegende Konzepte

In diesem Abschnitt werden die grundlegenden Konzepte beschrieben, auf denen die Vergrößerungs-API basiert. Sie enthält die folgenden Teile:

- [Typen von Bildschirmlupe](#types-of-magnifiers)
- [Vergrößerungsfaktor](#magnification-factor)
- [Farbeffekte](#color-effects)
- [Quell Rechteck](#source-rectangle)
- [Filter Liste](#filter-list)
- [Eingabe Transformation](#input-transform)
- [System Cursor](#system-cursor)

### <a name="types-of-magnifiers"></a>Typen von Bildschirmlupe

Die API unterstützt zwei Arten von Bildschirmlupe, die *Vollbild-Bildschirmlupe* und das Bildschirm *Lupe-Steuer* Element. Die Vollbild-Bildschirmlupe vergrößert den Inhalt des gesamten Bildschirms, während das Vergrößerungs Steuerelement den Inhalt eines bestimmten Bereichs des Bildschirms vergrößert und den Inhalt in einem Fenster anzeigt. Bei beiden Vergrößerungen werden Bilder und Text vergrößert, und beide ermöglichen es Ihnen, den Umfang der Vergrößerung zu steuern. Sie können auch Farbeffekte auf den vergrößerten Bildschirminhalt anwenden, um die Anzeige für Personen mit Farbfehlern zu erleichtern oder Farben mit mehr oder weniger Kontrast zu benötigen.

> [!Important]  
> Die Lupe-Steuerelement-API ist unter Windows Vista und höheren Betriebssystemen verfügbar, während die Vollbild-Bildschirmlupe nur unter Windows 8 und höheren Betriebssystemen verfügbar ist.

### <a name="magnification-factor"></a>Vergrößerungsfaktor

Sowohl der Vollbild-Bildschirmlupe als auch das Lupe-Steuerelement wenden eine Skalierungs Transformation an, um Bildschirminhalte zu vergrößern. Die von der Skalierungs Transformation angewendete Vergrößerung wird als *Vergrößerungsfaktor* bezeichnet. Sie wird als Gleit Komma Wert ausgedrückt, wobei 1,0 keiner Vergrößerung entspricht und größere Werte zu einer entsprechenden Vergrößerung führen. Mit dem Wert 1,5 wird der Bildschirminhalt beispielsweise um 50 Prozent vergrößert. Ein Vergrößerungsfaktor, der kleiner als 1,0 ist, ist ungültig.

### <a name="color-effects"></a>Farbeffekte

Farbeffekte werden erzielt, indem eine 5-x 5-Farb Transformationsmatrix auf die Farben der vergrößerten Bildschirminhalte angewendet wird. Die Matrix bestimmt die Intensitäten der roten, blauen, grünen und Alpha Komponenten des Inhalts. Weitere Informationen finden Sie unter [Verwenden einer Farb Matrix zum Transformieren einer einzelnen Farbe](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) in der Windows-GDI+-Dokumentation.

### <a name="source-rectangle"></a>Quell Rechteck

Die Vollbild-Bildschirmlupe wendet die Transformation für Skalierung und die Farb Transformation auf den gesamten Bildschirm an. Das Bildschirm Steuerelement kopiert dagegen einen Bildschirm, der als *Quell Rechteck* bezeichnet wird, in eine Offscreen-Bitmap. Anschließend wendet das-Steuerelement die Skalierungs Transformation und die Farb Transformation (sofern vorhanden) auf die Off-Screen-Bitmap an. Zum Schluss zeigt das Steuerelement die skalierte und Farb transformierte Bitmap im Fenster "Bildschirmlupe" an.

### <a name="filter-list"></a>Filter Liste

Standardmäßig vergrößert das Bildschirmlupe-Steuerelement alle Fenster im angegebenen Quell Rechteck. Durch Bereitstellen einer *Filterliste* von Fenster Handles können Sie jedoch steuern, welche Fenster in den vergrößerten Inhalt eingeschlossen werden und welche nicht. Weitere Informationen finden Sie unter [selektive Vergrößerung](#selective-magnification).

Die Vollbild-Bildschirmlupe unterstützt keine Filterliste. alle Fenster werden immer auf dem Bildschirm vergrößert.

### <a name="input-transform"></a>Eingabe Transformation

Normalerweise ist die Vergrößerung des Bildschirm Inhalts "unsichtbar" für Benutzer Stift-oder toucheingaben. Wenn der Benutzer z. b. auf das vergrößerte Bild eines-Steuer Elements tippt, übergibt das System nicht notwendigerweise die Eingabe an das-Steuerelement. Stattdessen übergibt das System die Eingabe an das beliebige Element (sofern vorhanden) an den angeprüften Bildschirm Koordinaten auf dem nicht vergrößerten Desktop. Mit der Funktion " [**magsettinputtransform**](/windows/win32/api/Magnification/nf-magnification-magsetinputtransform) " können Sie eine *Eingabe Transformation* angeben, die den Koordinaten Bereich des vergrößerten Bildschirm Inhalts dem tatsächlichen (nicht vergrößerten) Bildschirm Koordinaten Bereich zuordnet. Dadurch kann das System Stift-oder toucheingaben, die in vergrößertem Bildschirminhalt eingegeben werden, an das richtige Benutzeroberflächen Element auf dem Bildschirm übergeben.

> [!Note]  
> Der Aufrufprozess muss über UIAccess-Berechtigungen verfügen, um die Eingabe Transformation festzulegen. Weitere Informationen finden Sie unter [Sicherheitsüberlegungen zur Benutzeroberflächen Automatisierung](../uiauto-securityoverview.md) und [/MANIFESTUAC (bettet UAC-Informationen in Manifest ein)](/cpp/build/reference/manifestuac-embeds-uac-information-in-manifest).

### <a name="system-cursor"></a>System Cursor

Mit der Funktion " [**magshowsystemcursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) " können Sie den System Cursor anzeigen oder ausblenden. Wenn Sie den System Cursor beim Aktivieren der Vollbildschirm Bildschirmlupe anzeigen, wird der System Cursor immer zusammen mit dem restlichen Bildschirminhalt vergrößert. Wenn Sie den System Cursor ausblenden, wenn die Vollbild-Bildschirmlupe aktiv ist, ist der System Cursor überhaupt nicht sichtbar.

Mit dem Bildschirmlupe-Steuerelement zeigt die Funktion " [**magshowsystemcursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) " den nicht vergrößerten System Cursor an oder blendet sie aus, hat jedoch keine Auswirkung auf den vergrößerten System Cursor. Die Sichtbarkeit des vergrößerten System Cursors hängt davon ab, ob das Lupe Steuerelement den [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) Stil aufweist. Wenn dieses Format festgehalten wird, zeigt das Steuerelement für die Bildschirmlupe den vergrößerten System Cursor zusammen mit dem vergrößerten Bildschirminhalt an, wenn der System Cursor in das Quell Rechteck eintritt.

## <a name="initializing-the-magnifier-run-time-library"></a>Initialisieren der Lauf Zeit Bibliothek für die Bildschirmlupe

Bevor Sie beliebige andere Funktionen der Bildschirmlupe-API aufrufen können, müssen Sie die Bildschirm Lauf Zeit Objekte durch Aufrufen der Funktion " [**maginitialize**](/windows/win32/api/Magnification/nf-magnification-maginitialize) " erstellen und initialisieren. Wenn Sie die Bildschirmlupe abgeschlossen haben, müssen Sie die Funktion " [**maguninitialize**](/windows/win32/api/Magnification/nf-magnification-maguninitialize) " verwenden, um die Bildschirm Lauf Zeit Objekte zu zerstören und die zugeordneten Systemressourcen freizugeben.

## <a name="using-the-full-screen-magnifier"></a>Verwenden der Full-Screen Bildschirmlupe

Um die Vollbild-Bildschirmlupe zu verwenden, müssen Sie die Funktion [**magsetfullscreentransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) aufrufen. Der *maglevel* -Parameter gibt den Vergrößerungsfaktor an. Mit den Parametern *xoffset* und *yoffset* wird angegeben, wie der Bildschirm mit vergrößertem Bildschirm relativ zum Bildschirm positioniert wird.

Wenn der Bildschirminhalt vergrößert wird, wird er größer als der Bildschirm. Ein Teil des Inhalts erstreckt sich über die Ränder des Bildschirms hinaus und ist für den Benutzer unsichtbar. Mit den Parametern *xoffset* und *yoffset* der Funktion [**magsetfullscreentransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) wird festgelegt, welcher Teil des vergrößerten Bildschirm Inhalts auf dem Bildschirm angezeigt wird. Die Parameter geben die Koordinaten eines Punkts in den Bildschirm Inhalten ohne Vergrößerung an. Wenn der Inhalt vergrößert wird, wird er mit dem angegebenen Punkt in der oberen linken Ecke des Bildschirms positioniert.

Im folgenden Beispiel wird der Vergrößerungsfaktor für die Vollbild-Bildschirmlupe festgelegt, und der Mittelpunkt der vergrößerten Bildschirminhalte wird in der Mitte des Bildschirms platziert.

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

Verwenden Sie die Funktion " [**magsetfullscreencoloreffect**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreencoloreffect) ", um Farbeffekte auf den voll Bildinhalt anzuwenden, indem Sie eine Anwendungs definierte Farb Transformationsmatrix festlegen. Im folgenden Beispiel wird z. b. eine Farb Transformationsmatrix festgelegt, die Farben in Graustufen konvertiert.

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

Sie können den aktuellen Vergrößerungsfaktor und die Offset Werte abrufen, indem Sie die [**maggetfullscreentransform**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreentransform) -Funktion aufrufen. Sie können die aktuelle Farb Transformationsmatrix abrufen, indem Sie die [**maggetfullscreencoloreffect**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreencoloreffect) -Funktion aufrufen.

## <a name="using-the-magnifier-control"></a>Verwenden des Vergrößerungs Steuer Elements

Das Lupe Steuerelement vergrößert den Inhalt eines bestimmten Bereichs des Bildschirms und zeigt den Inhalt in einem Fenster an. In diesem Abschnitt wird beschrieben, wie Sie das Bildschirmlupe-Steuerelement verwenden. Sie enthält die folgenden Teile:

- [Erstellen des Vergrößerungs Steuer Elements](#creating-the-magnifier-control)
- [Initialisieren des Steuerelements](#initializing-the-control)
- [Festlegen des Quell Rechtecks](#setting-the-source-rectangle)
- [Anwenden von Farbeffekten](#applying-color-effects)
- [Selektive Vergrößerung](#selective-magnification)

### <a name="creating-the-magnifier-control"></a>Erstellen des Vergrößerungs Steuer Elements

Das Vergrößerungs Steuerelement muss in einem Fenster gehostet werden, das mit dem [**WS_EX_LAYERED**](../../winmsg/extended-window-styles.md) erweiterten Stil erstellt wurde. Nachdem Sie das Host Fenster erstellt haben, können Sie [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) aufrufen, um die Deckkraft des Host Fensters festzulegen. Das Host Fenster wird in der Regel auf vollständige Deckkraft festgelegt, um zu verhindern, dass der zugrunde liegende Bildschirminhalt angezeigt wird. Im folgenden Beispiel wird gezeigt, wie das Host Fenster auf vollständige Deckkraft festgelegt wird:

```C++
SetLayeredWindowAttributes(hwndHost, NULL, 255, LWA_ALPHA);
```

Wenn Sie den [**WS_EX_TRANSPARENT**](../../winmsg/extended-window-styles.md) Stil auf das Host Fenster anwenden, werden Mausklicks an die Position des Mauszeigers zurückgegeben, die sich hinter dem Host Fenster befindet. Beachten Sie, dass der Benutzer nicht in der Lage ist, das Vergrößerungs Fenster mit der Maus zu verschieben oder die Größe der Größe zu ändern, da das Host Fenster keine Mausklicks verarbeitet.

Die Fenster Klasse des Fenster Fensters der Bildschirmlupe muss **WC_MAGNIFIER** werden. Wenn Sie die [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) Formatvorlage anwenden, enthält das Vergrößerungs Steuerelement den System Cursor in den vergrößerten Bildschirminhalt, und der Cursor wird zusammen mit den Bildschirm Inhalten vergrößert.

Nachdem Sie das Vergrößerungs Steuerelement erstellt haben, behalten Sie das Fenster Handle bei, damit Sie es an andere Funktionen übergeben können.

Im folgenden Beispiel wird gezeigt, wie das Bildschirm Steuerelement erstellt wird.

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

Nachdem Sie das Steuerelement für die Bildschirmlupe erstellt haben, müssen Sie die Funktion " [**magsetwindowtransform**](/windows/win32/api/Magnification/nf-magnification-magsetwindowtransform) " aufrufen, um den Vergrößerungsfaktor anzugeben. Das ist einfach eine Frage der Angabe einer Matrix von

(*n*, 0,0, 0,0)

(0,0, *n*, 0,0)

(0,0, 0,0, 1,0)

wobei *n* der Vergrößerungsfaktor ist.

Im folgenden Beispiel wird gezeigt, wie der Vergrößerungsfaktor für das Lupe Steuerelement festgelegt wird.

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

### <a name="setting-the-source-rectangle"></a>Festlegen des Quell Rechtecks

Wenn der Benutzer den Mauszeiger auf dem Bildschirm bewegt, ruft die Anwendung die Funktion " [**magsetwindowsource**](/windows/win32/api/Magnification/nf-magnification-magsetwindowsource) " auf, um den Teil des zugrunde liegenden Bildschirms anzugeben, der vergrößert werden soll.

Die folgende Beispiel Funktion berechnet die Position und die Dimensionen des Quell Rechtecks (basierend auf der Mausposition und den Abmessungen des Vergrößerungs Fensters dividiert durch den Vergrößerungsfaktor) und legt das Quell Rechteck entsprechend fest. Die-Funktion zentriert auch den Client Bereich des Host Fensters an der Mausposition. Diese Funktion wird in Intervallen aufgerufen, um das Vergrößerungs Fenster zu aktualisieren.

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

Ein Vergrößerungs Steuerelement mit dem [**MS_INVERTCOLORS**](magapi-magnifier-styles.md) -Stil wendet eine integrierte Farb Transformationsmatrix an, die die Farben der vergrößerten Bildschirminhalte umkehrt. Die folgende Abbildung zeigt Bildschirminhalt in einem Bildschirm Steuerelement, das den **MS_INVERTCOLORS** Stil hat.

![Screenshot des vergrößerten Inhalts mit umgekehrten Farben](images/color-inversion.png)

Mithilfe der Funktion " [**magsetcoloreffect**](/windows/win32/api/Magnification/nf-magnification-magsetcoloreffect) " können Sie andere Farbeffekte durch Festlegen einer Anwendungs definierten Farb Transformationsmatrix anwenden. Beispielsweise wird mit der folgenden Funktion eine Farb Transformationsmatrix festgelegt, die Farben in Graustufen konvertiert.


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

Weitere Informationen zur Funktionsweise von Farb Transformationen finden [Sie unter Verwenden einer Farb Matrix zum Transformieren einer einzelnen Farbe](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) in der GDI+-Dokumentation.

### <a name="selective-magnification"></a>Selektive Vergrößerung

Standardmäßig wird die Vergrößerung auf alle Fenster außer dem Vergrößerungs Fenster selbst angewendet. Um anzugeben, welche Fenster vergrößert werden sollen, nennen Sie die Funktion " [**magsetwindowfilterlist**](/windows/win32/api/Magnification/nf-magnification-magsetwindowfilterlist) ". Diese Methode übernimmt entweder eine Liste von Fenstern, die vergrößert werden soll, oder eine Liste von Fenstern, die von der Vergrößerung ausgeschlossen werden sollen.

## <a name="related-topics"></a>Zugehörige Themen

[API zur Vergrößerung](entry-magapi-sdk.md)