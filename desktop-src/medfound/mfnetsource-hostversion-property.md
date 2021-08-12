---
description: Der Wert des felds \# &0034;c-hostexever&0034;, das die Netzwerkquelle für \# die Protokollierung verwendet.
ms.assetid: eee93457-483d-41dc-91c5-c12382d03152
title: MFNETSOURCE_HOSTVERSION -Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5f78a277de4fc5b0609be31f21f684357806dbb8609657a930cdc4816b1e43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243460"
---
# <a name="mfnetsource_hostversion-property"></a>MFNETSOURCE \_ HOSTVERSION(Eigenschaft)

Der Wert des Felds "c-hostexever", das die Netzwerkquelle für die Protokollierung verwendet. Anwendungen können diese Eigenschaft auf die Versionsnummer der Hostanwendung festlegen. Die Hostanwendung ist die .exe, die durch das Feld c-hostexe identifiziert wird.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

**LONGLONG**

VT \_ I8

**hVal**



## <a name="remarks"></a>Hinweise

Die Konstante **MFNETSOURCE \_ HOSTVERSION** definiert die GUID für diesen Eigenschaftsschlüssel. Der Eigenschaftenbezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren. Übergeben Sie zum Festlegen der -Eigenschaft einen **IPropertyStore-Zeiger** an den Quellre resolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle.](configuring-a-media-source.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Clientprotokollierung](client-logging.md)
</dt> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




