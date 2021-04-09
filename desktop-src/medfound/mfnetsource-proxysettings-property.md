---
description: Gibt die Konfigurationseinstellung für den standardproxylocator an.
ms.assetid: 85f2bd02-8a2f-46b5-b765-1a0bc5b6ccc3
title: MFNETSOURCE_PROXYSETTINGS-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1330773ab33674e58ef07b95a53c4493e6e6f6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130709"
---
# <a name="mfnetsource_proxysettings-property"></a>MF NetSource- \_ proxysettings-Eigenschaft

Gibt die Konfigurationseinstellung für den standardproxylocator an. Der Wert dieser Eigenschaft ist ein Member der [**mfnet \_ proxysettings**](/windows/desktop/api/mfidl/ne-mfidl-mfnet_proxysettings) -Enumeration.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**LONG**

VT \_ I4

**LVAL**



## <a name="remarks"></a>Bemerkungen

Die Konstante " **MF NetSource"- \_ Proxy Settings** definiert die GUID für diesen Eigenschafts Schlüssel. Der Eigenschaften Bezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um den proxylocator bei der Erstellung des standardproxylocator-Objekts zu konfigurieren. Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger im *pproxyconfig* -Parameter der [**mfkreateproxylocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) -Funktion.

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
</dt> <dt>

[Proxy Unterstützung für Netzwerk Quellen](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




