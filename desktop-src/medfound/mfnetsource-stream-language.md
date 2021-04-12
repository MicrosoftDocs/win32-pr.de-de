---
description: Speichert die Zeichenfolge, die im Accept-Language-Header gesendet wird.
ms.assetid: b6ac613c-099b-4415-84ad-c0f8ad5f667b
title: MFNETSOURCE_STREAM_LANGUAGE-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 200c49d4a14146277c66fbb3389cf1ba6ab13fef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393254"
---
# <a name="mfnetsource_stream_language-property"></a>MF-Quelldaten \_ Strom ( \_ sprach Eigenschaft)

Speichert die Zeichenfolge, die im Accept-Language-Header gesendet wird.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**WCHAR \** _

VT \_ LPWSTR

_ *pwszval**



## <a name="remarks"></a>Bemerkungen

Die MF-Quell \_ Datenstrom- \_ sprach Konstante definiert die GUID für den Eigenschafts Schlüssel. Der Eigenschaften Bezeichner (PID) ist 0 (null). Um diese Eigenschaft für die Netzwerkquelle festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




