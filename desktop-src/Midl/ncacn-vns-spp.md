---
title: ncacn_vns_spp-Attribut
description: Das Schlüsselwort ncacn \_ VNS \_ spp identifiziert Banyan VINES SPP als Protokollfamilie für den Endpunkt. Diese Protokollfamilie ist veraltet und sollte in neuen Anwendungen nicht verwendet werden.
ms.assetid: a2aff0a6-2e7e-43e4-a180-f1ddd0456843
keywords:
- ncacn_vns_spp Attribut-Mittel l
topic_type:
- apiref
api_name:
- ncacn_vns_spp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e72cd17ae65fbffc2cef280f15d12ba0ddbdbe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726080"
---
# <a name="ncacn_vns_spp-attribute"></a>ncacn \_ VNS- \_ spp-Attribut

Das Schlüsselwort **ncacn \_ VNS \_ spp** identifiziert Banyan VINES SPP als Protokollfamilie für den Endpunkt. Diese Protokollfamilie ist veraltet und sollte in neuen Anwendungen nicht verwendet werden.

``` syntax
endpoint("ncacn_vns_spp:server-name[port-address]")
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Servername* 
</dt> <dd>

Gibt den StreetTalk-Namen des Servers an. Der Name hat das Format item@group @organization . Das Element kann bis zu 31 Zeichen lang sein, und die Gruppe und die Organisation können bis zu 15 Zeichen lang sein.

</dd> <dt>

*Portname* 
</dt> <dd>

Gibt einen Banyan VINES-SPP-Port an. Der gültige Bereich für statische Endpunkte ist 250 – 511.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die entsprechende Banyan Enterprise-Client Software muss installiert sein, damit das **ncacn \_ VNS- \_ spp** -Transportprotokoll in verteilten Anwendungen unter Windows 2000 verwendet werden kann. Öffnen Sie nach der Installation die **Systemsteuerung**, wählen Sie **Konfiguration und hinzufügen** aus, und wählen Sie dann **Dienst \| Banyan \| RPC-Dienste für Banyan aus**. Die Unterstützung für 16-Bit-Clients erfordert die geeignete rebsoftware. Weitere Informationen über das Enterprise Client-Produkt und die 16-Bit-Reben Software finden Sie in der Banyan-Version.

Die Syntax der spp-Transport Port Zeichenfolge von Banyan Vines, wie alle Port Zeichenfolgen, wird unabhängig von der IDL-Spezifikation definiert. Der Compiler führt einige Syntax Überprüfungen durch, gewährleistet jedoch nicht, dass die Endpunkt Spezifikation korrekt ist. Einige Fehler werden möglicherweise zur Laufzeit und nicht zur Kompilierzeit gemeldet.

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

[**Dreher**](endpoint.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ncacn \_ bei \_ DSP**](ncacn-at-dsp.md)
</dt> <dt>

[**ncacn \_ dnet \_ NSP**](ncacn-dnet-nsp.md)
</dt> <dt>

[**ncacn \_ IP \_ TCP**](ncacn-ip-tcp.md)
</dt> <dt>

[**ncacn \_ NB \_ IPX**](ncacn-nb-ipx.md)
</dt> <dt>

[**ncacn- \_ SPX**](ncacn-spx.md)
</dt> <dt>

[**ncacn \_ NB \_ NB**](ncacn-nb-nb.md)
</dt> <dt>

[**ncacn \_ NB \_ TCP**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn \_ NP**](ncacn-np.md)
</dt> <dt>

[**Ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ IPX**](ncadg-ipx.md)
</dt> <dt>

[**ncadg \_ -IP- \_ UDP**](ncadg-ip-udp.md)
</dt> <dt>

[Zeichen folgen Bindung](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 