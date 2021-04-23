---
description: Diese Eigenschaft sendet einen Befehl an das Gerät, um nach einem angegebenen Zeitcode zu suchen. Der UVC-Gerätetreiber unterstützt diese Eigenschaft.
ms.assetid: 0502d59a-0a9e-4192-af9f-1553cd13a69c
title: KSPROPERTY_EXTXPORT_TIMECODE_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6852dc44e6ef10eebb59721f16a276ac5d4306a3
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909438"
---
# <a name="ksproperty_extxport_timecode_search"></a>KSPROPERTY \_ \_ EXTXPORT-ZEITCODESUCHE \_

Diese Eigenschaft sendet einen Befehl an das Gerät, um nach einem angegebenen Zeitcode zu suchen. Der UVC-Gerätetreiber unterstützt diese Eigenschaft.



| Bezeichnung | Wert |
|-------------------|----------------------------------------|
| Eigenschaftensatz-GUID | PROPSETID \_ \_ EXT-TRANSPORT              |
| Eigenschafts-ID       | KSPROPERTY \_ \_ EXTXPORT-ZEITCODESUCHE \_ |
| Datentyp         | **KSPROPERTY \_ EXTXPORT \_ S-Struktur**  |



 

## <a name="remarks"></a>Bemerkungen

Füllen Sie das **Timecode-Member** der **KSPROPERTY \_ EXTXPORT \_ S-Struktur** mit dem gewünschten Frame, der Sekunde, der Minute und der Stunde aus. Die **KSPROPERTY \_ EXTXPORT \_ S-Struktur** wird im Windows-DDK beschrieben.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Transporteigenschaftssatz für externe Geräte](external-device-transport-property-set.md)
</dt> </dl>

 

 



