---
description: Stellt den Framequelltyp dar.
ms.assetid: 4A2B427E-E654-48BA-8BF4-16F1B1F8D266
title: MF_DEVICESTREAM_ATTRIBUTE_FRAMESOURCE_TYPES-Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcce2e7f90f4e5f23e99bac8e532455fac1309cc0e20177c5800d85f4580e20a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013190"
---
# <a name="mf_devicestream_attribute_framesource_types-attribute"></a>MF \_ \_ DEVICESTREAM-ATTRIBUT \_ FRAMESOURCE \_ TYPES-Attribut

Stellt den Framequelltyp dar.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Dieser Wert dieses Attributs sollte eine Bitmaske eines oder mehrerer Werte aus der [**MFFrameSourceTypes-Enumeration**](/windows/desktop/api/mfapi/ne-mfapi-mfframesourcetypes) sein. Wenn dieses Attribut nicht für einen Medientyp definiert ist, wird davon ausgegangen, dass es den Wert **MFFrameSourceTypes::Color** hat, um die Abwärtskompatibilität zu unterstützen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1607 \[\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 




