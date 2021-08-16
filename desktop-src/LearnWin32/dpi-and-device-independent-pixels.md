---
title: DPI und Device-Independent Pixel
ms.assetid: d282de02-62f4-4a12-a77c-f602f6db0216
description: Weitere Informationen finden Sie unter DPI und Device-Independent Pixel.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9b3aebca97ac466f5158b07d1d976994030b4ba2c83b361a5d7a6d88b572fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118388346"
---
# <a name="dpi-and-device-independent-pixels"></a>DPI und Device-Independent Pixel

Um effektiv mit Windows programmieren zu können, müssen Sie zwei verwandte Konzepte verstehen:

-   Punkte pro Zoll (DPI)
-   Geräteunabhängiges Pixel (DEVICE-Independent Pixel, DIPs).

Beginnen wir mit DPI. Dies erfordert einen kurzen Umweg in die Typografie. In der Typografie wird die Größe des Typs in Einheiten gemessen, die als Punkte *bezeichnet werden.* Ein Punkt entspricht 1/72 Zoll.

<dl> 1 Pt = 1/72 Zoll  
</dl>

> [!Note]  
> Dies ist die Desktopveröffentlichungsdefinition des Punkts. In der Vergangenheit hat sich das genaue Maß eines Punkts variiert.

 

Beispielsweise ist eine 12-Punkt-Schriftart so konzipiert, dass sie in eine 1/6"-Textzeile (12/72) passt. Dies bedeutet natürlich nicht, dass jedes Zeichen in der Schriftart genau 1/6" hoch ist. Tatsächlich sind einige Zeichen möglicherweise größer als 1/6". In vielen Schriftarten ist das Zeichen DURCHSCHNITTLICH höher als die nominale Höhe der Schriftart. Um ordnungsgemäß angezeigt zu werden, benötigt die Schriftart zusätzlichen Platz zwischen dem Text. Dieser Bereich wird als führende *bezeichnet.*

Die folgende Abbildung zeigt eine 72-Punkt-Schriftart. Die soliden Linien zeigen einen hohen Begrenzungsfeld von 1" um den Text. Die gestrichelte Linie wird als Baseline *bezeichnet.* Die meisten Zeichen in einer Schriftart ruhen auf der Baseline. Die Höhe der Schriftart umfasst den Teil über der Baseline (den *Anstieg)* und den Teil unterhalb der Baseline (das *Abstiegsszenario).* In der hier gezeigten Schriftart beträgt der Anstieg 56 Punkte und der Abstieg 16 Punkte.

![Eine Abbildung, die eine 72-Punkt-Schriftart zeigt.](images/graphics11.png)

Wenn es jedoch um eine Computeranzeige geht, ist die Messung der Textgröße problematisch, da Pixel nicht alle dieselbe Größe aufweisen. Die Größe eines Pixels hängt von zwei Faktoren ab: der Anzeigeauflösung und der physischen Größe des Monitors. Daher sind physische Zoll kein nützliches Measure, da es keine feste Beziehung zwischen physischen Zoll und Pixeln gibt. Stattdessen werden Schriftarten in *logischen Einheiten* gemessen. Eine 72-Punkt-Schriftart ist als 1 logischer Zoll hoch definiert. Logische Zoll werden dann in Pixel konvertiert. Für viele Jahre Windows folgende Konvertierung verwendet: Ein logischer Zoll entspricht 96 Pixel. Mit diesem Skalierungsfaktor wird eine Schriftart mit 72 Punkten als 96 Pixel hoch gerendert. Eine 12-Punkt-Schriftart ist 16 Pixel hoch.

<dl> 12 Punkte = 12/72 logischer Zoll = 1/6 logischer Zoll = 96/6 Pixel = 16 Pixel  
</dl>

Dieser Skalierungsfaktor wird als 96 Punkte pro Zoll (DPI) beschrieben. Der Begriff Punkte leitet sich vom Drucken ab, bei dem physische Ink-Punkte auf Papier gedruckt werden. Bei Computeranzeigen wäre es genauer, 96 Pixel pro logischem Zoll zu sagen, aber der Begriff DPI ist hängen geblieben.

Da die tatsächlichen Pixelgrößen variieren, ist text, der auf einem Monitor lesbar ist, auf einem anderen Monitor möglicherweise zu klein. Außerdem haben Benutzer unterschiedliche Einstellungen– einige bevorzugen größeren Text. Aus diesem Grund ermöglicht Windows, die DPI-Einstellung zu ändern. Wenn der Benutzer beispielsweise die Anzeige auf 144 DPI festgelegt, ist eine Schriftart mit 72 Punkten 144 Pixel hoch. Die DPI-Standardeinstellungen sind 100 % (96 DPI), 125 % (120 DPI) und 150 % (144 DPI). Der Benutzer kann auch eine benutzerdefinierte Einstellung anwenden. Ab Windows 7 ist DPI eine Einstellung pro Benutzer.

## <a name="dwm-scaling"></a>DWM-Skalierung

Wenn ein Programm DPI nicht berücksichtigt, können die folgenden Fehler bei Einstellungen mit hohem DPI-Grad erkennbar sein:

-   Beschnittene Benutzeroberflächenelemente.
-   Falsches Layout.
-   Pixelierte Bitmaps und Symbole.
-   Falsche Mauskoordinaten, die sich auf Treffertests, Drag & Drop usw. auswirken können.

Um sicherzustellen, dass ältere Programme mit Hohen DPI-Einstellungen funktionieren, implementiert das DWM ein nützliches Fallback. Wenn ein Programm nicht als DPI-bewusst markiert ist, skaliert das DWM die gesamte Benutzeroberfläche entsprechend der DPI-Einstellung. Bei 144 DPI wird die Benutzeroberfläche beispielsweise um 150 % skaliert, einschließlich Text, Grafiken, Steuerelementen und Fenstergrößen. Wenn das Programm ein Fenster mit 500 × 500 erstellt, wird das Fenster tatsächlich als 750 × 750 Pixel angezeigt, und der Inhalt des Fensters wird entsprechend skaliert.

Dieses Verhalten bedeutet, dass ältere Programme bei Einstellungen mit hohem DPI-Grad "einfach funktionieren". Die Skalierung führt jedoch auch zu einer etwas unscharfen Darstellung, da die Skalierung angewendet wird, nachdem das Fenster gezeichnet wurde.

## <a name="dpi-aware-applications"></a>DPI-Aware Anwendungen

Um eine DWM-Skalierung zu vermeiden, kann sich ein Programm selbst als DPI-bewusst markieren. Dies weist das DWM an, keine automatische DPI-Skalierung durchzuführen. Alle neuen Anwendungen sollten DPI-bewusst sein, da das DPI-Bewusstsein die Darstellung der Benutzeroberfläche bei höheren DPI-Einstellungen verbessert.

Ein Programm deklariert sich selbst über sein Anwendungsmanifest als DPI-bewusst. Ein *Manifest ist* einfach eine XML-Datei, die eine DLL oder Anwendung beschreibt. Das Manifest ist in der Regel in die ausführbare Datei eingebettet, obwohl es als separate Datei bereitgestellt werden kann. Ein Manifest enthält Informationen wie DLL-Abhängigkeiten, die angeforderte Berechtigungsebene und die Version Windows, für die das Programm entworfen wurde.

Um zu deklarieren, dass Ihr Programm DPI-bewusst ist, fügen Sie die folgenden Informationen in das Manifest ein.

``` syntax
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
      <dpiAware>true</dpiAware>
    </asmv3:windowsSettings>
  </asmv3:application>
</assembly>
```

Die hier gezeigte Auflistung ist nur ein teilielles Manifest, aber der Visual Studio generiert den Rest des Manifests automatisch für Sie. Um ein partielles Manifest in Ihr Projekt ein-/aus- zu schließen, führen Sie die folgenden Schritte in Visual Studio.

1.  Klicken Sie **Project** Menü auf **Eigenschaft**.
2.  Erweitern Sie im linken Bereich **Konfigurationseigenschaften,** erweitern Sie **Manifesttool,** und klicken Sie dann auf **Eingabe und Ausgabe.**
3.  Geben Sie **im Textfeld Zusätzliche Manifestdateien** den Namen der Manifestdatei ein, und klicken Sie dann auf **OK.**

Indem Sie Ihr Programm als DPI-bewusst markieren, geben Sie dem DWM an, ihr Anwendungsfenster nicht zu skalieren. Wenn Sie nun ein Fenster mit 500 × 500 erstellen, belegt das Fenster unabhängig von der DPI-Einstellung des Benutzers 500 × 500 Pixel.

## <a name="gdi-and-dpi"></a>GDI und DPI

Die GDI-Zeichnung wird in Pixel gemessen. Das bedeutet, dass das resultierende Rechteck 200 Pixel breit und 100 Pixel groß ist, wenn Ihr Programm als DPI-bewusst markiert ist und Sie GDI bitten, ein 200 × 100-Rechteck zu zeichnen. GDI-Schriftgrößen werden jedoch auf die aktuelle DPI-Einstellung skaliert. Anders ausgedrückt: Wenn Sie eine Schriftart mit 72 Punkten erstellen, beträgt die Größe der Schriftart 96 Pixel bei 96 DPI, aber 144 Pixel bei 144 DPI. Hier ist eine 72-Punkt-Schriftart, die mit 144 DPI mit GDI gerendert wird.

![Ein Diagramm, das die DPI-Schriftskalierung in gdi zeigt.](images/graphics12.png)

Wenn Ihre Anwendung DPI-bewusst ist und Sie GDI zum Zeichnen verwenden, skalieren Sie alle Ihre Zeichnungskoordinaten so, dass sie mit dem DPI übereinstimmen.

## <a name="direct2d-and-dpi"></a>Direct2D und DPI

Direct2D führt automatisch eine Skalierung durch, um der DPI-Einstellung zu passen. In Direct2D werden Koordinaten in Einheiten gemessen, die als *geräteunabhängige Pixel (DEVICE-Independent Pixels,* DIPs) bezeichnet werden. Eine DIP ist als 1/96. eines *logischen Zolls* definiert. In Direct2D werden alle Zeichnungsvorgänge in DIPs angegeben und dann auf die aktuelle DPI-Einstellung skaliert.



| DPI-Einstellung | DIP-Größe    |
|-------------|-------------|
| 96          | 1 Pixel     |
| 120         | 1,25 Pixel |
| 144         | 1,5 Pixel  |



 

Wenn die DPI-Einstellung des Benutzers beispielsweise 144 DPI beträgt und Sie Direct2D auffordern, ein Rechteck mit 200 × 100 zu zeichnen, beträgt das Rechteck 300 × 150 physische Pixel. Darüber hinaus misst DirectWrite Schriftgrad in DIPs anstelle von Punkten. Um eine 12-Punkt-Schriftart zu erstellen, geben Sie 16 DIPs an (12 Punkte = 1/6 logischer Zoll = 96/6 DIPs). Wenn der Text auf dem Bildschirm gezeichnet wird, konvertiert Direct2D die DIPs in physische Pixel. Der Vorteil dieses Systems ist, dass die Maßeinheiten für Text und Zeichnung unabhängig von der aktuellen DPI-Einstellung konsistent sind.

Vorsicht: Maus- und Fensterkoordinaten werden weiterhin in physischen Pixeln angegeben, nicht in DIPs. Wenn Sie z. B. die [**\_ WM-LBUTTONDOWN-Nachricht**](/windows/desktop/inputdev/wm-lbuttondown) verarbeiten, wird die Mauszeigerposition in physischen Pixeln angegeben. Um einen Punkt an dieser Position zu zeichnen, müssen Sie die Pixelkoordinaten in DIPs konvertieren.

## <a name="converting-physical-pixels-to-dips"></a>Konvertieren physischer Pixel in DIPs

Bei der Konvertierung von physischen Pixeln in DIPs wird die folgende Formel verwendet.

<dl> DIPs = Pixel / (DPI/96.0)  
</dl>

Um die DPI-Einstellung abzurufen, rufen Sie die [**ID2D1Factory::GetDesktopDpi-Methode**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) auf. Der DPI wird als zwei Gleitkommawerte zurückgegeben, einer für die x-Achse und einer für die y-Achse. Theoretisch können sich diese Werte unterscheiden. Berechnen Sie einen separaten Skalierungsfaktor für jede Achse.


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



Dies ist eine alternative Möglichkeit, die DPI-Einstellung abzurufen, wenn Sie Direct2D nicht verwenden:


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
> Auf Windows 10 Version 1903 ist [**ID2D1Factory::GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) veraltet, und die Empfehlung lautet [**DisplayInformation::LogicalDpi**](/uwp/api/windows.graphics.display.displayinformation.logicaldpi?view=winrt-19041) für Windows Store Apps oder [**GetDpiForWindow**](/windows/win32/api/winuser/nf-winuser-getdpiforwindow) für Desktop-Apps. Wenn Sie sie weiterhin verwenden möchten, unterdrücken Sie die Compilerfehlermeldung, indem Sie die Zeile [**#pragma Warning(suppress: 4996)**](/cpp/error-messages/compiler-warnings/compiler-warning-level-3-c4996?view=vs-2019) direkt vor dem [**ID2D1Factory::GetDesktopDpi-Aufruf**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) schreiben. Obwohl dies nicht empfohlen wird, ist es möglich, die DPI-Standarderkennung programmgesteuert mit [**SetProcessDpiAwarenessContext**](/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext)festzulegen. Sobald ein Fenster (ein HWND) in Ihrem Prozess erstellt wurde, wird das Ändern des DPI-Erkennungsmodus nicht mehr unterstützt. Wenn Sie den Prozessstandard-DPI-Modus programmgesteuert festlegen, müssen Sie die entsprechende API aufrufen, bevor HWNDs erstellt wurden. Weitere Informationen finden Sie unter [Festlegen der DPI-Standarderkennung für einen Prozess.](../hidpi/setting-the-default-dpi-awareness-for-a-process.md)

## <a name="resizing-the-render-target"></a>Ändern der Größe des Renderziels

Wenn sich die Größe des Fensters ändert, müssen Sie die Größe des Renderziels entsprechend ändern. In den meisten Fällen müssen Sie auch das Layout aktualisieren und das Fenster neu malieren. Der folgende Code zeigt diese Schritte.


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



Die [**GetClientRect-Funktion**](/windows/desktop/api/winuser/nf-winuser-getclientrect) ruft die neue Größe des Clientbereichs in physischen Pixeln (nicht in DIPs) ab. Die [**ID2D1HwndRenderTarget::Resize-Methode**](../direct2d/id2d1hwndrendertarget-resize.md) aktualisiert die Größe des Renderziels, das ebenfalls in Pixel angegeben ist. Die [**InvalidateRect-Funktion**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) erzwingt einen erneuten Strich, indem der gesamte Clientbereich dem Updatebereich des Fensters hinzugefügt wird. (Siehe [Zeichnen des Fensters](painting-the-window.md)in Modul 1.)

Wenn das Fenster vergrößert oder verkleinert wird, müssen Sie in der Regel die Position der gezeichneten Objekte neu berechnen. Beispielsweise müssen im Kreisprogramm der Radius und der Mittelpunkt aktualisiert werden:


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



Die [**ID2D1RenderTarget::GetSize-Methode**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getsize) gibt die Größe des Renderziels in DIPs (nicht Pixel) zurück. Dies ist die geeignete Einheit zum Berechnen des Layouts. Es gibt eine eng verwandte Methode, [**ID2D1RenderTarget::GetPixelSize,**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelsize)die die Größe in physischen Pixeln zurückgibt. Bei einem **HWND-Renderziel** entspricht dieser Wert der von [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect)zurückgegebenen Größe. Denken Sie jedoch daran, dass das Zeichnen in DIPs und nicht in Pixeln erfolgt.

## <a name="next"></a>Nächste

[Verwenden von Farben in Direct2D](using-color-in-direct2d.md)

 

 
