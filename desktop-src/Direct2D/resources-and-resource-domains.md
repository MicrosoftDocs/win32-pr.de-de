---
title: Übersicht über Ressourcen
description: Beschreibt Direct2D-Ressourcen und wie sie freigegeben werden können.
ms.assetid: afd308a7-9524-4436-9a0e-8575383d96fa
keywords:
- Direct2D, Ressourcen
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 67dc8c34703c834dbf0f1b651e3c118831d88abe1676feaba68ac53ecb603565
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825111"
---
# <a name="resources-overview"></a>Übersicht über Ressourcen

Eine Direct2D-Ressource ist ein Objekt, das zum Zeichnen verwendet wird und durch eine Direct2D-Schnittstelle wie [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) oder [**ID2D1RenderTarget dargestellt wird.**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) In diesem Thema werden die Arten von Direct2D-Ressourcen und deren Freigabe beschrieben.

Dieses Thema enthält folgende Abschnitte:

-   [Informationen zu Direct2D-Ressourcen](#about-direct2d-resources)
-   [Geräteunabhängige Ressourcen](#device-independent-resources)
-   [Geräteabhängige Ressourcen](#device-dependent-resources)
-   [Freigeben von Factoryressourcen](#sharing-factory-resources)
-   [Freigeben von Renderzielressourcen](#sharing-render-target-resources)
    -   [Hardwarerenderingziele](#hardware-render-targets)
    -   [DXGI Surface Render Targets](#dxgi-surface-render-targets)
    -   [Kompatible Renderziele und freigegebene Bitmaps](#compatible-render-targets-and-shared-bitmaps)

## <a name="about-direct2d-resources"></a>Informationen zu Direct2D-Ressourcen

Viele hardwarebeschleunigte 2D-APIs sind auf ein CPU-orientiertes Ressourcenmodell und eine Reihe von Renderingvorgängen ausgelegt, die gut für CPUs funktionieren. Ein Teil der API ist dann hardwarebeschleunigt. Die Implementierung dieser APIs erfordert einen Ressourcen-Manager zum Zuordnen von CPU-Ressourcen zu Ressourcen auf der GPU. Aufgrund von GPU-Einschränkungen können einige Vorgänge unter Umständen nicht in jedem Fall beschleunigt werden. In diesen Fällen muss der Ressourcen-Manager zwischen CPU und GPU (was teuer ist) hin und her kommunizieren, damit er zum CPU-Rendering übergehen kann. In einigen Fällen kann es unvorhersehbar erzwingen, dass das Rendering vollständig auf die CPU zurückfallen muss. Darüber hinaus erfordern Renderingvorgänge, die einfach erscheinen, möglicherweise temporäre zwischengeschaltete Renderingschritte, die nicht in der API verfügbar gemacht werden und zusätzliche GPU-Ressourcen erfordern.

Direct2D bietet eine direktere Zuordnung zur vollständigen Nutzung der GPU. Es bietet zwei Kategorien von Ressourcen: geräteunabhängig und geräteabhängig.

-   Geräteunabhängige Ressourcen wie [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)werden auf der CPU beibehalten.
-   Geräteabhängige Ressourcen, z. B. [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) und [**ID2D1LinearGradientBrush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)werden Ressourcen auf der GPU direkt (wenn die Hardwarebeschleunigung verfügbar ist) zuordnen. Renderingaufrufe werden ausgeführt, indem Scheitelpunkt- und Abdeckungsinformationen aus einer Geometrie mit Texturinformationen kombiniert werden, die von den geräteabhängigen Ressourcen erzeugt werden.

Wenn Sie geräteabhängige Ressourcen erstellen, werden Systemressourcen (gpu, falls verfügbar oder CPU) zugeordnet, wenn das Gerät erstellt wird, und werden nicht von einem Renderingvorgang zu einem anderen geändert. In dieser Situation entfällt die Notwendigkeit eines Ressourcen-Managers. Zusätzlich zu den allgemeinen Leistungsverbesserungen, die durch die Beseitigung eines Ressourcen-Managers bereitgestellt werden, können Sie mit diesem Modell alle Zwischenrenderings direkt steuern.

Da Direct2D so viel Kontrolle über Ressourcen bietet, müssen Sie die verschiedenen Arten von Ressourcen verstehen und wissen, wann sie zusammen verwendet werden können.

## <a name="device-independent-resources"></a>Device-Independent Ressourcen

Wie im vorherigen Abschnitt beschrieben, befinden sich geräteunabhängige Ressourcen immer auf der CPU und werden nie einem Hardwarerenderinggerät zugeordnet. Im Folgenden finden Sie geräteunabhängige Ressourcen:

-   [**ID2D1DrawingStateBlock**](/windows/win32/api/d2d1/nn-d2d1-id2d1drawingstateblock)
-   [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
-   [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) und die Schnittstellen, die davon erben.
-   [**ID2D1GeometrySink und**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) [ **ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)
-   [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle)

Verwenden Sie [**eine ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), selbst eine geräteunabhängige Ressource, um geräteunabhängige Ressourcen zu erstellen. (Verwenden Sie zum Erstellen einer Factory die [**CreateFactory-Funktion.)**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory)

Mit Ausnahme von Renderzielen sind alle von einer Factory erstellten Ressourcen geräteunabhängig. Ein Renderziel ist eine geräteabhängige Ressource.

## <a name="device-dependent-resources"></a>Device-Dependent Ressourcen

Jede Ressource, die in der vorherigen Liste nicht benannt ist, ist eine geräteabhängige Ressource. Geräteabhängige Ressourcen sind einem bestimmten Renderinggerät zugeordnet. Wenn die Hardwarebeschleunigung verfügbar ist, ist dieses Gerät die GPU. In anderen Fällen ist dies die CPU.

Verwenden Sie ein Renderziel, um die meisten geräteabhängigen Ressourcen zu erstellen. In den meisten Fällen verwenden Sie eine Factory, um ein Renderziel zu erstellen.

Im Folgenden finden Sie Beispiele für geräteabhängige Ressourcen:

-   [**ID2D1Brush und**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) die Schnittstellen, die davon erben. Verwenden Sie ein Renderziel, um Pinsel zu erstellen.
-   [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer). Verwenden Sie ein Renderziel, um Ebenen zu erstellen.
-   [**ID2D1RenderTarget und**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) die Schnittstellen, die davon erben. Um ein Renderziel zu erstellen, verwenden Sie eine Factory oder ein anderes Renderziel.

> [!Note]  
> Beginnend mit Windows 8 gibt es neue Schnittstellen, die geräteabhängige Ressourcen erstellen. Ein [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) und ein [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) können eine Ressource gemeinsam nutzen, wenn der Gerätekontext und die Ressource aus demselben **ID2D1Device erstellt werden.**

 

Geräteabhängige Ressourcen werden unbrauchbar, wenn die zugeordneten Renderinggeräte nicht mehr verfügbar sind. Dies bedeutet, dass Sie das Renderziel und alle seine Ressourcen neu erstellen müssen, wenn Sie den [**D2DERR \_ RECREATE \_ TARGET-Fehler**](direct2d-error-codes.md) für ein Renderziel erhalten.

## <a name="sharing-factory-resources"></a>Freigeben von Factoryressourcen

Sie können alle geräteunabhängigen Ressourcen, die von einer Factory erstellt wurden, für alle anderen Ressourcen (geräteunabhängig oder geräteabhängig) freigeben, die von derselben Factory erstellt wurden. Beispielsweise können Sie zwei [**ID2D1RenderTarget-Objekte**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) verwenden, um dieselbe [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) zu zeichnen, wenn beide **ID2D1RenderTarget-Objekte** von derselben Factory erstellt wurden.

Die Senkenschnittstellen [**(ID2D1SimplifiedGeometrySink,**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)und [**ID2D1TessellationSink**](/windows/win32/api/d2d1/nn-d2d1-id2d1tessellationsink)) können für Ressourcen freigegeben werden, die von jeder Factory erstellt wurden. Im Gegensatz zu anderen Schnittstellen in Direct2D kann jede Implementierung einer Senkenschnittstelle verwendet werden. Beispielsweise können Sie Ihre eigene Implementierung von **ID2D1SimplifiedGeometrySink verwenden.**

## <a name="sharing-render-target-resources"></a>Freigeben von Renderzielressourcen

Ihre Möglichkeit zum Freigeben von Ressourcen, die von einem Renderziel erstellt wurden, hängt von der Art des Renderziels ab. Wenn Sie ein Renderziel vom Typ [**D2D1 \_ RENDER TARGET TYPE \_ \_ \_ DEFAULT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type)erstellen, können die von diesem Renderziel erstellten Ressourcen nur von diesem Renderziel verwendet werden (es sei denn, das Renderziel passt in eine der in den folgenden Abschnitten beschriebenen Kategorien). Dies liegt daran, dass Sie nicht wissen, welches Gerät das Renderziel am Ende verwendet. Es kann dazu kommen, dass es auf lokaler Hardware, Software oder auf der Hardware eines Remoteclients gerendert wird. Beispielsweise können Sie ein Programm schreiben, das nicht mehr funktioniert, wenn es remote angezeigt wird oder wenn das Renderziel größer als die von der Renderinghardware unterstützte maximale Größe ist.

In den folgenden Abschnitten werden die Umstände beschrieben, unter denen eine von einem Renderziel erstellte Ressource für ein anderes Renderziel freigegeben werden kann.

### <a name="hardware-render-targets"></a>Hardwarerenderingziele

Sie können Ressourcen für jedes Renderziel freigeben, das explizit Hardware verwendet, solange der Remotingmodus kompatibel ist. Der Remotingmodus ist nur dann kompatibel, wenn beide Renderziele das Verwendungsflag [**D2D1 \_ RENDER TARGET USAGE FORCE BITMAP \_ \_ \_ \_ \_ REMOTING**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) oder **D2D1 \_ RENDER TARGET USAGE \_ \_ \_ GDI \_ COMPATIBLE** verwenden oder kein Flag angegeben ist. Diese Einstellungen garantieren, dass sich die Ressourcen immer auf demselben Computer befinden. Um einen Verwendungsmodus  anzugeben, legen Sie das Verwendungsfeld der [**D2D1 \_ RENDER \_ TARGET \_ PROPERTIES-Struktur**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) fest, die Sie zum Erstellen des Renderziels mit mindestens einem **D2D1 \_ RENDER TARGET \_ \_ USAGE-Flag** verwendet haben.

Um ein Renderziel zu erstellen, das  explizit Hardwarerendering verwendet, legen Sie das Typfeld der [**D2D1 \_ RENDER \_ TARGET \_ PROPERTIES-Struktur,**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) die Sie zum Erstellen des Renderziels verwendet haben, auf [**D2D1 \_ RENDER TARGET TYPE HARDWARE \_ \_ \_ fest.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type)

### <a name="dxgi-surface-render-targets"></a>DXGI Surface Render Targets

Sie können ressourcen, die von einem DXGI-Oberflächenrenderingziel erstellt wurden, für jedes andere DXGI-Oberflächenrenderingziel freigeben, das das gleiche zugrunde liegende Direct3D-Gerät verwendet.

### <a name="compatible-render-targets-and-shared-bitmaps"></a>Kompatible Renderziele und freigegebene Bitmaps

Sie können Ressourcen zwischen einem Renderziel und kompatiblen Renderzielen freigeben, die von diesem Renderziel erstellt werden. Verwenden Sie zum Erstellen eines kompatiblen Renderziels die [**ID2D1RenderTarget::CreateCompatibleRenderTarget-Methode.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget))

Sie können die [**ID2D1RenderTarget::CreateSharedBitmap-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) verwenden, um eine [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) zu erstellen, die von den beiden Im Methodenaufruf angegebenen Renderzielen gemeinsam genutzt werden kann, wenn die Methode erfolgreich ist. Diese Methode ist erfolgreich, solange die beiden Renderziele das gleiche zugrunde liegende Gerät für das Rendering verwenden.

 

 
