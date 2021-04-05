---
description: Gibt an, wie oft die Netzwerkquelle versucht, erneut eine Verbindung mit dem Server herzustellen und das Streaming fortzusetzen, wenn die Verbindung unterbrochen wird.
ms.assetid: 185e15c6-910b-4e27-9087-cfe30a174194
title: MFNETSOURCE_AUTORECONNECTLIMIT-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dac2a81cb4d47d8113059924877670458ac22ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753136"
---
# <a name="mfnetsource_autoreconnectlimit-property"></a>MF NetSource- \_ autoreconnectlimit (Eigenschaft)

Gibt an, wie oft die Netzwerkquelle versucht, erneut eine Verbindung mit dem Server herzustellen und das Streaming fortzusetzen, wenn die Verbindung unterbrochen wird.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**DWORD** (als **Long** gespeichert)

VT \_ I4

**LVAL**



## <a name="remarks"></a>Bemerkungen

Die Konstante " **MF NetSource \_ autoreconnectlimit** " definiert die GUID für diesen Eigenschafts Schlüssel. Der Eigenschaften Bezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren. Um die-Eigenschaft festzulegen, übergeben Sie ein **IPropertyStore** -Objekt an den quellresolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).

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

 

 




