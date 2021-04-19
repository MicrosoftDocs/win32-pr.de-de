---
title: Enumerationen der Debugschicht
description: Die folgenden Enumerationen werden in d3d12sdklayers. h deklariert.
ms.assetid: 6E76C857-128E-4F0E-9711-72C4CF6C835C
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746c0def35c8eb282264cb4ab0b40eb5c08f0f9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339831"
---
# <a name="debug-layer-enumerations"></a>Enumerationen der Debugschicht

Die folgenden Enumerationen werden in d3d12sdklayers. h deklariert.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3D12 \_ Debug- \_ Befehls \_ Listen- \_ \_ Parametertyp**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_command_list_parameter_type)<br/>                                 | Gibt den Debug-Parametertyp an, der von [**ID3D12DebugCommandList1:: setdebugparameter**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugcommandlist1-setdebugparameter) und [**ID3D12DebugCommandList1:: getdebugparameter**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugcommandlist1-getdebugparameter)verwendet wird.<br/>                                                                                                                                                                                                      |
| [**D3D12 \_ Debug \_ - \_ Geräte \_ Parametertyp**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type)<br/>                                              | Gibt den Datentyp des Speichers an, auf den durch den *pData* -Parameter von [**ID3D12DebugDevice1:: setdebugparameter**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter) und [**ID3D12DebugDevice1:: getdebugparameter**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-getdebugparameter)verwiesen wird.<br/>                                                                                                                                                                                        |
| [**D3D12 \_ Debug- \_ Feature**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_feature)<br/>                                                                            | Flags für optionale Funktionen der D3D12-Debugebene.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**D3D12 \_ GPU- \_ basierte \_ Validierungsflags \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_flags)<br/>                                                | Beschreibt die Ebene der GPU-basierten Validierung, die zur Laufzeit durchgeführt werden soll.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| [**D3D12 \_ GPU- \_ basierter \_ Validierungs \_ Pipeline \_ Status \_ Create \_ Flags**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_pipeline_state_create_flags)<br/> | Gibt an, wie GPU-Based-Überprüfung gepatchte Pipeline Zustände während [**ID3D12Device:: deategraphicspipelinestate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) und [**ID3D12Device:: anatecomputepipelinestate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate)behandelt.<br/>                                                                                                                                                                             |
| [**D3D12 \_ GPU- \_ basierter \_ Validierungs- \_ Shader- \_ \_ patchmodus**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_shader_patch_mode)<br/>                      | Gibt den Typ der shaderpatching an, die von GPU-Based Validierung auf der Geräte-oder Befehlslisten Ebene verwendet wird.<br/>                                                                                                                                                                                                                                                                                                                                       |
| [**D3D12- \_ Nachrichten \_ Kategorie**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_category)<br/>                                                                      | Gibt Kategorien von Debugmeldungen an. Dadurch wird die Kategorie einer Nachricht identifiziert, wenn eine Nachricht mit [**ID3D12InfoQueue:: getMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getmessage) abgerufen und eine Nachricht mit [**ID3D12InfoQueue:: addMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-addmessage)hinzugefügt wird. Beim Erstellen eines Informations Warteschlangen Filters können diese Werte verwendet werden, um nach Kategorien von Nachrichten zuzulassen oder zu verweigern, die die Speicher-und Abruf Filter passieren. <br/> |
| [**D3D12 nach \_ richten- \_ ID**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_id)<br/>                                                                                  | Gibt debugmeldungs-IDs zum Einrichten eines Informations Warteschlangen Filters an (siehe [**D3D12 \_ Info \_ Queue \_ Filter**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter)). verwenden Sie diese Meldungen, um Nachrichten Kategorien zuzulassen oder zu verweigern, die die Speicher-und Abruf Filter passieren. Diese IDs werden von Methoden wie [**ID3D12InfoQueue:: getMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getmessage) oder [**ID3D12InfoQueue:: addMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-addmessage)verwendet. <br/>                        |
| [**D3D12- \_ Nachrichten \_ Schweregrad**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_severity)<br/>                                                                      | Debugnachrichten Schweregrade für eine Informations Warteschlange.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| [**D3D12- \_ rldo- \_ Flags**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_rldo_flags)<br/>                                                                                  | Gibt Optionen für die Menge der Informationen an, die über die Lebensdauer eines Live-Geräte Objekts berichtet werden. <br/>                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einrichtung der Direct3D 12-Programmierungsumgebung](directx-12-programming-environment-set-up.md)
</dt> <dt>

[Referenz der Debugschicht](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[Referenz für Direct3D 12](direct3d-12-reference.md)
</dt> </dl>

 

 





