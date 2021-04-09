---
title: Ncalrpc-Attribut
description: Das Ncalrpc-Schlüsselwort identifiziert die lokale prozessübergreifende Kommunikation als Protokollfamilie für den Endpunkt. Dieses Schlüsselwort ist einer der gültigen Protokoll Familiennamen, die mit dem Attribut \ Endpoint \ verwendet werden müssen.
ms.assetid: 0009f794-5c14-4484-9023-cb20c7030dc5
keywords:
- Ncalrpc-Attribut-Mittel l
topic_type:
- apiref
api_name:
- ncalrpc
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f20ae9e347303288868eeb16758736047fecc1b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948707"
---
# <a name="ncalrpc-attribute"></a>Ncalrpc-Attribut

Das **Ncalrpc** -Schlüsselwort identifiziert die lokale prozessübergreifende Kommunikation als Protokollfamilie für den Endpunkt. Dieses Schlüsselwort ist einer der gültigen Protokoll Familiennamen, die mit dem **\[** [**Endpunkt**](endpoint.md) Attribut verwendet werden müssen **\]** .

``` syntax
endpoint("ncalrpc:[port-name]")
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Portname* 
</dt> <dd>

Eine Zeichenfolge, die den Kommunikationsport (eine Anwendung, einen Dienst oder eine Instanz eines Dienstanbieter) angibt, der von einem Client verwendet wird, um prozessübergreifende Aufrufe an einen Server vorzunehmen. Die Zeichenfolge kann bis zu 53 Zeichen enthalten und darf keinen umgekehrten Schrägstrich ( \) Zeichen) enthalten. Der Computername darf nicht mit dem Schlüsselwort **Ncalrpc** verwendet werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Syntax der lokalen Port Zeichenfolge für die prozessübergreifende Kommunikation, wie alle Port Zeichenfolgen, wird durch die Transport Implementierung definiert und ist unabhängig von der IDL-Spezifikation. Der mittlerer l-Compiler führt eine eingeschränkte Syntax Überprüfung durch, gewährleistet jedoch nicht, dass die Endpunkt Spezifikation korrekt ist. Einige Klassen von Fehlern können zur Laufzeit und nicht zur Kompilierzeit gemeldet werden.

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

[**ncacn \_ VNS- \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**ncadg \_ -IP- \_ UDP**](ncadg-ip-udp.md)
</dt> <dt>

[**ncadg \_ IPX**](ncadg-ipx.md)
</dt> <dt>

[Zeichen folgen Bindung](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 