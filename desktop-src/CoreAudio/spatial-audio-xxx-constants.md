---
description: Die SPATIAL \_ AUDIO \_ XXX-Konstanten definieren Werte im Zusammenhang mit räumlichen Soundfeatures.
ms.assetid: F1A01BDB-0CC2-45ED-A423-8CC7F54D4E55
title: SPATIAL_AUDIO_XXX Konstanten (SpatialAudioMetadata.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db363260b21f47676c12aeb5eaf3c10149b571ed2771a4d9f907e98b0ba17aed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018248"
---
# <a name="spatial_audio_xxx-constants"></a>SPATIAL \_ AUDIO \_ XXX-Konstanten

Die SPATIAL \_ AUDIO \_ XXX-Konstanten definieren Werte im Zusammenhang mit räumlichen Soundfeatures.



| Konstante/Wert                                                                                                                                                                                                                                                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPATIAL_AUDIO_POSITION"></span><span id="spatial_audio_position"></span><dl> <dt>**SPATIAL \_ \_AUDIOPOSITION**</dt> <dt>200</dt> </dl>                                                   | Ein von Microsoft definierter Standardbefehl für räumliche Audiometadaten, der die Listenerposition im von [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) verwendeten Standardmodell darstellt, wobei sich der Kopf des Listeners an Koordinaten (0,0,0) befindet, die in Metern definiert sind.<br/> |
| <span id="SPATIAL_AUDIO_POSITION_BYTE_COUNT"></span><span id="spatial_audio_position_byte_count"></span><dl> <dt>**SPATIAL \_ AUDIOPOSITION \_ \_ BYTE \_ COUNT sizeof(float)**</dt> <dt> \* 3</dt> </dl> | Gibt die Größe des SPATIAL **\_ AUDIO \_ POSITION-Werts** an.<br/>                                                                                                                                                                                                        |
| <span id="SPATIAL_AUDIO_STANDARD_COMMANDS_START"></span><span id="spatial_audio_standard_commands_start"></span><dl> <dt>**SPATIAL \_ AUDIO \_ \_ STANDARD-BEFEHLE \_ AB**</dt> <dt>200</dt> </dl>    | Gibt den Anfang des Bereichs der von Microsoft reservierten Befehle für räumliche Audiometadaten an. Benutzerdefinierte Metadatenbefehle sind auf die Befehls-IDs 0 bis 199 beschränkt. Die Befehle 200 bis 255 sind für die Verwendung durch Microsoft reserviert.<br/>                                                           |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>SpatialAudioMetadata.h</dt> </dl> |



 

 




