---
description: Gibt die von der Netzwerkquelle erkannte Paket paar Bandbreite und Lauf Zeit Bandbreite an.
ms.assetid: 430de7fc-fe62-4b89-b3fc-7cd956e40892
title: MFNETSOURCE_PPBANDWIDTH-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae0f23f289f68e46bba726a4391023ce9001e2ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347053"
---
# <a name="mfnetsource_ppbandwidth-property"></a>Eigenschaft "MF NetSource \_ ppbandwidth"

Gibt die von der Netzwerkquelle erkannte Paket paar Bandbreite und Lauf Zeit Bandbreite an. Der Eigenschafts Wert ist ein Array mit zwei Werten:

-   Paket paar Bandbreite in Bits pro Sekunde.
-   Lauf Zeit Bandbreite in Bits pro Sekunde.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

Array von **ulong** -Werten (**CAUL**)

VT \_ Vector \| VT \_ UI4

**CAUL**



## <a name="remarks"></a>Bemerkungen

Die Konstante " **MF NetSource \_ ppbandwidth** " definiert die GUID für diesen Eigenschafts Schlüssel. Der Eigenschaften Bezeichner (PID) ist 0 (null).

Diese Eigenschaft ist schreibgeschützt. Um diese Eigenschaft abzurufen, Fragen Sie die Netzwerkquelle nach der **IPropertyStore** -Schnittstelle ab, und rufen Sie **IPropertyStore:: GetValue** auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Netzwerk Quell Features](network-source-features.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




