---
title: async_uuid-Attribut
description: Das \_ Schnittstellenattribut \async uuid\ weist den MIDL-Compiler an, sowohl synchrone als auch asynchrone Versionen einer COM-Schnittstelle zu definieren.
ms.assetid: 1c20eaa1-78b5-4463-a8c1-d81e55d5c618
keywords:
- async_uuid-Attribut MIDL
topic_type:
- apiref
api_name:
- async_uuid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83a784cadf470fa312a82e473f3934dbda1a2b6dce20d2ae34c7074c309398cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808234"
---
# <a name="async_uuid-attribute"></a>asynchrones \_ uuid-Attribut

Das **\[ asynchrone \_ \] uuid-Schnittstellenattribut** weist den MIDL-Compiler an, sowohl synchrone als auch asynchrone Versionen einer COM-Schnittstelle zu definieren.

``` syntax
[ 
    object, 
    uuid(string-uuid1), 
    async_uuid(string-uuid2)[ [, interface-attribute-list] 
]
interface interface-name : base-interface
{
    interface-definition
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*string-uuid1* 
</dt> <dd>

Eine vom Hilfsprogramm Uuidgen generierte UUID-Zeichenfolge, die die synchrone Version der Schnittstelle identifiziert.

</dd> <dt>

*string-uuid2* 
</dt> <dd>

Eine vom Hilfsprogramm Uuidgen generierte UUID-Zeichenfolge, die die asynchrone Version der Schnittstelle identifiziert.

</dd> <dt>

*interface-attribute-list* 
</dt> <dd>

Andere Attribute, die für die gesamte Schnittstelle gelten. Sie können das [**\[ \] Versionsattribut**](version.md) nicht in einer COM-Schnittstelle verwenden.

</dd> <dt>

*Schnittstellenname* 
</dt> <dd>

Der Name der Schnittstelle.

</dd> <dt>

*Basisschnittstelle* 
</dt> <dd>

Die Schnittstelle, von der diese Schnittstelle abgeleitet wird. Die Basisschnittstelle muss **IUnknown** oder eine asynchrone Schnittstelle sein, die direkt oder indirekt von **IUnknown** abgeleitet wird.

</dd> <dt>

*Schnittstellendefinition* 
</dt> <dd>

Gibt IDL-Anweisungen an, die die Definition der Schnittstelle bilden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Verwendung dieses Attributs erfordert Windows Version 2000 oder höher von Windows.

Wenn Sie das **\[ async \_ \] uuid-Attribut** auf eine COM-Schnittstelle (d. h. eine Schnittstelle mit dem [**\[ \] -Objektattribut)**](object.md) anwenden, generiert der MIDL-Compiler zusätzlich zur herkömmlichen synchronen Version eine asynchrone Definition der Schnittstelle. Die asynchrone Schnittstelle hat die gleichen Namen wie die synchrone Schnittstelle, jedoch mit dem Präfix "Async". Der Schnittstellenbezeichner (INTERFACE Identifier, IID) ist die UUID, die als Parameter für das **\[ \_ async uuid-Attribut \]** angegeben wird.

Für die asynchrone Schnittstelle teilt MIDL jede Methode in separate *Begin-* und *Finish-Methoden* auf. Die *begin-Methode* hat den Namen der synchronen Methode mit dem \_ Präfix "Begin" und schließt alle [**\[ in \]**](in.md) -Parameter aus der synchronen Methode ein. Die *finish-Methode* hat den Namen der synchronen Methode mit dem \_ Präfix "Finish" und enthält alle [**\[ \] out-Parameter**](out-idl.md) der synchronen Methode. Wenn die synchrone Methode über einen **\[ in verfügt, \]** werden out-Parameter in die asynchronen *Methoden begin* und *finish* eingeschlossen.

Wenn eine asynchrone Schnittstellenmethode über den [**\[ Aufruf \_ als \]**](call-as.md) Attribut verfügt, generiert MIDL Deklarationen für die *Begin-* und *finish-Methoden.* Sie müssen beide Methoden implementieren.

Jede asynchrone Schnittstelle ist ein Modifizierer für eine synchrone Schnittstelle und verfügt daher nicht über ein separates Vererbungsdiagramm. Dies bedeutet, dass Sie keine synchrone Schnittstelle über eine asynchrone Schnittstelle definieren können (außer **IUnknown**). Synchrone Schnittstellen können auch nicht von asynchronen Schnittstellen erben. Der MIDL-Compiler gibt eine Fehlermeldung aus, wenn Sie eine der beiden Versuche versuchen.

## <a name="examples"></a>Beispiele

``` syntax
[
    object, 
    uuid(0c733a30-2a1c-11ce-ade5-00aa0044773d),
    async_uuid(1c733a30-2a1c-11ce-ade5-00aa0044773d),
    pointer_default(unique)
]
interface IMyInterface : IUnknown
{
    /* Interface definition goes here*/
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Definieren von COM-Schnittstellen](/windows/desktop/com/defining-com-interfaces)
</dt> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**aufrufen \_ als**](call-as.md)
</dt> <dt>

[**iid \_ ist**](iid-is.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[**lokal**](local.md)
</dt> <dt>

[**Objekt (object)**](object.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**Version**](version.md)
</dt> </dl>

 

 