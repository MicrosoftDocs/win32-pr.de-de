---
title: uidefault-Attribut
description: Das Attribut \uidefault\ gibt an, dass das Typinformationsmitglied das Standardmitglied für die Anzeige auf der Benutzeroberfläche ist.
ms.assetid: e789be38-a509-437d-89c9-ebbc830e5ae2
keywords:
- uidefault attribute MIDL
topic_type:
- apiref
api_name:
- uidefault
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 891d37611eb931a8857157434419e5221e808710290f2e209f50c743bcb5b7ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013478"
---
# <a name="uidefault-attribute"></a>uidefault-Attribut

Das **\[ uidefault-Attribut \]** gibt an, dass der Typinformations-Member das Standardmitglied für die Anzeige auf der Benutzeroberfläche ist.

``` syntax
[method-attribute-list, uidefault]return-type method-name(method-parameter-list)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*method-attribute-list* 
</dt> <dd>

Andere Attribute, die für die Methode gelten.

</dd> <dt>

*return-type* 
</dt> <dd>

Der Typ der Daten, die die Methode nach Abschluss der Ausführung zurücksendet.

</dd> <dt>

*Methodenname* 
</dt> <dd>

Der Name der Methode.

</dd> <dt>

*method-parameter-list* 
</dt> <dd>

Null oder mehr Parameter für die Methode.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das Anwenden **\[ des \] uidefault-Attributs** auf einen Member einer Schnittstelle oder einer Disp-Schnittstelle weist Visual Basic zur Entwurfszeit an, dem Benutzer dieses Ereignis oder diese Eigenschaft automatisch anzuzeigen. Dies bedeutet, dass beim Doppelklicken des Benutzers auf ein Objekt Visual Basic ereignis in der Standard-Quellschnittstelle mit dem **\[ uidefault-Attribut \] springt.** Wenn der Benutzer ein Objekt auswählt, Visual Basic Eigenschaftenbrowser von Visual Basic die Eigenschaft in der Standardquellenschnittstelle mit diesem Attribut angezeigt. Wenn kein Ereignis oder keine Eigenschaft über das **\[ \] uidefault-Attribut** verfügt, Visual Basic das erste Ereignis oder die erste Eigenschaft in der Standardschnittstelle angezeigt.

### <a name="typeflag-representation"></a>Typflagdarstellung

Das Vorhandensein von FUNCFLAG \_ FUIDEFAULT oder VARFLAG \_ FUIDEFAULT

## <a name="examples"></a>Beispiele

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IForm: IDispatch
{
    [propget]HRESULT Backcolor([out, retval] long *Value);
    [propput]HRESULT Backcolor([in] long Value);
    [propget, uidefault]HRESULT Name([out, retval] BSTR *Value);
    [propput, uidefault]HRESULT Name([in] BSTR Value);
}
[
    odl,
    dual,
    uuid(87654321-1234-1234-1234-123456789ABC),
    restricted
] 
interface IFormEvents: IDispatch
{
    [uidefault]HRESULT Click();
    HRESULT Resize();
}

[
    uuid(12345678-1234-1234-1234-987654321ABC)
]
coclass Form
{
    [default] interface IForm;
    [default, source] interface IFormEvents;
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[ODL-Dateibeispiel](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 