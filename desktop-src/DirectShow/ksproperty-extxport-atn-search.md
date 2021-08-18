---
description: Diese Eigenschaft sendet einen Befehl an das Gerät, um nach einer absoluten Tracknummer (ATN) zu suchen. Der UVC-Gerätetreiber unterstützt diese Eigenschaft.
ms.assetid: 209e0aa3-d7a3-4b5c-ae5a-5063a3804a9d
title: KSPROPERTY_EXTXPORT_ATN_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61d35c1fce1e958aa475cc0344c2db320daa806326a49d0d6e939bf4ea86d49f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823270"
---
# <a name="ksproperty_extxport_atn_search"></a>KSPROPERTY \_ EXTXPORT \_ ATN \_ SEARCH

Diese Eigenschaft sendet einen Befehl an das Gerät, um nach einer absoluten Tracknummer (ATN) zu suchen. Der UVC-Gerätetreiber unterstützt diese Eigenschaft.



| Bezeichnung | Wert |
|-------------------|---------------------------------------|
| Eigenschaftensatz-GUID | PROPSETID \_ EXT \_ TRANSPORT             |
| Eigenschafts-ID       | KSPROPERTY \_ EXTXPORT \_ ATN \_ SEARCH     |
| Datentyp         | **KSPROPERTY \_ EXTXPORT \_ S-Struktur** |



 

## <a name="remarks"></a>Hinweise

Legen Sie den **dwAbsTrackNumber-Member** der **KSPROPERTY \_ EXTXPORT \_ S-Struktur** auf den folgenden Wert fest:


```
(absolute track number << 1) + continuity bit
```



Die UVC-Spezifikation definiert nicht, wie das Gerät das Continuity Bit verwendet. Die **KSPROPERTY \_ EXTXPORT \_ S-Struktur** wird im Windows DDK beschrieben.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Eigenschaftensatz für den Transport externer Geräte](external-device-transport-property-set.md)
</dt> </dl>

 

 



