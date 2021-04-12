---
title: Proxy Attribut
description: Das Attribut \ Proxy \ verhindert, dass die Automatisierung als Proxy-/stubhandler für eine duale Schnittstelle registriert wird.
ms.assetid: 88e59938-83c9-436a-931c-f4396fdcf653
keywords:
- Proxy Attribut-Mittel l
topic_type:
- apiref
api_name:
- proxy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa8c9d305b7f51a012ae26d7b1a76d2e3011fd7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472757"
---
# <a name="proxy-attribute"></a>Proxy Attribut

Das **\[ Proxy \]** Attribut verhindert, dass die Automatisierung als Proxy-/Stub-Handler für eine duale Schnittstelle registriert wird.

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

*Zeichenfolge-UUID* 
</dt> <dd>

Gibt eine Zeichenfolge an, die aus 8 hexadezimalen Ziffern gefolgt von einem Bindestrich und dann drei Gruppen von vier hexadezimalen Ziffern gefolgt von einem Bindestrich und dann 12 hexadezimal Ziffern besteht. Sie können die UUID-Zeichenfolge in Anführungszeichen einschließen, es sei denn, Sie verwenden den Mittel l-Compilerschalter [**/OSF**](-osf.md).

</dd> <dt>

*Interface-Attribute-List* 
</dt> <dd>

Gibt eine Liste von 0 (null) oder mehr IDL-Attributen an, die auf die gesamte Schnittstelle angewendet werden. Wenn zwei oder mehr Schnittstellen Attribute vorhanden sind, müssen diese durch Kommas getrennt werden.

</dd> <dt>

*Schnittstellen Name* 
</dt> <dd>

Der Name der Schnittstelle.

</dd> <dt>

*Basisschnittstelle* 
</dt> <dd>

Gibt den Namen einer Schnittstelle an, von der diese abgeleitete Schnittstelle Member-Funktionen, Statuscodes und Schnittstellen Attribute erbt. Die abgeleitete Schnittstelle erbt keine Typdefinitionen. Verwenden Sie hierzu das Schlüsselwort [**Import**](import.md) , um die IDL-Datei der Basisschnittstelle zu importieren.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Durch die Verwendung des \[ **Proxy** \] Attributs für eine duale Schnittstelle wird verhindert, dass der TLB generierte stubfunktionen übernimmt. Wenn dieses Attribut angegeben wird, sollte die Registrierung des Export der Typbibliothek-Proxys nicht aufgehoben werden, wenn die Registrierung des Export der Typbibliothek aufgehoben wird.

### <a name="flags"></a>Flags

<dl> <dt>

<span id="TYPEFLAG_PROXY"></span><span id="typeflag_proxy"></span>TYPEFLAG- \_ Proxy
</dt> <dd>

Schnittstellen können mit dem TYPEFLAG \_ -ProxyFlag gekennzeichnet werden, um anzugeben, dass Sie eine Proxy-/Stub-Dynamic Link Library verwenden werden. Dieses Flag gibt an, dass die Registrierung des Export der Typbibliothek-Proxys nicht aufgehoben werden soll, wenn die Registrierung der Typbibliothek aufgehoben

</dd> </dl>

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Erstellen einer Typbibliothek mit "Mittel l"**](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Ales**](dual.md)
</dt> <dt>

[**FUNCFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 