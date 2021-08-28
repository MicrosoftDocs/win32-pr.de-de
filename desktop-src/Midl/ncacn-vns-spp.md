---
title: ncacn_vns_spp-Attribut
description: Das Schlüsselwort ncacn \_ vns \_ spp identifiziert Banyan Vines SPP als Protokollfamilie für den Endpunkt. Diese Protokollfamilie ist veraltet und sollte nicht in neuen Anwendungen verwendet werden.
ms.assetid: a2aff0a6-2e7e-43e4-a180-f1ddd0456843
keywords:
- ncacn_vns_spp-Attribut MIDL
topic_type:
- apiref
api_name:
- ncacn_vns_spp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8409e7e9e0bfc01545ac73673f0653c5a4940c65422223233ec5005f5c9fc02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119560280"
---
# <a name="ncacn_vns_spp-attribute"></a>ncacn \_ vns \_ spp-Attribut

Das **Schlüsselwort ncacn \_ vns \_ spp** identifiziert Banyan Vines SPP als Protokollfamilie für den Endpunkt. Diese Protokollfamilie ist veraltet und sollte nicht in neuen Anwendungen verwendet werden.

``` syntax
endpoint("ncacn_vns_spp:server-name[port-address]")
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Servername* 
</dt> <dd>

Gibt den StreetTalk-Namen des Servers an. Der Name hat das Format item@group @organization . Das Element kann bis zu 31 Zeichen lang sein, und die Gruppe und Organisation kann bis zu 15 Zeichen lang sein.

</dd> <dt>

*Portname* 
</dt> <dd>

Gibt einen Banyan Vines-SPP-Port an. Der gültige Bereich für statische Endpunkte beträgt 250 bis 511.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Um das **ncacn \_ vns \_ spp-Transportprotokoll** in verteilten Anwendungen zu verwenden, die auf Windows 2000 ausgeführt werden, muss die entsprechende Banyan Enterprise Client-Software installiert sein. Öffnen Sie nach der Installation **Systemsteuerung**, wählen Sie **Konfiguration und Hinzufügen** aus, und wählen Sie dann **Service \| Banyan RPC services for \| Banyan** aus. Die Unterstützung für 16-Bit-Clients erfordert entsprechende Vines-Software. Weitere Informationen zum Enterprise Client-Produkt von Banyan und zur 16-Bit-Vines-Software von Banyan, wenden Sie sich an Banyan.

Die Syntax der Banyan Vines SPP-Transportportzeichenfolge wird wie alle Portzeichenfolgen unabhängig von der IDL-Spezifikation definiert. Der Compiler führt eine Syntaxüberprüfung durch, garantiert jedoch nicht, dass die Endpunktspezifikation korrekt ist. Einige Fehler können zur Laufzeit und nicht zur Kompilierzeit gemeldet werden.

> [!Note]  
> Diese Protokollfamilie wird in Windows XP nicht unterstützt.

 

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.1), 
    endpoint("ncacn_vns_spp:printer@sdkgrp@company[260]")
]
interface iface
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

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[Zeichenfolgenbindung](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 