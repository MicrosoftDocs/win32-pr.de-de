---
description: Diese Eigenschaft sendet einen Befehl an das Gerät, um nach einer absoluten Tracknummer (ATN) zu suchen. Der UVC-Gerätetreiber unterstützt diese Eigenschaft.
ms.assetid: 209e0aa3-d7a3-4b5c-ae5a-5063a3804a9d
title: KSPROPERTY_EXTXPORT_ATN_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4115c7ff1c4bc878b4ee80e284f11821c37909a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909447"
---
# <a name="ksproperty_extxport_atn_search"></a>KSPROPERTY \_ EXTXPORT \_ ATN \_ SEARCH

Diese Eigenschaft sendet einen Befehl an das Gerät, um nach einer absoluten Tracknummer (ATN) zu suchen. Der UVC-Gerätetreiber unterstützt diese Eigenschaft.



| Bezeichnung | Wert |
|-------------------|---------------------------------------|
| Eigenschaftensatz-GUID | PROPSETID \_ \_ EXT-TRANSPORT             |
| Eigenschafts-ID       | KSPROPERTY \_ EXTXPORT \_ ATN \_ SEARCH     |
| Datentyp         | **KSPROPERTY \_ EXTXPORT \_ S-Struktur** |



 

## <a name="remarks"></a>Bemerkungen

Legen Sie **das dwAbsTrackNumber-Member** der **KSPROPERTY \_ EXTXPORT \_ S-Struktur** auf den folgenden Wert fest:


```
(absolute track number << 1) + continuity bit
```



Die UVC-Spezifikation definiert nicht, wie das Gerät das Kontinuitätsbit verwendet. Die **KSPROPERTY \_ EXTXPORT \_ S-Struktur** wird im Windows-DDK beschrieben.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Transporteigenschaftssatz für externe Geräte](external-device-transport-property-set.md)
</dt> </dl>

 

 



