---
title: ncacn_spx-Attribut
description: Das ncacn- \_ SPX-Schlüsselwort identifiziert SPX als Protokollfamilie für den Endpunkt. Diese Protokollfamilie ist veraltet und sollte in neuen Anwendungen nicht verwendet werden.
ms.assetid: 45e93e25-e84d-4242-80b0-c4b61e80f716
keywords:
- ncacn_spx Attribut-Mittel l
topic_type:
- apiref
api_name:
- ncacn_spx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09d27cc746df906ff6b1a3290e41d860c76dc362
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106339880"
---
# <a name="ncacn_spx-attribute"></a>ncacn- \_ SPX-Attribut

Das **ncacn- \_ SPX** -Schlüsselwort identifiziert SPX als Protokollfamilie für den Endpunkt. Diese Protokollfamilie ist veraltet und sollte in neuen Anwendungen nicht verwendet werden.

``` syntax
endpoint("ncacn_spx:link-address[port-name]")
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Linkadresse* 
</dt> <dd>

Gibt den Host Server an. Dies kann entweder eine Zeichenfolge (der Servername) oder eine 20-stellige hexadezimal Zahl sein, die aus der Netzwerkadresse des Host Servers (8 Ziffern) besteht, die mit der Knotenadresse (12 Ziffern) verkettet ist. Anweisungen zum Abrufen der Netzwerkadresse und der Knotenadresse finden Sie unter "Hinweise". Eine **null** -Zeichenfolge gibt den lokalen Computer an.

</dd> <dt>

*Portname* 
</dt> <dd>

Gibt eine optionale 16-Bit-Zahl an, die die Socketadresse darstellt. Die Werte können zwischen 1 und 65.535 liegen. Wenn kein Wert angegeben wird, wählt der Endpunkt Zuordnung einen gültigen *Portnamen* Wert aus.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie den **ncacn- \_ SPX** -Transport verwenden, ist der Servername genau mit dem 32-Bit-Windows-Namen identisch. Da die Namen jedoch mithilfe von Novell-Protokollen verteilt werden, müssen Sie den Novell-Benennungs Konventionen entsprechen. Wenn ein Servername kein gültiger Novell-Name ist, können Server mit dem **ncacn- \_ SPX** -Transport keine Endpunkte erstellen. Im folgenden finden Sie eine unvollständige Liste von Zeichen, die in Novell-Servernamen nicht zulässig sind:

" \* + . / : ; < = >? \[ \] \\ \|

Der **ncacn- \_ SPX** -Transport wird von der mit MS Client 3,0 bereitgestellten NWLink-Version nicht unterstützt.

für 16-Bit-Windows-Client Anwendungen, die den **ncacn- \_ SPX** -Transport verwenden, muss die Datei Nwipxspx.dll installiert werden, um unter dem wow-Subsystem ausgeführt werden zu können. Wenden Sie sich an Novell, um diese Datei zu erhalten.

> [!Note]  
> Verwenden Sie zum Abrufen der Netzwerk-und Knoten Adressen das **com** -Hilfsprogramm von Novell oder die Novell-definierte API **ipxgetinternetaddress**. Unter Windows können Sie diese Adressen auch mit dem Befehl " **ipxroute config** " abrufen.

 

Die Syntax der SPX-Transport Port Zeichenfolge, wie alle Port Zeichenfolgen, wird unabhängig von der IDL-Spezifikation definiert. Der Compiler führt einige Syntax Überprüfungen durch, gewährleistet jedoch nicht, dass die Endpunkt Spezifikation korrekt ist. Einige Fehler werden möglicherweise zur Laufzeit und nicht zur Kompilierzeit gemeldet.

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_spx:[1000]") 
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

[**ncacn \_ NB \_ NB**](ncacn-nb-nb.md)
</dt> <dt>

[**ncacn \_ NB \_ TCP**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn \_ NP**](ncacn-np.md)
</dt> <dt>

[**ncacn \_ VNS- \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**Ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ IPX**](ncadg-ipx.md)
</dt> <dt>

[**ncadg \_ -IP- \_ UDP**](ncadg-ip-udp.md)
</dt> <dt>

[Zeichen folgen Bindung](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 