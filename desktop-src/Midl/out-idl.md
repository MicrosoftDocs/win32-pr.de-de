---
title: out-Attribut
description: Das \out\-Attribut identifiziert Zeigerparameter, die von der aufgerufenen Prozedur an die aufrufende Prozedur (vom Server zum Client) zurückgegeben werden.
ms.assetid: f92ef78a-321b-460e-a18a-b63a5e199ad0
keywords:
- out-Attribut MIDL
topic_type:
- apiref
api_name:
- out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32bdbd18c6412f943a124a62badb9c154fa9aeb64573919970ffc1dc4af17798
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066800"
---
# <a name="out-attribute"></a>out-Attribut

Das \[ **out-Attribut** identifiziert Zeigerparameter, die von der aufgerufenen Prozedur an die aufrufende Prozedur (vom Server zum \] Client) zurückgegeben werden.

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ out [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*function-attribute-list* 
</dt> <dd>

Gibt null oder mehr Attribute an, die für die Funktion gelten. Gültige Funktionsattribute sind rückruf , local, das \[ [](callback.md) \] \[ [](local.md) \] Zeigerattribut \[ [**ref,**](ref.md)unique oder ptr und die \] \[ [](unique.md) \] \[ [](ptr.md) \] Verwendungsattribute \[ [](string.md) \] \[ [](ignore.md) \] \[ [**\_**](context-handle.md) \] Zeichenfolge , ignorieren und Kontexthand handle .

</dd> <dt>

*Typspezifizierer* 
</dt> <dd>

Gibt einen [ \_ Basistyp, eine](midl-base-types.md) [**Struktur,**](struct.md)eine [**Union**](union.md)oder einen [**enum-Typ**](enum.md) oder Typbezeichner an. Eine optionale Speicherspezifikation kann dem *Typspezifizierer vorangestellt werden.*

</dd> <dt>

*Zeigerdeklarator* 
</dt> <dd>

Gibt null oder mehr Zeigerdeklaratoren an. Ein Zeigerdeklarator ist mit dem in C verwendeten Zeigerdeklarator identisch. sie wird aus dem \* Designator, Modifizierern wie **far** und dem Qualifizierer [**const erstellt.**](const.md)

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Gibt den Namen der Remoteprozedur an.

</dd> <dt>

*parameter-attribute-list* 
</dt> <dd>

Gibt null oder mehr Attribute an, die für einen angegebenen Parametertyp geeignet sind. Parameterattribute mit dem out-Attribut können auch das direktionale Attribut heraus nehmen. Die Feldattribute sind zuerst , last ist , length ist , max ist , size ist und switch type; das Zeigerattribut ref, unique oder ptr sowie das Kontexthand handle und die Zeichenfolge der \[  \] \[  \] \[ [**\_**](first-is.md) \] \[ [**\_**](last-is.md) \] \[ [**\_**](length-is.md) \] \[ [**\_**](max-is.md) \] \[ [**\_**](size-is.md) \] \[ [**\_**](switch-type.md) \] \[ [](ref.md) \] \[ [](unique.md) \] \[ [](ptr.md) \] Verwendungsattribute. \[ [**\_**](context-handle.md) \] \[ [](string.md) \] Das ignorierte \[ [**Verwendungsattribut**](ignore.md) \] kann nicht als Parameterattribut verwendet werden. Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*Deklarator* 
</dt> <dd>

Gibt die Standarddeklaratoren an, z. B. Bezeichner, Zeigerdeklaratoren und Arraydeklaratoren. Weitere Informationen finden Sie unter [Array- und Sized-Pointer Attribute,](array-and-sized-pointer-attributes.md) [**Arrays**](arrays-1.md)und [Arrays und Zeiger.](/windows/desktop/Rpc/arrays-and-pointers) Der Parameterdeklarator im Funktionsdeklarator, z. B. der Parametername, ist optional.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das out-Attribut gibt an, dass ein Parameter, der als Zeiger fungiert, und die zugehörigen Daten im Arbeitsspeicher von der aufgerufenen Prozedur an die aufrufende \[  \] Prozedur zurückübergibt werden sollen.

Das \[  \] out-Attribut muss ein Zeiger sein. DCE-IDL-Compiler erfordern das Vorhandensein eines expliziten \* als Zeigerdeklarator in der Parameterdeklaration. Microsoft IDL bietet eine Erweiterung, die diese Anforderung löscht und ein Array oder einen zuvor definierten Zeigertyp zulässt.

Ein verwandtes Attribut in gibt an, dass der Parameter von der aufrufenden Prozedur an \[ [](in.md) \] die aufgerufene Prozedur übergeben wird. Die \[ **Attribute in** \] und \[ **out** geben die \] Richtung an, in der die Parameter übergeben werden. Ein Parameter kann als \[ **in** \] -only, \[ **out** \] -only oder in \[ **,** out definiert **werden.** \]

Es wird davon ausgegangen, dass ein out-only-Parameter nicht definiert ist, wenn die Remoteprozedur aufgerufen wird und der Arbeitsspeicher für das Objekt \[  \] vom Server zugeordnet wird. Da Zeiger/Parameter der obersten Ebene immer auf gültigen Speicher verweisen müssen und daher nicht **NULL** sein dürfen, kann out nicht auf eindeutige zeiger der obersten Ebene oder \[  \] \[ [](unique.md) \] \[ [**ptr-Zeiger**](ptr.md) \] angewendet werden. Parameter, die \[ **eindeutige oder** \] \[ **ptr-Zeiger** sind, müssen sich entweder in oder in \] \[ [](in.md) \] \[ **out-Parametern**  \] befinden.

## <a name="examples"></a>Beispiele

``` syntax
HRESULT MyFunction([out] short * pcount);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Arrays**](arrays-1.md)
</dt> <dt>

[MIDL-Basistypen](midl-base-types.md)
</dt> <dt>

[**Rückruf**](callback.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**Kontexthand \_ handle**](context-handle.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[**first \_ is**](first-is.md)
</dt> <dt>

[**Ignorieren**](ignore.md)
</dt> <dt>

[**In**](in.md)
</dt> <dt>

[**last \_ is**](last-is.md)
</dt> <dt>

[**length \_ ist**](length-is.md)
</dt> <dt>

[**lokal**](local.md)
</dt> <dt>

[**max \_ is**](max-is.md)
</dt> <dt>

[**Ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**size \_ ist**](size-is.md)
</dt> <dt>

[**Schnur**](string.md)
</dt> <dt>

[**Struktur**](struct.md)
</dt> <dt>

[**\_switch-Typ**](switch-type.md)
</dt> <dt>

[**Union**](union.md)
</dt> <dt>

[**Einzigartige**](unique.md)
</dt> </dl>

 

 