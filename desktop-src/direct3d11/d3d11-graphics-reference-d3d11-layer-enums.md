---
title: Ebenenenumerationen
description: Dieser Abschnitt enthält Informationen zu ebenenenumerationen.
ms.assetid: 0fd0456b-2638-4b4c-8a34-a3e104a1a034
keywords:
- Enumerationen, Direct3D 11-Ebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e1cca3fa500a529930c8d0c39005697045d18b
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104976920"
---
# <a name="layer-enumerations"></a>Ebenenenumerationen

Dieser Abschnitt enthält Informationen zu ebenenenumerationen.


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3D11- \_ Nachrichten \_ Kategorie**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_category)<br/>                             | Kategorien von Debugmeldungen. Dadurch wird die Kategorie einer Nachricht identifiziert, wenn eine Nachricht mit [**ID3D11InfoQueue:: getMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) abgerufen und eine Nachricht mit [**ID3D11InfoQueue:: addMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage)hinzugefügt wird. Beim Erstellen eines [**Informations Warteschlangen Filters**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)können diese Werte verwendet werden, um nach Kategorien von Nachrichten zuzulassen oder zu verweigern, die die Speicher-und Abruf Filter passieren.<br/> |
| [**D3D11 nach \_ richten- \_ ID**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_id)<br/>                                         | Debugmeldungen zum Einrichten eines Informations Warteschlangen Filters (siehe [**D3D11 \_ Info \_ Queue \_ Filter**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)); verwenden Sie diese Meldungen, um Nachrichten Kategorien zuzulassen oder zu verweigern, die die Speicher-und Abruf Filter passieren. Diese IDs werden von Methoden wie [**ID3D11InfoQueue:: getMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) oder [**ID3D11InfoQueue:: addMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage)verwendet. <br/>                                                             |
| [**D3D11- \_ Nachrichten \_ Schweregrad**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_severity)<br/>                             | Debugnachrichten Schweregrade für eine Informations Warteschlange.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**D3D11- \_ rldo- \_ Flags**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_rldo_flags)<br/>                                         | Optionen für die Menge der Informationen, die über die Lebensdauer eines Geräte Objekts berichtet werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| [**D3D11- \_ Shader- \_ Überwachungs \_ Optionen**](/windows/win32/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_shader_tracking_options)<br/>              | Optionen, die angeben, wie die Shader-Debugverfolgung durchgeführt wird<br/>                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**D3D11- \_ Shader-nach \_ Verfolgungs \_ \_ Ressourcentyp**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_shader_tracking_resource_type)<br/> | Gibt an, welche Ressourcentypen nachverfolgt werden sollen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ebenenverweis](d3d11-graphics-reference-d3d11-layer.md)
</dt> </dl>

 

 





