---
description: Gibt die maximale Anzahl dynamischer Audioobjekte an, die vom audioendpunkt simuliert werden können.
ms.assetid: 6B6D73C1-C2E6-4C23-BBAD-7B51E8441C71
title: MF_MT_SPATIAL_AUDIO_MAX_DYNAMIC_OBJECTS-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358045079fb9cf52ad1fd0c8969f54723c7f02d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349884"
---
# <a name="mf_mt_spatial_audio_max_dynamic_objects-attribute"></a>Das \_ MF \_ MT \_ - \_ Attribut für räumliche \_ \_ Objekte mit räumlichen Daten

Gibt die maximale Anzahl dynamischer Audioobjekte an, die vom audioendpunkt simuliert werden können.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Ein [**imsspatialaudiosample**](/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample) -Wert kann weniger Stichproben enthalten als die Zahl, die von diesem Attribut angegeben wird. Wenn ein Beispiel mehr Audioobjekte enthält, als durch dieses Attribut angegeben sind, ist das Verhalten nicht definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1703, \[ nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                          |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




