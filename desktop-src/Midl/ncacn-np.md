---
title: ncacn_np-Attribut
description: Das \_ ncacn np-Schlüsselwort identifiziert Named Pipes als Protokollfamilie für den Endpunkt.
ms.assetid: 02961bb8-faf0-42e5-b134-dd2983e6d146
keywords:
- ncacn_np-Attribut MIDL
topic_type:
- apiref
api_name:
- ncacn_np
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7acf294241c1d38b2067ba54e315fc3240e5bb6eca81a6b12012f8dec457a8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013758"
---
# <a name="ncacn_np-attribute"></a>ncacn \_ np-Attribut

Das **ncacn \_ np-Schlüsselwort** identifiziert Named Pipes als Protokollfamilie für den Endpunkt.

``` syntax
endpoint("ncacn_np:server-name[\\pipe\\pipe-name]")
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Servername* 
</dt> <dd>

Optional. Gibt den Namen des Servers an. Umgekehrte Schrägstriche sind optional.

</dd> <dt>

*pipe-name* 
</dt> <dd>

Gibt einen gültigen Pipenamen an. Ein gültiger Pipename ist eine Zeichenfolge mit Bezeichnern, die durch umgekehrte Schrägstriche getrennt sind. Der erste Bezeichner muss [**pipe**](pipe.md)sein. Jeder Bezeichner muss durch zwei umgekehrte Schrägstriche getrennt werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Ein Server erstellt eine Instanz einer Named Pipe, die dann für jeden Client verfügbar ist. Wenn ein Client versucht, eine Verbindung herzustellen, wird die vorhandene Instanz diesem Client zugeordnet. Bevor ein anderer Client eine Verbindung herstellen kann, muss der Server eine weitere Instanz der Named Pipe erstellen. Wenn ein Client versucht, eine Bindung an den Server herzustellen, bevor die neue Instanz erstellt wird, schlägt der Bindungsaufruf [**RpcBindingFromStringBinding**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding)möglicherweise mit der Fehlermeldung RPC \_ S SERVER TOO BUSY \_ \_ \_ fehl. Daher müssen Sie sicherstellen, dass Ihre Clientanwendung den Fall behandelt, in dem der Server zu ausgelastet ist, um eine Verbindung zu akzeptieren. Der Client sollte den Vorgang automatisch wiederholen, den Benutzer zur Aktion auffordern oder ordnungsgemäß fehlschlagen.

Die Syntax der Named Pipe-Portzeichenfolge wird wie alle Portzeichenfolgen von der Transportimplementierungen definiert und ist unabhängig von der IDL-Spezifikation. Der MIDL-Compiler führt eine eingeschränkte Syntaxüberprüfung durch, garantiert jedoch nicht, dass die Endpunktspezifikation korrekt ist. Einige Fehlerklassen werden möglicherweise zur Laufzeit und nicht zur Kompilierzeit gemeldet.

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_np:[\\pipe\\stove\\hat]") 
] 
interface iface1
{
    // Interface definition statements.
}

[
    uuid(87654321-4000-2006-0000-20000000001b), 
    version(1.1), 
    endpoint("ncacn_np:\\\\myotherserver[\\pipe\\corncob]") 
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

[**ncacn \_ vns \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[**Zeichenfolgenbindung**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 