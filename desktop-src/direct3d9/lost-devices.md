---
description: Ein Direct3D-Gerät kann sich entweder in einem Betriebszustand oder in einem verlorenen Zustand befinden.
ms.assetid: dc4326ba-2ebc-4bca-8fba-02d8db739b8f
title: Verlorene Geräte (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 038d03f1d95e4beb90d0e592fc666972db4e92e5a2a986a7711023a6b9fa05b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728578"
---
# <a name="lost-devices-direct3d-9"></a>Verlorene Geräte (Direct3D 9)

Ein Direct3D-Gerät kann sich entweder in einem Betriebszustand oder in einem verlorenen Zustand befinden. Der Betriebszustand ist der normale Zustand des Geräts, in dem das Gerät ausgeführt wird und das gesamte Rendering wie erwartet darstellt. Das Gerät wechselt in den Zustand "Verloren", wenn ein Ereignis, z. B. der Verlust des Tastaturfokus in einer Vollbildanwendung, das Rendering unmöglich macht. Der verlorene Zustand wird durch den automatischen Fehler aller Renderingvorgänge gekennzeichnet, was bedeutet, dass die Renderingmethoden Erfolgscodes zurückgeben können, auch wenn die Renderingvorgänge fehlschlagen. In diesem Fall wird der Fehlercode D3DERR \_ DEVICELOST von [**IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)zurückgegeben.

Der vollständige Satz von Szenarien, die dazu führen können, dass ein Gerät verloren geht, ist nicht angegeben. Einige typische Beispiele sind der Verlust des Fokus, z. B. wenn der Benutzer ALT+TAB drückt oder wenn ein Systemdialog initialisiert wird. Geräte können auch aufgrund eines Energieverwaltungsereignisses oder wenn eine andere Anwendung einen Vollbildbetrieb annimmt, verloren gehen. Darüber hinaus versetzt jeder Fehler von [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) das Gerät in einen verlorenen Zustand.

Alle von [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) abgeleiteten Methoden funktionieren garantiert, nachdem ein Gerät verloren gegangen ist. Nach dem Verlust des Geräts hat jede Funktion im Allgemeinen die folgenden drei Optionen:

-   Fehler bei D3DERR \_ DEVICELOST: Dies bedeutet, dass die Anwendung erkennen muss, dass das Gerät verloren gegangen ist, damit die Anwendung erkennt, dass etwas nicht wie erwartet geschieht.
-   Fehler im Hintergrund, Rückgabe von S \_ OK oder anderer Rückgabecodes: Wenn eine Funktion im Hintergrund fehlschlägt, kann die Anwendung im Allgemeinen nicht zwischen dem Ergebnis von "Erfolg" und einem "automatischen Fehler" unterscheiden.
-   Die Funktion gibt einen Rückgabecode zurück.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:<br/> Ein Direct3D 9-Gerät gibt D3DERR \_ DEVICELOST zurück. Nachdem es von [**IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)zurückgegeben wurde, funktioniert das Emulationsverhalten nicht mehr, und alle zukünftigen Aufrufe schlagen fehl, bis das Gerät erfolgreich zurückgesetzt wurde.<br/> Ein Direct3D 9Ex-Gerät gibt nie D3DERR \_ DEVICELOST zurück, kann aber neue Statusmeldungen zurückgeben (siehe [Änderungen des Geräteverhaltens](dx9lh.md)).<br/> |



 

## <a name="responding-to-a-lost-device"></a>Reagieren auf ein verlorenes Gerät

Ein verlorenes Gerät muss ressourcen (einschließlich Videospeicherressourcen) neu erstellen, nachdem es zurückgesetzt wurde. Wenn ein Gerät verloren geht, fragt die Anwendung das Gerät ab, um festzustellen, ob es im Betriebszustand wiederhergestellt werden kann. Falls nicht, wartet die Anwendung, bis das Gerät wiederhergestellt werden kann.

Wenn das Gerät wiederhergestellt werden kann, bereitet die Anwendung das Gerät vor, indem alle Videospeicherressourcen und Austauschketten zerstört werden. Anschließend ruft die Anwendung die [**IDirect3DDevice9::Reset-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) auf. Reset ist die einzige Methode, die auswirkungen hat, wenn ein Gerät verloren geht, und ist die einzige Methode, mit der eine Anwendung das Gerät von einem verlorenen in einen betriebsbereiten Zustand ändern kann. Das Zurücksetzen schlägt fehl, es sei denn, die Anwendung gibt alle Ressourcen frei, die in D3DPOOL DEFAULT zugeordnet \_ sind, einschließlich der Ressourcen, die von den Methoden [**IDirect3DDevice9::CreateRenderTarget**](/windows/desktop/api) und [**IDirect3DDevice9::CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) erstellt wurden.

In den meisten Teilen geben die häufigen Aufrufe von Direct3D keine Informationen darüber zurück, ob das Gerät verloren gegangen ist. Die Anwendung kann weiterhin Renderingmethoden wie [**IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)aufrufen, ohne eine Benachrichtigung über ein verlorenes Gerät zu erhalten. Intern werden diese Vorgänge verworfen, bis das Gerät in den Betriebszustand zurückgesetzt wird.

Die Anwendung kann bestimmen, was beim Auftreten eines verloren gegangenen Geräts zu tun ist, indem sie den Rückgabewert der [**IDirect3DDevice9::TestCooperativeLevel-Methode abfragt.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel)

## <a name="locking-operations"></a>Sperrvorgänge

Intern führt Direct3D genügend Arbeit aus, um sicherzustellen, dass ein Sperrvorgang erfolgreich ist, nachdem ein Gerät verloren gegangen ist. Es ist jedoch nicht garantiert, dass die Daten der Videospeicherressource während des Sperrvorgangs korrekt sind. Es ist garantiert, dass kein Fehlercode zurückgegeben wird. Dadurch können Anwendungen geschrieben werden, ohne dass während eines Sperrvorgangs Geräteverluste zu beachten sind.

## <a name="resources"></a>Ressourcen

Ressourcen können Videospeicher nutzen. Da ein verlorenes Gerät vom Videospeicher getrennt ist, der dem Adapter gehört, ist es nicht möglich, die Zuordnung des Videospeichers zu garantieren, wenn das Gerät verloren geht. Daher werden alle Methoden zur Ressourcenerstellung implementiert, um erfolgreich zu sein, indem D3D OK zurückgegeben \_ wird, aber tatsächlich nur Dummy-Systemarbeitsspeicher zuweisen. Da jede Videoarbeitsspeicherressource zerstört werden muss, bevor die Größe des Geräts geändert wird, besteht kein Problem bei der überdimensionierten Zuweisung des Videospeichers. Diese Dummyoberflächen ermöglichen es, Sperr- und Kopiervorgänge normal zu funktionieren, bis die Anwendung [**IDirect3DDevice9::P resent aufruft**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) und feststellt, dass das Gerät verloren gegangen ist.

Der gesamte Videospeicher muss freigegeben werden, bevor ein Gerät von einem verlorenen Zustand in einen Betriebszustand zurückgesetzt werden kann. Dies bedeutet, dass die Anwendung alle Swapketten freigeben sollte, die mit [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) erstellt wurden, sowie alle Ressourcen, die in der D3DPOOL \_ DEFAULT-Speicherklasse platziert werden. Die Anwendung muss keine Ressourcen in den Speicherklassen D3DPOOL \_ MANAGED oder D3DPOOL \_ SYSTEMMEM freigeben. Andere Zustandsdaten werden durch den Übergang in einen Betriebszustand automatisch zerstört.

Es wird empfohlen, Anwendungen mit einem einzigen Codepfad zu entwickeln, um auf Geräteverluste zu reagieren. Dieser Codepfad ähnelt wahrscheinlich dem Codepfad, der zum Initialisieren des Geräts beim Start verwendet wird, wenn er nicht identisch ist.

## <a name="retrieved-data"></a>Abgerufene Daten

Direct3D ermöglicht Es Anwendungen, Textur- und Renderzustände anhand des Single-Pass-Renderings durch die Hardware mithilfe von [**IDirect3DDevice9::ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice)zu überprüfen. Diese Methode, die normalerweise während der Initialisierung der Anwendung aufgerufen wird, gibt D3DERR \_ DEVICELOST zurück, wenn das Gerät verloren gegangen ist.

Direct3D ermöglicht es Anwendungen auch, generierte oder zuvor geschriebene Bilder aus Videospeicherressourcen in nicht flüchtige Systemspeicherressourcen zu kopieren. Da die Quellimages solcher Übertragungen jederzeit verloren gegangen sein können, lässt Direct3D zu, dass solche Kopiervorgänge fehlschlagen, wenn das Gerät verloren geht.

In Bezug auf asynchrone Abfragen gibt [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) D3DERR \_ DEVICELOST zurück, wenn das FLUSH-Flag angegeben ist, um der Anwendung anzugeben, dass **IDirect3DQuery9::GetData** nie S OK zurückgibt. \_

Der Kopiervorgang [**IDirect3DDevice9::GetFrontBufferData**](/windows/desktop/api)kann mit D3DERR DEVICELOST fehlschlagen, \_ da keine primäre Oberfläche vorhanden ist, wenn das Gerät verloren geht. [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) kann auch mit D3DERR DEVICELOST fehlschlagen, \_ da kein Backpuffer erstellt werden kann, wenn das Gerät verloren geht. Beachten Sie, dass diese Fälle die einzige Instanz von D3DERR \_ DEVICELOST außerhalb der Methoden [**IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present), [**IDirect3DDevice9::TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel)und [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) sind.

## <a name="programmable-shaders"></a>Programmierbare Shader

In Direct3D 9 müssen Vertex-Shader und Pixel-Shader nach dem Zurücksetzen nicht neu erstellt werden. Sie werden gespeichert. In früheren Versionen von DirectX mussten Shader für ein verlorenes Gerät neu erstellt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Geräte](direct3d-devices.md)
</dt> </dl>

 

 
