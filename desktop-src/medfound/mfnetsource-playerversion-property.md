---
description: Der Wert des Felds \# &0034;c-playerversion&0034;, das die Netzwerkquelle \# für die Protokollierung verwendet.
ms.assetid: 7bc485de-345b-475c-bbae-0776aa63c93a
title: MFNETSOURCE_PLAYERVERSION -Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71828db44eca7c4318dbdb11e7934871911b06dbc4547f83723a9944f139ae26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738969"
---
# <a name="mfnetsource_playerversion-property"></a>MFNETSOURCE \_ PLAYERVERSION(Eigenschaft)

Der Wert des Felds "c-playerversion", das die Netzwerkquelle für die Protokollierung verwendet. Anwendungen können diese Eigenschaft auf die Versionsnummer der Anwendung festlegen.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

**LONGLONG**

VT \_ I8

**hVal**



## <a name="remarks"></a>Hinweise

Die Konstante **MFNETSOURCE \_ PLAYERVERSION** definiert die GUID für diesen Eigenschaftsschlüssel. Der Eigenschaftenbezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren. Übergeben Sie zum Festlegen der -Eigenschaft einen **IPropertyStore-Zeiger** an den Quellre resolver. Weitere Informationen finden Sie unter [Quellre resolver](source-resolver.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientprotokollierung](client-logging.md)
</dt> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




