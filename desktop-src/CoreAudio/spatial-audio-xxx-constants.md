---
description: Die \_ \_ Konstanten für räumliche Audio xxx definieren Werte, die sich auf räumliche Audiofunktionen beziehen.
ms.assetid: F1A01BDB-0CC2-45ED-A423-8CC7F54D4E55
title: SPATIAL_AUDIO_XXX Konstanten (spatialaudiometadata. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd2c92b970f69cf84e0744f21a41932a8851efed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360974"
---
# <a name="spatial_audio_xxx-constants"></a>Räumliche \_ Audiodateien \_ xxx-Konstanten

Die \_ \_ Konstanten für räumliche Audio xxx definieren Werte, die sich auf räumliche Audiofunktionen beziehen.



| Konstante/Wert                                                                                                                                                                                                                                                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPATIAL_AUDIO_POSITION"></span><span id="spatial_audio_position"></span><dl> <dt>**Räumlich \_ \_AudioPosition**</dt> <dt>200</dt> </dl>                                                   | Ein von Microsoft definierter standardmäßiger audiometadatenbefehl, der die listenerposition im Standardmodell darstellt, das von [**ispatialaudioclient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) verwendet wird, wobei der Listener an der Position an Koordinaten (0, 0, 0) liegt und in Meter definiert ist.<br/> |
| <span id="SPATIAL_AUDIO_POSITION_BYTE_COUNT"></span><span id="spatial_audio_position_byte_count"></span><dl> <dt>**Räumlich \_ \_ \_ Byte \_ Anzahl der AudioPosition**</dt> <dt>sizeof (float) \* 3</dt> </dl> | Gibt die Größe des Werts **der \_ räumlichen \_ AudioPosition** an.<br/>                                                                                                                                                                                                        |
| <span id="SPATIAL_AUDIO_STANDARD_COMMANDS_START"></span><span id="spatial_audio_standard_commands_start"></span><dl> <dt>**Räumlich \_ \_ \_ Audiostandardbefehle \_ starten**</dt> <dt>200</dt> </dl>    | Gibt den Anfang des Bereichs der von Microsoft reservierten räumlichen audiometadatenbefehle an. Benutzerdefinierte metadatenbefehle sind auf Befehls-IDs 0-199 beschränkt. Die Befehle 200-255 sind für die Verwendung durch Microsoft reserviert.<br/>                                                           |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Spatialaudiometadata. h</dt> </dl> |



 

 




