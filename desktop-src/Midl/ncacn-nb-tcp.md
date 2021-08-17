---
title: ncacn_nb_tcp-Attribut
description: Das tcp-Schlüsselwort ncacn nb wird verwendet, um \_ TCP über NetBIOS als \_ Protokollfamilie für den Endpunkt zu identifizieren. Diese Protokollfamilie ist veraltet und sollte nicht in neuen Anwendungen verwendet werden.
ms.assetid: 3633842c-d1f5-46d9-866e-e54f31415ea5
keywords:
- ncacn_nb_tcp MIDL-Attribut
topic_type:
- apiref
api_name:
- ncacn_nb_tcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683be3c986c81feb270d5d502f3da0f56a65d78973c60e4b664c2e4bd75e0494
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642165"
---
# <a name="ncacn_nb_tcp-attribute"></a>ncacn \_ nb \_ tcp-Attribut

Das **tcp-Schlüsselwort \_ \_ ncacn nb** wird verwendet, um TCP über NetBIOS als Protokollfamilie für den Endpunkt zu identifizieren. Diese Protokollfamilie ist veraltet und sollte nicht in neuen Anwendungen verwendet werden.

``` syntax
endpoint("ncacn_nb_tcp:[port-name]")
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Portname* 
</dt> <dd>

Gibt einen optionalen 8-Bit-Wert im Bereich von 1 bis 254 an. Werte kleiner als 0x20 sind reserviert. Wenn der *Portnamewert nicht* angegeben wird, wählt der Endpunktzuordnungsdienst den Portwert aus.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Syntax der NetBIOS-Portzeichenfolge wird wie alle Portzeichenfolgen von der Transportimplementierung definiert und ist unabhängig von der IDL-Spezifikation. Der MIDL-Compiler führt eine eingeschränkte Syntaxüberprüfung durch, garantiert jedoch nicht, dass die Endpunktspezifikation korrekt ist. Einige Fehlerklassen werden möglicherweise zur Laufzeit und nicht zur Kompilierzeit gemeldet.

> [!Note]  
> Diese Protokollfamilie wird in Windows XP nicht unterstützt.

 

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_nb_tcp:[100]") 
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

[**ncacn \_ nb \_ nb**](ncacn-nb-nb.md)
</dt> <dt>

[**ncacn \_ np**](ncacn-np.md)
</dt> <dt>

[**ncacn \_ spx**](ncacn-spx.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**Zeichenfolgenbindung**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 