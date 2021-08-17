---
title: Quellattribut
description: Das Attribut \source\ gibt an, dass ein Member einer Co-Klasse, Eigenschaft oder Methode eine Quelle von Ereignissen ist. Für einen Member einer Co-Klasse bedeutet dieses Attribut, dass der Member aufgerufen und nicht implementiert wird.
ms.assetid: fbd5411a-e614-4643-810a-f3765e7ec16d
keywords:
- Quellattribut MIDL
topic_type:
- apiref
api_name:
- source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08f7039505846d7a35bbd0e077456905c0d29ad13be398fe673ca5c1f8da25e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066680"
---
# <a name="source-attribute"></a>Quellattribut

Das **\[ \] Quellattribut** gibt an, dass ein Member einer [**Co-Klasse,**](coclass.md)-Eigenschaft oder -Methode eine Quelle von Ereignissen ist. Für einen Member einer **Co-Klasse** bedeutet dieses Attribut, dass der Member aufgerufen und nicht implementiert wird.

``` syntax
[
    coclass-attributes
]
coclass coclass-name
{
    [source [, optional-attributes] ] statement-type statement-name; 
  [, ...]
}

[source] object-type function-name(optional-parameter-list);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*coclass-attributes* 
</dt> <dd>

Null oder mehr Attribute, die auf die [**Co-Klasse**](coclass.md)angewendet werden.

</dd> <dt>

*coclass-name* 
</dt> <dd>

Der Namensbezeichner der [**Co-Klasse**](coclass.md).

</dd> <dt>

*optionale Attribute* 
</dt> <dd>

Null oder mehr MIDL-Attribute.

</dd> <dt>

*Anweisungstyp* 
</dt> <dd>

Kann [**interface**](interface.md) oder [**dispinterface**](dispinterface.md)sein.

</dd> <dt>

*Anweisungsname* 
</dt> <dd>

Der Name der [**Schnittstelle**](interface.md) oder [**Disp-Schnittstelle.**](dispinterface.md)

</dd> <dt>

*Objekttyp* 
</dt> <dd>

Der Typ des Objekts, das von der Methode zurückgegeben wird. Dieses Objekt ist eine Quelle von Ereignissen.

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Der Name einer Methode in einer [**Schnittstelle**](interface.md) oder [**Disp-Schnittstelle.**](dispinterface.md)

</dd> <dt>

*optional-parameter-list* 
</dt> <dd>

Null oder mehr Methodenparameter.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Bei einer Eigenschaft oder Methode gibt das **\[ \] Quellattribut** an, dass der Member ein Objekt oder variant zurückgibt, das eine Quelle von Ereignissen ist. Das -Objekt implementiert **IConnectionPointContainer.**

### <a name="flags"></a>Flags

IMPLTYPEFLAG \_ FSOURCE, VARFLAG \_ SOURCE, FUNCFLAG \_ SOURCE

## <a name="examples"></a>Beispiele

``` syntax
[default, source] dispinterface DIMyFaceAdviseSink;
[source]interface IMyFaceAdviseSink;
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[**Dispatchschnittstelle**](dispinterface.md)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Schnittstelle**](interface.md)
</dt> <dt>

[BEISPIEL FÜR ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Typeflags](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 