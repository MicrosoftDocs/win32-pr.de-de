---
title: propput-Attribut
description: Das \propput\-Attribut gibt eine Eigenschaftseinstellungsfunktion an. Die Eigenschaft muss den gleichen Namen wie die Funktion aufweisen.
ms.assetid: ffd8af15-42a4-4852-a29b-1fc66f673978
keywords:
- Propput-Attribut MIDL
topic_type:
- apiref
api_name:
- propput
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f0e34d4826abfa2df6cd1262ccd4bcec04344f4500ddf5c146816d23f6261c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641933"
---
# <a name="propput-attribute"></a>propput-Attribut

Das **\[ \] Propput-Attribut** gibt eine Eigenschaftseinstellungsfunktion an. Die -Eigenschaft muss den gleichen Namen wie die Funktion *aufweisen.*

``` syntax
[propput [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*optional-property-attributes* 
</dt> <dd>

Null oder mehr Eigenschaftsattribute.

</dd> <dt>

*rückgabetyp* 
</dt> <dd>

Der Typ der von der Remoteprozedur zurückgegebenen Daten.

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Der Name der Remoteprozedur.

</dd> <dt>

*parameters* 
</dt> <dd>

Null oder mehr Parameter für die Remoteprozedur.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Eine Funktion, die über das **\[ \] Propput-Attribut** verfügt, muss als letzter Parameter auch einen Parameter mit dem **\[** [**in-Attribut**](in.md) **\]** aufweisen.

Höchstens eines von **\[** [**propget,**](propget.md) **\]** **\[ propput \]** und **\[** [**propputref**](propputref.md) kann für eine Funktion angegeben **\]** werden.

Wenn das **\[** [**lcid-Attribut**](lcid.md) **\]** in der Parameterliste einer Funktion verwendet wird, die einen Parameter mit dem **\[ propput-Attribut \]** enthält, muss der **\[ lcid-Parameter \]** vor dem letzten Parameter liegen.

### <a name="flags"></a>Flags

INVOKE \_ PROPERTYPUT

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

[Unterschiede zwischen MIDL und MKTYPLIB](differences-between-midl-and-mktyplib.md)
</dt> <dt>

[BEISPIEL FÜR ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**Propputref**](propputref.md)
</dt> <dt>

[**Typeflags**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 