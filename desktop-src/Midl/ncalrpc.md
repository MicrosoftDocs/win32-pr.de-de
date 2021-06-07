---
title: ncalrpc-Attribut
description: Das Schlüsselwort ncalrpc identifiziert die lokale prozessübergreifende Kommunikation als Protokollfamilie für den Endpunkt. Dieses Schlüsselwort ist einer der gültigen Protokollfamiliennamen, die mit dem Attribut \endpoint\ verwendet werden müssen.
ms.assetid: 0009f794-5c14-4484-9023-cb20c7030dc5
keywords:
- ncalrpc-Attribut MIDL
topic_type:
- apiref
api_name:
- ncalrpc
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f5d22b572eb9ad2f2e46b029ec242b48d5cd684
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386879"
---
# <a name="ncalrpc-attribute"></a>ncalrpc-Attribut

Das **Schlüsselwort ncalrpc** identifiziert die lokale prozessübergreifende Kommunikation als Protokollfamilie für den Endpunkt. Dieses Schlüsselwort ist einer der gültigen Protokollfamiliennamen, die mit dem **\[** [](endpoint.md) **\]** Endpunktattribut verwendet werden müssen.

``` syntax
endpoint("ncalrpc:[port-name]")
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Portname* 
</dt> <dd>

Eine Zeichenfolge, die den Kommunikationsport (eine Anwendung, einen Dienst oder eine Instanz eines Diensts) angibt, den ein Client verwendet, um prozessübergreifende Aufrufe an einen Server zu tätigen. Die Zeichenfolge kann bis zu 53 Zeichen enthalten und darf keinen umgekehrten Schrägstrich \\ () enthalten. Der Computername darf nicht mit dem **Schlüsselwort ncalrpc** verwendet werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Syntax der lokalen Interprocess-Communication-Portzeichenfolge wird wie alle Portzeichenfolgen von der Transportimplementation definiert und ist unabhängig von der IDL-Spezifikation. Der MIDL-Compiler führt eine eingeschränkte Syntaxüberprüfung durch, garantiert jedoch nicht, dass die Endpunktspezifikation korrekt ist. Einige Fehlerklassen werden möglicherweise zur Laufzeit und nicht zur Kompilierzeit gemeldet.

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncalrpc:[myapplicationname]") 
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

[**ncacn \_ vns \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> <dt>

[Zeichenfolgenbindung](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 