---
title: async_uuid-Attribut
description: Das Attribut "\ Async \_ UUID \ Interface" weist den Mittel l-Compiler an, sowohl synchrone als auch asynchrone Versionen einer COM-Schnittstelle zu definieren.
ms.assetid: 1c20eaa1-78b5-4463-a8c1-d81e55d5c618
keywords:
- Async_uuid Attribut-Mittel l
topic_type:
- apiref
api_name:
- async_uuid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39fd7b4d9d9bf7a595415e55de778a419d91051c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101534"
---
# <a name="async_uuid-attribute"></a>Async- \_ uuid-Attribut

Das asynchrone **\[ \_ UUID \]** -Schnittstellen Attribut weist den Mittel l-Compiler an, sowohl synchrone als auch asynchrone Versionen einer COM-Schnittstelle zu definieren.

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

*String-uuid1* 
</dt> <dd>

Eine UUID-Zeichenfolge, die vom Hilfsprogramm uuidgen generiert wird und die synchrone Version der Schnittstelle identifiziert.

</dd> <dt>

*String-uuid2* 
</dt> <dd>

Eine UUID-Zeichenfolge, die vom Hilfsprogramm uuidgen generiert wird und die asynchrone Version der Schnittstelle identifiziert.

</dd> <dt>

*Interface-Attribute-List* 
</dt> <dd>

Andere Attribute, die auf die Schnittstelle als Ganzes angewendet werden. Sie können das [**\[ Versions \]**](version.md) Attribut nicht in einer COM-Schnittstelle verwenden.

</dd> <dt>

*Schnittstellen Name* 
</dt> <dd>

Der Name der Schnittstelle.

</dd> <dt>

*Basisschnittstelle* 
</dt> <dd>

Die Schnittstelle, von der diese Schnittstelle abgeleitet ist. Die Basisschnittstelle muss **IUnknown** oder eine asynchrone Schnittstelle sein, die entweder direkt oder indirekt von **IUnknown** abgeleitet ist.

</dd> <dt>

*Schnittstellen Definition* 
</dt> <dd>

Gibt IDL-Anweisungen an, die die Definition der-Schnittstelle bilden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Verwendung dieses Attributs erfordert Windows 2000 oder höhere Versionen von Windows.

Wenn Sie das asynchrone **\[ \_ UUID \]** -Attribut auf eine COM-Schnittstelle (d. h. eine Schnittstelle mit dem [**\[ Object \]**](object.md) -Attribut) anwenden, generiert der-compilercompiler zusätzlich zur herkömmlichen, synchronen Version eine asynchrone Definition der-Schnittstelle. Die asynchrone Schnittstelle hat dieselben Namen wie die synchrone Schnittstelle, jedoch mit einem Präfix "Async". Der Schnittstellen Bezeichner (IID) ist die UUID, die als Parameter für das asynchrone **\[ \_ UUID \]** -Attribut angegeben wird.

Bei der asynchronen-Schnittstelle teilt die Mittel l jede Methode in separate *Begin* -und *Finish* -Methoden auf. Die *Begin* -Methode verfügt über den synchronen Methodennamen mit dem \_ Präfix "BEGIN" und enthält alle [**\[ in \]**](in.md) -Parameter der synchronen Methode. Die " *Finish* "-Methode hat den Namen der synchronen Methode mit einem \_ Präfix "Finish" und enthält alle [**\[ out \]**](out-idl.md) -Parameter aus der synchronen Methode. Wenn die synchrone Methode über eine **\[ in- \] , out** -Parameter verfügt, werden Sie in die asynchronen *Begin* -und *Finish* -Methoden eingeschlossen.

Wenn eine asynchrone Schnittstellen Methode über den Befehl [**\[ \_ als \]**](call-as.md) Attribut verfügt, generiert die Mittel-l Deklarationen für die *Begin* -und die *Finish* -Methode. Beide Methoden müssen implementiert werden.

Jede asynchrone Schnittstelle ist ein Modifizierer in einer synchronen Schnittstelle und verfügt daher nicht über ein separates Vererbungs Diagramm. Dies bedeutet, dass Sie keine synchrone Schnittstelle von einer asynchronen Schnittstelle (außer **IUnknown**) definieren können. Und können keine synchronen Schnittstellen von asynchronen Schnittstellen erben. Der mittlerer l-Compiler gibt eine Fehlermeldung aus, wenn Sie eine der beiden Versuche ausführen.

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

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**aufzurufen \_ als**](call-as.md)
</dt> <dt>

[**IID \_ ist**](iid-is.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[**nah**](local.md)
</dt> <dt>

[**Objekt (object)**](object.md)
</dt> <dt>

[**vorgenommen**](out-idl.md)
</dt> <dt>

[**version**](version.md)
</dt> </dl>

 

 