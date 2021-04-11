---
description: Gibt die Portnummer des Proxy Servers an.
ms.assetid: cd84911b-3658-489f-b454-23eded0cbfa0
title: MFNETSOURCE_PROXYPORT-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 228f7d9390d53f7d8182a198879dcb2d81e3bae7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215134"
---
# <a name="mfnetsource_proxyport-property"></a>MF NetSource- \_ ProxyPort (Eigenschaft)

Gibt die Portnummer des Proxy Servers an.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**DWORD** (als **Long** gespeichert)

VT \_ I4

**LVAL**



## <a name="remarks"></a>Bemerkungen

Die Konstante **MF-Quelle \_ ProxyPort** definiert die GUID für diesen Eigenschafts Schlüssel. Der Eigenschaften Bezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um den proxylocator bei der Erstellung des proxylocator-Objekts zu konfigurieren. Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger im *pproxyconfig* -Parameter der [**mfkreateproxylocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) -Funktion. Wenn diese Eigenschaft nicht für http festgelegt ist, verwendet der proxylocator standardmäßig den Wert 80.

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

 

 




