---
description: Gibt an, ob der Datenstrom Wechsel in der Netzwerkquelle aktiviert ist.
ms.assetid: 691a3549-eaf8-4e3d-ad0e-e5b013658f78
title: MFNETSOURCE_THINNINGENABLED-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9d5b1b362f8776e80e3d12b591dbf2116217846
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958647"
---
# <a name="mfnetsource_thinningenabled-property"></a>MF-Quelle \_ thinningenabled (Eigenschaft)

Gibt an, ob der Datenstrom Wechsel in der Netzwerkquelle aktiviert ist. Der Datenstrom Wechsel ermöglicht es dem Medienserver, Datenströme in einer MBR-Datei (Multiple Bitrate) basierend auf der verfügbaren Bandbreite zu ändern.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

Boolescher Wert (**Long**)

VT \_ I4

**LVAL**



## <a name="remarks"></a>Bemerkungen

Die Konstante **MF-Quelle \_ thinningenabled** definiert die GUID für diesen Eigenschafts Schlüssel. Der Eigenschaften Bezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren. Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).

Der Standardwert dieser Eigenschaft ist **true**.

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

 

 




