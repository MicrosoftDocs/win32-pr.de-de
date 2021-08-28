---
title: Einführung in ein Gerät in Direct3D 11
description: Das Direct3D 11-Objektmodell trennt die Ressourcenerstellungs- und Renderingfunktionen in ein Gerät und einen oder mehrere Kontexte. diese Trennung wurde entwickelt, um Multithreading zu erleichtern.
ms.assetid: b9b45d18-f7b7-40f9-ae4e-576ca7a6eba7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9459574ad7d8732714ac54519294ae232e4d8d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475706"
---
# <a name="introduction-to-a-device-in-direct3d-11"></a>Einführung in ein Gerät in Direct3D 11

Das Direct3D 11-Objektmodell trennt die Ressourcenerstellungs- und Renderingfunktionen in ein Gerät und einen oder mehrere Kontexte. diese Trennung wurde entwickelt, um Multithreading zu erleichtern.

-   [Device](#introduction-to-a-device-in-direct3d-11)
-   [Gerätekontext](#device-context)
    -   [Sofortiger Kontext](#immediate-context)
    -   [Verzögerter Kontext](#deferred-context)
-   [Überlegungen zum Threading](#threading-considerations)
-   [Zugehörige Themen](#related-topics)

## <a name="device"></a>Gerät

Ein Gerät wird verwendet, um Ressourcen zu erstellen und die Funktionen eines Adapters aufzählen zu können. In Direct3D 11 wird ein Gerät mit einer [**ID3D11Device-Schnittstelle**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) dargestellt.

Jede Anwendung muss mindestens ein Gerät haben. Die meisten Anwendungen erstellen nur ein Gerät. Erstellen Sie ein Gerät für einen der auf Ihrem Computer installierten Hardwaretreiber, indem Sie [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) oder [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) aufrufen und den Treibertyp mit dem [**D3D \_ DRIVER \_ TYPE-Flag**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) angeben. Jedes Gerät kann je nach gewünschter Funktionalität einen oder mehrere Gerätekontexte verwenden.

## <a name="device-context"></a>Gerätekontext

Ein Gerätekontext enthält die Umstände oder Einstellungen, in denen ein Gerät verwendet wird. Genauer gesagt wird ein Gerätekontext verwendet, um den Pipelinezustand zu festlegen und Renderingbefehle mithilfe der Ressourcen zu generieren, die sich im Besitz eines Geräts befinden. Direct3D 11 implementiert zwei Arten von Gerätekontexten: einen für sofortiges Rendering und einen für verzögertes Rendering. beide Kontexte werden mit einer [**ID3D11DeviceContext-Schnittstelle**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) dargestellt.

### <a name="immediate-context"></a>Sofortiger Kontext

Ein direkter Kontext wird direkt an den Treiber gerendert. Jedes Gerät verfügt über einen und nur einen unmittelbaren Kontext, der Daten von der GPU abrufen kann. Ein direkter Kontext kann verwendet werden, um eine Befehlsliste sofort zu rendern (oder [wieder zu rendern).](overviews-direct3d-11-render-multi-thread-command-list.md)

Es gibt zwei Möglichkeiten, einen unmittelbaren Kontext zu erhalten:

-   Durch Aufrufen von [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) oder [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).
-   Durch Aufrufen [**von ID3D11Device::GetImmediateContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).

### <a name="deferred-context"></a>Verzögerter Kontext

Ein verzögerter Kontext zeichnet GPU-Befehle in einer [Befehlsliste auf.](overviews-direct3d-11-render-multi-thread-command-list.md) Ein verzögerter Kontext wird hauptsächlich für Multithreading verwendet und ist für eine Singlethreadanwendung nicht erforderlich. Ein verzögerter Kontext wird in der Regel von einem Arbeitsthread anstelle des Hauptrenderingthreads verwendet. Wenn Sie einen verzögerten Kontext erstellen, erbt er keinen Zustand vom unmittelbaren Kontext.

Um einen verzögerten Kontext zu erhalten, rufen Sie [**ID3D11Device::CreateDeferredContext auf.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext)

Jeder Kontext – unmittelbar oder verzögert – kann in jedem Thread verwendet werden, solange der Kontext nur in einem Thread gleichzeitig verwendet wird.

## <a name="threading-considerations"></a>Überlegungen zum Threading

In dieser Tabelle werden die Unterschiede zwischen dem Threadingmodell in Direct3D 11 und früheren Versionen von Direct3D aufgeführt.




| | | Unterschiede zwischen Direct3D 11 und früheren Versionen von Direct3D:<br /> Alle <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device-Schnittstellenmethoden</strong></a> sind Freithreadmethoden, was bedeutet, dass es sicher ist, dass mehrere Threads die Funktionen gleichzeitig aufrufen.<br /><ul><li>Alle <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>von ID3D11DeviceChild</strong></a>abgeleiteten Schnittstellen<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer"><strong>(ID3D11Buffer,</strong></a> <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a>usw.) sind Freithreads.</li><li>Direct3D 11 teilt das Erstellen und Rendern von Ressourcen in zwei Schnittstellen auf. Map, Unmap, Begin, End und GetData werden in <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> implementiert, da <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> die Reihenfolge der Vorgänge stark definiert. <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11resource"><strong>ID3D11Resource-</strong></a> und <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchrone</strong></a> Schnittstellen implementieren auch Methoden für Freethreadvorgänge.</li><li>Die <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext-Methoden</strong></a> (mit Ausnahme der Methoden, die in <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>vorhanden sind) sind kein Freethreading, d. h. sie erfordern Singlethreading. Möglicherweise ruft nur ein Thread eine seiner Methoden (Zeichnen, Kopieren, Zuordnen usw.) gleichzeitig auf.</li><li>Im Allgemeinen minimiert Freethreading die Anzahl der verwendeten Synchronisierungsprimitiven sowie deren Dauer. Eine Anwendung, die die Synchronisierung über einen längeren Zeitraum verwendet, kann sich jedoch direkt darauf auswirken, wie viel Parallelität eine Anwendung erreichen kann.</li></ul>ID3D10Device-Schnittstellenmethoden sind nicht als Freethread-Methoden konzipiert. ID3D10Device implementiert alle Erstellungs- und Renderingfunktionen (wie ID3D9Device in Direct3D 9). Map und Unmap werden auf von ID3D10Resource abgeleiteten Schnittstellen implementiert, Begin, End und GetData werden auf ID3D10Asynchronous abgeleiteten Schnittstellen implementiert.<br /> | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geräte](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 





