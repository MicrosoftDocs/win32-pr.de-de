---
description: Die Ressourcenverwaltung ist der Prozess, bei dem Ressourcen aus dem Speicher des System Speichers in den Gerät zugänglichen Speicher herauf gestuft und aus dem Speicher des Geräts verworfen werden.
ms.assetid: 4aa55313-b86c-48e7-829a-a0917c2ebae7
title: Verwalten von Ressourcen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ef7a8be0e71c652b6e3f2ed467e866fd922791
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213880"
---
# <a name="managing-resources-direct3d-9"></a>Verwalten von Ressourcen (Direct3D 9)

Die Ressourcenverwaltung ist der Prozess, bei dem Ressourcen aus dem Speicher des System Speichers in den Gerät zugänglichen Speicher herauf gestuft und aus dem Speicher des Geräts verworfen werden. Die Direct3D-Laufzeit verfügt über einen eigenen Verwaltungs Algorithmus, der auf einer zuletzt verwendeten Prioritäts Methode basiert. Direct3D wechselt zu einer zuletzt verwendeten Prioritäts Methode, wenn erkannt wird, dass mehr Ressourcen vorhanden sind, als auf dem Gerät zugänglichen Arbeitsspeicher vorhanden sind, werden in einem einzelnen Frame zwischen [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api) und [**IDirect3DDevice9:: EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) -Aufrufen verwendet.

Verwenden Sie das [**D3DPOOL- \_ Standardflag**](./d3dpool.md) zum Zeitpunkt der Erstellung, um anzugeben, dass eine Ressource in den Speicherpool eingefügt wird, der sich am besten für die für die angegebene Ressource angeforderten Verwendungen eignet. Dabei handelt es sich normalerweise um Videospeicher, einschließlich lokaler Video Arbeitsspeicher und Accelerated Graphics Port Speicher (AGP). Ressourcen im Standard Pool bleiben nicht durch Übergänge zwischen den verlorenen und Betriebszuständen des Geräts erhalten. Diese Ressourcen müssen vor dem Aufrufen von Reset freigegeben werden und müssen dann neu erstellt werden.

Verwenden Sie das [**D3DPOOL \_ Managed**](./d3dpool.md) -Flag zum Zeitpunkt der Erstellung, um eine verwaltete Ressource anzugeben. Verwaltete Ressourcen bleiben durch Übergänge zwischen den verlorenen und Betriebszuständen des Geräts erhalten. Diese Ressourcen sind sowohl im Video-als auch im Systemspeicher vorhanden. Eine verwaltete Ressource wird in den Videospeicher kopiert, wenn Sie während des Renderings benötigt wird. Das Gerät kann mit einem Rückruf von [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)wieder hergestellt werden, und solche Ressourcen funktionieren weiterhin normal, ohne dass Sie mit Daten neu geladen werden. Wenn das Gerät jedoch zerstört und neu erstellt werden muss, müssen alle Ressourcen neu erstellt werden.

Die Ressourcenverwaltung wird nicht für Ressourcen empfohlen, die sich mit hoher Häufigkeit ändern. Beispielsweise werden Vertex-und Index Puffer, die zum Durchlaufen eines Szenen Diagramms verwendet werden, jedes Frame Rendering, das nur für den Benutzer sichtbar ist, in jedem Rahmen geändert. Da verwaltete Ressourcen vom Systemspeicher unterstützt werden, müssen die Konstanten Änderungen im Systemspeicher aktualisiert werden, was zu einer schwerwiegenden Beeinträchtigung der Leistung führen kann. In diesem speziellen Szenario sollte [**D3DPOOL \_ default**](./d3dpool.md) zusammen mit [**D3DUSAGE \_ Dynamic**](d3dusage.md) verwendet werden.

Ein weiteres Beispiel, für das die Ressourcenverwaltung nicht empfohlen wird (und von der Laufzeit explizit nicht zulässig ist) ist die Verwaltung einer mit [**D3DUSAGE \_ renderTarget**](d3dusage.md)erstellten Textur. Wenn der von Renderingzielen verwendete Arbeitsspeicher von der Laufzeit verwaltet wird, müsste der Inhalt während des Renderings ständig in den Systemspeicher kopiert werden, was zu hohen Leistungseinbußen führen würde. Aus diesem Grund müssen Renderziele im Standard Pool erstellt werden. Wenn der CPU-Zugriff der in einem Renderziel enthaltenen Daten erforderlich ist, müssen die Daten in eine Ressource kopiert werden, die in [**D3DPOOL \_ SystemMem**](./d3dpool.md) mithilfe von [**IDirect3DDevice9:: UpdateTexture**](/windows/desktop/api)oder [**IDirect3DDevice9:: updatesurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) erstellt wurde.

Weitere Informationen zum verlorenen Status eines Geräts finden Sie unter [verlorene Geräte (Direct3D 9)](lost-devices.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Ressourcen](direct3d-resources.md)
</dt> </dl>

 

 
