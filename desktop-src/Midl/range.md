---
title: Bereichsattribut
description: Mit dem Attribut \range\ können Sie einen Bereich von zulässigen Werten für Argumente oder Felder angeben, deren Werte zur Laufzeit festgelegt werden. Bei Verwendung mit einem Pipetyp gibt das -Attribut den zulässigen Bereich für die Anzahl der Elemente in den Pipesegmenten an.
ms.assetid: 1609fea5-e82c-4389-b4f4-2cd8d0622cde
keywords:
- Range-Attribut MIDL
topic_type:
- apiref
api_name:
- range
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8be59ef1b212d0f6953063ce7ac3239d8940a5ea54a623990fc3d7af9f36ad3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764310"
---
# <a name="range-attribute"></a>Bereichsattribut

Mit **\[ dem \] Bereichsattribut** können Sie einen Bereich von zulässigen Werten für Argumente oder Felder angeben, deren Werte zur Laufzeit festgelegt werden. Bei Verwendung mit einem Pipetyp gibt das -Attribut den zulässigen Bereich für die Anzahl der Elemente in den Pipesegmenten an.

``` syntax
[range(low-val,high-val)] type-specifier declarator
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*low-val* 
</dt> <dd>

Der niedrigste zulässige Wert, den der Parameter oder das Feld halten kann.

</dd> <dt>

*high-val* 
</dt> <dd>

Der höchste zulässige Wert, den der Parameter oder das Feld halten kann.

</dd> <dt>

*Typspezifizierer* 
</dt> <dd>

Ein integraler Typ, der nicht [**hyper**](hyper.md) oder [**\_ \_ int64**](--int64.md)ist, ein Typbezeichner für einen integralen Typ, einen [**enum-Typ**](enum.md) oder einen Pipetypnamen.

</dd> <dt>

*Deklarator* 
</dt> <dd>

Ein C-Standarddeklarator, z. B. ein Bezeichner.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Verwenden Sie das **\[ \]** Bereichsattribut, um die Bedeutung vertraulicher Parameter oder Felder zu ändern, z. B. diejenigen, die für Größe oder Länge verwendet werden, mit konformen oder variierenden Arrays oder immer dann, wenn Sie einen Parameter- oder Feldwert mit einem Bereich gültiger Werte überprüfen möchten. Das -Attribut gilt für Parameter der obersten Ebene sowie für Parameter und Felder auf niedrigerer Ebene. Das Hinzufügen **\[ des \] Bereichsattributs** zu einem Typ ändert das Wire-Format nicht und wirkt sich daher nicht auf die Abwärtskompatibilität aus.

Das **\[ \] Bereichsattribut** kann auch für konforme Daten wie Puffer oder Arrays mit einem Konformitätsattribut verwendet werden. Die Auswirkung besteht in der Beschränkung aller Übereinstimmungsgrößen für die konformen Daten auf den angegebenen Bereich. Wenn die konformen Daten ein mehrdimensionales Array sind, ist jede Arraydimension auf den angegebenen Bereich beschränkt.

Die Verwendung **\[ des Bereichs \]** für konforme Daten erfordert, dass das Kompilierungsziel "ZIEL NT60" oder höher ist.

Beachten Sie, dass Sie die Compileroption [**/robust**](-robust.md) verwenden müssen, wenn Sie Ihre IDL-Datei kompilieren, um den Stubcode zu generieren, der diese Überprüfungen ausführen soll. Ohne den **Schalter /robust** ignoriert der MIDL-Compiler dieses Attribut.

## <a name="examples"></a>Beispiele

``` syntax
HRESULT Method1(
    [in, range(0,100)] ULONG m,
    [in, range(0,100)] ULONG n,
    [size_is(m,n)] ULONG **pplong);

void InPipe(
    [in, range(0, MAX_CHUNK) LONG_PIPE pipe_date);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[Arrays](/windows/desktop/Rpc/arrays)
</dt> <dt>

[**first \_ is**](first-is.md)
</dt> <dt>

[**last \_ is**](last-is.md)
</dt> <dt>

[**length \_ ist**](length-is.md)
</dt> <dt>

[**max \_ is**](max-is.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> <dt>

[**size \_ ist**](size-is.md)
</dt> <dt>

[**switch \_ ist**](switch-is.md)
</dt> </dl>

 

 