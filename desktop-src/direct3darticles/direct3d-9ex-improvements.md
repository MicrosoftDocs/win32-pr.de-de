---
title: Direct3D 9Ex-Verbesserungen
description: In diesem Thema wird Windows 7-Unterstützung für den flip-Modus Present und die zugehörigen aktuellen Statistiken in Direct3D 9Ex und Desktopfenster-Manager.
ms.assetid: cb92a162-57eb-4aee-af7a-c8ece37075a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3221b805f07408b27e19a00a42ca0c4733ea725bd32a51b5b3e340b48d2070f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118796992"
---
# <a name="direct3d-9ex-improvements"></a>Direct3D 9Ex-Verbesserungen

In diesem Thema wird Windows 7-Unterstützung für den flip-Modus Present und die zugehörigen aktuellen Statistiken in Direct3D 9Ex und Desktopfenster-Manager. Zielanwendungen umfassen Video- oder Bildfrequenz-basierte Präsentationsanwendungen. Anwendungen, die direct3D 9Ex Flip Mode Present verwenden, verringern die Systemressourcenauslastung, wenn DWM aktiviert ist. Aktuelle Statistikverbesserungen im Zusammenhang mit Flip Mode Present ermöglichen Direct3D 9Ex-Anwendungen, die Präsentationsrate besser zu steuern, indem Sie Echtzeitfeedback und Korrekturmechanismen bereitstellen. Ausführliche Erläuterungen und Zeiger auf Beispielressourcen sind enthalten.

Dieses Thema enthält folgende Abschnitte:

-   [Verbesserungen an Direct3D 9Ex für Windows 7](#whats-improved-about-direct3d-9ex-for-windows-7)
-   [Direct3D 9EX Flip Mode Presentation](#direct3d-9ex-flip-mode-presentation)
-   [Programmiermodell und APIs](#programming-model-and-apis)
    -   [Verwenden des Direct3D 9Ex Flip-Modells](#how-to-opt-into-the-direct3d-9ex-flip-model)
    -   [Entwurfsrichtlinien für Direct3D 9Ex Flip Model-Anwendungen](#design-guidelines-for-direct3d-9ex-flip-model-applications)
    -   [Framesynchronisierung von Direct3D 9Ex Flip Model-Anwendungen](#frame-synchronization-of-direct3d-9ex-flip-model-applications)
    -   [Framesynchronisierung für Fensteranwendungen, wenn DWM deaktiviert ist](#frame-synchronization-for-windowed-applications-when-dwm-is-off)
-   [Exemplarische Vorgehensweise für ein Direct3D 9Ex-Flip-Modell und ein Beispiel für eine aktuelle Statistik](#walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample)
    -   [Zusammenfassung der Programmierungseinstellungen Empfehlungen Framesynchronisierung](#summary-of-programming-recommendations-for-frame-synchronization)
-   [Schlussfolgerung zu Direct3D 9Ex-Verbesserungen](#conclusion-about-direct3d-9ex-improvements)
-   [Handlungsaufruf](#call-to-action)
-   [Zugehörige Themen](#related-topics)

## <a name="whats-improved-about-direct3d-9ex-for-windows-7"></a>Verbesserungen an Direct3D 9Ex für Windows 7

Flip Mode Presentation of Direct3D 9Ex ist ein verbesserter Modus zum Präsentieren von Bildern in Direct3D 9Ex, der gerenderte Bilder effizient an Windows 7 Desktopfenster-Manager (DWM) zur Komposition übergibt. Ab Windows Vista erstellt DWM den gesamten Desktop. Wenn DWM aktiviert ist, stellen Anwendungen im Fenstermodus ihren Inhalt auf dem Desktop mithilfe einer Methode namens Blt Mode Present to DWM (oder Blt Model) vor. Mit dem Blt-Modell verwaltet DWM eine Kopie der gerenderten Direct3D 9Ex-Oberfläche für die Desktopkomposition. Wenn die Anwendung aktualisiert wird, wird der neue Inhalt über blt auf die DWM-Oberfläche kopiert. Bei Anwendungen, die Direct3D- und GDI-Inhalte enthalten, werden die GDI-Daten auch auf die DWM-Oberfläche kopiert.

Verfügbar in Windows 7, Flip Mode Present to DWM (oder Flip Model) ist eine neue Präsentationsmethode, die im Wesentlichen die Übergabe von Handles von Anwendungsoberflächen zwischen Anwendungen im Fenstermodus und DWM ermöglicht. Zusätzlich zum Speichern von Ressourcen unterstützt Flip Model erweiterte aktuelle Statistiken.

Aktuelle Statistiken sind Frame-Timing-Informationen, mit denen Anwendungen Video- und Audiostreams synchronisieren und nach Videowiedergabefehlern wiederherstellen können. Die Frame-Timing-Informationen in aktuellen Statistiken ermöglichen Es Anwendungen, die Präsentationsrate ihrer Videoframes für eine reibungslosere Darstellung anzupassen. In Windows Vista, wo DWM eine entsprechende Kopie der Frameoberfläche für die Desktopkomposition verwaltet, können Anwendungen aktuelle Statistiken verwenden, die von DWM bereitgestellt werden. Diese Methode zum Abrufen vorhandener Statistiken ist weiterhin in Windows 7 für vorhandene Anwendungen verfügbar.

In Windows 7 sollten Direct3D 9Ex-basierte Anwendungen, die Flip Model übernehmen, D3D9Ex-APIs verwenden, um aktuelle Statistiken zu erhalten. Wenn DWM aktiviert ist, können Direct3D 9Ex-Anwendungen im Fenstermodus und im exklusiven Vollbildmodus dieselben aktuellen Statistikinformationen erwarten, wenn sie Flip Model verwenden. Direct3D 9Ex Flip Model present statistics (Direct3D 9Ex-Flip-Modell– Vorhandene Statistiken) ermöglicht Es Anwendungen, aktuelle Statistiken in Echtzeit und nicht erst nach der Anzeige des Frames auf dem Bildschirm abfragt zu können. die gleichen aktuellen Statistikinformationen sind für Fenstermodus-Flip-Model Anwendungen als Vollbildanwendungen verfügbar. Ein hinzugefügtes Flag in D3D9Ex-APIs ermöglicht Flip Model-Anwendungen, späte Frames zur Präsentationszeit effektiv zu verwerfen.

Direct3D 9Ex Flip Model sollte von neuen Video- oder Bildfrequenz-basierten Präsentationsanwendungen verwendet werden, die auf Windows 7. Aufgrund der Synchronisierung zwischen DWM und der Direct3D 9Ex-Runtime sollten Anwendungen, die Flip Model verwenden, zwischen 2 und 4 Backbuffer angeben, um eine reibungslose Darstellung sicherzustellen. Anwendungen, die aktuelle Statistikinformationen verwenden, profitieren von der Verwendung von Flip Model enabled (Flip-Modell aktiviert), um Statistikverbesserungen zu erhalten.

## <a name="direct3d-9ex-flip-mode-presentation"></a>Direct3D 9EX Flip Mode Presentation

Leistungsverbesserungen des Direct3D 9Ex-Flip-Modus sind auf dem System wichtig, wenn DWM aktiviert ist und sich die Anwendung im Fenstermodus befindet, und nicht im exklusiven Vollbildmodus. Die folgende Tabelle und Abbildung zeigen einen vereinfachten Vergleich der Speicherbandbreitenauslastungen und Systemlese- und -schreibvorgänge von Fensteranwendungen, die Flip Model und das Standardverwendungs-Blt-Modell auswählen.



| Blt-Modus für DWM vorhanden                                                                                                 | D3D9Ex Flip Mode Present to DWM                                             |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| 1. Die Anwendung aktualisiert ihren Rahmen (Schreiben)<br/>                                                                 | 1. Die Anwendung aktualisiert ihren Rahmen (Schreiben)<br/>                     |
| 2. Direct3D-Runtime kopiert Oberflächeninhalte auf eine DWM-Umleitungsoberfläche (Lesen, Schreiben)<br/>                       | 2. Direct3D-Runtime übergibt die Anwendungsoberfläche an DWM<br/>        |
| 3. Nach Abschluss der freigegebenen Oberflächenkopie rendert DWM die Anwendungsoberfläche auf dem Bildschirm (Lesen, Schreiben).<br/> | 3. DWM rendert die Anwendungsoberfläche auf dem Bildschirm (Lesen, Schreiben)<br/> |



 

![Abbildung eines Vergleichs des Blt-Modells und des Flip-Modells](images/blt-flip-mode-present.png)

Flip Mode Present reduziert die Systemspeicherauslastung, indem die Anzahl der Lese- und Schreibvorgänge durch die Direct3D-Runtime für die Fensterrahmenkomposition von DWM reduziert wird. Dies reduziert den Systemverbrauch und die Gesamtspeicherauslastung.

Anwendungen können den Direct3D 9Ex Flip-Modus nutzen, um Statistikverbesserungen anzuzeigen, wenn DWM aktiviert ist, unabhängig davon, ob sich die Anwendung im Fenstermodus oder im exklusiven Vollbildmodus befindet.

## <a name="programming-model-and-apis"></a>Programmiermodell und APIs

Neue Video- oder Bildfrequenz-Gaußging-Anwendungen, die Direct3D 9Ex-APIs auf Windows 7 verwenden, können von den Speicher- und Energieeinsparungen sowie von der verbesserten Darstellung profitieren, die der Flip-Modus bietet, wenn er auf Windows 7 ausgeführt wird. (Bei der Ausführung unter Windows Versionen wird die Anwendung von der Direct3D-Runtime standardmäßig auf den Blt-Modus Present festgelegt.)

Flip Mode Present (Vorhandener Flip-Modus) bedeutet, dass die Anwendung echtzeitbasiertes Feedback zu Statistiken und Korrekturmechanismen nutzen kann, wenn DWM aktiviert ist. Anwendungen, die den flip-Modus Present verwenden, sollten sich jedoch der Einschränkungen bewusst sein, wenn sie gleichzeitiges GDI-API-Rendering verwenden.

Sie können vorhandene Anwendungen so ändern, dass sie den flip-Modus Present nutzen, mit den gleichen Vorteilen und Einschränkungen wie die neu entwickelten Anwendungen.

### <a name="how-to-opt-into-the-direct3d-9ex-flip-model"></a>Verwenden des Direct3D 9Ex Flip-Modells

Direct3D 9Ex-Anwendungen, die Windows 7 als Ziel haben, können das Flip-Modell verwenden, indem sie die Swapkette mit dem [**D3DSWAPEFFECT \_ FLIPEX-Enumerationswert**](/windows/desktop/direct3d9/d3dswapeffect) erstellen. Um das Flip-Modell zu verwenden, geben Anwendungen die [**D3DPRESENT \_ PARAMETERS-Struktur**](/windows/desktop/direct3d9/d3dpresent-parameters) an und übergeben dann einen Zeiger auf diese Struktur, wenn sie die [**IDirect3D9Ex::CreateDeviceEx-API**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) aufrufen. In diesem Abschnitt wird beschrieben, wie Anwendungen, die Windows 7 als Ziel haben, **IDirect3D9Ex::CreateDeviceEx** verwenden, um das Flip-Modell zu verwenden. Weitere Informationen zur **IDirect3D9Ex::CreateDeviceEx-API** finden Sie unter **IDirect3D9Ex::CreateDeviceEx auf MSDN.**

Der Einfachheit halber wird die Syntax [**von D3DPRESENT \_ PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) und [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) hier wiederholt.

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

Wenn Sie Direct3D 9Ex-Anwendungen für Windows 7 ändern, um das Flip-Modell zu verwenden, sollten Sie folgende Punkte zu den angegebenen Membern von [**D3DPRESENT \_ PARAMETERS berücksichtigen:**](/windows/desktop/direct3d9/d3dpresent-parameters)

<dl> <dt>

**BackBufferCount**
</dt> <dd>

(Windows 7)

Wenn **SwapEffect** auf den neuen Swap Chain Effect-Typ D3DSWAPEFFECT FLIPEX festgelegt ist, sollte die Anzahl der Zurückpuffer gleich oder größer als 2 sein, um leistungsschädigende Anwendungsleistung zu verhindern, weil darauf gewartet wird, dass der vorherige Present-Puffer von DWM freigegeben \_ wird.

Wenn die Anwendung auch aktuelle Statistiken verwendet, die D3DSWAPEFFECT FLIPEX zugeordnet sind, wird empfohlen, die Anzahl der Zurückpuffer auf 2 bis \_ 4 zu setzen.

Die Verwendung von D3DSWAPEFFECT FLIPEX unter Windows Vista oder früheren Betriebssystemversionen gibt einen Fehler \_ von [**CreateDeviceEx zurück.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)

</dd> <dt>

**SwapEffect**
</dt> <dd>

(Windows 7)

Der neue D3DSWAPEFFECT FLIPEX Swap Chain Effect-Effekttyp gibt an, wann eine Anwendung den \_ Flip-Modus für DWM einschlägt. Sie ermöglicht der Anwendung eine effizientere Nutzung von Arbeitsspeicher und Leistung und ermöglicht es der Anwendung auch, die Vorteile der im Fenstermodus dargestellten Statistiken im Vollbildmodus zu nutzen. Das Verhalten der Vollbildanwendung ist nicht betroffen. Wenn Windowed auf **TRUE** und **SwapEffect** auf D3DSWAPEFFECT FLIPEX festgelegt ist, erstellt die Runtime einen zusätzlichen Backpuffer und rotiert das handle, das zum Puffer gehört, der zur Präsentationszeit zum Frontpuffer \_ wird.

</dd> <dt>

**Flags**
</dt> <dd>

(Windows 7)

Das [Flag D3DPRESENTFLAG \_ LOCKABLE \_ BACKBUFFER](/windows/desktop/direct3d9/d3dpresentflag) kann nicht festgelegt werden, wenn **SwapEffect** auf den neuen Swap Chain Effect-Typ [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) festgelegt ist.

</dd> </dl>

### <a name="design-guidelines-for-direct3d-9ex-flip-model-applications"></a>Entwurfsrichtlinien für Direct3D 9Ex Flip Model-Anwendungen

Verwenden Sie die Richtlinien in den folgenden Abschnitten, um Ihre Direct3D 9Ex Flip Model-Anwendungen zu entwerfen.

### <a name="use-flip-mode-present-in-a-separate-hwnd-from-blt-mode-present"></a>Verwenden des Flip-Modus, der in einem separaten HWND vom blt-Modus vorhanden ist

Anwendungen sollten den Direct3D 9Ex Flip-Modus verwenden, der in einem HWND vorhanden ist, das nicht auch von anderen APIs als Ziel verwendet wird, z. B. Blt Mode Present Direct3D 9Ex, andere Versionen von Direct3D oder GDI. Vorhandener Flip-Modus kann verwendet werden, um untergeordneten Fenstern zu präsentieren. Das heißt, Anwendungen können Flip Model verwenden, wenn es nicht mit Blt Model im selben HWND gemischt wird, wie in den folgenden Abbildungen gezeigt.

![Abbildung des übergeordneten Direct3d-Fensters und eines untergeordneten gdi-Fensters mit jeweils einem eigenen hwnd](images/parent-d3d.png)

![Abbildung des übergeordneten gdi-Fensters und eines untergeordneten Direct3D-Fensters mit jeweils einem eigenen hwnd](images/parent-gdi.png)

Da das Blt-Modell eine zusätzliche Kopie der Oberfläche verwaltet, können GDI- und andere Direct3D-Inhalte demselben HWND durch stückliche Updates von Direct3D und GDI hinzugefügt werden. Bei Verwendung des Flip-Modells sind nur Direct3D 9Ex-Inhalte in [**D3DSWAPEFFECT \_ FLIPEX-Swapketten**](/windows/desktop/direct3d9/d3dswapeffect) sichtbar, die an DWM übergeben werden. Alle anderen Inhaltsupdates für Blt Model Direct3D oder GDI werden ignoriert, wie in den folgenden Abbildungen dargestellt.

![Abbildung von gdi-Text, der möglicherweise nicht angezeigt wird, wenn ein Flip-Modell verwendet wird und sich direct3d- und gdi-Inhalt im gleichen hwnd befinden](images/d3d-gdi-same-hwnd.png)

![Abbildung von direct3d- und gdi-Inhalten, bei denen dwm aktiviert ist und sich die Anwendung im Fenstermodus befindet](images/d3d-gdinotext-same-hwnd.png)

Daher sollte Flip Model für Pufferoberflächen der Austauschkette aktiviert werden, bei denen das Direct3D 9Ex Flip Model allein im gesamten HWND gerendert wird.

### <a name="do-not-use-flip-model-with-gdis-scrollwindow-or-scrollwindowex"></a>Verwenden Sie das Flip-Modell nicht mit dem GDI-BildlaufWindow oder ScrollWindowEx.

Einige Direct3D 9Ex-Anwendungen verwenden die GDI-Funktionen ScrollWindow oder ScrollWindowEx, um Fensterinhalte zu aktualisieren, wenn ein Benutzerscrollereignis ausgelöst wird. ScrollWindow und ScrollWindowEx führen Blts von Fensterinhalten auf dem Bildschirm aus, wenn ein Fenster gescrollt wird. Diese Funktionen erfordern auch Blt-Modellupdates für GDI- und Direct3D 9Ex-Inhalte. Anwendungen, die beide Funktionen verwenden, zeigen nicht unbedingt sichtbaren Fensterinhalt an, der auf dem Bildschirm scrollt, wenn sich die Anwendung im Fenstermodus befindet und DWM aktiviert ist. Es wird empfohlen, die ScrollWindow- und ScrollWindowEx-APIs von GDI nicht in Ihren Anwendungen zu verwenden und stattdessen den Inhalt auf dem Bildschirm neu zu zeichnen, um einen Bildlauf durchzuführen.

### <a name="use-one-d3dswapeffect_flipex-swap-chain-per-hwnd"></a>Verwenden einer \_ D3DSWAPEFFECT-FLIPEX-Swapkette pro HWND

Anwendungen, die Flip Model verwenden, sollten nicht mehrere Flip Model-Swapketten verwenden, die auf denselben HWND ausgerichtet sind.

### <a name="frame-synchronization-of-direct3d-9ex-flip-model-applications"></a>Framesynchronisierung von Direct3D 9Ex Flip Model-Anwendungen

Aktuelle Statistiken sind Frame-Zeitsteuerungsinformationen, mit denen Medienanwendungen Video- und Audiostreams synchronisieren und nach Störungen bei der Videowiedergabe wiederherstellen können. Um die Verfügbarkeit vorhandener Statistiken zu ermöglichen, muss die Direct3D 9Ex-Anwendung sicherstellen, dass der *BehaviorFlags-Parameter,* den die Anwendung an [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) übergibt, das Geräteverhaltensflag [D3DCREATE \_ ENABLE \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate)enthält.

Der Einfachheit halber wird die Syntax von [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) hier wiederholt.

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

Direct3D 9Ex Flip Model fügt das [D3DPRESENT \_ FORCEIMMEDIATE-Präsentationsflag](/windows/desktop/direct3d9/d3dpresent) hinzu, das das Verhalten des [D3DPRESENT \_ INTERVAL IMMEDIATE-Präsentationsflags \_ ](/windows/desktop/direct3d9/d3dpresent) erzwingt. Die Direct3D 9Ex-Anwendung gibt diese Präsentationsflags im *dwFlags-Parameter* an, den die Anwendung an [**IDirect3DDevice9Ex::P resentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex)übergibt, wie hier gezeigt.

``` syntax
HRESULT PresentEx(
  CONST RECT *pSourceRect,
  CONST RECT *pDestRect,
  HWND hDestWindowOverride,
  CONST RGNDATA *pDirtyRegion,
  DWORD dwFlags
);
```

Wenn Sie Ihre Direct3D 9Ex-Anwendung für Windows 7 ändern, sollten Sie die folgenden Informationen zu den angegebenen [D3DPRESENT-Präsentationsflags](/windows/desktop/direct3d9/d3dpresent) berücksichtigen:

<dl> <dt>

[D3DPRESENT \_ DONOTFLIP](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

Dieses Flag ist nur im Vollbildmodus oder verfügbar.

(nur Windows 7)

, wenn die Anwendung den **SwapEffect-Member** von [**D3DPRESENT \_ PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) in einem Aufruf von [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)auf [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) festlegt.

</dd> <dt>

[D3DPRESENT \_ FORCEIMMEDIATE](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

(nur Windows 7)

Dieses Flag kann nur angegeben werden, wenn die Anwendung den **SwapEffect-Member** von [**D3DPRESENT \_ PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) in einem Aufruf von [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)auf [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) festlegt. Die Anwendung kann dieses Flag verwenden, um eine Oberfläche mit mehreren Frames später in der DWM Present-Warteschlange sofort zu aktualisieren, wobei im Wesentlichen Zwischenframes übersprungen werden.

FlipEx-fähige Anwendungen mit Fenstern können dieses Flag verwenden, um eine Oberfläche sofort mit einem Frame zu aktualisieren, der sich später in der DWM Present-Warteschlange befindet, wobei Zwischenframes übersprungen werden. Dies ist besonders nützlich für Medienanwendungen, die Frames verwerfen möchten, die erst spät erkannt wurden und nachfolgende Frames zur Kompositionszeit darstellen. [**IDirect3DDevice9Ex::P resentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) gibt einen Ungültigen Parameterfehler zurück, wenn dieses Flag nicht ordnungsgemäß angegeben ist.

</dd> </dl>

Um aktuelle Statistikinformationen abzurufen, ruft die Anwendung die [**D3DPRESENTSTATS-Struktur**](/windows/desktop/direct3d9/d3dpresentstats) ab, indem sie die [**IDirect3DSwapChain9Ex::GetPresentStatistics-API aufruft.**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85))

Die [**D3DPRESENTSTATS-Struktur**](/windows/desktop/direct3d9/d3dpresentstats) enthält Statistiken zu [**IDirect3DDevice9Ex::P resentEx-Aufrufen.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) Das Gerät muss mithilfe eines [**IDirect3D9Ex::CreateDeviceEx-Aufrufs**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) mit dem [D3DCREATE \_ ENABLE \_ PRESENTSTATS-Flag](/windows/desktop/direct3d9/d3dcreate) erstellt werden. Andernfalls sind die von [**GetPresentStatistics zurückgegebenen**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) Daten nicht definiert. Eine Flip-Model-fähige Direct3D 9Ex-Swapkette stellt sowohl im Fenstermodus als auch im Vollbildmodus aktuelle Statistikinformationen bereit.

Bei Blt-Model-fähigen Direct3D 9Ex-Swapketten im Fenstermodus sind alle [**D3DPRESENTSTATS-Strukturwerte**](/windows/desktop/direct3d9/d3dpresentstats) Nullen.

Für aktuelle FlipEx-Statistiken gibt [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) D3DERR \_ PRESENT STATISTICS \_ \_ DISJOINT in den folgenden Situationen zurück:

-   Erster Aufruf von [**GetPresentStatistics,**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) der den Anfang einer Sequenz angibt
-   Dwm transition from on to off (DWM-Übergang von ein zu aus)
-   Modusänderung: Entweder im Fenstermodus oder von Vollbild- oder Vollbild- zu Vollbildübergängen

Der Einfachheit halber wird die Syntax von [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) hier wiederholt.

``` syntax
HRESULT GetPresentStatistics(
  D3DPRESENTSTATS * pPresentationStatistics
);
```

Die [**IDirect3DSwapChain9Ex::GetLastPresentCount-Methode**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) gibt den letzten PresentCount zurück, d. h. die Present-ID des letzten erfolgreichen Present-Aufrufs, der von einem Anzeigegerät durchgeführt wurde, das der Austauschkette zugeordnet ist. Diese Present-ID ist der Wert des **PresentCount-Elements** der [**D3DPRESENTSTATS-Struktur.**](/windows/desktop/direct3d9/d3dpresentstats) Bei Blt-Model-fähigen Direct3D 9Ex-Swapketten sind im Fenstermodus alle **D3DPRESENTSTATS-Strukturwerte** Nullen.

Der Einfachheit halber wird die Syntax von [**IDirect3DSwapChain9Ex::GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) hier wiederholt.

``` syntax
HRESULT GetLastPresentCount(
  UINT * pLastPresentCount
);
```

Wenn Sie Ihre Direct3D 9Ex-Anwendung für Windows 7 ändern, sollten Sie die folgenden Informationen zur [**D3DPRESENTSTATS-Struktur**](/windows/desktop/direct3d9/d3dpresentstats) berücksichtigen:

-   Der PresentCount-Wert, den [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) zurückgibt, wird nicht aktualisiert, wenn ein [**PresentEx-Aufruf**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) mit D3DPRESENT \_ DONOTWAIT, der im *dwFlags-Parameter* angegeben ist, einen Fehler zurückgibt.
-   Wenn [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) mit D3DPRESENT \_ DONOTFLIP aufgerufen wird, ist ein [**GetPresentStatistics-Aufruf**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) erfolgreich, gibt aber keine aktualisierte [**D3DPRESENTSTATS-Struktur**](/windows/desktop/direct3d9/d3dpresentstats) zurück, wenn sich die Anwendung im Fenstermodus befindet.
-   **PresentRefreshCount** im Vergleich zu **SyncRefreshCount** in [**D3DPRESENTSTATS:**](/windows/desktop/direct3d9/d3dpresentstats)
    -   **PresentRefreshCount** ist gleich **SyncRefreshCount,** wenn die Anwendung auf jeder vsync präsentiert.
    -   **SyncRefreshCount** wird im vsync-Intervall abgerufen, als das aktuelle übermittelt wurde. **SyncQPCTime** entspricht ungefähr der Zeit, die dem vsync-Intervall zugeordnet ist.

``` syntax
typedef struct _D3DPRESENTSTATS {
    UINT PresentCount;
    UINT PresentRefreshCount;
    UINT SyncRefreshCount;
    LARGE_INTEGER SyncQPCTime;
    LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```

### <a name="frame-synchronization-for-windowed-applications-when-dwm-is-off"></a>Framesynchronisierung für Fensteranwendungen, wenn DWM deaktiviert ist

Wenn DWM deaktiviert ist, werden Anwendungen mit Fenstern direkt auf dem Bildschirm des Monitors angezeigt, ohne eine Flip chain zu durchlaufen. In Windows Vista wird das Abrufen von Framestatistikinformationen für Fensteranwendungen nicht unterstützt, wenn DWM deaktiviert ist. Um eine API zu verwalten, bei der Anwendungen keine DWM-fähigen Anwendungen benötigen, gibt Windows 7 Framestatistikinformationen für Fensteranwendungen zurück, wenn DWM deaktiviert ist. Die Framestatistiken, die zurückgegeben werden, wenn DWM deaktiviert ist, sind nur Schätzungen.

## <a name="walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample"></a>Walk-Through eines Direct3D 9Ex Flip Model and Present Statistics Sample

**So entscheiden Sie sich für flipex presentation for Direct3D 9Ex sample (FlipEx-Präsentation für Direct3D 9Ex-Beispiel)**

1.  Stellen Sie sicher, dass die Beispielanwendung unter Windows 7 oder höher ausgeführt wird.
2.  Legen Sie den **SwapEffect-Member** von [**D3DPRESENT \_ PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) in einem Aufruf von [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)auf [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) fest.


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



**So entscheiden Sie sich auch für das FlipEx-Beispiel "Present Statistics for Direct3D 9Ex" (Aktuelle Statistiken für Direct3D 9Ex)**

-   Legen Sie [D3DCREATE \_ ENABLE \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) im *BehaviorFlags-Parameter* von [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)fest.


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



**Erkennen und Wiederherstellen von Störungen zur Vermeidung von Störungen**

1.  Warteschlangenaufrufe: Die empfohlene Backbufferanzahl liegt zwischen 2 und 4.
2.  Direct3D 9Ex-Beispiel fügt einen impliziten Backbuffer hinzu, die tatsächliche Aktuelle Warteschlangenlänge ist Backbufferanzahl + 1.
3.  Erstellen Sie die Hilfsstruktur Present queue , um alle erfolgreich übermittelten Present-ID (PresentCount) und die zugeordnete, berechnete/erwartete PresentRefreshCount zu speichern.
4.  So erkennen Sie ein Störungsproblem:

    -   Rufen [**Sie GetPresentStatistics auf.**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85))
    -   Abrufen der Aktuellen ID (PresentCount) und vsync-Anzahl, wobei der Frame (PresentRefreshCount) des Frames angezeigt wird, dessen aktuelle Statistik abgerufen wird.
    -   Rufen Sie das erwartete PresentRefreshCount (TargetRefresh im Beispielcode) ab, das der Present-ID zugeordnet ist.
    -   Wenn der tatsächliche PresentRefreshCount-Wert später als erwartet liegt, ist eine Störung aufgetreten.

5.  So stellen Sie nach einer Störung wieder her:

    -   Berechnen Sie, wie viele Frames übersprungen werden sollen (g \_ iImmediates Variable im Beispielcode).
    -   Stellen Sie die übersprungenen Frames mit dem Intervall D3DPRESENT \_ FORCEIMMEDIATE dar.

**Überlegungen zur Fehlererkennung und -wiederherstellung**

1.  Bei der Wiederherstellung einer Störung wird N (g \_ iQueueDelay-Variable im Beispielcode) für Present-Aufrufe benötigt, wobei N (g \_ iQueueDelay) g \_ iImmediates plus Länge der Present-Warteschlange entspricht, d. h.:

    -   Überspringen von Frames mit Present interval D3DPRESENT \_ FORCEIMMEDIATE, plus
    -   Präsentiert in der Warteschlange, die verarbeitet werden muss

2.  Legen Sie einen Grenzwert für die Störungslänge fest (GLITCH \_ RECOVERY \_ LIMIT in Sample). Wenn die Beispielanwendung nach einer zu langen Störung (d. h. 1 Sekunde oder 60 vSyncs auf einem 60-Hz-Monitor) nicht wiederhergestellt werden kann, springen Sie über die zeitweilige Animation, und setzen Sie die Hilfswarteschlange Present zurück.


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

-   Die folgende Abbildung zeigt eine Anwendung mit einer Backbufferanzahl von 4. Die tatsächliche Aktuelle Warteschlangenlänge beträgt daher 5.

    ![Abbildung eines gerenderten Anwendungsframes und einer vorhandenen Warteschlange](images/sample-scenario.png)

    Frame A ist darauf ausgerichtet, auf dem Bildschirm die Synchronisierungsintervallanzahl 1 anzuzeigen, wurde jedoch erkannt, dass es im Synchronisierungsintervall 4 angezeigt wurde. Daher ist eine Störung aufgetreten. Nachfolgende 3 Frames werden mit D3DPRESENT \_ INTERVAL \_ FORCEIMMEDIATE dargestellt. Die Störung sollte insgesamt 8 Present-Aufrufe dauern, bevor sie wiederhergestellt wird. Der nächste Frame wird gemäß der Synchronisierungsintervallanzahl angezeigt.

### <a name="summary-of-programming-recommendations-for-frame-synchronization"></a>Zusammenfassung der Programmierung Empfehlungen für die Framesynchronisierung

-   Erstellen Sie eine Sicherungsliste aller LastPresentCount-IDs (abgerufen über [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount)) und der zugeordneten geschätzten PresentRefreshCount aller übermittelten Präsentierten.
    > [!Note]  
    > Wenn die Anwendung [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) mit D3DPRESENT \_ DONOTFLIP aufruft, ist der [**GetPresentStatistics-Aufruf**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) erfolgreich, gibt aber keine aktualisierte [**D3DPRESENTSTATS-Struktur**](/windows/desktop/direct3d9/d3dpresentstats) zurück, wenn sich die Anwendung im Fenstermodus befindet.

     

-   Rufen [**Sie GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) auf, um das tatsächliche PresentRefreshCount abzurufen, das jeder Present-ID der angezeigten Frames zugeordnet ist, um sicherzustellen, dass die Anwendung Fehlerrückrufe aus dem Aufruf verarbeitet.
-   Wenn das tatsächliche PresentRefreshCount-Element höher als das geschätzte PresentRefreshCount-Element ist, wird eine Störung erkannt. Kompensieren Sie dies, indem Sie "Present with D3DPRESENT FORCEIMMEDIATE" (Vorhanden mit D3DPRESENT FORCEIMMEDIATE) von verzögerten Frames \_ übermitteln.
-   Wenn ein Frame zu einem späteren Zeitpunkt in der Present-Warteschlange angezeigt wird, werden alle nachfolgenden Frames in der Warteschlange zu spät angezeigt. D3DPRESENT \_ FORCEIMMEDIATE korrigiert nur den nächsten Frame, der nach allen Frames in der Warteschlange angezeigt wird. Daher sollte die Anzahl der vorhandenen Warteschlangen oder Backbuffer nicht zu lang sein, sodass es weniger Framestörungen gibt, mit denen Aufholbedarf besteht. Die optimale Backbufferanzahl beträgt 2 bis 4.
-   Wenn PresentRefreshCount nach dem tatsächlichen PresentRefreshCount-Wert geschätzt wird, ist möglicherweise eine DWM-Drosselung aufgetreten. Die folgenden Lösungen sind möglich:

    -   Reduzieren der aktuellen Warteschlangenlänge
    -   Reduzieren der GPU-Arbeitsspeicheranforderungen mit allen anderen Mitteln neben der Reduzierung der Länge der aktuellen Warteschlange (d. h. Verringern der Qualität, Entfernen von Effekten usw.)
    -   Angeben von [**DwmEnableMMCSS,**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenablemmcss) um eine DWM-Drosselung im Allgemeinen zu verhindern

-   Überprüfen Sie die Anwendungsanzeigefunktionen und die Framestatistikleistung in den folgenden Szenarien:

    -   mit ein- und ausgeschalteter DWM
    -   Exklusiver Vollbildmodus und Modus mit Fenster
    -   Hardware mit geringerer Funktionalität

-   Wenn Anwendungen keine Wiederherstellung aus einer großen Anzahl von verfälschten Frames mit D3DPRESENT \_ FORCEIMMEDIATE Present durchführen können, können sie möglicherweise die folgenden Vorgänge ausführen:

    -   Reduzieren Sie die CPU- und GPU-Auslastung, indem Sie mit weniger Workload rendern.
    -   bei der Videocodierung schneller decodieren, indem Sie die Qualität und somit die CPU- und GPU-Auslastung reduzieren.

## <a name="conclusion-about-direct3d-9ex-improvements"></a>Schlussfolgerung zu Direct3D 9Ex-Verbesserungen

In Windows 7 können Anwendungen, die die Bildfrequenz von Videos oder Messgeräten während der Präsentation anzeigen, Flip Model verwenden. Die aktuellen Statistikverbesserungen im Zusammenhang mit Flip Model Direct3D 9Ex können Von Anwendungen profitieren, die die Darstellung pro Bildfrequenz synchronisieren, mit Echtzeitfeedback für die Glitcherkennung und -wiederherstellung. Entwickler, die das Direct3D 9Ex Flip-Modell übernehmen, sollten ein separates HWND von GDI-Inhalt und Bildfrequenzsynchronisierung berücksichtigen. Weitere Informationen finden Sie in diesem Thema und in der MSDN-Dokumentation. Weitere Dokumentation finden Sie im [DirectX Developer Center auf MSDN.](/previous-versions/windows/apps/hh452744(v=win.10))

## <a name="call-to-action"></a>Call-to-Action

Wir empfehlen Ihnen, direct3D 9Ex Flip Model und die aktuellen Statistiken auf Windows 7 zu verwenden, wenn Sie Anwendungen erstellen, die versuchen, die Präsentationsbildrate zu synchronisieren oder eine Wiederherstellung nach Anzeigeblitches zu versuchen.

## <a name="related-topics"></a>Zugehörige Themen

[DirectX Developer Center auf MSDN](/previous-versions/windows/apps/hh452744(v=win.10))
</dt> </dl>