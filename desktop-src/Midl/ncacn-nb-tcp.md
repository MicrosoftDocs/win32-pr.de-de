---
title: ncacn_nb_tcp-Attribut
description: Das Schlüsselwort ncacn \_ NB \_ TCP wird zum Identifizieren von TCP über NetBIOS als Protokollfamilie für den Endpunkt verwendet. Diese Protokollfamilie ist veraltet und sollte in neuen Anwendungen nicht verwendet werden.
ms.assetid: 3633842c-d1f5-46d9-866e-e54f31415ea5
keywords:
- ncacn_nb_tcp Attribut-Mittel l
topic_type:
- apiref
api_name:
- ncacn_nb_tcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d59a544c592643cffcb282ba8a0f3fdab48c03fd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314997"
---
# <a name="ncacn_nb_tcp-attribute"></a>ncacn \_ NB \_ TCP-Attribut

Das Schlüsselwort **ncacn \_ NB \_ TCP** wird zum Identifizieren von TCP über NetBIOS als Protokollfamilie für den Endpunkt verwendet. Diese Protokollfamilie ist veraltet und sollte in neuen Anwendungen nicht verwendet werden.

``` syntax
endpoint("ncacn_nb_tcp:[port-name]")
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
    endpoint("ncacn_nb_tcp:[100]") 
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

[**ncacn \_ NB \_ NB**](ncacn-nb-nb.md)
</dt> <dt>

[**ncacn \_ NP**](ncacn-np.md)
</dt> <dt>

[**ncacn- \_ SPX**](ncacn-spx.md)
</dt> <dt>

[**Ncalrpc**](ncalrpc.md)
</dt> <dt>

[**Zeichen folgen Bindung**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 