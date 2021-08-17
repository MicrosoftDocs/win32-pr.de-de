---
description: Gibt die Energiesparstufe eines Videodecoders an.
ms.assetid: 7e2ff8be-b21f-4833-a165-0112d4220677
title: AVDecVideoSWPowerLevel-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7c362e066a16e333cda402704a720b5e1b0b8534f1b56536d32009e6fa29663
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824220"
---
# <a name="avdecvideoswpowerlevel-property"></a>AVDecVideoSWPowerLevel-Eigenschaft

Gibt die Energiesparstufe eines Videodecoders an.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVDecVideoSWPowerLevel**

## <a name="property-value"></a>Eigenschaftswert

Der Bereich der möglichen Werte ist \[ 0..100 \] , einschließlich, mit der folgenden Bedeutung.



| Wert | Beschreibung                 |
|-------|-----------------------------|
| 0     | Optimieren Sie die Akkulaufzeit.  |
| 100   | Optimieren Sie die Videoqualität. |



 

Die [**eAVDecVideoSWPowerLevel-Enumeration**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel) definiert einige bestimmte Konstanten innerhalb dieses Bereichs.

## <a name="remarks"></a>Hinweise

Sie können diese Eigenschaft während der Wiedergabe festlegen, um die Energiesparstufe zu ändern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop-Apps \| UWP-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 \[ Server-Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Codec-API-Eigenschaften](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




