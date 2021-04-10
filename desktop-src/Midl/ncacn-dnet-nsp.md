---
title: ncacn_dnet_nsp-Attribut
description: Das Schlüsselwort ncacn \_ dnet \_ NSP identifiziert DECnet als Protokollfamilie für den Endpunkt. Diese Protokollfamilie ist veraltet und sollte in neuen Anwendungen nicht verwendet werden.
ms.assetid: 797251c1-c5d3-416b-8bc7-5b83bb7027e6
keywords:
- ncacn_dnet_nsp Attribut-Mittel l
topic_type:
- apiref
api_name:
- ncacn_dnet_nsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6312aff15d3bdef85d1e37829d669ce1faa5fbb4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101603"
---
# <a name="ncacn_dnet_nsp-attribute"></a>ncacn \_ dnet \_ NSP-Attribut

Das Schlüsselwort **ncacn \_ dnet \_ NSP** identifiziert DECnet als Protokollfamilie für den Endpunkt. Diese Protokollfamilie ist veraltet und sollte in neuen Anwendungen nicht verwendet werden.

``` syntax
endpoint("ncacn_dnet_nsp:server-name[port-name]")
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Servername* 
</dt> <dd>

Gibt den Namen oder die Internetadresse für den Server oder Host Computer an. Der Name ist eine Zeichenfolge.

</dd> <dt>

*Portname* 
</dt> <dd>

Gibt den Namen oder die Objekt Nummer eines DECnet-Objekts an. Der Objektname kann aus bis zu 16 Zeichen bestehen. Objektnummern kann das Nummern Zeichen () als Präfix vorangestellt werden \# .

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Syntax der Port Zeichenfolge für den DECnet-Transport wird, wie alle Port Zeichenfolgen, unabhängig von der IDL-Spezifikation definiert. Der Compiler führt einige Syntax Überprüfungen durch, gewährleistet jedoch nicht, dass die Endpunkt Spezifikation korrekt ist. Einige Fehler werden möglicherweise zur Laufzeit und nicht zur Kompilierzeit gemeldet.

> [!Note]  
> Diese Protokollfamilie wird in Windows XP nicht unterstützt.

 

## <a name="examples"></a>Beispiele

``` syntax
[   
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_dnet_nsp:node[RPC0034501]") 
interface iface
{
    // Interface definition statements.
}

[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.1), 
    endpoint("ncacn_dnet_nsp:node[#41]") 
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

[**Zeichen folgen Bindung**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 