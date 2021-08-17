---
title: ncadg_ip_udp-Attribut
description: Das Schlüsselwort ncadg \_ ip \_ udp identifiziert die Datagrammversion von TCP/IP als Protokollfamilie für den Endpunkt. Diese Protokollfamilie ist veraltet und sollte nicht in neuen Anwendungen verwendet werden.
ms.assetid: c9133fcc-6dc2-49da-9c6f-5ce3c51090d5
keywords:
- ncadg_ip_udp-Attribut MIDL
topic_type:
- apiref
api_name:
- ncadg_ip_udp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f91db32fd7636f956e64dafc0db15efb520e643b435995dd977db7a631a20c78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067060"
---
# <a name="ncadg_ip_udp-attribute"></a>ncadg \_ ip \_ udp-Attribut

Das **Schlüsselwort ncadg \_ ip \_ udp** identifiziert die Datagrammversion von TCP/IP als Protokollfamilie für den Endpunkt. Diese Protokollfamilie ist veraltet und sollte nicht in neuen Anwendungen verwendet werden.

``` syntax
endpoint("ncadg_ip_udp:server-name[port-name]")
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Servername* 
</dt> <dd>

Gibt den Namen oder die Internetadresse für den Server oder Hostcomputer an. Der Name ist eine Zeichenfolge und kann ein vollqualifizierter Domänenname sein. Die Internetadresse ist eine allgemeine Internetadressen-Notation.

</dd> <dt>

*Portname* 
</dt> <dd>

Gibt eine optionale 16-Bit-Zahl an. Werte kleiner als 1024 sind in der Regel reserviert. Wenn kein Wert angegeben wird, wählt der Endpunktzuordnungsdienst einen gültigen *Portnamenwert* aus.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die folgenden Einschränkungen gelten für die Datagrammprotokolle [**ncadg \_ ipx**](ncadg-ipx.md) und **ncadg \_ ip \_ udp:**

-   Rückrufe werden nicht unterstützt. Alle Funktionen, die das **\[** [](callback.md) **\]** Rückrufattribut verwenden, schlagen fehl.
-   Sie unterstützen nicht die [](pipe.md) Verwendung des Pipetypkonstruktors.

Die Syntax der TCP/IP-Transportportzeichenfolge wird wie alle Portzeichenfolgen unabhängig von der IDL-Spezifikation definiert. Der Compiler führt eine Syntaxüberprüfung durch, garantiert jedoch nicht, dass die Endpunktspezifikation korrekt ist. Einige Fehler können zur Laufzeit und nicht zur Kompilierzeit gemeldet werden.

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ip_udp:rainier[1404]") 
]
interface iface1
{
    // Interface definition statements.
}

[
    uuid(87654321-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ip_udp:128.10.2.30[1404]") 
]
interface iface2
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Endpunkt**](endpoint.md)
</dt> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**ncacn \_ bei \_ dsp**](ncacn-at-dsp.md)
</dt> <dt>

[**ncacn \_ dnet \_ nsp**](ncacn-dnet-nsp.md)
</dt> <dt>

[**ncacn \_ ip \_ tcp**](ncacn-ip-tcp.md)
</dt> <dt>

[**ncacn \_ nb \_ ipx**](ncacn-nb-ipx.md)
</dt> <dt>

[**ncacn \_ spx**](ncacn-spx.md)
</dt> <dt>

[**ncacn \_ nb \_ nb**](ncacn-nb-nb.md)
</dt> <dt>

[**ncacn \_ nb \_ tcp**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn \_ np**](ncacn-np.md)
</dt> <dt>

[**ncacn \_ vns \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> <dt>

[Zeichenfolgenbindung](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 