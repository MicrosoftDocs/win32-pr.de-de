---
title: ncacn_nb_ipx-Attribut
description: Das \_ ncacn nb \_ ipx-Schlüsselwort identifiziert NetBIOS über IPX als Protokollfamilie für den Endpunkt. Diese Protokollfamilie ist veraltet und sollte nicht in neuen Anwendungen verwendet werden.
ms.assetid: 641471d4-eba4-4d4a-a3fe-1e40b3751e38
keywords:
- ncacn_nb_ipx-Attribut MIDL
topic_type:
- apiref
api_name:
- ncacn_nb_ipx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c8be67485d86a6094e2a41c01d5e0cf78cdabe5e251a3ab9ae046a47ed05d6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642222"
---
# <a name="ncacn_nb_ipx-attribute"></a>ncacn \_ nb \_ ipx-Attribut

Das **ncacn \_ nb \_ ipx-Schlüsselwort** identifiziert NetBIOS über IPX als Protokollfamilie für den Endpunkt. Diese Protokollfamilie ist veraltet und sollte nicht in neuen Anwendungen verwendet werden.

``` syntax
endpoint("ncacn_nb_ipx:[port-name]")
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Portname* 
</dt> <dd>

Gibt einen optionalen 8-Bit-Wert im Bereich von 1 bis 254 an. Werte kleiner als 0x20 sind reserviert. Wenn der *Portnamewert* nicht angegeben ist, wählt der Endpunktzuordnungsdienst den Portwert aus.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Syntax der NetBIOS-Portzeichenfolge wird wie alle Portzeichenfolgen von der Transportimplementierungen definiert und ist unabhängig von der IDL-Spezifikation. Der MIDL-Compiler führt eine eingeschränkte Syntaxüberprüfung durch, garantiert jedoch nicht, dass die Endpunktspezifikation korrekt ist. Einige Fehlerklassen werden möglicherweise zur Laufzeit und nicht zur Kompilierzeit gemeldet.

> [!Note]  
> Diese Protokollfamilie wird in Windows XP nicht unterstützt.

 

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_nb_ipx:[100]") 
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

[**ncacn \_ ip \_ tcp**](ncacn-ip-tcp.md)
</dt> <dt>

[**ncacn \_ nb \_ tcp**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn \_ nb \_ nb**](ncacn-nb-nb.md)
</dt> <dt>

[**ncacn \_ bei \_ dsp**](ncacn-at-dsp.md)
</dt> <dt>

[**ncacn \_ spx**](ncacn-spx.md)
</dt> <dt>

[**ncacn \_ np**](ncacn-np.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> <dt>

[**Zeichenfolgenbindung**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 