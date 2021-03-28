---
title: Einführung in ein Gerät in Direct3D 11
description: Das Objektmodell Direct3D 11 trennt die Ressourcen Erstellung und Renderingfunktionalität in ein Gerät und einen oder mehrere Kontexte. Diese Trennung dient zum Vereinfachen von Multithreading.
ms.assetid: b9b45d18-f7b7-40f9-ae4e-576ca7a6eba7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b03333c6594f17d85fee28880e46928241e06c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104976049"
---
# <a name="introduction-to-a-device-in-direct3d-11"></a>Einführung in ein Gerät in Direct3D 11

Das Objektmodell Direct3D 11 trennt die Ressourcen Erstellung und Renderingfunktionalität in ein Gerät und einen oder mehrere Kontexte. Diese Trennung dient zum Vereinfachen von Multithreading.

-   [Device](#introduction-to-a-device-in-direct3d-11)
-   [Gerätekontext](#device-context)
    -   [Sofortiger Kontext](#immediate-context)
    -   [Verzögerter Kontext](#deferred-context)
-   [Überlegungen zum Threading](#threading-considerations)
-   [Zugehörige Themen](#related-topics)

## <a name="device"></a>Sicherungsmedium

Ein Gerät wird zum Erstellen von Ressourcen und zum Auflisten der Funktionen eines Anzeige Adapters verwendet. In Direct3D 11 wird ein Gerät mit einer [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) -Schnittstelle dargestellt.

Jede Anwendung muss mindestens ein Gerät aufweisen, die meisten Anwendungen erstellen nur ein Gerät. Erstellen Sie ein Gerät für einen der Hardwaretreiber, die auf Ihrem Computer installiert sind, indem Sie [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) oder [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) aufrufen und den Treibertyp mit dem [**D3D \_ Driver \_ Type**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) -Flag angeben. Jedes Gerät kann abhängig von der gewünschten Funktionalität einen oder mehrere Geräte Kontexte verwenden.

## <a name="device-context"></a>Gerätekontext

Ein Gerätekontext enthält den Umstand oder die Einstellung, in der ein Gerät verwendet wird. Genauer gesagt wird ein Gerätekontext verwendet, um den Pipeline Status festzulegen und renderingbefehle mithilfe der Ressourcen zu generieren, die sich im Besitz eines Geräts befinden. Direct3D 11 implementiert zwei Arten von Geräte Kontexten, eine für sofortiges Rendering und die andere für verzögertes Rendering. Beide Kontexte werden mit einer [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Schnittstelle dargestellt.

### <a name="immediate-context"></a>Sofortiger Kontext

Ein unmittelbarer Kontext wird direkt in den Treiber gerendert. Jedes Gerät verfügt über einen und nur einen unmittelbaren Kontext, der Daten von der GPU abrufen kann. Ein sofortiger Kontext kann verwendet werden, um eine [Befehlsliste](overviews-direct3d-11-render-multi-thread-command-list.md)sofort zu Rendering (oder wiederzugeben).

Es gibt zwei Möglichkeiten, einen unmittelbaren Kontext zu erhalten:

-   Durch Aufrufen von [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) oder [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).
-   Durch Aufrufen von [**ID3D11Device:: getimmediatecontext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).

### <a name="deferred-context"></a>Verzögerter Kontext

Ein verzögerter Kontext zeichnet GPU-Befehle in einer [Befehlsliste](overviews-direct3d-11-render-multi-thread-command-list.md)auf. Ein verzögerter Kontext wird hauptsächlich für Multithreading verwendet und ist für eine Single Thread-Anwendung nicht erforderlich. Ein verzögerter Kontext wird im Allgemeinen von einem Arbeits Thread anstelle des hauptrenderingthreads verwendet. Wenn Sie einen verzögerten Kontext erstellen, erben Sie keinen Zustand aus dem unmittelbaren Kontext.

Um einen verzögerten Kontext abzurufen, nennen Sie [**ID3D11Device:: | atedeferredcontext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).

Jeder Kontext, der unmittelbar oder verzögert ist, kann in jedem Thread verwendet werden, solange der Kontext nur in einem Thread gleichzeitig verwendet wird.

## <a name="threading-considerations"></a>Überlegungen zum Threading

In dieser Tabelle werden die Unterschiede im Threading Modell in Direct3D 11 aus früheren Versionen von Direct3D hervorgehoben.



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 11 und früheren Versionen von Direct3D:<br/> Alle <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> -Schnittstellen Methoden sind frei Thread. Dies bedeutet, dass es sicher ist, dass mehrere Threads gleichzeitig die Funktionen aufzurufen.<br/>
<ul>
<li>Alle <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>-abgeleiteten Schnittstellen (<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer"><strong>ID3D11Buffer</strong></a>, <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a>usw.) sind frei Thread.</li>
<li>Direct3D 11 teilt das Erstellen und Rendern von Ressourcen in zwei Schnittstellen auf. Map, unmap, BEGIN, End und GetData werden auf <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>Verknüpfung id3d11devicecontext aus</strong></a> implementiert, da <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> die Reihenfolge der Vorgänge stark definiert. <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11resource"><strong>ID3D11Resource</strong></a> -und <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a> -Schnittstellen implementieren auch Methoden für frei Hand Thread Vorgänge.</li>
<li>Die <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>Verknüpfung id3d11devicecontext aus</strong></a> -Methoden (mit Ausnahme derjenigen, die auf <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>vorhanden sind) sind nicht freigegeben, d. h., Sie erfordern ein einzelnes Threading. Nur ein Thread kann auf sichere Weise eine seiner Methoden (Draw, Copy, Map usw.) gleichzeitig aufrufen.</li>
<li>Im Allgemeinen minimiert das kostenlose Threading die Anzahl der verwendeten Synchronisierungs primitiven und deren Dauer. Eine Anwendung, die die Synchronisierung für einen längeren Zeitraum verwendet, kann jedoch direkt beeinflussen, wie viel Parallelität eine Anwendung erwarten kann.</li>
</ul>
ID3D10Device-Schnittstellen Methoden sind nicht als frei Hand Thread konzipiert. ID3D10Device implementiert alle Erstellungs-und Renderingfunktionen (wie ID3D9Device in Direct3D 9). Map und unmap werden auf ID3D10Resource-abgeleiteten Schnittstellen implementiert, BEGIN, End und GetData werden auf von ID3D10Asynchronous abgeleiteten Schnittstellen implementiert.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geräte](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 





