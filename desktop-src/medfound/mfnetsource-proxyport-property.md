---
description: Gibt die Portnummer des Proxyservers an.
ms.assetid: cd84911b-3658-489f-b454-23eded0cbfa0
title: MFNETSOURCE_PROXYPORT-Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ac286fdcce276a29f08fef9df536f9a92152729791ff04d63478246825a718f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874624"
---
# <a name="mfnetsource_proxyport-property"></a>MFNETSOURCE \_ PROXYPORT-Eigenschaft

Gibt die Portnummer des Proxyservers an.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

**DWORD** (gespeichert als **LONG**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Hinweise

Die Konstante **MFNETSOURCE \_ PROXYPORT** definiert die GUID für diesen Eigenschaftsschlüssel. Der Eigenschaftenbezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um den Proxylocator beim Erstellen des Proxylocatorobjekts zu konfigurieren. Um die Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore-Zeiger** im *pProxyConfig-Parameter* der [**MFCreateProxyLocator-Funktion.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) Wenn diese Eigenschaft nicht für HTTP festgelegt ist, verwendet der Proxylocator standardmäßig den Wert 80.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Proxyunterstützung für Netzwerkquellen](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




