---
description: Liste der URLs, an die die Netzwerkquelle Protokollierungs Informationen sendet.
ms.assetid: 772c5b57-273d-4289-9229-ef7a199c6473
title: MFNETSOURCE_LOGURL-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6956a7deb251ee9a25261a1b6c6a723973f7a03b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129781"
---
# <a name="mfnetsource_logurl-property"></a>MF NetSource- \_ LogURL (Eigenschaft)

Liste der URLs, an die die Netzwerkquelle Protokollierungs Informationen sendet.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

Array von Zeichen folgen mit breit Zeichen (**calpwstr**)

VT \_ Vector \| VT \_ LPWSTR

**calpwstr**



## <a name="remarks"></a>Bemerkungen

Die Konstante " **MF NetSource \_ LogURL** " definiert die GUID für diesen Eigenschafts Schlüssel. Der Eigenschaften Bezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren. Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).

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

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




