---
title: Ressourcen Übersicht
description: Beschreibt Direct2D-Ressourcen und wie Sie freigegeben werden können.
ms.assetid: afd308a7-9524-4436-9a0e-8575383d96fa
keywords:
- Direct2D, Ressourcen
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: bf4eb807a25b592e32a2d83436532af17462d70c
ms.sourcegitcommit: 7d0cc7eb398fee8f5be55cd654a12d29937d643c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/08/2021
ms.locfileid: "104350999"
---
# <a name="resources-overview"></a>Ressourcen Übersicht

Eine Direct2D-Ressource ist ein Objekt, das zum Zeichnen verwendet wird und durch eine Direct2D-Schnittstelle dargestellt wird, z. b. [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) oder [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget). In diesem Thema werden die Arten von Direct2D-Ressourcen und deren Freigabe beschrieben.

Dieses Thema enthält folgende Abschnitte:

-   [Informationen zu Direct2D-Ressourcen](#about-direct2d-resources)
-   [Geräteunabhängige Ressourcen](#device-independent-resources)
-   [Geräte abhängige Ressourcen](#device-dependent-resources)
-   [Freigeben von Factory-Ressourcen](#sharing-factory-resources)
-   [Freigeben von renderzielressourcen](#sharing-render-target-resources)
    -   [Hardwarrenderziele](#hardware-render-targets)
    -   [DXGI-Oberflächen Renderziele](#dxgi-surface-render-targets)
    -   [Kompatible Renderziele und freigegebene Bitmaps](#compatible-render-targets-and-shared-bitmaps)

## <a name="about-direct2d-resources"></a>Informationen zu Direct2D-Ressourcen

Viele hardwarebeschleunigte 2D-APIs sind für ein CPU-orientiertes Ressourcenmodell und eine Reihe von Renderingvorgängen konzipiert, die für CPUs gut geeignet sind. dann wird ein Teil der API Hardware beschleunigt. Zum Implementieren dieser APIs ist ein Ressourcen-Manager zum Mapping von CPU-Ressourcen zu Ressourcen auf der GPU erforderlich. Aufgrund von GPU-Einschränkungen können einige Vorgänge möglicherweise nicht in jedem Fall beschleunigt werden. In diesen Fällen muss der Ressourcen-Manager zwischen der CPU und der GPU (was teuer ist) zwischen der CPU und der GPU kommunizieren, sodass er zum CPU-Rendering übergehen kann. In einigen Fällen kann es vorkommen, dass Renderingvorgänge auf die CPU vollständig zurückgesetzt werden. Außerdem sind bei Renderingvorgängen, die einfach erscheinen, möglicherweise temporäre zwischenrenderingschritte erforderlich, die nicht in der API verfügbar gemacht werden und zusätzliche GPU-Ressourcen erfordern.

Direct2D bietet eine direktere Zuordnung, um die GPU vollständig zu nutzen. Es bietet zwei Kategorien von Ressourcen: Geräte unabhängig und Geräte abhängig.

-   Geräteunabhängige Ressourcen, z. b. [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), werden auf der CPU beibehalten.
-   Geräte abhängige Ressourcen, z. b. [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) und [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), werden direkt den Ressourcen auf der GPU zugeordnet (wenn die Hardwarebeschleunigung verfügbar ist). Renderingaufrufe werden durch das Kombinieren von Scheitelpunkt-und Abdeckungs Informationen aus einer Geometrie mit texturierungsinformationen durch die geräteabhängigen Ressourcen ausgeführt.

Wenn Sie Geräte abhängige Ressourcen erstellen, werden Systemressourcen (die GPU, falls verfügbar oder die CPU) zugeordnet, wenn das Gerät erstellt wird, und sich nicht von einem Renderingvorgang zu einem anderen ändern. Durch diese Situation entfällt die Notwendigkeit eines Ressourcen-Managers. Zusätzlich zu den allgemeinen Leistungsverbesserungen, die durch die Beseitigung eines Ressourcen-Managers bereitgestellt werden, können Sie mit diesem Modell jedes zwischen Rendering direkt steuern.

Da Direct2D so viel Kontrolle über Ressourcen bietet, müssen Sie sich mit den verschiedenen Arten von Ressourcen und deren Verwendung vertraut machen.

## <a name="device-independent-resources"></a>Device-Independent Ressourcen

Wie im vorherigen Abschnitt beschrieben, befinden sich geräteunabhängige Ressourcen immer auf der CPU und sind niemals einem Hardware Rendering-Gerät zugeordnet. Im folgenden sind geräteunabhängige Ressourcen aufgeführt:

-   [**ID2D1DrawingStateBlock**](/windows/win32/api/d2d1/nn-d2d1-id2d1drawingstateblock)
-   [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
-   [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) und die Schnittstellen, die von ihm erben.
-   [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) und [ **ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)
-   [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle)

Verwenden Sie eine [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)-geräteunabhängige Ressource, um geräteunabhängige Ressourcen zu erstellen. (Um eine Factory zu erstellen, verwenden Sie die Funktion " [**kreatefactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) ".)

Mit Ausnahme von renderzielen sind alle von einer Factory erstellten Ressourcen Geräte unabhängig. Ein Renderziel ist eine Geräte abhängige Ressource.

## <a name="device-dependent-resources"></a>Device-Dependent Ressourcen

Jede Ressource, die nicht in der vorherigen Liste benannt ist, ist eine Geräte abhängige Ressource. Geräte abhängige Ressourcen sind einem bestimmten renderinggerät zugeordnet. Wenn die Hardwarebeschleunigung verfügbar ist, ist dieses Gerät die GPU. In anderen Fällen ist es die CPU.

Verwenden Sie zum Erstellen der meisten geräteabhängigen Ressourcen ein Renderziel. Verwenden Sie in den meisten Fällen eine Factory zum Erstellen eines Renderziels.

Im folgenden finden Sie Beispiele für Geräte abhängige Ressourcen:

-   [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) und die Schnittstellen, die von ihm erben. Verwenden Sie ein Renderziel, um Pinsel zu erstellen.
-   [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer). Verwenden Sie zum Erstellen von Ebenen ein Renderziel.
-   [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) und die Schnittstellen, die von ihm erben. Verwenden Sie zum Erstellen eines Renderziels eine Factory oder ein anderes Renderziel.

> [!Note]  
> Ab Windows 8 gibt es neue Schnittstellen, mit denen Geräte abhängige Ressourcen erstellt werden. Eine [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) und eine [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) können eine Ressource freigeben, wenn der Gerätekontext und die Ressource aus demselben **ID2D1Device** erstellt werden.

 

Geräte abhängige Ressourcen werden unbrauchbar, wenn die zugehörigen renderinggeräte nicht mehr verfügbar sind. Dies bedeutet, dass Sie beim Empfang des D2DERR-Erstellungs [**\_ \_ Ziel**](direct2d-error-codes.md) Fehlers für ein Renderziel das Renderziel und alle zugehörigen Ressourcen neu erstellen müssen.

## <a name="sharing-factory-resources"></a>Freigeben von Factory-Ressourcen

Sie können alle geräteunabhängigen Ressourcen, die von einer Factory erstellt wurden, mit allen anderen Ressourcen (Geräte unabhängig oder Geräte abhängig) freigeben, die von der gleichen Factory erstellt wurden. Beispielsweise können Sie zwei [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) -Objekte zum Zeichnen desselben [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) verwenden, wenn beide **ID2D1RenderTarget** -Objekte von derselben Factory erstellt wurden.

Die senkschnittstellen ([**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink), [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)und [**ID2D1TessellationSink**](/windows/win32/api/d2d1/nn-d2d1-id2d1tessellationsink)) können mit von einer beliebigen Factory erstellten Ressourcen gemeinsam genutzt werden. Im Gegensatz zu anderen Schnittstellen in Direct2D kann jede Implementierung einer Sink-Schnittstelle verwendet werden. Beispielsweise können Sie Ihre eigene Implementierung von **ID2D1SimplifiedGeometrySink** verwenden.

## <a name="sharing-render-target-resources"></a>Freigeben von renderzielressourcen

Die Möglichkeit, von einem Renderziel erstellte Ressourcen freizugeben, hängt von der Art des Renderziels ab. Wenn Sie ein Renderziel vom Typ [**D2D1 \_ \_ renderzieltyp \_ \_ Standard**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type)erstellen, können die von diesem Renderziel erstellten Ressourcen nur von diesem Renderziel verwendet werden (es sei denn, das Renderziel passt in eine der Kategorien, die in den folgenden Abschnitten beschrieben sind). Dies liegt daran, dass Sie nicht wissen, auf welchem Gerät das Renderziel am Ende steht – es könnte das Rendering an lokaler Hardware, Software oder auf der Hardware eines Remote Clients durchführen. Sie könnten z. b. ein Programm schreiben, das nicht mehr funktioniert, wenn es Remote angezeigt wird, oder wenn das Renderziel über die maximale Größe hinausgeht, die von der renderinghardware unterstützt wird.

In den folgenden Abschnitten werden die Umstände beschrieben, unter denen eine durch ein Renderziel erstellte Ressource mit einem anderen Renderziel gemeinsam genutzt werden kann.

### <a name="hardware-render-targets"></a>Hardwarrenderziele

Sie können Ressourcen zwischen jedem Renderziel freigeben, das explizit Hardware verwendet, solange der Remoting-Modus kompatibel ist. Der Remoting-Modus ist nur garantiert kompatibel, wenn beide Renderziele das Flag " [**D2D1 \_ \_ Renderziel \_ Usage \_ Force \_ Bitmap \_ Remoting**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) " oder " **D2D1 \_ \_ renderzielverwendung \_ \_ GDI- \_ kompatibel** " verwenden, oder wenn keines der Flags angegeben ist. Mit diesen Einstellungen wird sichergestellt, dass sich die Ressourcen immer auf demselben Computer befinden. Um einen Verwendungs Modus anzugeben, legen Sie das Feld **Verwendung** der [**D2D1 \_ \_ Renderziel- \_ Eigenschaften**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) Struktur fest, die Sie zum Erstellen des Renderziels mit einem oder mehreren **D2D1- \_ \_ Renderziel- \_ nutzungsflags** verwendet haben.

Legen Sie zum Erstellen eines Renderziels, das explizit das Hardware Rendering verwendet, das **typanfeld** der [**D2D1 \_ \_ Renderziel- \_ Eigenschafts**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) Struktur fest, das Sie zum Erstellen des Renderziels auf [**D2D1 \_ \_ renderzieltyp \_ \_ Hardware**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type)verwendet haben.

### <a name="dxgi-surface-render-targets"></a>DXGI-Oberflächen Renderziele

Sie können Ressourcen, die von einem DXGI-Oberflächen Rendering erstellt wurden, mit einem beliebigen anderen DXGI-Oberflächen Renderziel freigeben, das das gleiche zugrunde liegende Direct3D-Gerät verwendet.

### <a name="compatible-render-targets-and-shared-bitmaps"></a>Kompatible Renderziele und freigegebene Bitmaps

Sie können Ressourcen zwischen einem Renderziel und kompatiblen renderzielen freigeben, die von diesem Renderziel erstellt werden. Wenn Sie ein kompatibles Renderziel erstellen möchten, verwenden Sie die [**ID2D1RenderTarget::**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) -Methode.

Sie können die [**ID2D1RenderTarget:: kreatesharedbitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) -Methode verwenden, um eine [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) zu erstellen, die von den beiden renderzielen gemeinsam genutzt werden kann, die im Methoden Aufrufwert angegeben werden, wenn die Methode erfolgreich ist. Diese Methode ist erfolgreich, solange die beiden Renderziele dasselbe zugrunde liegende Gerät zum Rendern verwenden.

 

 
