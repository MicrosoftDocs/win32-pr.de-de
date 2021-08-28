---
description: Gibt eine durch Semikolons getrennte Liste von Medienservern an, die Verbindungen von Clientanwendungen ohne Verwendung eines Proxyservers akzeptieren können.
ms.assetid: 218883c5-9a26-4733-8308-1827cf1f2cd7
title: MFNETSOURCE_PROXYEXCEPTIONLIST-Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e87c07068d31cdd5e9762dab14e2a61edbe9c8f90f8750acc1b23c851ad47c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113490"
---
# <a name="mfnetsource_proxyexceptionlist-property"></a>MFNETSOURCE \_ PROXYEXCEPTIONLIST-Eigenschaft

Gibt eine durch Semikolons getrennte Liste von Medienservern an, die Verbindungen von Clientanwendungen ohne Verwendung eines Proxyservers akzeptieren können.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

Breitzeichenfolge (**WCHAR** \* )

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>Hinweise

Die Konstante **MFNETSOURCE \_ PROXYEXCEPTIONLIST** definiert die GUID für diesen Eigenschaftsschlüssel. Der Eigenschaftenbezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um den Proxylocator beim Erstellen des Proxylocatorobjekts zu konfigurieren. Um die Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore-Zeiger** im *pProxyConfig-Parameter* der [**MFCreateProxyLocator-Funktion.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) Der Proxylocator führt keine Proxyerkennung für diese Adressen durch.

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

 

 




