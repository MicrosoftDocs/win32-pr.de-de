---
title: ncacn_nb_ipx-Attribut
description: Das Schlüsselwort ncacn \_ NB \_ IPX identifiziert NetBIOS über IPX als Protokollfamilie für den Endpunkt. Diese Protokollfamilie ist veraltet und sollte in neuen Anwendungen nicht verwendet werden.
ms.assetid: 641471d4-eba4-4d4a-a3fe-1e40b3751e38
keywords:
- ncacn_nb_ipx Attribut-Mittel l
topic_type:
- apiref
api_name:
- ncacn_nb_ipx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 156b5c460c4cc8638640e7eb3500ec9a7a9fa0b0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340906"
---
# <a name="ncacn_nb_ipx-attribute"></a>ncacn- \_ NB- \_ IPX-Attribut

Das Schlüsselwort **ncacn \_ NB \_ IPX** identifiziert NetBIOS über IPX als Protokollfamilie für den Endpunkt. Diese Protokollfamilie ist veraltet und sollte in neuen Anwendungen nicht verwendet werden.

``` syntax
endpoint("ncacn_nb_ipx:[port-name]")
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Portname* 
</dt> <dd>

Gibt einen optionalen 8-Bit-Wert zwischen 1 und 254 an. Werte von weniger als 0x20 sind reserviert. Wenn der *Port-Name-* Wert nicht angegeben wird, wählt der Endpunkt Zuordnung den Portwert aus.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Syntax der NetBIOS-Port Zeichenfolge wird wie alle Port Zeichenfolgen durch die Transport Implementierung definiert und ist unabhängig von der IDL-Spezifikation. Der mittlerer l-Compiler führt eine eingeschränkte Syntax Überprüfung durch, gewährleistet jedoch nicht, dass die Endpunkt Spezifikation korrekt ist. Einige Klassen von Fehlern können zur Laufzeit und nicht zur Kompilierzeit gemeldet werden.

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

[**Dreher**](endpoint.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ncacn \_ IP \_ TCP**](ncacn-ip-tcp.md)
</dt> <dt>

[**ncacn \_ NB \_ TCP**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn \_ NB \_ NB**](ncacn-nb-nb.md)
</dt> <dt>

[**ncacn \_ bei \_ DSP**](ncacn-at-dsp.md)
</dt> <dt>

[**ncacn- \_ SPX**](ncacn-spx.md)
</dt> <dt>

[**ncacn \_ NP**](ncacn-np.md)
</dt> <dt>

[**Ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ -IP- \_ UDP**](ncadg-ip-udp.md)
</dt> <dt>

[**ncadg \_ IPX**](ncadg-ipx.md)
</dt> <dt>

[**Zeichen folgen Bindung**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 