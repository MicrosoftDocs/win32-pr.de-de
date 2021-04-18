---
title: ncacn_ip_tcp-Attribut
description: Das ncacn \_ IP- \_ TCP-Schlüsselwort identifiziert TCP/IP als Protokollfamilie für den Endpunkt.
ms.assetid: 8142c667-9a5f-4066-a36d-1bb5ce551d21
keywords:
- ncacn_ip_tcp Attribut-Mittel l
topic_type:
- apiref
api_name:
- ncacn_ip_tcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1adb57951e862ebcdfa6889aae170bfdf5a14f96
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340706"
---
# <a name="ncacn_ip_tcp-attribute"></a>ncacn \_ -IP- \_ TCP-Attribut

Das **ncacn \_ IP- \_ TCP** -Schlüsselwort identifiziert TCP/IP als Protokollfamilie für den Endpunkt.

``` syntax
endpoint("ncacn_ip_tcp:server-name[port-name]")
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Servername* 
</dt> <dd>

Gibt den Namen oder die Internet Adresse für den Server oder Host Computer an. Der Name ist eine Zeichenfolge. Die Internetadresse ist eine gängige Internet Adress Notation.

</dd> <dt>

*Portname* 
</dt> <dd>

Gibt eine optionale 16-Bit-Zahl an. Werte, die kleiner als 1024 sind, sind normalerweise reserviert. Wenn kein Wert angegeben wird, wählt der Endpunkt Zuordnung einen gültigen *Portnamen* Wert aus.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Syntax der TCP/IP-Transport Port Zeichenfolge, wie alle Port Zeichenfolgen, wird unabhängig von der IDL-Spezifikation definiert. Der Compiler führt einige Syntax Überprüfungen durch, gewährleistet jedoch nicht, dass die Endpunkt Spezifikation korrekt ist. Einige Fehler werden möglicherweise zur Laufzeit und nicht zur Kompilierzeit gemeldet.

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

[**Dreher**](endpoint.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ncacn \_ NB \_ TCP**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn \_ NP**](ncacn-np.md)
</dt> <dt>

[**ncacn- \_ SPX**](ncacn-spx.md)
</dt> <dt>

[**Ncalrpc**](ncalrpc.md)
</dt> <dt>

[**Zeichen folgen Bindung**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 