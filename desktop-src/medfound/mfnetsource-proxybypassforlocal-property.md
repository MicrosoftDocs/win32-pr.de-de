---
description: Gibt an, ob der proxylocator einen Proxy Server für lokale Adressen verwenden soll.
ms.assetid: 384343f5-5919-44da-b8ea-0c994b4743a8
title: MFNETSOURCE_PROXYBYPASSFORLOCAL-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9476571ddd593b7930be1aa4376a836de3d75206
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749193"
---
# <a name="mfnetsource_proxybypassforlocal-property"></a>MF-Quelle \_ proxybypassforlocal (Eigenschaft)

Gibt an, ob der proxylocator einen Proxy Server für lokale Adressen verwenden soll.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

Boolescher Wert (**Long**)

VT \_ I4

**LVAL**



## <a name="remarks"></a>Bemerkungen

Die Konstante **MF-Quelle \_ proxybypassforlocal** definiert die GUID für diesen Eigenschafts Schlüssel. Der Eigenschaften Bezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um den proxylocator bei der Erstellung des proxylocator-Objekts zu konfigurieren. Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger im *pproxyconfig* -Parameter der [**mfkreateproxylocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) -Funktion. Der Wert muss auf 0 festgelegt werden, wenn der Proxy Server für lokale Adressen verwendet werden soll. Andernfalls konfiguriert ein Wert ungleich NULL den standardproxylocator, um den Proxy Server für lokale Adressen zu überspringen.

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

 

 




