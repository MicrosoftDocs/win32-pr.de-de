---
description: Gibt den &\# 0034; Leaky Bucket&\# 0034; Parameter für einen Stream in einer ASF-Medien Senke an.
ms.assetid: b01e59b6-0a7f-4125-867c-532385a27c15
title: MFPKEY_ASFSTREAMSINK_CORRECTED_LEAKYBUCKET-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a4ebc2dc41a1f43906aff5d2fe8caea8d53057
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862955"
---
# <a name="mfpkey_asfstreamsink_corrected_leakybucket-property"></a>Mfpkey \_ asfstreamsink \_ korrigiert \_ leakybucket-Eigenschaft

Gibt die Parameter für den "Leaky Bucket" (siehe Hinweise) für einen Datenstrom in einer ASF-Medien Senke an.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

Array von **DWORD** -Werten (**CAUL**)

VT \_ Vector \| VT \_ UI4

**CAUL**



## <a name="remarks"></a>Bemerkungen

Eine Anwendung kann diese Eigenschaft für einen Datenstrom der ASF-Medien Senke festlegen, nachdem der Medientyp für den Stream ausgehandelt wurde. Verwenden Sie diese Eigenschaft, um das tatsächliche Puffer Fenster anzugeben, das der Windows Media-Codec verwenden wird. Sie können diese Informationen vom Codec abrufen, indem Sie die **iwmcodecleakybucket** -Schnittstelle verwenden, die im Windows Media-Format-SDK dokumentiert ist.

Der Wert dieser Eigenschaft ist ein Array von drei **DWORD** -Werten in der folgenden Reihenfolge:

-   Bitrate in Bits pro Sekunde.
-   Puffergröße in Bytes.
-   Anfängliche Puffer Füllgröße in Byte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMF-Senke**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)
</dt> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




