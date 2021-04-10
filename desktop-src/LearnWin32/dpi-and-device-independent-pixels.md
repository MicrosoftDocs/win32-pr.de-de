---
title: DPI-und Device-Independent Pixel
ms.assetid: d282de02-62f4-4a12-a77c-f602f6db0216
description: 'Weitere Informationen: dpi und Device-Independent Pixel'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6f04e1a056611fcdfe8b59ff65b38ecec99eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868660"
---
# <a name="dpi-and-device-independent-pixels"></a>DPI-und Device-Independent Pixel

Um effektiv mit Windows-Grafiken zu programmieren, müssen Sie zwei verwandte Konzepte verstehen:

-   Punkte pro Zoll (dpi)
-   Geräte unabhängiges Pixel (Dips).

Beginnen wir mit dpi. Dies erfordert eine kurze Umleitung in typografieweise. In der Typografie wird die Größe des Typs in Einheiten gemessen, die als *Punkte* bezeichnet werden. Ein Punkt ist gleich 1/72 Zoll.

<dl> 1 pt = 1/72 Zoll  
</dl>

> [!Note]  
> Dies ist die Desktop Veröffentlichungs Definition des Punkts. In der Vergangenheit hat sich das genaue Measure eines Punkts geändert.

 

Beispielsweise ist eine 12-Punkt-Schriftart so konzipiert, dass Sie in eine 1/6 "(12/72) Textzeile passt. Dies bedeutet natürlich nicht, dass jedes Zeichen in der Schriftart genau 1/6 "groß ist. Tatsächlich können einige Zeichen größer als 1/6 "sein. In vielen Schriftarten ist das Zeichen "" z. b. größer als die nominale Höhe der Schriftart. Um ordnungsgemäß angezeigt zu werden, benötigt die Schriftart zusätzlichen Leerraum zwischen dem Text. Dieser Bereich wird als *führende* bezeichnet.

Die folgende Abbildung zeigt eine 72-Punkt-Schriftart. Die einschließenden Linien zeigen ein "großes Begrenzungsfeld um den Text an. Die gestrichelte Linie wird als *Baseline* bezeichnet. Die meisten Zeichen in einer Schriftart verbleibenden die Baseline. Die Höhe der Schriftart umfasst den Teil oberhalb der Baseline (der *Aufstieg*) und den Teil unterhalb der Baseline (der *Abstieg*). In der hier gezeigten Schriftart ist der Anstieg 56 Punkte, und der Abstieg ist 16 Punkte.

![eine Abbildung, die eine 72-Punkt-Schriftart anzeigt.](images/graphics11.png)

Bei einer Computer Anzeige ist das Messen der Textgröße jedoch problematisch, da Pixel nicht die gleiche Größe aufweisen. Die Größe eines Pixels hängt von zwei Faktoren ab: der Anzeige Auflösung und der physischen Größe des Monitors. Aus diesem Grund sind physische Zoll-Einheiten kein nützliches Measure, da es keine fixierte Beziehung zwischen physischen Zoll und Pixel gibt. Stattdessen werden Schriftarten in *logischen* Einheiten gemessen. Eine 72-Punkt Schriftart ist als ein logischer Zoll definiert. Logische Zoll werden dann in Pixel konvertiert. Seit vielen Jahren hat Windows die folgende Konvertierung verwendet: ein logischer Zoll ist 96 Pixel. Bei Verwendung dieses Skalierungsfaktors wird eine 72-Punkt-Schriftart als 96 Pixel hoch gerendert. Eine 12-Punkt-Schriftart ist 16 Pixel hoch.

<dl> 12 Punkte = 12/72 logischer Zoll = 1/6 logischer Zoll = 96/6 Pixel = 16 Pixel  
</dl>

Dieser Skalierungsfaktor wird als 96 Punkte pro Zoll (dpi) beschrieben. Der Begriff "Punkte" leitet sich vom Druck ab, bei dem physische Handzettel auf Papier abgelegt werden. Bei Computer anzeigen wäre es genauer gesagt, dass Sie 96 Pixel pro logischem Zoll, aber der Begriff dpi nicht mehr angezeigt wird.

Da die tatsächlichen Pixelgrößen variieren, kann Text, der auf einem Monitor lesbar ist, auf einem anderen Monitor zu klein sein. Außerdem haben die Benutzer unterschiedliche Vorlieben – einige Personen bevorzugen größere Texte. Aus diesem Grund ermöglicht Windows dem Benutzer das Ändern der dpi-Einstellung. Wenn der Benutzer z. b. die Anzeige auf 144 dpi festlegt, ist eine 72-Punkt-Schriftart 144 Pixel hoch. Die standardmäßigen dpi-Einstellungen lauten 100% (96 dpi), 125% (120 dpi) und 150% (144 dpi). Der Benutzer kann auch eine benutzerdefinierte Einstellung anwenden. Ab Windows 7 ist dpi eine Einstellung pro Benutzer.

## <a name="dwm-scaling"></a>DWM-Skalierung

Wenn ein Programm dpi nicht berücksichtigt, sind möglicherweise die folgenden Fehler bei den Einstellungen für hohe DPI-Einstellungen erkennbar:

-   Clipped UI-Elemente.
-   Falsches Layout.
-   Pixel-Bitmaps und-Symbole.
-   Falsche Maus Koordinaten, die Auswirkungen auf Treffer Tests, Drag & Drop usw. haben können.

Um sicherzustellen, dass ältere Programme bei High-dpi-Einstellungen funktionieren, implementiert die DWM einen nützlichen Fallback. Wenn ein Programm nicht als dpi-fähig gekennzeichnet ist, skaliert die DWM die gesamte Benutzeroberfläche entsprechend der dpi-Einstellung. Beispielsweise wird die Benutzeroberfläche bei 144 dpi um 150% skaliert, einschließlich Text, Grafiken, Steuerelementen und Fenstergrößen. Wenn das Programm ein 500 × 500-Fenster erstellt, wird das Fenster tatsächlich als 750 × 750 Pixel angezeigt, und der Inhalt des Fensters wird entsprechend skaliert.

Dieses Verhalten bedeutet, dass ältere Programme bei High-dpi-Einstellungen "just work" funktionieren. Die Skalierung führt jedoch auch zu einem etwas unscharf dargestellten aussehen, da die Skalierung nach dem Zeichnen des Fensters angewendet wird.

## <a name="dpi-aware-applications"></a>DPI-Aware Anwendungen

Um die DWM-Skalierung zu vermeiden, kann sich ein Programm selbst als dpi-fähig kennzeichnen. Dies weist den DWM an, keine automatische DPI-Skalierung auszuführen. Alle neuen Anwendungen sollten für die dpi-Unterstützung entworfen werden, da die Darstellung der Benutzeroberfläche bei höheren dpi-Einstellungen durch die dpi-Erkennung verbessert wird.

Ein Programm deklariert sich über sein Anwendungs Manifest mit dpi-Werten. Ein *Manifest* ist eine einfache XML-Datei, die eine DLL oder Anwendung beschreibt. Das Manifest ist in der Regel in die ausführbare Datei eingebettet, obwohl es als separate Datei bereitgestellt werden kann. Ein Manifest enthält Informationen, wie z. b. dll-Abhängigkeiten, die angeforderte Berechtigungsebene und die Version von Windows, für die das Programm entworfen wurde.

Um zu deklarieren, dass das Programm dpi-fähig ist, fügen Sie die folgenden Informationen in das Manifest ein.

``` syntax
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
      <dpiAware>true</dpiAware>
    </asmv3:windowsSettings>
  </asmv3:application>
</assembly>
```

Die hier gezeigte Auflistung ist nur ein partielles Manifest, aber der Visual Studio-Linker generiert automatisch den Rest des Manifests. Führen Sie in Visual Studio die folgenden Schritte aus, um ein partielles Manifest in das Projekt einzuschließen.

1.  Klicken Sie im Menü **Projekt** auf **Eigenschaft**.
2.  Erweitern Sie im linken Bereich **Konfigurations Eigenschaften**, erweitern Sie **Manifest-Tool**, und klicken Sie dann auf **Eingabe und Ausgabe**.
3.  Geben Sie im Textfeld **zusätzliche Manifest-Dateien** den Namen der Manifest-Datei ein, und klicken Sie dann auf **OK**.

Wenn Sie Ihr Programm als dpi-fähig markieren, weisen Sie die DWM an, das Anwendungsfenster nicht zu skalieren. Wenn Sie nun ein Fenster mit dem Wert 500 × 500 erstellen, belegt das Fenster unabhängig von der dpi-Einstellung des Benutzers 500 × 500 Pixel.

## <a name="gdi-and-dpi"></a>GDI und dpi

Die GDI-Zeichnung wird in Pixel gemessen. Dies bedeutet Folgendes: Wenn Ihr Programm als dpi-fähig markiert ist, und Sie GDI zum Zeichnen eines 200 × 100-Rechtecks auffordern, wird das resultierende Rechteck 200 Pixel breit und 100 Pixel auf dem Bildschirm angezeigt. GDI-Schriftgrößen werden jedoch auf die aktuelle dpi-Einstellung skaliert. Anders ausgedrückt: Wenn Sie eine 72-Punkt-Schriftart erstellen, beträgt die Schriftart 96 Pixel bei 96 dpi, aber 144 Pixel bei 144 dpi. Hier sehen Sie eine 72-Punkt Schriftart, die mit GDI bei 144 dpi gerendert wird

![ein Diagramm, das die Skalierung von dpi-Schriftart in GDI anzeigt.](images/graphics12.png)

Wenn Ihre Anwendung dpi-fähig ist und Sie GDI zum Zeichnen verwenden, Skalieren Sie alle Zeichnungs Koordinaten entsprechend der dpi-Größe.

## <a name="direct2d-and-dpi"></a>Direct2D und dpi

Direct2D führt die Skalierung automatisch entsprechend der dpi-Einstellung aus. In Direct2D werden Koordinaten in Einheiten gemessen, die als *geräteunabhängige Pixel (Device-Independent Pixels* , Dips) bezeichnet werden. Eine DIP ist als 1/96-eines *logischen* Zoll definiert. In Direct2D werden alle Zeichnungsvorgänge in Dips angegeben und dann auf die aktuelle dpi-Einstellung skaliert.



| DPI-Einstellung | DIP-Größe    |
|-------------|-------------|
| 96          | 1 Pixel     |
| 120         | 1,25 Pixel |
| 144         | 1,5 Pixel  |



 

Wenn die dpi-Einstellung des Benutzers z. b. 144 dpi ist und Sie Direct2D zum Zeichnen eines 200 × 100-Rechtecks auffordern, wird das Rechteck 300 × 150 physischer Pixel sein. Außerdem misst DirectWrite Schriftgrößen in Dips anstelle von Punkten. Um eine Schriftart mit 12 Punkten zu erstellen, geben Sie 16 Dips an (12 Punkte = 1/6 logischer Zoll = 96/6 Dips). Wenn der Text auf dem Bildschirm gezeichnet wird, konvertiert Direct2D die Dips in physische Pixel. Der Vorteil dieses Systems besteht darin, dass die Maßeinheiten sowohl für Text als auch für Zeichnung konsistent sind, unabhängig von der aktuellen dpi-Einstellung.

Ein Wort mit Vorsicht: Maus-und Fenster Koordinaten werden immer noch in physischen Pixeln, nicht in Dips angegeben. Wenn Sie z. b. die [**WM- \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown) -Meldung verarbeiten, wird die MouseDown-Position in physischen Pixeln angegeben. Um einen Punkt an dieser Position zu zeichnen, müssen Sie die Pixelkoordinaten in Dips konvertieren.

## <a name="converting-physical-pixels-to-dips"></a>Umstellen physischer Pixel in Dips

Die Konvertierung von physischen Pixeln in Dips verwendet die folgende Formel.

<dl> Dips = Pixel/(dpi/96.0)  
</dl>

Um die dpi-Einstellung abzurufen, müssen Sie die [**ID2D1Factory:: getdesktopdpi**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) -Methode aufrufen. Der dpi-Wert wird als zwei Gleit Komma Werte zurückgegeben, eine für die x-Achse und eine für die y-Achse. Theoretisch können sich diese Werte unterscheiden. Berechnen Sie einen separaten Skalierungsfaktor für jede Achse.


```C++
float g_DPIScaleX = 1.0f;
float g_DPIScaleY = 1.0f;

void InitializeDPIScale(ID2D1Factory *pFactory)
{
    FLOAT dpiX, dpiY;

    pFactory->GetDesktopDpi(&dpiX, &dpiY);

    g_DPIScaleX = dpiX/96.0f;
    g_DPIScaleY = dpiY/96.0f;
}

template <typename T>
float PixelsToDipsX(T x)
{
    return static_cast<float>(x) / g_DPIScaleX;
}

template <typename T>
float PixelsToDipsY(T y)
{
    return static_cast<float>(y) / g_DPIScaleY;
}
```



Dies ist eine alternative Möglichkeit, die dpi-Einstellung zu erhalten, wenn Sie nicht Direct2D verwenden:


```C++
void InitializeDPIScale(HWND hwnd)
{
    HDC hdc = GetDC(hwnd);
    g_DPIScaleX = GetDeviceCaps(hdc, LOGPIXELSX) / 96.0f;
    g_DPIScaleY = GetDeviceCaps(hdc, LOGPIXELSY) / 96.0f;
    ReleaseDC(hwnd, hdc);
}
```
> [!Note]  
> Unter Windows 10, Version 1903, ist  [**ID2D1Factory:: getdesktopdpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) veraltet, und die Empfehlung lautet " [**Displayinformation:: logicaldpi**](/uwp/api/windows.graphics.display.displayinformation.logicaldpi?view=winrt-19041) for Windows Store Apps" oder " [**getdpiforwindow**](/windows/win32/api/winuser/nf-winuser-getdpiforwindow) " für Desktop-Apps. Wenn Sie Sie weiterhin verwenden möchten, unterdrücken Sie die Compilerfehlermeldung, indem Sie die Zeile [**#pragma Warnung (unterdrücken: 4996)**](/cpp/error-messages/compiler-warnings/compiler-warning-level-3-c4996?view=vs-2019) direkt vor dem [**ID2D1Factory:: getdesktopdpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) -Befehl schreiben. Obwohl dies nicht empfohlen wird, ist es möglich, das standardmäßige dpi-Bewusstsein mithilfe von [**setprocessdpiawareness Context**](/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext)Programm gesteuert festzulegen. Sobald ein Fenster (ein HWND) in Ihrem Prozess erstellt wurde, wird das Ändern des dpi-Informationsmodus nicht mehr unterstützt. Wenn Sie den Prozess-Standard-dpi-Informationsmodus Programm gesteuert festlegen, müssen Sie die entsprechende API vor dem Erstellen von HWNDs aufruft. Weitere Informationen finden Sie [unter Festlegen der Standard-dpi-Informationen für einen Prozess](../hidpi/setting-the-default-dpi-awareness-for-a-process.md).

## <a name="resizing-the-render-target"></a>Ändern der Größe des Renderziels

Wenn die Größe des Fensters geändert wird, müssen Sie die Größe des Renderziels entsprechend anpassen. In den meisten Fällen müssen Sie auch das Layout aktualisieren und das Fenster neu zeichnen. Der folgende Code zeigt diese Schritte.


```C++
void MainWindow::Resize()
{
    if (pRenderTarget != NULL)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(rc.right, rc.bottom);

        pRenderTarget->Resize(size);
        CalculateLayout();
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



Die [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect) -Funktion Ruft die neue Größe des Client Bereichs in physischen Pixeln (nicht Dips) ab. Die [**ID2D1HwndRenderTarget:: Resize**](../direct2d/id2d1hwndrendertarget-resize.md) -Methode aktualisiert die Größe des Renderziels, auch in Pixel angegeben. Die [**invalidatup**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) -Funktion erzwingt eine Umgestaltung durch Hinzufügen des gesamten Client Bereichs zum Aktualisierungs Bereich des Fensters. (Siehe zeichnen [des Fensters](painting-the-window.md)in Modul 1.)

Wenn das Fenster wächst oder verkleinert wird, müssen Sie in der Regel die Position der Objekte neu berechnen, die Sie zeichnen. Im kreisprogramm müssen z. b. der RADIUS und der Mittelpunkt aktualisiert werden:


```C++
void MainWindow::CalculateLayout()
{
    if (pRenderTarget != NULL)
    {
        D2D1_SIZE_F size = pRenderTarget->GetSize();
        const float x = size.width / 2;
        const float y = size.height / 2;
        const float radius = min(x, y);
        ellipse = D2D1::Ellipse(D2D1::Point2F(x, y), radius, radius);
    }
}
```



Die [**ID2D1RenderTarget:: GetSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getsize) -Methode gibt die Größe des Renderziels in Dips (nicht Pixel) zurück. Dies ist die geeignete Einheit zum Berechnen des Layouts. Es gibt eine eng verwandte Methode, [**ID2D1RenderTarget:: getpixelsize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelsize), die die Größe in physischen Pixeln zurückgibt. Für ein **HWND** -Renderziel entspricht dieser Wert der Größe, die von [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect)zurückgegeben wurde. Beachten Sie jedoch, dass das Zeichnen in Dips und nicht in Pixel erfolgt.

## <a name="next"></a>Nächste

[Verwenden von Color in Direct2D](using-color-in-direct2d.md)

 

 
