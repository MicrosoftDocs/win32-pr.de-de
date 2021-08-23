---
title: nonbrowsable-Attribut
description: Verwenden Sie das Attribut \nonbrowsable\, um eine Schnittstelle oder einen Dispinterface-Member zu markieren, die nicht in einem Eigenschaftenbrowser angezeigt werden sollen.
ms.assetid: 94e868cc-8d9c-4b8a-ac18-1ea513a103da
keywords:
- MIDL-Attribut, das nicht browsbar ist
topic_type:
- apiref
api_name:
- nonbrowsable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b6349683c3a3c591752036d9a5e2995d368460a049a79d2e1cf4123beb2b0ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066950"
---
# <a name="nonbrowsable-attribute"></a>nonbrowsable-Attribut

Verwenden Sie **\[ das \] nicht durchbrowsbare Attribut,** um eine Schnittstelle oder einen Dispinterface-Member zu markieren, die nicht in einem Eigenschaftenbrowser angezeigt werden sollen.

``` syntax
[property-attribute-list, nonbrowsable]return-type property-name(prop-param-list)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*property-attribute-list* 
</dt> <dd>

Andere Attribute, die für die Eigenschaft gelten.

</dd> <dt>

*return-type* 
</dt> <dd>

Der Typ der von der -Methode zurückgegebenen Daten.

</dd> <dt>

*Eigenschaftenname* 
</dt> <dd>

Der Name der Eigenschaft oder Methode.

</dd> <dt>

*prop-param-list* 
</dt> <dd>

Null oder mehr Parameter, die an die Methode übergeben werden sollen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Bestimmte Eigenschaften sollten nicht in einem Eigenschaftenbrowser angezeigt werden. Dies kann daran liegt, dass das Abrufen des Werts sehr lange dauern würde. Im Beispiel wird verhindert, dass der Benutzer versucht, die *Count-Eigenschaft* abzurufen, die die Anzahl der Zeilen im Dynaset zurückgibt. Diese Zahl kann die Ergebnisse einer sehr großen Abfrage darstellen.

Andere Eigenschaften können unerwartete Auswirkungen auf den Browser haben. Betrachten Sie beispielsweise ein Steuerelement mit der Eigenschaft "IsSelected", um zu bestimmen, ob das Steuerelement ausgewählt ist. Wenn "IsSelected" auf FALSE festgelegt ist, durchsucht ein auswahlbasierter Eigenschaftenbrowser ein anderes Objekt.

Beachten Sie, dass eine Eigenschaft, die **\[ als nicht browsbar \]** gekennzeichnet ist, weiterhin in einem Objektbrowser angezeigt wird, der keine Eigenschaftswerte enthält.

### <a name="typeflag-representation"></a>Typflagdarstellung

Das Vorhandensein von FUNCFLAG \_ FNONBROWSABLE oder VARFLAG \_ FNONBROWSABLE.

## <a name="examples"></a>Beispiele

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IDynaset:IDispatch
{
    [propget, nonbrowsable]HRESULT Count([out, retval] long *Value);
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL-Dateibeispiel](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 