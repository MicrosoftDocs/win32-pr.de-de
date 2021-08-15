---
description: Die Ressourcenverwaltung ist der Prozess, bei dem Ressourcen aus dem Systemspeicher in einen speicherbereiten Speicher mit Geräteverfügbarkeit heraufgestuft und aus dem vom Gerät zugänglichen Speicher verworfen werden.
ms.assetid: 4aa55313-b86c-48e7-829a-a0917c2ebae7
title: Verwalten von Ressourcen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b860f1c394de932f167de94a3552315b1b70396e9900fccc079ab09142c9e31c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728463"
---
# <a name="managing-resources-direct3d-9"></a>Verwalten von Ressourcen (Direct3D 9)

Die Ressourcenverwaltung ist der Prozess, bei dem Ressourcen aus dem Systemspeicher in einen speicherbereiten Speicher mit Geräteverfügbarkeit heraufgestuft und aus dem vom Gerät zugänglichen Speicher verworfen werden. Die Direct3D-Laufzeit verfügt über einen eigenen Verwaltungsalgorithmus, der auf einer Am wenigsten kürzlich verwendeten Prioritätstechnik basiert. Direct3D wechselt zu einer zuletzt verwendeten Prioritätstechnik, wenn erkannt wird, dass mehr Ressourcen, als im gerätezugänglichen Speicher gleichzeitig vorhanden sein können, in einem einzelnen Frame verwendet werden – zwischen [**IDirect3DDevice9::BeginScene-**](/windows/desktop/api) und [**IDirect3DDevice9::EndScene-Aufrufen.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene)

Verwenden Sie das [**D3DPOOL \_ DEFAULT-Flag**](./d3dpool.md) zur Erstellungszeit, um anzugeben, dass eine Ressource im Speicherpool platziert wird, der für die für die angegebene Ressource angeforderte Nutzung am besten geeignet ist. Dies ist in der Regel Videospeicher, einschließlich des lokalen Videospeichers und des beschleunigten AGP-Speichers (Graphics Port). Ressourcen im Standardpool bleiben nicht über Übergänge zwischen dem Verloren-Status und dem Betriebszustände des Geräts erhalten. Diese Ressourcen müssen vor dem Aufrufen von reset freigegeben und dann neu erstellt werden.

Verwenden Sie das [**D3DPOOL \_ MANAGED-Flag**](./d3dpool.md) zum Zeitpunkt der Erstellung, um eine verwaltete Ressource anzugeben. Verwaltete Ressourcen bleiben über Übergänge zwischen dem Verloren-Status und dem Betriebszustände des Geräts erhalten. Diese Ressourcen sind sowohl im Video- als auch im Systemspeicher vorhanden. Eine verwaltete Ressource wird in den Videospeicher kopiert, wenn sie während des Renderings benötigt wird. Das Gerät kann mit einem Aufruf von [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)wiederhergestellt werden, und solche Ressourcen funktionieren weiterhin normal, ohne dass sie mit Daten erneut geladen werden. Wenn das Gerät jedoch zerstört und neu erstellt werden muss, müssen alle Ressourcen neu erstellt werden.

Die Ressourcenverwaltung wird nicht für Ressourcen empfohlen, die sich mit hoher Häufigkeit ändern. Beispielsweise ändern Scheitelpunkt- und Indexpuffer, die zum Durchlaufen eines Szenendiagramms verwendet werden, bei jedem Frame, der nur die für den Benutzer sichtbare Geometrie rendert, jeden Frame. Da verwaltete Ressourcen durch Systemspeicher gesichert werden, müssen die konstanten Änderungen im Systemspeicher aktualisiert werden, was zu einer schwerwiegenden Leistungsbeeinträchtigung führen kann. Für dieses spezielle Szenario sollte [**D3DPOOL \_ DEFAULT**](./d3dpool.md) zusammen mit [**D3DUSAGE \_ DYNAMIC**](d3dusage.md) verwendet werden.

Ein weiteres Beispiel, für das die Ressourcenverwaltung nicht empfohlen wird (und von der Laufzeit explizit nicht zugelassen wird), ist die Verwaltung einer Textur, die mit [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md)erstellt wurde. Wenn der von Renderzielen verwendete Arbeitsspeicher von der Laufzeit verwaltet wird, muss der Inhalt während des Renderings ständig in den Systemspeicher kopiert werden, was zu großen Leistungseinbußen führt. Aus diesem Grund müssen Renderziele im Standardpool erstellt werden. Wenn CPU-Zugriff auf die in einem Renderziel enthaltenen Daten erforderlich ist, müssen die Daten in eine Ressource kopiert werden, die in [**D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) mit [**IDirect3DDevice9::UpdateTexture**](/windows/desktop/api)oder [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) erstellt wurde.

Weitere Informationen zum Verlustzustand eines Geräts finden Sie unter [Verlorene Geräte (Direct3D 9).](lost-devices.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Ressourcen](direct3d-resources.md)
</dt> </dl>

 

 
