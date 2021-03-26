---
title: Direct3D 11 auf downlevelhardware
description: In diesem Abschnitt wird erläutert, wie Direct3D 11 für die Unterstützung neuer und vorhandener Hardware (von DirectX 9 bis DirectX 11) konzipiert ist.
ms.assetid: 9a1ca4ff-df3d-46e5-8895-37199523343e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f730a43db803e1e5198794167d0078a5b2896f6c
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104568430"
---
# <a name="direct3d-11-on-downlevel-hardware"></a>Direct3D 11 auf downlevelhardware

In diesem Abschnitt wird erläutert, wie Direct3D 11 für die Unterstützung neuer und vorhandener Hardware (von DirectX 9 bis DirectX 11) konzipiert ist.

Dieses Diagramm zeigt, wie Direct3D 11 neue und vorhandene Hardware unterstützt.

![Diagramm der Hardware, die von Direct3D 11 unterstützt wird](images/d3d11-on-downlevel-hardware.png)

Mit Direct3D 11 wird ein neues Paradigma namens Funktionsebenen eingeführt. Eine Featureebene ist ein gut definierter Satz von GPU-Funktionen. Mithilfe einer Featureebene können Sie eine Direct3D-Anwendung auf eine downlevelversion von Direct3D-Hardware anwenden.

Der [Verweis Bereich 10level9](d3d11-graphics-reference-10level9.md) listet die Unterschiede zwischen der Art und Weise, wie sich verschiedene [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) -und [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Methoden auf verschiedenen 10 Level9-featureebenen


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                  | BESCHREIBUNG                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Direct3D-Featureebenen](overviews-direct3d-11-devices-downlevel-intro.md)<br/>                                | In diesem Thema werden Direct3D Funktionsebenen erläutert.<br/>                                                                                                                       |
| [Ausnahmen](overviews-direct3d-11-devices-downlevel-exceptions.md)<br/>                                        | In diesem Thema werden Ausnahmen bei der Verwendung von Direct3D 11 auf downlevelhardware beschrieben. <br/>                                                                                      |
| [Compute-Shader auf downlevelhardware](overviews-direct3d-11-devices-downlevel-compute-shaders.md)<br/>        | In diesem Thema wird die Verwendung von [Compute-Shadern](direct3d-11-advanced-stages-compute-shader.md) in einer Direct3D 11-App auf Direct3D 10-Hardware erläutert.<br/>             |
| [Verhindern unerwünschter NULL-Pixel-Shader-Srvs](overviews-direct3d-11-devices-downlevel-prevent-null-srvs.md)<br/> | In diesem Thema wird erläutert, wie Sie den Treiber umgehen, der **null** -Shader-Ressourcen Sichten (Srvs) empfängt, auch wenn nicht-**null** -Srvs an die Pixel-Shader-Phase gebunden sind.<br/> |



 

## <a name="how-to-topics-about-feature-levels"></a>Themen zur Vorgehensweise bei Funktionsebenen



| Thema                                                                                                                                                                                                                                                                   | BESCHREIBUNG                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="How_To__Get_the_Device_Feature_Level"></span><span id="how_to__get_the_device_feature_level"></span><span id="HOW_TO__GET_THE_DEVICE_FEATURE_LEVEL"></span>[Gewusst wie: erhalten der Geräte Funktionsebene](overviews-direct3d-11-devices-downlevel-get.md)<br/> | Erfahren Sie, wie Sie eine Featureebene erhalten.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geräte](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 





