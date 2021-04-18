---
description: Diese Dokumentation bezieht sich speziell auf die Windows Vista-Erweiterungen für DirectX-Grafiken.
ms.assetid: 3cc0b08c-e126-4f1b-b5d1-0d6c1ebeb0c5
title: Funktions Zusammenfassung (Direct3D 9 für Windows Vista)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d5cf2447297b7f24edf7d0200e640d5aef90bff
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344170"
---
# <a name="feature-summary-direct3d-9-for-windows-vista"></a>Funktions Zusammenfassung (Direct3D 9 für Windows Vista)

Diese Dokumentation bezieht sich speziell auf die Windows Vista-Erweiterungen für DirectX-Grafiken. Um die Leistungsfähigkeit von DirectX für Windows Vista zu entwickeln, müssen Sie sowohl das Windows Vista SDK als auch das DirectX SDK installieren. Anwendungen, die DirectX für Windows Vista verwenden, müssen Hardware verwenden, die den WDDM-Treiber (Windows-Gerätetreiber Modell) im Gegensatz zum XPDM (XP-Treibermodell) verwendet. Treiber, die die WDDM nicht implementieren, können Windows Vista DirectX-Grafik Schnittstellen nicht instanziieren.

Entdecken Sie die neuen DirectX-Grafik Features in Windows Vista in einem der folgenden Abschnitte:

-   [Änderungen am Geräteverhalten](#device-behavior-changes)
-   [Deaktivieren der Verarbeitung von Multithreaded-Software Scheitel Punkten](#disabling-multithreaded-software-vertex-processing)
-   [Eine bitfläche](#one-bit-surfaces)
-   [Lesetiefe/Schablonen Puffer](#reading-depthstencil-buffers)
-   [Freigeben von Ressourcen](#sharing-resources)
-   [sRGB-Konvertierung vor dem Mischen](#srgb-conversion-before-blending)
-   [Verbesserungen bei stretchrect](#stretchrect-improvements)
-   [Textur Erstellung im System Speicher](#texture-creation-in-system-memory)

## <a name="device-behavior-changes"></a>Änderungen am Geräteverhalten

Geräte gehen nun in zwei Fällen verloren: Wenn die Hardware zurückgesetzt wird, weil Sie nicht mehr angezeigt wird, und wenn der Gerätetreiber angehalten wird. Wenn die Hardware nicht mehr reagiert, kann das Gerät durch Aufrufen von [**retartex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex)zurückgesetzt werden. Wenn die Hardware nicht mehr vorhanden ist, geht der Texturspeicher verloren.

Nach dem Beenden eines Treibers muss das IDirect9Ex-Objekt neu erstellt werden, um das Rendering fortzusetzen.

Wenn der Präsentationsbereich von einem anderen Fenster im Fenstermodus verdeckt wird oder wenn eine Vollbildanwendung minimiert wird, gibt der [**presentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) S \_ D3DPRESENTATIONOCCLUDED zurück. Vollbildanwendungen können das Rendering fortsetzen, wenn Sie eine [**WM \_ activateapp**](../winmsg/wm-activateapp.md) -Rückruf Meldung erhalten.

In früheren Versionen von DirectX war die einzige Möglichkeit zur Wiederherstellung, das Gerät zurückzusetzen und alle Videospeicher Ressourcen und Austausch Ketten neu zu erstellen. Mit DirectX für Windows Vista bewirkt das Aufrufen von Reset nach einer Modusänderung nicht, dass Texturspeicher Oberflächen, Texturen und Zustandsinformationen verloren gehen und diese Ressourcen nicht neu erstellt werden müssen.

## <a name="disabling-multithreaded-software-vertex-processing"></a>Deaktivieren der Verarbeitung von Multithreaded-Software Scheitel Punkten

Ein neues Caps-Bit (D3DCREATE \_ deaktiviert \_ PSGP- \_ Threading) wurde hinzugefügt, das Multithreading für die Verarbeitung von Software Scheitel Punkten (Report tex Processing, Swap) deaktiviert. Verwenden Sie dieses Makro, um ein verhaltensflag für IDirect3D9:: kreatedevice zu generieren.


```
#define D3DCREATE_DISABLE_PSGP_THREADING
```



## <a name="one-bit-surfaces"></a>Eine bitfläche

Es gibt einen neuen ein-Bit-Oberflächen Formattyp, der für die Verarbeitung von Text Symbolen besonders nützlich sein kann. Das neue Format wird als D3DFMT \_ a1 bezeichnet. Eine einmal-Oberfläche ist für die Verwendung als pixelbasierte Textur oder die renderzielausgabe vorgesehen, die von composerects oder ColorFill generiert wurde. Es gibt keine separaten Obergrenzen für die Breite und Höhe der Oberfläche. eine-Implementierung muss eine einzelne Größen Oberfläche unterstützen, bei der es sich um 2K texeln x 8K texeln handelt.

Eine 1-Bit-Oberfläche verfügt über ein Bit pro Texttyp. Daher bedeutet eine solche, dass alle Komponenten (r, g, b, a) eines Pixels 1 sind, und 0 bedeutet, dass alle Komponenten gleich 0 sind. Sie können eine-Bit-Oberfläche mit den folgenden APIs verwenden: ColorFill, updatesurface und UpdateTexture.

Wenn eine einmalige Oberfläche gelesen wird, kann die Laufzeit entweder eine Punkt-oder eine Zugriffsfilterung durchführen. Der Verbindungs Filter kann angepasst werden (siehe [**SetConfiguration-monokernel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-setconvolutionmonokernel)).

Es gibt einige Einschränkungen für die einzelnen-Bit-Oberflächen:

-   MIP-Zuordnung wird nicht unterstützt.
-   sRGB-Daten können nicht auf einer 1-Bit-Oberfläche gelesen oder geschrieben werden.
-   Eine einmalige Oberfläche kann nicht als Scheitelpunkt Textur oder für Multisampling verwendet werden.

## <a name="reading-depthstencil-buffers"></a>Lesetiefe/Schablonen Puffer

Verwenden Sie IDirect3DDevice9:: updatesurface, um Tiefe/Schablone-Daten aus Oberflächen zu lesen oder zu schreiben, die von IDirect3DDevice9:: an-DepthStencilSurface oder IDirect3DDevice9:: getdepthstencilsurface abgerufen wurden.

Erstellen Sie zuerst mit IDirect3DDevice9:: foateoffscreenplainsurface eine Oberfläche für Lockable, Tiefe oder Schablone. Verwenden Sie eines der folgenden Formate:

-   D3DFMT \_ D16 \_ Lockable
-   D3DFMT \_ D32F \_ Lockable
-   D3DFMT \_ d32 \_ Lockable
-   D3DFMT \_ S8 \_ Sperr fähig

Übertragen Sie die Daten zwischen dem tiefen-/Stencil-Puffer und der neu erstellten Sperr baren Tiefe oder Schablone-Oberfläche. Die Übertragung erfolgt mithilfe von IDirect3DDevice9:: updatesurface.

Updatesurface schlägt fehl, wenn beide Oberflächen ein Sperr bares Format aufweisen oder beide nicht sperrbar sind.

Wenn Sie nicht vorhandene Daten übertragen, führt dies zu einem Fehler (z. b. bei der Übertragung von einer nicht Sperr baren tiefen Oberfläche auf eine \_ Sperr Bare D3DFMT S8- \_ Oberfläche).

Die restlichen Einschränkungen für IDirect3DDevice9:: updatesurface gelten weiterhin.

## <a name="sharing-resources"></a>Freigeben von Ressourcen

Direct3D-Ressourcen können jetzt von Geräten oder Prozessen gemeinsam genutzt werden. Dies gilt für alle Direct3D-Ressourcen wie z. b. Texturen, Vertex-Puffer, Index Puffer oder Oberflächen (z. b. Renderziele, tiefen Schablone oder außerhalb des Bildschirms). Um freigegeben zu werden, müssen Sie zum Zeitpunkt der Erstellung eine Ressource für die Freigabe festlegen und die Ressource im Standard Pool (D3DPOOL \_ Default) suchen. Nachdem eine Ressource für die Freigabe erstellt wurde, kann Sie auf allen Geräten innerhalb eines Prozesses freigegeben oder über Prozesse hinweg gemeinsam genutzt werden.

Um freigegebene Ressourcen zu aktivieren, verfügen die ressourcenerstellungs-APIs über einen zusätzlichen handle-Parameter. Dies ist ein Handle, das auf die freigegebene Ressource verweist. In früheren Revisionen von DirectX war dieses Argument Teil der API-Signatur, wurde jedoch nicht verwendet und muss auf **null** festgelegt werden. Ab Windows Vista verwenden Sie psharedhandle wie folgt:

-   Legen Sie den Zeiger (psharedhandle) auf **null** fest, um keine Ressource freizugeben. Dies entspricht dem Verhalten von DirectX vor Windows Vista.
-   Um eine freigegebene Ressource zu erstellen, rufen Sie eine beliebige ressourcenerstellungs-API (siehe unten) mit einem nicht initialisierten Handle auf (der Zeiger selbst ist nicht **null** (psharedhandle! = **null**), aber der Zeiger verweist auf einen **null** -Wert ( \* psharedhandle = = **null**)). Die API generiert eine freigegebene Ressource und gibt ein gültiges Handle zurück.
-   Wenn Sie eine zuvor erstellte freigegebene Ressource mithilfe eines freigegebenen Ressourcen Handles, das nicht NULL ist, öffnen und darauf zugreifen möchten, legen Sie psharedhandle auf die Adresse dieses Handles fest. Nachdem Sie die zuvor erstellte freigegebene Ressource auf diese Weise geöffnet haben, können Sie die zurückgegebene Schnittstelle in der Direct3D 9-oder Direct3D 9Ex-API verwenden, als ob die Schnittstelle eine typische Ressource dieses Typs wäre.

Ressourcenerstellungs-APIs enthalten "-up [**Texture**](/windows/desktop/api)", " [**kreatevolumetexture**](/windows/desktop/api)", " [**deecubetexture**](/windows/desktop/api)", " [**kreaterendertarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)", " [**kreatevertexbuffer**](/windows/desktop/api)", " [**kreateindexbuffer**](/windows/desktop/api)", " [**kreatedepthstencilsurface**](/windows/desktop/api)", " [**kreateoffscreenplainsurface**](/windows/desktop/api)", [**"**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createrendertargetex) [**kreatedepthstencilsurfaceex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createdepthstencilsurfaceex)", " [**kreateoffscreenplainsurfaceex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createoffscreenplainsurfaceex)"

Es gibt einige Einschränkungen für die Verwendung von freigegebenen Ressourcen. Dazu gehören:

-   Die API, mit der Sie eine freigegebene Ressource öffnen, muss mit der API, die Sie zum Erstellen der freigegebenen Ressource verwendet haben, identisch sein. Wenn Sie z. b. zum Erstellen einer freigegebenen Ressource " [**kreatetexture**](/windows/desktop/api) " verwendet haben, müssen Sie die freigegebene Ressource mithilfe von " **kreatetexture** " öffnen. Wenn Sie mit " [**anaterendertarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget) " eine freigegebene Ressource erstellt haben, müssen Sie die freigegebene Ressource mithilfe von " **anaterendertarget** " öffnen usw.
-   Wenn Sie eine freigegebene Ressource öffnen, müssen Sie D3DPOOL \_ default angeben.
-   \_Bei der gemeinsamen Nutzung kann es zu Leistungseinbußen kommen, wenn die Ressourcen freigegeben werden. Lockable Rendertargets kann nicht auf Hardware freigegeben werden.
-   Verweise auf eine prozessübergreifende freigegebene Ressource müssen die gleichen Dimensionen wie die ursprüngliche Ressource aufweisen. Wenn Sie ein Handle Prozess übergreifend übergeben, schließen Sie die Dimensions Informationen ein, damit der Verweis identisch erstellt werden kann.
-   Freigegebene prozessübergreifende Oberflächen bieten keine Synchronisierungs Mechanismen. Lese-/schreibänderungen an einer freigegebenen Oberfläche spiegeln möglicherweise nicht die Ansicht der Oberfläche eines verweisenden Prozesses wider, wenn dies erwartet wird. Verwenden Sie zum Bereitstellen der Synchronisierung Ereignis Abfragen, oder Sperren Sie die Textur.
-   Nur der Prozess, der anfänglich eine freigegebene Ressource erstellt, kann Sie Sperren (jeder Prozess, der einen Verweis auf diese freigegebene Ressource öffnet), kann Sie sperren.
-   Wenn eine freigegebene Ressource gesperrt ist, können andere Prozesse nicht überprüfen, ob die Ressource verfügbar ist.

## <a name="srgb-conversion-before-blending"></a>sRGB-Konvertierung vor dem Mischen

Sie können jetzt überprüfen, ob das Gerät Pipeline Daten in sRGB konvertieren kann, bevor das Frame Puffer gemischt wird. Dies impliziert, dass das Gerät die renderzielwerte aus sRGB konvertiert. Um festzustellen, ob die Konvertierung von der Hardware unterstützt wird, überprüfen Sie diese Obergrenze:


```
D3DPMISCCAPS_POSTBLENDSRGBCONVERT
```



Diese Obergrenze identifiziert Hardware, die vor dem mischen die Konvertierung in sRGB unterstützt. Diese Funktion ist wichtig für das hochwertige Rendering von FP16-Frame Puffern im Desktop Fenster-Manager (DWM).

## <a name="stretchrect-improvements"></a>Verbesserungen bei stretchrect

In früheren Versionen von DirectX hat stretchrect viele Einschränkungen, um unterschiedliche Treiber zu unterstützen (siehe IDirect3DDevice9:: stretchrect). Windows Vista baut auf dem Windows-Gerätetreiber Modell (WDDM) auf. Dieses neue Treibermodell ist weitaus robuster und ermöglicht es den Treibern, bestimmte Fälle in der Hardware zu verarbeiten.

Im Allgemeinen besteht die einzige verbleibende Einschränkung darin, dass das Renderziel mit der Verwendung von " \_ Renderziel" (D3DUSAGE renderTarget) erstellt werden muss. Diese Einschränkung wird aufgehoben, wenn Sie eine einfache Kopie durchlaufen (wobei Quelle und dest dasselbe Format aufweisen, dieselbe Größe und keine unter Rechtecke vorhanden sind).

## <a name="texture-creation-in-system-memory"></a>Textur Erstellung im System Speicher

Anwendungen, die mehr Flexibilität in Bezug auf die Verwendung, Zuweisung und Löschung des System Arbeitsspeichers benötigen, können jetzt Texturen aus einem Systemspeicher Zeiger erstellen. Eine Anwendung kann z. b. eine Direct3D-Textur aus einem GDI-Bitmap-Zeiger für System Arbeitsspeicher erstellen.

Sie müssen zwei Dinge durchführen, um eine solche Textur zu erstellen:

-   Weisen Sie genügend System Arbeitsspeicher zum Speichern der Textur Oberfläche zu. Die Mindestanzahl von Bytes beträgt Breite x Höhe x Bytes pro Pixel.
-   Übergeben Sie die Adresse eines Zeigers an die Systemspeicher Oberfläche für den Handle- \* Parameter an IDirect3DDevice9:: foatetexture.

Hier sehen Sie den Funktionsprototyp für IDirect3DDevice9:: kreatetexture:


```
STDMETHOD(CreateTexture)(THIS_ UINT Width, UINT Height, UINT Levels, 
    DWORD Usage, D3DFORMAT Format, D3DPOOL Pool, IDirect3DTexture9** ppTexture, 
    HANDLE* pSharedHandle)
```



Eine systemarbeits Speicher-Textur weist die folgenden Einschränkungen auf:

-   Die Textur Breite muss der Textur Breite und der Anzahl der Bytes pro Pixel entsprechen.
-   Wenn Sie komprimierte Formate (DXT-Formate) verwenden, ist die Anwendung für die Zuordnung der richtigen Größe verantwortlich.
-   Nur Texturen mit einer einzelnen MipMap-Ebene werden unterstützt.
-   Der Wert, der für das Pool-Argument an "kreatetexture" übergeben wird, muss D3DPOOL \_ SystemMem sein.
-   Diese API umschließt den bereitgestellten Speicher in eine Textur. Teilen Sie diesen Arbeitsspeicher erst auf, wenn Sie diesen Vorgang abgeschlossen haben.

 

 
