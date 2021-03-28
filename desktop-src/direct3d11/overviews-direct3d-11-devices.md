---
title: Geräte (Direct3D 11-Grafiken)
description: In diesem Abschnitt werden Direct3D 11 Geräte-und Gerätekontext Objekte beschrieben.
ms.assetid: 61d1ea92-e657-4931-8475-74a3123c72f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dda010b3801952e90514fac6307556f8f6fbaff
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104993678"
---
# <a name="devices-direct3d-11-graphics"></a>Geräte (Direct3D 11-Grafiken)

Ein Direct3D-Gerät ordnet Objekte zu und zerstört Sie, rendert primitive und kommuniziert mit einem Grafiktreiber und der Hardware. In Direct3D 11 wird ein Gerät in ein Geräte Objekt zum Erstellen von Ressourcen und ein Gerätekontext Objekt, das das Rendering ausführt, getrennt. In diesem Abschnitt werden Direct3D 11 Geräte-und Gerätekontext Objekte beschrieben.

Objekte, die von einem Gerät erstellt werden, können nicht direkt mit anderen Geräten verwendet werden. Verwenden Sie eine freigegebene Ressource zum Freigeben von Daten zwischen mehreren Geräten, mit der Einschränkung, dass ein frei gegebenes Objekt nur von dem Gerät verwendet werden kann, von dem es erstellt wurde.


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                                                         | BESCHREIBUNG                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Einführung in ein Gerät in Direct3D 11](overviews-direct3d-11-devices-intro.md)<br/>                                                                 | Das Objektmodell Direct3D 11 trennt die Ressourcen Erstellung und Renderingfunktionalität in ein Gerät und einen oder mehrere Kontexte. Diese Trennung dient zum Vereinfachen von Multithreading.<br/>                                                  |
| [Software Ebenen](overviews-direct3d-11-devices-layers.md)<br/>                                                                                        | Die Direct3D 11-Laufzeit wird mit Ebenen erstellt, beginnend mit den grundlegenden Funktionen im Kern und der Erstellung Optionaler und Entwickler-Assist-Funktionen in äußeren Schichten. In diesem Abschnitt werden die Funktionen der einzelnen Ebenen beschrieben.<br/> |
| [Einschränkungen beim Erstellen von Warp-und Referenz Geräten](overviews-direct3d-11-devices-limitations.md)<br/>                                                   | Zum Erstellen von Warp-und Referenz Geräten in Direct3D 10,1 und Direct3D 11,0 sind einige Einschränkungen vorhanden. Diese Einschränkungen werden in diesem Thema erläutert.<br/>                                                                                              |
| [Direct3D 11 auf downlevelhardware](overviews-direct3d-11-devices-downlevel.md)<br/>                                                                   | In diesem Abschnitt wird erläutert, wie Direct3D 11 für die Unterstützung neuer und vorhandener Hardware (von DirectX 9 bis DirectX 11) konzipiert ist.<br/>                                                                                                             |
| [Verwenden von Direct3D 11 Feature-Daten zum ergänzen von Direct3D-Funktionsebenen](using-direct3d-optional-features-to-supplement-direct3d-feature-levels.md)<br/> | Erfahren Sie, wie Sie die Geräte Unterstützung auf optionale Features überprüfen, einschließlich der Features, die in neueren Versionen von Windows hinzugefügt wurden.<br/>                                                                                                           |



 

## <a name="how-to-topics-about-devices"></a>Gewusst wie-Themen zu Geräten



| Thema                                                                                                                                                                                                                                                                                                    | BESCHREIBUNG                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span id="How_To__Create_a_Reference_Device"></span><span id="how_to__create_a_reference_device"></span><span id="HOW_TO__CREATE_A_REFERENCE_DEVICE"></span>[Vorgehensweise: Erstellen eines Referenz Geräts](overviews-direct3d-11-devices-create-ref.md)<br/>                                                 | Hier wird beschrieben, wie ein Referenzgerät erstellt wird.<br/>                            |
| <span id="How_To__Create_a_WARP_Device"></span><span id="how_to__create_a_warp_device"></span><span id="HOW_TO__CREATE_A_WARP_DEVICE"></span>[Vorgehensweise: Erstellen eines Warp-Geräts](overviews-direct3d-11-devices-create-warp.md)<br/>                                                                    | Hier wird beschrieben, wie ein Warp-Gerät erstellt wird.<br/>                                 |
| <span id="How_To__Create_a_Swap_Chain"></span><span id="how_to__create_a_swap_chain"></span><span id="HOW_TO__CREATE_A_SWAP_CHAIN"></span>[Gewusst wie: Erstellen einer SwapChain](overviews-direct3d-11-devices-create-swap-chain.md)<br/>                                                                  | Hier wird beschrieben, wie eine SwapChain erstellt wird.<br/>                                  |
| <span id="How_To__Enumerate_Adapters"></span><span id="how_to__enumerate_adapters"></span><span id="HOW_TO__ENUMERATE_ADAPTERS"></span>[Gewusst wie: Aufzählen von Adaptern](overviews-direct3d-11-devices-enum.md)<br/>                                                                                   | Beschreibt, wie die physischen Anzeige Adapter aufgelistet werden.<br/>              |
| <span id="How_To__Get_Adapter_Display_Modes"></span><span id="how_to__get_adapter_display_modes"></span><span id="HOW_TO__GET_ADAPTER_DISPLAY_MODES"></span>[Gewusst wie: Anzeigen von Adapter Anzeigemodi](overviews-direct3d-11-devices-get-adapter-info.md)<br/>                                           | Hier wird beschrieben, wie Sie die unterstützten Anzeigefunktionen eines Adapters erhalten.<br/> |
| <span id="How_To__Create_a_Device_and_Immediate_Context"></span><span id="how_to__create_a_device_and_immediate_context"></span><span id="HOW_TO__CREATE_A_DEVICE_AND_IMMEDIATE_CONTEXT"></span>[Gewusst wie: Erstellen eines Geräts und eines unmittelbaren Kontexts](overviews-direct3d-11-devices-initialize.md)<br/> | Beschreibt, wie ein Gerät initialisiert wird.<br/>                                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieranleitung für Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

 





