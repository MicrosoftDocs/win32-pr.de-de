---
description: Diese Eigenschaft sendet einen Befehl an das Gerät, um nach einem angegebenen Zeitcode zu suchen. Der UVC-Gerätetreiber unterstützt diese Eigenschaft.
ms.assetid: 0502d59a-0a9e-4192-af9f-1553cd13a69c
title: KSPROPERTY_EXTXPORT_TIMECODE_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f49b8e71d664cf266428d33c99b87859765623ca8205843bbfee108da5f7d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153188"
---
# <a name="ksproperty_extxport_timecode_search"></a>KSPROPERTY \_ EXTXPORT \_ TIMECODE \_ SEARCH

Diese Eigenschaft sendet einen Befehl an das Gerät, um nach einem angegebenen Zeitcode zu suchen. Der UVC-Gerätetreiber unterstützt diese Eigenschaft.



| Bezeichnung | Wert |
|-------------------|----------------------------------------|
| Eigenschaftensatz-GUID | PROPSETID \_ EXT \_ TRANSPORT              |
| Eigenschafts-ID       | KSPROPERTY \_ EXTXPORT \_ TIMECODE \_ SEARCH |
| Datentyp         | **KSPROPERTY \_ EXTXPORT \_ S-Struktur**  |



 

## <a name="remarks"></a>Hinweise

Füllen Sie den **Timecodemember** der **KSPROPERTY \_ EXTXPORT \_ S-Struktur** mit dem gewünschten Frame, der sekunde, der Minute und der Stunde aus. Die **KSPROPERTY \_ EXTXPORT \_ S-Struktur** wird im Windows DDK beschrieben.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaftensatz für den Transport externer Geräte](external-device-transport-property-set.md)
</dt> </dl>

 

 



