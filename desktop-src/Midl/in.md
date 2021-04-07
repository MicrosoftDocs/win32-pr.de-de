---
title: in-Attribut
description: Das Attribut \ in \ gibt an, dass ein Parameter von der aufrufenden Prozedur an die aufgerufene Prozedur übergeben werden soll.
ms.assetid: 85d5617e-8b73-449a-9627-2c8d5ab2b629
keywords:
- in attributmittell
topic_type:
- apiref
api_name:
- in
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b606a834b394197960777fa485d112a94212ec45
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726968"
---
# <a name="in-attribute"></a>in-Attribut

Das **\[ in \]** -Attribut gibt an, dass ein Parameter von der aufrufenden Prozedur an die aufgerufene Prozedur übergeben werden soll.

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ in [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Function-Attribute-List* 
</dt> <dd>

Gibt 0 (null) oder mehr Attribute an, die für die Funktion gelten. Gültige Funktions Attribute sind **\[ Callback \]**, **\[ local \]**, das Zeiger Attribut **\[ ref \]**, **\[ Unique \]** oder **\[ ptr \]** und die Verwendungs Attribute **\[ Zeichenfolge \]**, **\[ Ignore \]** und **\[ Kontext \_ handle \]**.

</dd> <dt>

*Typspezifizierer* 
</dt> <dd>

Gibt einen **\_ Basistyp**, eine [**Struktur**](struct.md), eine [**Union**](union.md)oder einen Aufzählungstyp [**oder einen**](enum.md) Typbezeichner an. Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden.

</dd> <dt>

*Zeiger-Deklarator* 
</dt> <dd>

Gibt 0 (null) oder mehr Zeiger Deklaratoren an. Ein zeigerdeklarator ist derselbe wie der in C verwendete zeigerdeklarator. Sie wird aus dem Kenn \* Zeichner, den Modifizierern, z. b. **weit**, und dem Qualifizierer " [**Konstanten**](const.md)" erstellt.

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Remote Prozedur an.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

Gibt NULL oder mehr Attribute an, die für den angegebenen Parametertyp geeignet sind. Parameter Attribute mit dem **\[ in \]** -Attribut können auch **\[ \]** das **\[ \]** **\[ \]** direktionale Attribut übernehmen. die **\[ \]** **\[ \_ \]** Feld Attribute **\[ \_ sind \] zuerst** **\[ \_ \]** **\[ \_ \]** **\[ \_ \]** **\[ \]**, "Last", "length", "Max is", "size" und "Switch Type", das Zeiger Attribut "ref", "Unique" oder "PTR" und das **\[ Kontext \_ handle \]** für Verwendungs Attribute **\[ \_ \]** Das Usage-Attribut " **\[ Ignore \]** " kann nicht als Parameter Attribut verwendet werden. Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*Deklarator* 
</dt> <dd>

Gibt Standard-C-Deklaratoren an, z. b. Bezeichner, Zeiger Deklaratoren und Array Deklaratoren. Weitere Informationen finden Sie unter [Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**Arrays**](arrays-1.md)und [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers). Der parameterdeklarator im funktionsdedeclarator (z. b. der Parameter Name) ist optional.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das **\[ in \]** -Attribut verfügt über ein umgekehrter Attribut, **\[** [](out-idl.md) **\]** das angibt, dass ein Parameter von der aufgerufenen Prozedur an die aufrufende Prozedur zurückgegeben werden soll. Die Attribute " **\[ in \]** " und " **\[ out \]** " werden als direktionale Parameter Attribute bezeichnet, da Sie die Richtung angeben, in der Parameter übergeben werden. Ein Parameter kann als " **\[ in \]**", " **\[ out \]**" oder " **\[ in**" oder " **out \]**" definiert werden.

Das **\[ in \]** -Attribut identifiziert Parameter, die vom Clientstub für die Übertragung an den Server gemarshallt werden.

Das **\[ in \]** -Attribut wird standardmäßig auf einen Parameter angewendet, wenn kein direktionales Parameter Attribut angegeben wird.

## <a name="examples"></a>Beispiele

``` syntax
HRESULT MyFunction([in] short count);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**mittlere Benutzer Zuordnungen \_ \_**](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[**vorgenommen**](out-idl.md)
</dt> </dl>

 

 