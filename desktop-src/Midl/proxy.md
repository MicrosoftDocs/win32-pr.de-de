---
title: Proxyattribut
description: Das \proxy\-Attribut verhindert, dass automation sich als Proxy-/Stubhandler für eine duale Schnittstelle registriert.
ms.assetid: 88e59938-83c9-436a-931c-f4396fdcf653
keywords:
- Proxyattribut MIDL
topic_type:
- apiref
api_name:
- proxy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37e81cb7f67f87153825db59d921b6ee9ec7df6cd334ed2228896c8dec5f9d5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641419"
---
# <a name="proxy-attribute"></a>Proxyattribut

Das **\[ \] Proxyattribut** verhindert, dass automation sich als Proxy-/Stubhandler für eine duale Schnittstelle registriert.

``` syntax
[ 
    proxy, 
    uuid(string-uuid <>)
    [ , interface-attribute-list <>] 
] 
interface interface-name <> : base-interface <>
{
    ...
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*string-uuid* 
</dt> <dd>

Gibt eine Zeichenfolge an, die aus acht Hexadezimalziffern gefolgt von einem Bindestrich und dann aus drei Gruppen von jeweils vier Hexadezimalziffern gefolgt von einem Bindestrich und dann 12 Hexadezimalziffern besteht. Sie können die UUID-Zeichenfolge in Anführungszeichen einschließen, außer wenn Sie den MIDL-Compilerschalter [**/osf**](-osf.md)verwenden.

</dd> <dt>

*interface-attribute-list* 
</dt> <dd>

Gibt eine Liste von null oder mehr IDL-Attributen an, die für die gesamte Schnittstelle gelten. Wenn zwei oder mehr Schnittstellenattribute vorhanden sind, müssen sie durch Kommas getrennt werden.

</dd> <dt>

*Schnittstellenname* 
</dt> <dd>

Name der Schnittstelle.

</dd> <dt>

*Basisschnittstelle* 
</dt> <dd>

Gibt den Namen einer Schnittstelle an, von der diese abgeleitete Schnittstelle Memberfunktionen, Statuscodes und Schnittstellenattribute erbt. Die abgeleitete Schnittstelle erbt keine Typdefinitionen. Verwenden Sie hierzu [](import.md) das Importschlüsselwort, um die IDL-Datei der Basisschnittstelle zu importieren.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Verwendung des \[  \] Proxyattributs für eine duale Schnittstelle verhindert, dass der TLB generierte Stubs übernimmt. Wenn dieses Attribut angegeben wird, sollte die Registrierung des typelib-Proxys nicht aufgehoben werden, wenn die Registrierung der TypeLib aufgehoben wird.

### <a name="flags"></a>Flags

<dl> <dt>

<span id="TYPEFLAG_PROXY"></span><span id="typeflag_proxy"></span>\_TYPEFLAG-PROXY
</dt> <dd>

Schnittstellen können mit dem \_ TYPEFLAG-PROXYflag gekennzeichnet werden, um anzugeben, dass sie eine Proxy-/Stub-Dynamic Link-Bibliothek verwenden. Dieses Flag gibt an, dass die Registrierung des typelib-Proxys nicht aufgehoben werden soll, wenn die Registrierung der TypeLib aufgehoben wird.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Generieren einer Typbibliothek mit MIDL**](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Dual**](dual.md)
</dt> <dt>

[**Typeflags**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 