---
title: uidefault-Attribut
description: Das Attribut \ Uidefault \ gibt an, dass das Typinformationsmember der Standard Member für die Anzeige in der Benutzeroberfläche ist.
ms.assetid: e789be38-a509-437d-89c9-ebbc830e5ae2
keywords:
- Uidefault-Attribut-Mittel l
topic_type:
- apiref
api_name:
- uidefault
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcef39f36abad7c7cb5562b2d892761bd1bb7b5b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390171"
---
# <a name="uidefault-attribute"></a>uidefault-Attribut

Das **\[ Uidefault \]** -Attribut gibt an, dass der Typinformationsmember der Standard Member für die Anzeige in der Benutzeroberfläche ist.

``` syntax
[method-attribute-list, uidefault]return-type method-name(method-parameter-list)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Method-Attribute-List* 
</dt> <dd>

Andere Attribute, die auf die-Methode angewendet werden.

</dd> <dt>

*Rückgabetyp* 
</dt> <dd>

Der Typ der Daten, die von der Methode zurückgegeben werden, wenn Sie die Ausführung beendet.

</dd> <dt>

*Methodenname* 
</dt> <dd>

Der Name der Methode.

</dd> <dt>

*method-Parameter-List* 
</dt> <dd>

NULL oder mehr Parameter für die Methode.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie das **\[ Uidefault \]** -Attribut auf einen Member einer Schnittstelle oder eine dispinterface anwenden, wird Visual Basic zur Entwurfszeit aufgefordert, das Ereignis oder die Eigenschaft automatisch für den Benutzer anzuzeigen. Dies bedeutet Folgendes: Wenn der Benutzer auf ein Objekt doppelklickt, springt Visual Basic zum Ereignis in der standardmäßigen Quell Schnittstelle, das über das **\[ Uidefault \]** -Attribut verfügt. Wenn der Benutzer ein Objekt auswählt, zeigt der Eigenschaften Browser Visual Basic die Eigenschaft in der standardmäßigen Quell Schnittstelle an, die über dieses Attribut verfügt. Wenn kein Ereignis oder keine Eigenschaft über das **\[ Uidefault \]** -Attribut verfügt, zeigt Visual Basic das erste Ereignis oder die Eigenschaft an, das in der Standardschnittstelle aufgeführt ist.

### <a name="typeflag-representation"></a>TYPEFLAG-Darstellung

Das vorhanden sein von funcflag \_ fuidefault oder varflag \_ fuidefault

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

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 