---
title: Direct3D 11 auf Downlevelhardware
description: In diesem Abschnitt wird erläutert, wie Direct3D 11 für die Unterstützung neuer und vorhandener Hardware von DirectX 9 bis DirectX 11 konzipiert ist.
ms.assetid: 9a1ca4ff-df3d-46e5-8895-37199523343e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb9dde5bfaa32808752206ebe96702aaaf10cc39c1e053675ddfced765331be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045508"
---
# <a name="direct3d-11-on-downlevel-hardware"></a>Direct3D 11 auf Downlevelhardware

In diesem Abschnitt wird erläutert, wie Direct3D 11 für die Unterstützung neuer und vorhandener Hardware von DirectX 9 bis DirectX 11 konzipiert ist.

Dieses Diagramm zeigt, wie Direct3D 11 neue und vorhandene Hardware unterstützt.

![Diagramm der Hardware, die direct3d 11 unterstützt](images/d3d11-on-downlevel-hardware.png)

Mit Direct3D 11 wird ein neues Paradigma eingeführt, das als Featureebenen bezeichnet wird. Eine Featureebene ist ein klar definierter Satz von GPU-Funktionen. Mithilfe einer Funktionsebene können Sie eine Direct3D-Anwendung als Ziel für die Ausführung auf einer downlevel-Version der Direct3D-Hardware verwenden.

Im [Abschnitt Referenz zu 10Level9](d3d11-graphics-reference-10level9.md) werden die Unterschiede zwischen dem Verhalten verschiedener [**ID3D11Device-**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) und [**ID3D11DeviceContext-Methoden**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) auf verschiedenen 10Level9-Featureebenen aufgeführt.


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                  | Beschreibung                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Direct3D-Featureebenen](overviews-direct3d-11-devices-downlevel-intro.md)<br/>                                | In diesem Thema werden Direct3D-Featureebenen erläutert.<br/>                                                                                                                       |
| [Ausnahmen](overviews-direct3d-11-devices-downlevel-exceptions.md)<br/>                                        | In diesem Thema werden Ausnahmen bei der Verwendung von Direct3D 11 auf hardware downlevelr Hardware beschrieben. <br/>                                                                                      |
| [Berechnen von Shadern auf hardware downlevelr Hardware](overviews-direct3d-11-devices-downlevel-compute-shaders.md)<br/>        | In diesem Thema wird [](direct3d-11-advanced-stages-compute-shader.md) erläutert, wie Compute-Shader in einer Direct3D 11-App auf Direct3D 10-Hardware verwendet werden.<br/>             |
| [Verhindern unerwünschter SRVs für NULL-Pixel-Shader](overviews-direct3d-11-devices-downlevel-prevent-null-srvs.md)<br/> | In diesem Thema wird erläutert, wie Der Treiber, der NULL-Shaderressourcenansichten (SRVs) empfängt, umgangen wird, selbst wenn SRVs ohne **NULL** an die Pixelschattenstufe gebunden sind. <br/> |



 

## <a name="how-to-topics-about-feature-levels"></a>Themen zu Featureebenen



| Thema                                                                                                                                                                                                                                                                   | Beschreibung                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="How_To__Get_the_Device_Feature_Level"></span><span id="how_to__get_the_device_feature_level"></span><span id="HOW_TO__GET_THE_DEVICE_FEATURE_LEVEL"></span>[How To: Get the Device Feature Level](overviews-direct3d-11-devices-downlevel-get.md)<br/> | Hier erfahren Sie, wie Sie eine Funktionsebene erhalten.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geräte](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 





