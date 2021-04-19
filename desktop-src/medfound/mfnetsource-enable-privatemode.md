---
description: Aktiviert den privaten Download Modus in der Netzwerkquelle.
ms.assetid: 679661A7-1D31-43F3-A64E-16ADCB5414B0
title: MFNETSOURCE_ENABLE_PRIVATEMODE-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53aa0bde3bf76ded278e0e3ee37465adb717972a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348232"
---
# <a name="mfnetsource_enable_privatemode-property"></a>MF NetSource \_ - \_ Eigenschaft ' privatemode ' aktivieren

Aktiviert den privaten Download Modus in der Netzwerkquelle.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**BOOL**

VT \_ I4

**LVAL**



## <a name="remarks"></a>Bemerkungen

Wenn diese Eigenschaft den Wert **true** hat, wird der Cache gelöscht, wenn die Sitzung beendet wird.

Die **MF NetSource- \_ clientguid** -Konstante definiert die GUID für den Eigenschafts Schlüssel. Der Eigenschaften Bezeichner (PID) ist 0 (null). Um diese Eigenschaft für die Netzwerkquelle festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                          |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




