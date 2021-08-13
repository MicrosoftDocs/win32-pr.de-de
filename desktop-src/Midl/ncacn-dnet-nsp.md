---
title: ncacn_dnet_nsp-Attribut
description: Das ncacn \_ dnet \_ nsp-Schlüsselwort identifiziert DECnet als Protokollfamilie für den Endpunkt. Diese Protokollfamilie ist veraltet und sollte nicht in neuen Anwendungen verwendet werden.
ms.assetid: 797251c1-c5d3-416b-8bc7-5b83bb7027e6
keywords:
- ncacn_dnet_nsp MIDL-Attribut
topic_type:
- apiref
api_name:
- ncacn_dnet_nsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4fa7448ff9d0cf3946ad3d0293ade19a5c2c0c407ca157d79c2c425f4a8ef6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642761"
---
# <a name="ncacn_dnet_nsp-attribute"></a>ncacn \_ dnet \_ nsp-Attribut

Das **ncacn \_ dnet \_ nsp-Schlüsselwort** identifiziert DECnet als Protokollfamilie für den Endpunkt. Diese Protokollfamilie ist veraltet und sollte nicht in neuen Anwendungen verwendet werden.

``` syntax
endpoint("ncacn_dnet_nsp:server-name[port-name]")
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Servername* 
</dt> <dd>

Gibt den Namen oder die Internetadresse für den Server oder Hostcomputer an. Der Name ist eine Zeichenfolge.

</dd> <dt>

*Portname* 
</dt> <dd>

Gibt einen DECnet-Objektnamen oder eine Objektnummer an. Der Objektname kann aus bis zu 16 Zeichen bestehen. Objektnummern kann das Nummernzeichen () vorangestellt \# werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Syntax der DECnet-Transportportzeichenfolge wird wie alle Portzeichenfolgen unabhängig von der IDL-Spezifikation definiert. Der Compiler führt einige Syntaxüberprüfungen durch, garantiert jedoch nicht, dass die Endpunktspezifikation korrekt ist. Einige Fehler werden möglicherweise zur Laufzeit und nicht zur Kompilierzeit gemeldet.

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

[**Endpunkt**](endpoint.md)
</dt> <dt>

[**Zeichenfolgenbindung**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 