---
description: Ein Direct3D-Gerät kann entweder einen Betriebsstatus oder einen verlorenen Status aufweisen.
ms.assetid: dc4326ba-2ebc-4bca-8fba-02d8db739b8f
title: Verlorene Geräte (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a808cb113f5c2fd35a741e0efc7c6b8af9e127df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341829"
---
# <a name="lost-devices-direct3d-9"></a>Verlorene Geräte (Direct3D 9)

Ein Direct3D-Gerät kann entweder einen Betriebsstatus oder einen verlorenen Status aufweisen. Der Betriebsstatus ist der normale Status des Geräts, auf dem das Gerät ausgeführt wird, und zeigt das gesamte Rendering erwartungsgemäß an. Das Gerät wechselt in den verlorenen Zustand, wenn ein Ereignis, z. b. der Verlust des Tastaturfokus in einer Vollbildanwendung, dazu führt, dass das Rendering unmöglich wird. Der Verlust Status wird durch den stillen Ausfall aller Renderingvorgänge gekennzeichnet, was bedeutet, dass die Renderingmethoden Erfolgs Codes zurückgeben können, auch wenn die Renderingvorgänge fehlschlagen. In dieser Situation wird der Fehlercode D3DERR \_ DeviceLost von IDirect3DDevice9 zurückgegeben [**::P erneut gesendet**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).

Der gesamte Satz von Szenarien, die dazu führen können, dass ein Gerät verloren geht, ist nicht angegeben. Einige typische Beispiele sind z. b. der Fokus Fokus, z. b. wenn der Benutzer Alt + Tab drückt oder wenn ein System Dialogfeld initialisiert wird. Geräte können auch aufgrund eines Energie Verwaltungs Ereignisses oder bei einer anderen Anwendung, die den voll Bild Betrieb annimmt, verloren gehen. Außerdem versetzt jeder Fehler von [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) das Gerät in einen verlorenen Zustand.

Alle Methoden, die von [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) abgeleitet werden, funktionieren garantiert, nachdem ein Gerät verloren gegangen ist. Nach dem Verlust des Geräts verfügt jede Funktion in der Regel über die folgenden drei Optionen:

-   D3DERR \_ DeviceLost schlägt fehl. Dies bedeutet, dass die Anwendung erkennen muss, dass das Gerät verloren gegangen ist, damit die Anwendung erkennt, dass etwas nicht wie erwartet ausgeführt wird.
-   Im Hintergrund \_ tritt ein Fehler auf, oder es werden alle anderen Rückgabecodes zurückgegeben. Wenn eine Funktion im Hintergrund fehlschlägt, kann die Anwendung im Allgemeinen nicht zwischen dem Ergebnis "Erfolg" und einem "stillen Fehler" unterscheiden.
-   Die-Funktion gibt einen Rückgabecode zurück.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:<br/> Ein Direct3D 9-Gerät gibt D3DERR \_ DeviceLost zurück. Nachdem der Wert von [**:P IDirect3DDevice9**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)zurückgegeben wurde, wird das Emulations Verhalten nicht mehr ausgeführt, und alle zukünftigen Aufrufe schlagen fehl, bis das Gerät erfolgreich zurückgesetzt wurde.<br/> Ein Direct3D 9Ex-Gerät gibt nie D3DERR \_ DeviceLost zurück, kann jedoch neue Statusmeldungen zurückgeben (siehe [Änderungen am Geräteverhalten](dx9lh.md)).<br/> |



 

## <a name="responding-to-a-lost-device"></a>Reagieren auf ein verlorenes Gerät

Ein verlorenes Gerät muss Ressourcen (einschließlich Videospeicher Ressourcen) neu erstellen, nachdem es zurückgesetzt wurde. Wenn ein Gerät verloren geht, wird das Gerät von der Anwendung abgefragt, um festzustellen, ob es im Betriebszustand wieder hergestellt werden kann. Andernfalls wartet die Anwendung, bis das Gerät wieder hergestellt werden kann.

Wenn das Gerät wieder hergestellt werden kann, bereitet die Anwendung das Gerät vor, indem alle Videospeicher Ressourcen und alle Austausch Ketten zerstört werden. Anschließend ruft die Anwendung die [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) -Methode auf. Reset ist die einzige Methode, die eine Auswirkung hat, wenn ein Gerät verloren geht, und ist die einzige Methode, mit der eine Anwendung das Gerät von einem verloren gegangenen Betriebszustand ändern kann. Die zurück Setzung schlägt fehl, es sei denn, die Anwendung gibt alle Ressourcen frei, die in D3DPOOL default zugeordnet sind \_ , einschließlich derjenigen, die von den Methoden [**IDirect3DDevice9:: createrendertarget**](/windows/desktop/api) und [**IDirect3DDevice9:: createdepthstencilsurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) erstellt werden.

Meistens werden bei den Hochleistungs Aufrufen von Direct3D keine Informationen darüber zurückgegeben, ob das Gerät verloren gegangen ist. Die Anwendung kann weiterhin Renderingmethoden (z. b. [**IDirect3DDevice9::D rawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)) aufzurufen, ohne eine Benachrichtigung über ein verlorenes Gerät zu erhalten. Intern werden diese Vorgänge verworfen, bis das Gerät auf den Betriebszustand zurückgesetzt wird.

Die Anwendung kann ermitteln, was bei einem verlorenen Gerät zu tun ist, indem der Rückgabewert der [**IDirect3DDevice9:: testkooperativelevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel) -Methode abgefragt wird.

## <a name="locking-operations"></a>Sperr Vorgänge

Intern führt Direct3D ausreichend Arbeit aus, um sicherzustellen, dass ein Sperr Vorgang erfolgreich ist, nachdem ein Gerät verloren gegangen ist. Es ist jedoch nicht sichergestellt, dass die Daten der Videospeicher Ressource während des Sperr Vorgangs korrekt sind. Es ist sichergestellt, dass kein Fehlercode zurückgegeben wird. Dies ermöglicht das Schreiben von Anwendungen, ohne dass bei einem Sperr Vorgang Geräte Verluste auftreten müssen.

## <a name="resources"></a>Ressourcen

Ressourcen können Videospeicher verbrauchen. Da ein verlorener Gerät von dem Videospeicher getrennt ist, der sich im Besitz des Adapters befindet, ist es nicht möglich, die Zuordnung von Video Arbeitsspeicher zu gewährleisten, wenn das Gerät verloren geht. Folglich werden alle Ressourcen Erstellungs Methoden erfolgreich implementiert, indem D3D OK zurückgegeben \_ wird, aber tatsächlich wird nur ein dummysystemspeicher belegt. Da jede Videospeicher Ressource vor dem Ändern der Größe des Geräts zerstört werden muss, besteht kein Problem mit der Überbelegung von Video Arbeitsspeicher. Diese Pseudo Oberflächen ermöglichen das ordnungsgemäße Funktionieren von Sperr-und Kopier Vorgängen, bis die Anwendung [**IDirect3DDevice9 aufruft::P erneut gesendet**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) und ermittelt, dass das Gerät verloren gegangen ist.

Der gesamte Videospeicher muss freigegeben werden, bevor ein Gerät von einem verlorenen in einen Betriebsstatus zurückgesetzt werden kann. Dies bedeutet, dass die Anwendung alle mit [**IDirect3DDevice9:: createadditionalswapchain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) erstellten Austausch Ketten und alle Ressourcen, die in der D3DPOOL- \_ Standard Speicher Klasse platziert werden, freigeben soll. Die Anwendung muss keine Ressourcen in den \_ Speicher Klassen D3DPOOL Managed oder D3DPOOL \_ SystemMem freigeben. Andere Zustandsdaten werden automatisch durch den Übergang in einen Betriebsstatus zerstört.

Es wird empfohlen, Anwendungen mit einem einzigen Codepfad zu entwickeln, um auf Geräte Verluste zu reagieren. Dieser Codepfad ist wahrscheinlich ähnlich, wenn er nicht identisch ist, mit dem Codepfad, der zum Initialisieren des Geräts beim Start verwendet wird.

## <a name="retrieved-data"></a>Abgerufene Daten

Direct3D ermöglicht Anwendungen das Überprüfen von Textur-und renderzuständen mit einem einzelnen Pass Rendering von der Hardware mithilfe von [**IDirect3DDevice9:: ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice). Diese Methode, die in der Regel während der Initialisierung der Anwendung aufgerufen wird, gibt D3DERR \_ DeviceLost zurück, wenn das Gerät verloren gegangen ist.

Direct3D ermöglicht Anwendungen auch das Kopieren generierter oder zuvor geschriebener Images aus Video-Memory-Ressourcen in nicht flüchtige Systemspeicher Ressourcen. Da die Quell Abbilder dieser Übertragungen jederzeit verloren gehen können, kann Direct3D dazu führen, dass solche Kopiervorgänge fehlschlagen, wenn das Gerät verloren geht.

Bei asynchronen Abfragen gibt [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) D3DERR \_ DeviceLost zurück, wenn das Flush-Flag angegeben wird, um für die Anwendung anzugeben, dass **IDirect3DQuery9:: GetData** niemals S OK zurückgibt \_ .

Der Kopiervorgang, [**IDirect3DDevice9:: getfrontbufferdata**](/windows/desktop/api), kann mit D3DERR \_ DeviceLost fehlschlagen, da es keine primäre Oberfläche gibt, wenn das Gerät verloren geht. [**IDirect3DDevice9:: kreateadditionalswapchain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) kann auch mit D3DERR \_ DeviceLost nicht ausgeführt werden, da ein BackBuffer nicht erstellt werden kann, wenn das Gerät verloren geht. Beachten Sie, dass diese Fälle die einzige Instanz von D3DERR \_ DeviceLost außerhalb der [**IDirect3DDevice9::P Resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)-, [**IDirect3DDevice9:: testkooperativelevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel)-und [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) -Methode sind.

## <a name="programmable-shaders"></a>Programmierbare Shader

In Direct3D 9 müssen Vertex-Shader und Pixel-Shader nach dem Zurücksetzen nicht neu erstellt werden. Sie werden gespeichert. In früheren Versionen von DirectX erforderte ein verlorenes Gerät, dass Shader neu erstellt werden mussten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Geräte](direct3d-devices.md)
</dt> </dl>

 

 
