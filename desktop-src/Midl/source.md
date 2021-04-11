---
title: Quellattribut
description: Das Attribut \ Source \ gibt an, dass ein Member einer Co-Klasse, einer Eigenschaft oder Methode eine Quelle von Ereignissen ist. Bei einem Member einer Co-Klasse bedeutet dieses Attribut, dass der Member aufgerufen wird, anstatt implementiert zu werden.
ms.assetid: fbd5411a-e614-4643-810a-f3765e7ec16d
keywords:
- Quell Attribut-Mittel l
topic_type:
- apiref
api_name:
- source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 621e97fd20b6b96d275044dc7cbe701faee29712
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948616"
---
# <a name="source-attribute"></a>Quellattribut

Das **\[ Source \]** -Attribut gibt an, dass ein Member einer [**Co-Klasse**](coclass.md), einer Eigenschaft oder Methode eine Quelle von Ereignissen ist. Bei einem Member einer **Co-Klasse** bedeutet dieses Attribut, dass der Member aufgerufen wird, anstatt implementiert zu werden.

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

*coclass-Attribute* 
</dt> <dd>

0 (null) oder mehr Attribute, die auf die [**Co-Klasse**](coclass.md)angewendet werden.

</dd> <dt>

*Name der Co-Klasse* 
</dt> <dd>

Der namens Bezeichner der [**Co-Klasse**](coclass.md).

</dd> <dt>

*optionale Attribute* 
</dt> <dd>

NULL oder mehr mittlere Attribute.

</dd> <dt>

*Anweisungstyp* 
</dt> <dd>

Kann " [**Interface**](interface.md) " oder " [**dispinterface**](dispinterface.md)" sein.

</dd> <dt>

*Anweisungs Name* 
</dt> <dd>

Der Name der [**Schnittstelle**](interface.md) oder der [**dispinterface**](dispinterface.md).

</dd> <dt>

*Objekttyp* 
</dt> <dd>

Der Typ des Objekts, das von der Methode zurückgegeben wird. Dieses Objekt ist eine Quelle von Ereignissen.

</dd> <dt>

*function-name* 
</dt> <dd>

Der Name einer Methode in einer [**Schnittstelle**](interface.md) oder einer [**dispinterface**](dispinterface.md).

</dd> <dt>

*Optional-Parameter-List* 
</dt> <dd>

NULL oder mehr Methoden Parameter.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Bei einer Eigenschaft oder Methode gibt das **\[ Quell \]** Attribut an, dass der Member ein Objekt oder eine Variante zurückgibt, das eine Quelle von Ereignissen ist. Das Objekt implementiert **IConnectionPointContainer**.

### <a name="flags"></a>Flags

impltypeflag \_ f Source, varflag \_ Source, funcflag \_ Source

## <a name="examples"></a>Beispiele

``` syntax
[default, source] dispinterface DIMyFaceAdviseSink;
[source]interface IMyFaceAdviseSink;
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**berfläche**](interface.md)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[FUNCFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 