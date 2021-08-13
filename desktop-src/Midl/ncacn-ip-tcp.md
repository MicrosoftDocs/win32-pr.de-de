---
title: ncacn_ip_tcp-Attribut
description: Das ncacn \_ ip \_ tcp-Schlüsselwort identifiziert TCP/IP als Protokollfamilie für den Endpunkt.
ms.assetid: 8142c667-9a5f-4066-a36d-1bb5ce551d21
keywords:
- ncacn_ip_tcp MIDL-Attribut
topic_type:
- apiref
api_name:
- ncacn_ip_tcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c34ba0a872af79245469818121761a38d356316b53a31743f9ebf2cd66f72325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642230"
---
# <a name="ncacn_ip_tcp-attribute"></a>ncacn \_ ip \_ tcp-Attribut

Das **schlüsselwort ncacn \_ ip \_ tcp** identifiziert TCP/IP als Protokollfamilie für den Endpunkt.

``` syntax
endpoint("ncacn_ip_tcp:server-name[port-name]")
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Servername* 
</dt> <dd>

Gibt den Namen oder die Internetadresse für den Server oder Hostcomputer an. Der Name ist eine Zeichenfolge. Die Internetadresse ist eine gängige Internetadressen-Notation.

</dd> <dt>

*Portname* 
</dt> <dd>

Gibt eine optionale 16-Bit-Zahl an. Werte kleiner als 1024 sind in der Regel reserviert. Wenn kein Wert angegeben wird, wählt der Endpunktzuordnungsdienst einen *gültigen Portnamenwert* aus.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Syntax der TCP/IP-Transportportzeichenfolge wird wie alle Portzeichenfolgen unabhängig von der IDL-Spezifikation definiert. Der Compiler führt einige Syntaxüberprüfungen durch, garantiert jedoch nicht, dass die Endpunktspezifikation korrekt ist. Einige Fehler werden möglicherweise zur Laufzeit und nicht zur Kompilierzeit gemeldet.

## <a name="examples"></a>Beispiele

``` syntax
[   
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_ip_tcp:rainier[1404]") 
]
interface iface
{
    // Interface definition statements.
}

 
endpoint("ncacn_ip_tcp:128.10.2.30[1404]")
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Endpunkt**](endpoint.md)
</dt> <dt>

[Schnittstellendefinitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ncacn \_ nb \_ tcp**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn \_ np**](ncacn-np.md)
</dt> <dt>

[**ncacn \_ spx**](ncacn-spx.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**Zeichenfolgenbindung**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 