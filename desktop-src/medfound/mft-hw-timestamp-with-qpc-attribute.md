---
description: Gibt an, ob eine Hardware Geräte Quelle die Systemzeit für Zeitstempel verwendet.
ms.assetid: 54cdfa13-955a-4e92-b337-f645d526a1b8
title: MFT_HW_TIMESTAMP_WITH_QPC_Attribute-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94f6f7d50db89e99e76e7b7ea509f444c3998bb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348905"
---
# <a name="mft_hw_timestamp_with_qpc_attribute-attribute"></a>MFT- \_ HW- \_ Zeitstempel \_ mit \_ QPC- \_ Attribut Attribut

Gibt an, ob eine Hardware Geräte Quelle die Systemzeit für Zeitstempel verwendet.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Bemerkungen

Wenn dieses Attribut auf **true** festgelegt ist, verwendet die Geräte Quelle die von **QueryPerformanceCounter** zurückgegebene Systemzeit für Zeitstempel. Andernfalls verwendet die Geräte Quelle die Uhr des Geräts. Der Standardwert ist **FALSE**.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>"MF Transform. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Geräte Attribute erfassen](capture-device-attributes.md)
</dt> </dl>

 

 




