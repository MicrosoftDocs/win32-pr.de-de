---
title: propput-Attribut
description: Das Attribut \ propput \ gibt eine Eigenschafts Einstellungs Funktion an. Die-Eigenschaft muss den gleichen Namen wie die Funktion aufweisen.
ms.assetid: ffd8af15-42a4-4852-a29b-1fc66f673978
keywords:
- propput-Attribut-Mittel l
topic_type:
- apiref
api_name:
- propput
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79bf5520a3f4f4872801145064f49a8108cf602a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101502"
---
# <a name="propput-attribute"></a>propput-Attribut

Das **\[ PROPPUT \]** -Attribut gibt eine Eigenschafts Einstellungs Funktion an. Die-Eigenschaft muss den gleichen Namen wie die Funktion aufweisen *.*

``` syntax
[propput [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*optionale-Property-Attribute* 
</dt> <dd>

NULL oder mehr Eigenschafts Attribute.

</dd> <dt>

*Rückgabetyp* 
</dt> <dd>

Der Typ der Daten, die von der Remote Prozedur zurückgegeben werden.

</dd> <dt>

*function-name* 
</dt> <dd>

Der Name der Remote Prozedur.

</dd> <dt>

*parameters* 
</dt> <dd>

NULL oder mehr Parameter für die Remote Prozedur.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Eine Funktion, die über das **\[ PROPPUT \]** -Attribut verfügt, muss ebenfalls als letzten Parameter einen Parameter haben, der das **\[** [**in**](in.md) - **\]** Attribut aufweist.

**\[** Für eine Funktion kann höchstens ein [**propget**](propget.md) **\]** -, **\[ PROPPUT \]** -und **\[** [**PROPPUTREF**](propputref.md) -Konstruktor **\]** angegeben werden.

Wenn das **\[** [**LCID**](lcid.md) - **\]** Attribut in der Parameterliste einer Funktion verwendet wird, die einen Parameter mit dem **\[ PROPPUT \]** -Attribut enthält, muss der **\[ LCID \]** -Parameter den Wert Second bis The Last aufweisen.

### <a name="flags"></a>Flags

\_PropertyPut aufrufen

## <a name="examples"></a>Beispiele

``` syntax
interface InMyFace : IDispatch                         
{
    [propget, 
     helpstring("A meaningful comment.")] HRESULT Method1(
         [out, retval] int* ReturnVal); 

    [propput, 
     helpstring("Another meaningful comment.")] HRESULT Method1(
         [in] int Value);
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Unterschiede zwischen "Mittel l" und "MkTypLib"](differences-between-midl-and-mktyplib.md)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**FUNCFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 