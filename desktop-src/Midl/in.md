---
title: in-Attribut
description: Das \in\-Attribut gibt an, dass ein Parameter von der aufrufenden Prozedur an die aufgerufene Prozedur übergeben werden soll.
ms.assetid: 85d5617e-8b73-449a-9627-2c8d5ab2b629
keywords:
- im MIDL-Attribut
topic_type:
- apiref
api_name:
- in
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb78ad08dd5ba5494181d3fb2adecb7a8441e4716c42ba6cd4f1c119b3ccb046
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067230"
---
# <a name="in-attribute"></a>in-Attribut

Das **\[ \] in-Attribut** gibt an, dass ein Parameter von der aufrufenden Prozedur an die aufgerufene Prozedur übergeben werden soll.

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ in [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*function-attribute-list* 
</dt> <dd>

Gibt null oder mehr Attribute an, die für die Funktion gelten. Gültige Funktionsattribute sind **\[ \] rückruf,** **\[ \] local,** das Zeigerattribut **\[ ref, \]** **\[ eindeutig \]** oder **\[ ptr \]** und die Verwendungsattribute **\[ Zeichenfolge \]**, **\[ ignorieren \]** und **\[ \_ Kontexthandle \]**.

</dd> <dt>

*Typspezifizierer* 
</dt> <dd>

Gibt einen **\_ Basistyp,** [**eine Struktur,**](struct.md) [**einen Union-**](union.md)oder [**Enumerationstyp**](enum.md) oder einen Typbezeichner an. Eine optionale Speicherspezifikation kann dem *Typspezifizierer* vorangestellt werden.

</dd> <dt>

*Zeigerdeklarator* 
</dt> <dd>

Gibt null oder mehr Zeigerdeklaratoren an. Ein Zeigerdeklarator entspricht dem in C verwendeten Zeigerdeklarator. sie wird aus dem \* Bezeichner, Modifizierern wie **far** und dem Qualifizierer [**const**](const.md)erstellt.

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Gibt den Namen der Remoteprozedur an.

</dd> <dt>

*parameter-attribute-list* 
</dt> <dd>

Gibt null oder mehr Attribute an, die für den angegebenen Parametertyp geeignet sind. Parameterattribute mit dem **\[ in-Attribut \]** können auch das direktionale Attribut **\[ \] herausnehmen.** Die Feldattribute **\[ sind zuerst \_ \]**, die letzte **\[ \_ ist \]**, die Länge ist , max **\[ \_ \]** **\[ \_ ist \]**, die Größe **\[ \_ ist \]** und der **\[ \_ Switchtyp, \]** das Zeigerattribut **\[ ref \]**, **\[ eindeutig \]** oder **\[ ptr; \]** und das **\[ \_ Kontexthandle \]** der Verwendungsattribute und die **\[ Zeichenfolge \]**. Das Verwendungsattribut **\[ ignore \]** kann nicht als Parameterattribut verwendet werden. Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*Deklarator* 
</dt> <dd>

Gibt C-Standarddeklaratoren an, z. B. Bezeichner, Zeigerdeklaratoren und Arraydeklaratoren. Weitere Informationen finden Sie unter [Array- und Sized-Pointer Attribute,](array-and-sized-pointer-attributes.md) [**Arrays**](arrays-1.md)und [Arrays und Zeiger.](/windows/desktop/Rpc/arrays-and-pointers) Der Parameterdeklarator im Funktionsdeklarator, z. B. der Parametername, ist optional.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das **\[ \] in-Attribut** verfügt über das umgekehrte Attribut **\[** [**out,**](out-idl.md) **\]** das angibt, dass ein Parameter von der aufgerufenen Prozedur an die aufrufende Prozedur zurückgegeben werden soll. Die **\[ In- \]** und **\[ Out-Attribute \]** werden als Richtungsparameterattribute bezeichnet, da sie die Richtung angeben, in der Parameter übergeben werden. Ein Parameter kann als **\[ in \]**, **\[ out \]** oder **\[ in**, **out \]** definiert werden.

Das **\[ attribut in \]** identifiziert Parameter, die vom Clientstub für die Übertragung an den Server gemarshallt werden.

Das **\[ \] in-Attribut** wird standardmäßig auf einen Parameter angewendet, wenn kein direktionales Parameterattribut angegeben wird.

## <a name="examples"></a>Beispiele

``` syntax
HRESULT MyFunction([in] short count);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**midl \_ user \_ allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[**out**](out-idl.md)
</dt> </dl>

 

 