---
title: Geräte (Direct3D 11-Grafiken)
description: In diesem Abschnitt werden Direct3D 11-Geräte- und Gerätekontextobjekte beschrieben.
ms.assetid: 61d1ea92-e657-4931-8475-74a3123c72f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e77cfd255c43cc902f2583fe22575bef2567609f43b6f893984e99dec713532
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851120"
---
# <a name="devices-direct3d-11-graphics"></a>Geräte (Direct3D 11-Grafiken)

Ein Direct3D-Gerät ordnet Objekte zu und zerstört sie, rendert Primitive und kommuniziert mit einem Grafiktreiber und der Hardware. In Direct3D 11 wird ein Gerät in ein Geräteobjekt zum Erstellen von Ressourcen und ein Gerätekontextobjekt, das renderingt, getrennt. In diesem Abschnitt werden Direct3D 11-Geräte- und Gerätekontextobjekte beschrieben.

Von einem Gerät erstellte Objekte können nicht direkt mit anderen Geräten verwendet werden. Verwenden Sie eine freigegebene Ressource, um Daten zwischen mehreren Geräten frei zu geben, mit der Einschränkung, dass ein freigegebenes Objekt nur von dem Gerät verwendet werden kann, das es erstellt hat.


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                                                         | Beschreibung                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Einführung in ein Gerät in Direct3D 11](overviews-direct3d-11-devices-intro.md)<br/>                                                                 | Das Direct3D 11-Objektmodell trennt die Ressourcenerstellungs- und Renderingfunktionen in ein Gerät und einen oder mehrere Kontexte. diese Trennung wurde entwickelt, um Multithreading zu erleichtern.<br/>                                                  |
| [Softwareebenen](overviews-direct3d-11-devices-layers.md)<br/>                                                                                        | Die Direct3D 11-Runtime wird mit Ebenen erstellt, beginnend mit der grundlegenden Funktionalität im Kern und dem Erstellen optionaler und entwicklerassistenter Funktionen in äußeren Ebenen. In diesem Abschnitt werden die Funktionen der einzelnen Ebenen beschrieben.<br/> |
| [Einschränkungen beim Erstellen von WARP- und Verweisgeräten](overviews-direct3d-11-devices-limitations.md)<br/>                                                   | Beim Erstellen von WARP- und Reference-Geräten in Direct3D 10.1 und Direct3D 11.0 gelten einige Einschränkungen. In diesem Thema werden diese Einschränkungen erläutert.<br/>                                                                                              |
| [Direct3D 11 auf Downlevelhardware](overviews-direct3d-11-devices-downlevel.md)<br/>                                                                   | In diesem Abschnitt wird erläutert, wie Direct3D 11 für die Unterstützung neuer und vorhandener Hardware von DirectX 9 bis DirectX 11 konzipiert ist.<br/>                                                                                                             |
| [Verwenden von Direct3D 11-Featuredaten zur Ergänzung der Direct3D-Featureebenen](using-direct3d-optional-features-to-supplement-direct3d-feature-levels.md)<br/> | Hier erfahren Sie, wie Sie die Geräteunterstützung auf optionale Features überprüfen, einschließlich Features, die in neueren Versionen von Windows.<br/>                                                                                                           |



 

## <a name="how-to-topics-about-devices"></a>Themen zu Geräten



| Thema                                                                                                                                                                                                                                                                                                    | Beschreibung                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span id="How_To__Create_a_Reference_Device"></span><span id="how_to__create_a_reference_device"></span><span id="HOW_TO__CREATE_A_REFERENCE_DEVICE"></span>[How To: Erstellen eines Referenzgeräts](overviews-direct3d-11-devices-create-ref.md)<br/>                                                 | Beschreibt, wie ein Referenzgerät erstellt wird.<br/>                            |
| <span id="How_To__Create_a_WARP_Device"></span><span id="how_to__create_a_warp_device"></span><span id="HOW_TO__CREATE_A_WARP_DEVICE"></span>[How To: Erstellen eines WARP-Geräts](overviews-direct3d-11-devices-create-warp.md)<br/>                                                                    | Beschreibt das Erstellen eines WARP-Geräts.<br/>                                 |
| <span id="How_To__Create_a_Swap_Chain"></span><span id="how_to__create_a_swap_chain"></span><span id="HOW_TO__CREATE_A_SWAP_CHAIN"></span>[How To: Create a Swap Chain](overviews-direct3d-11-devices-create-swap-chain.md)<br/>                                                                  | Beschreibt, wie eine Swapkette erstellt wird.<br/>                                  |
| <span id="How_To__Enumerate_Adapters"></span><span id="how_to__enumerate_adapters"></span><span id="HOW_TO__ENUMERATE_ADAPTERS"></span>[How To: Enumerate Adapters](overviews-direct3d-11-devices-enum.md)<br/>                                                                                   | Beschreibt, wie die physischen Anzeigeadapter aufzählt werden.<br/>              |
| <span id="How_To__Get_Adapter_Display_Modes"></span><span id="how_to__get_adapter_display_modes"></span><span id="HOW_TO__GET_ADAPTER_DISPLAY_MODES"></span>[How To: Get Adapter Display Modes](overviews-direct3d-11-devices-get-adapter-info.md)<br/>                                           | Beschreibt, wie sie die unterstützten Anzeigefunktionen eines Adapters erhalten.<br/> |
| <span id="How_To__Create_a_Device_and_Immediate_Context"></span><span id="how_to__create_a_device_and_immediate_context"></span><span id="HOW_TO__CREATE_A_DEVICE_AND_IMMEDIATE_CONTEXT"></span>[How To: Erstellen eines Geräts und sofortigen Kontexts](overviews-direct3d-11-devices-initialize.md)<br/> | Beschreibt, wie ein Gerät initialisiert wird.<br/>                                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieranleitung für Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

 





