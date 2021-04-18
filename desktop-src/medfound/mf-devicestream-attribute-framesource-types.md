---
description: Stellt den Rahmen Quelltyp dar.
ms.assetid: 4A2B427E-E654-48BA-8BF4-16F1B1F8D266
title: MF_DEVICESTREAM_ATTRIBUTE_FRAMESOURCE_TYPES-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8823a828a81290fe3b039c8959d694c62331622f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357452"
---
# <a name="mf_devicestream_attribute_framesource_types-attribute"></a>Attribut für das MF- \_ \_ Attribut " \_ framesource" \_

Stellt den Rahmen Quelltyp dar.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Dieser Wert dieses Attributs muss eine Bitmaske von einem oder mehreren Werten aus der Enumeration " [**mfframesourcetypes**](/windows/desktop/api/mfapi/ne-mfapi-mfframesourcetypes) " sein. Wenn dieses Attribut nicht für einen Medientyp definiert ist, wird angenommen, dass es den Wert **mfframesourcetypes:: Color** hat, um die Abwärtskompatibilität zu unterstützen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1607, \[ nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




