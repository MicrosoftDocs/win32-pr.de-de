---
title: ncadg_ipx-Attribut
description: Das Schlüsselwort ncadg \_ ipx identifiziert IPX als Protokollfamilie für den Endpunkt. Diese Protokollfamilie ist veraltet und sollte nicht in neuen Anwendungen verwendet werden.
ms.assetid: 6b136eb9-4e18-43ff-993b-a2ad005273f1
keywords:
- ncadg_ipx MIDL-Attribut
topic_type:
- apiref
api_name:
- ncadg_ipx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbca1ef3cb5f51e54fe8b95aa16326c6438903ff9717258edea9fac491eebafa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067050"
---
# <a name="ncadg_ipx-attribute"></a>ncadg \_ ipx-Attribut

Das **Schlüsselwort ncadg \_ ipx** identifiziert IPX als Protokollfamilie für den Endpunkt. Diese Protokollfamilie ist veraltet und sollte nicht in neuen Anwendungen verwendet werden.

``` syntax
endpoint("ncadg_ipx:link-address[port-name]")
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Linkadresse* 
</dt> <dd>

Gibt den Hostserver an. Dies kann entweder eine Zeichenfolge (der Servername) oder eine 20-stellige Hexadezimalzahl sein, die aus der Netzwerkadresse (8 Ziffern) des Hostservers besteht, die mit der Knotenadresse (12 Ziffern) verkettet ist. Anweisungen zum Abrufen der Netzwerkadresse und Knotenadresse finden Sie unter Hinweise. Eine **NULL-Zeichenfolge** gibt den lokalen Computer an.

</dd> <dt>

*Portname* 
</dt> <dd>

Gibt eine optionale 16-Bit-Zahl an, die die Socketadresse darstellt. Die Werte können zwischen 1 und 65535 liegen. Wenn kein Wert angegeben wird, wählt der Endpunktzuordnungsdienst einen *gültigen Portnamenwert* aus.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die folgenden Einschränkungen gelten für die Datagrammprotokolle **ncadg \_ ipx** und [**ncadg \_ ip \_ udp:**](ncadg-ip-udp.md)

-   Rückrufe werden nicht unterstützt. Alle Funktionen, die das **\[** [**Rückrufattribut**](callback.md) **\]** verwenden, führen zu einem Fehler.
-   Die Verwendung des Pipetypkonstruktors [**wird**](pipe.md) nicht unterstützt.

Bei Verwendung des **ncadg-ipx-Transports \_** ist der Servername identisch mit dem 32-Bit-Windows Servernamen. Da die Namen jedoch mithilfe von Protokollen von Werden verteilt werden, müssen sie den Benennungskonventionen von Bein entsprechen. Wenn es sich bei einem Servernamen nicht um einen gültigen Namen handelt, können Server keine Endpunkte mit dem **ncadg \_ ipx-Transport** erstellen. Im Folgenden finden Sie eine partielle Liste von Zeichen, die in Den-Servernamen unzulässig sind:

" \* + . / : ; < = > ? \[ \] \\ \|

Der **ncadg \_ ipx-Transport** wird von der version of NWLink unterstützt, die mit MS Client 3.0 bereitgestellt wird.

16-Bit-Windows-Clientanwendungen, die den **ncadg \_ ipx-Transport** verwenden, erfordern, dass die Datei Nwipxspx.dll installiert ist, um unter dem WOW-Subsystem ausgeführt zu werden. Wenden Sie sich an Den, um diese Datei zu erhalten.

Um die Netzwerk- und Knotenadressen zu erhalten, verwenden Sie das **Comcheck-Hilfsprogramm** von Perl oder die von DerTegetInternetAddress definierte **API.** Auf Windows können Sie diese Adressen auch mit dem Befehl **ipxroute config** abrufen.

Die Syntax der TCP/IP-Transportportzeichenfolge wird wie alle Portzeichenfolgen unabhängig von der IDL-Spezifikation definiert. Der Compiler führt einige Syntaxüberprüfungen durch, garantiert jedoch nicht, dass die Endpunktspezifikation korrekt ist. Einige Fehler werden möglicherweise zur Laufzeit und nicht zur Kompilierzeit gemeldet.

> [!Note]  
> Diese Protokollfamilie wird in Windows XP nicht unterstützt.

 

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ipx:[1000]") 
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

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[Zeichenfolgenbindung](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 