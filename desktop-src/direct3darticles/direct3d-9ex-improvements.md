---
title: Direct3D 9Ex-Verbesserungen
description: In diesem Thema wird die Unterstützung zusätzlicher Windows 7-Unterstützung für den Flip-Modus und die zugehörigen aktuellen Statistiken in Direct3D 9Ex und Desktopfenster-Manager beschrieben.
ms.assetid: cb92a162-57eb-4aee-af7a-c8ece37075a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42eef10b6caaa959cb750f073c97a0f665384463
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390774"
---
# <a name="direct3d-9ex-improvements"></a>Direct3D 9Ex-Verbesserungen

In diesem Thema wird die Unterstützung zusätzlicher Windows 7-Unterstützung für den Flip-Modus und die zugehörigen aktuellen Statistiken in Direct3D 9Ex und Desktopfenster-Manager beschrieben. Zielanwendungen sind Video-oder Frameraten basierte Präsentations Anwendungen. Anwendungen, die den Direct3D 9Ex-Flip-Modus verwenden, verringern die Systemressourcen Auslastung, wenn DWM aktiviert ist. Aktuelle Statistik Erweiterungen im Zusammenhang mit dem Flip-Modus ermöglichen es Direct3D 9Ex-Anwendungen, die Präsentations Rate besser zu steuern, indem Sie Echtzeitfeedback und Korrekturmechanismen bereitstellen. Ausführliche Erläuterungen und Zeiger auf Beispiel Ressourcen sind enthalten.

Dieses Thema enthält folgende Abschnitte:

-   [Verbesserte Informationen zu Direct3D 9Ex für Windows 7](#whats-improved-about-direct3d-9ex-for-windows-7)
-   [Direct3D 9Ex-Flip-Modus-Präsentation](#direct3d-9ex-flip-mode-presentation)
-   [Programmiermodell und APIs](#programming-model-and-apis)
    -   [So abonnieren Sie das Direct3D 9Ex-Flip-Modell](#how-to-opt-into-the-direct3d-9ex-flip-model)
    -   [Entwurfs Richtlinien für Direct3D 9Ex-Flip Model-Anwendungen](#design-guidelines-for-direct3d-9ex-flip-model-applications)
    -   [Frame Synchronisierung von Direct3D 9Ex-kippen-Modell Anwendungen](#frame-synchronization-of-direct3d-9ex-flip-model-applications)
    -   [Rahmen Synchronisierung für Fenster Anwendungen, wenn DWM deaktiviert ist](#frame-synchronization-for-windowed-applications-when-dwm-is-off)
-   [Exemplarische Vorgehensweise: Beispiel für ein Direct3D 9Ex-Flip-Modell und eine aktuelle Statistik](#walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample)
    -   [Zusammenfassung der Programmier Empfehlungen für die Frame-Synchronisierung](#summary-of-programming-recommendations-for-frame-synchronization)
-   [Schlussfolgerung zu Direct3D 9Ex-Verbesserungen](#conclusion-about-direct3d-9ex-improvements)
-   [Aktions Aufrufe](#call-to-action)
-   [Zugehörige Themen](#related-topics)

## <a name="whats-improved-about-direct3d-9ex-for-windows-7"></a>Verbesserte Informationen zu Direct3D 9Ex für Windows 7

Die Darstellung des Flip-Modus von Direct3D 9Ex ist ein verbesserter Modus für das darstellen von Bildern in Direct3D 9Ex, die gerenderte Bilder effizient an Windows 7 Desktopfenster-Manager (DWM) für die Komposition übergibt. Ab Windows Vista stellt DWM den gesamten Desktop dar. Wenn DWM aktiviert ist, stellen Fenster-modusanwendungen ihren Inhalt auf dem Desktop dar, indem Sie eine Methode namens BLT-Modus für dwm (oder BLT-Modell) verwenden. Beim BLT-Modell verwaltet DWM eine Kopie der gerenderten Direct3D 9Ex-Oberfläche für die Desktop Komposition. Wenn die Anwendung aktualisiert wird, wird der neue Inhalt über ein BLT auf die DWM-Oberfläche kopiert. Bei Anwendungen, die Direct3D-und GDI-Inhalte enthalten, werden die GDI-Daten auch auf die DWM-Oberfläche kopiert.

Der in Windows 7 verfügbare Flip-Modus für die DWM (oder das Flip-Modell) ist eine neue Präsentationsmethode, die im Wesentlichen das Übergeben von Handles von Anwendungs Oberflächen zwischen Anwendungen im Fenstermodus und DWM ermöglicht. Zusätzlich zum Speichern von Ressourcen unterstützt das Flip Model erweiterte vorhandene Statistiken.

Aktuelle Statistiken sind Informationen zur Rahmen Zeit, die Anwendungen verwenden können, um Video-und Audiostreams zu synchronisieren und die Wiederherstellung von Videowiedergabe-Störungen durchführen. Die Informationen zur Rahmen Zeitangabe in der aktuellen Statistik ermöglichen es Anwendungen, die Präsentations Rate ihrer Video Frames für eine reibungslosere Darstellung anzupassen. In Windows Vista, wo DWM eine entsprechende Kopie der Frame Oberfläche für die Desktop Komposition beibehält, können Anwendungen die von DWM bereitgestellten aktuellen Statistiken verwenden. Diese Methode zum Abrufen vorhandener Statistiken ist in Windows 7 für vorhandene Anwendungen weiterhin verfügbar.

In Windows 7 sollten Direct3D 9Ex-basierte Anwendungen, die ein Flip-Modell übernehmen, D3D9Ex-APIs verwenden, um aktuelle Statistiken abzurufen. Wenn DWM aktiviert ist, können der Fenstermodus und der exklusive Vollbildmodus Direct3D 9Ex-Anwendungen bei Verwendung von Flip Model die gleichen aktuellen Statistik Informationen erwarten. Direct3D 9Ex Flip Model Present Statistics ermöglicht Anwendungen, vorhandene Statistiken in Echtzeit abzufragen, statt den Frame auf dem Bildschirm anzuzeigen. die gleichen aktuellen Statistik Informationen sind für Flip-Model aktivierte Anwendungen im Fenstermodus als Vollbildanwendungen verfügbar. ein hinzugefügtes Flag in D3D9Ex-APIs ermöglicht das Kippen von Modell Anwendungen zum effektiven verwerfen späterer Frames zur Präsentationszeit.

Das Direct3D 9Ex-Flip-Modell sollte von neuen Video-oder Frameraten basierten Präsentations Anwendungen für Windows 7 verwendet werden. Aufgrund der Synchronisierung zwischen DWM und der Direct3D 9Ex-Laufzeit sollten Anwendungen, die das Flip Model verwenden, zwischen 2 und 4 backbuffers angeben, um eine reibungslose Darstellung sicherzustellen. Die Anwendungen, die aktuelle Statistik Informationen verwenden, profitieren von der Verwendung von Flip-Modellen, die Verbesserungen der Statistik

## <a name="direct3d-9ex-flip-mode-presentation"></a>Direct3D 9Ex-Flip-Modus-Präsentation

Leistungsverbesserungen für den Direct3D 9Ex-Flip-Modus sind im System wichtig, wenn DWM eingeschaltet ist und sich die Anwendung im Fenstermodus befindet und nicht im Vollbildmodus. In der folgenden Tabelle und Abbildung ist ein vereinfachter Vergleich der Speicher Bandbreiten-Verwendungen und der System Lese-und Schreibvorgänge von Fenster Anwendungen dargestellt, die das Modell kippen im Vergleich zum standardmäßigen BLT-Modell verwenden.



| BLT-Modus für DWM vorhanden                                                                                                 | D3D9Ex-Flip-Modus für DWM vorhanden                                             |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| 1. die Anwendung aktualisiert Ihren Frame (schreiben).<br/>                                                                 | 1. die Anwendung aktualisiert Ihren Frame (schreiben).<br/>                     |
| 2. Direct3D Runtime kopiert Oberflächen Inhalte in eine DWM-Umleitungs Oberfläche (lesen, schreiben)<br/>                       | 2. Direct3D Runtime übergibt die Anwendungsoberfläche an DWM<br/>        |
| 3. Nachdem die freigegebene Oberflächen Kopie abgeschlossen ist, rendert DWM die Anwendungsoberfläche auf dem Bildschirm (lesen, schreiben)<br/> | 3. DWM rendert die Anwendungsoberfläche auf dem Bildschirm (lesen, schreiben)<br/> |



 

![Abbildung eines Vergleichs zwischen dem BLT-Modell und dem Flip-Modell](images/blt-flip-mode-present.png)

Der Flip-Modus stellt die Systemspeicher Auslastung durch Verringern der Anzahl von Lese-und Schreibvorgängen durch die Direct3D-Laufzeit für die Zusammenstellung des Fensterrahmens durch DWM reduziert. Dadurch wird der System Energieverbrauch und die Gesamtspeicher Auslastung reduziert.

Anwendungen können den Direct3D 9Ex-Flip-Modus nutzen, wenn DWM eingeschaltet ist, und zwar unabhängig davon, ob sich die Anwendung im Fenstermodus oder im Vollbildmodus befindet.

## <a name="programming-model-and-apis"></a>Programmiermodell und APIs

Neue Video-oder Framerate: Wenn Anwendungen, die Direct3D 9Ex-APIs unter Windows 7 verwenden, genutzt werden können, kann der Arbeitsspeicher und die Energieeinsparung und die verbesserte Darstellung des Flip-Modus bei Ausführung unter Windows 7 genutzt werden. (Bei Ausführung unter früheren Windows-Versionen wird die Anwendung von der Direct3D-Laufzeit standardmäßig auf den BLT-Modus festgelegt.)

Der Flip-Modus ist erforderlich, wenn die Anwendung die Echt Zeit Statistik-Feedback-und Korrekturmechanismen nutzen kann, wenn DWM eingeschaltet ist. Anwendungen, die den Flip-Modus verwenden, sollten jedoch die Einschränkungen beachten, wenn Sie das gleichzeitige GDI-API-Rendering verwenden.

Sie können vorhandene Anwendungen so ändern, dass Sie den Modus "Flip-Modus" mit den gleichen Vorteilen und Einschränkungen wie die neu entwickelten Anwendungen nutzen.

### <a name="how-to-opt-into-the-direct3d-9ex-flip-model"></a>So abonnieren Sie das Direct3D 9Ex-Flip-Modell

Direct3D 9Ex-Anwendungen, die auf Windows 7 abzielen, können das Flip-Modell nutzen, indem Sie die Swapkette mit dem [**D3DSWAPEFFECT \_ flipex**](/windows/desktop/direct3d9/d3dswapeffect) -Enumerationswert erstellen. Um das Flip-Modell zu abonnieren, geben Anwendungen die [**D3DPRESENT \_ Parameters**](/windows/desktop/direct3d9/d3dpresent-parameters) -Struktur an und übergeben dann einen Zeiger auf diese Struktur, wenn Sie die [**IDirect3D9Ex:: deatedeviceex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) -API aufrufen. In diesem Abschnitt wird beschrieben, wie Anwendungen, die auf Windows 7 abzielen, **IDirect3D9Ex:: kreatedeviceex** verwenden, um das Flip-Modell zu abonnieren. Weitere Informationen zur **IDirect3D9Ex:: deatedeviceex** -API finden Sie auf der MSDN-Website unter **IDirect3D9Ex:: kreatedeviceex**.

Der Zweck wird die Syntax von [**D3DPRESENT \_ Parametern**](/windows/desktop/direct3d9/d3dpresent-parameters) und [**IDirect3D9Ex:: kreatedeviceex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) hier wiederholt.

``` syntax
HRESULT CreateDeviceEx(
  UINT Adapter,
  D3DDEVTYPE DeviceType,
  HWND hFocusWindow,
  DWORD BehaviorFlags,
  D3DPRESENT_PARAMETERS* pPresentationParameters,
  D3DDISPLAYMODEEX *pFullscreenDisplayMode,
  IDirect3DDevice9Ex **ppReturnedDeviceInterface
);
```

``` syntax
typedef struct D3DPRESENT_PARAMETERS {
    UINT BackBufferWidth, BackBufferHeight;
    D3DFORMAT BackBufferFormat;
    UINT BackBufferCount;
    D3DMULTISAMPLE_TYPE MultiSampleType;
    DWORD MultiSampleQuality;
    D3DSWAPEFFECT SwapEffect;
    HWND hDeviceWindow;
    BOOL Windowed;
    BOOL EnableAutoDepthStencil;
    D3DFORMAT AutoDepthStencilFormat;
    DWORD Flags;
    UINT FullScreen_RefreshRateInHz;
    UINT PresentationInterval;
} D3DPRESENT_PARAMETERS, *LPD3DPRESENT_PARAMETERS;
```

Wenn Sie Direct3D 9Ex-Anwendungen für Windows 7 ändern, um das Flip-Modell zu abonnieren, sollten Sie die folgenden Elemente zu den angegebenen Membern von [**D3DPRESENT- \_ Parametern**](/windows/desktop/direct3d9/d3dpresent-parameters)berücksichtigen:

<dl> <dt>

**BackBufferCount**
</dt> <dd>

(Nur Windows 7)

Wenn **SwapEffect** auf den neuen D3DSWAPEFFECT flipex-SwapChain-Effekt-Typ festgelegt ist \_ , sollte die zurück Puffer Anzahl gleich oder größer als 2 sein, um eine Anwendungsleistung zu verhindern, weil darauf gewartet wird, dass der vorherige aktuelle Puffer von DWM freigegeben wird.

Wenn die Anwendung auch aktuelle Statistiken verwendet, die D3DSWAPEFFECT \_ flipex zugeordnet sind, empfiehlt es sich, die zurück Puffer Anzahl auf von 2 auf 4 festzulegen.

Die Verwendung \_ von D3DSWAPEFFECT flipex unter Windows Vista oder früheren Betriebssystemversionen führt zu einem Fehler von " [**devatedeviceex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)".

</dd> <dt>

**SwapEffect verwenden**
</dt> <dd>

(Nur Windows 7)

Der neue D3DSWAPEFFECT \_ flipex-SwapChain-Effekt wird festgelegt, wenn eine Anwendung den Flip-Modus annimmt, der in DWM vorhanden ist. Dies ermöglicht es der Anwendung, den Arbeitsspeicher und die Leistung effizienter zu nutzen, und ermöglicht es der Anwendung, die voll Bild Anzeige im Fenstermodus zu nutzen. Das Verhalten von Vollbildanwendungen ist nicht betroffen. Wenn "Windowed" auf " **true** " festgelegt ist und " **Swap-Effekt** " auf D3DSWAPEFFECT flipex festgelegt ist \_ , erstellt die Laufzeit einen zusätzlichen Hintergrund Puffer und rotiert, welches Handle zu dem Puffer gehört, der zur Präsentationszeit zum Vordergrund Puffer wird.

</dd> <dt>

**Flags**
</dt> <dd>

(Nur Windows 7)

Das [D3DPRESENTFLAG \_ Lockable \_ BackBuffer](/windows/desktop/direct3d9/d3dpresentflag) -Flag kann nicht festgelegt werden, wenn SwapEffect auf den neuen [**D3DSWAPEFFECT \_ flipex**](/windows/desktop/direct3d9/d3dswapeffect) - **SwapChain** -Effekt-Typ festgelegt ist.

</dd> </dl>

### <a name="design-guidelines-for-direct3d-9ex-flip-model-applications"></a>Entwurfs Richtlinien für Direct3D 9Ex-Flip Model-Anwendungen

Verwenden Sie die Richtlinien in den folgenden Abschnitten, um Ihre Direct3D 9Ex-Flip-Modell Anwendungen zu entwerfen.

### <a name="use-flip-mode-present-in-a-separate-hwnd-from-blt-mode-present"></a>Verwenden des Flip-Modus, der in einem separaten HWND aus dem BLT-Modus vorhanden ist

Anwendungen sollten den Direct3D 9Ex-Flip-Modus verwenden, der in einem HWND enthalten ist, das nicht auch andere APIs als Ziel hat, einschließlich BLT-Modus Direct3D 9Ex, andere Versionen von Direct3D oder GDI. Der im Fenster "Kippen" vorhandene Modus kann verwendet werden, um untergeordnete Fenster anzuzeigen. Das heißt, Anwendungen können das Flip-Modell verwenden, wenn es nicht mit dem BLT-Modell im gleichen HWND gemischt wird, wie in den folgenden Abbildungen dargestellt.

![Darstellung des übergeordneten Fensters Direct3D und eines untergeordneten GDI-Fensters mit jeweils eigenem HWND](images/parent-d3d.png)

![Darstellung des übergeordneten GDI-Fensters und eines untergeordneten Direct3D-Fensters mit jeweils eigenem HWND](images/parent-gdi.png)

Da das BLT-Modell eine zusätzliche Kopie der Oberfläche beibehält, können GDI und andere Direct3D-Inhalte dem gleichen HWND durch schrittweise Updates von Direct3D und GDI hinzugefügt werden. Mit dem Flip-Modell werden nur Direct3D 9Ex-Inhalte in [**D3DSWAPEFFECT \_ flipex**](/windows/desktop/direct3d9/d3dswapeffect) -Austausch Ketten, die an DWM übermittelt werden, sichtbar. Alle anderen BLT-modellDirect3D-und GDI-Inhalts Aktualisierungen werden ignoriert, wie in den folgenden Abbildungen dargestellt.

![Abbildung des GDI-Texts, der möglicherweise nicht angezeigt wird, wenn das Modell Kippen verwendet wird und sich Direct3D-und GDI-Inhalt im gleichen HWND befinden](images/d3d-gdi-same-hwnd.png)

![Abbildung des Direct3D-und GDI-Inhalts, in dem DWM aktiviert ist und die Anwendung im Fenstermodus ausgeführt wird](images/d3d-gdinotext-same-hwnd.png)

Daher sollte das Flip-Modell für Swapketten-Puffer Oberflächen aktiviert werden, bei denen das Direct3D 9Ex-Flip-Modell allein auf das gesamte HWND gerendert wird.

### <a name="do-not-use-flip-model-with-gdis-scrollwindow-or-scrollwindowex"></a>Verwenden Sie "Flip Model" nicht mit dem "scrollwindow" oder "scrollwindowex" von GDI

Einige Direct3D 9Ex-Anwendungen verwenden die Funktionen scrollwindow oder scrollwindowex von GDI zum Aktualisieren von Fenster Inhalten, wenn ein Benutzer scrollereignis ausgelöst wird. Scrollwindow und scrollwindowex führen BLTS von Fenster Inhalten auf dem Bildschirm aus, während ein Fenster einen Bildlauf ausführt. Diese Funktionen erfordern auch BLT-Modell Updates für GDI und Direct3D 9Ex-Inhalt. Anwendungen, die eine der beiden Funktionen verwenden, zeigen nicht notwendigerweise sichtbare Fenster Inhalte auf dem Bildschirm an, wenn sich die Anwendung im Fenstermodus befindet und DWM aktiviert ist. Es wird empfohlen, die scrollwindow-und scrollwindowex-APIs von GDI nicht in Ihren Anwendungen zu verwenden und stattdessen ihren Inhalt auf dem Bildschirm neu zu zeichnen.

### <a name="use-one-d3dswapeffect_flipex-swap-chain-per-hwnd"></a>Verwenden Sie eine D3DSWAPEFFECT \_ flipex-Swap-Kette pro HWND.

Anwendungen, die das Flip-Modell verwenden, sollten nicht mehrere Flip-Modell Austausch Ketten verwenden, die auf das gleiche HWND abzielen.

### <a name="frame-synchronization-of-direct3d-9ex-flip-model-applications"></a>Frame Synchronisierung von Direct3D 9Ex-kippen-Modell Anwendungen

Aktuelle Statistiken sind Informationen zu Frame Timeouts, die Medienanwendungen zum Synchronisieren von Video-und Audiodatenströmen und zum Wiederherstellen von Videowiedergabe-Störungen verwenden. Um die Verfügbarkeit der aktuellen Statistik zu aktivieren, muss die Anwendung Direct3D 9Ex sicherstellen, dass der von der Anwendung an [**IDirect3D9Ex:: deatedeviceex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) übergebene Parameter " *verhaltenflags* " das geräteverhaltenflag [D3DCREATE " \_ \_ presentstats aktivieren](/windows/desktop/direct3d9/d3dcreate)" enthält.

Die Syntax von [**IDirect3D9Ex:: kreatedeviceex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) wird hier wiederholt.

``` syntax
HRESULT CreateDeviceEx(
  UINT Adapter,
  D3DDEVTYPE DeviceType,
  HWND hFocusWindow,
  DWORD BehaviorFlags,
  D3DPRESENT_PARAMETERS* pPresentationParameters,
  D3DDISPLAYMODEEX *pFullscreenDisplayMode,
  IDirect3DDevice9Ex **ppReturnedDeviceInterface
);
```

Das Direct3D 9Ex-Flip-Modell fügt das [D3DPRESENT \_ forceimvermittler](/windows/desktop/direct3d9/d3dpresent) -präsentationsflag hinzu, das das D3DPRESENT Interval-Verhalten der [ \_ \_ unmittelbaren](/windows/desktop/direct3d9/d3dpresent) Darstellung/Flag erzwingt. Die Anwendung Direct3D 9Ex gibt diese Präsentationsflags im *dwFlags* -Parameter an, den die Anwendung an [**IDirect3DDevice9Ex::P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex)übergibt, wie hier gezeigt.

``` syntax
HRESULT PresentEx(
  CONST RECT *pSourceRect,
  CONST RECT *pDestRect,
  HWND hDestWindowOverride,
  CONST RGNDATA *pDirtyRegion,
  DWORD dwFlags
);
```

Wenn Sie Ihre Direct3D 9Ex-Anwendung für Windows 7 ändern, sollten Sie die folgenden Informationen zu den angegebenen [D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) Presentation-Flags berücksichtigen:

<dl> <dt>

[D3DPRESENT \_ donotflip](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

Dieses Flag ist nur im Vollbildmodus verfügbar.

(Nur Windows 7)

Wenn die Anwendung den " **deviapeffect** "-Member von "D3DPRESENT"- [**\_ Parametern**](/windows/desktop/direct3d9/d3dpresent-parameters) in einem [**Aufrufen von "**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) [**" für " \_ "**](/windows/desktop/direct3d9/d3dswapeffect) auf "" festlegt.

</dd> <dt>

[D3DPRESENT \_ forceimvermittlung](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

(Nur Windows 7)

Dieses Flag kann nur angegeben werden, wenn die Anwendung den " **deviapeffect** "-Member der [**D3DPRESENT- \_ Parameter**](/windows/desktop/direct3d9/d3dpresent-parameters) auf " [**D3DSWAPEFFECT \_ flipex**](/windows/desktop/direct3d9/d3dswapeffect) " in einem Aufrufen von " [**kreatedeviceex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)" festlegt. Die Anwendung kann dieses Flag verwenden, um eine Oberfläche mit mehreren Frames zu einem späteren Zeitpunkt in der vorhandenen DWM-Warteschlange zu aktualisieren, wobei im Grunde zwischen Frames übersprungen werden.

Fenster mit flipex-aktivierten Anwendungen können mit diesem Flag sofort eine Oberfläche mit einem Frame aktualisieren, der später in der DWM-Warteschlange vorhanden ist, und zwischen Frames übersprungen. Dies ist besonders nützlich für Medienanwendungen, die Frames verwerfen möchten, die als spät erkannt wurden, und die nachfolgenden Frames zum Zeitpunkt der Komposition darstellen. [**IDirect3DDevice9Ex::P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) gibt einen Fehler wegen eines ungültigen Parameters zurück, wenn dieses Flag nicht ordnungsgemäß angegeben ist.

</dd> </dl>

Zum Abrufen der aktuellen Statistik Informationen erhält die Anwendung die [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) -Struktur durch Aufrufen der [**IDirect3DSwapChain9Ex:: getpresentstatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) -API.

Die [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) -Struktur enthält Statistiken zu [**IDirect3DDevice9Ex::P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) -aufrufen. Das Gerät muss mithilfe eines [**IDirect3D9Ex:: ":: kreatedeviceex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) "- [Aufrufes mit dem D3DCREATE \_ enable \_ presentstats](/windows/desktop/direct3d9/d3dcreate) -Flag erstellt werden. Andernfalls sind die von [**getpresentstatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) zurückgegebenen Daten nicht definiert. Eine mit einem Flip-Modell aktivierte Direct3D 9Ex-Swapkette stellt aktuelle Statistik Informationen sowohl im Fenstermodus als auch im Vollbildmodus bereit.

Für BLT-Model-aktivierte Direct3D 9Ex-Swapketten im Fenstermodus werden alle [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) -Struktur Werte als Nullen verwendet.

Für eine flipex-Statistik gibt [**getpresentstatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) \_ \_ \_ in den folgenden Situationen eine Disjunktion der D3DERR Present Statistics zurück:

-   Zuerst Aufrufen von [**getpresentstatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) , was den Anfang einer Sequenz anzeigt
-   DWM-Übergang von on zu Off
-   Modusänderung: entweder der Fenstermodus zum oder vom Vollbildmodus oder vom Vollbildmodus bis zum voll Bild Übergang

Die Syntax von [**getpresentstatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) wird hier wiederholt.

``` syntax
HRESULT GetPresentStatistics(
  D3DPRESENTSTATS * pPresentationStatistics
);
```

Die [**IDirect3DSwapChain9Ex:: getlastpresentcount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) -Methode gibt den letzten presentcount zurück, d. h. die aktuelle ID des letzten erfolgreichen Aufrufens, der von einem Anzeigegerät erfolgt ist, das der Swapkette zugeordnet ist. Diese vorhandene ID ist der Wert des **presentcount** -Members der [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) -Struktur. Bei BLT-Modell fähigen Direct3D 9Ex-Swapketten werden im Fenstermodus alle **D3DPRESENTSTATS** -Struktur Werte als Nullen verwendet.

Die Syntax von [**IDirect3DSwapChain9Ex:: getlastpresentcount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) wird hier wiederholt.

``` syntax
HRESULT GetLastPresentCount(
  UINT * pLastPresentCount
);
```

Wenn Sie Ihre Direct3D 9Ex-Anwendung für Windows 7 ändern, sollten Sie die folgenden Informationen zur [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) -Struktur berücksichtigen:

-   Der von [**getlastpresentcount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) zurückgegebene presentcount-Wert wird nicht aktualisiert, wenn ein im dwFlags-Parameter angegebener [**presentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) -Befehl mit D3DPRESENT \_ donotwait einen Fehler zurückgibt. 
-   Wenn [**presentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) mit D3DPRESENT \_ donotflip aufgerufen wird, wird ein [**getpresentstatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) -Aufruf erfolgreich ausgeführt, aber es wird keine aktualisierte [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) -Struktur zurückgegeben, wenn sich die Anwendung im Fenstermodus befindet.
-   **Presentfreshcount** im Vergleich zu **synkrefreshcount** in [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats):
    -   **Presentfreshcount** ist gleich **synkrefreshcount** , wenn die Anwendung bei jeder VSYNC-Funktion dargestellt wird.
    -   **Synkrefreshcount** wird im VSYNC-Intervall abgerufen, wenn der vorhandene gesendet wurde. **syncqpctime** ist ungefähr die Zeit, die dem VSYNC-Intervall zugeordnet ist.

``` syntax
typedef struct _D3DPRESENTSTATS {
    UINT PresentCount;
    UINT PresentRefreshCount;
    UINT SyncRefreshCount;
    LARGE_INTEGER SyncQPCTime;
    LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```

### <a name="frame-synchronization-for-windowed-applications-when-dwm-is-off"></a>Rahmen Synchronisierung für Fenster Anwendungen, wenn DWM deaktiviert ist

Wenn DWM deaktiviert ist, werden Fenster Anwendungen direkt auf dem Bildschirm Monitor angezeigt, ohne dass eine Flip-Kette durchlaufen wird. In Windows Vista wird die Beschaffung von Frame Statistik Informationen für Fenster Anwendungen nicht unterstützt, wenn DWM deaktiviert ist. Um eine API zu verwalten, bei der Anwendungen nicht DWM-fähig sein müssen, gibt Windows 7 Frame Statistik Informationen für Fenster Anwendungen zurück, wenn DWM deaktiviert ist. Die bei Deaktivierung von DWM zurückgegebene Frame Statistik sind nur Schädigungen.

## <a name="walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample"></a>Walk-Through eines Direct3D 9Ex-Flip-Modells und präsentieren von Statistik Beispielen

**So abonnieren Sie die flipex-Präsentation für Direct3D 9Ex Sample**

1.  Stellen Sie sicher, dass die Beispielanwendung unter Windows 7 oder einer höheren Version des Betriebssystems ausgeführt wird.
2.  Legen Sie in einem Aufrufen von " [**fiatedeviceex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)" den Member " **Swap** " von [**D3DPRESENT- \_ Parametern**](/windows/desktop/direct3d9/d3dpresent-parameters) auf [**D3DSWAPEFFECT \_ flipex**](/windows/desktop/direct3d9/d3dswapeffect) fest.


```C++
    OSVERSIONINFO version;
    ZeroMemory(&version, sizeof(version));
    version.dwOSVersionInfoSize = sizeof(version);
    GetVersionEx(&version);
    
    // Sample would run only on Win7 or higher
    // Flip Model present and its associated present statistics behavior are only available on Windows 7 or higher operating system
    bool bIsWin7 = (version.dwMajorVersion > 6) || 
        ((version.dwMajorVersion == 6) && (version.dwMinorVersion >= 1));

    if (!bIsWin7)
    {
        MessageBox(NULL, L"This sample requires Windows 7 or higher", NULL, MB_OK);
        return 0;
    }
```



**Zum Abonnieren von flipex zugeordnete Statistik für Direct3D 9Ex Sample**

-   Set [D3DCREATE \_ Aktivieren Sie \_ presentstats](/windows/desktop/direct3d9/d3dcreate) im *verhaltenflags* -Parameter von " [**kreatedeviceex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)".


```C++
    // Set up the structure used to create the D3DDevice
    D3DPRESENT_PARAMETERS d3dpp;
    ZeroMemory(&d3dpp, sizeof(d3dpp));

    d3dpp.Windowed = TRUE;
    d3dpp.SwapEffect = D3DSWAPEFFECT_FLIPEX;        // Opts into Flip Model present for D3D9Ex swapchain
    d3dpp.BackBufferFormat = D3DFMT_X8R8G8B8;
    d3dpp.BackBufferWidth = 256;                
    d3dpp.BackBufferHeight = 256;
    d3dpp.BackBufferCount = QUEUE_SIZE;
    d3dpp.PresentationInterval = D3DPRESENT_INTERVAL_ONE;

    g_iWidth = d3dpp.BackBufferWidth;
    g_iHeight = d3dpp.BackBufferHeight;

    // Create the D3DDevice with present statistics enabled - set D3DCREATE_ENABLE_PRESENTSTATS for behaviorFlags parameter
    if(FAILED(g_pD3D->CreateDeviceEx(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                      D3DCREATE_HARDWARE_VERTEXPROCESSING | D3DCREATE_ENABLE_PRESENTSTATS,
                                      &d3dpp, NULL, &g_pd3dDevice)))
    {
        return E_FAIL;
    }
```



**So vermeiden Sie das erkennen und Wiederherstellen von Störungen**

1.  Warteschlangen Aufrufe vorhanden: die empfohlene Swapkette-Anzahl liegt zwischen 2 und 4.
2.  Direct3D 9Ex Sample fügt einen impliziten Swapkette hinzu, die tatsächliche Warteschlangen Länge ist die Swapkette-Anzahl + 1.
3.  Erstellen Sie eine Warteschlangen Struktur, um alle der aktuellen ID (presentcount) und zugeordnete, berechnete/erwartete presentaktualisierungzahl zu speichern.
4.  So erkennen Sie das Auftreten eines Ereignisses:

    -   Aufrufen von [**getpresentstatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)).
    -   Dient zum Ermitteln der aktuellen ID (presentcount) und der VSYNC-Anzahl, bei der der Frame (presenterfrischendes count) des Frames angezeigt wird, dessen aktuelle Statistik abgerufen wird.
    -   Rufen Sie die erwartete presentaktualisierungzahl (targetrefresh im Beispielcode) ab, die mit der aktuellen ID verknüpft ist.
    -   Wenn die tatsächliche presentaktuellem Anzahl später als erwartet ist, ist ein Fehler aufgetreten.

5.  So stellen Sie eine Wiederherstellung nach einem Fehler:

    -   Berechnen Sie, wie viele Frames übersprungen werden sollen (g \_ iunmittelates Variable im Beispielcode).
    -   Präsentieren Sie die übersprungenen Frames mit Interval D3DPRESENT \_ forceimvermittler.

**Überlegungen zur Erkennung und Wiederherstellung von Störung**

1.  Die glitch-Wiederherstellung nimmt N (g \_ iqueuedelay-Variable im Beispielcode) Anzahl der aktuellen Aufrufe an, wobei n (g \_ iqueuedelay) dem Wert g \_ iunmittelates plus length der aktuellen Warteschlange entspricht, d. h.:

    -   Überspringen von Frames mit vorhandenes Intervall D3DPRESENT \_ forceimvermittler, plus
    -   In der Warteschlange befindliche präsente, die verarbeitet werden müssen

2.  Legen Sie eine Beschränkung auf die Länge des zulässigen Werts fest (das Limit für die \_ Wiederherstellung \_ in Stichproben). Wenn die Beispielanwendung keine Wiederherstellung nach einem zu langen Fehler (d. h. 1 Sekunde oder 60 vsyncs auf dem 60Hz-Monitor) durchgeführt werden kann, überspringen Sie die periodische Animation, und setzen Sie die vorhandene hilfswarteschlange zurück.


```C++
VOID Render()
{
    g_pd3dDevice->Clear(0, NULL, D3DCLEAR_TARGET, D3DCOLOR_XRGB(0, 0, 0), 1.0f, 0);

    g_pd3dDevice->BeginScene();

    // Compute new animation parameters for time and frame based animations

    // Time-based is a difference between base and current SyncRefreshCount
    g_aTimeBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_LastSyncRefreshCount - g_SyncRefreshCount;
    // Frame-based is incrementing frame value
    g_aFrameBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_iFrameNumber;

    RenderBlurredMesh(TRUE);    // Time-based
    RenderBlurredMesh(FALSE);   // Frame-based

    g_iBlurHistoryCounter = (g_iBlurHistoryCounter + 1) % BLUR_FRAMES;

    DrawText();

    g_pd3dDevice->EndScene();

    // Performs glitch recovery if glitch was detected
    if (g_bGlitchRecovery && (g_iImmediates > 0))
    {
        // If we have present immediates queued as a result of glitch detected, issue forceimmediate Presents for glitch recovery 
        g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_FORCEIMMEDIATE);
        g_iImmediates--;
        g_iShowingGlitchRecovery = MESSAGE_SHOW;
    }
    // Otherwise, Present normally
    else
    {
        g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, 0);
    }

    // Add to helper Present queue: PresentID + expected present refresh count of last submitted Present
    UINT PresentCount;
    g_pd3dSwapChain->GetLastPresentCount(&PresentCount);
    g_Queue.QueueFrame(PresentCount, g_TargetRefreshCount);
    
    // QueueDelay specifies # Present calls to be processed before another glitch recovery attempt
    if (g_iQueueDelay > 0)
    {
        g_iQueueDelay--;
    }

    if (g_bGlitchRecovery)
    {
        // Additional DONOTFLIP presents for frame conversions, which basically follows the same logic, but without rendering
        for (DWORD i = 0; i < g_iDoNotFlipNum; i++)
        {
            if (g_TargetRefreshCount != -1)
            {
                g_TargetRefreshCount++;
                g_iFrameNumber++;
                g_aTimeBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_LastSyncRefreshCount - g_SyncRefreshCount;
                g_aFrameBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_iFrameNumber;
                g_iBlurHistoryCounter = (g_iBlurHistoryCounter + 1) % BLUR_FRAMES;
            }
            
            if (g_iImmediates > 0)
            {
                g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_FORCEIMMEDIATE | D3DPRESENT_DONOTFLIP);
                g_iImmediates--;
            }
            else
            {
                g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_DONOTFLIP);
            }
            UINT PresentCount;
            g_pd3dSwapChain->GetLastPresentCount(&PresentCount);
            g_Queue.QueueFrame(PresentCount, g_TargetRefreshCount);

            if (g_iQueueDelay > 0)
            {
                g_iQueueDelay--;
            }
        }
    }

    // Check Present Stats info for glitch detection 
    D3DPRESENTSTATS PresentStats;

    // Obtain present statistics information for successfully displayed presents
    HRESULT hr = g_pd3dSwapChain->GetPresentStats(&PresentStats);

    if (SUCCEEDED(hr))
    {
        // Time-based update
        g_LastSyncRefreshCount = PresentStats.SyncRefreshCount;
        if ((g_SyncRefreshCount == -1) && (PresentStats.PresentCount != 0))
        {
            // First time SyncRefreshCount is reported, use it as base
            g_SyncRefreshCount = PresentStats.SyncRefreshCount;
        }

        // Fetch frame from the queue...
        UINT TargetRefresh = g_Queue.DequeueFrame(PresentStats.PresentCount);

        // If PresentStats returned a really old frame that we no longer have in the queue, just don't do any glitch detection
        if (TargetRefresh == FRAME_NOT_FOUND)
            return;

        if (g_TargetRefreshCount == -1)
        {
            // This is first time issued frame is confirmed by present stats, so fill target refresh count for all frames in the queue
            g_TargetRefreshCount = g_Queue.FillRefreshCounts(PresentStats.PresentCount, g_SyncRefreshCount);
        } 
        else
        {
            g_TargetRefreshCount++;
            g_iFrameNumber++;

            // To determine whether we're glitching, see if our estimated refresh count is confirmed
            // if the frame is displayed later than the expected vsync count
            if (TargetRefresh < PresentStats.PresentRefreshCount)
            {
                // then, glitch is detected!

                // If glitch is too big, don't bother recovering from it, just jump animation
                if ((PresentStats.PresentRefreshCount - TargetRefresh) > GLITCH_RECOVERY_LIMIT)
                {
                    g_iStartFrame += PresentStats.SyncRefreshCount - g_SyncRefreshCount;
                    ResetAnimation();
                    if (g_bGlitchRecovery)
                        g_iGlitchesInaRow++;    
                } 
                // Otherwise, compute number of immediate presents to recover from it -- if we?re not still trying to recover from another glitch
                else if (g_iQueueDelay == 0)
                {
                      // skip frames to catch up to expected refresh count
                    g_iImmediates = PresentStats.PresentRefreshCount - TargetRefresh;
                    // QueueDelay specifies # Present calls before another glitch recovery 
                    g_iQueueDelay = g_iImmediates + QUEUE_SIZE;
                    if (g_bGlitchRecovery)
                        g_iGlitchesInaRow++;
                }
            }
            else
            {
                // No glitch, reset glitch count
                g_iGlitchesInaRow = 0;
            }
        }
    }
    else if (hr == D3DERR_PRESENT_STATISTICS_DISJOINT)
    {
        // D3DERR_PRESENT_STATISTICS_DISJOINT means measurements should be started from the scratch (could be caused by mode change or DWM on/off transition)
        ResetAnimation();
    }

    // If we got too many glitches in a row, reduce framerate conversion factor (that is, render less frames)
    if (g_iGlitchesInaRow == FRAMECONVERSION_GLITCH_LIMIT)
    {
        if (g_iDoNotFlipNum < FRAMECONVERSION_LIMIT)
        {
            g_iDoNotFlipNum++;
        }
        g_iGlitchesInaRow = 0;
        g_iShowingDoNotFlipBump = MESSAGE_SHOW;
    }
}
```



**Beispielszenario**

-   In der folgenden Abbildung ist eine Anwendung mit einer backpufferanzahl von 4 dargestellt. Die tatsächliche Warteschlangen Länge ist daher 5.

    ![Abbildung der von einem applicas gerenderten Frames und der aktuellen Warteschlange](images/sample-scenario.png)

    Frame A ist darauf ausgerichtet, bei der Synchronisierungs Intervall Anzahl von 1 auf den Bildschirm zu wechseln, aber es wurde erkannt, dass die Synchronisierungs Intervall Anzahl von 4 angezeigt wurde. Daher ist ein Fehler aufgetreten. Nachfolgende 3 Rahmen werden mit D3DPRESENT \_ Interval \_ forceimvermittler präsentiert. Der Fehler muss insgesamt acht vorhandene Aufrufe annehmen, bevor er wieder hergestellt wird. der nächste Frame wird gemäß der angegebenen Synchronisierungs Intervall Anzahl angezeigt.

### <a name="summary-of-programming-recommendations-for-frame-synchronization"></a>Zusammenfassung der Programmier Empfehlungen für die Frame-Synchronisierung

-   Erstellen Sie eine Sicherungsliste aller lastpresentcount-IDs (abgerufen über [**getlastpresentcount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount)) und der zugeordneten geschätzten presenterfrischendes-Anzahl aller übermittelten über Mitt lungs-IDs.
    > [!Note]  
    > Wenn die Anwendung einen [**presentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) mit D3DPRESENT \_ donotflip aufruft, wird der [**getpresentstatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) -Aufruf erfolgreich ausgeführt, aber es wird keine aktualisierte [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) -Struktur zurückgegeben, wenn sich die Anwendung im Fenstermodus befindet.

     

-   Rufen Sie [**getpresentstatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) auf, um die tatsächliche presentaktualzahl zu erhalten, die den einzelnen vorhandenen IDs der angezeigten Frames zugeordnet ist, um sicherzustellen, dass die Anwendung Fehler Rückgaben aus dem-Befehl behandelt.
-   Wenn die tatsächliche presentaktuellem Anzahl nach der geschätzten Anzahl der Present-Werte liegt, wird eine Störung erkannt. Kompensieren Sie durch das Übermitteln von zurückliegenden Frames mit D3DPRESENT \_ forceimvermittler.
-   Wenn ein Frame in der aktuellen Warteschlange spät angezeigt wird, werden alle nachfolgenden Frames in der Warteschlange später angezeigt. D3DPRESENT \_ forceimvermittlung korrigiert nur den nächsten Frame, der nach allen in der Warteschlange befindlichen Frames angezeigt werden soll. Daher sollte die vorhandene Warteschlange oder die backpufferanzahl nicht zu lang sein. Daher gibt es weniger Frame-gleitungen, mit denen Sie sich abfangen können. Die optimale Puffer Anzahl ist 2 bis 4.
-   Wenn die geschätzte presentaktuellem Anzahl nach der tatsächlichen presenterfrischen-Anzahl liegt, ist möglicherweise eine DWM-Drosselung aufgetreten. Folgende Lösungen sind möglich:

    -   Reduzieren der aktuellen Warteschlangen Länge
    -   Reduzieren der GPU-Speicheranforderungen auf andere Weise, außer der Verringerung der aktuellen Warteschlangen Länge (d. h. der absteigenden Qualität, der Entfernung von Effekten usw.)
    -   Angeben von [**dwmenablemmcss**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenablemmcss) zum Verhindern der DWM-Drosselung im allgemeinen

-   Überprüfen Sie die Anwendungs Anzeige Funktionalität und die Leistung von Frame Statistiken in den folgenden Szenarien:

    -   mit DWM ein-und ausschalten
    -   Vollbildmodus für exklusive und Fenster
    -   geringere Funktions Hardware

-   Wenn Anwendungen eine große Anzahl von glitscherten Frames mit D3DPRESENT \_ forceimvermittlung nicht wiederherstellen können, können Sie möglicherweise die folgenden Vorgänge ausführen:

    -   reduzieren Sie die CPU-und GPU-Nutzung durch Rendering mit weniger Arbeitsauslastung.
    -   im Fall von Video Decodierung sollten Sie schneller decodieren, indem Sie Qualität und somit CPU-und GPU-Auslastung verringern.

## <a name="conclusion-about-direct3d-9ex-improvements"></a>Schlussfolgerung zu Direct3D 9Ex-Verbesserungen

Unter Windows 7 können Anwendungen, die während der Präsentation Video-oder Messgeräte Frameraten anzeigen, das Kippen von Modellen beschließen. Die aktuellen Verbesserungen der Statistik, die dem Flip-Modell zugeordnet sind Direct3D 9Ex können Anwendungen profitieren, die die Präsentation pro Frame-Rate synchronisieren, mit Echtzeitfeedback für die Erkennung und Wiederherstellung von Daten. Entwickler, die das Direct3D 9Ex-Flip-Modell übernehmen, sollten das Ziel eines separaten HWND von GDI-Inhalten und der Frameraten Synchronisierung berücksichtigen. Weitere Informationen finden Sie in diesem Thema und in der MSDN-Dokumentation. Weitere Dokumentationen finden Sie unter [DirectX Developer Center auf MSDN](/previous-versions/windows/apps/hh452744(v=win.10)).

## <a name="call-to-action"></a>Call-to-Action

Wir empfehlen Ihnen, das Direct3D 9Ex-Flip-Modell und seine aktuellen Statistiken unter Windows 7 zu verwenden, wenn Sie Anwendungen erstellen, die versuchen, die Präsentations Frame Rate zu synchronisieren oder nach Anzeige Abrufe wiederherzustellen.

## <a name="related-topics"></a>Zugehörige Themen

[DirectX Developer Center auf MSDN](/previous-versions/windows/apps/hh452744(v=win.10))
</dt> </dl>