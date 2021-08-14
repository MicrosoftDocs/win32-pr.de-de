---
description: Diese Dokumentation bezieht sich speziell auf die Windows Vista-Erweiterungen für DirectX-Grafiken.
ms.assetid: 3cc0b08c-e126-4f1b-b5d1-0d6c1ebeb0c5
title: Funktionszusammenfassung (Direct3D 9 für Windows Vista)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242af80fa4d6f00c1e55d4852884f9fbbf8de287c6792b3b4aaaad196a6cd113
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523077"
---
# <a name="feature-summary-direct3d-9-for-windows-vista"></a>Funktionszusammenfassung (Direct3D 9 für Windows Vista)

Diese Dokumentation bezieht sich speziell auf die Windows Vista-Erweiterungen für DirectX-Grafiken. Um die Leistungsfähigkeit von DirectX für Windows Vista zu entwickeln, müssen Sie das Windows Vista SDK sowie das DirectX SDK installieren. Anwendungen, die DirectX für Windows Vista verwenden, müssen Hardware verwenden, die den WDDM-Treiber (Windows Gerätetreibermodell) im Gegensatz zum XPDM (XP-Treibermodell) verwendet. -Treiber, die das WDDM nicht implementieren, können Windows Vista DirectX-Grafikschnittstellen nicht instanziieren.

Entdecken Sie die neuen DirectX-Grafikfeatures in Windows Vista in einem der folgenden Abschnitte:

-   [Änderungen am Geräteverhalten](#device-behavior-changes)
-   [Deaktivieren der Multithreadverarbeitung von Softwarevertex](#disabling-multithreaded-software-vertex-processing)
-   [One-Bit-Oberflächen](#one-bit-surfaces)
-   [Lesen von Tiefen-/Schablonenpuffern](#reading-depthstencil-buffers)
-   [Freigeben von Ressourcen](#sharing-resources)
-   [sRGB-Konvertierung vor dem Mischen](#srgb-conversion-before-blending)
-   [StretchRect-Verbesserungen](#stretchrect-improvements)
-   [Texturerstellung im Systemspeicher](#texture-creation-in-system-memory)

## <a name="device-behavior-changes"></a>Änderungen am Geräteverhalten

Geräte gehen jetzt nur unter zwei Umständen verloren: , wenn die Hardware zurückgesetzt wird, weil sie hängt, und wenn der Gerätetreiber beendet wird. Wenn die Hardware hängt, kann das Gerät durch Aufrufen von [**ResetEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex)zurückgesetzt werden. Wenn die Hardware hängt, geht der Texturspeicher verloren.

Nachdem ein Treiber beendet wurde, muss das IDirect9Ex-Objekt neu erstellt werden, um das Rendering fortzusetzen.

Wenn der Präsentationsbereich von einem anderen Fenster im Fenstermodus verdeckt wird oder eine Vollbildanwendung minimiert wird, gibt [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) S \_ D3DPRESENTATIONOCCLUDED zurück. Vollbildanwendungen können das Rendering fortsetzen, wenn sie eine [**WM \_ ACTIVATEAPP-Rückrufmeldung**](../winmsg/wm-activateapp.md) erhalten.

In früheren Versionen von DirectX bestand die einzige Möglichkeit zur Wiederherstellung darin, das Gerät zurückzusetzen und alle Videospeicherressourcen und Tauschketten neu zu erstellen, wenn eine Anwendung einen Moduswechsel hatte. Bei DirectX für Windows Vista führt das Aufrufen von Reset nach einer Modusänderung nicht dazu, dass Texturspeicheroberflächen, Texturen und Zustandsinformationen verloren gehen und diese Ressourcen nicht neu erstellt werden müssen.

## <a name="disabling-multithreaded-software-vertex-processing"></a>Deaktivieren der Multithreadverarbeitung von Softwarevertex

Es wurde ein neues Caps-Bit (D3DCREATE \_ DISABLE \_ PSGP \_ THREADING) hinzugefügt, das Multithreading für die Softwarevertexverarbeitung (Swvp) deaktiviert. Verwenden Sie dieses Makro, um ein Verhaltensflag für IDirect3D9::CreateDevice zu generieren.


```
#define D3DCREATE_DISABLE_PSGP_THREADING
```



## <a name="one-bit-surfaces"></a>One-Bit-Oberflächen

Es gibt einen neuen Ein-Bit-Oberflächenformattyp, der besonders nützlich für die Verarbeitung von Textglyphen sein kann. Das neue Format heißt D3DFMT \_ A1. Eine Ein-Bit-Oberfläche ist so konzipiert, dass sie entweder als Pixeltextur oder als Renderzielausgabe verwendet wird, die von ComposeRects oder ColorFill generiert wird. Es gibt keine separaten Obergrenzen für die Breite und Höhe der Oberfläche. Eine Implementierung muss eine einzelne Oberfläche mit 2K Texel x 8K Texel unterstützen.

Eine Ein-Bit-Oberfläche verfügt über ein Bit pro Texel. daher würde ein -Wert bedeuten, dass alle Komponenten (r,g,b,a) eines Pixels 1 und 0 (null) bedeuten würden, dass alle Komponenten gleich 0 sind. Sie können One-Bit-Oberflächen mit den folgenden APIs verwenden: ColorFill, UpdateSurface und UpdateTexture.

Wenn eine One-Bit-Oberfläche gelesen wird, kann die Laufzeit entweder Punktstichproben oder Konvolutionsfilterung ausführen. Der Konvolutionsfilter kann angepasst werden (siehe [**SetConvolutionMonoKernel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-setconvolutionmonokernel)).

Es gibt einige Einschränkungen für One-Bit-Oberflächen:

-   Mip-Zuordnung wird nicht unterstützt
-   sRGB-Daten können nicht gelesen oder in eine Ein-Bit-Oberfläche geschrieben werden.
-   Eine Ein-Bit-Oberfläche kann nicht als Scheitelpunkttextur oder für Multisampling verwendet werden.

## <a name="reading-depthstencil-buffers"></a>Lesen von Tiefen-/Schablonenpuffern

Verwenden Sie IDirect3DDevice9::UpdateSurface, um Tiefen-/Schablonendaten von Oberflächen zu lesen oder zu schreiben, die von IDirect3DDevice9::CreateDepthStencilSurface oder IDirect3DDevice9::GetDepthStencilSurface abgerufen wurden.

Erstellen Sie zunächst mithilfe von IDirect3DDevice9::CreateOffscreenPlainSurface eine besperrbare Oberfläche, nur Tiefe oder Schablone. Verwenden Sie eines der folgenden Formate:

-   D3DFMT \_ D16 \_ LOCKABLE
-   D3DFMT \_ D32F \_ LOCKABLE
-   D3DFMT \_ D32 \_ LOCKABLE
-   D3DFMT \_ S8 \_ LOCKABLE

Übertragen Sie zweitens Daten zwischen dem Tiefen-/Schablonenpuffer und der neu erstellten sperrbaren Tiefe oder Schablonenoberfläche. Die Übertragung erfolgt mit IDirect3DDevice9::UpdateSurface.

UpdateSurface schlägt fehl, wenn beide Oberflächen ein LOCKABLE-Format aufweisen oder beide nicht sperrbar sind.

Das Übertragen nicht vorhandener Daten führt zu einem Fehler (z.B. übertragung von einer nicht sperrbaren Tiefenoberfläche auf eine D3DFMT \_ S8 \_ LOCKABLE-Oberfläche).

Die restlichen Einschränkungen für IDirect3DDevice9::UpdateSurface gelten weiterhin.

## <a name="sharing-resources"></a>Freigeben von Ressourcen

Direct3D-Ressourcen können jetzt von Geräten oder Prozessen gemeinsam genutzt werden. Dies gilt für alle Direct3D-Ressourcen, einschließlich Texturen, Scheitelpunktpuffer, Indexpuffer oder Oberflächen (z. B. Renderziele, Tiefenschablonenpuffer oder einfache Oberflächen außerhalb des Bildschirms). Um freigegeben zu werden, müssen Sie zum Zeitpunkt der Erstellung eine Ressource für die Freigabe festlegen und die Ressource im Standardpool (D3DPOOL \_ DEFAULT) suchen. Sobald eine Ressource für die Freigabe erstellt wurde, kann sie geräteübergreifend innerhalb eines Prozesses oder prozessübergreifend freigegeben werden.

Um freigegebene Ressourcen zu aktivieren, verfügen die RESSOURCENerstellungs-APIs über einen zusätzlichen Handleparameter. Dies ist ein HANDLE, das auf die freigegebene Ressource verweist. In früheren Revisionen von DirectX war dieses Argument Teil der API-Signatur, wurde jedoch nicht verwendet und muss auf **NULL** festgelegt werden. Ab Windows Vista können Sie pSharedHandle wie folgt verwenden:

-   Legen Sie den Zeiger (pSharedHandle) auf **NULL** fest, um keine Ressource freizugeben. Dies entspricht dem Verhalten von DirectX vor Windows Vista.
-   Um eine freigegebene Ressource zu erstellen, rufen Sie eine beliebige API zum Erstellen von Ressourcen (siehe unten) mit einem nicht initialisierten Handle auf (der Zeiger selbst ist nicht **NULL** (pSharedHandle != **NULL**), aber der Zeiger zeigt auf einen **NULL-Wert** ( \* pSharedHandle == **NULL**)). Die API generiert eine freigegebene Ressource und gibt ein gültiges Handle zurück.
-   Legen Sie pSharedHandle auf die Adresse dieses Handles fest, um eine zuvor erstellte freigegebene Ressource mit einem freigegebenen Ressourcenhandle ohne NULL zu öffnen und darauf zuzugreifen. Nachdem Sie die zuvor erstellte freigegebene Ressource auf diese Weise geöffnet haben, können Sie die zurückgegebene Schnittstelle in der Direct3D 9- oder Direct3D 9Ex-API verwenden, als wäre die Schnittstelle eine typische Ressource dieses Typs.

Ressourcenerstellungs-APIs umfassen [**: CreateTexture,**](/windows/desktop/api) [**CreateVolumeTexture,**](/windows/desktop/api) [**CreateCubeTexture,**](/windows/desktop/api) [**CreateRenderTarget,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget) [**CreateVertexBuffer,**](/windows/desktop/api) [**CreateIndexBuffer,**](/windows/desktop/api) [**CreateDepthStencilSurface,**](/windows/desktop/api) [**CreateOffscreenPlainSurface,**](/windows/desktop/api) [**CreateDepthStencilSurfaceEx,**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createdepthstencilsurfaceex) [**CreateOffscreenPlainSurfaceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createoffscreenplainsurfaceex)und [**CreateRenderTargetEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createrendertargetex).

Es gibt einige Einschränkungen für die Verwendung freigegebener Ressourcen. Dazu gehören:

-   Die API, die Sie zum Öffnen einer freigegebenen Ressource verwenden, muss mit der API übereinstimmen, die Sie zum Erstellen der freigegebenen Ressource verwendet haben. Wenn Sie beispielsweise [**CreateTexture**](/windows/desktop/api) zum Erstellen einer freigegebenen Ressource verwendet haben, müssen Sie **CreateTexture** verwenden, um diese freigegebene Ressource zu öffnen. Wenn Sie [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget) zum Erstellen einer freigegebenen Ressource verwendet haben, müssen Sie **CreateRenderTarget** verwenden, um diese freigegebene Ressource zu öffnen usw.
-   Wenn Sie eine freigegebene Ressource öffnen, müssen Sie D3DPOOL \_ DEFAULT angeben.
-   Sperrbare Ressourcen (z.B. Texturen mit D3DUSAGE \_ DYNAMIC, Scheitelpunktpuffer und Indexpuffer) können bei der Freigabe eine schlechte Leistung aufweisen. Sperrbare Renderziele können auf einigen Hardwarekomponenten nicht freigegeben werden.
-   Verweise auf eine prozessübergreifende freigegebene Ressource müssen die gleichen Dimensionen wie die ursprüngliche Ressource aufweisen. Schließen Sie beim Übergeben eines Handles über den Prozess die Dimensionsinformationen ein, damit der Verweis identisch erstellt werden kann.
-   Freigegebene prozessübergreifende Oberflächen bieten keinen Synchronisierungsmechanismus. Lese-/Schreibänderungen an einer freigegebenen Oberfläche spiegeln möglicherweise nicht wie erwartet die Ansicht eines verweisenden Prozesses der Oberfläche wider. Um eine Synchronisierung bereitzustellen, verwenden Sie Ereignisabfragen, oder sperren Sie die Textur.
-   Nur der Prozess, der anfänglich eine freigegebene Ressource erstellt, kann sie sperren (jeder Prozess, der einen Verweis auf diese freigegebene Ressource öffnet, kann sie nicht sperren).
-   Wenn eine freigegebene Ressource gesperrt ist, gibt es keine Überprüfung für andere Prozesse, um zu wissen, ob die Ressource verfügbar ist.

## <a name="srgb-conversion-before-blending"></a>sRGB-Konvertierung vor dem Mischen

Sie können nun überprüfen, ob das Gerät Pipelinedaten vor dem Einfügen von Framepuffern in sRGB konvertieren kann. Dies bedeutet, dass das Gerät die Renderzielwerte aus sRGB konvertiert. Um festzustellen, ob die Konvertierung von der Hardware unterstützt wird, überprüfen Sie diese Obergrenze:


```
D3DPMISCCAPS_POSTBLENDSRGBCONVERT
```



Diese Obergrenze identifiziert Hardware, die die Konvertierung in sRGB vor dem Mischen unterstützt. Diese Funktion ist wichtig für das qualitativ hochwertige Rendering aus fp16-Framepuffern im Desktopfenster-Manager (DWM).

## <a name="stretchrect-improvements"></a>StretchRect-Verbesserungen

In früheren Versionen von DirectX gelten für StretchRect viele Einschränkungen für verschiedene Treiber (siehe IDirect3DDevice9::StretchRect). Windows Vista basiert auf dem Windows Device Driver Model (WDDM). Dieses neue Treibermodell ist wesentlich robuster und ermöglicht es Treibern, Sonderfälle in der Hardware zu verarbeiten.

Im Allgemeinen besteht die einzige verbleibende Einschränkung darin, dass das Renderziel mit Renderzielverwendung (D3DUSAGE RENDERTARGET) erstellt worden sein \_ muss. Diese Einschränkung wird aufgehoben, wenn Sie eine einfache Kopie erstellen (wobei Quelle und Dest das gleiche Format, dieselbe Größe aufweisen und keine Unterrechtecke vorhanden sind).

## <a name="texture-creation-in-system-memory"></a>Texturerstellung im Systemspeicher

Anwendungen, die mehr Flexibilität hinsichtlich der Verwendung, Zuordnung und Löschung des Systemspeichers benötigen, können jetzt Texturen aus einem Systemspeicherzeiger erstellen. Beispielsweise könnte eine Anwendung eine Direct3D-Textur aus einem GDI-Systemspeicherbitmapzeiger erstellen.

Sie müssen zwei Dinge tun, um eine solche Textur zu erstellen:

-   Ordnen Sie genügend Systemspeicher für die Texturoberfläche zu. Die Mindestanzahl von Bytes ist Breite x Höhe x Bytes pro Pixel.
-   Übergeben Sie die Adresse eines Zeigers auf die Systemspeicheroberfläche für den \* HANDLE-Parameter an IDirect3DDevice9::CreateTexture.

Hier ist der Funktionsprototyp für IDirect3DDevice9::CreateTexture:


```
STDMETHOD(CreateTexture)(THIS_ UINT Width, UINT Height, UINT Levels, 
    DWORD Usage, D3DFORMAT Format, D3DPOOL Pool, IDirect3DTexture9** ppTexture, 
    HANDLE* pSharedHandle)
```



Für eine Textur des Systemspeichers gelten die folgenden Einschränkungen:

-   Die Texturhöhe muss der Texturbreite entsprechen, die der Anzahl der Bytes pro Pixel entspricht.
-   Bei Verwendung komprimierter Formate (DXT-Formate) ist die Anwendung für die Zuordnung der richtigen Größe verantwortlich.
-   Nur Texturen mit einer einzelnen Mipmapebene werden unterstützt.
-   Der wert, der für das Pool-Argument an CreateTexture übergeben wird, muss D3DPOOL \_ SYSTEMMEM sein.
-   Diese API umschließt den bereitgestellten Speicher in einer Textur. Geben Sie die Zuordnung dieses Arbeitsspeichers erst wieder auf, wenn Sie damit fertig sind.

 

 
