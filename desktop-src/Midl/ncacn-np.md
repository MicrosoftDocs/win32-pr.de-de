---
title: ncacn_np-Attribut
description: Das Schlüsselwort ncacn \_ NP identifiziert Named Pipes als Protokollfamilie für den Endpunkt.
ms.assetid: 02961bb8-faf0-42e5-b134-dd2983e6d146
keywords:
- ncacn_np Attribut-Mittel l
topic_type:
- apiref
api_name:
- ncacn_np
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84634e6bb5d2b634439be767ad44749291cffe11
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726736"
---
# <a name="ncacn_np-attribute"></a>ncacn- \_ NP-Attribut

Das Schlüsselwort **ncacn \_ NP** identifiziert Named Pipes als Protokollfamilie für den Endpunkt.

``` syntax
endpoint("ncacn_np:server-name[\\pipe\\pipe-name]")
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Servername* 
</dt> <dd>

Dies ist optional. Gibt den Namen des Servers an. Umgekehrte Schrägstriche sind optional.

</dd> <dt>

*Pipename* 
</dt> <dd>

Gibt einen gültigen Pipenamen an. Ein gültiger Pipename ist eine Zeichenfolge, die Bezeichner enthält, die durch umgekehrte Schrägstriche getrennt sind. Der erste Bezeichner muss eine [**Pipe**](pipe.md)sein. Jeder Bezeichner muss durch zwei umgekehrte Schrägstriche getrennt werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Ein Server erstellt eine Instanz einer Named Pipe, die dann jedem Client zur Verfügung steht. Wenn ein Client versucht, eine Verbindung herzustellen, wird die vorhandene Instanz diesem Client zugeordnet. Bevor ein anderer Client eine Verbindung herstellen kann, muss vom Server eine weitere Instanz des Named Pipe erstellt werden. Wenn ein Client versucht, eine Bindung mit dem Server herzustellen, bevor die neue Instanz erstellt wird, schlägt der Bindungs Aufruf [**RpcBindingFromStringBinding**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding)möglicherweise fehl, und die Fehlermeldung RPC \_ S \_ Server ist \_ \_ ausgelastet. Daher müssen Sie sicherstellen, dass die Client Anwendung den Fall behandelt, in dem der Server zu stark ausgelastet ist, um eine Verbindung zu akzeptieren. Der Client sollte automatisch einen Wiederholungsversuch durchführen, den Benutzer zur Eingabe einer Aktion auffordern oder ordnungsgemäß fehlschlagen.

Die Syntax der Named Pipe-Port Zeichenfolge, wie alle Port Zeichenfolgen, wird von der Transport Implementierung definiert und ist unabhängig von der IDL-Spezifikation. Der mittlerer l-Compiler führt eine eingeschränkte Syntax Überprüfung durch, gewährleistet jedoch nicht, dass die Endpunkt Spezifikation korrekt ist. Einige Klassen von Fehlern können zur Laufzeit und nicht zur Kompilierzeit gemeldet werden.

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

[**ncacn \_ VNS- \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**Ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ IPX**](ncadg-ipx.md)
</dt> <dt>

[**ncadg \_ -IP- \_ UDP**](ncadg-ip-udp.md)
</dt> <dt>

[**Zeichen folgen Bindung**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 