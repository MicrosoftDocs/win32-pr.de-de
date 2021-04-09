---
title: defaultvtable-Attribut
description: Das Attribut "\ defaultvtable \" definiert eine Schnittstelle als standardmäßige Vtable-Schnittstelle.
ms.assetid: 05e50935-c630-4f9e-a7ec-3bb70a9834f1
keywords:
- defaultvtable-Attribut-Mittel l
topic_type:
- apiref
api_name:
- defaultvtable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8086d60d0936dcf56738afadea4244a5fff758b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858224"
---
# <a name="defaultvtable-attribute"></a>defaultvtable-Attribut

Das **\[ defaultvtable \]** -Attribut definiert eine Schnittstelle als standardmäßige Vtable-Schnittstelle.

``` syntax
[
    coclass-attribute-list, 
    defaultvtable
]
coclass coclass-name
{
    coclass-interface-list
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*coclass-Attribute-List* 
</dt> <dd>

Andere Attribute, die auf die-Klasse angewendet werden. Die **\[** Attribute " [**Source**](source.md) " **\]** und " **\[** [**UUID**](uuid.md) " **\]** sind erforderlich.

</dd> <dt>

*Name der Co-Klasse* 
</dt> <dd>

Der Name der Klasse.

</dd> <dt>

*coclass-Interface-List* 
</dt> <dd>

Eine Liste der Schnittstellen für die-Klasse.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Eine standardmäßige Vtable-Schnittstelle kann keine dispinterface sein – Sie muss eine Dual-oder Vtable-oder-Schnittstelle sein. Wenn die Schnittstelle eine duale Schnittstelle ist, können senken davon ausgehen, dass Sie Ereignisse über Vtable empfangen werden.

Eine Klasse kann eine standardmäßige Quell Schnittstelle und eine standardmäßige Vtable-Quell Schnittstelle sein, wie im Beispiel gezeigt. In diesem Fall sollte eine Anweisungs Senke IID \_ IDispatch verwenden, um dispatchereignisse zu empfangen und den Schnittstellen Bezeichner zum Empfangen von Vtable-Ereignissen zu verwenden.

### <a name="typeflag-representation"></a>TYPEFLAG-Darstellung

Das vorhanden sein von impltypeflag \_ fdefaultvtable.

## <a name="examples"></a>Beispiele

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IForm: IDispatch
{
    [propget] HRESULT Backcolor([out, retval] long *Value);
    [propput] HRESULT Backcolor([in] long Value);
    [propget] HRESULT Name([out, retval] BSTR *Value);
    [propput] HRESULT Name([in] BSTR Value);}

[
    dual,
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    restricted
]
interface IFormEvents: IDispatch
{
    HRESULT Click();
    HRESULT Resize();}

    [
        uuid(1e123456-1f3c-1069-996b-123456789ABC)
    ]
    coclass Form
    {
        [default] interface IForm;
        [default, defaultvtable, source] interface IFormEvents;
    }
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Ausgangs**](source.md)
</dt> <dt>

[**UUID**](uuid.md)
</dt> </dl>

 

 